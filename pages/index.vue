<template>
  <section class="h-lvh flex items-center justify-center gap-4 z-10">
    <div class="max-w-lg title-rotate space-y-4">
      <h1 class="text-6xl">
        Enjoy Our <br />
        Delicious Meal
      </h1>
      <p class="text-xl">
        Resto is a perfect restaurant that has been established at the 1990, And
        that's the reason we're professional in our job! Another reason that can
        prove it is the satisfaction of our thousands or milions customers
      </p>
    </div>

    <div class="max-w-sm overflow-hidden">
      <img class="pizza-image" src="/main-page-pizza-image.png" alt="pizza" />
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.pizza-image {
  animation: image-spin 20s linear infinite;
}

@keyframes image-spin {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

.title-rotate {
  animation: rotate 0.8s ease-in;
}

@keyframes rotate {
  0% {
    opacity: 0;
    transform: translateX(-5rem);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>
