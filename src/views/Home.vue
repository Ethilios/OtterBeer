<template>
  <div id="home-page">
    <Hero :heading="Testing"></Hero>
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue';

export default {
  name: 'Home',
  components: {
    Hero
  },
}
</script>



