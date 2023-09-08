<script setup>
import { ref, onMounted } from "vue"
import BtnAccion from './BtnAccion.vue'
import { db } from '../data/botones'


const color = ref("pink")
const name = ref("Botón 01")
const botones = ref([])

onMounted(() => {
    botones.value = db
    console.log(typeof(botones.value[6].color))
    console.log(botones.value[6].color)
})


</script>

<template>
    <div class="p-2">
        <h2 class="font-black text-2xl text-center">Control</h2>
        <div class="mt-2 grid items-end  md:grid-cols-1">
            <div>
                <div class="relative">
                    <input 
                        type="text" 
                        id="filled_success" 
                        aria-describedby="filled_success_help" 
                        class="block rounded-t-lg px-2.5 pb-2.5 pt-5 w-full text-sm text-gray-900 bg-gray-50 dark:bg-gray-700 border-0 border-b-2 border-green-600 dark:border-green-500 appearance-none dark:text-white dark:focus:border-green-500 focus:outline-none focus:ring-0 focus:border-green-600 peer" 
                        placeholder=" " />
                    <label 
                        for="filled_success" 
                        class="absolute text-sm text-green-600 dark:text-green-500 duration-300 transform -translate-y-4 scale-75 top-4 z-10 origin-[0] left-2.5 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-4"
                        >Iniciar Jugada
                    </label>
                </div>
                <p 
                    id="filled_success_help" 
                    class="mt-2 text-xs text-green-600 dark:text-green-400">
                    <span class="font-medium">Se muestra la jugada actual. </span>
                </p>
            </div>
        </div>
        <div class="mt-5 grid grid-rows-5 grid-flow-col gap-2" >
            <BtnAccion
                v-for="boton in botones" 
                :key="boton.id"
                :boton="boton"
            />
        </div>
        
    </div>
</template>