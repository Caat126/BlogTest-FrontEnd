<template>
    <!-- Page Header Start -->
    <div class="container py-5 px-2 bg-primary">
        <div class="row py-5 px-4">
            <div class="col-sm-6 text-center text-md-left">
                <h1 class="mb-3 mb-md-0 text-white text-uppercase font-weight-bold">Sobre Mí</h1>
            </div>
            <div class="col-sm-6 text-center text-md-right">
                <div class="d-inline-flex pt-2">
                    <h4 class="m-0 text-white">
                        <RouterLink to="/" class="text-white">Inicio</RouterLink>
                    </h4>
                    <h4 class="m-0 text-white px-2">/</h4>
                    <h4 class="m-0 text-white">Sobre Mí</h4>
                </div>
            </div>
        </div>
    </div>
    <!-- Page Header End -->

    <!-- About Start -->
    <div class="container bg-white pt-5">
        <div class="row px-3 pb-5">
            <div class="col-md-12">
                <h2 class="mb-4 font-weight-bold">Dev FullStack con amplia experiencia</h2>
                <img class="img-fluid float-left w-50 mr-4 mb-3" src="/Eu.png" alt="Image">
                <p class="m-0 text-justify">
                    Saludos, soy un desarrollador Full Stack con una trayectoria que abarca varios años de experiencia
                    en el diseño, desarrollo y despliegue de aplicaciones web y móviles. Mi viaje en la programación
                    comenzó con una sólida formación en ingeniería informática, la cual ha sido complementada con una
                    constante búsqueda de aprendizaje y actualización en las últimas tecnologías del sector.
                    <br><br>
                    En el ámbito front-end, poseo una profunda experiencia en la creación de interfaces de usuario
                    dinámicas y atractivas utilizando tecnologías como HTML5, CSS3 y JavaScript, junto con frameworks
                    modernos como Vue.js y Laravel. Esta combinación de habilidades me permite no solo materializar
                    diseños atractivos, sino también optimizar el rendimiento y la usabilidad de las aplicaciones.
                    <br><br>
                    En el backend, me especializo en el desarrollo de APIs robustas y escalables utilizando Node.js y
                    Express, además de la implementación y administración eficiente de bases de datos SQL y NoSQL como
                    MySQL, PostgreSQL y MongoDB. Mi enfoque en el diseño de arquitecturas sólidas y seguras me ha
                    permitido desarrollar sistemas que manejan grandes volúmenes de datos de manera eficiente y
                    confiable.
                    <br><br>
                    Además, cuento con experiencia en la integración de servicios de terceros, como sistemas de pago y
                    APIs de redes sociales, así como en la implementación de autenticación y autorización seguras
                    utilizando técnicas como JWT y OAuth.
                    <br><br>
                    Lo que más me apasiona de ser desarrollador Full Stack es la capacidad de trabajar en todos los
                    aspectos de un proyecto, desde la concepción y el diseño hasta la implementación y el despliegue, lo
                    que me permite tener una visión completa del proceso de desarrollo y garantizar la entrega de
                    productos de alta calidad que satisfagan las necesidades del cliente y los usuarios finales. Estoy
                    constantemente buscando desafíos nuevos y emocionantes que me permitan seguir creciendo
                    profesionalmente y contribuir al éxito de proyectos innovadores y ambiciosos.
                </p>
            </div>
            <div class="col-md-12 pt-4">
                <div class="d-flex flex-column skills">
                    <div class="progress mb-3">
                        <div class="progress-bar" role="progressbar" style="width: 90%;" aria-valuenow="25"
                            aria-valuemin="0" aria-valuemax="100">HTML 90%</div>
                    </div>
                    <div class="progress mb-3">
                        <div class="progress-bar" role="progressbar" style="width: 85%;" aria-valuenow="25"
                            aria-valuemin="0" aria-valuemax="100">CSS 85%</div>
                    </div>
                    <div class="progress mb-3">
                        <div class="progress-bar" role="progressbar" style="width: 80%;" aria-valuenow="25"
                            aria-valuemin="0" aria-valuemax="100"> JavaScript 80%</div>
                    </div>
                    <div class="progress mb-3">
                        <div class="progress-bar" role="progressbar" style="width: 75%;" aria-valuenow="25"
                            aria-valuemin="0" aria-valuemax="100"> Vue 75%</div>
                    </div>
                    <div class="progress mb-3">
                        <div class="progress-bar" role="progressbar" style="width: 70%;" aria-valuenow="25"
                            aria-valuemin="0" aria-valuemax="100"> PHP 70%</div>
                    </div>
                    <div class="progress mb-3">
                        <div class="progress-bar" role="progressbar" style="width: 80%;" aria-valuenow="25"
                            aria-valuemin="0" aria-valuemax="100"> Laravel 80%</div>
                    </div>
                    <div class="progress mb-3">
                        <div class="progress-bar" role="progressbar" style="width: 75%;" aria-valuenow="25"
                            aria-valuemin="0" aria-valuemax="100"> API REST 75%</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- About End -->


</template>

<script>
export default {

    setup() {

        return {

        }
    }
}
</script>

<style></style>