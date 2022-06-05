<script setup lang="ts">
import type Image from "../interfaces/Image"

definePageMeta({
    layout: "home",
})

const heroImage: Image = {
    src: "/reforger.webp",
    alt: "reforger",
    width: 1920,
    height: 1080,
}
</script>

<template>
    <Hero :image="heroImage">
        <template #title>
            ACE Mod
        </template>
        <template #tagline>
            Modular realism modifications for the Arma series by Bohemia Interactive
        </template>
    </Hero>
    <LayoutContainer>
        <LayoutGrid2 :gaps="false">
            <template #col1>
                <LayoutImageBox :image="{ src: '/backdrop_ace3.webp', alt: 'ACE3', width: 736, height: 414 }" :link="{ href: 'https://ace3.acemod.org/' }">
                    ACE3
                </LayoutImageBox>
            </template>
            <template #col2>
                <LayoutImageBox :image="{ src: '/backdrop_anvil.webp', alt: 'Anvil', width: 736, height: 414 }" :link="{ href: '', disabled: true }">
                    Anvil<br>
                    <small class="font-normal italic">coming soon</small>
                </LayoutImageBox>
            </template>
        </LayoutGrid2>
        <LayoutGrid4>
            <template #col1>
                <LayoutBox class="h-full">
                    <h1 class="font-bold">
                        Increased realism
                    </h1>
                    <p>
                        Our mods aim to enhance most of the aspects in the Arma series and align the gameplay closer to reality.
                    </p>
                </LayoutBox>
            </template>
            <template #col2>
                <LayoutBox class="h-full">
                    <h1 class="font-bold">
                        Additional features
                    </h1>
                    <p>ACE adds new features that are missing in the base game. This can range from new devices, vehicles and even consumables.</p>
                </LayoutBox>
            </template>
            <template #col3>
                <LayoutBox class="h-full">
                    <h1 class="font-bold">
                        Performance optimized
                    </h1>
                    <p>
                        New or enhanced features shouldn't come at the price of performance. Years of experience and our own development guidelines significantly reduce most performance impacts.
                    </p>
                </LayoutBox>
            </template>
            <template #col4>
                <LayoutBox class="h-full">
                    <h1 class="font-bold">
                        Open Source Development
                    </h1>
                    <p>
                        Our mods are entirely open-source, and everyone is free to propose changes and actively join development.
                    </p>
                </LayoutBox>
            </template>
        </LayoutGrid4>
        <SpecialJoinDiscord />
    </LayoutContainer>
</template>
