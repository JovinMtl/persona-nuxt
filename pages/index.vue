<template>
    <div>
        <div style="width: 100%;height: 10px"></div>
        <h2 style="width: 100%;height: 50px;display: flex;
            justify-content: center; align-items: center;
            margin-bottom: 15px;font-family: 'Satisfy';font-weight: 400;">{{ title_jove }}</h2>
        <me-nu></me-nu>

        <div>
          <div id="e" class="menuContainer" style="display: flex;justify-content: center;">
            <show-pic></show-pic>
          </div>
          <div class="centered">
              <open-pic></open-pic>
          </div>
          <div class="centered">
                <sum-mary></sum-mary>
          </div>
          <div class="centered">
              <my-offer></my-offer>
          </div> 
        </div>  
        
        <!-- <br>THis is my Hello world, Thierry Nsanzumukiza -->
    </div>
    <!-- <NuxtPage/> -->
</template>
<script setup lang="ts">
import meNu from '~/views/me-nu.vue';
import showPic from '~/views/show-pic.vue';
import openPic from '~/views/open-pic.vue';
import sumMary from '~/views/sum-mary.vue';
import myOffer from '~/views/my-offer.vue';

const title_jove = "Welcome to the official website of Thierry"
</script>
