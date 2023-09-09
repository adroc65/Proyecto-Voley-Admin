<script setup>
 const props = defineProps({
        controlSets: {
            type: Object,
            required: true
        },
        sets: {
            type: Array,
            required: true
        }
    })
</script>

<template>
    <div
        class="grid w-full rounded-lg border border-neutral-700 bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)]">
        <div
            class="border-b-2 border-[#0000002d] px-6 py-3 text-black">
            Sets a Jugar: <span>{{ controlSets.total }}</span>
        </div>
        <div class="p-2">
            <h5 class="text-center">Jugando Set #{{ controlSets.jugando }}</h5>
            <div v-for="set in sets">
                <p :class="set.estado">{{ set.name }}: 
                    <span>{{ set.estado ==='completado'? set.mCasa +" - "+set.mVisita : set.estado }}</span>
                </p>
            </div>
        </div>
    </div>
</template>

<style scoped>

span{
    font-weight: bold;
    font-size: normal;
}
h5{
    margin-bottom: 2px;
    font-weight: bold;
    font-size: larger;
    text-decoration: underline black;
    
}
p{
    padding: .2rem .2rem;
    margin-bottom: .2rem;
    border-radius: 1rem;
    text-align: center;
}
span{
    text-transform: capitalize;
}
.completado{
    background-color: #86e49d;
}
.jugando{
    background-color: #d893a3;
}
.pendiente{
    background-color: #ebc474;
}

</style>