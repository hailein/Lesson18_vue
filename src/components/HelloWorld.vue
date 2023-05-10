<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  },

  imageUrl: String
})
</script>

<template>
  <div class="greetings">
    <h1>{{ msg }}</h1>
  </div>
  <img src="imageUrl" alt="">
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
