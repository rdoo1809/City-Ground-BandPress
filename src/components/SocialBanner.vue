<script>
export default {
  name: 'SocialBanner'
}
</script>

<template>
  <div class="social-banner">
    <a href="https://www.instagram.com/city_ground_band/" target="_blank"><i class="fa-brands fa-instagram fa-2xl"></i></a>
    <a href="https://www.youtube.com/@city_ground_band" target="_blank"><i class="fa-brands fa-youtube fa-2xl"></i></a>
    <a href="https://www.tiktok.com/@city_ground_band" target="_blank"><i class="fa-brands fa-tiktok fa-2xl"></i></a>
    <a href="https://www.facebook.com/profile.php?id=100095432928820" target="_blank"><i class="fa-brands fa-facebook fa-2xl"></i></a>
  </div>
</template>

<style scoped>

.social-banner {
  width: 100%;
  margin-bottom: 20px;
  display: flex;
  justify-content: center;
}

i {
  color: white;
  padding: 20px 8px;
}
</style>