<template>
  <div>
    <h1>Iteration2</h1>
    <p>
      This is my firt sum:={{ numero }}+{{ numero }}={{ suma }} ;) xdddddddd
      <br />
      asifhuvsdvhf 2+ 2= {{ 2 + 2 }}
    </p>
    <div>
      <h1>part2ofinteraction2</h1>
      <input type="text" v-model="number1" />
      <input type="text" v-model="number2" />
      <p>Now the new result is: {{ result }}</p>
    </div>
    <hr />
    <h1>Iteration3</h1>
    <p v-if="conditional">La variable conditional es true</p>
    <p v-else>La variable conditional es false</p>
    <h3>v show</h3>
    <p v-show="conditional">La variable conditional es true</p>
    <p v-show="conditionalfalsaaa">La variable conditional es false</p>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";
const number1 = ref("0");
const number2 = ref("0");
const result = computed(() => {
  return parseInt(number1.value) + parseInt(number2.value);
});

const numero = ref(2);
const suma = ref(numero.value + numero.value);
const conditional = ref(true);
const conditionalfalsaaa = ref(false);
</script>

<style scoped></style>
