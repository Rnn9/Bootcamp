<template>
  <v-carousel
    cycle
    interval="4000"
    :show-arrows="false"
    id="carousel"
    delimiter-icon="mdi-minus"
    hide-delimiter-background
    class="mt-10"
  >
    <v-carousel-item>
      <!-- <v-img src="../assets/width.png"></v-img> -->
    </v-carousel-item>
    <v-carousel-item>
      <!-- <v-img src="../assets/width.png"></v-img> -->
    </v-carousel-item>
    <v-carousel-item>
      <!-- <v-img src="../assets/width.png"></v-img> -->
    </v-carousel-item>
    <v-carousel-item>
      <!-- <v-img src="../assets/width.png"></v-img> -->
    </v-carousel-item>
  </v-carousel>
</template>


<script>
export default {
  data() {
    return {
      image: "../assets/setup.jpg",
    };
  },
};
</script>