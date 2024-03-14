<script setup lang="ts">
import AppNavbar from './components/AppNavbar.vue'

const imageURL: string =
  'https://images.unsplash.com/photo-1687593883595-6b678fc5c413?q=80&w=1587&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
</script>

<template>
  <header>
    <AppNavbar />
  </header>
  <main class="grid--container">
    <section class="grid--item">
      <div class="hero">
        <h1>Raman Verma</h1>
        <p>Software Developer</p>
      </div>
      <p>
        Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint
        ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat excepteur
        officia. Reprehenderit nostrud nostrud ipsum Lorem est aliquip amet voluptate voluptate
        dolor minim nulla est proident.
      </p>
    </section>
    <section class="grid--item"></section>
    <section class="grid--item">
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