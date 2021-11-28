<template>
  <Header logo="MeuFreela" />
  <Main />
  <Footer devHall="DevHall" />
</template>

<script>
// Tá perdido por aqui maldito? kkk
import "./assets/styles/main.css";
import Header from "./components/header/index.vue";
import Main from "./components/main/index.vue";
import Footer from "./components/footer/index.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
};
</script>
