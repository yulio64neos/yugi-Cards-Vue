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
      <swiper
        :slides-per-view="3"
        :space-between="30"
        :loop="false"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide
          v-for="n in 5"
          :key="n"
          class="test"
          :class="{ test_2: true }"
        >
          <div>{{ 29 + n }}</div>
          <img
            :src="getImageUrl(29 + n)"
            width="600"
            height="400"
            class="img-fluid w-100 mx-auto"
            blank="true"
          />
        </swiper-slide>
      </swiper>
      <swiper
        :slides-per-view="3"
        :space-between="30"
        loop
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide
          v-for="n in 5"
          :key="n"
          class="test"
          :class="{ test_2: true }"
        >
          <div>{{ 34 + n }}</div>
          <img
            :src="getImageUrl(34 + n)"
            width="600"
            height="400"
            class="img-fluid w-100 mx-auto"
            blank="true"
          />
        </swiper-slide>
      </swiper>

      <h2>pagination - navigation</h2>
      <swiper
        :slides-per-view="3"
        :space-between="30"
        :loop="false"
        :pagination="true"
        :navigation="true"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide
          v-for="n in 5"
          :key="n"
          class="test"
          :class="{ test_2: true }"
        >
          <div>{{ 34 + n }}</div>
          <img
            :src="getImageUrl(34 + n)"
            width="600"
            height="400"
            class="img-fluid w-100 mx-auto"
            blank="true"
          />
        </swiper-slide>
      </swiper>
    </section>
  </div>
</template>

<script>
import { Navigation, Pagination } from "swiper";
import { SwiperCore, Swiper, SwiperSlide } from "swiper-vue2";
import "swiper/swiper-bundle.css";
SwiperCore.use([Navigation, Pagination]);
export default {
  data() {
    return {
      //Imagenes
      imgBanner: require("../assets/Caraturlas/logoJapan.png"),
      imgDragon: require("@/assets/Caraturlas/dragonBlanco.png"),
      imgCartas: require("@/assets/Caraturlas/cartas.png"),
      imgYugis: require("@/assets/Caraturlas/trio_yugi.png"),
      imgTea: require("@/assets/Caraturlas/Tea.png"),
    };
  },

  components: {
    Swiper,
    SwiperSlide,
  },
  methods: {
    getImageUrl(imageId) {
      return `https://picsum.photos/600/400/?image=${imageId}`;
    },
    onSwiper(swiper) {
      console.log(swiper);
    },
    onSlideChange() {
      console.log("slide change");
    },
  },
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

.img-fluid {
  max-width: 100%;
  height: auto;
}
.w-100 {
  width: 100%;
}
.ml-auto,
.mx-auto {
  margin-left: auto;
}
.mr-auto,
.mx-auto {
  margin-right: auto;
}
</style>