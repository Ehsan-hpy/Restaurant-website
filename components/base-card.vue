<template>
  <div
    class="w-60 h-60 p-4 flex flex-col items-center rounded-xl text-center even:-mb-60 duration-500 hover:shadow-gray-300 hover:shadow-lg"
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
