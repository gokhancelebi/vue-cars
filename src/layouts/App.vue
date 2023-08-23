<script setup>
import Container from '../components/Container.vue';
import Header from '../components/header.vue';

</script>
<template>
  <Header />
  <main>
    <Container class="mt-10">
      <RouterView />
    </Container>
  </main>
</template>
 