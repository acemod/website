<script setup>
useHead({
    title: "ACE Mod",
    htmlAttrs: {
        lang: "en",
    },
    link: [
        {
            rel: "icon", type: "image/png", href: "/3.png",
        },
    ],
})
</script>

<template>
    <NuxtLayout>
        <NuxtPage />
    </NuxtLayout>
</template>

<style>
:root {
    --ace-dark-base-color-values: 34,34,34;
    --ace-dark-base-color: rgb(var(--ace-dark-base-color-values));
    --ace-dark-bg-color: var(--ace-dark-base-color);
    --ace-text-color: var(--ace-dark-base-color);
}

html,
body,
#__nuxt {
    height: 100vh;
    margin: 0;
    padding: 0;
}

html {
    color: var(--ace-text-color);
}

html.dark {
    background: var(--ace-dark-bg-color);
    color: white;
}

main h1,
main h2,
main h3,
main h4,
main p {
    margin-bottom: 0.5em;
    hyphens: auto;
}
</style>
