<template>
  <div>
    <p>Product details for {{ product.id }}</p>
    <p>
{{product.title}}
    </p>
    <p>{{product.price}}</p>
  </div>
</template>

<script setup>
//id must match
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id

// fetch product
const { data: product } = await useFetch(uri)

definePageMeta({
    layout:'products',
})
</script>

<style scoped></style>
