<script setup>  
defineProps([
    "class"
])
</script>
<template>

    <div class="container mx-auto " :class="class">
        <slot />
    </div>

</template>
<style scoped>
.container{
    max-width: 1100px;
}
</style>