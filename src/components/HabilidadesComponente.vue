<script setup>
import { ref } from 'vue';

// Definir las habilidades
const habilidades = ref({
  lenguajesDeProgramacion: [
    { nombre: 'JavaScript', nivel: 'Avanzado', porcentaje: 90 },
    { nombre: 'Python', nivel: 'Intermedio', porcentaje: 60 },
    { nombre: 'HTML/CSS', nivel: 'Avanzado', porcentaje: 85 },
    { nombre: 'Java', nivel: 'Intermedio', porcentaje: 60 },
    { nombre: 'SQL', nivel: 'Intermedio', porcentaje: 65 }
  ],
  frameworksYLibrerias: [
    { nombre: 'React.js', nivel: 'Avanzado', porcentaje: 90 },
    { nombre: 'Vue.js', nivel: 'Intermedio', porcentaje: 65 },
    { nombre: 'Node.js', nivel: 'Avanzado', porcentaje: 85 },
    { nombre: 'Django', nivel: 'Intermedio', porcentaje: 70 },
    { nombre: 'Bootstrap', nivel: 'Avanzado', porcentaje: 80 }
  ],
  herramientasYSoftware: [
    { nombre: 'Git', nivel: 'Avanzado', porcentaje: 95 },
    { nombre: 'Docker', nivel: 'Intermedio', porcentaje: 60 },
    { nombre: 'Jenkins', nivel: 'Intermedio', porcentaje: 60 },
    { nombre: 'Figma', nivel: 'Intermedio', porcentaje: 65 },
    { nombre: 'Visual Studio Code', nivel: 'Avanzado', porcentaje: 90 }
  ],
  basesDeDatos: [
    { nombre: 'MongoDB', nivel: 'Avanzado', porcentaje: 85 },
    { nombre: 'MySQL', nivel: 'Intermedio', porcentaje: 70 },
    { nombre: 'PostgreSQL', nivel: 'Intermedio', porcentaje: 70 }
  ],
  idiomas: [
    { nombre: 'Español', nivel: 'Nativo', porcentaje: 100 },
    { nombre: 'Inglés', nivel: 'Intermedio', porcentaje: 60 }
  ]
});
</script>

<template>
  <section class="habilidades">
    <h2 class="titulo">Mis Habilidades</h2>

    <!-- Lenguajes de Programación -->
    <div class="categoria">
      <h3 class="categoria-titulo">Lenguajes de Programación</h3>
      <ul class="lista">
        <li v-for="(habilidad, index) in habilidades.lenguajesDeProgramacion" :key="index" class="habilidad-item">
          <div class="habilidad-info">
            <span class="habilidad-nombre">{{ habilidad.nombre }}</span>
            <span class="habilidad-nivel">{{ habilidad.nivel }}</span>
          </div>
          <div class="barra-progreso">
            <div class="progreso" :style="{ width: habilidad.porcentaje + '%' }"></div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Frameworks y Librerías -->
    <div class="categoria">
      <h3 class="categoria-titulo">Frameworks y Librerías</h3>
      <ul class="lista">
        <li v-for="(habilidad, index) in habilidades.frameworksYLibrerias" :key="index" class="habilidad-item">
          <div class="habilidad-info">
            <span class="habilidad-nombre">{{ habilidad.nombre }}</span>
            <span class="habilidad-nivel">{{ habilidad.nivel }}</span>
          </div>
          <div class="barra-progreso">
            <div class="progreso" :style="{ width: habilidad.porcentaje + '%' }"></div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Herramientas y Software -->
    <div class="categoria">
      <h3 class="categoria-titulo">Herramientas y Software</h3>
      <ul class="lista">
        <li v-for="(habilidad, index) in habilidades.herramientasYSoftware" :key="index" class="habilidad-item">
          <div class="habilidad-info">
            <span class="habilidad-nombre">{{ habilidad.nombre }}</span>
            <span class="habilidad-nivel">{{ habilidad.nivel }}</span>
          </div>
          <div class="barra-progreso">
            <div class="progreso" :style="{ width: habilidad.porcentaje + '%' }"></div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Bases de Datos -->
    <div class="categoria">
      <h3 class="categoria-titulo">Bases de Datos</h3>
      <ul class="lista">
        <li v-for="(habilidad, index) in habilidades.basesDeDatos" :key="index" class="habilidad-item">
          <div class="habilidad-info">
            <span class="habilidad-nombre">{{ habilidad.nombre }}</span>
            <span class="habilidad-nivel">{{ habilidad.nivel }}</span>
          </div>
          <div class="barra-progreso">
            <div class="progreso" :style="{ width: habilidad.porcentaje + '%' }"></div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Idiomas -->
    <div class="categoria">
      <h3 class="categoria-titulo">Idiomas</h3>
      <ul class="lista">
        <li v-for="(idioma, index) in habilidades.idiomas" :key="index" class="habilidad-item">
          <div class="habilidad-info">
            <span class="habilidad-nombre">{{ idioma.nombre }}</span>
            <span class="habilidad-nivel">{{ idioma.nivel }}</span>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.habilidades {
  margin: 40px auto;
  padding: 20px;
  max-width: 1200px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f4f7fa;
  border-radius: 12px;
}

.titulo {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 30px;
  color: #2f4f4f;
  font-weight: bold;
}

.categoria {
  margin-bottom: 40px;
}

.categoria-titulo {
  font-size: 1.8rem;
  font-weight: bold;
  color: #5e81ac;
  margin-bottom: 10px;
  text-transform: uppercase;
}

.lista {
  list-style-type: none;
  padding: 0;
}

.habilidad-item {
  background-color: #fff;
  padding: 15px;
  margin-bottom: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.habilidad-info {
  display: flex;
  flex-direction: column;
}

.habilidad-nombre {
  font-size: 1.1rem;
  color: #333;
  font-weight: bold;
}

.habilidad-nivel {
  font-size: 1rem;
  color: #777;
  font-style: italic;
}

.barra-progreso {
  width: 60%;
  height: 8px;
  background-color: #e0e0e0;
  border-radius: 5px;
  margin-left: 20px;
}

.progreso {
  height: 100%;
  background-color: #5e81ac;
  border-radius: 5px;
}
</style>
