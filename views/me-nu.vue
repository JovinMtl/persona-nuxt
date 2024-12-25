<template>
    <div class="menuSticky">
        <div class="centered menu">
            <div class="menuContent">
                
                <nuxt-link to="/" class="unline" :class="!opt1 ? 'unclicked':'clicked'">
                    <div class=" fs tex">Home</div></nuxt-link>
                    <!-- <router-link to="" class="unline fs tex">
                        Home
                    </router-link> -->
                
                <nuxt-link to="portfolio" class="unline" 
                    :class="!opt2 ? 'unclicked wantClick':'clicked'">
                    <div class="fs tex">
                        Portfolio
                    </div>
                </nuxt-link>
                
                <nuxt-link  to="interests" class="unline" :class="!opt3 ? 'unclicked':'clicked'">
                    <div class="fs tex">
                        Interests
                    </div>
                </nuxt-link >
                <nuxt-link  to="/" class="unline" :class="!opt4 ? 'unclicked':'clicked'">
                    <div class="fs tex">
                        Contact
                    </div>
                </nuxt-link >
            </div>
        </div>
    </div>
</template>
<script setup lang="ts">
import { ref, onMounted } from 'vue'

const p = defineProps(['active'])
const opt1 = ref<boolean>(false)
const opt2 = ref<boolean>(false)
const opt3 = ref<boolean>(false)
const opt4 = ref<boolean>(false)

console.log("The menu selected is: ", p)
const disablingAnime = ()=>{
    // will select that element with 'anime' class and 
    // remove such properties making animation
    const animatedElement = document.querySelector('.wantClick')
    // get its styles properties
    const ani_s = getComputedStyle(animatedElement)
    console.log("First the animation name is : ", ani_s.getPropertyValue('animation-name'))
    animatedElement.style.animationName = 'Jove'
    console.log("Now the animation name is : ", ani_s.getPropertyValue('animation-name'))
}
</script>


<style scoped>
.centered{
    text-align: center;
}
.menu{
    background-color: #c5b5a1;
}
.unline{
    text-decoration: none;
    color: white;
}
.wantClick{
    animation-name: newThing;
    animation-iteration-count: infinite;
    animation-duration: 1s;
    animation-timing-function: ease;
    animation-delay: 15s;
}
@keyframes newThing {
    0%{
        transform: rotate(15deg);
    }
    40%{
        transform: rotate(-15deg);
        background-color: salmon;
    }
    90%{
        transform: rotate(0deg);
    }
}
.menuContent{
    display: inline-flex;
}
.clicked{
    display: inline-flex;
    align-content: center; 
    align-items: center;
    text-align: center;
    height: 41px; 
    width: 20vw; 
    background-color: black;
    border-radius: 25px;
    border: 3px solid black;
    margin-left: 1vw;
    transition-duration: 1s;
    transition-property: all;

}
.unclicked{
    display: inline-flex;
    margin: auto;
    height: 41px; 
    width: 20vw; 
    background-color: red;
    border-radius: 25px;
    border: 3px solid black;
    margin-left: 1vw;
}
.unline{
    text-decoration: none;
    color: white;
}
.wantClick{
    animation-name: newThing;
    animation-iteration-count: infinite;
    animation-duration: 1s;
    animation-timing-function: ease;
    animation-delay: 15s;
}
.tex{
    display: inline-flex; 
    text-align: center;
    margin: auto;
}
.menuSticky{
    position: sticky;
    top: 0;
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-bottom: 1px groove rgba(255, 255, 255, 0.26);
    margin: -20px;
}
.menu{
    display: inline-block;
    position: relative;
    text-align: center;
    align-content: center;
    align-items: center;
    width: 90vw;
    height: 40px;
    border-radius: 25px;
    padding-right: 1vw;
}
.menuContent{
    display: inline-flex;
}

@media screen and (min-width: 260px) {
    .fs{
        font-size: 11px;
    }
    .menuSticky{
        height: 60px;
        backdrop-filter: hue-rotate(120deg) blur(4px);
        -webkit-backdrop-filter: hue-rotate(120deg) blur(4px);
    }
}
@media screen and (min-width: 370px) {
    .fs{
        font-size: 13px;
    }
}
@media screen and (min-width: 470px) {
    .fs{
        font-size: 16px;
    }
}


@media screen and (min-width: 600px) {
    .menu{
        display: inline-block;
        position: relative;
        background-color: transparent;
        text-align: center;
        align-content: center;
        align-items: center;
        width: 75vw;
        height: 40px;
        border-radius: 25px;
        padding-right: 1vw;
    }
    .menuSticky{
        height: 80px;
        backdrop-filter: hue-rotate(120deg) blur(12px);
        -webkit-backdrop-filter: hue-rotate(120deg) blur(12px);
    }
    
    .unclicked{
        height: 41px; 
        width: 12vw; 
        background-color: red;
        align-content: center; 
        border-radius: 25px;
        border: 3px solid black;
        margin-left: 1vw;
    }
    .fs{
        font-size: 18px;
    }
}
@media screen and (min-width: 850px) {
    .fs{
        font-size: 20px;
    }
    .welcomeText{
        font-size: 1.5rem;
    }
    .menuSticky{
        height: 120px;
        padding-bottom: .6rem;
    }
    .unclicked{
        height: 50px;
    }
    .clicked{
        height: 50px;
    }
}
</style>