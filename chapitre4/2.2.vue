<script setup lang="ts">
const texte = 'Bonjour <strong>Vue.js</strong>'
const html = '<span style="color: red">Texte rouge</span>'
</script>

<template>
  <!-- v-text : equivalent a {{ }} -->
  <p v-text="texte"></p>
  <!-- Resultat : Bonjour <strong>Vue.js</strong> (echappe) -->

  <!-- v-html : interprete le HTML -->
  <p v-html="html"></p>
  <!-- Resultat : Texte rouge (en rouge) -->
</template>
