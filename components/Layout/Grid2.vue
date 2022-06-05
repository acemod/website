<script setup lang="ts">
interface Props {
    gaps?: boolean
}

withDefaults(defineProps<Props>(), { gaps: true })
</script>

<template>
    <div
        class="grid mb-8 md:grid-cols-2 lg:md:mb-16"
        :class="{ 'gap-4 lg:gap-8': gaps }"
    >
        <div class="h-full">
            <slot name="col1" />
        </div>
        <div class="h-full">
            <slot name="col2" />
        </div>
    </div>
</template>
