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
      <v-btn class="tmplsrouter" variant="text" :href="links.mplsrouter">@@@</v-btn>
      <v-btn class="tce1" variant="text" :href="links.ce1">@@@</v-btn>
      <v-btn class="tce2" variant="text" :href="links.ce2">@@@</v-btn>
      <v-btn class="tlegacype" variant="text" :href="links.ce3">@@@</v-btn>
      <v-btn class="tpe1" variant="text" :href="links.pe1">@@@</v-btn>
      <v-btn class="tpe2" variant="text" :href="links.pe2">@@@</v-btn>
      <v-btn class="tcr-internet" variant="text" :href="links.internet">@@@</v-btn>
      <v-btn class="tcr-internet1" variant="text" :href="links.internet1">@@@</v-btn>
      <v-btn class="tcr-internet2" variant="text" :href="links.internet2">@@@</v-btn>
      <v-btn class="twansim1" variant="text" :href="links.wansim1">@@@</v-btn>
      <v-btn class="tswitch1" variant="text" :href="links.switch1">@</v-btn>
      <v-btn class="tswitch2" variant="text" :href="links.switch2">@</v-btn>

      <v-btn class="tvce1" variant="text" :href="links.vce1">@@@</v-btn>
      <v-btn class="tvce2" variant="text" :href="links.vce2">@@@</v-btn>
      <v-btn class="tvce3" variant="text" :href="links.vce3">@@@</v-btn>
      <v-btn class="tvcg1" variant="text" :href="links.vcg1">@@@</v-btn>
      <v-btn class="tvcg2" variant="text" :href="links.vcg2">@@@</v-btn>

      <v-btn class="tvco" variant="text" :href="links.vco">@@@</v-btn>
      <v-btn class="tgw1" variant="text" :href="links.gw1">@@@</v-btn>
      <v-btn class="tvcmp" variant="text" :href="links.vcmp">@@@</v-btn>
      <v-btn class="tdc" variant="text" :href="links.dc">@@@</v-btn>


      <v-btn class="trouted1" variant="text" :href="links.routed1">@@@</v-btn>
      <v-btn class="tclient1" variant="text" :href="links.client1">@@@</v-btn>
      <v-btn class="trouted2" variant="text" :href="links.routed2">@@@</v-btn>
      <v-btn class="tclient2" variant="text" :href="links.client2">@@@</v-btn>
      <v-btn class="tclient3" variant="text" :href="links.client3">@@@</v-btn>
      <v-btn class="tlegacyclient" variant="text" :href="links.legacyclient">@@@</v-btn>

    </v-img>
  </v-card> 
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue';

const model = ref('10.121.10.34');

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
  .tmplsrouter{
    left: 660px;
    top: 40px;
  }
  .tce1{
    left: 230px;
    top: 110px;
  }
  .tce2{
    left: 510px;
    top: 245px;
  }
  .tlegacype{
    left: 800px;
    top: 135px;
  }
  .tpe1{
    left: 980px;
    top: 495px;
  }
  .tpe2{
    left: 960px;
    top: 570px;
  }
  .tcr-internet{
    left: 270px; 
    top: 500px; 
  }
  .tcr-internet1{
    left: 120px;
    top: 570px;
  }
  .tcr-internet2{
    left: 200px;
    top: 570px;
  }
  .twansim1{
    left: 145px;
    top: 330px;
  }
  .tswitch1{
    left: -580px;
    top: 310px;
  }
  .tswitch2{
    left: -300px;
    top: 195px;
  }
  .tvce1{
    left: -550px;
    top: 300px;
  }
  .tvce2{
    left: -405px;
    top: 305px;
  }
  .tvce3{
    left: -215px;
    top: 235px;
  }
  .tvcg1{
    left: 10px;
    top: 500px;
  }
  .tvcg2{
    left: -60px;
    top: 580px;
  }
  .tvco{
    left: -355px;
    top: 730px;
  }
  .tgw1{
    left: -600px;
    top: 730px;
  }
  .tvcmp{
    left: -845px;
    top: 750px;
  }
  .tdc{
    left: 730px;
    top: 830px;
  }
  .trouted1{
    left:90px; 
    top: 190px; 
  }
  .tclient1{
    left: 205px; 
    top: 160px; 
  }
  .trouted2{
    left: 290px; 
    top: 65px; 
  }
  .tclient2{
    left: 275px;
    top: 125px;
  }
  .tclient3{
    left: 410px; 
    top: 115px; 
  }
  .tlegacyclient{
    left: 580px; 
    top: 200px; 
  }
  
</style>