<template>
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="8" lg="6">
          <v-card>
            <v-row align="center">
              <v-col cols="auto">
                <v-avatar size="48">
                  <v-icon size="36">mdi-account-group</v-icon>
                </v-avatar>
              </v-col>
              <v-col>
                <v-card-title class="text-h5 text-center">I link dei Bro Users</v-card-title>
              </v-col>
            </v-row>
            <v-card-text>
              <v-list dense>
                <v-list-item
                  v-for="(link, index) in links"
                  :key="index"
                  :href="link.url"
                  target="_blank"
                >
                  <v-list-item-icon>
                    <v-icon>{{ link.icon }}</v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title>{{ link.name }}</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-card-text>
          </v-card>
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
  /* Add custom styles here */
  </style>
  