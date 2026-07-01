<script setup>
const model = defineModel({
  type: String,
  default: 'default'
})
</script>
<template>
  <h2>CustomInput</h2>
  <input v-model="model" type="text">
  <p>model: {{ model }}</p>
</template>
