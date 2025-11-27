<script setup lang="ts">
import { ref } from 'vue'

// Creer des refs reactives
const compteur = ref(0)
const message = ref('Bonjour')
const estVisible = ref(true)

// Acceder/modifier avec .value dans le script
function incrementer() {
  compteur.value++
  console.log(compteur.value)
}

function changerMessage() {
  message.value = 'Au revoir'
}
</script>

<template>
  <!-- Dans le template, .value est automatique -->
  <p>Compteur: {{ compteur }}</p>
  <p>Message: {{ message }}</p>

  <button @click="incrementer">+1</button>
  <button @click="changerMessage">Changer</button>
</template>
