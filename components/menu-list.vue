<template>
  <div class="flex flex-col gap-7 overflow-hidden">
    <div
      v-for="item in defnieCat"
      :key="item.id"
      class="flex p-4 bg-gradient-to-r text-black rounded-lg animate-rotate"
      :class="{
        breakfast: category === 'breakfast',
        lunch: category === 'lunch',
        dinner: category === 'dinner',
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
  if (props.category === "dinner") {
    return dinnerItems;
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

const dinnerItems = [
  {
    name: "Crosan",
    price: 20,
    imageSrc: "/menu images/burger.jpg",
    id: 9,
  },
  {
    name: "Crosan",
    price: 20,
    imageSrc: "/menu images/burger.jpg",
    id: 10,
  },
  {
    name: "Crosan",
    price: 20,
    imageSrc: "/menu images/burger.jpg",
    id: 11,
  },
  {
    name: "Crosan",
    price: 20,
    imageSrc: "/menu images/burger.jpg",
    id: 12,
  },
];
</script>

<style scoped>
.breakfast {
  @apply from-yellow-200 to-gray-300;
}

.lunch {
  @apply from-orange-300 to-gray-300;
}

.dinner {
  @apply from-red-200 to-gray-300;
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
