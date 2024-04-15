<template>
  <v-card
    class="mx-auto"
    max-width="450"
    text="If you want to check the status of Lab Booking, please log in first. Follow the prompts."
    title="Login Lab Booking"
  >

    <template v-slot:actions>
      <v-btn
        :loading="loading"
        class="flex-grow-1"
        height="48"
        variant="tonal"
        @click="openGoogle"
      >
        Login
      </v-btn>
    </template>
  </v-card>
</template>

<script setup>
import { ref } from 'vue';

const loading = ref(false);

const openGoogle = () => {
  window.open('http://10.121.10.174/admin.php', '_blank');
};
</script>
