<script setup lang="ts">
import { ref, computed } from 'vue'

const prenom = ref('Alice')
const nom = ref('Dupont')
const articles = ref([
  { nom: 'Article 1', prix: 10, quantite: 2 },
  { nom: 'Article 2', prix: 25, quantite: 1 },
  { nom: 'Article 3', prix: 15, quantite: 3 }
])

// Computed en lecture seule
const nomComplet = computed(() => {
  return `${prenom.value} ${nom.value}`
})

const total = computed(() => {
  return articles.value.reduce((sum, article) => {
    return sum + article.prix * article.quantite
  }, 0)
})

const nombreArticles = computed(() => articles.value.length)

// Computed avec getter et setter
const nomCompletEditable = computed({
  get() {
    return `${prenom.value} ${nom.value}`
  },
  set(nouveauNom: string) {
    const [p, n] = nouveauNom.split(' ')
    prenom.value = p
    nom.value = n || ''
  }
})
</script>

<template>
  <p>Nom complet: {{ nomComplet }}</p>
  <p>Total: {{ total }} EUR</p>
  <p>{{ nombreArticles }} articles</p>

  <!-- Computed avec setter -->
  <input v-model="nomCompletEditable">
</template>
