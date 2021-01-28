<template>
    <div class="presentation compo">
        <div class="container ">
            <div class="container-presentation">
                <img src="../../assets/img/Nath.jpg" class="img-nathan" />

                <div class="presentation-list">
                    <ul>
                        <li>Nathan Mathieu</li>
                        <li>23 ans</li>
                        <li>Etudiant en web design</li>
                    </ul>
                </div>
            </div>
            <div class="hr"></div>

            <div class="presentation-text">
                <p>
                    Je m'appelle Nathan Mathieu, j'ai 23 ans et je recherche un stage dans le développement web orienté font-end. <br /><br />
                    Je suis actuellement étudiant à l'IEPS d'Arlon en section Web Design et je suis la formation proposé par Dyma.fr.
                </p>
            </div>

            <div class="hr"></div>

            <div class="container-title">Liens :</div>

            <div class="liens">
                <a :href="`${publicPath}./files/Nathan_Mathieu_CV.pdf`" target="_blank">
                    <div>
                        <img src="../../assets/img/pdf.svg" />
                    </div>
                    <p>Le CV au format pdf</p>
                </a>
            </div>

            <div class="liens">
                <a href="https://dyma.fr/developer/5e9b29c210ce791920221195" target="_blank">
                    <div>
                        <img src="../../assets/img/dyma.svg" />
                    </div>
                    <p>Mon profil Dyma</p>
                </a>
            </div>

            <div class="liens">
                <a href="https://github.com/Nathan-Mathieu" target="_blank">
                    <div>
                        <img src="../../assets/img/competences/icons/github.svg" />
                    </div>
                    <p>Mon profil Github</p>
                </a>
            </div>

            <div class="liens">
                <a href="https://solidarite4810.be" target="_blank">
                    <div>
                        <img src="../../assets/img/s4810.svg" />
                    </div>
                    <p>Solidarité 4810</p>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Presentation",
    data() {
        return {
            publicPath: process.env.BASE_URL,
        };
    },
};
</script>

<style scoped>
@import "./Presentation.css";
</style>
