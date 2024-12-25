<template>
    <div>
        <div style="width: 100%;height: 30px"></div>
        <div style="width: 100%;height: 40px;display: flex;
            justify-content: center; align-items: center;
            margin-bottom: 15px;">{{ title_jove }}</div>
        <me-nu></me-nu>
        
        <!-- <br>THis is my Hello world, Thierry Nsanzumukiza -->
    </div>
    <!-- <NuxtPage/> -->
</template>
<script setup lang="ts">
import meNu from '~/views/me-nu.vue';

const title_jove = "My interests are shared here"
</script>