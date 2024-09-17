<script setup>
    import { ref } from 'vue'

    import skirteez from '@/assets/projects/skirteez.png'
    import ebarangay from '@/assets/projects/e-barangay.png'
    import howtell from '@/assets/projects/howtell.png'
    import sports from '@/assets/projects/sports.png'
    import resteria from '@/assets/projects/resteria.png'

    import html from '@/assets/techs/html.svg'
    import css from '@/assets/techs/css.svg'
    import js from '@/assets/techs/js.svg'
    import php from '@/assets/techs/php.svg'
    import sql from '@/assets/techs/sql.svg'
    import vue from '@/assets/techs/vue.svg'
    import tw from '@/assets/techs/tw.svg'
    import lv from '@/assets/techs/lv.svg'

    const projs = ref([
        {
            title: 'Skirteez',
            img: skirteez,
            description: 'Skirteez is an online platform showcasing various types of skirts, from preloved to new, offering a range of affordable, high-quality options.',
            tools: [html,css,js,tw],
            
        },
        {
            title: 'Barangay Dosuno',
            img: ebarangay,
            description: 'This website provides essential information about Barangay Dosuno, allowing residents to easily request barangay clearance,and indigency certificates',
            tools: [tw, vue, lv, sql],
        },
        {
            title: 'Howtell',
            img: howtell,
            description: 'Howtell offers detailed information on available hotels, providing an easy way for users to find accommodations that suit their needs.',
            tools: [html,css,js],
        },
        {
            title: 'Resteria',
            img: resteria,
            description: 'Resteria is an online food ordering system that not only lets users place orders but also incorporates sentiment analysis to enhance customer experience.',
            tools: [html,css,js,php],
        },
        {
            title: 'Sports Website',
            img: sports,
            description: 'This platform features a variety of basketball exercises and drills, helping athletes improve their skills through guided training routines.',
            tools: [vue,tw],
        },

    ])
</script>


<template>
    <hr class="my-6 h-px border-t-0 bg-transparent bg-gradient-to-r from-transparent via-neutral-500 to-transparent opacity-25 dark:via-neutral-400" />
    <section class="relative p-8 md:p-14">
        <div class="pb-8">
            <h1 class="text-3xl md:text-4xl font-bold text-center text-white ">Featured Projects</h1>
        </div>
        <div class="flex flex-wrap gap-4 justify-center text-white">
            <div v-for="proj in projs" :key="proj.title" class="rounded-xl overflow-hidden border border-gray-600 max-w-sm">
                <div class="relative rounded-lg">
                    <img class="w-full" :src="proj.img" alt="Product Image">
                </div>
                <div class="p-4">
                    <h3 class="text-lg font-medium mb-2">{{proj.title}}</h3>
                    <p class="text-gray-400 text-sm mb-4">{{proj.description}}</p>
                    <div class="flex items-center justify-between mt-10">
                        <div class="text-gray-400 text-sm">
                            <div class="flex items-center text-md font-semibold">Technology</div>
                            <!-- Looping through tools -->
                            <ul class="flex flex-row mt-2 space-x-3">
                                <li v-for="tool in proj.tools" :key="tool" class="text-gray-500">
                                    <img :src="tool" alt="" class="w-5 h-5">
                                </li>
                            </ul>
                        </div>
                        <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded">
                            Repository
                        </button>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>