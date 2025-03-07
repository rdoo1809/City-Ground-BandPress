<script setup>
</script>

<template>
  <div class="container">
    <div class="full-width-container">
      <div class="sub-container">
        <h2>GET IN TOUCH WITH US!</h2>
        <p>Book us for your next event, restaurant, wedding, we do it all!</p>
        <p><a>CONTACT</a></p>
      </div>

      <div class="sub-container">
        <h2>MERCH ORDER</h2>
        <p>Looking to rep City Ground? Order our T-Shirt today!</p>
        <p><a>ORDER FORM</a></p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  width: 100vw;
  display: flex;
  justify-content: center;
}

.full-width-container {
  display: flex;
  justify-content: space-between;
  border-radius: 16px;
  width: 80%;
  gap: 20px;
  padding: 20px;
  background: linear-gradient(45deg, rgba(0, 197, 255, 0.53), rgba(144, 48, 112, 0.55));

}

.sub-container {
  flex: 1;
  padding: 20px;
}

.sub-container h2 {
  font-size: 1.5rem;
  margin-bottom: 10px;
  color: white;
}

.sub-container p {
  color: white;
}

a {
  color: white;
  text-decoration: underline;
}

@media (max-width: 500px) {
  .full-width-container {
    flex-direction: column;
  }
}
</style>