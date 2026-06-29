<script setup>
import { ref } from 'vue'

const userInput = ref('')
const message = ref('')
const checked = ref('not checked')

</script>
<template>
  <h1>v-model</h1>
  <h2>text</h2>
  <input v-model="userInput" type="text">
  <p>{{ userInput }}</p>
  <h2>textarea</h2>
  <textarea v-model="message"></textarea>
  <p style="white-space: pre;">{{ message }}</p>
  <h2>CheckBox</h2>
  <input id="checkbox" type="checkbox" v-model="checked" true-value="checked" false-value="not checked"/>
  <label for="checkbox">{{ checked }}</label>
</template>

<style scoped>

</style>
