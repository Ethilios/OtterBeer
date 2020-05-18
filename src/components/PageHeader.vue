



// Not in Use




<template>
    <div class="top-section">
        <div class="main-heading">
            <h1>Otter Beer</h1>
        </div>
        <nav class="main-navbar">
            <ul>
                <li><router-link to="/">Home</router-link></li>
                <li><router-link to="../views/about">Light</router-link></li>
                <li><router-link to="/Medium">Medium</router-link></li>
                <li><router-link to="/Dark">Dark</router-link></li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'PageHeader',
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Jost:wght@500&display=swap');

.top-section {
  font-family: Jost, sans-serif;
}

    h1 {
    font-weight: 400;
    }

    .main-heading {
    margin-left: 5%;
    width: 30%;
    float: left;
    position: relative;
    }

    .main-navbar {
    margin-left: 10%;
    display: inline;
    font-size: 1.2em;
    }

    .main-navbar ul{
        list-style: none;
        margin-left: 60%;
        margin-top: -1%;
    }

    .main-navbar ul li {
        float: left;
        margin-left: 5%;
    }

    .main-navbar ul li a{
        text-decoration: none;
        color: black;
    }

    .main-navbar ul li a.active{
        text-decoration: underline;
    }

</style>