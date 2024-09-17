<script setup>
    import Button from '@/components/Button.vue'
</script>

<template>
    <div class="relative top-0 left-0 w-full bg-gray-950 opacity-[.8]">
        <div class="mx-auto mt-3 max-w-7xl px-6 md:px-20 ">
            <div class="relative flex h-16 justify-between">
                <div class="flex flex-1 items-stretch justify-start">
                    <a class="flex flex-shrink-0 items-center" href="#">
                        <img class="block h-20 w-auto" src="@/assets/logo.svg">
                    </a>
                </div>
                <div class="flex-shrink-0 flex px-2 py-3 items-center space-x-8 ">
                    <Button class="">CV</Button>
                </div>
            </div>
        </div>
    </div>
</template>