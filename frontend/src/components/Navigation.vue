<template>
  <v-navigation-drawer
    expand-on-hover
    rail
  >
    <v-list>
      <v-list-item
        prepend-avatar="@/assets/VeloCloud.png"
        subtitle=".pdl@broadcom.com"
        title="SDE-TS-SASE-APAC"
      >
      <v-select
        :items="items"
        density="compact"
        label="LAB"
        variant="solo-filled"
        @update:modelValue="select"
      ></v-select>

      </v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list density="compact" nav>
      <v-list-item prepend-icon="mdi-wrench" title="Configeration" value="myfiles"></v-list-item>
      <v-list-item prepend-icon="mdi-dialpad" title="Verify" value="shared"></v-list-item>
      <v-list-item prepend-icon="mdi-call-split" title="Traffic" value="starred"></v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script lang="ts" setup>
import { ref, defineExpose, watchEffect, defineEmits } from 'vue';

// Define reactive variable for vlaus and items
const vlaus = ref('Access');
const items = ref(['Reservation', 'Five site','Three site']);

// Define custom event to emit updateComps
const emits = defineEmits(['updateComps']);

// Method to handle selection change and emit updateComps event
const select = (value: string) => {
  vlaus.value = value;
};

// Expose vlaus value to the parent component
defineExpose({
  vlaus,
});

// Emit the updateComps event when vlaus changes
watchEffect(() => {
  emits('updateComps');
});
</script>
