<template>
    <div class="projets compo">
        <div class="container">
            <div class="container-title">Certaines de mes intégrations :</div>
            <div class="hr"></div>
            <div class="all-integrations">
                <div v-show="isProjectsDisplayed" class="animate__animated animate__fadeInRight">
                    <div class="integration-block ">
                        <a href="https://solidarite4810.be" target="_blank">
                            <img src="../../assets/img/integrations/s4810.png" alt="Solidarité 4810" />
                            <div class="integration-block-title">solidarite4810.be</div>
                        </a>
                    </div>

                    <div class="integration-block">
                        <a href="https://cranky-shannon-0449d6.netlify.app/" target="_blank">
                            <img src="../../assets/img/integrations/simon.png" />
                            <div class="integration-block-title">Jeu du Simon</div>
                        </a>
                    </div>

                    <div class="integration-block ">
                        <a href="https://fervent-hopper-18b8b7.netlify.app/" target="_blank">
                            <img src="../../assets/img/integrations/password.png" />
                            <div class="integration-block-title">Password Generator</div>
                        </a>
                    </div>

                    <div class="integration-block ">
                        <a href="https://goofy-curie-e8f2b9.netlify.app/" target="_blank">
                            <img src="../../assets/img/integrations/meteo.png" />
                            <div class="integration-block-title">App Météo</div>
                        </a>
                    </div>

                    <div class="integration-block ">
                        <a href="https://affectionate-mestorf-bac324.netlify.app/" target="_blank">
                            <img src="../../assets/img/integrations/color.png" />
                            <div class="integration-block-title">Color Picker</div>
                        </a>
                    </div>

                    <div class="integration-block ">
                        <a href="https://objective-varahamihira-fb67b2.netlify.app/" target="_blank">
                            <img src="../../assets/img/integrations/todo.png" />
                            <div class="integration-block-title">To do List</div>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Projets",
    data() {
        return {
            isProjectsDisplayed: false,
        };
    },
    created() {
        window.addEventListener("scroll", () => {
            let scrolled = window.scrollY;
            if (scrolled > 2800) {
                this.isProjectsDisplayed = true;
            }
        });
    },
};
</script>

<style>
@import "./Projets.css";
</style>
