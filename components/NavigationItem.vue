<script setup lang="ts">
import type Link from "../interfaces/Link"

interface Props {
    link: Link
}

defineProps<Props>()
</script>

<template>
    <a :href="link.href" :target="link.target">
        {{ link.text }}
    </a>
</template>
