<template>
  <div>
    <hr />
    <h1>Im da foooteer</h1>
    <hr />
    <h2>Iteration4:</h2>
    <div v-for="(eachPost, index) in data" :key="index">
      <h1 :class="color ? 'bgColor' : 'bgSinColor'">
        {{ index }}-{{ eachPost.title }}
      </h1>
      <p>{{ eachPost.description }}</p>
      <p>{{ eachPost.content }}</p>
    </div>

    <button @click="color = !color">click</button>
    <!-- "In this case"->              colorfunction  same as color =!color-->
  </div>
</template>

<script setup>
import { ref } from "vue";

const data = ref([
  {
    title: "El marinero",
    description: "un pato muy salvaje que mata cocodrilos",
    content: "aaaaaaaa",
  },
  {
    title: "El submarinero",
    description: "un pez nemo que mata tiburones",
    content: "bbbbbbb",
  },
  {
    title: "El oceanero",
    description: "anashe description about how a ocean can be cocinero",
    content: "xdddddddddd",
  },
]);

let color = ref(true);
const colorfunction = () => {
  color.value = !color.value;
};
console.log(colorfunction());
</script>

<style scoped>
.bgColor {
  background-color: green;
}
.bgSinColor {
  background-color: red;
}
</style>
