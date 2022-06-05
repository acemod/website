<script setup lang="ts">
import type Image from "../../interfaces/Image"
import type Link from "../../interfaces/Link"

interface Props {
    image: Image
    link: Link
}

defineProps<Props>()
</script>

<template>
    <a :href="link.href" class="image-box relative h-full flex justify-center items-center overflow-hidden">
        <img
            class="absolute object-cover left-0 top-0 w-full h-full z-0 transition-transform"
            :src="image.src" :alt="image.alt" :width="image.width" :height="image.height"
        >
        <div class="relative py-16 md:py-8 z-10 text-4xl font-bold text-center text-white">
            <slot />
        </div>
    </a>
</template>

<style scoped>
.image-box:hover img {
    transform: scale(1.1);
}
</style>
