<template>
  <div id="app">
    <navigation></navigation>
    <transition name="router-anim">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
import Navigation from '@/components/Navigation.vue';

export default {
  name: 'App',
  components: {
    Navigation
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Jost:wght@500&display=swap');

#app {
  font-family: Jost, sans-serif;
  position: absolute;
}

.router-anim-leave-active {
    animation: leaving 1s;
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
    animation-duration: 3s;
    opacity: 0;
}
@keyframes entering {
  from {
    transform: translateX(-50px);
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

</style>