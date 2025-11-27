<template>
  <div class="container">
    <h1>Titre</h1>
    <p>Paragraphe</p>
  </div>
</template>

<style scoped>
/* Ces styles s'appliquent UNIQUEMENT a ce composant */
.container {
  padding: 20px;
  background: #f5f5f5;
}

h1 {
  color: #42b883;
}

p {
  font-size: 16px;
}
</style>

<!--
Vue genere un attribut unique, ex: data-v-7ba5bd90
Le CSS devient:
.container[data-v-7ba5bd90] { ... }
h1[data-v-7ba5bd90] { ... }
-->
