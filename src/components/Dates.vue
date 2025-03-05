<script setup>
import Event from "./Event.vue";
</script>

<template>
  <div class="dates-container">
    <h2>Upcoming Dates</h2>
    <Event title="EdelWeiss Tavern" description="Join us at the EdelWeiss Tavern to get your socks rocked off!" month="March" day="26" link="https://www.edelweisstavern.ca" />
    <Event title="Room47" description="Join us at the Room47 to get your socks rocked off!" month="March" day="26" link="https://www.edelweisstavern.ca" />
  </div>
</template>

<style scoped>
h2 {
  font-size: 2rem;
  color: white;
}

.dates-container {
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>