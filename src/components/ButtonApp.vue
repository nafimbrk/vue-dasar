<script setup>
import MyButton from './MyButton.vue';
import Container from './Container.vue';

function clickHandler() {
    alert('you click me')
}
</script>

<template>
    <Container title="Contoh Button">
        <template #header="attributes">
            <h1>Button App {{ attributes.counter }}</h1>
        </template>
        <template v-slot:default="attributes">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero sed asperiores reprehenderit maiores ut impedit ipsam est cum reiciendis perferendis?</p>
            <MyButton class="button" @click="clickHandler" :name="attributes.counter" contoh="Kurniawan" />
        </template>
        <template #footer>
            <p>aksjgfdsfsdfgsdfsf</p>
        </template>
    </Container>
</template>

<style scoped>
.button {
    background-color: blue;
    color: white;
}
</style>