<script setup>
import { ref } from 'vue'
import CustomInput from './components/CustomInput.vue';
const userInput = ref('hello')
</script>

<template>
  <h1>v-model</h1>
  <CustomInput v-model="userInput" />
  <p>userInput: {{ userInput }}</p>
</template>
