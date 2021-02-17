<template>
    <div class="infos compo">
        <div class="container">
            <div class="infos-block">
                <div  class="animate__animated animate__fadeIn">
                    <div class="btns">
                        <button @click="switchTab('contact')" :class="{ active: contact }">Contact</button>
                        <button @click="switchTab('parcours')" :class="{ active: parcours }">Parcours Scolaire</button>
                        <button @click="switchTab('experience')" :class="{ active: experience }">Expérience</button>
                    </div>
                    <div class="displayCurrentTab">
                        <div v-if="contact" class="contact tab">
                            <div class="contact-elem">
                                <div class="icon-user"><i class="fas fa-user"></i></div>
                                <div>Nathan Mathieu <br />né le 26-06-1997</div>
                            </div>

                            <div class="contact-elem">
                                <i class="fas fa-phone-alt"></i>
                                +32 474 57 48 94
                            </div>

                            <div class="contact-elem ">
                                <i class="fas fa-envelope"></i>
                                <div>nathan.mathieu <img src="../../assets/img/at.svg" /> gmail.com</div>
                            </div>

                            <div class="contact-elem">
                                <i class="fas fa-home"></i>
                                <div>6750<br />P. Luxembourg<br />Belgique</div>
                            </div>
                        </div>

                        <div v-if="parcours" class="parcours tab">
                            <div class="contact-item-elem">
                                <div class="contact-item-annee">En cours</div>
                                <div class="contact-item-text">Web Design IEPSA à Arlon + formation web Dyma</div>
                            </div>

                            <div class="contact-item-elem">
                                <div class="contact-item-annee">2019</div>
                                <div class="contact-item-text">Formation Algorithmes TECHNOBEL</div>
                            </div>

                            <div class="contact-item-elem">
                                <div class="contact-item-annee">2016 - 2017</div>
                                <div class="contact-item-text">Informatique de gestion, IESN de Namur</div>
                            </div>

                            <div class="contact-item-elem">
                                <div class="contact-item-annee">2015 - 2016</div>
                                <div class="contact-item-text">Faculté d’informatique de Namur</div>
                            </div>

                            <div class="contact-item-elem">
                                <div class="contact-item-annee">2014 - 2015</div>
                                <div class="contact-item-text">Obtention du CESS au CNDB de Virton</div>
                            </div>
                        </div>

                        <div v-if="experience" class="experience tab">
                            <div class="contact-item-elem">
                                <div class="contact-item-annee">2018</div>
                                <div class="contact-item-text">Administrateur de systèmes d'information au CPAS de Virton & MRS «l’Amitié»</div>
                            </div>

                            <div class="contact-item-elem">
                                <div class="contact-item-annee">2016</div>
                                <div class="contact-item-text">Travail d'étudiant en réception et gestion des marchandises au Cora de Messancy</div>
                            </div>

                            <div class="contact-item-elem">
                                <div class="contact-item-annee">2014 - 2015 - 2017 :</div>
                                <div class="contact-item-text">Travail d'étudiant au Cora de Messancy</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Infos",
    data() {
        return {
            contact: true,
            parcours: false,
            experience: false,
            isInfosDisplayed: false,
        };
    },
    methods: {
        switchTab(tab) {
            this.contact = false;
            this.parcours = false;
            this.experience = false;
            if (tab == "contact") {
                this.contact = true;
            } else if (tab == "parcours") {
                this.parcours = true;
            } else {
                this.experience = true;
            }
        },
    },
    created() {
        window.addEventListener("scroll", () => {
            let scrolled = window.scrollY;
            if (scrolled > 700) {
                this.isInfosDisplayed = true;
            }
        });
    },
};
</script>

<style scoped>
@import "./Infos.css";
</style>
