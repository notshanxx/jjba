<script setup lang="ts">
import Gallery from '../components/PictureGallery.vue'
import { character } from '../fetched-data'
let chars = character
</script>

<template>
  <h1>This is Character GAllery</h1>
  <Gallery :what-data="chars" />
</template>

<style>
h1 {
  text-align: center;
}
</style>
