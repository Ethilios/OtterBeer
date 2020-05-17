<template>
    <div class="top-section">
        <div class="main-heading">
            <h1>Otter Beer</h1>
        </div>
        <nav class="main-navbar">
            <ul>
                <li><a class="active" href="#home">Home</a></li>
                <li><a href="./light.html">Light</a></li>
                <li><a href="./medium.html">Medium</a></li>
                <li><a href="./dark.html">Dark</a></li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'PageHeader',
    props: {
        
    }
}
</script>

<style scoped>

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