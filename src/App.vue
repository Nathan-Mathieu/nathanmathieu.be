<template>
    <div id="app">
        <!-- <header>
            <div class="title animate__animated animate__fadeInUp">nathanmathieu.be</div>
        </header> -->
        <presentation></presentation>
        <infos></infos>
        <competences></competences>
        <projets></projets>
    </div>
</template>

<script>
import Presentation from "./components/Presentation/Presentation.vue";
import Infos from "./components/Infos/Infos.vue";
import Competences from "./components/Competences/Competences.vue";
import Projets from "./components/Projets/Projets.vue";

export default {
    name: "App",
    components: {
        Presentation,
        Infos,
        Competences,
        Projets,
    },
};
</script>

<style>
@import "./style.css";
</style>
