<template>
    <div class="centered welcomeText bigWidth">
        <div class="mt-20 fw-b" style="font-family: Satisfy;">
            Nsanzumukiza Thierry Jovin
        </div> 
       
        <div class="m-20 c-b ff-o">
            Discover Thierry, a  Full Stack Developer based in 
            <span style="font-weight: 700;">Burundi</span>
            with 5+ years of experience in programming.
            
            Caring about good solution, satisfaction and happy coding in Python, Django & DRF, Vue.js, HTML and CSS.
        </div>
    </div>
</template>

<style>
.centered{
    text-align: center;
}
.welcomeText{
    font-family: Satisfy, sans-serif;
    font-size: 18px;

}
.mt-20{margin-top: 20px;}
.fw-b{font-weight: bolder;}
.m-20{margin: 20px;}
.c-b{color: brown;}
.ff-o{font-family: Sen, sans-serif; font-weight: 100;}


@media screen and (min-width: 850px) {
    .welcomeText{
        font-size: 1.5rem;
    }
}
@media screen and (min-width: 1050px){
    .bigWidth{
        max-width: 80%;
    }
}
</style>