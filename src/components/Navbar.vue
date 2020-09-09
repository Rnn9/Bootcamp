<template>
  <v-app-bar color="black" absolute height="70px">
    <v-img max-width="33" max-height="45" class="ml-2 ml-sm-4 ml-md-7" src="../assets/logo.svg"></v-img>
    <v-toolbar-title class="ml-1 logot">Bootcamp</v-toolbar-title>

    <v-spacer></v-spacer>

    <div class="d-flex menu_list">
      <a
        class="font-weight-medium ml-3 ma-0 link white--text"
        @click="$vuetify.goTo('#about', options)"
      >О нас</a>
      <a
        class="font-weight-medium ml-3 ma-0 link white--text"
        @click="$vuetify.goTo('#price', options)"
      >Конфигурация | Цены</a>
      <a
        class="font-weight-medium ml-3 ma-0 link white--text"
        @click="$vuetify.goTo('#carousel', options)"
      >Галерея</a>
      <a
        class="font-weight-medium ml-3 ma-0 link white--text"
        @click="$vuetify.goTo('#contacts', options)"
      >Контакты</a>
    </div>

    <v-btn dark @click="sheet = !sheet" class="ml-3 menu_button">
      <i class="fas fa-bars"></i>
    </v-btn>

    <v-bottom-sheet v-model="sheet">
      <v-sheet class="d-flex justify-center">
        <v-list>
          <v-list-item @click="sheet = false">
            <v-list-item-avatar>
              <v-avatar size="32px" tile>
                <i class="fas fa-stream"></i>
              </v-avatar>
            </v-list-item-avatar>
            <v-list-item-title>О нас</v-list-item-title>
          </v-list-item>

          <v-list-item @click="sheet = false">
            <v-list-item-avatar>
              <v-avatar size="32px" tile>
                <i class="fas fa-desktop"></i>
              </v-avatar>
            </v-list-item-avatar>
            <v-list-item-title>Конфигурация | Цены</v-list-item-title>
          </v-list-item>
          <v-list-item @click="sheet = false">
            <v-list-item-avatar>
              <v-avatar size="32px" tile>
                <i class="fas fa-images"></i>
              </v-avatar>
            </v-list-item-avatar>
            <v-list-item-title>Галерея</v-list-item-title>
          </v-list-item>
          <v-list-item @click="sheet = false">
            <v-list-item-avatar>
              <v-avatar size="32px" tile>
                <i class="fas fa-map-marker-alt"></i>
              </v-avatar>
            </v-list-item-avatar>
            <v-list-item-title>Контакты</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-sheet>
    </v-bottom-sheet>
  </v-app-bar>
</template>





// @click="$vuetify.goTo('#about', options)"

<script>
export default {
  data: () => ({
    sheet: false,
  }),
  computed: {
    options() {
      return {
        duration: 1200,
        offset: 0,
        easing: "easeInOutCubic",
      };
    },
  },
};
</script>

<style scoped>
.menu_button {
  display: none;
}

.link::after {
  content: "";
  display: block;
  width: 0;
  height: 2px;
  background: #fff;
  transition: width 0.3s;
}
.link:hover::after {
  width: 100%;
  transition: width 0.3s;
}
@media only screen and (max-width: 700px) {
  .menu_button {
    display: block;
  }
  .menu_list a {
    display: none;
  }
}
</style>