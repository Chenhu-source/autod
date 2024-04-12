
<template>
  <v-select
    :items="items"
    density="compact"
    label="LAB"
    @update:modelValue="select"
  ></v-select>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';
  import { useRouter } from 'vue-router'; 

  const router = useRouter();
  const items = ref([
    'Reservation',
    'Access',
  ]);
 
  const select = function (value) {
    if (value === 'Reservation') {
      router.push('/reservation');
    }
    if (value === 'Access') {
      router.push('/labaccess');
    }
  }
</script>
