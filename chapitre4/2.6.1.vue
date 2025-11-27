<template>
  <!-- .prevent : preventDefault() -->
  <form @submit.prevent="soumettre">
    <button type="submit">Envoyer</button>
  </form>

  <!-- .stop : stopPropagation() -->
  <div @click="parent">
    <button @click.stop="enfant">Ne propage pas</button>
  </div>

  <!-- .once : s'execute une seule fois -->
  <button @click.once="executerUneFois">Une fois</button>

  <!-- .self : seulement si l'evenement vient de l'element lui-meme -->
  <div @click.self="divClick">
    <button>Le click ici ne declenche pas divClick</button>
  </div>

  <!-- Combinaison de modificateurs -->
  <form @submit.prevent.stop="soumettre"></form>

  <!-- .capture : mode capture -->
  <div @click.capture="handler">...</div>

  <!-- .passive : pour le scroll (performance) -->
  <div @scroll.passive="onScroll">...</div>
</template>
