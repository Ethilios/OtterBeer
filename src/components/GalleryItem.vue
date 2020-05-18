<template>
    <div class="item-container">
        <div class="item"><img src={{item-image-src}} alt="beer image"></div>
        <div class="item-overlay">
            <div class="overlay-text">
                {{item-text}}
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
props: {
    item-image-src,
    item-title,
    item-text
}
</script>

<style>

</style>