<template>
    <div class="sidebar">
                <div class="sidebar-text d-flex flex-column h-100 justify-content-center text-center">
                    <img class="mx-auto d-block w-75 bg-primary img-fluid rounded-circle mb-4 p-3" src="/Eu.png" alt="Image">
                    <h1 class="font-weight-bold">{{ nombre }}</h1>
                    <p class="mb-4" style="text-align: justify;">
                        Bienvenido a mi blog personal, mi nombre es {{ nombre }} y espero que te guste y encuentres informacion util para tus proyectos.
                    </p>
                    <div class="d-flex justify-content-center mb-5">
                        <a class="btn btn-outline-primary mr-2" href="https://github.com/Caat126" target="_blank"><i class="fab fa-github"></i></a>
                        <a class="btn btn-outline-primary mr-2" href="https://www.facebook.com/profile.php?id=1345941534" target="_blank"><i class="fab fa-facebook-f"></i></a>
                        <a class="btn btn-outline-primary mr-2" href="www.linkedin.com/in/carlos-andrés-arguedas-teodovich-3b4a80252" target="_blank"><i class="fab fa-linkedin-in"></i></a>
                        <a class="btn btn-outline-primary mr-2" href="https://www.instagram.com/ca2t/" target="_blank"><i class="fab fa-instagram"></i></a>
                    </div>
                    <RouterLink to="/contacto" class="btn btn-lg btn-block btn-primary mt-auto">Contáctame</RouterLink>
                </div>
                <div class="sidebar-icon d-flex flex-column h-100 justify-content-center text-right">
                    <i class="fas fa-2x fa-angle-double-right text-primary"></i>
                </div>
            </div>
</template>

<script setup>
defineProps({
    nombre: {
        type: String,
        required: true
    }
})

</script>

<style scoped></style>