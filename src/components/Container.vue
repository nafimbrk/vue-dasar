<script setup>
import { ref, useSlots } from 'vue';

const counter = ref(0)
</script>

<template>
  <div v-if="$slots.header">
    <slot name="header" :counter="counter">
        <p>Default Header</p>
    </slot>
  </div>
  <div v-if="$slots.default">
    <slot name="default" :counter="counter">
        <p>Default Content</p>
    </slot>
  </div>
  <div v-if="$slots.footer">
    <slot name="footer" :counter="counter">
        <p>Default Footer</p>
    </slot>
  </div>
  <div>
    <button @click="counter++">Increment Counter</button>
  </div>
</template>

<style scoped></style>
