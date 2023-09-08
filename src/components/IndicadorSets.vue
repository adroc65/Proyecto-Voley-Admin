<template>
    <div
        class="block w-48 max-w-[18rem] rounded-lg border border-neutral-700 bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)]">
        <div
            class="border-b-2 border-[#0000002d] px-6 py-3 text-black">
            Sets a Jugar: <span>5</span>
        </div>
        <div class="p-2">
            <h5>Jugando Set #3</h5>
            <div class="p-2">
                <p class="jugado">Set #1: <span>25-18</span></p>
                <p class="jugado">Set #2: <span>15-25</span></p>
                <p class="jugando">Set #3: <span>Jugando</span></p>
                <p class="pendiente">Set #4: <span>Pendiente</span></p>
                <p class="pendiente">Set #5: <span>Pendiente</span></p>
            </div>
            
            
        </div>
    </div>
</template>

<script setup>

</script>

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
.jugado{
    color: blue;
}
.jugando{
    color: red;
}
.pendiente{
    color: gray;
}

</style>