<template>
    <div class="competences compo">
        <div class="container">
            <div class="container-title">Languages, frameworks & CMS</div>
            <div class="hr"></div>
            <div class="language-block">
                <img class="icon" src="../../assets/img/competences/icons/html.svg" alt="html" />
                <p>:</p>
                <div class="circles-block">
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/half_circle.svg" />
                </div>
            </div>
            <div class="language-block">
                <img class="icon" src="../../assets/img/competences/icons/css.svg" alt="css" />
                <p>:</p>
                <div class="circles-block">
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/half_circle.svg" />
                </div>
            </div>
            <div class="language-block">
                <img class="icon" src="../../assets/img/competences/icons/javascript.svg" alt="javascript" />
                <p>:</p>
                <div class="circles-block">
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/half_circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                </div>
            </div>
            <div class="language-block">
                <img class="icon" src="../../assets/img/competences/icons/joomla.png" alt="joomla" />
                <p>:</p>
                <div class="circles-block">
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/half_circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                </div>
            </div>
            <div class="language-block">
                <img class="icon" src="../../assets/img/competences/icons/wordpress.svg" alt="wordpress" />
                <p>:</p>
                <div class="circles-block">
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/half_circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                </div>
            </div>
            <div class="language-block">
                <img class="icon" src="../../assets/img/competences/icons/vuejs.svg" alt="vuejs" />
                <p>:</p>
                <div class="circles-block">
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/half_circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                </div>
            </div>
            <div class="language-block">
                <img class="icon" src="../../assets/img/competences/icons/bootstrap.svg" alt="bootstrap" />
                <p>:</p>
                <div class="circles-block">
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                </div>
            </div>
            <div class="language-block">
                <img class="icon" src="../../assets/img/competences/icons/sass.svg" alt="sass" />
                <p>:</p>
                <div class="circles-block">
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                    <img src="../../assets/img/competences/empty_circle.svg" />
                </div>
            </div>

            <div class="margin-v"></div>

            <div class="container-title">En Cours d'apprentissage {{ load }}</div>
            <div class="hr"></div>
            <div class="encours">
                <div class="encours-line">
                    <img src="../../assets/img/competences/icons/vuejs.svg" alt="vuejs" />
                    <img src="../../assets/img/competences/icons/sass.svg" alt="sass" />
                    <img src="../../assets/img/competences/icons/bootstrap.svg" alt="bootstrap" />
                    <img src="../../assets/img/competences/icons/php.svg" alt="php" />
                </div>
                <div class="encours-line">
                    <img src="../../assets/img/competences/icons/wordpress.svg" alt="wordpress" />
                    <img src="../../assets/img/competences/icons/nodejs.svg" alt="nodejs" />
                    <img src="../../assets/img/competences/icons/docker.svg" alt="docker" />
                </div>
            </div>

            <div class="margin-v"></div>

            <div class="container-title">Outils</div>
            <div class="hr"></div>
            <div class="encours">
                <div class="encours-line">
                    <img src="../../assets/img/competences/icons/vscode.svg" alt="vscode" />
                    <img src="../../assets/img/competences/icons/photoshop.svg" alt="photoshop" />
                    <img src="../../assets/img/competences/icons/illustrator.svg" alt="illustrator" />
                    <img src="../../assets/img/competences/icons/github.svg" alt="github" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Competences",
    data() {
        return {
            load_elems: ["/", "-", "\\"],
            load: "",
            i: 0,
        };
    },
    methods: {
        loading() {
            setInterval(() => {
                if (this.i < 2) {
                    this.i++;
                } else {
                    this.i = 0;
                }
                this.load = this.load_elems[this.i];
            }, 300);
        },
        displayImg() {
            let scrolled = window.scrollY;

            if (scrolled > 250) {
                console.log(scrolled);
            }
        },
    },
    created() {
        this.loading();
    },
};
</script>

<style scoped>
@import "./Competences.css";
</style>
