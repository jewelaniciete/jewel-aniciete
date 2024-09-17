<script setup>
import { ref } from 'vue'

import fb from '@/assets/socials/fb.svg'
import link from '@/assets/socials/linkedin.svg'
import git from '@/assets/socials/github.svg'
import red from '@/assets/socials/reddit.svg'

const socials = ref([
                {
                    title: 'Facebook',
                    img: fb,
                    link: 'https://www.facebook.com/jewel.aniciete',
                },
                {
                    title: 'Linkdn',
                    img: link,
                    link: 'https://www.linkedin.com/in/jewel-aniciete-236313212/',
                },
                {
                    title: 'Github',
                    img: git,
                    link: 'https://github.com/jewelaniciete',
                },
                {
                    title: 'Reddit',
                    img: red,
                    link: 'https://www.reddit.com/user/AJ7_Prod/',
                },
            ])

</script>

<template>
    <section class="relative p-8 md:p-14">
        <div class="grid md:grid-cols-12">
            <!-- 10% Width Column -->
            <div class="order-2 md:order-1 md:col-span-2 md:px-16 flex-row md:flex-col flex gap-1 md:gap-4 pt-4 w-full">
                <div v-for="social in socials" :key="social.title" class="flex items-center">
                    <a :href="social.link" target="_blank" rel="noopener" class="flex flex-col md:flex-row items-center gap-2">
                        <img class="rounded-full max-w-[70%] md:max-w-[40%] mx-auto hover-trigger shadow-lg shadow-gray-900" :src="social.img" alt="">
                        <p class="text-center text-md text-white font-bold p-1 hover-popup opacity-0 transition-opacity duration-300">{{ social.title }}</p>
                    </a>
                </div>
            </div>
            <!-- 80% Width Column -->
            <div class="order-1 md:order-2 md:col-span-8 w-full mx-auto py-12 md:px-16 flex-col flex gap-4 justify-center items-center pb-2 pt-4">
                <div class="card w-60">
                    <div class="card__content text-center relative py-32 transition-transform duration-1000 text-white font-bold">
                        <img src="@/assets/hero_image.jpg" alt="My Image" class="card__front absolute top-0 bottom-0 right-0 left-0 rounded-full shadow-lg shadow-gray-900">
                        <img src="@/assets/header_image.jpg" alt="My Image" class="card__back absolute top-0 bottom-0 right-0 left-0 rounded-full shadow-lg shadow-gray-900 ">
                    </div>
                </div>
                
                <div class="w-full flex flex-col justify-center items-center gap-2 text-white dark:text-gray-800 md:mt-0">
                    <h2 class="capitalize text-xl text-white font-semibold">Hi, I'm Jewel Aniciete</h2>
                    <h1 class="text-4xl md:text-5xl text-white font-bold text-center">WEB DEVELOPER</h1>
                    <a href="mailto:jewelaniciete@gmail" class="text-white text-lg">jewelaniciete@gmail.com</a>
                    <div class="grid grid-cols-2 gap-5 sm:mt-4 xs:mt-2">
                        <!-- <button class="px-6 py-1 border text-white rounded-sm">Download Resume</button>
                        <button class="px-6 py-1 border text-white rounded-sm">Contact Me</button> -->
                    </div>
                </div>
            </div>
            <!-- 10% Width Column -->
            <div class="hidden md:order-3 md:col-span-2 w-full mx-auto py-12 md:px-16 flex-col md:flex justify-center items-center pb-10 pt-4 relative">
                <div class="absolute bottom-4 p-2 flex gap-2 flex-row justify-center items-cente">
                    <img class="rounded-full mx-auto" src="@/assets/socials/image.png" alt="My Image" />
                </div>
            </div>
        </div>
    </section>
</template>

<style>
.card { perspective: 800px;}
.card__content {transform-style: preserve-3d;}
.card:hover .card__content {transform: rotateY(.5turn);}

.card__front,
.card__back { backface-visibility: hidden;}
.card__back{ transform: rotateY(.5turn);}


  /* Show the p element when the image is hovered */
  .hover-trigger:hover + .hover-popup {
    opacity: 1;
  }

  /* Transition effect for the popup */
  .hover-popup {
    transition: opacity 0.3s ease;
    pointer-events: none; /* Avoid blocking hover */
  }
</style>

