<template>
  <div class="bg-gray-100 shadow-xl aspect-w-1 aspect-h-1">
    <img :src="imageURL" :alt="product.attributes.Title" loading="lazy" />
  </div>
</template>

<script setup>
const props = defineProps({
  product: Object,
});

const config = useRuntimeConfig();
const imageURL = computed(() => {
  return `${config.public.apiBase}${props.product.attribute.Image.data.attributes.formats.medium.url}`;
});
</script>
