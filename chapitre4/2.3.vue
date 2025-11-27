<script setup lang="ts">
const imageUrl = '/images/logo.png'
const altText = 'Logo Vue.js'
const lienActif = true
const inputId = 'email-input'
</script>

<template>
  <!-- Syntaxe complete -->
  <img v-bind:src="imageUrl" v-bind:alt="altText">

  <!-- Syntaxe raccourcie (recommandee) -->
  <img :src="imageUrl" :alt="altText">

  <!-- Attribut dynamique -->
  <a :href="lienActif ? '/dashboard' : '#'">Dashboard</a>

  <!-- Plusieurs attributs -->
  <input :id="inputId" :name="inputId" type="email">
</template>
