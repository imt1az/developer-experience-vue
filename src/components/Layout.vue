<template>
  <div class="relative flex min-h-screen  bg-gray-700">
    <!-- Side Bar -->
    <div class="bg-gray-900 text-cyan-100">
      <div class="flex justify-center items-center mt-14 transition-all duration-1000" :class="{'md:w-72':isOpen,'w-16':!isOpen}">
        <svg  
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          strokeWidth="{1.5}"
          stroke="currentColor"
          class="w-10 h-10 cursor-pointer"
        >
          <path
            strokeLinecap="round"
            strokeLinejoin="round"
            d="M2.25 18.75a60.07 60.07 0 0115.797 2.101c.727.198 1.453-.342 1.453-1.096V18.75M3.75 4.5v.75A.75.75 0 013 6h-.75m0 0v-.375c0-.621.504-1.125 1.125-1.125H20.25M2.25 6v9m18-10.5v.75c0 .414.336.75.75.75h.75m-1.5-1.5h.375c.621 0 1.125.504 1.125 1.125v9.75c0 .621-.504 1.125-1.125 1.125h-.375m1.5-1.5H21a.75.75 0 00-.75.75v.75m0 0H3.75m0 0h-.375a1.125 1.125 0 01-1.125-1.125V15m1.5 1.5v-.75A.75.75 0 003 15h-.75M15 10.5a3 3 0 11-6 0 3 3 0 016 0zm3 0h.008v.008H18V10.5zm-12 0h.008v.008H6V10.5z"
          />
        </svg>
        <span v-if="isOpen" class="text-4xl font-extrabold transition-all duration-1000">Demo</span>
      </div>
      <nav  @click="isOpen=!isOpen" class="flex justify-center p-4 bg-gray-700 mt-4 rounded-l-full ml-4">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-9 h-9 bg-red-800 rounded-full cursor-pointer"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25"
          />
        </svg>
        <button v-if="isOpen"><span class="text-white text-xl px-2 font-medium">Home</span></button>
      </nav>
    </div>

    <!-- Drawer -->
    
    <div class="flex-1">
      <!-- Header -->
      <Header />

   <main>
        <slot />
      </main>

     
    </div>
  </div>
</template>

<script setup>
import Header from "./Header.vue";

import { ref } from "vue";

let isOpen = ref(true);

function hoverEffect(){
  isOpen = !isOpen
  console.log(isOpen)
}


</script>

<style scoped>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
