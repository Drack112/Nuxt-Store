<template>
  <section
    class="relative mb-20 -mt-24 border-b-4 md:mb-10 header border-brand-beige"
  >
    <div class="absolute inset-0 z-0 overflow-hidden">
      <img
        :src="HeaderBG"
        class="object-cover w-full h-full"
        alt="Pick a sick wick"
      />
    </div>
    <div class="relative z-20 h-full header-content">
      <div
        class="absolute flex flex-col justify-center p-8 mx-auto hero-box"
      ></div>
    </div>
  </section>

  <div v-for="product in products.data" v-bind:key="product">
    <NuxtLink class="font-bold" :to="`/products/${product.id}`">{{
      product.attributes.Title
    }}</NuxtLink>
    <p>{{ product.attributes.Description }}</p>
  </div>
</template>

<script setup>
import HeaderBG from "assets/images/header-bg.jpg";

const config = useRuntimeConfig();
const { data: products } = await useFetch(
  () =>
    `${config.public.apiBase}/products?pagination[start]=0&pagination[limit]=4&populate=*`
);
</script>

<style scoped>
@screen md {
  .hero-box {
    left: 10%;
    top: 175px;
    width: 485px;
  }
}

@screen md {
  .header {
    height: 700px;
  }
}

@screen md {
  .home-header-image {
    top: -110px;
    height: 770px;
    width: 100%;
  }
}

.hero-box {
  bottom: -50px;
  left: 0px;
  width: 100%;
}

@screen md {
  .hero-box {
    left: 10%;
    top: 100px;
    width: 485px;
  }
}
</style>
