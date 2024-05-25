<template>
  <nav
    class="flex justify-around items-center w-full h-16 gap-8 fixed backdrop-blur-lg z-20"
  >
    <div class="flex items-center gap-2">
      <img class="w-14 rounded-full image" src="/Logo.jfif" />
      <h2 class="font-bold text-2xl">Resto</h2>
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

  <div
    class="h-auto min-h-lvh bg-[url('/bg-main.jpg')] bg-cover bg-no-repeat w-full fixed -z-20 bg-blur-color"
  ></div>

  <slot />
</template>

<script setup>
const pages = [
  { name: "Home", url: "/" },
  { name: "About", url: "/about" },
  { name: "Menu", url: "/menu" },
  { name: "Contact", url: "/home" },
];
</script>

<style scoped>
.bg-blur-color::before {
  content: "";
  display: block;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(4 7 38 / 82%);
  z-index: -10;
}

.router-link-active {
  @apply border-b-2;
}
</style>
