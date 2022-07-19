<script setup>
import HeaderTop from "./components/HeaderTop.vue";
import HeaderBig from "./components/HeaderBig.vue";
import HeroBlock from "./components/HeroBlock.vue";
import BrandsCarousel from "./components/BrandsCarousel.vue";
import CatalogNav from "./components/CatalogNav.vue";
import { ref } from "vue";

const isCatalogOpen = ref(false);

function toggleCatalog() {
  isCatalogOpen.value = !isCatalogOpen.value;
}
</script>

<template>
  <div>
    <header class="header">
      <HeaderTop />
      <HeaderBig :toggleCatalog="toggleCatalog" :isCatalogOpen="isCatalogOpen"/>
      <CatalogNav :isCatalogOpen="isCatalogOpen"/>
      <div class="overlay" v-if="isCatalogOpen"></div>
      <HeroBlock />
      <BrandsCarousel />
    </header>
  </div>
</template>
