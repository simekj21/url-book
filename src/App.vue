<template>
  <h4>Change main 2</h4>
  <h3 class="text-2xl font-bold text-center p-4">New change on main branch</h3>
  <h3 class="text-2xl font-bold text-center p-4">Change on feature 1</h3>
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 p-4">
    <a 
      v-for="url in urls" 
      :key="url.id" 
      class="bg-white shadow-md rounded-lg p-4 cursor-pointer transition duration-300 ease-in-out transform hover:scale-105"
      :href="url.url"
      target="_blank"
    >
      <img v-if="url.img" :src="url.img" alt="logo" class="" />
      <h2 v-else class="text-xl font-bold text-center">{{ url.name }}</h2>
  </a>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

interface URL {
  id: number;
  name: string;
  url: string;
  shortUrl: string;
  img: string;
}

const urls = ref<URL[]>([
  {
    id: 1,
    name: 'Google',
    url: 'https://www.google.com',
    shortUrl: 'https://bit.ly/3y3z3z3',
    img: './src/assets/google_logo.png',
  },
  {
    id: 2,
    name: 'Facebook',
    url: 'https://www.facebook.com',
    shortUrl: 'https://bit.ly/3y3z3z3',
    img: '',
  },
  {
    id: 3,
    name: 'Twitter',
    url: 'https://www.twitter.com',
    shortUrl: 'https://bit.ly/3y3z3z3',
    img: '',
  },
]);

</script>

<style scoped>

</style>
