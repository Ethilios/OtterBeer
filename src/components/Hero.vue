<template>
    <div class="hero">
        <div class="hero-image">
            <img src="@/assets/beer-banner-blue-fade.jpg" alt="beer bottles" style="width:100%;">
        </div>
        <div class="hero-text">
            <h1>{{heading}}</h1>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        heading: String
    }
}
</script>

<style scoped>
.hero {
    position: relative;
    text-align: center;
    color: aliceblue;
}

.hero-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: calc(14px + (23 - 10) * ((100vw - 300px) / (1600 - 300)));
}

</style>