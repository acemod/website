<script setup>
useHead({
    title: "ACE Mod",
    htmlAttrs: {
        lang: "en",
    },
    link: [
        {
            rel: "icon", type: "image/png", href: "/nuxt.png",
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
html,
body,
#__nuxt {
    height: 100vh;
    margin: 0;
    padding: 0;
}

html {
    color: #222;
}

html.dark {
    background: #222;
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
