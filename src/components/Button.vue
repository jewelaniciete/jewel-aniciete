
<script setup>
    import { ref } from 'vue';
    const pdfUrl = ref('/public/jewel-aniciete-resume.pdf');
</script>   

<template>
    <a
        class="text-white font-semibold border text-xl p-2 rounded-lg shadow-sm shadow-white"
        :href="pdfUrl" target="_blank"  rel="noopener noreferrer">
        <slot />
    </a>
</template>