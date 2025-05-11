<template>
  <nav>
    <ul>
      <li><a href="#" @click.prevent="$emit('navigate', 'home')">Accueil</a></li>
      <li><a href="#" @click.prevent="$emit('navigate', 'projects')">Projets</a></li>
      <li><a href="#" @click.prevent="$emit('navigate', 'contact')">Contact</a></li>
    </ul>
  </nav>
</template>

<style scoped>
nav ul { display: flex; gap: 1rem; list-style: none; }
a { text-decoration: none; color: #42b983; }
a:hover { text-decoration: underline; }
</style>
