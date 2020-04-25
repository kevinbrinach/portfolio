<template>
  <v-app >
    <toolbar id="app" />
    <v-content id="app">
      <router-view class="grey--text" style="background-color: " />
    </v-content>
    <footer-portfolio/>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Toolbar from "./components/Toolbar.vue";
import FooterPortfolio from "./components/Footer";

export default {
  name: "App",

  components: {
    HelloWorld,
    Toolbar,
    FooterPortfolio
  },

  data: () => ({
    //
  })
};
</script>

<style lang="scss">
.v-app {
   font-family: League Spartan, sans-serif !important;
    .title { // To pin point specific classes of some components
       font-family: League Spartan, sans-serif !important;
    }
 }
</style>
