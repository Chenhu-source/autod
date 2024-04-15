<template>
    <v-card
      class="image-container"
      rounded="0"
    >
      <v-responsive class="mx-auto" max-width="344">
        <v-text-field v-model="model" hide-details="auto" label="Management IP" clearable></v-text-field>
      </v-responsive>
      <v-img
        class="image-container"
        src="@/assets/ThreeSite.png"
        cover
      >
      <!---router and switch --->
        <v-btn class="mplsrouter" variant="text" :href="links.mplsrouter">@@@</v-btn>
      </v-img>
    </v-card> 
  </template>
  
  <script lang="ts" setup>
  import { ref, computed } from 'vue';
  
  const model = ref('10.121.10.37');
  
  const links = computed(() => {
    return {
      mplsrouter: `ssh://root@${model.value}:2162`,
    };
  });
  </script>
  
  <style>
    .image-container {
      width: 1538px; 
      height: 1000px; 
      overflow: hidden; 
    }
    .mplsrouter{
      left: 710px; 
      top: 80px; 
    }
  </style>