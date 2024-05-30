<template>
  <div class="flex flex-col gap-7 overflow-hidden">
    <div
      v-for="item in defnieCat"
      :key="item.id"
      class="flex p-4 bg-gradient-to-r text-black rounded-lg animate-rotate"
      :class="{
        breakfast: category === 'breakfast',
        lunch: category === 'lunch',
      }"
    >
      <div>
        <img :src="item.imageSrc" :alt="item.name" class="w-20 rounded-full" />
      </div>
      <div class="flex flex-col justify-center gap-2">
        <div class="flex justify-around">
          <h2 class="text-xl">{{ item.name }}</h2>
          <p class="text-lg">{{ item.price }}$</p>
        </div>
        <hr class="border-gray-900 w-11/12 ml-6" />
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["category"]);

const defnieCat = computed(() => {
  if (props.category === null) return null;
  if (props.category === "breakfast") {
    return breakFastItems;
  }
  if (props.category === "lunch") {
    return lunchItems;
  }
});

const lunchItems = [
  {
    name: "Special Burger",
    price: 15,
    imageSrc: "/menu images/burger.jpg",
    id: 1,
  },
  {
    name: "Special Burger",
    price: 15,
    imageSrc: "/menu images/burger.jpg",
    id: 2,
  },
  {
    name: "Special Burger",
    price: 15,
    imageSrc: "/menu images/burger.jpg",
    id: 3,
  },
  {
    name: "Special Burger",
    price: 15,
    imageSrc: "/menu images/burger.jpg",
    id: 4,
  },
];

const breakFastItems = [
  {
    name: "Crosan",
    price: 20,
    imageSrc: "/menu images/burger.jpg",
    id: 5,
  },
  {
    name: "Crosan",
    price: 20,
    imageSrc: "/menu images/burger.jpg",
    id: 6,
  },
  {
    name: "Crosan",
    price: 20,
    imageSrc: "/menu images/burger.jpg",
    id: 7,
  },
  {
    name: "Crosan",
    price: 20,
    imageSrc: "/menu images/burger.jpg",
    id: 8,
  },
];
</script>

<style scoped>
.lunch {
  @apply from-orange-300 to-orange-400;
}

.breakfast {
  @apply from-red-300 to-red-400;
}

.animate-rotate {
  animation: rotate 0.6s linear;
}

@keyframes rotate {
  from {
    opacity: 0;
    transform: translateY(-4rem);
  }
}
</style>
