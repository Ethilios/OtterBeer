<template>
    <div class="gallery">
        <div class="item-container">
            <img src='@/assets/item-placeholder.jpg' alt="beer image">
            <div class="item-overlay">
                <div class="overlay-text">
                    <div class="heading">{{title}}</div>
                    <div class="text"></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'GalleryItem',
    components: {

    },
    props: {
        title: String,
        source: String,
        text: String,
    }
}
</script>

<style>

.item-container {
    position: relative;
}

.item-container img {
    display: block;
    width: 100%;
    height: auto;
}

.item-overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: .5s ease;
    background-color: black;
}

.item-container:hover .item-overlay {
  opacity: 1;
}

.overlay-text {
  color: white;
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;
}

</style>