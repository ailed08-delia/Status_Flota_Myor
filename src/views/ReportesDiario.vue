<template>
    <div class="container my-2">
       <div class="row justify-content-center">
        <div class="col-12 col-lg-12">
               <div class="card">
                   <h5 class="card-header" style="font-weight: bold;">AEK-829</h5>
                   <div class="card-body">
                       <div class="text-center mb-4">
                           <h3 style="font-weight: bold;">REPORTES DIARIO</h3>
                       </div>
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