<template>
      <div style="width: 100vw; display: flex; flex-direction: column; align-items: center">
        <h2>{{ pastPresent() }} Dates</h2>

        <div style="display: flex; gap: 2rem; margin-bottom: 2rem">
          <button
              @click="activeTab = 'going'" class="pill"
          >
            Where We're Going
          </button>

          <button
              @click="activeTab = 'been'" class="pill"
          >
            Where We've Been
          </button>
        </div>

        <div v-if="activeTab === 'going'" class="dates-container">
          <Event title="White Rabbit Acoustic Jam"
                 description="Join us at the white rabbit for our 3-hour acoustic show!"
                 month="April" day="12" link="https://whiterabbitwaterloo.com"/>
        </div>
        <div v-if="activeTab === 'been'" class="dates-container">
          <Event title="White Rabbit" description="Join us at the White Rabbit for our next accoustic gig!"
                 month="March" day="8" :link="whiteRabbitLink"/>
          <Event title="Room47" description="Join us at the Room47 to get your socks rocked off!" month="March" day="22"
                 :link="room47Link"/>
          <Event title="Out of the Blues" description="Join us at our Toronto debut! Click the link for tickets."
                 month="March" day="26" :link="torontoLink"/>
        </div>

      </div>
</template>

<script setup>
import {ref} from 'vue'
import Event from "./Event.vue";

const whiteRabbitLink = "https://whiterabbitwaterloo.com";
const room47Link = "https://www.room47kw.com";
const edelweissLink = "https://www.edelweisstavern.ca";
const torontoLink = "https://www.eventbrite.com/e/out-of-the-blues-in-support-of-stellas-place-tickets-1218129912359?aff=oddtdtcreator";

const activeTab = ref('going')

const pastPresent = () => {
  return activeTab.value === 'been' ? "Past" : "Upcoming"
}
</script>

<style scoped>
.dates-container {
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.pill {
  color: white;
  font-family: "Oswald", sans-serif;
  font-size: 24px;
  background: linear-gradient(45deg, rgba(0, 197, 255, 0.53), rgba(144, 48, 112, 0.55));
  border-radius: 2rem;
}
</style>