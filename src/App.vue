<script setup lang="ts">
import AppNavbar from './components/AppNavbar.vue'
</script>

<template>
  <header>
    <AppNavbar />
  </header>
  <main class="grid--container">
    <section class="grid--item hero">
      <h1>Software Developer</h1>
      <p>
        Hi, I'm Raman Verma, With a history of impactful contributions with multiple startups, and
        transforming their visions into tangible products. I've been consistently delivering
        exceptional user experiences and driving projects towards success. My expertise extends
        beyond Flutter, encompassing various technologies, allowing me to adapt to diverse project
        requirements and deliver impactful solutions.
      </p>
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
  grid-template-columns: repeat(4, 1fr);
  gap: 4rem;
}

.grid--item {
  display: flex;
  flex-direction: column;

  padding: 1rem;
}

.hero {
  grid-column: span 2;
}
</style>
