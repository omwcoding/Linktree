<template>
  <v-main class="main-background">
    <router-view />
  </v-main>
</template>

<script setup>
import data from '@/data';
</script>

<style>
.main-background {
  background-image: url("@/assets/background.jpg"); /* Imposta l'immagine di sfondo */
  background-size: cover; /* Imposta il ridimensionamento dell'immagine */
  background-position: center center; /* Centra l'immagine */
  /* Aggiungi altre regole di stile necessarie */
}
</style>
