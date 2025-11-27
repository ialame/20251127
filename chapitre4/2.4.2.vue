<script setup lang="ts">
import { ref } from 'vue'

const classeActive = ref('active')
const classeErreur = ref('')
</script>

<template>
  <!-- Tableau de classes -->
  <div :class="[classeActive, classeErreur]">Element</div>

  <!-- Avec ternaire -->
  <div :class="[estActif ? 'active' : 'inactive', 'base']">
    Element
  </div>

  <!-- Objet dans tableau -->
  <div :class="['base', { active: estActif }]">Element</div>
</template>
