<template>
  <div class="bg-gray-100 shadow-xl aspect-w-1 aspect-h-1">
    <img :src="imageUrl" :alt="product.attributes.Title" loading="lazy" />
  </div>
</template>

<script setup>
const props = defineProps({
  product: Object,
});

const config = useRuntimeConfig();
const imageUrl = computed(() => {
  return `${config.public.apiBase}${props.product.attributes.Image.data.attributes.url}`;
});
</script>
