<template>
    <div>
        <div style="background-color: red;
            width: 100%;height: 50px;display: flex;
            justify-content: center;
            margin-bottom: 10px;">This is the title</div>
        <me-nu></me-nu>
        <div v-if="choiceMenu==1" style="
            position: relative;
            text-align: center;
            margin: 20px;
            width: 100vw;">
            <summ-ary></summ-ary>
        </div>
        <div v-if="choiceMenu==2" style="
            position: relative;
            text-align: center;
            margin: 20px;
            width: 100vw;">
            <port-folio></port-folio>
        </div>
        
        <!-- <br>THis is my Hello world, Thierry Nsanzumukiza -->
    </div>
    <!-- <NuxtPage/> -->
</template>
<script setup lang="ts">
import heaDer from '../views/hea-der.vue';
import meNu from '~/views/me-nu.vue';
import summAry from '~/views/summ-ary.vue';
import portFolio from '~/views/port-folio.vue';

const title_jove = "Welcome to the official website of Thierry"
const route = useRoute()
const choiceMenu = ref(1)
if(route.params.selectedOption == 'portfolio'){
    choiceMenu.value = 2
}
</script>