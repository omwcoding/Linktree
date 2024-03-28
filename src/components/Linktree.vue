<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" md="8" lg="6">
          <v-row align="center">
            <v-col cols="12" md="12" class="avatar">
              <v-avatar size="100">
                <v-img src="@/assets/brousers.jpg" alt="Bro Users" />
              </v-avatar>
            </v-col>
            <v-col cols="12" md="12">
              <v-card-title class="text-h5 text-center">I link dei Bro Users</v-card-title>
            </v-col>
          </v-row>
            <v-row justify="center">
              <v-col cols="12" v-for="(link, index) in links" :key="index">
                <v-btn
                  :href="link.url"
                  target="_blank"
                  color="primary"
                  class="link-button"
                  block
                >
                  <v-icon>{{ link.icon }}</v-icon>
                  <span>{{ link.name }}</span>
                </v-btn>
              </v-col>
            </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref } from 'vue';

const links = ref([
  { name: 'Instagram', url: 'https://instagram.com', icon: 'mdi-instagram' },
  { name: 'Telegram', url: 'https://t.me', icon: 'mdi-telegram' },
  { name: 'Chi siamo', url: '/#/brousers', icon: 'mdi-account' },
  { name: 'Contatti', url: '/#/contatti', icon: 'mdi-email' },
]);
</script>

<style>
.transparent-card {
  background-color: transparent !important;
}

.avatar {
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Personalizzazione dello stile dei bottoni */
.v-btn.link-button {
  margin-bottom: 8px; /* Aggiungi spazio tra i bottoni */
}
</style>
