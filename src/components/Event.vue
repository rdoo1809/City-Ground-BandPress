<script setup>
const props = defineProps({
  day: {
    type: Number,
    required: true
  },
  month: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  link: {
    type: String,
    required: false
  }
});
</script>

<template>
  <div class="date-card">
    <div class="date-box">
      <span class="date-number">{{ day }}</span>
      <span class="date-month">{{ month }}</span>
    </div>

    <div class="date-info">
      <h3 class="description">{{ title }}</h3>
      <p class="sub-description">{{ description }}</p>
      <a v-if="link" target="_blank" :href="link" class="event-link">Venue Information</a>
    </div>

  </div>
</template>

<style scoped>
.date-card {
  width: 50%;
  display: flex;
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 12px;
  margin: 6px 0;
  background-color: #f9f9f9;
  box-shadow: 0 4px 6px rgba(255, 255, 255, 0.3), 0 1px 3px rgba(255, 255, 255, 0.2);
}

.date-box {
  width: 150px;
  text-align: center;
  align-content: center;
  background-color: rgb(0, 197, 255);
  color: white;
  padding: 20px;
  border-radius: 8px;
  margin-right: 15px;
}

.date-number {
  font-size: 3rem;
  font-weight: bold;
}

.date-month {
  font-size: 1.2rem;
}

.date-info {
  display: flex; /* Enable flexbox */
  flex-direction: column; /* Align items vertically */
  flex-grow: 1; /* Take up the remaining space */
  text-align: center; /* Center text */
}

.description {
  font-size: 1.5rem;
  font-weight: bold;
  margin: 0;
}

.sub-description {
  color: #666;
}

.event-link {
  color: rgb(0, 197, 255);
  font-weight: bold;
}

.event-link:hover {
  text-decoration: underline;
}
</style>