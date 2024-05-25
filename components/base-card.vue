<template>
  <div
    class="w-60 h-60 p-4 flex flex-col items-center rounded-xl text-center md:even:-mb-60 duration-500 even:text-purple-400 text-blue-400 hover:shadow-gray-900 hover:shadow-2xl"
  >
    <header class="text-5xl">
      <slot name="header"> </slot>
    </header>

    <main class="text-xl">
      <slot></slot>
    </main>

    <footer class="text-md mt-6">
      <slot name="footer"></slot>
    </footer>
  </div>
</template>

<style scoped>
div:hover {
  transform: translateY(-10px);
}
</style>
