<template>
    <div class="bg-gradient py-10">
        <div class="w-11/12 mx-auto mt-10 md:mt-28">
            <div>
                <div class="flex justify-center mb-3">
                    <img class="w-16"
                        src="https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcTUhN39dunzNkt4d438asFWey5ldBK3iTizctR-atLFPztqKcU9"
                        alt="">
                </div>
                <h4 class="text-2xl font-bold text-center">Contracted. Accustomed.</h4>
                <p class="text-lg text-gray-600 text-center mt-2 md:w-4/12 mx-auto">More than 5000 customers have already
                    tried Contractbook - see what they're saying!</p>
            </div>
            <div class="mt-5">
                <Carousel :items-to-show="1" :wrap-around="true">
                    <Slide v-for="(card, index) in cards" :key="index">
                        <a :href="card.link"
                            class="block max-w-sm px-5 py-10 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
                            <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">"{{ card.title
                            }}"
                            </h5>
                            <p class="font-normal text-gray-700 dark:text-gray-400">{{ card.description }}</p>
                            <div class="flex justify-center mt-5 mb-2">
                                <img class="w-16 h-16 rounded-full" :src="card.image" alt="Rounded avatar">
                            </div>
                            <p>{{ card.deg }}</p>
                        </a>
                    </Slide>

                    <template #addons>
                        <Navigation />
                    </template>
                </Carousel>
            </div>
            <div class="flex flex-col md:flex-row md:justify-center my-5">
                <button class="text-lg py-2 px-5 border rounded-lg border-blue-600 mr-2">See More Testimonials</button>
                <button class="text-lg py-2 px-5 border rounded-lg border-blue-600 text-white bg-blue-600">Join Contractbook Family</button>
            </div>
        </div>
    </div>
</template>
  
<script>
import { defineComponent } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
    name: 'WrapAround',
    components: {
        Carousel,
        Slide,
        Navigation,
    },
    data() {
        return {
            cards: [
                {
                    link: '#',
                    title: 'Serious time saver',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur vel orci nec metus malesuada tincidunt. Etiam quis dui condimentum, varius libero at, tempor neque.',
                    deg: "Paromita Haque, CEO at GoodCorp",
                    image: "https://flowbite.com/docs/images/people/profile-picture-1.jpg",
                },
                {
                    link: '#',
                    title: 'Serious time saver',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur vel orci nec metus malesuada tincidunt. Etiam quis dui condimentum, varius libero at, tempor neque.',
                    deg: "Paromita Haque, CEO at GoodCorp",
                    image: "https://flowbite.com/docs/images/people/profile-picture-2.jpg",
                },
                {
                    link: '#',
                    title: 'Serious time saver',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur vel orci nec metus malesuada tincidunt. Etiam quis dui condimentum, varius libero at, tempor neque.',
                    deg: "Paromita Haque, CEO at GoodCorp",
                    image: "https://flowbite.com/docs/images/people/profile-picture-3.jpg",
                },
            ],
        }
    },
})
</script>
  
<style>
.bg-gradient {
    background: linear-gradient(
    to bottom,
    #FFFFFF 50%,
    #F8F8FF 50%
)}



.carousel__item {
    min-height: 200px;
    width: 100%;
    background-color: var(--vc-clr-primary);
    color: var(--vc-clr-white);
    font-size: 20px;
    border-radius: 8px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.carousel__slide {
    padding: 10px;
}

.carousel__prev,
.carousel__next {
    box-sizing: content-box;
}</style>