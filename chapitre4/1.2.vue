<script setup lang="ts">
// Logique du composant (Composition API)
import { ref } from 'vue'

const message = ref('Bonjour Vue!')
</script>

<template>
  <!-- Structure HTML du composant -->
  <div class="container">
    <h1>{{ message }}</h1>
  </div>
</template>

<style scoped>
/* Styles CSS (scoped = locaux au composant) */
.container {
  padding: 20px;
}

h1 {
  color: #42b883;
}
</style>
