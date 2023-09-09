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
            class="border-b-2 border-[#0000002d] p-1 text-neutral-600 uppercase font-bold">
            {{ marcador.nombre }}:
        </div>
        <div class="p-1 text-center">
            <h5 class="border-b-2 border-[#0000002d] p-1 text-3xl font-bold font-mono">
                <span>{{ marcador.cantidadPtos }}</span>
            </h5>
        </div>
        <div class="flex justify-center">
            <table>
            <thead>
                <tr class="solid">
                    <th scope="col">T.O</th>
                    <th scope="col">CHG</th>
                    <th scope="col">SQ</th>
                    <th scope="col">RT</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>{{ marcador.timeOuts }}</td>
                    <td>{{ marcador.cambios }}</td>
                    <td><p :class="marcador.saque">{{ marcador.saque }}</p></td>
                    <td>{{ marcador.rotacion }}</td>
                </tr>
            </tbody>
        </table>
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
.Si{
    background-color: #86e49d;
    color: #006b21;
    font-weight: bold;
}
.No{
    background-color: #d893a3;
    color: #b30021;
}
p{
    padding: 3px 5px;
    border-radius: 10px;
}

table {
    font-size: small;
    table-layout: fixed;
    border-collapse: collapse;
    
}
table thead tr{
    background-color: #303030;
    color: white;
    
}
table tr{
    border: 1px #909090 solid;
}
table td,th{
    padding: 1px 6px 1px 6px;
    text-align: center;
    font-weight: normal;
    border: 1px #909090 dotted;
}

</style>