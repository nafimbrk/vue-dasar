<script setup>
import Counter from "./Counter.vue";    
import CounterStateles from "./CounterStateles.vue";
import { ref  } from "vue";

const counter1 = "Eko"
const counter2 = "Budi"

const counter = ref(0)

function increment(value) {
    counter.value += value
}
</script>

<template>
  <Counter :name="counter1" initial-count="10" /> 
  <Counter :name="counter2" initial-count="20" /> 

  <CounterStateles name="Joko" :counter="counter" :increment="1" @click="increment" />
  <CounterStateles name="Anwar" :counter="counter" :increment="2" @click="increment" />
</template>

<style scoped></style>
