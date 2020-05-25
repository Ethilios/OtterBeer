<template>
  <div id="app">
    <navigation></navigation>
    <transition name="router-anim">
      <router-view></router-view>
    </transition>
    <!-- <a href="https://app.cosmicjs.com/add-bucket?import_bucket=5ecb65dae003460008a635d1"><img src="https://cdn.cosmicjs.com/51fe54d0-4f6e-11e9-9f32-8d001da69630-powered-by-cosmicjs.svg" /></a> -->
  </div>
</template>

<script>
import Navigation from '@/components/Navigation.vue';

export default {
  name: 'App',
  components: {
    Navigation
  },
}

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Jost:wght@500&display=swap');

#app {
  font-family: Jost, sans-serif;
  position: absolute;
  width: inherit;
}

.router-anim-leave-active {
    animation: leaving .5s;
}
@keyframes leaving {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-50px);
    opacity: 0;
  }
}

.router-anim-enter-active {
    animation: entering 1s;
    animation-duration: 2.5s;
}
@keyframes entering {
  from {
    transform: translateX(-50px);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

</style>