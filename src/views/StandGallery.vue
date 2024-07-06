<script setup lang="ts">
//need setup to get data from outside js

import Gallery from '../components/PictureGallery.vue'
import { stand } from '../fetched-data'
let standnigga = stand
</script>

<template>
  <h1>This is Stands gallery</h1>
  <Gallery :what-data="standnigga" />
</template>

<style></style>
