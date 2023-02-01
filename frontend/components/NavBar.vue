<template>
  <nav>
    <ul class="flex flex-col items-center justify-center text-center gap-6">
      <li
        class="text-xl font-bold tracking-tighter transition-colors text-brand-grey-800 font-heading hover:text-orange-600"
      >
        <NuxtLink to="/">Home</NuxtLink>
      </li>
      <li
        class="text-xl font-bold tracking-tighter transition-colors text-brand-grey-800 font-heading hover:text-orange-600"
      >
        <NuxtLink to="/">Shop</NuxtLink>
      </li>
      <li
        class="text-xl font-bold tracking-tighter transition-colors text-brand-grey-800 font-heading hover:text-orange-600"
      >
        <NuxtLink to="/">Contact</NuxtLink>
      </li>
      <li
        class="text-xl font-bold tracking-tighter transition-colors text-brand-grey-800 font-heading hover:text-orange-600"
      >
        <NuxtLink to="/">GitHub</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.router-link-active {
  @apply text-brand-orange;
}
</style>
