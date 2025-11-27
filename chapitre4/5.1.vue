<script setup lang="ts">
import { ref } from 'vue'

const estConnecte = ref(false)
const role = ref('utilisateur')
const score = ref(75)
</script>

<template>
  <!-- v-if simple -->
  <p v-if="estConnecte">Bienvenue!</p>

  <!-- v-if / v-else -->
  <div v-if="estConnecte">
    <p>Contenu pour utilisateur connecte</p>
  </div>
  <div v-else>
    <p>Veuillez vous connecter</p>
  </div>

  <!-- v-if / v-else-if / v-else -->
  <p v-if="score >= 90">Excellent!</p>
  <p v-else-if="score >= 70">Bien</p>
  <p v-else-if="score >= 50">Passable</p>
  <p v-else>Insuffisant</p>

  <!-- Avec role -->
  <nav v-if="role === 'admin'">
    <a href="/admin">Administration</a>
  </nav>
  <nav v-else-if="role === 'moderateur'">
    <a href="/moderation">Moderation</a>
  </nav>
  <nav v-else>
    <a href="/profil">Mon profil</a>
  </nav>
</template>
