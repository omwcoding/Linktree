<template>
  <v-footer elevation="2" :color="data.primaryColor">
    <v-row no-gutters>
      <v-col class="text-center mt-4" cols="12">
        {{ new Date().getFullYear() }} —
        <strong>{{ data.name }}</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script setup>
  import data from '@/data';
</script>
