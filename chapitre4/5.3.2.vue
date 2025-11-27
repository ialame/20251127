<script setup lang="ts">
import { ref, computed } from 'vue'

const taches = ref([
  { id: 1, texte: 'Tache 1', fait: false },
  { id: 2, texte: 'Tache 2', fait: true },
  { id: 3, texte: 'Tache 3', fait: false }
])

// BONNE PRATIQUE : filtrer avec computed
const tachesActives = computed(() =>
  taches.value.filter(t => !t.fait)
)
</script>

<template>
  <!-- MAUVAIS : v-if et v-for sur le meme element -->
  <!-- v-if a priorite, tache n'existe pas encore! -->
  <!--
  <li v-for="tache in taches" v-if="!tache.fait" :key="tache.id">
    {{ tache.texte }}
  </li>
  -->

  <!-- BON : utiliser computed -->
  <li v-for="tache in tachesActives" :key="tache.id">
    {{ tache.texte }}
  </li>

  <!-- OU : v-if sur un parent/template -->
  <template v-for="tache in taches" :key="tache.id">
    <li v-if="!tache.fait">
      {{ tache.texte }}
    </li>
  </template>
</template>
