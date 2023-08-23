<script setup>

import cars from './../data/cars.json'
import Card from './../components/Card.vue'
 
console.log(cars)

</script>
<template>
<div class="grid grid-cols-3 gap-3">
  <Card v-for="car in cars" :car="car" :key="car.id" />
</div>        
</template>