<script setup>
import NavLink from "./NavLink.vue";
import Logo from "/public/images/logo.png"
</script>

<template>
  <nav class="navbar navbar-expand-lg footer">
    <img class="logo" alt="City Ground Logo" :src="Logo"/>

    <div>
      <p> &copy City Ground 2025</p>
    </div>
  </nav>
</template>

<style scoped>
.footer {
  width: 100vw;
  padding: 6px 0px;
}

p {
  color: white;
  margin: 0;
}

.logo {
  height: 100px;
}
</style>
