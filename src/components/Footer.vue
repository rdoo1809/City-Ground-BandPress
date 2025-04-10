<script setup>
import NavLink from "./NavLink.vue";
import Logo from "/public/images/logo.png"
import SocialBanner from "./SocialBanner.vue";
</script>

<template>
  <nav class="navbar navbar-expand-lg footer">
    <img class="logo" alt="City Ground Logo" :src="Logo"/>

    <SocialBanner />

    <div class="copyright">
      <p>&copy City Ground 2025</p>
      <p><a href=https://band-press-main-7qzk6r.laravel.cloud/ target="_blank">Band Press</a></p>
    </div>
  </nav>
</template>

<style scoped>
.footer {
  width: 100vw;
  padding: 20px 0px;
}

p, a {
  color: white;
  margin: 0;
  font-family: "Oswald", sans-serif;
}

.logo {
  height: 100px;
}

.copyright {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}
</style>
