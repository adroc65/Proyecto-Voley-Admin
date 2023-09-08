<script setup>

const props = defineProps({
    boton: {
        type: Object,
        required: true
    }
})

</script>

<template>    
    <!-- <button 
        type="button"
        :class="`bg-${boton.color}-500 hover:bg-${boton.color}-600 focus:ring-${boton.color}-500`"
        class="py-3 px-4 inline-flex justify-center items-center gap-2 font-semibold text-white rounded-md border border-transparentfocus:outline-none focus:ring-2 focus:ring-offset-2 transition-all text-sm dark:focus:ring-offset-gray-800"              
        > {{ boton.nombre }}
    </button>     -->

    <button
        :class="boton.color"
        class="text-white font-bold py-2 px-4 rounded-lg border border-transparentfocus:outline-none focus:ring-2 focus:ring-offset-2 transition-all text-sm dark:focus:ring-offset-gray-800"
        >{{ boton.nombre }} - {{ boton.color }}
    </button>

</template>

<style scoped>
.blue{
    background-color: #0091EA;
}
.blue:hover{
    background-color: #0277BD;
}
.gray{
    background-color: #607D8B;
}
.gray:hover{
    background-color: #616161;
}
.indigo{
    background-color: #303F9F;
}
.indigo:hover{
    background-color: #1A237E;
}
.green{
    background-color: #388E3C;
}
.green:hover{
    background-color: #1B5E20;
}

</style>