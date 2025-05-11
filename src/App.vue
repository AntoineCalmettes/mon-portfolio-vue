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
body { font-family: 'Segoe UI', sans-serif; background: #f9f9f9; margin: 0; }
main { padding: 2rem; }
</style>
