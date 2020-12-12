<template>
    <header>
        <div class="nav-list">
            <nav class="navbar navbar-expand-lg navbar-light bg-light">
                <a class="navbar-brand" href="#"><img :src="logo" width="30px" height="30px" alt="logo" class="d-inline-block align-top">{{title}}</a>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav mr-auto">
                        <li v-for="link in links" :key="link.id" :class="link.class">
                            <a class="nav-link" :href="link.href">{{link.name}}<span class="sr-only">{{link.x}}</span></a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
        <div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
            <div class="carousel-inner">
                <div class="carousel-item active">
                    <img src="../assets/img/banner.jpg" class="d-block w-100" alt="Banner">
                </div>
                <div class="carousel-item">
                    <img src="../assets/img/banner2.jpg" class="d-block w-100" alt="Banner">
                </div>
                <div class="carousel-item">
                    <img src="../assets/img/banner3.jpg" class="d-block w-100" alt="Banner">
                </div>
                <div class="carousel-item">
                    <img src="../assets/img/banner4.jpg" class="d-block w-100" alt="Banner">
                </div>
<!--
                <div v-for="carro in carruseles" :key="carro.id">
                    <div :class="carro.class">
                        <img :src="carro.img" class="d-block w-100" alt="Banner">
                    </div>
                </div>
-->
            </div>
        </div>
    </header>
</template>

<script>
    export default {
        data() {
            return {
                name: "PageHeader",
                title: "Medio Ambiente",
                logo: require("../assets/img/logo.png"),
                links: [
                    { href: "#", name: "Inicio", x: "(current)", class:"nav-item active"},
                    { href: "#services", name: "Servicios", x: "", class:"nav-item"},
                    { href: "#news", name: "Noticias", x: "", class:"nav-item"},
                    { href: "#team", name: "Equipo", x: "", class:"nav-item"}
                ],
                carruseles: [
                    {img: require("../assets/img/banner.jpg"), class:"carousel-item active"},
                    {img: require("../assets/img/banner2.jpg"), class:"carousel-item"},
                    {img: require("../assets/img/banner3.jpg"), class:"carousel-item"},
                    {img: require("../assets/img/banner4.jpg"), class:"carousel-item"}
                ]
            }
        },
        components: {

        }
    }

</script>

<style scoped>

</style>
