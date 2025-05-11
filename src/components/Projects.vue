<template>
  <section class="projects">
    <h2>Mes Projets</h2>
    <h3>Page en cours de construction</h3>
    <div v-for="project in projects" :key="project.title" class="project-card">
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
      <p><strong>Technos :</strong> {{ project.technos }}</p>
      <a :href="project.link" target="_blank">Voir le projet</a>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: "Portfolio Vue.js",
    description: "Mon propre portfolio réalisé avec Vue.js et Vite.",
    technos: "Vue.js, Vite, CSS",
    link: "#"
  },
  {
    title: "Todo App",
    description: "Application de gestion de tâches.",
    technos: "Vue.js, LocalStorage",
    link: "#"
  }
]
</script>

<style scoped>
.projects {
  max-width: 800px;
  margin: 2rem auto;
  padding: 1.5rem;
  background: linear-gradient(135deg, #f4f8fb 0%, #e8f6ef 100%);
  border-radius: 16px;
  box-shadow: 0 8px 32px rgba(60,60,60,0.08);
  color: #232b2b; /* Texte foncé */
}

h2, h3 {
  color: #2d7a59;
  margin-bottom: 1rem;
}

.project-card {
  background: #fff;
  border: 1px solid #b3e5d6;
  border-radius: 10px;
  padding: 1.2rem;
  margin: 1.2rem 0;
  box-shadow: 0 2px 12px rgba(66,185,131,0.07);
  color: #232b2b;
}

.project-card h3 {
  margin-top: 0;
  color: #42b983;
}

a {
  color: #42b983;
  text-decoration: none;
  font-weight: 500;
}

a:hover {
  text-decoration: underline;
}

@media (max-width: 600px) {
  .projects {
    padding: 0.5rem;
  }
  .project-card {
    padding: 0.7rem;
  }
}
</style>
