<script setup>
import icono1 from '/src/assets/ventas.svg';
import icono2 from '/src/assets/ecomerce.svg';
import icono3 from '/src/assets/configuracion.svg';
import icono4 from '/src/assets/uiux.svg';
import icono5 from '/src/assets/watch.svg';

import { ref } from 'vue';
const titulo = 'Desarrollador Backend';
const fecha = 'Desde Marzo 2021 / Actualidad';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'Lideré el desarrollo de un sistema de gestión de inventarios en tiempo real que optimizó el flujo de trabajo y redujo los errores en un 25%.' },
    { id: 2, src: icono2, parrafo: 'Desarrollé y mantuve APIs RESTful utilizando Node.js y Express, mejorando la eficiencia de la comunicación entre sistemas en un 30%.' },
    { id: 3, src: icono3, parrafo: 'Implementé soluciones de bases de datos NoSQL con MongoDB, mejorando la escalabilidad y el rendimiento de la plataforma.' },
    { id: 4, src: icono4, parrafo: 'Trabajé estrechamente con equipos de frontend y UX/UI para garantizar la integración eficiente de la interfaz y la experiencia del usuario.' },
    { id: 5, src: icono5, parrafo: 'Automatizé el proceso de testing y despliegue continuo utilizando herramientas como Jenkins y Docker, reduciendo los errores en producción en un 40%.' },
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experiencia in experiencias" :key="experiencia.id">
                <img class="imagen-svg" :src="experiencia.src" width="45rem" :alt="experiencia.parrafo">
                <p>{{ experiencia.parrafo }}</p>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: coral;
}

.fecha {
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>
