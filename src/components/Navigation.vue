<template>
    <div class="top-section">
        <div class="main-heading">
            <h1>Otter Beer</h1>
        </div>
        <nav class="main-navbar">
            <router-link id="left-most" to="/">Home</router-link>
            <router-link to="/light">Light</router-link>
            <router-link to="/medium">Medium</router-link>
            <router-link to="/dark">Dark</router-link>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'Navigation'
}
</script>

<style>
h1 {
  font-weight: 400;
}

.top-section {
  display: flex;
}

.main-heading {
  margin-left: 5%;
  margin-right: 24%;
  float: inline-start;
  font-size: calc(14px + (26 - 14) * ((100vw - 300px) / (1600 - 300)));
}

.main-navbar {
  margin-left: 15vw;
  margin-top: 4%;
  font-size: calc(14px + (23 - 10) * ((100vw - 300px) / (1600 - 300)));
}

#left-most {
  margin-left: 0%;
}

.main-navbar a{
    text-decoration: none;
    margin-left: 12%;
    color: darkslateblue;
}

.main-navbar a:hover {
  color: darkviolet;
}

.main-navbar a.router-link-exact-active{
    text-decoration: underline;
}
</style>