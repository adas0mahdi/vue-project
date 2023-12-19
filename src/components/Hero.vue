<script setup>
import { ChevronDownIcon } from "@heroicons/vue/24/outline";
</script>
<!-- Hero.vue -->
<template>
  <!-- Background Image Section -->
  <div class="absolute top-0 left-0 z-10 overflow-hidden">
    <img
      class="scale-125 translate-x-11 w-full h-full object-cover min-h-screen"
      src="../assets/image/hero.jpg"
      alt="Passion Craft Background Image"
    />

    <!-- Centered Content Section -->
    <header
      class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 text-white text-center"
    >
      <h1 class="text-4xl md:text-6xl lg:text-7xl xl:text-8xl pb-4">
        Passion Craft
      </h1>
      <button
        class="text-black bg-white px-8 py-2 rounded-full hover:bg-slate-300"
        aria-label="Order Now"
      >
        Order Now
      </button>
    </header>

    <!-- Navigation Section -->
    <div
      class="absolute bottom-[1rem] left-1/2 transform -translate-x-1/2 text-white text-[20px] md:bottom-4 md:text-[24px]"
    >
      <a href="#" class="hover:underline font-light">MORE</a>
      <ChevronDownIcon class="h-6 w-6 inline-block ml-1 mb-1" />
    </div>
  </div>

  <!-- Empty Section -->
  <div
    class="-z-40 pointer-events-none w-full h-[577px] md:h-[580px] lg:h-[750px] xl:h-[890px]"
  >
    <!-- Your content for the empty section goes here -->
  </div>
</template>