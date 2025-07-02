<script setup>
const items= [{
    id: 1,
    text: 'learn vue 3',
    done: true
}, {
    id: 2,
    text: 'learn vue router',
    done: false
}, {
    id: 3,
    text: 'learn vuex',
    done: false
}]
</script>

<template>
    <h1>Todo List</h1>
    <template v-for="item in items">
        <ul v-if="!item.done" :key="item.id">
        <li v-for="(value, key) in item">
            {{ key }} : {{ value }}
        </li>
    </ul>
    </template>

        <h1 v-for="n in 10">Hello {{ n }}</h1>
</template>