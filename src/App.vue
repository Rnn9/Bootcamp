<template>
  <div>
    <v-app>
      <navbar />
      <parallax />
      <about />
      <price />
      <carousel />
      <Map />
    </v-app>
  </div>
</template>


<script>
import Navbar from "./components/Navbar.vue";
import Carousel from './components/Carousel.vue';
import Parallax from "./components/Parallax.vue";
import About from "./components/About";
import Price from "./components/Price";
import Map from "./components/Map";

export default {
  name: "App",

  components: {
    Navbar,
    Carousel,
    Parallax,
    About,
    Price,
    Map,
  },

  data: () => ({
    //
  }),
};
</script>


<style scoped>
@import "./assets/styles/main.css";
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@300;400;700&display=swap');
@font-face {
  font-family: 'Raleway', sans-serif;;
  src: local('Raleway');
}
#app {
  font-family: 'Raleway';
}
</style>

