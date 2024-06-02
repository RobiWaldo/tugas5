<template>
    <q-page class="bg-black text-white">
      <Navbar @toggle-drawer="toggleDrawer" />
      <Carousel :images="carouselImages" />
      <div class="q-pa-md row justify-center">
        <ProductCard
          v-for="product in products"
          :key="product.id"
          :product="product"
        />
      </div>
      <Footer />
    </q-page>
  </template>
  
  <script>
  import { QPage } from 'quasar';
  import Navbar from './Navbar.vue';
  import Carousel from './Carousel.vue';
  import ProductCard from './ProductCard.vue';
  import Footer from './Footer.vue';
  
  export default {
    components: {
      QPage,
      Navbar,
      Carousel,
      ProductCard,
      Footer
    },
    props: {
      carouselImages: {
        type: Array,
        required: true
      },
      products: {
        type: Array,
        required: true
      }
    },
    methods: {
      toggleDrawer() {
        // toggle drawer logic
      }
    }
  }
  </script>
  
  <style scoped>
  .q-page {
    min-height: 300vh;
    display: flex;
    flex-direction: column;
    padding-bottom: 100px;
  }

  </style>
  