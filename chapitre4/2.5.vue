<script setup lang="ts">
import { ref, computed } from 'vue'

const couleur = ref('red')
const taille = ref(16)

const stylesCalcules = computed(() => ({
  color: couleur.value,
  fontSize: `${taille.value}px`,
  fontWeight: 'bold'
}))
</script>

<template>
  <!-- Objet de styles (camelCase) -->
  <p :style="{ color: couleur, fontSize: taille + 'px' }">
    Texte style
  </p>

  <!-- Ou kebab-case avec quotes -->
  <p :style="{ 'font-size': taille + 'px' }">Texte</p>

  <!-- Avec computed -->
  <p :style="stylesCalcules">Texte calcule</p>

  <!-- Tableau de styles (fusion) -->
  <p :style="[stylesBase, stylesSpecifiques]">Texte</p>
</template>
