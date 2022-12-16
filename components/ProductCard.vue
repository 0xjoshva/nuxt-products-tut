<template>
  <div>
    <img :src="product.image" alt="">
    <p>{{product.title}}</p>
    <nuxt-link :to="`/products/${product.id}`">
        <p>View Details</p>
    </nuxt-link>
  </div>
</template>

<script setup>
const { product } = defineProps(['product'])
</script>

<style scoped>

</style>