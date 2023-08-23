<script setup>

import cars from './../data/cars.json'
import { useRoute, useRouter } from 'vue-router';

const route = useRoute()
const router = useRouter()
const car_id = parseInt(route.params.car_id)
const car = cars.find(c => c.id === car_id)

</script>
<template>
    <div class="grid grid-cols-2">
        <p class="border p-2 text-center">
            Name
        </p>
        <p class="border p-2 text-center">
            {{ car.name }}
        </p>
        <p class="border p-2 text-center">
            Price
        </p>
        <p class="border p-2 text-center">
            {{ car.price }}
        </p>
        <p class="border p-2 text-center">
            Year
        </p>
        <p class="border p-2 text-center">
            {{ car.year }}
        </p>
    </div>
    <button @click="router.push(`/car/${car_id}/contact`)" class="p-2 rounded border mt-2">Show Contact</button>
    <router-view />
</template>