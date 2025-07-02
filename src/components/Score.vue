<script setup>
import { ref } from 'vue';

const score = ref(40)
</script>

<template>
    <h1>Score App</h1>
    <div v-show="score > 50">
        score is {{ score }}
    </div>
    <div v-if="score > 90">
        yay cool score {{ score }}
    </div>
    <div v-else-if="score > 70">
        good score {{ score }}
    </div>
    <div v-else>
        ups, bad score {{ score }}
    </div>
</template>

<style scoped>

</style>