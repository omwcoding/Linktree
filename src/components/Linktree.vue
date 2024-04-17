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
              <v-card-title class="text-h5 text-center title-card">I link dei Bro Users</v-card-title>
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
  { name: 'Instagram', url: 'https://instagram.com/bro__users', icon: 'mdi-instagram' },
  { name: 'Wannight Bot', url: 'https://t.me/wannight_bot', icon: 'mdi-telegram' },
  { name: 'Chi siamo', url: '/#/brousers', icon: 'mdi-account' },
  { name: 'Contatti', url: '/#/contattaci', icon: 'mdi-email' },
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

.avatar img {
  max-width: 100%;
  max-height: 100%;
  object-fit: cover;
}

.v-btn.link-button {
  margin-bottom: 8px;
}

.background-clip {
  background-clip: text;
}

.title-card {
  background: linear-gradient(to right, purple, rgb(29, 123, 154), rgb(112, 255, 112));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  -webkit-text-fill-color: transparent;
  position: relative;
}

.title-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5); /* Adjust color and transparency as needed */
  backdrop-filter: blur(10px); /* Adjust blur radius as needed */
  z-index: -1;
}
</style>
