<template>
    <div>
<img :src="product.image">
<p>{{product.title}}</p>
<p>{{product.description}}</p>
    </div>
</template>

<script setup>
const { product } = defineProps(['product'])
</script>

<style scoped>

</style>