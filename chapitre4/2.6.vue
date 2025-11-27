<script setup lang="ts">
import { ref } from 'vue'

const compteur = ref(0)

function incrementer() {
  compteur.value++
}

function gererClick(event: MouseEvent) {
  console.log('Position:', event.clientX, event.clientY)
}

function saluer(nom: string) {
  alert(`Bonjour ${nom}!`)
}
</script>

<template>
  <!-- Syntaxe complete -->
  <button v-on:click="incrementer">+1</button>

  <!-- Syntaxe raccourcie (recommandee) -->
  <button @click="incrementer">Compteur: {{ compteur }}</button>

  <!-- Expression inline -->
  <button @click="compteur++">+1 inline</button>

  <!-- Avec argument -->
  <button @click="saluer('Alice')">Saluer</button>

  <!-- Acces a l'evenement -->
  <button @click="gererClick">Click</button>

  <!-- $event pour l'evenement natif avec arguments -->
  <button @click="gererClick($event)">Click</button>
</template>
