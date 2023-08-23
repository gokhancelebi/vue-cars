<script setup>
import cars from './../data/cars.json'
import {useRoute} from 'vue-router'

const route = useRoute()

const car_id = parseInt(route.params.car_id)

const car = cars.find(c => c.id === car_id)

</script>
<template>
    <p>
        {{ car }}
    </p>
</template>