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
      src="@/assets/FiveSite.png"
      cover
    >
    <!---router and switch --->
      <v-btn class="mplsrouter" variant="text" :href="links.mplsrouter">@@@</v-btn>
      <v-btn class="ce1" variant="text" :href="links.ce1">@@@</v-btn>
      <v-btn class="ce2" variant="text" :href="links.ce2">@@@</v-btn>
      <v-btn class="ce3" variant="text" :href="links.ce3">@@@</v-btn>
      <v-btn class="legacype" variant="text" :href="links.legacype">@@@</v-btn>
      <v-btn class="ce4" variant="text" :href="links.ce4">@@@</v-btn>
      <v-btn class="pe1" variant="text" :href="links.pe1">@@@</v-btn>
      <v-btn class="pe2" variant="text" :href="links.pe2">@@@</v-btn>
      <v-btn class="cr-internet" variant="text" :href="links.internet">@@@</v-btn>
      <v-btn class="cr-internet1" variant="text" :href="links.internet1">@@@</v-btn>
      <v-btn class="cr-internet2" variant="text" :href="links.internet2">@@@</v-btn>
      <v-btn class="wansim1" variant="text" :href="links.wansim1">@@@</v-btn>
      <v-btn class="wansim2" variant="text" :href="links.wansim2">@@@</v-btn>
      <v-btn class="switch1" variant="text" :href="links.switch1">@</v-btn>
      <v-btn class="switch2" variant="text" :href="links.switch2">@</v-btn>
      <v-btn class="switch5" variant="text" :href="links.switch5">@</v-btn>
      
      <!---velocloud --->
      <v-btn class="vce1" variant="text" :href="links.vce1">@@@</v-btn>
      <v-btn class="vce2" variant="text" :href="links.vce2">@@@</v-btn>
      <v-btn class="vce3" variant="text" :href="links.vce3">@@@</v-btn>
      <v-btn class="vce4" variant="text" :href="links.vce4">@@@</v-btn>
      <v-btn class="vce5" variant="text" :href="links.vce5">@@@</v-btn>
      <v-btn class="vcg1" variant="text" :href="links.vcg1">@@@</v-btn>
      <v-btn class="vcg2" variant="text" :href="links.vcg2">@@@</v-btn>
      <v-btn class="vco" variant="text" :href="links.vco">@@@</v-btn>
      <v-btn class="gw1" variant="text" :href="links.gw1">@@@</v-btn>
      <v-btn class="gw2" variant="text" :href="links.gw2">@@@</v-btn>
      <v-btn class="vcmp" variant="text" :href="links.vcmp">@@@</v-btn>
      <v-btn class="dc" variant="text" :href="links.dc">@@@</v-btn>


      <!---client --->
      <v-btn class="routed1" variant="text" :href="links.routed1">@@@</v-btn>
      <v-btn class="client1" variant="text" :href="links.client1">@@@</v-btn>
      <v-btn class="routed2" variant="text" :href="links.routed2">@@@</v-btn>
      <v-btn class="client2" variant="text" :href="links.client2">@@@</v-btn>
      <v-btn class="client3" variant="text" :href="links.client3">@@@</v-btn>
      <v-btn class="client4" variant="text" :href="links.client4">@@@</v-btn>
      <v-btn class="clientd4" variant="text" :href="links.clientd4"></v-btn>
      <v-btn class="legacyclient" variant="text" :href="links.legacyclient">@@@</v-btn>
      <v-btn class="routed5" variant="text" :href="links.routed5">@@@</v-btn>
      <v-btn class="client5" variant="text" :href="links.client5">@@@</v-btn>
    </v-img>
  </v-card> 
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue';

const model = ref('10.121.10.37');

const links = computed(() => {
  return {
    mplsrouter: `ssh://root@${model.value}:2162`,
    ce1: `ssh://root@${model.value}:2156`,
    ce2: `ssh://root@${model.value}:2158`,
    ce3: `ssh://root@${model.value}:2159`,
    legacype: `ssh://root@${model.value}:2160`,
    ce4: `ssh://root@${model.value}:2157`,
    pe1: `ssh://root@${model.value}:2153`,
    pe2: `ssh://root@${model.value}:2160`,
    internet: `ssh://root@${model.value}:2164`,
    internet1: `ssh://root@${model.value}:2023`,
    internet2: `ssh://root@${model.value}:2165`,
    wansim1: `ssh://root@${model.value}:2152`,
    wansim2: `ssh://root@${model.value}:2024`,
    switch1: `ssh://root@${model.value}:2030`,
    switch2: `ssh://root@${model.value}:2163`,
    switch5: `ssh://root@${model.value}:2031`,
    vce1: `ssh://root@${model.value}:1001`,
    vce2: `ssh://root@${model.value}:1002`,
    vce3: `ssh://root@${model.value}:1003`,
    vce4: `ssh://root@${model.value}:1004`,
    vce5: `ssh://root@${model.value}:1005`,
    vcg1: `ssh://root@${model.value}:2011`,
    vcg2: `ssh://root@${model.value}:2012`,
    vco: `ssh://root@${model.value}:9999`,
    gw1: `ssh://root@${model.value}:2040`,
    gw2: `ssh://root@${model.value}:2041`,
    vcmp: `ssh://root@${model.value}:2050`,
    dc: `ssh://root@${model.value}:2070`,
    routed1: `ssh://root@${model.value}:2006`,
    client1: `ssh://root@${model.value}:2001`,
    routed2: `ssh://root@${model.value}:2151`,
    client2: `ssh://root@${model.value}:2002`,
    client3: `ssh://root@${model.value}:2003`,
    client4: `ssh://root@${model.value}:2004`,
    clientd4: `ssh://root@${model.value}:2004`,
    legacyclient: `ssh://root@${model.value}:2161`,
    routed5: `ssh://root@${model.value}:2007`,
    client5: `ssh://root@${model.value}:2005`,
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
  .ce1{
    left: 310px; 
    top: 145px; 
  }
  .ce2{
    left: 420px; 
    top: 145px; 
  }
  .ce3{
    left: 560px; 
    top: 145px; 
  }
  .legacype{
    left: 910px; 
    top: 160px; 
  }
  .ce4{
    left: 30px; 
    top: 780px; 
  }
  .pe1{
    left: 930px; 
    top: 505px; 
  }
  .pe2{
    left: 905px; 
    top: 570px; 
  }
  .cr-internet{
    left: 170px; 
    top: 500px; 
  }
  .cr-internet1{
    left: 20px; 
    top: 570px; 
  }
  .cr-internet2{
    left: 100px; 
    top: 570px; 
  }
  .wansim1{
    left: 170px; 
    top: 350px; 
  }
  .wansim2{
    left: 180px; 
    top: 350px; 
  }
  .switch1{
    left: -720px; 
    top: 320px; 
  }
  .switch2{
    left: -460px; 
    top: 225px; 
  }
  .switch5{
    left: -850px; 
    top: 630px; 
  }
  .vce1{
    left: -750px; 
    top: 320px; 
  }
  .vce2{
    left: -670px; 
    top: 335px; 
  }
  .vce3{
    left: -515px; 
    top: 275px; 
  }
  .vce4{
    left: -360px; 
    top: 275px; 
  }
  .vce5{
    left: -1015px; 
    top: 635px; 
  }
  .vcg1{
    left: 1180px; 
    top: 475px; 
  }
  .vcg2{
    left: 1100px; 
    top: 550px; 
  }
  .vco{
    left: 780px; 
    top: 690px; 
  }
  .gw1{
    left: 500px; 
    top: 690px; 
  }
  .gw2{
    left: 500px; 
    top: 690px; 
  }
  .vcmp{
    left: 240px; 
    top: 700px; 
  }
  .dc{
    left: 325px; 
    top: 880px; 
  }
  .routed1{
    left: -270px; 
    top: 215px; 
  }
  .client1{
    left: -170px; 
    top: 185px; 
  }
  .routed2{
    left: 20px; 
    top: 185px; 
  }
  .client2{
    left: -80px; 
    top: 295px; 
  }
  .client3{
    left: 10px; 
    top: 145px; 
  }
  .client4{
    left: 120px; 
    top: 155px; 
  }
  .clientd4{
    left: 50px; 
    top: 105px; 
  }
  .legacyclient{
    left: 170px; 
    top: 240px; 
  }
  .routed5{
    left: -870px; 
    top: 690px; 
  }
  .client5{
    left: -720px; 
    top: 660px; 
  }
</style>