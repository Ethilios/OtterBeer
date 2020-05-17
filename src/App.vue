<template>
  <div id="app">
    <page-header></page-header>
    <hero :heading="home_heading"></hero>
  </div>
</template>

<script>
import PageHeader from './components/PageHeader.vue'
import Hero from './components/Hero.vue'

var bg_colour = process.env.VUE_APP_PALE_BLUE;

export default {
  name: 'App',
  components: {
    PageHeader,
    Hero
  },
  data() {
    return {
      home_heading: "Featured Favourites",
      bg_colour: bg_colour
    };
  },
}
</script>

<style>

@import url("https://fonts.googleapis.com/css2?family=Jost:wght@500&display=swap");

#app {
  font-family: Jost, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #CDF4FF;
}

</style>
