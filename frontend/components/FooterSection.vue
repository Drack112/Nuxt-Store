<template>
  <footer class="py-12 text-white bg-brand-grey-800">
    <Container class="grid grid-cols-12 gap-6">
      <div class="col-span-12 md:col-span-6">
        <img :src="LogoWhite" class="w-32" alt="Pick A Sick Wick" />
        <p class="py-4 md:w-4/5">
          Pick A Sick Wick is a JAMStack demo site built with Nuxt3, Strapi 4
          and Snipcart
        </p>
      </div>
      <div class="col-span-12 md:col-span-3">
        <Heading tag="h4" font-style="h4" color="text-white">Menu</Heading>
        <ul>
          <li class="underline list-disc list-inside">
            <NuxtLink>About</NuxtLink>
          </li>
          <li class="underline list-disc list-inside">
            <NuxtLink>Shop</NuxtLink>
          </li>
          <li class="underline list-disc list-inside">
            <NuxtLink>Contact</NuxtLink>
          </li>
        </ul>
      </div>
      <div class="col-span-12 md:col-span-3">
        <Heading tag="h4" font-style="h4" color="text-white">Contact</Heading>
        <p>The Wick Factory,</p>
        <p>Flame lane,</p>
        <p>Waxiton,</p>
        <p>United Kindgom</p>
      </div>
    </Container>
  </footer>
</template>

<script setup>
import LogoWhite from "assets/images/logo-white.svg";
</script>
