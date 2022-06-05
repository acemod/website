<script setup lang="ts">
import type Image from "../../interfaces/Image"
import type Link from "../../interfaces/Link"

interface Props {
    image: Image
    link: Link
    overlayColor?: string
    opacity?: number
}

const props = withDefaults(defineProps<Props>(), { overlayColor: "transparent", opacity: 0.2 })
</script>

<template>
    <a :href="link.href" class="image-box relative h-full flex justify-center items-center overflow-hidden">
        <div class="image-box-bg absolute left-0 top-0 w-full h-full">
            <div class="absolute top-0 left-0 h-full w-full pointer-events-none z-20" :style="`background-color: ${overlayColor}; opacity: ${opacity}`" />
            <img
                class="object-cover w-full h-full transition-transform duration-500 z-10"
                :src="image.src" :alt="image.alt" :width="image.width" :height="image.height"
            >
        </div>
        <div class="relative py-32 md:py-24 z-30 text-4xl font-bold text-center text-white">
            <slot />
        </div>
    </a>
</template>

<style scoped>
.image-box:hover img {
    transform: scale(1.1);
}
</style>
