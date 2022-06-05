<script setup lang="ts">
import type Image from "../interfaces/Image"

interface Props {
    image: Image
}

defineProps<Props>()
</script>

<template>
    <section class="relative mb-16">
        <!-- <img
            class="absolute object-cover left-0 top-0 w-full h-full z-0"
            :src="image.src" :alt="image.alt" :width="image.width" :height="image.height"
        > -->
        <LayoutContainer>
            <div class="relative mx-auto z-10 pt-16 pb-8 md:w-2/3">
                <h1 class="text-6xl font-bold mb-4">
                    <slot name="title" />
                </h1>
                <p class="text-3xl">
                    <slot name="tagline" />
                </p>
            </div>
        </LayoutContainer>
    </section>
</template>
