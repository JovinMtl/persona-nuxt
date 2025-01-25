<template>
    <div style="display: flex; justify-content: center;">
        <div style="background-color: rgba(155,55,105,0.2);" v-if="actualOption"  :style="{
            border: `2px solid ${offers[actualOption].color}`,
            borderRadius: '20px',
            margin: '5px 20px',
            padding: '10px 10px',
            }" class="bigWidth">
            <span :style="{
                fontWeight: 'bolder', 
                borderBottom: `2px solid ${offers[actualOption].color}`,
                display:'block',
                margin: '0px -12px',
                paddingBottom: '5px',
                }">
                {{ offers[actualOption].title }}
            </span>  <br>
            {{ offers[actualOption].content }}
        </div>
    </div>
    <br>
    <div id="connect" class="ff-1" style="font-weight: bolder;
        margin-left: -0.5rem;">
        <span style="color: brown; font-size: 18px">Connect with me</span>  
        <span style="position: relative; top: .6rem; 
                font-size: 2rem;">
            <span style="margin-left: .3rem; top: 3rem;">&nbsp;</span>
            <a href="https://www.linkedin.com/in/thierry-nsanzumukiza-9b8bb1109" 
                target="_blank"  rel="noopener noreferrer" style="color: blue;">
                <svg xmlns="http://www.w3.org/2000/svg" width="2rem" height="2rem" viewBox="-2 -2 24 24"><g fill="blue"><path d="M15 11.13v3.697h-2.143v-3.45c0-.866-.31-1.457-1.086-1.457c-.592 0-.945.398-1.1.784c-.056.138-.071.33-.071.522v3.601H8.456s.029-5.842 0-6.447H10.6v.913l-.014.021h.014v-.02c.285-.44.793-1.066 1.932-1.066c1.41 0 2.468.922 2.468 2.902M6.213 5.271C5.48 5.271 5 5.753 5 6.385c0 .62.466 1.115 1.185 1.115h.014c.748 0 1.213-.496 1.213-1.115c-.014-.632-.465-1.114-1.199-1.114m-1.086 9.556h2.144V8.38H5.127z"/><path d="M4 2a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V4a2 2 0 0 0-2-2zm0-2h12a4 4 0 0 1 4 4v12a4 4 0 0 1-4 4H4a4 4 0 0 1-4-4V4a4 4 0 0 1 4-4"/></g></svg>
            </a>
            <span style="margin-left: .9rem;">&nbsp;</span>
            <a href="mailto:nsanzumukizath@gmail.com" style="color: blue;">
                <svg xmlns="http://www.w3.org/2000/svg" width="2rem" height="2rem" viewBox="0 0 20 20"><path fill="blue" d="M15.5 4A2.5 2.5 0 0 1 18 6.5v8a2.5 2.5 0 0 1-2.5 2.5h-11A2.5 2.5 0 0 1 2 14.5v-8A2.5 2.5 0 0 1 4.5 4zM17 7.961l-6.746 3.97a.5.5 0 0 1-.426.038l-.082-.038L3 7.963V14.5A1.5 1.5 0 0 0 4.5 16h11a1.5 1.5 0 0 0 1.5-1.5zM15.5 5h-11A1.5 1.5 0 0 0 3 6.5v.302l7 4.118l7-4.12v-.3A1.5 1.5 0 0 0 15.5 5"/></svg>
            </a>
            <span style="margin-left: .9rem; color:'black'">&nbsp;</span>
            <a href="https://wa.me/+25779071453" style="color: green;">
                <Icon name="line-md:linkedin" style="color: black" />

            </a>
            
            
            
        </span>
        
    </div>
    <!-- //copright -->
</template>
<script lang="ts">
import { computed, defineComponent } from 'vue'
import { Offer } from '../auxiliaire/types'
export default defineComponent ({
    props:[
        'option',
    ],
    setup(props) {
        const offers:Offer = [
            {
                'title':'',
                'content':'',
                'color': ''
            },
            {
                'title' : "Let's consider contract",
                'content' : `This is the most of the part I wish you could work with me.
                    In this setting, I can forget about ever-changing aspirations and settle my mind 
                    at developping my career within your environment. Being among your favorite achievers would
                    motivate me as long as my values are aligned with your corporate goals.`,
                'color' : 'black'
            },
            {
                'title' : "For individuals",
                'content' : `This is something we can negotiate. 
                        I'm eager to get started working on your project.`,
                'color': 'salmon'
            }
        ]
        const actualOption = computed(()=>{
            return props.option
        })
        return {
            actualOption, offers,
        }
    },
})
</script>

