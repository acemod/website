<template>
    <div class="relative w-100px h-23px">
        <img class="logo-white mr-2 absolute top-0 left-0 transition-opacity" src="/ace3-logo-white-tiny.webp" alt="ACE logo" height="23" width="100">
        <img class="logo-black mr-2 absolute top-0 left-0 transition-opacity" src="/ace3-logo-black-tiny.webp" alt="ACE logo" height="23" width="100">
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
