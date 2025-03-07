<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  imageSrc: {
    type: String,
    required: true
  }
});
</script>

<template>
  <div class="hero-holder">
    <img :src="imageSrc" alt="Box Image" class="hero-image" />
  </div>
</template>

<style scoped>
.hero-holder {
  width: 25%;
}

.hero-image {
  width: 100%;
}

</style>
