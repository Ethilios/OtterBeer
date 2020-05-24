<template>
    <div id="light-page">
        <Hero heading="Light"></Hero>
        <Gallery></Gallery>
    </div>
</template>

<script>
import Hero from '@/components/Hero.vue';
import Gallery from '@/components/Gallery.vue';

export default {
  name: 'Light',
  components: {
    Hero,
    Gallery,
  }
}
</script>