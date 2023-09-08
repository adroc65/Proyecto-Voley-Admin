<script setup>

</script>

<template>
    <div class="p-2">
        <h2 class="font-black text-2xl text-center">Marcador</h2>
        <div class="flex flex-col">
            <div class="overflow-x-auto sm:-mx-6 lg:-mx-8">
                <div class="inline-block min-w-full py-2 sm:px-6 lg:px-8">
                    <div class="overflow-hidden">
                        <table class="min-w-full text-center text-xs font-light">
                            <thead
                                class="border-b bg-neutral-800 font-medium text-white dark:border-neutral-500 dark:bg-neutral-900">
                                <tr>
                                    <th scope="col" class=" px-4 py-3">#</th>
                                    <th scope="col" class=" px-4 py-3">Local</th>
                                    <th scope="col" class=" px-4 py-3">Visita</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr class="border-b dark:border-neutral-500">
                                    <td class="whitespace-nowrap  px-2 py-2 font-medium">Actual</td>
                                    <td class="whitespace-nowrap  px-2 py-2 font-bold text-2xl bg-green-300">13</td>
                                    <td class="whitespace-nowrap  px-2 py-2 font-bold text-2xl">12</td>
                                </tr>
                                <tr class="border-b dark:border-neutral-500">
                                    <td class="whitespace-nowrap  px-2 py-1 font-medium">Set #1</td>
                                    <td class="whitespace-nowrap  px-2 py-1 ">25</td>
                                    <td class="whitespace-nowrap  px-2 py-1">19</td>
                                </tr>
                                <tr class="border-b dark:border-neutral-500">
                                    <td class="whitespace-nowrap  px-2 py-1 font-medium">Set #2</td>
                                    <td class="whitespace-nowrap  px-2 py-1 ">23</td>
                                    <td class="whitespace-nowrap  px-2 py-1">25</td>
                                </tr>
                                <tr class="border-b dark:border-neutral-500">
                                    <td class="whitespace-nowrap  px-2 py-1 font-medium">Set #3</td>
                                    <td class="whitespace-nowrap  px-2 py-1 ">55</td>
                                    <td class="whitespace-nowrap  px-2 py-1">15</td>
                                </tr>
                                <tr class="border-b dark:border-neutral-500">
                                    <td class="whitespace-nowrap  px-2 py-1 font-medium">Set #4</td>
                                    <td class="whitespace-nowrap  px-2 py-1 ">20</td>
                                    <td class="whitespace-nowrap  px-2 py-1">25</td>
                                </tr>
                                <tr class="border-b dark:border-neutral-500">
                                    <td class="whitespace-nowrap  px-2 py-1 font-bold text-blue-600">Set #5</td>
                                    <td colspan="2" class="whitespace-nowrap  px-2 py-1 font-bold text-base text-red-600">
                                        En progreso ...
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>