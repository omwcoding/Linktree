<template>
  <v-footer elevation="2" class="custom-footer">
    <v-row no-gutters>
      <v-col class="text-center mt-1" cols="12">
        {{ new Date().getFullYear() }} —
        <strong>{{ data.name }}</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script setup>
import data from '@/data';
</script>

<style>
.custom-footer {
  max-height: 40px; /* Modifica la massima altezza del footer secondo le tue preferenze */
  background-color: rgba(255, 255, 255, 0.3); /* Imposta un colore di sfondo trasparente con opacità */
}
.custom-footer .text-center {
  font-size: 15px; /* Riduci la dimensione del testo del footer */
  margin-top: 0; /* Riduci il margine superiore del testo del footer */
}
</style>
