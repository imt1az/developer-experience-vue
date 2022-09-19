
<template>
<Layout>
<Collapseable
      @clickedOnTittle="handleClickOnTitle"
      v-for="item in collapseableData"
      :key="item.id"
    >
      <template #title>{{ item.title }}</template>
      
      <h1 class="text-3xl text-center font-bold mb-4">{{ item.title }}</h1>
      <p class="my-10" v-for="(paragraph, i) in item.content" :key="i">
        {{ paragraph }}
      </p>
    </Collapseable>

</Layout>
</template>

<script setup>
import { ref } from "vue";
import Layout from "./components/Layout.vue";
import Content from "./components/Content.vue";
import Collapseable from "./components/Collapseable.vue";
const currentOpenIndex = ref(0);
const collapseableData = ref([
  {
    id: 1,
    title: "User",
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
    content: [
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis explicabo dicta voluptas neque repellat numquam, veritatis fugit quasi tenetur asperiores rerum? Id ipsum quidem quos quaerat inventore veniam eos recusandae.",
    ],
  },
]);

function handleClickOnTitle() {
  collapseableData.value = collapseableData.value.reverse();
}
</script>




