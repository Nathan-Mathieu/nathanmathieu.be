<template>
    <div class="competences compo">
        <div class="container">

            <div class="container-title">Languages, frameworks & CMS</div>

            <div class="hr"></div>

            <div class="languages">
                <div class="language-block" v-show="isLanguagesDisplayed">
                    <img class="icon animate__animated animate__fadeInLeft" src="../../assets/img/competences/icons/html.svg" alt="html" />
                    <img class="icon animate__animated animate__fadeIn" src="../../assets/img/competences/icons/css.svg" alt="css" />
                    <img class="icon animate__animated animate__fadeInRight" src="../../assets/img/competences/icons/javascript.svg" alt="javascript" />
                </div>

                <div class="language-block" v-show="isLanguagesDisplayed">
                    <img class="icon animate__animated animate__fadeInLeft" src="../../assets/img/competences/icons/vuejs.svg" alt="vuejs" />
                    <img class="icon animate__animated animate__fadeIn" src="../../assets/img/competences/icons/wordpress.svg" alt="wordpress" />
                    <img class="icon animate__animated animate__fadeInRight" src="../../assets/img/competences/icons/joomla.png" alt="joomla" />
                </div>
                <div class="language-block" v-show="isLanguagesDisplayed">
                    <img class="icon animate__animated animate__fadeInLeft" src="../../assets/img/competences/icons/bootstrap.svg" alt="bootstrap" />
                    <img class="icon animate__animated animate__fadeIn" src="../../assets/img/competences/icons/sass.svg" alt="sass" />
                    <img class="icon animate__animated animate__fadeInRight" src="../../assets/img/competences/icons/webpack.svg" alt="webpack" />
                </div>
            </div>

            <div class="margin-v"></div>

            <div class="container-title">En Cours d'apprentissage {{ load }}</div>
            <div class="hr"></div>
            <div class="encours">
                <div class="encours-line" v-show="isEnCoursDisplayed">
                    <img src="../../assets/img/competences/icons/vuejs.svg" alt="vuejs" class=" animate__animated animate__fadeInLeft"/>
                    <img src="../../assets/img/competences/icons/sass.svg" alt="sass" class="animate__animated animate__fadeIn"/>
                    <img src="../../assets/img/competences/icons/bootstrap.svg" alt="bootstrap" class="animate__animated animate__fadeIn"/>
                    <img src="../../assets/img/competences/icons/php.svg" alt="php" class="animate__animated animate__fadeInRight"/>
                </div>
                <div class="encours-line" v-show="isEnCoursDisplayed">
                    <img src="../../assets/img/competences/icons/wordpress.svg" alt="wordpress" class=" animate__animated animate__fadeInLeft"/>
                    <img src="../../assets/img/competences/icons/nodejs.svg" alt="nodejs" class="animate__animated animate__fadeIn"/>
                    <img src="../../assets/img/competences/icons/docker.svg" alt="docker" class="animate__animated animate__fadeInRight"/>
                </div>
            </div>

            <div class="margin-v"></div>

            <div class="container-title">Outils</div>
            <div class="hr"></div>
            <div class="outils">
                <div class="encours-line" v-show="isOutilsDisplayed">
                    <img src="../../assets/img/competences/icons/vscode.svg" alt="vscode" class=" animate__animated animate__fadeInLeft"/>
                    <img src="../../assets/img/competences/icons/photoshop.svg" alt="photoshop" class="animate__animated animate__fadeIn"/>
                    <img src="../../assets/img/competences/icons/illustrator.svg" alt="illustrator" class="animate__animated animate__fadeIn"/>
                    <img src="../../assets/img/competences/icons/github.svg" alt="github" class="animate__animated animate__fadeInRight"/>
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
            isLanguagesDisplayed: false,
            isEnCoursDisplayed: false,
            isOutilsDisplayed: false,
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
        displayImg() {},
    },
    created() {
        this.loading();

        window.addEventListener("scroll", () => {
            let scrolled = window.scrollY;
            if (scrolled > 1500) {
                this.isLanguagesDisplayed = true;
            }
            if(scrolled > 1800){
                this.isEnCoursDisplayed = true;
            }
            if(scrolled > 2100){
                this.isOutilsDisplayed = true;
            }
        });
    },
};
</script>

<style scoped>
@import "./Competences.css";
</style>
