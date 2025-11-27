<script setup lang="ts">
const estDesactive = true
const estCoche = false
</script>

<template>
  <!-- L'attribut est present si true, absent si false -->
  <button :disabled="estDesactive">Envoyer</button>
  <!-- Resultat : <button disabled>Envoyer</button> -->

  <input type="checkbox" :checked="estCoche">
  <!-- Resultat : <input type="checkbox"> (pas de checked) -->
</template>
