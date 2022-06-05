<script setup lang="ts">
interface Props {
    gaps?: boolean
}

withDefaults(defineProps<Props>(), { gaps: true })
</script>

<template>
    <div
        class="grid mb-16 md:grid-cols-2 lg:grid-cols-4"
        :class="{ 'gap-4 lg:gap-8': gaps }"
    >
        <div class="h-full">
            <slot name="col1" />
        </div>
        <div class="h-full">
            <slot name="col2" />
        </div>
        <div class="h-full">
            <slot name="col3" />
        </div>
        <div class="h-full">
            <slot name="col4" />
        </div>
    </div>
</template>
