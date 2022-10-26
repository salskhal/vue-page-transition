<script setup>
import Navbar from "./components/Navbar.vue";
</script>

<template>
  <div class="container">
    <Navbar />
    <div>
      <RouterView />
    </div>
  </div>
</template>

<style scoped>
.container {
  position: relative;
  height: 100vh;
  overflow: hidden;
  /* padding-inline: 3rem; */
  padding: 6rem 3rem;
}

@media screen and (min-width: 1024px) {
  .container {
    padding-inline: 6rem;
  }
}

/* header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
} */
</style>
