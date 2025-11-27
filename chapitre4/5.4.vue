<script setup lang="ts">
import { ref } from 'vue'

const compteur = ref(0)
const items = ref([1, 2, 3, 4, 5])
</script>

<template>
  <!-- v-once : rendu une seule fois, jamais re-rendu -->
  <h1 v-once>Titre statique: {{ compteur }}</h1>
  <!-- Meme si compteur change, le titre reste le meme -->

  <p>Compteur dynamique: {{ compteur }}</p>
  <button @click="compteur++">+1</button>

  <!-- v-memo : re-render seulement si les dependances changent -->
  <div v-for="item in items" :key="item" v-memo="[item]">
    <p>Item: {{ item }}</p>
    <p>Compteur: {{ compteur }}</p>
    <!-- Cette div n'est re-rendue que si 'item' change,
         pas quand 'compteur' change -->
  </div>
</template>
