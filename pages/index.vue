<template>
  <section class="h-lvh bg-[url('/bg-main.jpg')] bg-cover bg-no-repeat">
    <h1>Hi</h1>
  </section>
</template>

<script setup></script>

<style scoped>
section::before {
  content: "";
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(5 19 60 / 70%);
}
</style>
