<template>
<div class="px-6 py-4">
<div class="relative ">
    <img class="w-full" src="../static/Rectangle.png" alt="">
        <div class="absolute bg-gradient-to-t from-black bottom-0 pt-5 w-full  z-10">
            <div class="flex justify-between items-center px-3 pb-6">
                <div class="text-white">
                    <div class="flex items-center pb-2">
                        <p class="text-2xl font-semibold ">Charlotte</p>&nbsp;&nbsp;
                        <p class="text-sm font-medium">(300USD)</p>
                    </div>
                    <div class="flex items-center">
                        <img src="../static/home/location.png" alt="">&nbsp;&nbsp;
                        <p>3 Kilometers away</p>
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