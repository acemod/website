<script setup lang="ts">
import type Link from "../../interfaces/Link"

const links: Link[] = [
    {
        href: "https://ace3.acemod.org",
        text: "ACE3",
        target: "_blank",
    },
    {
        href: "#",
        text: "Anvil",
        disabled: true,
    },
    {
        href: "https://github.com/acemod",
        text: "GitHub",
        target: "_blank",
    },
]

const mobileMenuOpen = ref(false)
const toggleMobileMenu = () => {
    mobileMenuOpen.value = !mobileMenuOpen.value
}
const closeMenu = () => {
    mobileMenuOpen.value = false
}

watch(() => mobileMenuOpen.value, () => {
    const htmlElement = document.querySelector("html")
    if (mobileMenuOpen.value) {
        htmlElement!.classList.add("overflow-y-hidden")
    }
    else {
        htmlElement!.classList.remove("overflow-y-hidden")
    }
})
</script>

<template>
    <div class="container mx-auto px-4 md:px-8">
        <div class="flex justify-between items-center h-16">
            <NuxtLink to="/" class="flex items-center z-50">
                <HeaderNavigationLogo />
            </NuxtLink>

            <nav
                class="mobile-nav items-center absolute hidden w-100vw h-100vh bg-white dark:bg-black dark:bg-opacity-90 flex-col justify-center top-0 left-0
                md:relative md:flex md:flex-row md:w-auto md:h-auto md:bg-transparent md:dark:bg-transparent"
                :class="{ '!flex': mobileMenuOpen, 'active': mobileMenuOpen }"
            >
                <template v-for="link in links" :key="link.href">
                    <HeaderNavigationItem :link="link" />
                </template>
            </nav>
            <button
                class="mobile-nav-button block md:hidden w-8 h-8 z-50" aria-label="mobile navigation"
                :aria-expanded="mobileMenuOpen" aria-controls="mobile-nav" @click="toggleMobileMenu"
            >
                <div class="container  flex flex-col justify-between items-end w-6 h-6">
                    <span class="top h-0.75 bg-gray-800 dark:bg-white transition-all duration-300" />
                    <span class="middle h-0.75 bg-gray-800 dark:bg-white transition-all duration-300" />
                    <span class="bottom h-0.75 bg-gray-800 dark:bg-white transition-all duration-300" />
                </div>
            </button>
        </div>
    </div>
</template>

<style scoped>
.mobile-nav-button .top {
    width: 0.75rem;
}

.mobile-nav-button .middle {
    width: 1.5rem;
}

.mobile-nav-button .bottom {
    width: 1.25rem;
}

.mobile-nav-button:hover .top {
    width: 1.25rem;
}

.mobile-nav-button:hover .middle {
    width: 1.75rem;
}

.mobile-nav-button:hover .bottom {
    width: 1rem;
}
</style>
