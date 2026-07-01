<script setup>
import { ref } from 'vue'

const userInput = ref('')
const message = ref('')
const checked = ref('not checked')
const fruit = ref([])

const gender = ref('male')

const selected = ref([])
</script>
<template>
  <h1>v-model</h1>
  <h2>text</h2>
  <input v-model.lazy.trim.number="userInput" type="text">
  <p>{{ userInput }}</p>
  <h2>textarea</h2>
  <textarea v-model.trim="message"></textarea>
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

  <h2>Radio</h2>
  <input id="male" v-model="gender" type="radio" value="male">
  <label for="male">male</label>
  <input id="female" v-model="gender" type="radio" value="female">
  <label for="female">female</label>
  <p>{{ gender }}</p>

  <h2>Select</h2>
  <select v-model="selected" multiple>
    <option value="" disabled>Select One</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <p>{{ selected }}</p>
</template>

<style scoped>

</style>
