<script setup>
import NavBar from "./components/NavBar.vue";
import Hero from "./components/Hero.vue"
import Dates from "./components/Dates.vue";
import InstaWidget from "./components/InstaWidget.vue";
import CoverFlow from "./components/CoverFlow.vue";
import Footer from "./components/Footer.vue";
import Information from "./components/Information.vue";
import Pills from "./components/Pills.vue";
</script>

<template>
  <NavBar id="navbar" />
  <Hero />
<!--  <InstaWidget />-->
  <Dates id="upcoming" />
  <CoverFlow id="releases" />
  <Information id="information" />

  <Pills />

  <Footer />
</template>

<style scoped>
</style>
