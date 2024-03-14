<script setup lang="ts">
import AppNavbar from './components/AppNavbar.vue'

const images: string[] = [
    "https://images.unsplash.com/photo-1459411552884-841db9b3cc2a?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxleHBsb3JlLWZlZWR8NHx8fGVufDB8fHx8fA%3D%3D",
    "https://images.unsplash.com/photo-1599987662084-97832741bfa2?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxleHBsb3JlLWZlZWR8N3x8fGVufDB8fHx8fA%3D%3D",
    "https://images.unsplash.com/photo-1557180295-76eee20ae8aa?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxleHBsb3JlLWZlZWR8MXx8fGVufDB8fHx8fA%3D%3D",
    "https://images.unsplash.com/photo-1528825871115-3581a5387919?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxleHBsb3JlLWZlZWR8MTJ8fHxlbnwwfHx8fHw%3D",
];
</script>

<template>
    <header>
        <AppNavbar />
    </header>
    <main class="grid--container">
        <section class="grid--item">
            <h1>Software Developer</h1>
            <p>
                Hi, I'm Raman Verma, With a history of impactful contributions with multiple startups, and
                transforming their visions into tangible products. I've been consistently delivering
                exceptional user experiences and driving projects towards success. My expertise extends
                beyond Flutter, encompassing various technologies, allowing me to adapt to diverse project
                requirements and deliver impactful solutions.
            </p>
        </section>
        <section class="grid--item">
            <div class="grid--alt-container">
                <!-- An overlay needs to be opened on hovering this image, The overlay will be animated with color as background and text and description of the work as well -->
                <!-- Basically it'll represent condences information of the work/project like Title, Short Description, Image, Tech Stack used with quick links to the source/deployment-->
                <img class="grid--alt-container--item" :src="url" :alt="index.toString()" v-for="(url, index) in images"
                    :key="url">
            </div>
            <!-- Add a single or at max two most recent blogs to fill the empty space -->
            <!-- Layout needs to be super clean with text only and it should be obvious on first glance that it's a write up -->
        </section>
    </main>
</template>

<style scoped>
main {
    margin: 2rem 0;
}

img {
    height: 100%;
    width: 100%;

    object-fit: cover;

    filter: grayscale();
    cursor: pointer;

    border-radius: 1rem;
    transition: filter 1s;
}

img:hover {
    filter: none;
}

h1 {
    font-size: 3rem;
    padding: 1rem 0;
}

p {
    font-size: 1.2rem;
    padding: 1rem 0;
}

.grid--container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 4rem;
}

.grid--item {
    display: flex;
    flex-direction: column;

    padding: 1rem;
}

.grid--alt-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
}

.grid--alt-container--item {
    max-height: 150px;
}
</style>
