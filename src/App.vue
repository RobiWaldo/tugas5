<template>
  <q-layout>
    <q-page-container>
      <LandingPage
        :carousel-images="carouselImages"
        :products="products"
        @navigate="handleNavigate"
      />
    </q-page-container>
  </q-layout>
</template>

<script>
import { QLayout, QPageContainer } from 'quasar';
import LandingPage from './components/LandingPage.vue';

export default {
  components: {
    QLayout,
    QPageContainer,
    LandingPage
  },
  data() {
    return {
      carouselImages: [
        'https://img-new.cgtrader.com/items/4084204/238bf3c1cf/air-jordan-4-jumpman-variety-pack-3d-model-238bf3c1cf.jpg',
        'https://img-new.cgtrader.com/items/4084204/81def6fa5c/air-jordan-4-jumpman-variety-pack-3d-model-81def6fa5c.jpg',
        'https://img-new.cgtrader.com/items/4084204/c2ceb732e2/air-jordan-4-jumpman-variety-pack-3d-model-c2ceb732e2.jpg',
        'https://img-new.cgtrader.com/items/4084204/94ee08a138/air-jordan-4-jumpman-variety-pack-3d-model-94ee08a138.jpg'
      ],
      products: [
        { id: 1, name: 'Nike Air Max 1 v2', price: 'Rp 2.199.000', image: 'https://img-new.cgtrader.com/items/2089873/56aaf8bfd1/nike-air-max-1-v2-3d-model-max-obj-3ds-fbx.jpg' },
        { id: 2, name: 'Air Jordan Variety ', price: 'Rp 5.259.000', image: 'https://img-new.cgtrader.com/items/4083487/1b96c491c3/air-jordan-1-variety-pack-3d-model-1b96c491c3.jpg' },
        { id: 3, name: 'Air Force Nike PBR', price: 'Rp 1.549.000', image: 'https://img-new.cgtrader.com/items/2832802/8600f746d8/air-force-1-low-nike-pbr-3d-model-8600f746d8.jpg' },
      ]
    };
  },
  methods: {
    handleNavigate(page) {
      console.log(`Navigating to ${page}`);
      // Implement the navigation logic here
      // For example, using Vue Router:
      // this.$router.push({ name: page });
    }
  }
}
</script>

<style>
#q-app {
  background-color: black;
  padding-bottom: 300px;
}
</style>
