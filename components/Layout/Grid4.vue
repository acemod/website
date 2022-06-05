<template>
    <div class="grid gap-4 mb-8 md:grid-cols-2 lg:grid-cols-4 lg:gap-8 lg:md:mb-16">
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
