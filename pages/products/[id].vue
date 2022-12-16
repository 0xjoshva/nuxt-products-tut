<template>
  <Head>
    <Title>Nuxt Dojo | {{product.title}}</Title>
    <Meta name="description" :content="product.description"/>
  </Head>
  <div>
<ProductDetails :product="product"/>
  </div>
</template>

<script setup>
//id must match
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id

// fetch product
const { data: product } = await useFetch(uri)


//direct to error page if /products/ does not have integer at the end
//throw error message and status code
if (!product.value) {
  throw createError({statusCode: 404, statusMessage: "product not found", fatal: true})
}
definePageMeta({
    layout:'products',
})
</script>

<style scoped></style>