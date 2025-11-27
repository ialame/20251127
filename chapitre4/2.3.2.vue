<script setup lang="ts">
const attributsInput = {
  id: 'username',
  type: 'text',
  placeholder: 'Entrez votre nom',
  required: true
}
</script>

<template>
  <!-- Lier tous les attributs d'un objet -->
  <input v-bind="attributsInput">
  <!-- Equivalent a:
       <input id="username" type="text"
              placeholder="Entrez votre nom" required> -->
</template>
