<script setup>
import NavLink from "./NavLink.vue";
import Logo from "/public/images/logo.png"
</script>

<template>
  <nav class="navbar navbar-expand-lg footer">
    <img class="logo" alt="City Ground Logo" :src="Logo"/>
      <div>
        <ul class="nav-list">
          <NavLink title="HOME" href="#navbar"/>
          <NavLink title="UPCOMING" href="#upcoming"/>
          <NavLink title="RELEASES" href="#releases"/>
          <NavLink title="CONTACT" href="#information"/>
        </ul>
    </div>
  </nav>
</template>

<style scoped>
.footer {
  width: 100vw;
  padding: 6px 0;
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
