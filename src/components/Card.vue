<script setup>
import cars from './../data/cars.json';

const props = defineProps(['car'])

const car = props.car
 
</script>

<template>
    <router-link :to="{ name:'carDetail', params : {car_id : car.id}}" class="rounded border p-2 text-center hover:bg-gray-300">
      {{ car.name }}
    </router-link>
</template>