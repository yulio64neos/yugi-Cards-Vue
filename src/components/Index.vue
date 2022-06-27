<template>
  <div class="container">
    <section>
      <div class="row">
        <div class="col-lg-6 text-center">
          <img class="logojap img-fluid" :src="imgBanner" />
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
            dictum eu purus sed eleifend. Nunc vitae justo lobortis, rutrum
            ligula vel, ornare quam. Sed dictum vestibulum orci, ac malesuada
            elit fringilla a.
          </p>
        </div>
        <div class="col-lg-6 text-center">
          <img :src="imgDragon" class="img-fluid" />
        </div>
      </div>
    </section>
    <section class="trio">
      <div class="row text-center">
        <div class="col-lg-4">
          <img :src="imgCartas" class="img-fluid cartas" alt="" />
          <h4>Duelo de Cartas</h4>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
            dictum eu purus sed eleifend.
          </p>
        </div>
        <div class="col-lg-4">
          <img :src="imgYugis" class="img-fluid cartas" alt="" />
          <h4>Yugi - Jaden - Yusei</h4>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
            dictum eu purus sed eleifend.
          </p>
        </div>
        <div class="col-lg-4">
          <img :src="imgTea" class="img-fluid cartas" alt="" />
          <h4>Tea</h4>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
            dictum eu purus sed eleifend.
          </p>
        </div>
      </div>
    </section>
    <section class="trio">
      <carousel-3d>
        <slide v-for="(img, i) in images" :index="i">
          <img :src="img.picture" class="img-fluid" />
        </slide>
      </carousel-3d>
    </section>
  </div>
</template>

<script>
import { Carousel3d, Slide } from "vue-carousel-3d";
export default {
  components: {
    Carousel3d,
    Slide,
  },
  data() {
    return {
      //Imagenes
      imgBanner: require("../assets/Caraturlas/logoJapan.png"),
      imgDragon: require("@/assets/Caraturlas/dragonBlanco.png"),
      imgCartas: require("@/assets/Caraturlas/cartas.png"),
      imgYugis: require("@/assets/Caraturlas/trio_yugi.png"),
      imgTea: require("@/assets/Caraturlas/Tea.png"),

      //Slides
      slides: 7,
      //Imagenes
      images:[
        {
          picture : require("@/assets/Caraturlas/bannerYugi.jpg")
        },
        {
          picture : require("@/assets/Caraturlas/aniversario.jpg")
        },
        {
          picture : require("@/assets/Caraturlas/yugi-kaiba.jpg")
        },
      ]
    };
  },

  methods: {},
};
</script>

<style lang="scss" scoped>
.logojap {
  width: 600px;
  margin-top: 50px;
  margin-bottom: 30px;
}

.trio {
  padding: 80px 0;
}
.cartas {
  width: 100px;
  margin-top: 20px;
}
</style>