<template>
<div class="px-6 py-4">
<div class="relative ">
    <img v-touch:swipe="swipeHandler" class="w-full" :src="showing.src" alt="">
        <div id="cornav" class="absolute top-5 flex mx-2">
            <svg v-for="items in 5" class="mx-1 corsvg" width="50%" style="fill:rgb(221 215 215); opacity:61% ; " height="8" >
                <rect width="100%" height="8"   />
                </svg>
        </div>
        <div class="absolute bg-gradient-to-t from-black bottom-0 pt-5 w-full  z-10">
            <div class="flex justify-between items-center px-3 pb-6">
                <div class="text-white">
                    <div class="flex items-center pb-2">
                        <p class="text-2xl font-semibold ">{{showing.name}}</p>&nbsp;&nbsp;
                        <p class="text-sm font-medium">({{showing.price}}USD)</p>
                    </div>
                    <div class="flex items-center">
                        <img src="../static/home/location.png" alt="">&nbsp;&nbsp;
                        <p>{{showing.distance}} Kilometers away</p>
                    </div>
                    
                </div>
                <img class="h-full" src="../static/home/info.png" alt="">
            </div>
            <div class="flex justify-around">
                <NuxtLink to="home"><img src="../static/home/reload.png" alt=""></NuxtLink>
                <NuxtLink to="home"><img src="../static/home/close.png" alt=""></NuxtLink>
                <NuxtLink to="home"><img src="../static/home/msg.png" alt=""></NuxtLink>
                <NuxtLink to="home"><img src="../static/home/like.png" alt=""></NuxtLink>
                <NuxtLink to="home"><img src="../static/home/car.png" alt=""></NuxtLink>
            </div>
    </div>
</div>

</div>

</template>

<script>
import Vue from 'vue'
import Vue2TouchEvents from 'vue2-touch-events'

Vue.use(Vue2TouchEvents)
export default{
    methods: {
        swipeHandler (direction) {
            if(direction=='right'){
                
                if((this.index-1)<0){
                    this.index = this.cordata.length-1
                }
                else{
                    this.index -= 1
                }
            }
            else if(direction=='left'){
                 if((this.index+2)>this.cordata.length){
                    this.index = 0
                }
                else{
                    this.index += 1
                }
            }
            let corsvg = document.getElementsByClassName("corsvg");
            var len =  corsvg.length;
            for(var i=0 ; i<len; i++){
            corsvg[i].style.fill = "#9A9A9A"
            corsvg[i].style.opacity = "63%"
            }
            const element = document.getElementById("cornav");
            let numb = element.childNodes[this.index] 
             numb.style.opacity = "100";
             numb.style.fill = "#fff"
        }
        
    },
    computed:{
        showing(){
            return this.cordata[this.index]
        }
    },
    data(){
        return{
            index:2,
            cordata:[
                {
                name:'Charlotte',
                src:'../_nuxt/static/Rectangle.png',
                price:'100',
                distance:'1'
                },
                {
                name:'Asim',
                src:'../_nuxt/static/girl2.jpg',
                price:'200',
                distance:'2'
                },
                {
                name:'Annus',
                src:'../_nuxt/static/Rectangle.png',
                price:'300',
                distance:'3'
                },
                {
                name:'Shehzad',
                src:'../_nuxt/static/girl2.jpg',
                price:'400',
                distance:'4'
                },
                {
                name:'Shehzad',
                src:'../_nuxt/static/girl2.jpg',
                price:'500',
                distance:'5'
                },
            ]
        }
    }
}

</script>