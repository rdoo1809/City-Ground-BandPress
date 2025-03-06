<script setup>
import { onMounted } from "vue";
import CoverOne from "/public/images/cover_one.jpeg"
import CoverTwo from "/public/images/cover_two.jpeg"

onMounted(() => {
  const $ = window.jQuery;
  $(".carousel").flipster({
    style: "carousel",
    spacing: -0.3,
  });
});
</script>

<template>
  <div class="hero">
    <div class="carousel">
      <ul>
        <li>
          <a href="https://www.youtube.com/watch?v=fagEbM5qvCw" target="_blank">
            <img :src="CoverOne" alt="Album Cover" />
          </a>
        </li>
        <li>
          <a href="https://open.spotify.com/album/78js2kiq60tVIFTrxAwLog?highlight=spotify:track:2YUvWayvjvWRqIWOGptljw" target="_blank">
            <img :src="CoverTwo" alt="Album Cover" />
          </a>
        </li>
        <li>
          <a href="https://open.spotify.com/album/10lWyz6dRO5LC7IybMwpZp?highlight=spotify:track:5Y59pWSdYMAtpRwdxF7WTO" target="_blank">
            <img :src="CoverOne" alt="Album Cover" />
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.hero {
  width: 100%;
  height: 100vh;
  background-color: #000;
  overflow-x: hidden;
}
.hero .carousel {
  width: 300px;
  margin: 100px auto 0;
  overflow: visible;
}

@media (max-width: 500px) {
  img {
    height: 200px;
  }
}
</style>
