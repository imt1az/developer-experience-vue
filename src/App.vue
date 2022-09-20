<template>
  <Layout @clickedOnHome="handleClickOnHome">

    <Collapseable :data="collapseableData"></Collapseable>
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
    toggle: true,
    active:false,
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
    toggle: true,
    active:true,
    content: [
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis explicabo dicta voluptas neque repellat numquam, veritatis fugit quasi tenetur asperiores rerum? Id ipsum quidem quos quaerat inventore veniam eos recusandae.",
    ],
  },
]);

function handleClickOnTitle() {
  collapseableData.value = collapseableData.value.reverse();
}

function handleClickOnHome() {
  console.log("Hello");
}
</script>
