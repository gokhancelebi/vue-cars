<script setup>
import {onMounted} from 'vue'

import Container from './Container.vue';
import logo_url from './../assets/logo.png'


onMounted(() => {
  const logo = document.getElementById('main-logo');
  logo.src = logo_url;
})

</script>
<template>
    <header class="border-b header-shadow font-bold">
    <Container class="flex justify-between items-center h-30">
      <RouterLink to="/">
        <img id="main-logo" src="">
      </RouterLink>
      <ul class="flex gap-10">
        <li>
          <router-link to="/" active-class="font-bold">HOME</router-link>
        </li>
        <li>
          <a href="#"  active-class="font-bold">PRODUCTS</a>
        </li>
        <li>
          <a href="#"  active-class="font-bold">CONTACT</a>
        </li>
        <li>
          <RouterLink  active-class="font-bold" to="/about">ABOUT US</RouterLink>
        </li>
      </ul>
    </Container>
  </header> 
</template>