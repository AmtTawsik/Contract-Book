<template>
    <div class="mt-10 md:mt-28">
        <div class="flex justify-center mb-3">
            <img class="w-16" :src="logo1" alt="">
        </div>
        <h4 class="text-center text-3xl md:text-4xl font-semibold">From creation</h4>
        <h4 class="text-center text-3xl md:text-4xl font-semibold mb-3">to management</h4>
        <p class="text-center text-lg text-gray-600 md:w-5/12 mx-auto md:px-7">Say goodbye to printers, paper and time wasted on creating, signing and storing your contracts. No more printer frustrations. Contractbook makes it all digital and hassle-free.</p>
        <div class="my-5 md:my-10">
            <img class="w-full" :src="fullimg" alt="">
        </div>
        <div class="flex justify-center">
            <button class="py-2.5 px-5 text-violet-600 hover:text-violet-700 font-semibold border border-violet-500 hover:border-violet-600">Watch the Video</button>
        </div>
    </div>
</template>

<script setup>
import logo1 from '../../assets/images/logo1.png'
import fullimg from '../../assets/images/fullimg.png'
</script>