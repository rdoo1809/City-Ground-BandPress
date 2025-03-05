<script setup>
import HeroImage from "./HeroImage.vue";
import HeroMack from "/public/images/hero-mack.jpeg";
import HeroAdam from "/public/images/hero-adam.jpeg";
import HeroLiam from "/public/images/hero-liam.jpeg";
import HeroNolan from "/public/images/hero-nolan.jpeg";
</script>

<template>
  <div class="container">
    <HeroImage :image-src="HeroMack" />
    <HeroImage :image-src="HeroAdam" />
    <HeroImage :image-src="HeroLiam" />
    <HeroImage :image-src="HeroNolan" />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  width: 100vw;
}
</style>
