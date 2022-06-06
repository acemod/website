<template>
    <header class="relative top-0 left-0 z-50 w-full md:fixed">
        <HeaderNavigation />
    </header>
</template>

<style scoped>
header {
    background-color: rgba(255, 255, 255, 0.9);
}

.dark header {
    background-color: rgba(var(--ace-dark-base-color-values), 0.9);
}

/* if backdrop support: very transparent and blurred */
@supports ((-webkit-backdrop-filter: none) or (backdrop-filter: none)) {
    header {
        background-color: rgba(255, 255, 255, 0.45);
        -webkit-backdrop-filter: saturate(50%) blur(0.5rem);
        backdrop-filter: saturate(50%) blur(0.5rem);
    }

    .dark header {
        background-color: rgba(var(--ace-dark-base-color-values), 0.1);
    }
}
</style>
