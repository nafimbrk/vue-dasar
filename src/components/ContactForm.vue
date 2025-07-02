<script setup>
const model = defineModel({
  type: Object,
  required: true,
  get: (value) => {
    value.email = value.email.toUpperCase()
    return value
  }
});
</script>

<template>
  <h1>Contact Us</h1>
  <form>
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="model.name" />
    </div>
    <div>
      <label for="email">Email</label>
      <input type="email" id="email" v-model="model.email" />
    </div>
    <div>
      <label for="age">Age</label>
      <input type="number" id="age" v-model="model.age" />
    </div>
    <div>
      <label for="type">Type</label>
      <select name="type" id="type" v-model="model.type">
        <option value="Regular">Regular</option>
        <option value="VIP">VIP</option>
      </select>
    </div>
    <div>
      <label for="complain">Complain</label>
      <input type="checkbox" id="complain" v-model="model.complain" />
    </div>
    <div>
      <label for="message">Message</label>
      <textarea name="message" id="message" v-model="model.message"></textarea>
    </div>
  </form>
</template>

<style scoped></style>
