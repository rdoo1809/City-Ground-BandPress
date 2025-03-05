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
  display: flex;
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 15px;
  background-color: #f9f9f9;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.date-box {
  width: 150px;
  text-align: center;
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
  flex-grow: 1;
}

.description {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 10px;
}

.sub-description {
  font-size: 1rem;
  color: #666;
}

/* Styling for the link */
.event-link {
  display: inline-block;
  margin-top: 10px;
  font-size: 1rem;
  color: rgb(0, 197, 255);
  text-decoration: none;
  font-weight: bold;
}

.event-link:hover {
  text-decoration: underline;
}
</style>