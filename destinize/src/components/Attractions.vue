<template>
    <section class="
    border w-full h-fit py-6  flex flex-col items-center justify-center
    ">

    <div class="w-full h-fit flex flex-col items-center justify-center ">
            <h3 class="font-semibold text-blue-500 text-center
            lg:text-left lg:text-2xl">
                BUSCA POR ATRAÇÕES TURÍSTICAS
            </h3>
            <h1 class="font-bold text-blue-950 text-4xl text-center mt-2
            lg:text-center lg:text-6xl lg:mt-4">
                Procure atrações turísticas perto de você
            </h1>
            <p class="text-center py-4 w-86 lg:w-fit lg:text-xl">
                Este recurso permite que você pesquise atrações turísticas ou locais atualmente populares em sua <br> região, para que você esteja sempre atualizado e não se confunda novamente.
            </p>
    </div>

    <img 
    src="../img/mapa.png"
    class=" w-72 h-72 object-cover rounded-md shadow-md mt-6
    lg:w-4/5 lg:h-4/5"
    />

    <div class="py-12 flex-col flex  lg:flex-row">
        <div
        v-for="description in descriptions"
        :key="description.id"
        class="w-full py-4 flex justify-evenly mt-2
        lg:justify-center lg:mt-4 ">

        <div class="w-14 h-14 bg-gray-200 rounded-full shadow-sm flex items-center"></div>

        <div class="border w-4/5 ml-2">
            <h4 class="font-bold text-md text-blue-950">{{ description.titulo }}</h4>
            <p class="text-gray-600">{{ description.descricao }}</p>
        </div>

        </div>
    </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';

const descriptions = ref([
    {
        id: 1,
        titulo: 'Popular perto de você',
        descricao: 'Um ponto turístico popular e definitivamente conhecido por todos perto de você.'
    },
    {
        id: 2,
        titulo: 'Favoritos perto de você!',
        descricao: 'Lugar favorito e apreciado por todos na sua região.'
    },
    {
        id: 3,
        titulo: 'Há muitas pessoas perto de você',
        descricao: 'O local mais visitado por moradores e turistas!'
    }
]);
</script>