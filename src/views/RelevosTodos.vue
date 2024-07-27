<template>
  <div class="container my-2">
    <div class="row justify-content-center">
      <div class="col-12 col-lg-12">
        <div class="card">
          <h5 class="card-header" style="font-weight: bold">AEK-829</h5>
          <div class="card-body">
            <div class="container">
              <h3 class="text-center" style="font-weight: bold">RELEVOS</h3>
              <hr>
              <div class="d-flex align-items-start">
                <div
                  class="nav flex-column nav-pills me-20"
                  id="v-pills-tab"
                  role="tablist"
                  aria-orientation="vertical"
                >
                  <button
                    v-for="(relevo, index) in relevos"
                    :key="index"
                    :class="['nav-link', { active: index === 0 }]"
                    :id="`${relevo.id}-tab`"
                    data-bs-toggle="pill"
                    :data-bs-target="`#${relevo.id}`"
                    type="button"
                    role="tab"
                    :aria-controls="`${relevo.id}`"
                    :aria-selected="index === 0"
                    class="custom-button mb-2"
                  >
                    {{ relevo.label }}
                  </button>
                </div>

                <div class="container tab-content" id="v-pills-tabContent">
                  <div
                    v-for="(relevo, index) in relevos"
                    :key="index"
                    :id="relevo.id"
                    class="tab-pane fade w-100"
                    :class="['tab-pane', { 'show active': index === 0 }]"
                    role="tabpanel"
                    :aria-labelledby="`${relevo.id}-tab`"
                  >
                    <form>
                      <h3 class="mb-4 text-center" style="font-weight: bold">{{ relevo.label }}</h3>
                      <hr>
                      <div
                        v-for="(input, inputIndex) in relevo.inputs"
                        :key="inputIndex"
                        class="mb-3"
                      >
                        <label :for="input.id" class="form-label">{{ input.label }}</label>
                        <input
                          v-if="input.type === 'text' || input.type === 'time'"
                          :type="input.type"
                          class="form-control w-100"
                          :id="input.id"
                          style="width: 50%"
                        />
                        <textarea
                          v-else-if="input.type === 'textarea'"
                          class="form-control w-100"
                          :id="input.id"
                          rows="3"
                          style="width: 50%"
                        ></textarea>
                      </div>
                      <button type="submit" class="btn btn-primary w-100">Guardar</button>
                    </form>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
     
<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      relevos: [
        {
          id: 'primerRelevo',
          label: 'Primer Relevo',
          inputs: [
            { id: 'relevo', label: '1er Relevo', type: 'text' },
            { id: 'horaRelevo', label: 'Hora del 1er Relevo', type: 'time' },
            { id: 'tiempo', label: '1er Tiempo', type: 'text' },
            { id: 'tiempoEjecutado', label: '1er Tiempo Ejecutado', type: 'text' },
            { id: 'observacion', label: '1era Observación', type: 'textarea' }
          ]
        },
        {
          id: 'segundoRelevo',
          label: 'Segundo Relevo',
          inputs: [
            { id: 'relevo', label: '2do Relevo', type: 'text' },
            { id: 'horaRelevo', label: 'Hora del 2do Relevo', type: 'time' },
            { id: 'tiempo', label: '2do Tiempo', type: 'text' },
            { id: 'tiempoEjecutado', label: '2do Tiempo Ejecutado', type: 'text' },
            { id: 'observacion', label: '2da Observación', type: 'textarea' }
          ]
        },
        {
          id: 'tercerRelevo',
          label: 'Tercer Relevo',
          inputs: [
            { id: 'relevo', label: '3er Relevo', type: 'text' },
            { id: 'horaRelevo', label: 'Hora del 3er Relevo', type: 'time' },
            { id: 'tiempo', label: '3er Tiempo', type: 'text' },
            { id: 'tiempoEjecutado', label: '3er Tiempo Ejecutado', type: 'text' },
            { id: 'observacion', label: '3ra Observación', type: 'textarea' }
          ]
        },
        {
          id: 'cuartoRelevo',
          label: 'Cuarto Relevo',
          inputs: [
            { id: 'relevo', label: '4to Relevo', type: 'text' },
            { id: 'horaRelevo', label: 'Hora del 4to Relevo', type: 'time' },
            { id: 'tiempo', label: '4to Tiempo', type: 'text' },
            { id: 'tiempoEjecutado', label: '4to Tiempo Ejecutado', type: 'text' },
            { id: 'observacion', label: '4ta Observación', type: 'textarea' }
          ]
        },
        {
          id: 'quintoRelevo',
          label: 'Quinto Relevo',
          inputs: [
            { id: 'relevo', label: '5to Relevo', type: 'text' },
            { id: 'horaRelevo', label: 'Hora del 5to Relevo', type: 'time' },
            { id: 'tiempo', label: '5to Tiempo', type: 'text' },
            { id: 'tiempoEjecutado', label: '5to Tiempo Ejecutado', type: 'text' },
            { id: 'observacion', label: '5ta Observación', type: 'textarea' }
          ]
        },
        {
          id: 'sextoRelevo',
          label: 'Sexto Relevo',
          inputs: [
            { id: 'relevo', label: '6to Relevo', type: 'text' },
            { id: 'horaRelevo', label: 'Hora del 6to Relevo', type: 'time' },
            { id: 'tiempo', label: '6to Tiempo', type: 'text' },
            { id: 'tiempoEjecutado', label: '6to Tiempo Ejecutado', type: 'text' },
            { id: 'observacion', label: '6ta Observación', type: 'textarea' }
          ]
        },
        {
          id: 'setimoRelevo',
          label: 'Sétimo Relevo',
          inputs: [
            { id: 'relevo', label: '7mo Relevo', type: 'text' },
            { id: 'horaRelevo', label: 'Hora del 7mo Relevo', type: 'time' },
            { id: 'tiempo', label: '7mo Tiempo', type: 'text' },
            { id: 'tiempoEjecutado', label: '7mo Tiempo Ejecutado', type: 'text' },
            { id: 'observacion', label: '7ma Observación', type: 'textarea' }
          ]
        },
        {
          id: 'octavoRelevo',
          label: 'Octavo Relevo',
          inputs: [
            { id: 'relevo', label: '8vo Relevo', type: 'text' },
            { id: 'horaRelevo', label: 'Hora del 8vo Relevo', type: 'time' },
            { id: 'tiempo', label: '8vo Tiempo', type: 'text' },
            { id: 'tiempoEjecutado', label: '8vo Tiempo Ejecutado', type: 'text' },
            { id: 'observacion', label: '8va Observación', type: 'textarea' }
          ]
        },
        {
          id: 'novenoRelevo',
          label: 'Noveno Relevo',
          inputs: [
            { id: 'relevo', label: '9no Relevo', type: 'text' },
            { id: 'horaRelevo', label: 'Hora del 9no Relevo', type: 'time' },
            { id: 'tiempo', label: '9no Tiempo', type: 'text' },
            { id: 'tiempoEjecutado', label: '9no Tiempo Ejecutado', type: 'text' },
            { id: 'observacion', label: '9na Observación', type: 'textarea' }
          ]
        }
      ]
    }
  }
})
</script>     
<style scoped>
.custom-button {
  width: 200px;
  height: 60px;
  margin-right: 50px;
  background-color: #007bff;
  color: #fff;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  font-size: 1rem;
}

.custom-button.active {
  background-color: #0056b3;
}
</style>