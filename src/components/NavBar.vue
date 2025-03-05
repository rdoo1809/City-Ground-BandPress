<script setup>
import NavLink from "./NavLink.vue";
import Logo from "/public/images/logo.png"
</script>

<template>
  <nav class="navbar navbar-expand-lg nav">
    <img class="logo" alt="City Ground Logo" :src="Logo"/>

      <div>
        <ul class="nav-list">
          <NavLink title="HOME" href="#"/>
          <NavLink title="UPCOMING" href="#"/>
          <NavLink title="RELEASES" href="#"/>
          <NavLink title="CONTACT" href="#"/>
        </ul>
    </div>
  </nav>
</template>

<style scoped>
.nav {
  width: 100vw;
  padding: 6px 0px;
}

.nav-list {
  padding: 0;
  display: flex;
  justify-content: center;
}

.logo {
  height: 100px;
}
</style>
