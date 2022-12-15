<template>
    <div>
      <p>Products</p>
      <div v-for="p in products" :key="p.id">
        <NuxtLink :to="`/products/${p.id}`">{{p.title}} sss</NuxtLink>
</div>
      
    </div>
</template>

<script setup>
definePageMeta({
    layout:'products',
})

const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<style scoped>

</style>