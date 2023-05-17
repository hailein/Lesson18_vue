<script>
import HelloWorld from './components/HelloWorld.vue'
import EnjoyButton from './components/EnjoyButton.vue'
import worksData from './assets/works.json'

export default {
  data() {
    return {
      works: worksData,
    };
  },
};
</script>

<template>
  <main>

    <div class="wrapper">
      <HelloWorld
       title="Relax and enjoy" 
       imageUrl="https://images.unsplash.com/photo-1588434487755-e211e0aae297?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxfDB8MXxyYW5kb218MHx8bG9maXx8fHx8fDE2ODM3MTAyMDY&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=1080.com/it/s/foto/lo-fi"
       /> 
    </div>

    <div>
      <EnjoyButton msg="Clicca qui per un po' di Lo-fi" />
    </div>

    <div id="works">
      <div v-for="work in works" :key="work.id">
        <h1> {{ work.title }}</h1>
        <p>
        {{work.description}}
        </p>
        <div>
        <img :src= "work.image_thumbnail" width="200" height="200">
        </div>
      </div>
    </div>

    <!-- <div>
      <HelloWorld
      :title="work.title"
      :abstract="work.description"
      :imageUrl="work.image_thumbnail"
      />
    </div> -->
    
  </main>
</template>

<style scoped>
main {
  background-color: rgb(255, 220, 250);
  width: 100vw;
  height: 100vh;
  margin: 0;
}

@media (min-width: 1024px) {
  main {
    display: flex;
    place-items: left;
    flex-direction: column;
  }

  main .wrapper {
    display: flex;
    place-items: flex-start;
    justify-content: left;
    flex-direction: column;
  }
}
</style>
