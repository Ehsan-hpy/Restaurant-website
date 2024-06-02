<template>
  <section class="h-lvh flex flex-col justify-center items-center gap-12">
    <div class="w-full flex justify-center gap-8">
      <MenuCategories @changeCategory="updateCategory" :category="category" />
    </div>

    <div class="w-full flex justify-center gap-10">
      <MenuList :category="category" />
      <MenuList :category="category" />
    </div>
  </section>
</template>

<script setup>
const category = useState("category", () => "breakfast");

function updateCategory(newCategory) {
  category.value = newCategory;
}
</script>

<style></style>
