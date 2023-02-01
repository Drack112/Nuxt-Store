<template>
  <Title>Pick a Sick Wick - Candle Shop</Title>
  <NuxtPage />
</template>

<style>
body {
  @apply text-brand-grey bg-brand-beige-300;
}

.snipcart-modal__container {
  z-index: 100;
}
</style>

<script setup>
useHead({
  link: [
    { rel: "preconnect", href: "https://fonts.googleapis.com" },
    { rel: "preconnect", href: "https://fonts.gstatic.com" },
    {
      href: "https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700;800;900&family=Source+Sans+Pro:wght@300;400;600;700;900&display=swap",
      rel: "stylesheet",
    },
    { rel: "preconnect", href: "https://app.snipcart.com" },
    { rel: "preconnect", href: "https://cdn.snipcart.com" },
    {
      rel: "stylesheet",
      href: "https://cdn.snipcart.com/themes/v3.2.1/default/snipcart.css",
    },
  ],
  script: [
    {
      src: "https://cdn.snipcart.com/themes/v3.2.1/default/snipcart.js",
      async: true,
    },
  ],
});

const router = useRouter();

// Scroll to top after each navigation
router.afterEach(() => {
  window.scrollTo(0, 0);
});
</script>
