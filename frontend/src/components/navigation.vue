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
