<script setup lang="ts">
import AppNavbar from './components/AppNavbar.vue'
</script>

<template>
  <header>
    <AppNavbar />
  </header>
  <main class="grid--container">
    <section class="grid--item">
      <div class="hero">
        <h1>Software Developer</h1>
      </div>
      <p>
        Hi, I'm Raman Verma, with a background in collaborating with multiple startups, and
        transforming their visions into tangible products. I've been consistently delivering
        exceptional user experiences and driving projects towards success. My expertise extends
        beyond Flutter, encompassing various technologies, allowing me to adapt to diverse project
        requirements and deliver impactful solutions.
        <!-- This one seems more generic/obvious and might not need it at all -->
        <!-- Committed to continuous learning, I stay updated with industry trends to ensure the highest standards of innovation and quality. -->
      </p>
    </section>
    <!-- Not sure what to do with this space, Possibly better use as an empty space or maybe show blogs? -->
    <section class="grid--item"></section>
    <section class="grid--item">
      <!-- Project Specific Probably???? -->
      <p>
        Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint
        ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat excepteur
        officia. Reprehenderit nostrud nostrud ipsum Lorem est aliquip amet voluptate voluptate
        dolor minim nulla est proident.
      </p>
      <!-- <img :src=imageURL alt=""> -->
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

.hero {
  font-size: 2rem;
  font-family: var(--heading-font-family);
}

.hero > h1 {
  font-size: 3rem;
  margin: 1rem 0;
}

.hero > p {
  margin: 1rem 0;
}

section > p {
  padding: 1rem 0;
  margin-bottom: 2rem;
}

.grid--container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 4rem;
}

.grid--item {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
./components/AppNavbar.vue
