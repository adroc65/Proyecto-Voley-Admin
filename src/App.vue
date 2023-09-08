<script setup>
/**
 * Ver este link de componebtes en Tailwind:
 * https://headlessui.com/
 */
  import Header from './components/Header.vue'
  import Layout from './components/Layout.vue'
  import LayoutFlex from './components/LayoutFlex.vue'
  import { db } from "./data/botones"


</script>

<template>
  <div class="container mx-auto mt-5 ">
    <Header />
    <Layout />
  </div>
</template>
