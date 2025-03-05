<script setup>
</script>

<template>
  <div class="upcoming-dates">
    <h2>Upcoming Dates</h2>

    <div class="dates-container">

      <div class="date-card">
        <div class="date-box">
          <span class="date-number">25</span>
          <span class="date-month">March</span>
        </div>
        <div class="date-info">
          <h3 class="description">Event Title</h3>
          <p class="sub-description">Detailed information about the event.</p>
        </div>
      </div>

<!--      <div class="date-card">-->
<!--        <div class="date-box">-->
<!--          <span class="date-number">10</span>-->
<!--          <span class="date-month">April</span>-->
<!--        </div>-->
<!--        <div class="date-info">-->
<!--          <h3 class="description">Another Event</h3>-->
<!--          <p class="sub-description">Details of another event happening soon.</p>-->
<!--        </div>-->
<!--      </div>-->

    </div>
  </div>
</template>

<style scoped>
.upcoming-dates {
  padding: 20px;
}

h2 {
  font-size: 2rem;
}

.dates-container {
  display: flex;
  gap: 20px;
  width: 100%;
}

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
  background-color: #2e8b57;
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
</style>