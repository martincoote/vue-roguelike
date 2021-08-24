<template>
  <div id="app">
    <div class="map">
      <Hero :x=2 :y=3 />
    </div>
  </div>
</template>

<script>
import Hero from './components/Hero.vue'

export default {
  name: 'App',
  components: {
    Hero
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.map {
  display: grid;
  grid-template-columns: repeat(9, 2rem);
  grid-template-rows: repeat(9, 2rem);
  align-items: center;
  justify-items: center;
  border: 2px solid black;
  width: max-content;
  margin: 0 auto;
  background: 
    repeating-linear-gradient(to right, transparent  0rem 1.9rem, black 1.9rem 2rem),
    repeating-linear-gradient(to top, transparent  0rem 1.9rem, black 1.9rem 2rem)
  ;
}
</style>
