<script setup lang="ts">
import type Link from "../interfaces/Link"

const links: Link[] = [
    {
        href: "https://ace3.acemod.org",
        text: "ACE3",
        target: "_blank",
    },
    {
        href: "https://anvil.acemod.org",
        text: "Anvil",
        target: "_blank",
    },
    {
        href: "https://github.com/acemod",
        text: "GitHub",
        target: "_blank",
    },
]
</script>

<template>
    <div class="px-8">
        <div class=" flex  justify-between">
            <NuxtLink to="/" class="flex items-center ">
                <img
                    class="mr-2"
                    src="ace3-logo-white-tiny.webp" alt="ACE logo"
                    height="23" width="100"
                >
            </NuxtLink>
            <div>
                <nav class="flex font-bold">
                    <template v-for="link in links" :key="link.href">
                        <NavigationItem :link="link" />
                    </template>
                </nav>
            </div>
        </div>
    </div>
</template>
