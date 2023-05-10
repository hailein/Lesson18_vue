<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="greetings">
    <h1>{{ msg }}</h1>
       <div class="enjoy_button">
        <a href="https://www.youtube.com/watch?v=lTRiuFIWV54">Enjoy</a>
       </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

.enjoy_button {
  font-size: 2rem;
  font-weight: 300;
background-color: black;
border-radius: 15px;
  padding: 5%;
  text-align: center;
}

a {
  color: white;
}

.greetings h1,
.greetings .enjoy_button {
  text-align: left;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings .enjoy_button {
    text-align: center;
  }
}
</style>
