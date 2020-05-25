<template>
    <div class="gallery">
        <div class="item-container">
            <img :src="defaultImage" alt="beer image">
            <div class="item-overlay">
                <div class="overlay-text">
                    <div class="heading">{{cosmicObj.name}}</div>
                    <div class="text">{{cosmicObj.brewery}}</div>
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
        cosmicObj: {
            required: true,
            type: Object
        }
    },
    data() {
        return {}
    },
    computed: {
        defaultImage() {
            let defaultImage
            this.cosmicObj.metafields.map((field) => {
                if (field.title === 'image') return defaultImage = field.url
            })
            return defaultImage
        },
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
    border-radius: 10px;
}

.item-overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100%;
    width: 100%;
    border-radius: 10px;
    opacity: 0;
    transition: .5s ease;
    background-color: darkslateblue;
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