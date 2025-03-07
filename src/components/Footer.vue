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
      <p>RJD</p>
    </div>
  </nav>
</template>

<style scoped>
.footer {
  width: 100vw;
  padding: 20px 0px;
}

p {
  color: white;
  margin: 0;
}

.logo {
  height: 100px;
}

.copyright {
  display: flex;
  justify-content: space-evenly;
}
</style>
