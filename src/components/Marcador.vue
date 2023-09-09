<script setup>
    const props = defineProps({
        marcador: {
            type: Object,
            required: true
        },
    })

    const headers = ['T.O','CHG','SAQ','ROT']

</script>

<template>
    <div
        :class="marcador.color"
        class="grid w-full rounded-lg border border-neutral-700 shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)]">
        <h3 class="border-b-2 border-[#0000002d] pl-1 text-neutral-600 uppercase font-bold">
            Marcador {{ marcador.nombre }}:
        </h3>
        
        <h5 class="py-3 border-b-2 border-[#0000002d] text-center text-5xl font-bold font-mono">
            {{ marcador.cantidadPtos }}
        </h5>
        
        <div class="grid content-end p-2">
            <table>
                <thead>
                    <tr>
                        <th scope="col">Item</th>
                        <th scope="col">Valor</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <th scope="row">{{ headers[0] }}</th>
                        <td>{{ marcador.timeOuts }}</td>
                    </tr>
                    <tr>
                        <th scope="row">{{ headers[1] }}</th>
                        <td>{{ marcador.cambios }}</td>
                    </tr>
                    <tr>
                        <th scope="row">{{ headers[2] }}</th>
                        <td><p :class="marcador.saque">{{ marcador.saque }}</p></td>
                    </tr>
                    <tr>
                        <th scope="row">{{ headers[3] }}</th>
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
    padding: 2px 2px;
    border-radius: 15px;
}

table {
    font-size: medium;
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
tbody tr th{
    font-weight: bold;
}
table td,th{
    padding: 1px 6px 1px 6px;
    text-align: center;
    border: 1px #909090 solid;
}

</style>