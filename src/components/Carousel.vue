<template>
    <q-carousel
      v-model="slide"
      animated
      infinite
      :autoplay="true"
      swipeable
      transition-prev="jump-right"
      transition-next="jump-left"
      class="bg-black text-white"
    >
      <q-carousel-slide
        v-for="(image, index) in images"
        :key="index"
        :name="index"
        :img-src="image"
      />
    </q-carousel>
  </template>
  
  <script>
  import { QCarousel, QCarouselSlide } from 'quasar';
  
  export default {
    components: {
      QCarousel,
      QCarouselSlide
    },
    props: {
      images: {
        type: Array,
        required: true
      }
    },
    data() {
      return {
        slide: 0
      };
    }
  }
  </script>
  
  <style scoped>
  .q-carousel {
    height: 500px;
  }
  </style>
  