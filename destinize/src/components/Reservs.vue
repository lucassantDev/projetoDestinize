<template>
    <section class="
    w-full h-fit py-6  flex flex-col items-center justify-center
    lg:h-screen lg:flex-row 
    ">
        <div class="lg:w-1/2">
            <h3 class="font-semibold text-blue-500 text-center
            lg:text-left lg:text-2xl">
                RESERVAS
            </h3>
            <h1 
            class="font-bold text-blue-950 text-3xl text-center mt-2
            lg:text-left lg:text-5xl lg:mt-4">
                Não quer fazer fila?<br>Basta fazer uma reserva!
             </h1>

            <div
                v-for="card in cards"
                :key="card.id"
                class="w-full py-4 flex items-center justify-evenly mt-2
                lg:justify-start lg:mt-4"
            >

                <div class="w-12 h-12 bg-yellow-400 rounded-xl shadow-md lg:w-14 lg:h-14"></div>
                <div class="flex flex-col w-3/4 lg:ml-12 lg:w-92">
                    <h2 class="font-semibold text-blue-950">{{ card.titulo }}</h2>
                    <p class="text-gray-600">{{ card.descricao }}</p>
                </div>

            </div>
        </div>

        <img 
        src="../img/reserva.png"
        class=" w-84 
        lg:w-3xl"
        />
    </section>
</template>

<script setup>
import { ref } from 'vue';
import { Search, Pencil, Heart } from '@lucide/vue';

const cards = ref([
    {
        id: 1,
        icone: Search,
        titulo: 'Encontre o lugar que você deseja',
        descricao: 'Encontre o próximo destino que você visitará com Destinize!'
    },
    {
        id: 2,
        icone: Pencil,
        titulo: 'Preencha os dados e confirme o pagamento.',
        descricao: 'Escreva e complete os seus dados para efeitos de dados de reserva.'
    },
    {
        id: 3,
        icone: Heart,
        titulo: 'Basta entrar e aproveitar!',
        descricao: 'Você pode entrar direto e aproveitar suas férias sem obstáculos.'
    }
]);
</script>