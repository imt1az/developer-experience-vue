<template>
  <div class="bg-gray-200 min-h-screen">
    <!-- User -->
   <div class="flex justify-center">
    <div class="relative w-[1200px] overflow-hidden mt-5">
      <input
        type="checkbox"
        class="peer absolute top-0 right-3 w-6 h-12 z-50 cursor-pointer opacity-0 "
      />
      <div class="bg-blue-500 h-12 w-full pl-5 flex items-center rounded-lg">
        <h1 class="text-lg font-semibold text-white">User</h1>
      </div>
      <!-- Arrow Icon -->
     <div class="absolute top-3 right-3 transition-transform duration-500 rotate-0 peer-checked:rotate-180 text-white">
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
      </div>
      <!-- Content -->
      <div class="bg-white overflow-hidden transition-all duration-500 max-h-[0] peer-checked:max-h-[100vh] border-blue-900">
        <div class="p-4 min-h-screen">
            <h1 class="text-3xl font-bold text-center my-5">User</h1>
          <p class="my-14">
            Headless UI keeps track of a lot of state about each component, like
            which listbox option is currently selected, whether a popover is
            open or closed, or which item in a menu is currently active via the
            keyboard. But because the components are headless and completely
            unstyled out of the box, you can't see this information in your UI
            until you provide the styles you want for each state yourself.
          </p>
          <p class="my-14">
            Headless UI keeps track of a lot of state about each component, like
            which listbox option is currently selected, whether a popover is
            open or closed, or which item in a menu is currently active via the
            keyboard. But because the components are headless and completely
            unstyled out of the box, you can't see this information in your UI
            until you provide the styles you want for each state yourself.
          </p>
          <p class="my-14">
            Headless UI keeps track of a lot of state about each component, like
            which listbox option is currently selected, whether a popover is
            open or closed, or which item in a menu is currently active via the
            keyboard. But because the components are headless and completely
            unstyled out of the box, you can't see this information in your UI
            until you provide the styles you want for each state yourself.
          </p>
          <p class="my-14">
            Headless UI keeps track of a lot of state about each component, like
            which listbox option is currently selected, whether a popover is
            open or closed, or which item in a menu is currently active via the
            keyboard. But because the components are headless and completely
            unstyled out of the box, you can't see this information in your UI
            until you provide the styles you want for each state yourself.
          </p>
        </div>
      </div>
    </div>
   </div>

    <!-- View -->
   <div class="flex justify-center">
    <div class="relative w-[1200px] overflow-hidden mt-5">
      <input
        type="checkbox"
        class="peer absolute top-0 right-3 w-6 h-12 z-50 cursor-pointer opacity-0 "
      />
      <div class="bg-blue-500 h-12 w-full pl-5 flex items-center rounded-lg">
        <h1 class="text-lg font-semibold text-white">View</h1>
      </div>
      <!-- Arrow Icon -->
     <div class="absolute top-3 right-3 transition-transform duration-500 rotate-0 peer-checked:rotate-180 text-white">
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
      </div>
      <!-- Content -->
      <div class="bg-white overflow-hidden transition-all duration-500 max-h-[0] peer-checked:max-h-[100vh] border-blue-900">
        <div class="p-4 min-h-screen">
            <h1 class="text-3xl font-bold text-center my-5">View</h1>
          <p class="my-14">
            Headless UI keeps track of a lot of state about each component, like
            which listbox option is currently selected, whether a popover is
            open or closed, or which item in a menu is currently active via the
            keyboard. But because the components are headless and completely
            unstyled out of the box, you can't see this information in your UI
            until you provide the styles you want for each state yourself.
          </p>
          <p class="my-14">
            Headless UI keeps track of a lot of state about each component, like
            which listbox option is currently selected, whether a popover is
            open or closed, or which item in a menu is currently active via the
            keyboard. But because the components are headless and completely
            unstyled out of the box, you can't see this information in your UI
            until you provide the styles you want for each state yourself.
          </p>
          <p class="my-14">
            Headless UI keeps track of a lot of state about each component, like
            which listbox option is currently selected, whether a popover is
            open or closed, or which item in a menu is currently active via the
            keyboard. But because the components are headless and completely
            unstyled out of the box, you can't see this information in your UI
            until you provide the styles you want for each state yourself.
          </p>
          <p class="my-14">
            Headless UI keeps track of a lot of state about each component, like
            which listbox option is currently selected, whether a popover is
            open or closed, or which item in a menu is currently active via the
            keyboard. But because the components are headless and completely
            unstyled out of the box, you can't see this information in your UI
            until you provide the styles you want for each state yourself.
          </p>
        </div>
      </div>
    </div>
   </div>
  </div>
</template>

<script setup>
import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";
import { ChevronDownIcon } from "@heroicons/vue/20/solid";
</script>
