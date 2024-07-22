<template>
    <div class="container my-2">
       <div class="row justify-content-center">
        <div class="col-12 col-lg-12">
               <div class="card">
                   <h5 class="card-header" style="font-weight: bold;">AEK-829</h5>
                   <div class="card-body">
                       <div class="text-center mb-4">
                           <h3 style="font-weight: bold;">INFORMACIÓN GENERAL</h3>
                       </div>
                       <form @submit.prevent="submitForm">
                           <div class="row">
                               <div class="col-md-6">
                                   <!-- Columna izquierda -->
                                   <div class="mb-3">
                                       <label for="placa" class="form-label">PLACA:</label>
                                       <input v-model="placa" type="text" class="form-control" id="placa" placeholder="Ingrese la placa">
                                   </div>
                                   <div class="mb-3">
                                       <label for="furgon" class="form-label">FURGÓN:</label>
                                       <input v-model="furgon" type="text" class="form-control" id="furgon" placeholder="Ingrese el furgón">
                                   </div>
                                   <div class="mb-3">
                                       <label for="piloto" class="form-label">PILOTO:</label>
                                       <input v-model="piloto" type="text" class="form-control" id="piloto" placeholder="Ingrese el piloto">
                                   </div>
                                   <div class="mb-3">
                                       <label for="copiloto" class="form-label">COPILOTO:</label>
                                       <input v-model="copiloto" type="text" class="form-control" id="copiloto" placeholder="Ingrese el copiloto">
                                   </div>
                                   <div class="mb-3">
                                       <label for="conduce" class="form-label">¿CONDUCE?:</label>
                                       <input v-model="conduce" type="text" class="form-control" id="conduce" placeholder="¿Conduce?">
                                   </div>
                                   <div class="mb-3">
                                       <label for="ruta" class="form-label">RUTA:</label>
                                       <input v-model="ruta" type="text" class="form-control" id="ruta" placeholder="Ingrese la ruta">
                                   </div>
                                   <div class="mb-3">
                                       <label for="fechaSalida" class="form-label">Fecha de Salida:</label>
                                       <input v-model="fechaSalida" type="date" class="form-control" id="fechaSalida">
                                   </div>
                               </div>
                               <div class="col-md-6">
                                   <!-- Columna derecha -->
                                   <div class="mb-3">
                                       <label for="horaSalida" class="form-label">Hora de Salida:</label>
                                       <input v-model="horaSalida" type="time" class="form-control" id="horaSalida">
                                   </div>
                                   <div class="mb-3">
                                       <label for="tipoCarga" class="form-label">Tipo de Carga:</label>
                                       <input v-model="tipoCarga" type="text" class="form-control" id="tipoCarga" placeholder="Ingrese el tipo de carga">
                                   </div>
                                   <div class="mb-3">
                                       <label for="guias" class="form-label">Guías:</label>
                                       <div class="input-group">
                                           <input v-model="guias" type="text" class="form-control" id="guias" placeholder="Ingrese las guías">
                                           <button @click="agregarGuia" class="btn btn-success" type="button">Agregar</button>
                                       </div>
                                   </div>
                                   <div class="mb-3">
                                       <label for="pesoPlanilla" class="form-label">Peso Planilla:</label>
                                       <div class="input-group">
                                           <input v-model="pesoPlanilla" type="number" class="form-control" id="pesoPlanilla" placeholder="Ingrese el peso planilla" step="0.01">
                                           <button @click="agregarPeso" class="btn btn-success" type="button">Agregar</button>
                                       </div>
                                   </div>
                                   <div class="mb-3">
                                       <label for="pesoBalanza" class="form-label">Peso Balanza:</label>
                                       <input v-model="pesoBalanza" type="number" class="form-control" id="pesoBalanza" placeholder="Ingrese el peso balanza" step="0.01">
                                   </div>
                                   <div class="mb-3">
                                       <label for="horaPeaje" class="form-label">Hora de Peaje:</label>
                                       <input v-model="horaPeaje" type="time" class="form-control" id="horaPeaje">
                                   </div>
                                   <div class="mb-3">
                                       <label for="ubicacionActual" class="form-label">Ubicación Actual:</label>
                                       <input v-model="ubicacionActual" type="text" class="form-control" id="ubicacionActual" placeholder="Ingrese la ubicación actual">
                                   </div>
                               </div>
                           </div>
                           <div class="text-center mt-4">
                             
                               <a href="#" class="btn btn-primary">Guardar</a>
                           </div>
                       </form>
                   </div>
               </div>
           </div>
       </div>
   </div>
   
   
   
     </template>
     
     <script>
     export default {
       data() {
         return {
           placa: '',
           furgon: '',
           piloto: '',
           copiloto: '',
           conduce: '',
           ruta: '',
           fechaSalida: '',
           horaSalida: '',
           tipoCarga: '',
           guias: '',
           pesoPlanilla: '',
           pesoBalanza: '',
           horaPeaje: '',
           ubicacionActual: ''
         };
       },
       computed: {
         tiempoTotal() {
           // Implementa la lógica para calcular el tiempo total ejecutado según tus requerimientos
           return '2 días 3 horas'; // Ejemplo estático, sustituir con la lógica adecuada
         }
       },
       methods: {
         agregarGuia() {
           console.log('Agregar guía:', this.guias);
         },
         agregarPeso() {
           console.log('Agregar peso:', this.pesoPlanilla);
         },
         submitForm() {
           console.log('Formulario enviado');
           // Aquí puedes enviar los datos del formulario a través de una API o realizar otras acciones necesarias
         }
       }
     };
     </script>
     
     <style scoped>
     /* Estilos opcionales para personalizar el formulario */
     </style>
     