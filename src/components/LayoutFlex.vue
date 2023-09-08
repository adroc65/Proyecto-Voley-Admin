<script setup>

  import Control from './Control.vue'
  import Estadisticas from './Estadisticas.vue'
  import Marcador from './Marcador.vue'
  import Jugadas from './Jugadas.vue'
  import Rotacion from './Rotacion.vue'

</script>

<template>
    <div class="mt-4 px-2 mx-auto xl:container">
        <div class="flex flex-col lg:flex-row">
            <div class="lg:w-1/3 mr-2 flex-col">
                <div class="mb-2 lg:h-3/4 overflow-y-scroll bg-orange-300 shadow-md rounded-lg">
                    <Estadisticas />
                </div>
                <div class="lg:h-1/4 bg-orange-600 shadow-md rounded-lg">
                    <Rotacion />
                </div>
            </div>
            <div class="mr-2 flex-col lg:w-2/3 ">
                <div class="mb-2 lg:h-2/5 bg-gray-300 shadow-md rounded-lg">
                    <Marcador />
                </div>
                <div class="lg:h-3/5 bg-gray-400 shadow-md rounded-lg">
                    <Control />
                </div>
            </div>
            <div class="overflow-y-scroll lg:w-1/3 bg-blue-200 shadow-md rounded-lg">
                <Jugadas />
            </div>
        </div>
    </div>
    
</template>