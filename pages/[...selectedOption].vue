<template>
    <div>
        <hea-der></hea-der>
        <div style="background-color: blue;
            position: absolute; top: 5px;
            text-align: center;
            width: 100vw;">{{ title_jove }}</div>
        <div>
            <me-nu></me-nu>
        </div>
        
        <br>THis is my Hello world, Thierry Nsanzumukiza</div>
    <!-- <NuxtPage/> -->
</template>
<script setup lang="ts">
import heaDer from '../views/hea-der.vue';
import meNu from '~/views/me-nu.vue';

const title_jove = "Welcome to the official website of Thierry"
</script>