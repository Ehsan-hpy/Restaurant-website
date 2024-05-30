<template>
  <div
    class="flex flex-col items-center"
    @click="$emit('change-category', 'breakfast')"
  >
    <h2>Breakfast</h2>
    <img
      src="https://img.icons8.com/external-others-iconmarket/48/external-breakfast-food-others-iconmarket-2.png"
      alt="Breakfast"
    />
  </div>
  <div @click="$emit('change-category', 'lunch')">
    <h2>Lunch</h2>
    <img src="https://img.icons8.com/fluency/48/hamburger.png" alt="Lunch" />
  </div>
  <div @click="$emit('change-category', 'dinner')">
    <h2>Dinner</h2>
    <img
      src="https://img.icons8.com/fluency/48/salami-pizza.png"
      alt="Dinner"
    />
  </div>
</template>

<script setup>
defineEmits(["change-category"]);
</script>
