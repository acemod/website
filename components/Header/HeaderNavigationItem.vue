<script setup lang="ts">
import type Link from "../../interfaces/Link"

interface Props {
    link: Link
}

defineProps<Props>()
</script>

<template>
    <div class="block h-16 md:mx-4 first-of-type:ml-0 last-of-type:mr-0 flex font-bold items-center">
        <a
            class="font-bold transition-colors hover:text-brand-primary text-2xl md:text-base"
            :href="link.href" :target="link.target"
            :disabled="link.disabled"
        >
            {{ link.text }}
        </a>
    </div>
</template>
