<script>
/* import HelloWorld from './components/HelloWorld.vue'
import EnjoyButton from './components/EnjoyButton.vue' */

import Header from './components/Header.vue'
import SocialLink from './components/SocialLink.vue'
import PortfolioItem from './components/PortfolioItem.vue'

import contentsData from './assets/contents.json'

export default {
  data() {
    return {
      contents: contentsData,
    };
  },

  components: {
    PortfolioItem,
    Header,
    SocialLink,
  },
};
</script>

<template>
  <main>
    <Header />

    <div id="works" class="row">
      <div class="col-12 col-md-6" v-for="work in contents.works" :key="work.id">
         <PortfolioItem 
          :title="work.title"
          :abstract="work.description"
          :imageUrl="work.image_thumbnail"
        />
      </div>
    </div>

    <div id="social-links" class="row">
      <ul>
        <li v-for="link in contents.social_links" :key="link.id">
          <SocialLink 
            :id="link.id"
            :name="link.name"
            :url="link.url"
          />
        </li>
      </ul>
    </div>

<!--     <div id="works">
      <div v-for="work in works" :key="work.id">
        <h1> {{ work.title }}</h1>
        <p>
        {{work.description}}
        </p>
        <div>
        <img :src= "work.image_thumbnail" width="200" height="200">
        </div>
      </div>
    </div> -->

  </main>
</template>

<style scoped>

header {
  line-height: 1.5;
}

main {
  background-color: rgb(255, 220, 250);
  width: 100vw;
  height: 100vh;
  margin: 0;
}
</style>
