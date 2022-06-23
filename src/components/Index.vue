<template>
  <div class="container">
    <section>
      <!-- <div class="bg-light">
         <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
             <div class="carousel-inner">
                 <div class="carousel-item active">
                     <img src="../assets/Caraturlas/yugi-kaiba.jpg" class="d-block w-100" alt="...">
                 </div>
                 <div class="carousel-item">
                     <img src="../assets/Caraturlas/aniversario.jpg" class="d-block w-100" alt="...">
                 </div>
             </div>
         </div>
      </div> -->
      <div class="row">
        <div class="col-lg-6">
          <p class="titulo">Yu-Gi-Oh!</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
            dictum eu purus sed eleifend. Nunc vitae justo lobortis, rutrum
            ligula vel, ornare quam. Sed dictum vestibulum orci, ac malesuada
            elit fringilla a.
          </p>
        </div>
        <div class="col-lg-6 text-center">
          <img src="../assets/Caraturlas/dragonBlanco.png" class="img-fluid" />
        </div>
      </div>
    </section>
    <section class="trio">
      <div class="row text-center">
        <div class="col-lg-4">
          <img src="../assets/Caraturlas/cartas.png" class="img-fluid cartas" alt="" />
          <h4>Duelo de Cartas</h4>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
            dictum eu purus sed eleifend.
          </p>
        </div>
        <div class="col-lg-4">
        <img src="../assets/Caraturlas/trio_yugi.png" class="img-fluid cartas" alt="" />
        <h4>Yugi - Jaden - Yusei</h4>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
            dictum eu purus sed eleifend.
          </p>
        </div>
        <div class="col-lg-4">
          <img src="../assets/Caraturlas/Tea.png" class="img-fluid cartas" alt="" />
        <h4>Tea</h4>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
            dictum eu purus sed eleifend.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.titulo {
  font-size: 80px;
  font-weight: 600;
  margin-top: 100px;
}

.trio {
  padding: 80px 0;
}
.cartas{
    width: 100px;
    margin-top: 20px;
}
</style>