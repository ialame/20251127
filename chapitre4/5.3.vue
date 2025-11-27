<script setup lang="ts">
import { ref } from 'vue'

const fruits = ref(['Pomme', 'Banane', 'Orange'])

const utilisateurs = ref([
  { id: 1, nom: 'Alice', age: 25 },
  { id: 2, nom: 'Bob', age: 30 },
  { id: 3, nom: 'Charlie', age: 35 }
])

const objet = ref({
  titre: 'Mon objet',
  auteur: 'Alice',
  date: '2025-01-15'
})
</script>

<template>
  <!-- Iteration sur un tableau -->
  <ul>
    <li v-for="fruit in fruits" :key="fruit">
      {{ fruit }}
    </li>
  </ul>

  <!-- Avec index -->
  <ul>
    <li v-for="(fruit, index) in fruits" :key="index">
      {{ index + 1 }}. {{ fruit }}
    </li>
  </ul>

  <!-- Tableau d'objets (TOUJOURS utiliser :key avec id unique) -->
  <div v-for="user in utilisateurs" :key="user.id" class="card">
    <h3>{{ user.nom }}</h3>
    <p>Age: {{ user.age }} ans</p>
  </div>

  <!-- Iteration sur un objet -->
  <ul>
    <li v-for="(valeur, cle) in objet" :key="cle">
      {{ cle }}: {{ valeur }}
    </li>
  </ul>

  <!-- Avec index aussi -->
  <li v-for="(valeur, cle, index) in objet" :key="cle">
    {{ index }}. {{ cle }}: {{ valeur }}
  </li>

  <!-- Iteration sur un nombre -->
  <span v-for="n in 5" :key="n">{{ n }} </span>
  <!-- 1 2 3 4 5 -->
</template>
