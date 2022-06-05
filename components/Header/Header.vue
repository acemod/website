<template>
    <header class="relative top-0 left-0 z-50 w-full md:fixed">
        <HeaderNavigation />
    </header>
</template>

<style scoped>
header {
    -webkit-backdrop-filter: saturate(50%) blur(0.5rem);
    backdrop-filter: saturate(50%) blur(0.5rem);
    background-color: rgba(255,255,255,0.35);
}

.dark header {
    background-color: transparent;
}
</style>
