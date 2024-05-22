<template>
  <section
    class="h-lvh flex items-center justify-center bg-[url('/bg-main.jpg')] bg-cover bg-no-repeat relative -z-20"
  >
    <div class="max-w-lg text">
      <h1 class="text-7xl">
        Enjoy Our <br />
        Delicious Meal
      </h1>
      <p class="text-xl">
        Resto is a perfect restaurant that has been established at the 1990, And
        that's the reason we're professional in our job! Another reason that can
        prove it is the satisfaction of our thousands or milions customers
      </p>
    </div>

    <div class="max-w-md">
      <img class="pizza-image" src="/main-page-pizza-image.png" alt="pizza" />
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
section::before {
  content: "";
  display: block;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(5 19 60 / 70%);
  z-index: -10;
}

.pizza-image {
  animation: image-spin 15s linear infinite;
}

@keyframes image-spin {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}
</style>
