<template>
  <div id="app">
    <div class="top-section">
        <div class="main-heading">
            <h1>Otter Beer</h1>
        </div>
        <nav class="main-navbar">
          <router-link to="/">Home</router-link>
          <router-link to="/about">Light</router-link>
          <router-link to="/Medium">Medium</router-link>
          <router-link to="/Dark">Dark</router-link>
        </nav>
    </div>
    <router-view/>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Jost:wght@500&display=swap');

#app {
  font-family: Jost, sans-serif;
}

h1 {
  font-weight: 400;
}

.main-heading {
  margin-left: 5%;
  width: 55%;
  float: left;
  position: relative;
}

.main-navbar {
  font-size: 1.2em;
  margin-left: 60%;
  display: inline;
}

nav a {
  float: left;
  margin-left: 2%;
  text-decoration: none;
  color: black;
}

nav a:hover {
  color: blueviolet;
}

nav a.router-link-exact-active{
    text-decoration: underline;
}

</style>