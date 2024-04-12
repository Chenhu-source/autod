<template>
  <div>
    <!-- Pass the updateComps method as a prop to the navigation component -->
    <navigation ref="nav" :update-comps="updateComps" />
  </div>
  <div>
    <!-- Conditional rendering based on the value of mains -->
    <component :is="comps"></component>
  </div>
</template>

<script lang="ts" setup>
import { ref, watchEffect } from 'vue';
import reservation from '../components/reservation.vue';
import navigation from '../components/navigation.vue'; // Import the Navigation component
import fivesite from '../components/fivesite.vue';

const nav = ref<InstanceType<typeof navigation> | null>(null); // Define ref for navigation component
const mains = ref(''); // Initialize mains ref with an empty string
const comps = ref<any>(null); // Initialize comps ref with null

// Method to reactively update comps based on mains
const updateComps = (value) => {
  if (value === 'Five site') {
    comps.value = fivesite; // Display the AccessBar component
  } else if (value === 'Reservation') {
    comps.value = reservation; // Display the Reservation component
  } else {
    comps.value = null; // Display nothing if mains doesn't match any condition
  }
};

// Watch for changes in nav and update mains accordingly
watchEffect(() => {
  mains.value = nav.value?.vlaus;
});

// Define a watcher to reactively update comps based on mains
watchEffect(() => {
  updateComps(mains.value);
});

</script>
