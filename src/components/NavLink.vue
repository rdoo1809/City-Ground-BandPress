<template>
  <li class="nav-item">
    <a :href="href" class="nav-link">
      {{ title }}
    </a>
  </li>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    href: {
      type: String,
      required: true
    },
  }
};
</script>

<style scoped>
.nav-item{
  list-style: none;
}

.nav-link{
  color: white;
  padding: 0 1rem;
}

.nav-link:hover {
  color: rgb(0, 197, 255);
}

.nav-link.active {
  color: rgb(0, 197, 255);
}
</style>
