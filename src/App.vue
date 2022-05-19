<template>
  <div id="app">
    <div class="wrapper-card">
      <app-flipcard>
        <flipcard-back slot="back" />
        <flipcard-front slot="front" />
      </app-flipcard>

      <!-- <app-flipcard>
        <flipcard-front slot="front"/>
      </app-flipcard> -->
    </div>
    <img alt="Vue logo" src="./assets/logo.png">
    <app-test/>
    <img alt="Vue logo" src="./assets/logo.png">
  </div>
</template>

<script>
import AppFlipCard from './components/AppFlipCard.vue'
import AppTest from './components/test.vue'
import FlipCardBack from './components/FlipCardBack.vue'
import FlipCardFront from './components/FlipCardFront.vue'

export default {
  name: 'App',
  components: {
    'app-flipcard': AppFlipCard,
    'flipcard-back': FlipCardBack,
    'flipcard-front': FlipCardFront,
    'app-test': AppTest,
  },
  methods:{
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  min-height: 100vh;
  background-color: azure;
}

.wrapper-card {
  padding-top: 2rem;
  width: 95%;
  max-width: 634px;
  margin: 0 auto;
  display: flex;
  flex-flow: column;
  gap:1rem;
}
</style>
