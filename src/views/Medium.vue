<template>
    <div id="medium-page">
        <Hero heading="Medium"></Hero>
        <Gallery></Gallery>
    </div>
</template>

<script>
import Hero from '@/components/Hero.vue';
import Gallery from '@/components/Gallery.vue';

export default {
  name: 'Medium',
  components: {
    Hero,
    Gallery,
  }
}
</script>