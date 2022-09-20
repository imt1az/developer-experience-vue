<template>
  <!-- User -->

  <div class="flex flex-col items-center">
    <div
      v-for="(item, index) in collapseableData"
      :key="item.id"
      class="relative w-[80vw] overflow-hidden mt-5"
    >
      <div  class="">
        <Transition name="toogle">
        <div v-if="!item.toggle" @click="swap(index)"
          class="bg-red-800 h-12 w-full pl-5 rounded-lg cursor-pointer transition-transform duration-1000 toggle"
        >
          <h1
            class="text-2xl  font-semibold text-white text-center cursor-pointer"
          >
            {{ item.title }}
          </h1>
        </div>
        </Transition>
      </div>

      <!-- Arrow Icon -->
      <div
        v-if="item.icon"
        @click="activeBody(index)"
        class="absolute top-3 right-3 transition-transform duration-500 rotate-0 text-white"
      >
        <svg
          v-if="item.icon"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-8 h-8"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M19.5 8.25l-7.5 7.5-7.5-7.5"
          />
        </svg>
      </div>
      <!-- Content -->
      <Transition name="fade">
        <div
          class="bg-white overflow-hidden border-blue-900 min-h-screen"
          v-if="item.active"
        >
          <div class="p-4 min-h-screen">
            <!-- Content -->
            <!-- <slot /> -->
            <h1 class="text-5xl font-semibold text-black text-center">
              {{ item.title }}
            </h1>
            <p
              class="m-20 p-20 font-semibold"
              v-for="(paragraph, i) in item.content"
              :key="i"
            >
              {{ paragraph }}
            </p>
          </div>
        </div>
      </Transition>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const collapseableData = ref([
  {
    id: 1,
    title: "User",
    toggle: false,
    active: false,
    icon: true,
    content: [
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis explicabo dicta voluptas neque repellat numquam, veritatis fugit quasi tenetur asperiores rerum? Id ipsum quidem quos quaerat inventore veniam eos recusandae.",
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis explicabo dicta voluptas neque repellat numquam, veritatis fugit quasi tenetur asperiores rerum? Id ipsum quidem quos quaerat inventore veniam eos recusandae.",
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis explicabo dicta voluptas neque repellat numquam, veritatis fugit quasi tenetur asperiores rerum? Id ipsum quidem quos quaerat inventore veniam eos recusandae.",
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis explicabo dicta voluptas neque repellat numquam, veritatis fugit quasi tenetur asperiores rerum? Id ipsum quidem quos quaerat inventore veniam eos recusandae.",
    ],
  },
  {
    id: 2,
    title: "View",
    toggle: false,
    active: true,
    icon: false,
    content: [
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis explicabo dicta voluptas neque repellat numquam, veritatis fugit quasi tenetur asperiores rerum? Id ipsum quidem quos quaerat inventore veniam eos recusandae.",
    ],
  },
]);

function activeBody(index) {
  collapseableData.value[1].active = !this.collapseableData[1].active;
  collapseableData.value[1].icon = !collapseableData.value[1].icon;
  console.log(this.collapseableData[index].active);
  // collapseableData.value.forEach((item, id) => {
  //   if (id !== index) {
  //     item.active = false;
  //   }
  // });
}

function swap(index) {
  console.log("reverse");
  if (collapseableData.value[1].active) {
    collapseableData.value[1].active = !collapseableData.value[1].active;
  }
  collapseableData.value[index].toggle = !collapseableData.value[index].toggle;

  // Icon Active When Reverse
  collapseableData.value[0].icon = true;
  collapseableData.value[1].icon = true;
  console.log(collapseableData.value[index].toggle);
  setTimeout(() => {
    collapseableData.value[1].toggle = false;
    collapseableData.value[0].toggle = false;
    collapseableData.value = collapseableData.value.reverse();
  }, 500);
}
</script>

<style scoped>


.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.toogle-enter-from{
  transition: all 3s linear;
}
.toogle-enter-to{
  transition: all 3s linear;
}
.toogle-leave-to{
  transform: translateY(100px);
}

.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

</style>
