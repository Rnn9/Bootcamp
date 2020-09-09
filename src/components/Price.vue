<template>
  <v-main id="price">
    <v-container>
      <v-row align="center">
        <v-col cols="12 text-center">
          <h1 class="font-weight-bold pricing pricing_section_title">Конфигурация | Цены</h1>
        </v-col>
      </v-row>

      <v-tabs centered v-model="tab" background-color="transparent" color="white">
        <v-tab>
          <span class="font-weight-normal text--primary" style="font-size: 12px">Стандарт зал</span>
        </v-tab>
        <v-tab>
          <span class="font-weight-normal text--primary" style="font-size: 12px">VIP зал</span>
        </v-tab>
        <v-tabs-items
          v-model="tab"
          class="rounded-lg mt-10 price_tab"
          style="opacity: 0.9"
          continuous
        >
          <v-tab-item class="price_tab rounded-lg">
            <v-row>
              <v-col class="d-flex justify-center mt-0 mt-sm-3 mt-md-5 mt-lg-7 mx-auto" cols="10" sm="6" md="6" lg="6">
                <div>
                  <h1 class="font-weight-bold text-center">Железо</h1>
                  <div>
                    <v-card-text class="pa-5">
                      <p>
                        <span class="font-weight-bold">Видеокарта</span>: GTX 1070 Ti
                      </p>
                      <p>
                        <span class="font-weight-bold">Процессор</span>: Intel Core i5 8500
                      </p>
                      <p>
                        <span class="font-weight-bold">Оперативная память</span>: Corsair 16 GB
                      </p>
                      <p>
                        <span class="font-weight-bold">SSD</span>: Samsung Evo 860 250GB
                      </p>
                    </v-card-text>
                  </div>
                  <h1 class="font-weight-bold text-center">Переферия</h1>
                  <v-card-text class="pa-5">
                    <p>
                      <span class="font-weight-bold">Монитор</span>: BenQ 2411p 144hz
                    </p>
                    <p>
                      <span class="font-weight-bold">Мышка</span>: Zowie ec-1 a
                    </p>
                    <p>
                      <span class="font-weight-bold">Наушники</span>: HyperX Stinger
                    </p>
                  </v-card-text>
                </div>
              </v-col>
              <v-col class="d-flex justify-center mt-0 mt-sm-3 mt-md-5 mt-lg-7 mx-auto" cols="10" sm="6" md="6" lg="6">
                <div>
                  <h1 class="font-weight-bold text-center">Цены</h1>
                  <div>
                    <v-card-text class="pa-5">
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">1</span> час: 50 сом
                      </p>
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">3</span> часа: 100 сом
                      </p>
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">5</span> часов: 150 сом
                      </p>
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">7</span> часов: 220 сом
                      </p>
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">Ночь</span>: 200 сом
                      </p>
                    </v-card-text>
                  </div>
                </div>
              </v-col>
            </v-row>
          </v-tab-item>
          <v-tab-item class="price_tab rounded-lg">
            <v-row>
              <v-col class="d-flex justify-center mt-7">
                <div>
                  <h1 class="font-weight-bold text-center">Железо</h1>
                  <div>
                    <v-card-text class="pa-5">
                      <p>
                        <span class="font-weight-bold">Видеокарта</span>: GTX 1070 Ti
                      </p>
                      <p>
                        <span class="font-weight-bold">Процессор</span>: Intel Core i5 8500
                      </p>
                      <p>
                        <span class="font-weight-bold">Оперативная память</span>: Corsair 16 GB
                      </p>
                      <p>
                        <span class="font-weight-bold">SSD</span>: Samsung Evo 860 250GB
                      </p>
                    </v-card-text>
                  </div>
                  <h1 class="font-weight-bold text-center">Переферия</h1>
                  <v-card-text class="pa-5">
                    <p>
                      <span class="font-weight-bold">Монитор</span>: BenQ 2411p 144hz
                    </p>
                    <p>
                      <span class="font-weight-bold">Мышка</span>: Zowie ec-1 a
                    </p>
                    <p>
                      <span class="font-weight-bold">Наушники</span>: HyperX Stinger
                    </p>
                  </v-card-text>
                </div>
              </v-col>
              <v-col class="d-flex justify-center mt-7">
                <div>
                  <h1 class="font-weight-bold text-center">Цены</h1>
                  <div>
                    <v-card-text class="pa-5text-center">
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">1</span> час: 50 сом
                      </p>
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">3</span> часа: 100 сом
                      </p>
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">5</span> часов: 150 сом
                      </p>
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">7</span> часов: 220 сом
                      </p>
                      <p>
                        <span class="font-weight-bold" style="font-size: 18px">Ночь</span>: 200 сом
                      </p>
                    </v-card-text>
                  </div>
                </div>
              </v-col>
            </v-row>
          </v-tab-item>
        </v-tabs-items>
      </v-tabs>
    </v-container>
  </v-main>
</template>


<script>
export default {
  data: () => ({
    isActive: false,
    tab: null,
  }),
};
</script>


<style scoped>
.pricing_section_title {
  font-size: 40px;
}
.pricing {
  font-family: "Raleway", sans-serif;
}
@media only screen and (max-width: 700px) {
  .pricing_section_title {
    font-size: 30px;
  }
}
@media only screen and (max-width: 600px) {
  .pricing_section_title {
    font-size: 25px;
  }
}
</style>

