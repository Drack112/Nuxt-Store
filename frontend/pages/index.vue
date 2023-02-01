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
      <div class="absolute flex flex-col justify-center p-8 mx-auto hero-box">
        <div class="relative px-6 py-8 bg-white rounded-lg drop-shadow-2xl">
          <Heading tag="h3" font-style="h3">Smelly Candles</Heading>
          <Heading tag="h2" font-style="h2">Only The Sickest Wicks</Heading>
          <p>
            If you're like us and can't get enough of burning things in your own
            home, pick a sick wick.
          </p>
          <span class="font-bold"
            >feed your burning habit safely with added benefit of smelling
            delicious</span
          >
          <Button class="absolute md:-right-3 md:-bottom-3">Shop Now</Button>
        </div>
      </div>
    </div>
  </section>
  <section>
    <Container>
      <div class="w-full mx-auto mb-12 text-center md:w-2/3 lg:w-1/4">
        <Heading tag="h2" font-style="h2">Our candles</Heading>
        <Heading tag="h3" font-style="h3" class="mb-2"
          >All our candles our hand made 100% verified to satisfy any
          pyromaniac's itch to burn things in house</Heading
        >
      </div>
    </Container>
  </section>
  <div class="flex justify-center mt-10">
    <Button theme="secondary"> View all the sick wicks </Button>
  </div>
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
