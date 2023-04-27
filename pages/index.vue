<script setup>
const { data } = await useAsyncData('hello', () => queryContent('/website-config').findOne())
console.log(data)
</script>

<template>
    <main>
        <TheHero :bulmaColor="data.hero.color">
            {{ data.hero.title }}</TheHero>
        <BlogPostList />
    </main>
</template>
