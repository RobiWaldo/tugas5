<template>
    <q-card flat bordered class="my-card">
      <q-img :src="product.image" />
      <q-card-section>
        <div class="text-h6">{{ product.name }}</div>
        <div class="text-subtitle1">{{ product.price }}</div>
      </q-card-section>
    </q-card>
  </template>
  
  <script>
  import { QCard, QImg, QCardSection } from 'quasar';
  
  export default {
    components: {
      QCard,
      QImg,
      QCardSection
    },
    props: {
      product: {
        type: Object,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .my-card {
    max-width: 200px;
    margin: 10px;
  }

  .text-h6{
    color: black;
  }
  .text-subtitle1{
    color: black;
  }
  </style>
  