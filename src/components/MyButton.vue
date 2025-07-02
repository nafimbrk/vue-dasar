<script setup>
import { useAttrs } from 'vue';

const props = defineProps(['contoh'])
console.log(props);

const atrributes = useAttrs()
console.log(atrributes);
</script>

<template>
    <button>My Button : {{ atrributes.name }}</button>
</template>

<style scoped>

</style>