<template>
  <v-main id="contacts" class="pt-10">
    <v-container >
      <v-row class="mb-5">
        <v-col cols="10" lg="7" md="9" sm="7" class="mx-auto">
          <div id="map" style="width: 100%; height:200px" class="pa-0"></div>
        </v-col>
        <v-col cols="10" lg="5" md="3" sm="5" class="mx-auto">
          <div class="pt-4">
            <div class="d-flex">
              <i class="fas fa-map-marker-alt"></i>
              <span class="font-weight-normal pl-3">Бульвар эркиндик, 35 | <span class="font-weight-bold">24/7</span> </span>
            </div>
            <div class="d-flex pt-3">
              <a href="https://www.instagram.com/bootcamp_gaming/" target="_blank">
                <i class="fab fa-instagram"></i>
              </a>
              <span class="font-weight-normal pl-3">@bootcamp_gaming</span>
            </div>
            <div class="d-flex pt-3">
              <a href="https://t.me/rn941" target="_blank">
                <i class="fab fa-telegram"></i>
              </a>
              <span class="font-weight-normal pl-3">@rnn941</span>
            </div>
            <div class="d-flex pt-3">
              <a href="https://wa.me/996555999966" target="_blank">
                <i class="fab fa-whatsapp"></i>
              </a>
              <span class="font-weight-normal pl-3">+996 555 99 99 66</span>
            </div>
          </div>
        </v-col>
      </v-row>
      <v-divider></v-divider>
      <div class="d-flex pt-7 pb-3 ">
        <v-img max-width="40" max-height="45" src="../assets/logo.png"></v-img>
        <v-toolbar-title class="ml-1 logot text-justify">Bootcamp®</v-toolbar-title>
        <v-spacer></v-spacer>
        <p class="ma-0 pa-0 mt-1">
          made with
          <i class="fas fa-heart"></i> and
          <i class="fas fa-coffee"></i>
        </p>
      </div>
    </v-container>
  </v-main>
</template>



<script>
import DG from "2gis-maps";

export default {
  data() {
    return {
      map: null,
    };
  },
  mounted() {
    (this.map = new DG.map("map", {
      center: [42.8723, 74.6072],
      zoom: 18,
      fullscreenControl: false,
      zoomControl: false,
      inertia: true,
      scrollWheelZoom: "center",
    })),
      DG.marker([42.8723, 74.6071])
        .addTo(this.map)
        .bindLabel(`Мы находимся здесь! <br/> Эркиндик бульвар, 35`, {
          static: true,
        });
  },
  beforeDestroy() {
    if (this.map) this.map.remove();
  },
};
</script>


<style scoped>
.fa-map-marker-alt {
  font-size: 30px;
  transition: 0.6s;
  color: white;
}
.fa-map-marker-alt:hover {
  transform: translate(0, -4px);
  color: #15479e;
}
.fab {
  font-size: 30px;
  transition: 0.6s;
  color: white;
}
.fab:hover {
  transform: translate(0, -4px);
}
.fa-instagram:hover {
  color: #e4405f;
}
.fa-telegram:hover {
  color: #0088cc;
}
.fa-whatsapp:hover {
  color: #25d366;
}

.fas {
  transition: 0.6s;
  color: white;
}
.fa-heart:hover {
  transform: translate(0, -4px);
  color: #c12d65;
}
.fa-coffee:hover {
  transform: translate(0, -4px);
  color: #6f4e37;
}
.instagram {
  background: url("../assets/instagram.svg");
  display: block;
  width: 30px;
  height: 30px;
}
</style>