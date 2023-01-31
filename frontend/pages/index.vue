<template>
  <div v-for="product in products.data" v-bind:key="product">
    <NuxtLink class="font-bold" :to="`/products/${product.id}`">{{
      product.attributes.Title
    }}</NuxtLink>
    <p>{{ product.attributes.Description }}</p>
  </div>
</template>

<script setup>
const { data: products } = await useFetch(
  () => "http://127.0.0.1:1337/api/products"
);
</script>
