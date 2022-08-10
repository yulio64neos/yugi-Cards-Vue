<template>
  <div id="app">
    <Navbar/>
    <router-view/>
    <Footer_inf/>
  </div>
</template>

<script>
import Navbar from '../src/components/Navbar.vue'
import Footer_inf from './components/Footer_inf.vue'
export default{
  components:{
    Navbar,
    Footer_inf
  }
}
</script>

<style>
@font-face {
  font-family: "Lora";
  src: local("Lora"), url(./fonts/Lora/Lora-Italic-VariableFont_wght.ttf) format("truetype");
}
#app {
  font-family: "Lora";
}
</style>
