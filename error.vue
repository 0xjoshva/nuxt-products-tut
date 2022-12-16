<template>
  <div>
    <p>{{ error.statusCode }}</p>
    <p>oops you visited the wrong page</p>
    <p>{{ error.message }}</p>
    <nuxt-link to="/">Go back home</nuxt-link>
  </div>
</template>

<script setup>
defineProps(["error"])
</script>

<style scoped></style>
