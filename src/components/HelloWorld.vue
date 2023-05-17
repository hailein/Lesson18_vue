<script setup>
defineProps({
  title: String,
  imageUrl: String,
})
</script>

<template>

  <h1>{{ title }}</h1>

  <div class="gallery">
    <img :src="imageUrl" width="200" height="200">
    <img :src="imageUrl" width="200" height="200">
    <img :src="imageUrl" width="200" height="200">
  </div>

</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2rem;
}

.gallery  {
  display: flex;
  flex-wrap: nowrap;
  align-items: center;
  gap: 2rem;
}

@media (min-width: 1024px) {
h1{
    text-align: left;
  }
}
</style>
