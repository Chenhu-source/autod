<template>
  <div>
    <!-- Pass the updateComps method as a prop to the navigation component -->
    <Navigation ref="nav" :update-comps="updateComps" />
  </div>
  <div>
    <!-- Conditional rendering based on the value of mains -->
    <component :is="comps"></component>
  </div>
</template>

<script lang="ts" setup>
import { ref, watchEffect } from 'vue';
import Reservation from '../components/Reservation.vue';
import Fivesite from '../components/Fivesite.vue';
import Threesite from '../components/Threesite.vue';
import Welcome from '../components/Welcome.vue';
import Navigation from '../components/Navigation.vue';

const nav = ref<null>(null); // Define ref for navigation component
const mains = ref(''); // Initialize mains ref with an empty string
const comps = ref<any>(null); // Initialize comps ref with null

// Method to reactively update comps based on mains
const updateComps = (value) => {
  if (value === 'Five site') {
    comps.value = Fivesite; // Display the AccessBar component
  } else if (value === 'Reservation') {
    comps.value = Reservation; // Display the Reservation component
  } else if (value === 'Three site') {
    comps.value = Threesite; // Display the Reservation component
  } else {
    comps.value = Welcome; // Display nothing if mains doesn't match any condition
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
