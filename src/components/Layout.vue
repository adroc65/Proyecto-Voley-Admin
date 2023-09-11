<script setup>
import { ref, reactive } from "vue";

import Control from './Control.vue'
import Estadisticas from './Estadisticas.vue'
import Marcador from './Marcador.vue'
import Jugadas from './Jugadas.vue'
import Rotacion from './Rotacion.vue'
import TablaPuntos from './Tabla.vue'
import TablaCss from './TablaCss.vue'
import IndicadorSets from './IndicadorSets.vue'

const marcadorCasa = reactive({
    nombre: 'Casa',
    color: 'primary',
    cantidadPtos: '16',
    saque: 'No',
    rotacion: '1',
    timeOuts: '0',
    cambios: '0',
})
const marcadorVisita = reactive({
    nombre: 'Visita',
    color: 'secondary',
    cantidadPtos: '9',
    saque: 'Si',
    rotacion: '3',
    timeOuts: '2',
    cambios: '1',
})
const controlSets = reactive({
    total: '5',
    jugando: '3',
    finPartido: false,
})
const sets = ref([
    {
        name: 'Set #1',
        estado: 'completado',
        mCasa: '25',
        mVisita: '18'
    },
    {
        name: 'Set #2',
        estado: 'completado',
        mCasa: '15',
        mVisita: '25'
    },
    {
        name: 'Set #3',
        estado: 'jugando',
        mCasa: 'x',
        mVisita: 'x'
    },
    {
        name: 'Set #4',
        estado: 'pendiente',
        mCasa: 'x',
        mVisita: 'x'
    },
    {
        name: 'Set #5',
        estado: 'pendiente',
        mCasa: 'x',
        mVisita: 'x'
    },
])


const marcador = () => {
    
    console.log(controlSets.jugando)
    const estado = `controlSets.${controlSets.jugando}`
    
    
}
marcador()

</script>

<template>

    <div class="p-10 grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-5">
        <!--Card 1-->
        <div class="md:col-span-3 lg:col-span-4 placeholder:rounded-md bg-gray-300 overflow-hidden shadow-lg">
            <div class="grid grid-cols-1 md:grid-cols-2 items-center gap-2">
                
                <img class="h-64 p-2" src="https://cdn.pixabay.com/photo/2017/08/05/02/39/volleyball-2582096_1280.jpg" alt="voleibol, ball">
                
                
                <div class="px-2 py-4 text-center">
                    <div class="font-bold text-xl mb-2">Estadisticas</div>
                    <p class="text-black text-base">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, Nonea! Maiores et perferendis eaque, exercitationem praesentium nihil.
                    </p>
                </div>

                <div class="flex md:col-span-2 px-2 pt-4 pb-3 justify-center" role="group">
                    <button type="button" class="px-2 lg:px-4 py-2 text-xs lg:text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-l-lg hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-2 focus:ring-blue-700 focus:text-blue-700 dark:bg-gray-700 dark:border-gray-600 dark:text-white dark:hover:text-white dark:hover:bg-gray-600 dark:focus:ring-blue-500 dark:focus:text-white">
                        Profile
                    </button>
                    <button type="button" class="px-2 lg:px-4 py-2 text-xs lg:text-sm font-medium text-gray-900 bg-white border-t border-b border-gray-200 hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-2 focus:ring-blue-700 focus:text-blue-700 dark:bg-gray-700 dark:border-gray-600 dark:text-white dark:hover:text-white dark:hover:bg-gray-600 dark:focus:ring-blue-500 dark:focus:text-white">
                        Settings
                    </button>
                    <button type="button" class="px-2 lg:px-4 py-2 text-xs lg:text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-r-md hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-2 focus:ring-blue-700 focus:text-blue-700 dark:bg-gray-700 dark:border-gray-600 dark:text-white dark:hover:text-white dark:hover:bg-gray-600 dark:focus:ring-blue-500 dark:focus:text-white">
                        Messages
                    </button>
                </div>
            </div>
        </div>

        <!--Card 2-->
        <div class="rounded-md overflow-hidden shadow-lg">
            <img class="w-full" src="https://cdn.pixabay.com/photo/2020/05/04/15/34/text-5129634_1280.jpg" alt="Marcador Electrónico">
            <div class="px-6 py-4">
                <div class="font-bold text-xl mb-2">River</div>
                <p class="text-gray-700 text-base">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, Nonea! Maiores et perferendis eaque, exercitationem praesentium nihil.
                </p>
            </div>
            <div class="px-6 pt-4 pb-1">
                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-1">#photography</span>
                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-1">#travel</span>
                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-1">#summer</span>
            </div>
        </div>

        <!--Card 3-->
        <div class="p-2 md:col-span-2 lg:col-span-3 rounded-md bg-gray-300 overflow-hidden shadow-lg">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 md:grid-rows-3 gap-2">
                <div class="grid justify-items-center  content-center row-span-2">
                    <div class="font-bold text-xl uppercase">Control de Sets</div>
                    <IndicadorSets 
                        :controlSets = "controlSets"
                        :sets = "sets"
                    />
                       
                </div>
                <div  class="grid justify-items-center md:col-span-2 lg:col-span-1 lg:row-span-2">
                    <Marcador :marcador = "marcadorCasa" />
                </div>
                <div  class="grid justify-items-center md:col-span-2 lg:col-span-1 lg:row-span-2">
                    <Marcador :marcador = "marcadorVisita" />
                </div>
                <div class="grid justify-items-center content-center md:col-span-3 " id="div1">
                    <TablaCss /> 
                </div>
            </div>
        </div>

    </div> 
    
</template>

<style scoped>

#div1 {
    height:120px;
    margin-bottom: 0; 
    overflow-x: auto; 
    overflow-y: hidden; 
    white-space: nowrap;
    padding: 1px;
    scrollbar-width: thin;   
}

*::-webkit-scrollbar {
  height: .75em;
}
*::-webkit-scrollbar-track {
  background: hsl(180 100% 30% / 1);
  border-radius: 100vw;
  margin-inline: .25em;
}

*::-webkit-scrollbar-thumb {
  background: hsl(180 100% 20% / 1);
  border: 3px solid hsl(180 100% 30% / 1);
  border-radius: 100vw;
  
}
*::-webkit-scrollbar-thumb:hover {
  background: hsl(180 100% 10% / 1);
}

</style>
