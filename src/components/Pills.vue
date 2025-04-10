<template>
  <div style="width: 100vw; display: flex; flex-direction: column; align-items: center">
    <h2>{{ pastPresent() }} Dates</h2>

    <div style="display: flex; gap: 2rem; margin-bottom: 2rem">
      <button @click="activeTab = 'going'" class="pill">
        Where We're Going
      </button>
      <button @click="activeTab = 'been'" class="pill">
        Where We've Been
      </button>
    </div>

    <div v-if="activeTab === 'going'" class="dates-container">
      <Event
          v-for="(event, index) in upcomingEvents"
          :key="index"
          :title="event.title"
          :description="event.description"
          :month="event.month"
          :day="event.day"
          :link="event.link"
      />
    </div>

    <div v-if="activeTab === 'been'" class="dates-container">
      <Event
          v-for="(event, index) in pastEvents"
          :key="index"
          :title="event.title"
          :description="event.description"
          :month="event.month"
          :day="event.day"
          :link="event.link"
      />
    </div>
  </div>
</template>

<script setup>
import {ref, computed} from 'vue'
import Event from './Event.vue'

const whiteRabbitLink = 'https://whiterabbitwaterloo.com'
const room47Link = 'https://www.room47kw.com'
const edelweissLink = 'https://www.edelweisstavern.ca'
const torontoLink = 'https://www.eventbrite.com/e/out-of-the-blues-in-support-of-stellas-place-tickets-1218129912359?aff=oddtdtcreator'

const activeTab = ref('going')

const events = ref([
  
  
  {
    title: 'White Rabbit',
    description: 'Join us at the White Rabbit for our next acoustic gig!',
    month: 'March',
    day: '8',
    link: whiteRabbitLink
  },
  {
    title: 'Room47',
    description: 'Join us at the Room47 to get your socks rocked off!',
    month: 'March',
    day: '22',
    link: room47Link
  },
  {
    title: 'Out of the Blues',
    description: 'Join us at our Toronto debut! Click the link for tickets.',
    month: 'March',
    day: '26',
    link: torontoLink
  },
  {
    title: 'White Rabbit Acoustic Jam',
    description: 'Join us at the white rabbit for our 3-hour acoustic show!',
    month: 'April',
    day: '12',
    link: 'https://whiterabbitwaterloo.com'
  }
,
  {
    title: "Test Event",
    description: "This is a test",
    month: "April",
    day: "20",
    link: "https://venue.com"
  }
,
  {
    title: "Test Event",
    description: "This is a test",
    month: "April",
    day: "20",
    link: "https://venue.com"
  }
])

const isPastEvent = (month, day) => {
  const today = new Date()
  const monthMap = {
    'January': 0, 'February': 1, 'March': 2, 'April': 3, 'May': 4, 'June': 5,
    'July': 6, 'August': 7, 'September': 8, 'October': 9, 'November': 10, 'December': 11
  }
  const eventMonth = monthMap[month]
  const eventDate = new Date(today.getFullYear(), eventMonth, day)

  return eventDate < today
}

const upcomingEvents = computed(() => {
  return events.value.filter(event => !isPastEvent(event.month, event.day))
})

const pastEvents = computed(() => {
  return events.value.filter(event => isPastEvent(event.month, event.day))
})

const pastPresent = () => {
  return activeTab.value === 'been' ? 'Past' : 'Upcoming'
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
  font-family: 'Oswald', sans-serif;
  font-size: 24px;
  background: linear-gradient(45deg, rgba(0, 197, 255, 0.53), rgba(144, 48, 112, 0.55));
  border-radius: 2rem;
}
</style>