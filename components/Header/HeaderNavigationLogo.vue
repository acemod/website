<template>
    <div class="relative w-100px h-23px">
        <picture class="logo-white mr-2 absolute top-0 left-0 transition-opacity w-full h-full">
            <source srcset="/ace3-logo-white-tiny@2x.webp 2x">
            <img src="/ace3-logo-white-tiny.webp" alt="ACE logo" width="100" height="23">
        </picture>

        <picture class="logo-black mr-2 absolute top-0 left-0 transition-opacity w-full h-full">
            <source srcset="/ace3-logo-black-tiny@2x.webp 2x">
            <img src="/ace3-logo-black-tiny.webp" alt="ACE logo" width="100" height="23">
        </picture>
    </div>
</template>

<style scoped>
.dark .logo-black {
    opacity: 0;
}

.logo-white {
    opacity: 1;
}

html:not(.dark) .logo-black {
    opacity: 1;
}

html:not(.dark) .logo-white {
    opacity: 0;
}
</style>
