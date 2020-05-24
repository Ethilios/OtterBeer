<template>
    <div id="dark-page">
        <Hero heading="Dark"></Hero>
        <Gallery></Gallery>
    </div>
</template>

<script>
import Hero from '@/components/Hero.vue';
import Gallery from '@/components/Gallery.vue';

export default {
  name: 'Dark',
  components: {
    Hero,
    Gallery,
  }
}
</script>