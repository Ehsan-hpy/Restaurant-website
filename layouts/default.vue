<template>
  <nav
    class="flex justify-around items-center w-full h-16 gap-8 fixed backdrop-blur-lg"
  >
    <div>
      <img class="w-14 rounded-full image" src="/Logo.jfif" />
    </div>

    <ul class="flex gap-10">
      <li v-for="page in pages" :key="page.name">
        <NuxtLink
          class="px-3 py-2 rounded-md text-gray-200 hover:bg-gray-600 duration-200"
          :to="page.url"
          >{{ page.name }}</NuxtLink
        >
      </li>
      <li></li>
    </ul>
  </nav>

  <slot />
</template>

<script setup>
const pages = [
  { name: "Home", url: "/" },
  { name: "Menu", url: "/menu" },
  { name: "About", url: "/home" },
  { name: "Contact", url: "/home" },
];
</script>

<style scoped>
.router-link-active {
  @apply border-b-2;
}
</style>
