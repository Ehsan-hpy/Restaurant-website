<template>
  <div
    @click="$emit('change-category', 'breakfast')"
    :class="{
      active: category === 'breakfast',
    }"
  >
    <h2>Breakfast</h2>
    <img
      src="https://img.icons8.com/external-others-iconmarket/48/external-breakfast-food-others-iconmarket-2.png"
      alt="Breakfast"
    />
  </div>
  <div
    @click="$emit('change-category', 'lunch')"
    :class="{
      active: category === 'lunch',
    }"
  >
    <h2>Lunch</h2>
    <img src="https://img.icons8.com/fluency/48/hamburger.png" alt="Lunch" />
  </div>
  <div
    @click="$emit('change-category', 'dinner')"
    :class="{
      active: category === 'dinner',
    }"
  >
    <h2>Dinner</h2>
    <img
      src="https://img.icons8.com/fluency/48/salami-pizza.png"
      alt="Dinner"
    />
  </div>
</template>

<script setup>
defineProps(["category"]);
defineEmits(["change-category"]);
</script>

<style scoped>
div {
  @apply w-24 p-4 rounded-xl flex flex-col items-center cursor-pointer duration-500 hover:bg-gray-600;
}

.active {
  @apply -translate-y-4 shadow-2xl shadow-black bg-gray-600;
}
</style>
