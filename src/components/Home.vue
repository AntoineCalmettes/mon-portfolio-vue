<template>
  <section class="about">
    <div class="about-header">
      <img
        src="https://media.licdn.com/dms/image/v2/D4E03AQFN5V5qFgdRZA/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1669499484577?e=1752710400&v=beta&t=Ra9vF4DnU_XkA1WbROfwk4PRC013ym9kPdywgIsGsCg"
        alt="Photo de profil" class="profile-pic" />
      <div>
        <h1>Antoine Calmettes</h1>
        <h2>À propos de moi</h2>
        <p class="subtitle">
          Développeur Full Stack
        </p>
      </div>
    </div>
    <div class="about-main">
      <p>
        <span class="icon">💼</span>
        <strong>Depuis 2019</strong>, je travaille en tant que développeur Full Stack dans plusieurs entreprises
        et secteurs variés.
        Je me suis spécialisé dans le framework <strong>Symfony 4+</strong> et <strong>JavaScript</strong>
        (React.js, Angular, Vue.js).
      </p>
      <div class="tech-logos">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSA7Ix_IDCQl5usWfXoH648kdugwxrDfaziUg&s" alt="PHP" title="PHP" />
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5d/Symfony_logo.svg/2560px-Symfony_logo.svg.png" alt="Symfony" title="Symfony" />
        <img src="https://img.icons8.com/ios-filled/50/000000/mysql-logo.png" alt="MySQL" title="MySQL" />
        <img src="https://upload.wikimedia.org/wikipedia/commons/5/50/Oracle_logo.svg" alt="Oracle" title="Oracle" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg"
          alt="TypeScript" title="TypeScript" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"
          alt="JavaScript" title="JavaScript" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React.js"
          title="React.js" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/angularjs/angularjs-original.svg" alt="Angular"
          title="Angular" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg" alt="Vue.js"
          title="Vue.js" />
        <img src="https://zonetuto.fr/wp-content/uploads/2023/01/framework-php-laravel-logo-2048x594.png" alt="Laravel"
          title="Laravel" />
      </div>

      <div class="skills-section">
        <h3><span class="icon">🛠️</span> Compétences techniques</h3>
        <ul class="skills-list">
          <li><span class="dot"></span> Test unitaire & fonctionnel</li>

          <li><span class="dot"></span> Développement d'API REST en Symfony 4+ avec Doctrine & PHP 7+</li>
          <li><span class="dot"></span> Micro-services en Node.js & MongoDB</li>
          <li><span class="dot"></span> Architecture et gestion de bases de données MySQL</li>
          <li><span class="dot"></span> Intégration d'interfaces en Angular, React.js , Vue.js</li>
          <li><span class="dot"></span> Programmation Orientée Objet & Modélisation UML</li>
          <li><span class="dot"></span> Déploiement CI/CD avec Docker</li>
          <li><span class="dot"></span> Intégration de WebServices & APIs externes</li>
          <li><span class="dot"></span> Relation client & gestion des retours</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  max-width: 900px;
  margin: 2rem auto;
  padding: 2rem 2.5rem;
  background: white;
  border-radius: 18px;
  box-shadow: 0 8px 32px rgba(60, 60, 60, 0.10);
  font-family: 'Segoe UI', 'Roboto', Arial, sans-serif;
  color: #232b2b;
}

.about-header {
  display: flex;
  align-items: center;
  gap: 2rem;
  margin-bottom: 1.5rem;
}

.profile-pic {
  border-radius: 50%;
  width: 200px;
  height: 200px;
  object-fit: cover;
  border: 5px solid #42b983;
  box-shadow: 0 2px 12px rgba(66, 185, 131, 0.18);
}

.subtitle {
  color: #2d7a59;
  font-size: 1.15rem;
  margin-top: 0.7rem;
  font-weight: 500;
}

.about-main {
  margin-top: 1rem;
}

.icon {
  font-size: 1.2rem;
  margin-right: 0.5rem;
}

.skills-section,
.softskills-section {
  margin-top: 1.5rem;
}

.skills-list {
  list-style: none;
  padding: 0;
  margin: 0.5rem 0 0 0;
}

.skills-list li {
  display: flex;
  align-items: center;
  margin-bottom: 0.5rem;
  font-size: 1.06rem;
}

.dot {
  display: inline-block;
  vertical-align: middle;
}

/* Version mobile : point un peu plus gros pour la visibilité */
@media (max-width: 600px) {
  .dot {
    width: 12px;
    height: 12px;
    margin-right: 1rem;
  }
}


@media (max-width: 700px) {
  .about {
    padding: 1rem;
  }

  .about-header {
    flex-direction: column;
    gap: 1rem;
    text-align: center;
  }

  .profile-pic {
    width: 140px;
    height: 140px;
  }
}

.tech-logos {
  display: flex;
  flex-wrap: wrap;
  gap: 18px;
  margin: 1.2rem 0 0.5rem 0;
  align-items: center;
  justify-content: flex-start;
}

.tech-logos img {
  height: 44px;
  width: auto;
  background: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(60, 60, 60, 0.08);
  padding: 6px;
  transition: transform 0.2s;
}

.tech-logos img:hover {
  transform: scale(1.1) rotate(-2deg);
  box-shadow: 0 6px 18px rgba(66, 185, 131, 0.18);
}

@media (max-width: 700px) {
  .tech-logos {
    justify-content: center;
    gap: 10px;
  }

  .tech-logos img {
    height: 32px;
    padding: 3px;
  }
}
</style>
