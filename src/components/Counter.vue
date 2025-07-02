<script setup>
import { nextTick, ref } from 'vue'

console.log('load component');
let counter = ref({
    count: 0,
    name: 'Eko'
})

async function increment() {
    console.info(`increment count : ${counter.value.count}`)
    counter.value = {
        name: counter.value.name,
        count: counter.value.count + 1
    }

    await nextTick()

    counter.value.count++
    
    await nextTick()

    counter.value.count++
    
    await nextTick()

    console.log('increment count after nexttick');
    
}
</script>

<template>
    <div>
        <h1 id="count">Counter {{ counter.name }} : {{ counter.count }}</h1>
        <button v-on:click="increment">Incremet</button>
    </div>
</template>

<style scoped>
</style>