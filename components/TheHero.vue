<script setup>
const props = defineProps(['bulmaColor'])

</script>

<template>
    <section class="hero is-medium is-bold" :class="props.bulmaColor ?? 'is-info'">
        <div class="hero-body">
            <div class="container has-text-centered">
                <h1 class="title is-size-1">
                    <slot />
                </h1>
                <slot name="subtitle" />
            </div>
        </div>
    </section>
</template>

<style>
.hero-body {
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    height: 400px;
}
</style>
