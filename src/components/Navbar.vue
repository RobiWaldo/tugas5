<template>
    <q-header elevated>
      <q-toolbar>
        <q-btn flat round icon="menu" @click="toggleDrawer" />
        <q-toolbar-title>
          Toko Sepatu Online
        </q-toolbar-title>
        <q-space />
        <q-btn flat label="Beranda" @click="navigate('beranda')" />
        <q-btn flat label="Produk" @click="navigate('produk')" />
        <q-btn flat label="Keranjang" @click="navigate('keranjang')" />
      </q-toolbar>
    </q-header>
  </template>
  
  <script>
  import { QHeader, QToolbar, QToolbarTitle, QBtn, QSpace } from 'quasar';
  
  export default {
    components: {
      QHeader,
      QToolbar,
      QToolbarTitle,
      QBtn,
      QSpace
    },
    methods: {
      toggleDrawer() {
        this.$emit('toggle-drawer');
      },
      navigate(page) {
        this.$emit('navigate', page);
      }
    }
  }
  </script>
  
  <style scoped>
  .q-header {
    background-color: black;
    color: white;
  }
  </style>
  