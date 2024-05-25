<template>
  <section class="min-h-lvh flex flex-col items-center pt-28 gap-20">
    <div
      class="flex gap-2 bg-gradient-to-r from-purple-300 to-purple-400 text-transparent bg-clip-text"
    >
      <h1 class="text-6xl">Welcome to</h1>
      <img class="w-16 rounded-full" src="/Logo.jfif" alt="Logo" />
      <h1 class="text-6xl">Resto</h1>
    </div>

    <div
      class="grid items-center grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4"
    >
      <BaseCard>
        <template #header>
          <UIcon name="i-heroicons-user" />
        </template>

        <template #default>
          <h2>Master Chefs</h2>
        </template>

        <template #footer>
          <p>We have very professional and experienced chefs!</p>
        </template>
      </BaseCard>

      <BaseCard>
        <template #header>
          <UIcon name="i-heroicons-shield-check" />
        </template>

        <template #default>
          <h2>Hight Quality Food</h2>
        </template>

        <template #footer>
          <p>We make our foods with very fresh and tasty materials!</p>
        </template>
      </BaseCard>

      <BaseCard>
        <template #header>
          <UIcon name="i-heroicons-shopping-cart" />
        </template>

        <template #default>
          <h2>Online Order</h2>
        </template>

        <template #footer>
          <p>Along with online ordering and response as soon as possible!</p>
        </template>
      </BaseCard>

      <BaseCard>
        <template #header>
          <UIcon name="i-heroicons-phone-arrow-down-left" />
        </template>

        <template #default>
          <h2>24/7 Service</h2>
        </template>

        <template #footer>
          <p>You can order online whenever you want!</p>
        </template>
      </BaseCard>
    </div>
  </section>
</template>

<style></style>
