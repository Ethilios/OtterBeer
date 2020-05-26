<template>
    <div class="gallery">
        <div class="item-container">
            <img :src="this.defaultImage" alt="beer image">
            <div class="item-overlay">
                <div class="overlay-text">
                    <div class="heading">{{this.name}}</div>
                    <div class="text">{{this.brewery}}</div>
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
                if (field.title === 'Image') return defaultImage = field.url
            })
            return defaultImage
        },
        description() {
            let description
            this.cosmicObj.metafields.map((field) => {
                if (field.title === 'Description') return description = field.value
            })
            return description
        },
        name() {
            let name
            this.cosmicObj.metafields.map((field) => {
                if (field.title === 'Name') return name = field.value
            })
            return name
        },
        brewery() {
            let brewery
            this.cosmicObj.metafields.map((field) => {
                if (field.title === 'Brewery') return brewery = field.value
            })
            return brewery
        }
    },
    mounted() {
        console.log("Name:",
                    "Image:",
                    "Brewery:",
                    "Description:",)
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

.overlay-text .text {
    color: darkviolet;
}

</style>