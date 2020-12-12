<template>
    <div id="app">
        <!--Encabezado-->
        <page-header id="Inicio"></page-header>
        <hr>
        <section id="services" class="servicios">
            <div class="container-fluid">
                <div class="row justify-content-center mb-5">
                    <div class="col-sm-6 col-xs-12 col-lg-4 mt-5">
                        <div class="d-flex justify-content-center p-2">
                            <img src="../src/assets/img/glass_of_water.jpg" class="card-img-top" width="300" height="400" alt="Service1">
                        </div>
                        <div class="card">
                            <!-- Servicio 1 -->
                            <div class="card-body">
                                <p class="card-text">Con esta herramienta podrás realizar un cálculo aproximado de tu consumo de agua diario y mensual.</p>
                                <a href="https://www.watercalculator.org/" class="btn btn-primary" target="_blank">Conocer más...</a>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-6 col-xs-12 col-lg-4 mt-5">
                        <div class="d-flex justify-content-center p-2">
                            <img src="../src/assets/img/carbon_foot_print.jpeg" class="card-img-top" width="300" height="400" alt="Service2">
                        </div>
                        <div class="card">
                            <!-- Servicio 2 -->
                            <div class="card-body">
                                <p class="card-text">¿Sabes que es la huella de carbono? Con este aplicativo podrás saberlo e identificar hábitos que pueden estar dañando el planeta y tu salud.</p>
                                <a href="https://www.carbonfootprint.com/calculator.aspx" class="btn btn-primary" target="_blank">Conocer más...</a>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-6 col-xs-12 col-lg-4 mt-5">
                        <div class="d-flex justify-content-center p-2">
                            <img src="../src/assets/img/recycle_bin.jpg" class="card-img-top" width="300" height="400" alt="Service3">
                        </div>
                        <div class="card">
                            <!-- Servicio 3 -->
                            <div class="card-body">
                                <p class="card-text">¿Tienes montones de basura electronica o baterias y no sabes que hacer con ella? Conoce los puntos de recolección más cercanos y cuida del planeta.</p>
                                <a href="https://www.redverde.co/" class="btn btn-primary" target="_blank">Conocer más...</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <hr>
        <!--Movies-->
        <div class="container-fluid">
            <div id="news"></div>
            <section-api></section-api>
        </div>
        <!--Team-->
        <hr>
        <h2 class="d-flex justify-content-center align-items-center">{{tittle}}</h2>
        <div id="team" class="container-fluid">
            <div class="row justify-content-center mb-5">
                <div class="col mt-5" v-for="(item, index) of team" :key="index">
                    <team-card v-bind:member="item"></team-card>
                </div>
            </div>
        </div>
        <!-- Footer -->
        <hr>
        <page-footer></page-footer>
    </div>
</template>

<script>
    import PageHeader from './components/PageHeader.vue'
    import TeamCard from './components/TeamCard.vue'
    import PageFooter from './components/PageFooter.vue'
    import SectionApi from './components/SectionApi'

    export default {

        name: 'App',
        components: {
            PageHeader,
            TeamCard,
            PageFooter,
            SectionApi
        },
        data() {
            return {
                tittle: "Team Members",
                team: [{
                        codigo: 1,
                        nombre: "Aquiles Elías Celedón Caballero",
                        descripcion: "Ingeniero de Sistemas en formación. 29 años de edad, amante de los gatos y los videojuegos.",
                        rol: "Desarrollador Backend",
                        imagen: require("../src/assets/img/Aquiles.jpg"),
                        alt: "Aquiles Celedón",
                    },
                    {
                        codigo: 2,
                        nombre: "Wilmer Andrés Alarcón Tobasura",
                        descripcion: "Ingeniero Industrial, especializado en Producción y Logística de la Universidad Distrital. Candidato a Magister en Investigación de Operaciones y Estadística. Hobbies principales: lectura y Modelos de Producción.",
                        rol: "Arquitecto de Software",
                        imagen: require("../src/assets/img/Wilmer.jpg"),
                        alt: "Wilmer Alarcón",
                    },
                    {
                        codigo: 3,
                        nombre: "Johan Iván Vega Bello",
                        descripcion: "Ingeniero de Sistemas en formación. 20 años de edad, amante de los videojuegos y el mundo del hardware.",
                        rol: "Tester",
                        imagen: require("../src/assets/img/Johan.jpg"),
                        alt: "Johan Vega",
                    },
                    {
                        codigo: 4,
                        nombre: "Brandon Estiven Franco Quiceno",
                        descripcion: "Ingeniero de Sistemas y Computación, graduado de la Universidad Tecnológica de Pereira. 28 años de edad y apasionado por la lectura.",
                        rol: "Desarrollador Frontend",
                        imagen: require("../src/assets/img/Foto.jpg"),
                        alt: "Brandon Franco",
                    }
                ]
            }
        }
    }

</script>
