<script setup lang="ts">
const nom = 'Alice'
const age = 25
const date = new Date()
</script>

<template>
  <!-- Affichage simple -->
  <p>Bonjour {{ nom }}!</p>

  <!-- Expressions JavaScript -->
  <p>Age: {{ age }} ans</p>
  <p>Majeur: {{ age >= 18 ? 'Oui' : 'Non' }}</p>
  <p>Nom en majuscules: {{ nom.toUpperCase() }}</p>
  <p>Date: {{ date.toLocaleDateString('fr-FR') }}</p>

  <!-- Calculs -->
  <p>Dans 10 ans: {{ age + 10 }} ans</p>
</template>
