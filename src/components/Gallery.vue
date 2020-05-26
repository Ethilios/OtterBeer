<template>
  <div class="gallery">
      <GalleryItem 
        v-for="(obj, index) in cosmicAssetObjs" 
        :key="index"
        :cosmicObj="obj"
        >
      </GalleryItem>
  </div>
</template>

<style scoped>
.gallery{
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(50px, auto);
  float: left;
  margin: 5% 7% 10% 9%;
  width: 85%;
}

.gallery .gallery { /* Prevents Recursively creating grid layout */
  display: block;
  margin: 4% 2%;
}

@media only screen and (max-width: 875px) {
  /* Smaller window - remove a column */
  .gallery {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media only screen and (min-width: 1200px) { 
  /* Improves layour of gallery on larger/full screen*/

}

@media only screen and (min-width: 1400px) {
  /* Bigger window - add a column */
  .gallery {
    grid-template-columns: repeat(5, 1fr);
  }
}


</style>

<script>
import GalleryItem from "./GalleryItem.vue";

export default {
    name: 'Gallery',
    components: {
      GalleryItem
    },
    data() {
      return {
        cosmicAssetObjs: [],
      }
    },
    mounted() {
      // Instantiate Cosmic
      const Cosmic = require('cosmicjs')()
      // Instantiate the Otter Beer bucket
      const bucket = Cosmic.bucket({
        slug: 'otter-beer',
        read_key: 'LDZg20C3CyfC5YuOWlhci9bnS3JWp2ujxlRJLewPkXN7Tw3LBE'
      })

      bucket.getBucket().then(data => {
        console.log(data)
        data.bucket.objects.map((object) => {
          this.cosmicAssetObjs.push(object)
        })
      })
    }
}
</script>