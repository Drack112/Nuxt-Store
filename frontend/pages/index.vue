<template>
  <div v-for="product in products.data" v-bind:key="product">
    <NuxtLink class="font-bold" :to="`/products/${product.id}`">{{
      product.attributes.Title
    }}</NuxtLink>
    <p>{{ product.attributes.Description }}</p>
  </div>
</template>

<script setup>
const config = useRuntimeConfig();
const { data: products } = await useFetch(
  () =>
    `${config.public.apiBase}/products?pagination[start]=0&pagination[limit]=4&populate=*`
);
</script>
