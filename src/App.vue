<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Informacion from './components/Informacion.vue'
</script>

<template>
  <div class="wrapper">
    <Informacion nombre="Carlos Andrés Arguedas" />

    <div class="content">
      <!-- Navbar Start -->
      <div class="container p-0">
        <nav class="navbar navbar-expand-lg bg-secondary navbar-dark">
          <a href="#" class="navbar-brand d-block d-lg-none">Navigation</a>
          <button type="button" class="navbar-toggler" data-toggle="collapse" data-target="#navbarCollapse">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse justify-content-between" id="navbarCollapse">
            <div class="navbar-nav m-auto">
              <RouterLink to="/" class="nav-item nav-link">Inicio</RouterLink>
              <RouterLink to="/blog" class="nav-item nav-link">Blog</RouterLink>
              <RouterLink to="/categorias" class="nav-item nav-link">Categorias</RouterLink>
              <RouterLink to="/sobremi" class="nav-item nav-link">Sobre mí</RouterLink>
              <RouterLink to="/contacto" class="nav-item nav-link">Contacto</RouterLink>
            </div>
          </div>
        </nav>
      </div>
      <!-- Navbar End -->
      <RouterView />

      <!-- Footer Start -->
      <div class="container py-4 bg-secondary text-center">
        <p class="m-0 text-white">
          &copy; <a class="text-white font-weight-bold" href="#">BlogPersonalTest</a>. Todos los derechos reservados. Diseñado por <a
            class="text-white font-weight-bold" href="https://github.com/Caat126">Caat126</a>
        </p>
      </div>
      <!-- Footer End -->

    </div>
  </div>


</template>
