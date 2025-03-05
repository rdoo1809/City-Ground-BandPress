<script setup>
import HeroImage from "./HeroImage.vue";
import HeroMack from "/public/images/hero-mack.jpeg";
import HeroAdam from "/public/images/hero-adam.jpeg";
import HeroLiam from "/public/images/hero-liam.jpeg";
import HeroNolan from "/public/images/hero-nolan.jpeg";
</script>

<template>
  <div class="container">
    <HeroImage :image-src="HeroMack" class="hero-image" />
    <HeroImage :image-src="HeroAdam" class="hero-image" />
    <HeroImage :image-src="HeroLiam" class="hero-image" />
    <HeroImage :image-src="HeroNolan" class="hero-image" />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  width: 100vw;
}

.hero-image {
  opacity: 0;
  transform: translateX(-100%);
  animation: slideIn 1s ease-out forwards;
}

.hero-image:nth-child(1) {
  animation-delay: 0.2s;
}

.hero-image:nth-child(2) {
  animation-delay: 0.4s;
}

.hero-image:nth-child(3) {
  animation-delay: 0.6s;
}

.hero-image:nth-child(4) {
  animation-delay: 0.8s;
}

@keyframes slideIn {
  0% {
    opacity: 0;
    transform: translateX(-100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>
