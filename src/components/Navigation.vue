<template>
    <div class="top-section">
        <div class="main-heading">
            <h1>Otter Beer</h1>
        </div>
        <nav class="main-navbar">
            <router-link class="routerlink" to="/">Home</router-link>
            <router-link class="routerlink" to="/light">Light</router-link>
            <router-link class="routerlink" to="/medium">Medium</router-link>
            <router-link class="routerlink" to="/dark">Dark</router-link>
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

.main-heading {
  margin-left: 5%;
  float: left;
  position: relative;
  font-size: 2.5vw;
}

@media only screen and (min-width: 1000px) {
  .main-heading {
    font-size: 2vw;
  }
}

.main-navbar {
  font-size: 1.2em;
  float: inline-end;
  padding-left: 60%;
  padding-top: 6%;
}

.main-navbar a{
    color: black;
    text-decoration: none;
    margin-left: 4%;
}

.main-navbar a:hover {
  color: rgb(109, 9, 202);
}

.main-navbar a.router-link-exact-active{
    text-decoration: underline;
}
</style>