<script setup lang="ts">
import { ref } from 'vue'

const estActif = ref(true)
const aErreur = ref(false)
</script>

<template>
  <!-- Classe conditionnelle -->
  <div :class="{ active: estActif }">Element</div>
  <!-- Si estActif = true : <div class="active"> -->

  <!-- Plusieurs classes conditionnelles -->
  <div :class="{
    active: estActif,
    'text-danger': aErreur,
    disabled: !estActif
  }">
    Element
  </div>

  <!-- Combinaison avec classe statique -->
  <div class="base" :class="{ active: estActif }">
    Element
  </div>
  <!-- Resultat : <div class="base active"> -->
</template>
