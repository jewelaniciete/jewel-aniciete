<script setup>
import { ref } from 'vue'

import html from '@/assets/techs/html.svg'
import css from '@/assets/techs/css.svg'
import js from '@/assets/techs/js.svg'
import php from '@/assets/techs/php.svg'
import java from '@/assets/techs/java.svg'
import sql from '@/assets/techs/sql.svg'

import vue from '@/assets/techs/vue.svg'
import nuxt from '@/assets/techs/nuxt.svg'
import lv from '@/assets/techs/lv.svg'
import tw from '@/assets/techs/tw.svg'
import bs from '@/assets/techs/bs.svg'

import gh from '@/assets/socials/github.svg'
import gl from '@/assets/techs/gitlab.svg'
import fm from '@/assets/techs/figma.svg'
import ab from '@/assets/techs/adobe.svg'

const progs = ref([
                {
                    title: 'HTML',
                    img: html,
                },
                {
                    title: 'CSS',
                    img: css,
                },
                {
                    title: 'Javascript',
                    img: js,
                },
                {
                    title: 'PHP',
                    img: php,
                },
                {
                    title: 'Java',
                    img: java,
                },
                {
                    title: 'SQL',
                    img: sql,
                },
                {
                    title: 'Vue',
                    img: vue,
                },
                {
                    title: 'Nuxt',
                    img: nuxt,
                },
                {
                    title: 'Laravel',
                    img: lv,
                },
                {
                    title: 'Tailwind',
                    img: tw,
                },
                {
                    title: 'Bootstrap',
                    img: bs,
                },
                {
                    title: 'Github',
                    img: gh,
                },
                {
                    title: 'Gitlab',
                    img: gl,
                },
                {
                    title: 'Figma',
                    img: fm,
                },
            ])
</script>


<template>
    <hr class="my-6 h-px border-t-0 bg-transparent bg-gradient-to-r from-transparent via-neutral-500 to-transparent opacity-25 dark:via-neutral-400" />
    <section class="relative p-8 md:p-14 text-white">
        <div class="flex items-center justify-center flex-col">
            <div class="max-w-lg pb-2">
                <h1 class="text-3xl md:text-4xl font-bold text-center text-white">Showcasing Skillsets</h1>
            </div>
            <div class="flex flex-col justify-center items-center">
                <div class="grid grid-cols-1 gap-16 md:gap-10">
                    <div class="flex flex-col items-center justify-center">
                        <ul class="grid grid-cols-4 md:grid-cols-7 mt-6 justify-center gap-2">
                            <li v-for="prog in progs" :key="prog.title" class="flex flex-col items-center mt-5">
                                <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white dark:text-gray-400">
                                    <div class="flex flex-col items-center">
                                        <img class="w-8 h-8" :src="prog.img" alt="">
                                        <p class="mt-8 text-center">{{prog.title}}</p>
                                    </div>
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>