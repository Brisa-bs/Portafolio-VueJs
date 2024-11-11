<script setup>
import { ref } from 'vue';

const experiencia = ref([
  {
    year: 2020,
    title: 'Desarrolladora Junior Freelance',
    description: 'Comencé a trabajar como desarrolladora junior independiente...',
  },
  {
    year: 2021,
    title: 'Prácticas Profesionales en Desarrollo Web',
    description: 'Realicé prácticas profesionales en una agencia de desarrollo web...',
  },
  // Agregar más objetos aquí
]);
</script>

<template>
  <section class="experiencia">
    <h2>Mi Experiencia Profesional</h2>
    <ul class="timeline-list">
      <li v-for="(job, index) in experiencia" :key="index" class="timeline-item">
        <div class="timeline-year">{{ job.year }}</div>
        <div class="timeline-content">
          <h3 class="timeline-title">{{ job.title }}</h3>
          <p class="timeline-description">{{ job.description }}</p>
        </div>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.experiencia {
  margin: 20px auto;
  padding: 20px;
  max-width: 800px;
  font-family: Arial, sans-serif;
}

.experiencia h2 {
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
