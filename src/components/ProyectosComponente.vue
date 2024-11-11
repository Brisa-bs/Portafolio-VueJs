<script setup>
import { ref } from 'vue';

// Lista de proyectos
const proyectos = ref([
  {
    id: 1,
    nombre: 'Portfolio Web',
    descripcion: 'Un sitio web personal para mostrar mis proyectos y habilidades en programación.',
    tecnologias: ['Vue.js', 'Vite', 'CSS', 'HTML'],
    enlace: 'https://www.tu-portfolio.com',
  },
  {
    id: 2,
    nombre: 'Aplicación de Tareas',
    descripcion: 'Una aplicación para gestionar tareas diarias con capacidad de agregar, editar y eliminar tareas.',
    tecnologias: ['Vue.js', 'Vuex', 'Firebase'],
    enlace: 'https://www.tu-aplicacion-tareas.com',
  },
  {
    id: 3,
    nombre: 'E-commerce con Vue',
    descripcion: 'Una tienda en línea simple creada con Vue.js y Firebase para la gestión de productos.',
    tecnologias: ['Vue.js', 'Firebase', 'Vue Router'],
    enlace: 'https://www.tu-ecommerce.com',
  },
  {
    id: 4,
    nombre: 'Blog Personal',
    descripcion: 'Un blog para compartir artículos técnicos, experiencias y tutoriales sobre desarrollo web.',
    tecnologias: ['Vue.js', 'Node.js', 'Express'],
    enlace: 'https://www.tu-blog.com',
  },
]);
</script>

<template>
  <section class="proyectos">
    <h2>Mis Proyectos</h2>
    <ul class="proyectos-lista">
      <li v-for="proyecto in proyectos" :key="proyecto.id" class="proyecto-item">
        <div class="proyecto-contenido">
          <h3 class="proyecto-nombre">{{ proyecto.nombre }}</h3>
          <p class="proyecto-descripcion">{{ proyecto.descripcion }}</p>
          <p class="proyecto-tecnologias">
            <strong>Tecnologías utilizadas:</strong>
            <span v-for="(tec, index) in proyecto.tecnologias" :key="index">{{ tec }}{{ index < proyecto.tecnologias.length - 1 ? ', ' : '' }}</span>
          </p>
          <a :href="proyecto.enlace" class="proyecto-enlace" target="_blank" rel="noopener noreferrer">Ver proyecto</a>
        </div>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.proyectos {
  margin: 40px auto;
  padding: 20px;
  max-width: 1000px;
  font-family: Arial, sans-serif;
}

.proyectos h2 {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 30px;
  color: #333;
}

.proyectos-lista {
  list-style-type: none;
  padding: 0;
}

.proyecto-item {
  background-color: #f9f9f9;
  margin-bottom: 20px;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.proyecto-contenido {
  display: flex;
  flex-direction: column;
}

.proyecto-nombre {
  font-size: 1.5rem;
  font-weight: bold;
  color: #5e81ac;
  margin-bottom: 10px;
}

.proyecto-descripcion {
  font-size: 1rem;
  color: #555;
  margin-bottom: 10px;
}

.proyecto-tecnologias {
  font-size: 1rem;
  color: #777;
}

.proyecto-enlace {
  margin-top: 10px;
  color: #5e81ac;
  font-weight: bold;
  text-decoration: none;
}

.proyecto-enlace:hover {
  text-decoration: underline;
}
</style>
