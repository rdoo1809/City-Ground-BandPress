<script setup>
import HeroImage from "./HeroImage.vue";
import HeroMack from "/public/images/hero-mack.jpeg";
import HeroAdam from "/public/images/hero-adam.jpeg";
</script>

<template>
  <div class="container">
    <HeroImage :image-src="HeroMack" />
    <HeroImage :image-src="HeroAdam" />
    <HeroImage :image-src="HeroMack" />
    <HeroImage :image-src="HeroAdam" />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  width: 100vw;
}
</style>
