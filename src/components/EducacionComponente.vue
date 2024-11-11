<script setup>
import { ref } from 'vue';

// Definir los eventos de la línea de tiempo (educación)
const timeline = ref([
  {
    year: 2020,
    title: 'Inicio de la Tecnica Universitaria en Programación',
    description: 'Comencé mis estudios en la carrera de Tecnica Universitaria en Programación en la Universidad Tecnológica Nacional (UTN). Durante este año me centré en aprender los fundamentos de la programación y las primeras tecnologías como JavaScript y HTML.',
  },
  {
    year: 2021,
    title: 'Primeros Proyectos',
    description: 'Empecé a realizar mis primeros proyectos prácticos, aplicando lo aprendido en la carrera. Trabajé con JavaScript, creando pequeñas aplicaciones web como un gestor de tareas y una página de portfolio personal.',
  },
  {
    year: 2022,
    title: 'Cursos de Backend y Frameworks',
    description: 'Realicé varios cursos complementarios sobre desarrollo backend y frameworks modernos como Vue.js y Node.js. Esto me permitió adquirir habilidades más avanzadas en programación y mejorar mis aplicaciones web.',
  },
  {
    year: 2023,
    title: 'Práctica Profesional y Trabajo Independiente',
    description: 'Durante este año, comencé a trabajar de manera independiente en varios proyectos freelance. Además, realicé prácticas profesionales en una empresa de desarrollo web, donde pude aplicar mis conocimientos en un entorno real.',
  },
  {
    year: 2024,
    title: 'Especialización y Proyectos Avanzados',
    description: 'Estoy completando mi formación con un enfoque en tecnologías avanzadas como el desarrollo de aplicaciones móviles con Vue, APIs RESTful y bases de datos. Mi objetivo es seguir mejorando mis habilidades y prepararme para un futuro profesional en desarrollo full-stack.',
  },
]);
</script>

<template>
  <section class="timeline">
    <h2>Mi Línea de Tiempo Educativa</h2>
    <ul class="timeline-list">
      <li v-for="(event, index) in timeline" :key="index" class="timeline-item">
        <div class="timeline-year">{{ event.year }}</div>
        <div class="timeline-content">
          <h3 class="timeline-title">{{ event.title }}</h3>
          <p class="timeline-description">{{ event.description }}</p>
        </div>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.timeline {
  margin: 20px auto;
  padding: 20px;
  max-width: 800px;
  font-family: Arial, sans-serif;
}

.timeline h2 {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 30px;
  color: #333;
}

.timeline-list {
  list-style-type: none;
  padding: 0;
  position: relative;
}

.timeline-item {
  display: flex;
  flex-direction: row;
  margin-bottom: 20px;
  padding-left: 50px;
  position: relative;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 2px;
  background-color: #5e81ac;
}

.timeline-year {
  font-size: 1.5rem;
  font-weight: bold;
  color: #5e81ac;
  margin-right: 15px;
  width: 80px;
}

.timeline-content {
  background-color: #f4f4f4;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  width: calc(100% - 80px);
}

.timeline-title {
  font-size: 1.2rem;
  font-weight: bold;
  color: #333;
  margin-bottom: 8px;
}

.timeline-description {
  font-size: 1rem;
  color: #555;
}
</style>
