<template>
  <div id="app">
    <page-services></page-services>
    <!--Movies-->
    <div class="container-fluid">
          <section-api></section-api>
    </div>
    <!--Team-->
    <h2 class="d-flex justify-content-center align-items-center">{{tittle}}</h2>
    <div class="container-fluid">
      <div class="row justify-content-center mb-5">
        <div class="col mt-5" v-for="(item, index) of team" :key="index">
          <team-card v-bind:member="item"></team-card>
        </div>
      </div>
    </div>
    <!-- Footer -->
    <page-footer></page-footer>
  </div>
</template>

<script>

import TeamCard from './components/TeamCard.vue'
import PageFooter from './components/PageFooter.vue'
import SectionApi from './components/SectionApi'
import PageServices from './components/PageServices.vue'

export default {
  
  name: 'App',
  components:{
    TeamCard,
    PageFooter,
    SectionApi,
    PageServices,
  },
  data(){
    return{
      tittle: "Team Members",
      team: [
        {
          codigo: 1,
          nombre: "Aquiles Elías Celedón Caballero",
          descripcion: "Ingeniero de Sistemas en formación. 29 años de edad, amante de los gatos y los videojuegos.",
          rol: "Desarrollador Backend",
          imagen: "./img/Aquiles.jpg",
          alt: "Aquiles Celedón",
        },
        {
          codigo: 2,
          nombre: "Wilmer Andrés Alarcón Tobasura",
          descripcion: "Ingeniero Industrial, especializado en Producción y Logística de la Universidad Distrital. Candidato a Magister en Investigación de Operaciones y Estadística. Hobbies principales: lectura y Modelos de Producción.",
          rol: "Arquitecto de Software",
          imagen: "./img/Wilmer.jpg",
          alt: "Wilmer Alarcón",
        },
        {
          codigo: 3,
          nombre: "Johan Iván Vega Bello",
          descripcion: "Ingeniero de Sistemas en formación. 20 años de edad, amante de los videojuegos y el mundo del hardware.",
          rol: "Tester",
          imagen: "./img/Johan.jpg",
          alt: "Johan Vega",
        },
        {
          codigo: 4,
          nombre: "Brandon Estiven Franco Quiceno",
          descripcion: "Ingeniero de Sistemas y Computación, graduado de la Universidad Tecnológica de Pereira. 28 años de edad y apasionado por la lectura.",
          rol: "Desarrollador Frontend",
          imagen: "./img/Foto.jpg",
          alt: "Brandon Franco",
        }
      ]
    }
  }
}
</script>