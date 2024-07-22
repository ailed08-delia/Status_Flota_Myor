<template>
  <div>
    <div class="container">
      <div class="title-container" style="text-align: center">
        <h2 style="font-size: 2.5rem; font-weight: bold">STATUS DIARIO DE FLOTA NACIONAL</h2>
      </div>
      <br />
      <div class="col-8">
        <div class="container-fluid">
          <form class="d-flex align-items-center">
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
          <button
            type="button"
            class="btn btn-primary w-100"
            style="font-weight: bold; font-size: 1.2rem"
          >
            INFORMACIÓN GENERAL
          </button>
        </div>
        <div class="col-12 col-sm-4 d-flex justify-content-center mb-2">
          <button
            to="/Relevos.vue"
            type="button"
            class="btn btn-warning w-100"
            style="font-weight: bold; font-size: 1.2rem"
          >
            RELEVOS
          </button>
        </div>
        <div class="col-12 col-sm-4 d-flex justify-content-center mb-2">
          <button
            type="button"
            class="btn btn-success w-100"
            style="font-weight: bold; font-size: 1.2rem"
          >
            REPORTES
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
  
  
  
    <script lang="ts">
</script>
  
    <style scoped>
.card-header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  background-color: #ffffff; /* Fondo blanco */
  color: #7f0000; /* Color de texto rojo para el título */
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 2px solid #7f0000; /* Borde rojo en la parte inferior */
  box-sizing: border-box; /* Ajusta el modelo de caja para incluir el padding en el ancho total */
}

.title-container {
  flex: 1; /* Ocupa el espacio restante */
}

.logo-container {
  margin-left: 10px; /* Agrega espacio entre el título y la imagen */
}

.logo {
  width: 165px; /* Ancho de la imagen */
  height: 56px; /* Alto de la imagen */
}

h2 {
  font-weight: bold; /* Texto en negrita */
  margin: 0; /* Elimina el margen predeterminado del título */
  color: #7f0000; /* Color rojo */
}
</style>