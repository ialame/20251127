<script setup lang="ts">
import { ref } from 'vue'

const texte = ref('')
const nombre = ref(0)
const coche = ref(false)
const selection = ref('option1')
const selections = ref<string[]>([])
const choix = ref('')
</script>

<template>
  <!-- Input texte -->
  <input v-model="texte" type="text">
  <p>Texte: {{ texte }}</p>

  <!-- Input nombre -->
  <input v-model.number="nombre" type="number">

  <!-- Checkbox simple -->
  <input v-model="coche" type="checkbox" id="cb">
  <label for="cb">Accepter</label>

  <!-- Checkboxes multiples -->
  <input v-model="selections" type="checkbox" value="a"> A
  <input v-model="selections" type="checkbox" value="b"> B
  <input v-model="selections" type="checkbox" value="c"> C
  <!-- selections = ['a', 'c'] si A et C coches -->

  <!-- Radio buttons -->
  <input v-model="choix" type="radio" value="opt1"> Option 1
  <input v-model="choix" type="radio" value="opt2"> Option 2

  <!-- Select -->
  <select v-model="selection">
    <option value="option1">Option 1</option>
    <option value="option2">Option 2</option>
    <option value="option3">Option 3</option>
  </select>

  <!-- Select multiple -->
  <select v-model="selections" multiple>
    <option value="a">A</option>
    <option value="b">B</option>
    <option value="c">C</option>
  </select>

  <!-- Textarea -->
  <textarea v-model="texte"></textarea>
</template>
