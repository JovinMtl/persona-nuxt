<template>
    <div class="openImage t-a">
        <img src="/personaFoto/jove_-18_.png" class="im"></img>
        <blockquote class="quote c">
            <span class="bq-1 v-a m-50 l-h c d-i">“</span>
            <span class="d-i">Before downloading one file, please delete two.</span>
            <span class="bq-2 v-a m-50 l-h c d-i">”</span>
            <span class="author">— Th. Jov. Nsanzumukiza</span>
        </blockquote>            
    </div>
</template>

<style>
.openImage{
    text-align: center;
    display: inline-block;
    text-align: center;
    width: 90vw;
    height: auto;
    border-radius: 18px;
}
.t-a{
    text-align: center;
}
.im{
    border-radius:200px;
    margin-top:-10px; 
    border: 12px double black;
}
.quote {
    font-size: 20px;
    font-style: italic;
    border-left: 4px solid salmon ;
    padding-left: 20px;
    padding-right: 20px;
    margin: 20px 0;
}
.c{
    color: #333;
}
.bq-1{
    font-size: 72px;
}
.v-a{
    vertical-align: middle;
}
.m-50{
    margin-top: -50px;
}
.l-h{
    line-height: 0;
}
.d-i{
    display: inline;
    font-family: rubik;
}
.bq-2{
    font-size: 42px;
}
.author{
    display: block;
    font-size: 20px;
    font-weight: bold;
    color: #666;
    margin-top: 10px;
}


@media screen and (min-width: 850px) {
    .openImage{
        width: 45vw;
    }
    .im{
        border-radius: 500px;
    }
}
</style>
