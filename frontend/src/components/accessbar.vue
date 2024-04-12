<template>
  <v-sheet class="mx-auto" width="300">
    <v-form @submit.prevent="handleSubmit">
      <v-text-field
        v-model="ip"
        :rules="rules"
        label="Management IP"
      ></v-text-field>
      <v-select
        v-model="selectedItem"
        label="Type"
        :items="['Five site', 'Three site']"
      ></v-select>
      <v-btn class="mt-2" type="submit" block>Submit</v-btn>
    </v-form>
  
  </v-sheet>
</template>

<script lang="ts" setup>
  // Import necessary libraries
  import { ref } from 'vue';
  import { useRouter } from 'vue-router'; 

  // Declare reactive variables
  const router = useRouter();
  const selectedItem = ref('');
  const ip = ref('');

  // Define validation rules
  const rules = [
    value => {
      if (value) return true
      return 'You must enter a Management IP.'
    },
  ];

  // Define form submission handler
  const handleSubmit = function() {
    if (selectedItem.value === 'Five site') {
      router.push({ 
        path: '/labssh', 
        params: { ip: ip.value },
      });
    } else {
      router.push('/reservation');
    }
  }
</script>

