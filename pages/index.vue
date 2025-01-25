<template>
    <div>
        <div style="width: 100%;height: 30px"></div>
        <div style="width: 100%;height: 40px;display: flex;
            justify-content: center; align-items: center;
            margin-bottom: 15px;font-family: 'Satisfy'; font-size: larger;">{{ title_jove }}</div>
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
