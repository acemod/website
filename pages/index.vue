<template>
    <Hero>
        <template #title>
            ACE Mod
        </template>
        <template #tagline>
            Modular realism modifications for the Arma series by Bohemia Interactive
        </template>
    </Hero>
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
                    New or enhanced features shouldn't come at the price of performance. Years of experience and our own development guidelines reduce any performance impact significantly.
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
</template>
