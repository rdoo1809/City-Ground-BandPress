<script setup>
import Logo from "/public/images/logo.png"

</script>

<template>
  <!-- Cover Flow -->
  <div class="hero">
    <div class="carousel">
      <ul>
        <li>
          <a
              href="https://www.youtube.com/watch?v=fagEbM5qvCw"
              target="_blank"
          ><img
              class="albumCov"
              :src="Logo"
              alt="Faytak"
          /></a>
        </li>
        <li>
          <a
              href="https://www.youtube.com/watch?v=7C60dRoZ6bc"
              target="_blank"
          ><img
              class="albumCov"
              :src="Logo"
              alt="Masa2Altesh"
          /></a>
        </li>
        <li>
          <a
              href="https://www.youtube.com/watch?v=7C60dRoZ6bc"
              target="_blank"
          ><img
              class="albumCov"
              :src="Logo"
              alt="Masa2Altesh"
          /></a>
        </li>
      </ul>
    </div>
  </div>
  <!-- End of cover flow -->
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

/*
.carousel img {
  -webkit-box-reflect: below 20px
    linear-gradient(rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0.1));
} */
</style>
