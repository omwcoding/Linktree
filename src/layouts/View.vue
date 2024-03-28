<template>
  <v-main :style="{ backgroundColor: data.secondaryColor }">
    <router-view />
  </v-main>
</template>

<script setup>
  import data from '@/data';
</script>
