<script setup lang="ts">
const props = defineProps({
    href: String,
    text: String
})
</script>

<template>
    <a :href="props.href">{{ props.text }}</a>
</template>

<style scoped>
a {
    min-width: 100px;
    margin: 0 1.5rem;

    font: 500 1.5rem var(--heading-font-family);
    text-align: center;

    transition: font-weight 0.1s;
}

a:hover {
    font-weight: 900;
}
</style>
