<template>
    <div>
      <p>Products</p>
      <div v-for="p in products" :key="p.id">
        <ProductCard :product = "p"/>
</div>
      
    </div>
</template>

<script setup>
definePageMeta({
    layout:'products',
})

useHead({
    title: 'Nuxt Dojo | Merch',
    meta: [
        { name: 'description', content: 'Nuxt 3 Merch'}
    ]
})
const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<style scoped>

</style>
