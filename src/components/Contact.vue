<template>
  <section class="contact">
    <h2>Contact</h2>
    <div class="contact-details">
      <div class="info">
        <p><span class="icon">📧</span>
          <a href="mailto:antoine.calmettes.pro@gmail.com">antoine.calmettes.pro@gmail.com</a>
        </p>
        <p><span class="icon">📱</span>
          <a href="tel:+33617180998">+33 6 17 18 09 98</a>
        </p>
      </div>
      <div class="socials">
        <a href="https://www.linkedin.com/in/antoine-calmettes/" target="_blank" rel="noopener" title="LinkedIn">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" alt="LinkedIn" />
        </a>
        <a href="https://github.com/AntoineCalmettes" target="_blank" rel="noopener" title="GitHub">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub" />
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
const name = ref('')
const email = ref('')
const message = ref('')
const sent = ref(false)

function send() {
  // Ici tu pourrais envoyer le message à une API ou un email
  sent.value = true
  setTimeout(() => sent.value = false, 3000)
  name.value = email.value = message.value = ''
}
</script>

<style scoped>
.contact {
  max-width: 650px;
  margin: 2rem auto;
  padding: 2.5rem 2rem;
  border-radius: 16px;
  box-shadow: 0 8px 32px rgba(60,60,60,0.08);
  font-family: 'Segoe UI', 'Roboto', Arial, sans-serif;
  color: #232b2b;
}
.contact-details {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1.5rem;
  margin-bottom: 2rem;
  flex-wrap: wrap;
}
.info {
  font-size: 1.08rem;
}
.info p {
  margin: 0.3rem 0;
  display: flex;
  align-items: center;
}
.icon {
  font-size: 1.3rem;
  margin-right: 0.7rem;
  color: #42b983;
}
.socials {
  display: flex;
  gap: 18px;
}
.socials img {
  width: 38px;
  height: 38px;
  transition: transform 0.18s, box-shadow 0.18s;
  border-radius: 8px;
  background: #fff;
  box-shadow: 0 2px 8px rgba(60,60,60,0.07);
  padding: 3px;
}
.socials img:hover {
  transform: scale(1.13) rotate(-3deg);
  box-shadow: 0 6px 18px rgba(66,185,131,0.18);
}
.contact-form {
  margin-top: 2rem;
}
form {
  display: flex;
  flex-direction: column;
  gap: 0.7rem;
  max-width: 420px;
  margin: auto;
}
input, textarea {
  padding: 0.7rem;
  border-radius: 6px;
  border: 1px solid #b3e5d6;
  font-size: 1rem;
  background: #fff;
  color: #232b2b;
  box-shadow: 0 1px 3px rgba(66,185,131,0.06);
}
button {
  background: #42b983;
  color: #fff;
  border: none;
  padding: 0.7rem;
  border-radius: 6px;
  font-size: 1.07rem;
  cursor: pointer;
  font-weight: 500;
  transition: background 0.17s;
}
button:hover {
  background: #338e6b;
}
.sent {
  color: #338e6b;
  margin-top: 0.5rem;
  text-align: center;
  font-weight: 500;
}
@media (max-width: 600px) {
  .contact {
    padding: 1rem 0.5rem;
  }
  .contact-details {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.8rem;
  }
  .socials {
    gap: 12px;
  }
}
</style>
