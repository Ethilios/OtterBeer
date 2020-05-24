<template>
  <div class="gallery">
      <GalleryItem v-for="item in items" :key="item.id" :title="item.title" :source="item.source" :text="item.text"></GalleryItem>
  </div>
</template>

<style scoped>
.gallery{
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(50px, auto);
  float: left;
  margin-top: 5%;
  margin-bottom: 10%;
  padding: 0 5%;
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
  .gallery {
    padding: 0 7%;
  }
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
        items: [
          { 
            id: '001',
            title: 'Title One',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '002',
            title: 'Title Two',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '003',
            title: 'Title Three',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '004',
            title: 'Title Four',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '005',
            title: 'Title Five',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '006',
            title: 'Title Six',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '007',
            title: 'Title Seven',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '008',
            title: 'Title Eight',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '009',
            title: 'Title Nine',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '010',
            title: 'Title Ten',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '011',
            title: 'Title Eleven',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          },
          { 
            id: '012',
            title: 'Title Twelve',
            source: '@/assets/item-placeholder.jpg',
            text: 'This is the text'
          }
        ]
      };
    }
}
</script>