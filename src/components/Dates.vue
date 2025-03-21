<script setup>
import Event from "./Event.vue";

const whiteRabbitLink = "https://whiterabbitwaterloo.com";
const room47Link = "https://www.room47kw.com";
const edelweissLink = "https://www.edelweisstavern.ca";
const torontoLink = "https://www.eventbrite.com/e/out-of-the-blues-in-support-of-stellas-place-tickets-1218129912359?aff=oddtdtcreator";
</script>

<template>
  <div class="dates-container">
    <h2>Upcoming Dates</h2>
    <Event title="White Rabbit" description="Join us at the White Rabbit for our next accoustic gig!"
           month="March" day="8":link="whiteRabbitLink"/>
    <Event title="Room47" description="Join us at the Room47 to get your socks rocked off!" month="March" day="22"
           :link="room47Link"/>
    <Event title="Out of the Blues" description="Join us at our Toronto debut! Click the link for tickets."
           month="March" day="26" :link="torontoLink"/>
  <Event title="Ryan Dooley" description="event details"
  month="april" day="20" link="http://127.0.0.1:8000/dashboard" />
</div>
</template>

<style scoped>
.dates-container {
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>