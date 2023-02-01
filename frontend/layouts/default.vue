<template>
  <div class="relative font-body">
    <HeaderSection />
    <section class="pt-24 bg-brand-beige-300">
      <slot />
    </section>
    <FooterSection />
  </div>
</template>

<style scoped>
body {
  --webkit-font-smoothing: antialised;
}
</style>
