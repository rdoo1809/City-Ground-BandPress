<script setup>
import { defineProps } from "vue";

const props = defineProps({
  link: {
    type: String,
    required: true,
  },
  image: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <li>
    <a :href="link" target="_blank">
      <img :src="image" alt="Album Cover" />
    </a>
  </li>
</template>

<style scoped>

@media (max-width: 500px) {
  img {
    height: 200px;
  }
}
</style>
