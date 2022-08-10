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
          <qr-code 
            text="https://goo.gl/9eIWP9"
            size="60"
            color="#f1c40f"
            bg-color="#3498db" 
            error-level="L">
        </qr-code>
        </div>
        <div class="col-lg-6 text-center">
          <img :src="imgDragon" class="img-fluid" />
        </div>
      </div>
    </section>

    <section class="trio">
      <div class="row text-center">
        <div class="col-lg-4" v-for="(item, i) in trioDiv" :index="i">
          <img :src="item.images" class="img-fluid cartas" alt="" />
          <h4>{{item.personaje}}</h4>
          <p>
            {{item.descripcion}}
          </p>
        </div>
      </div>
    </section>

    <section class="trio">
      <p class="fs-1 Gal">Galería</p>
      <carousel-3d class="">
        <slide v-for="(img, i) in pictures" :index="i">
          <img :src="require('@/assets/Caraturlas/' + img)" class="img-fluid cardsCar" />
        </slide>
      </carousel-3d>
    </section>

    <section>
      <div class="row text-center">
        <img :src="imgBannerDragon" class="img-fluid"/>
        <h1>Leyendas</h1>
      </div>
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
      imgBannerDragon: require("@/assets/Caraturlas/robot2.png"),

      //Slides
      slides: 7,
      //Imagenes
      pictures: [
        "bannerYugi.jpg",
        "aniversario.jpg",
        "yugi-kaiba.jpg"
      ],
      trioDiv:[
        {
          personaje : 'Tea',
          descripcion : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Done dictum eu purus sed eleifend.',
          images : require("@/assets/Caraturlas/cartas.png"),
        },
        {
          personaje : 'Yugi - Jaden - Yusei',
          descripcion : 'Aliquam nec diam fermentum lectus aliquet placerat mollis tincidunt enim. Donec quis ligula ac ex ultrices ullamcorper. Quisque a turpis non urna ultrices mattis et vitae metus.',
          images: require("@/assets/Caraturlas/trio_yugi.png"),
        },
        {
          personaje : 'Tea',
          descripcion : 'Ut placerat, nisl ut blandit pellentesque, mi odio consectetur erat, vitae accumsan ex lacus sed ante. Morbi congue sapien ac nisi aliquet, sed pulvinar eros tempus..',
          images: require("@/assets/Caraturlas/Tea.png"),
        }
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

.Gal{
  font-size: 60px;
}
.cardsCar{
  width: 470px;
  height: 270px;
}
.cardsCar:hover{
  transform: scale(1.5);
}
</style>