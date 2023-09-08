<script setup>
    const props = defineProps({
        marcador: {
            type: Object,
            required: true
        },
    })
</script>

<template>
    <div
        :class="marcador.color"
        class="block w-40 max-w-[12rem] rounded-lg border border-neutral-700 shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-600">
        <div
            class="border-b-2 border-[#0000002d] p-2 text-neutral-600 uppercase font-bold">
            {{ marcador.nombre }}
        </div>
        <div class="p-3 text-center">
            <h5 class="text-3xl font-bold font-mono">
                <span>{{ marcador.cantidadPtos }}</span>
            </h5>
            
        </div>
    </div>
</template>



<style scoped>
.primary{
    background-color: cyan;
}
.secondary{
    background-color: white;
}
</style>