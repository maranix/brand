<script setup lang="ts">
import NavbarItem from './NavbarItem.vue'
</script>

<template>
  <nav>
    <NavbarItem href="/" text="Maranix" text-align="start"/>
    <div class="nav--links">
      <NavbarItem href="works" text="Works" />
      <NavbarItem href="blogs" text="Blogs" />
      <NavbarItem href="about" text="About" />
      <NavbarItem href="contact" text="Contact" />
    </div>
  </nav>
</template>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav--links {
  width: 50%;

  display: flex;
  justify-content: end;
}
</style>
