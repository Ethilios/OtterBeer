<template>
  <div id="home-page">
    <Hero heading="Featured Favourites"></Hero>
    <Gallery></Gallery>
    </div>
</template>

<script>
import Hero from '@/components/Hero.vue';
import Gallery from '@/components/Gallery.vue';

export default {
  name: 'Home',
  components: {
    Hero,
    Gallery,
  }
}
</script>




