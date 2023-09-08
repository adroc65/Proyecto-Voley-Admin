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
import MarcadorCasa from './MarcadorCasa.vue'

const marcadorCasa = reactive({
    nombre: 'Casa',
    color: 'primary',
    cantidadPtos: '17',
})
const marcadorVisita = reactive({
    nombre: 'Visita',
    color: 'secondary',
    cantidadPtos: '9',
})

</script>

<template>

    <div class="p-10 grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 lg:grid-cols-3 xl:grid-cols-3 gap-5">
        <!--Card 1-->
        <div class="md:col-span-3 rounded-md bg-gray-400 overflow-hidden shadow-lg">
            <div class="grid grid-cols-1 md:grid-cols-2 items-center gap-2">
                
                <img class="h-64 p-2" src="https://cdn.pixabay.com/photo/2017/08/05/02/39/volleyball-2582096_1280.jpg" alt="voleibol, ball">
                
                
                <div class="px-6 py-4 text-center">
                    <div class="font-bold text-xl mb-2">Estadisticas</div>
                    <p class="text-black text-base">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, Nonea! Maiores et perferendis eaque, exercitationem praesentium nihil.
                    </p>
                </div>

                <div class="flex md:col-span-2 px-6 pt-4 pb-3 justify-center" role="group">
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
            <div class="px-6 pt-4 pb-2">
                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#photography</span>
                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#travel</span>
                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#summer</span>
            </div>
        </div>

        <!--Card 3-->
        <div class="p-5 md:col-span-2 rounded-md overflow-hidden shadow-lg">
            <div class="mb-5 grid grid-cols-1 md:grid-cols-2 grid-rows-2 gap-2 justify-items-center">
                <div class="row-span-2">
                    <div class="font-bold text-xl">Control de Sets</div>
                    <div class="">
                        <IndicadorSets />
                    </div>    
                </div>
                <div class="">
                    <div class="font-bold text-xl">MARCADOR</div>
                    <MarcadorCasa 
                        :marcador = "marcadorCasa"
                    />
                </div>
                <div class="grid content-center">
                    <MarcadorCasa 
                        :marcador = "marcadorVisita"
                    />
                </div>
            </div>
            <div class="flex md:col-span-2 justify-center">
                <TablaCss /> 
            </div>
                     
        </div>
    </div> 
    
</template>