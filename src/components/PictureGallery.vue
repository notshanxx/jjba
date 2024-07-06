<script setup lang="ts">
let assetsUrl = `https://jojos-bizarre-api.netlify.app/assets/`
let prop = defineProps(['what-data'])
let data = JSON.parse(JSON.stringify(prop)).whatData

console.log(data.whatData)
</script>

<template>
  <!-- <h1>Gallery</h1> -->

  <!-- <ul>
    <li v-for="item in char">
      {{ item.name }}
    </li>
  </ul> -->

  <div class="grid">
    <div v-for="item in data" :key="item.id">
      <!-- <i>{{ item.nationality }}</i> -->
      <img v-bind:src="assetsUrl + item.image" loading="lazy" />
      <h3>{{ item.name }}</h3>
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
h3 {
  background-color: rgba(0, 0, 0, 0.336);
  position: absolute;

  border-radius: 0 0 5px 5px;
  bottom: 0;
  text-align: center;
  width: 100%;
  z-index: 2;
}
h3:hover {
  background: gray;
}

.grid {
  margin: 0 2rem;
  columns: 3;
}

.grid div {
  background-color: rgb(226, 226, 226);
  border-radius: 5px;
  position: relative;
  margin-bottom: 1rem;
  min-height: 100px;
}

img {
  border-radius: 5px;

  max-width: 100%;
}
@media only screen and (min-width: 768px) {
  /* For desktop: */
  .grid {
    margin: 0 10rem;
    columns: 5;
  }
  h3 {
    font-size: 2rem;
  }
}
</style>
