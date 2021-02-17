<template>
  <div id="app">
    <header>
      <div class="animate__animated animate__bounceInRight">nathanmathieu.be</div>
    </header>

    <div id="content">
      <section>
        <infos></infos>
        <competences></competences>
        <projets></projets>
      </section>

      <aside>
        <presentation></presentation>
      </aside>
    </div>

    <div id="responsive-content">
      <presentation></presentation>
      <infos></infos>
      <competences></competences>
      <projets></projets>
    </div>

    <div class="progress-container">
      <div class="progress-bar" id="myBar" v-bind:style="{ width: progressWidth + '%' }"></div>
    </div>

    <footer>
      © Nathan Mathieu 2021
    </footer>
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
  data() {
    return {
      progressWidth: 0,
    };
  },
  created() {
    window.addEventListener("scroll", () => {
      this.progress();
    });
  },
  methods: {
    progress() {
      let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
      let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
      let scrolled = (winScroll / height) * 100;
      this.progressWidth = scrolled;
    },
  },
};
</script>

<style>
@import "./style.css";
</style>
