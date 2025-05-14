<template>
  <Navbar @navigate="currentPage = $event" />
  <main>
    <Home v-if="currentPage === 'home'" />
    <Projects v-else-if="currentPage === 'projects'" />
    <Contact v-else-if="currentPage === 'contact'" />
  </main>
</template>

<script setup>
import { ref } from 'vue'
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'

const currentPage = ref('home')
</script>

<style>
body {
  font-family: 'Segoe UI', sans-serif;
  background: #f9f9f9;
  margin: 0;
  min-height: 100vh;
}

/* Centrage et style du contenu principal */
main {
  padding: 2rem;
  max-width: 600px;
  margin: 2rem auto 0 auto;
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 2px 16px #0001;
}

/* Responsive pour mobile */
@media (max-width: 600px) {
  main {
    padding: 1rem;
    margin: 1rem auto 0 auto;
    min-height: 80vh;
  }
  body {
    font-size: 1.05rem;
  }
}
</style>
