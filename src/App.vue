<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>
<template>
  <div style="width: 100%">
    <br>
    <div class="container">
      <div class="title-container" style="text-align: center">
        <h2 style="font-size: 2.5rem; font-weight: bold">STATUS  DIARIO DE FLOTA NACIONAL</h2>
      </div>
      <br/>
      <div class="col-8"> 
        <div style="width: 100%;">
          <form class="d-flex align-items-center justify-content-center">
            <label for="placa" class="me-4 fw-bold">PLACA:</label>
            <input
              id="placa"
              class="form-control me-4"
              type="search"
              placeholder="AEK-829"
              aria-label="BUSCAR"
              style="width: 400px; flex: 1"
            />
            <button type="button" class="btn btn-primary" style="min-width: 150px">Buscar</button>
          </form>
        </div>
      </div>
    </div>
    <div class="container mt-4">
      <div class="row d-flex justify-content-center">
        <div class="col-12 col-sm-4 d-flex justify-content-center mb-2">
          <router-link
            to="/InformacionGeneral"
            tag="button"
            class="btn btn-primary w-100"
            style="font-weight: bold; font-size: 1.2rem;height: 100%"
          >INFORMACIÓN GENERAL 
          </router-link>
        </div>
        <div class="col-12 col-sm-4 d-flex justify-content-center mb-2">
          <router-link to="/RelevosTodos" class="btn btn-warning w-100 d-flex align-items-center justify-content-center" style="font-weight: bold; font-size: 1.2rem; height: 100%">
    RELEVOS
  </router-link>  
        </div>
        <div class="col-12 col-sm-4 d-flex justify-content-center mb-2">
          <router-link to="/ReportesDiario" class="btn btn-success w-100 d-flex align-items-center justify-content-center" style="font-weight: bold; font-size: 1.2rem;">
    REPORTES
  </router-link>
        </div>
      </div>
    </div>
    <RouterView />
  </div>
</template>


<style>
body, html {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

#app {
  display: flex;
  flex-direction: column;
  align-items: flex-start; /* Alinea los elementos al inicio (arriba) */
  height: 100vh; /* Asegura que el contenedor ocupe toda la altura de la ventana */
}

.title-container {
  flex: 1; /* Ocupa el espacio restante */
}

h2 {
  font-weight: bold; /* Texto en negrita */
  margin: 0; /* Elimina el margen predeterminado del título */
  color: #7f0000; /* Color rojo */
}
</style>

