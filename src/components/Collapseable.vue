<template>
  <!-- User -->
  <div class="flex justify-center">
    <div class="relative w-[900px] overflow-hidden mt-5">
      <div class="bg-blue-500 h-12 w-full pl-5 flex items-center rounded-lg">
        <h1
          class="text-lg font-semibold text-white"
          @click="$emit('clickedOnTittle')"
        >
          <slot name="title"></slot>
        </h1>
      </div>
      <!-- Arrow Icon -->
      <button
        @click="isOpen = !isOpen"
        class="absolute top-3 right-3 transition-transform duration-500 rotate-0 text-white"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M19.5 8.25l-7.5 7.5-7.5-7.5"
          />
        </svg>
      </button>
      <!-- Content -->
      <div
        class="bg-white overflow-hidden transition-all duration-500 border-blue-900"
        :class="{ 'max-h-[0]': !isOpen, 'max-h-screen': isOpen }"
      >
        <div class="p-4 min-h-screen">
          <!-- Content -->
          <slot />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isOpen = ref(false);
</script>