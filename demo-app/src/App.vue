<script setup>
import { ref } from 'vue'

const userInput = ref('')
const message = ref('')
const checked = ref('not checked')
const fruit = ref([])
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
  <p>Fruits</p>
  <input id="Apple" v-model="fruit" type="checkbox"  value="Apple">
  <label for="Apple">Apple</label>
  <input id="Banana" v-model="fruit" type="checkbox" value="Banana">
  <label for="Banana">Banana</label>
  <input id="Grape" v-model="fruit" type="checkbox" value="Grape">
  <label for="Grape">Grape</label>
  <p>{{ fruit }}</p>
</template>

<style scoped>

</style>
