<template>
  <v-main id="about">
    <v-container>
      <v-row align="center" class="mt-7 mb-7">
        <v-col cols="12 text-center">
          <h1 class="font-weight-bold about_section_title">Высокая производительность</h1>
        </v-col>
      </v-row>
      <v-row>
        <v-col lg="8" md="7" sm="8" cols="12" class="mx-sm-auto mx-auto">
          <v-img src="../assets/fps.gif" class="rounded-r-xl rounded-sm mt-md-8 mt-lg-0" max-height="430px" max-width="766"></v-img>
        </v-col>
        <v-col lg="4" md="5" sm="8" cols="11" class="mx-sm-auto mx-auto">
          <div>
            <h1 class="font-weight-bold text-sm-center text-md-start text-lg-start text-center about_section_subheader">
              <ICountUp :delay="delay" :endVal="hz" :options="options2" @ready="hzDisplay" />hz | FPS
              <ICountUp :delay="delay" :endVal="endVal" :options="options" @ready="onReady" />
            </h1>
            <p class="font-weight-light mt-3">
              Frames Per Second
              – количество изображений, отображающихся на экране за указанную единицу времени.
              <br />Чем выше значение FPS – тем больше кадров отображается на дисплее.
              Игра становится быстрой, отзывчивой и приятной.
              FPS в CS:GO и шутерах играет важнейшую роль,
              поскольку геймплей предполагает
              точное попадание по вражеским моделям и с
              низкой частотой кадров эта задача существенно усложняется.
              <br />Наши компьютеры поддерживают максимальный FPS для комфортной игры в любых играх
            </p>
          </div>
        </v-col>
      </v-row>
      <v-row class="mb-16 mt-sm-5 mt-md-8 mt-lg-16">
        <v-col lg="4" md="5" sm="8" cols="11" class="mx-sm-auto mx-auto">
          <h1 class="font-weight-bold text-sm-center text-md-start text-lg-start text-center about_section_subheader">Комфорт</h1>
          <p class="font-weight-light mt-3">
            Frames Per Second
            – количество изображений, отображающихся на экране за указанную единицу времени.
            <br />Чем выше значение FPS – тем больше кадров отображается на дисплее.
            Игра становится быстрой, отзывчивой и приятной.
            FPS в CS:GO и шутерах играет важнейшую роль,
            поскольку геймплей предполагает
            точное попадание по вражеским моделям и с
            низкой частотой кадров эта задача существенно усложняется.
            <br />Наши компьютеры поддерживают максимальный FPS для комфортной игры в любых играх
          </p>
        </v-col>
        <v-col cols="12" lg="8" md="7" sm="8" class="mx-sm-auto mt-md-8 mx-auto">
          <v-img src="../assets/desk.jpg" class="rounded-l-xl rounded-sm mt-md-8 mt-lg-0" max-height="430px" max-width="766"></v-img>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>


<script>
import ICountUp from "vue-countup-v2";
export default {
  components: {
    ICountUp,
  },
  data() {
    return {
      delay: 1000,
      hz: 240,
      options2: {
        useEasing: true,
        useGrouping: true,
        separator: ",",
        decimal: ".",
        prefix: "",
        suffix: "",
        startVal: "144",
        duration: 2,
      },
      endVal: Math.floor(Math.random() * (320 - 200) + 200),
      options: {
        useEasing: true,
        useGrouping: true,
        separator: ",",
        decimal: ".",
        prefix: "",
        suffix: "",
        startVal: "0",
        duration: 1,
      },
    };
  },
  methods: {
    onReady: function (instance) {
      setInterval(() => {
        instance.start(
          (this.endVal = Math.floor(Math.random() * (320 - 200) + 200))
        );
      }, 500);
    },
    hzDisplay: function (instance) {
      setTimeout(() => {
        if (this.hz == 144) {
        instance.update(this.hz = 240);
      } else {
        instance.update(this.hz = 144);
      }
      }, 7000 );
    },
  },
};
</script>

<style  scoped>
.about_section_title {
  font-size: 40px;
}
@media only screen and (max-width: 700px) {
  .about_section_title {
    font-size: 35px;
  }
  .about_section_subheader {
    font-size: 30px;
  }
}
@media only screen and (max-width: 600px) {
  .about_section_title {
    font-size: 30px;
  }
  .about_section_subheader {
    font-size: 25px;
  }
}

</style>