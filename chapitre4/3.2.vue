<script setup lang="ts">
import { reactive } from 'vue'

// Objet reactif
const etat = reactive({
  compteur: 0,
  message: 'Bonjour',
  utilisateur: {
    nom: 'Alice',
    age: 25
  }
})

// Tableau reactif
const taches = reactive([
  { id: 1, texte: 'Tache 1', fait: false },
  { id: 2, texte: 'Tache 2', fait: true }
])

// Pas besoin de .value !
function incrementer() {
  etat.compteur++
}

function ajouterTache() {
  taches.push({
    id: taches.length + 1,
    texte: 'Nouvelle tache',
    fait: false
  })
}
</script>

<template>
  <p>Compteur: {{ etat.compteur }}</p>
  <p>Utilisateur: {{ etat.utilisateur.nom }}</p>

  <ul>
    <li v-for="tache in taches" :key="tache.id">
      {{ tache.texte }}
    </li>
  </ul>
</template>
