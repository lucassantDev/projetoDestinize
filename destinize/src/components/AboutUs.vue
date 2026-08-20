<template>
     <section class="border w-full h-fit py-6  flex flex-col items-center justify-evenly lg:h-screen">
            <div class="w-full h-fit flex flex-col items-center justify-center">
                <h3 class="font-semibold text-blue-500 text-center
                    lg:text-left lg:text-2xl">DEPOIMENTO DE TESTEMUNHAS
                </h3>
                <h1 class="font-bold text-blue-950 text-4xl w-64 text-center mt-2
                lg:text-center lg:text-6xl lg:mt-4 lg:w-full">O que dizem sobre nós?
                </h1>
                <p class="text-center py-4 text-gray-600 w-88 lg:w-fit lg:text-xl">
                    Ficou curioso para saber as  avaliações  dos usuários que utilizam o aplicativo e site Destinize <br>
                    para decidir para onde ir nas próximas férias? Venha conferir abaixo!
                </p>
            </div>

            <div class="gap-6 w-full flex flex-col items-center justify-evenly lg:flex-row">
                <div
                    v-for="feedback in feedbacks"
                    :key="feedback.id"
                    class="w-64 h-44 shadow-md py-4 flex flex-col items-center justify-evenly mt-2
                    lg:w-84 h-84 lg:mt-4 lg:shadow-xl"
                >
                    <img
                    :src="feedback.img"
                    class="w-24 h-24 object-cover mb-2
                    lg:w-28 lg:h-28
                    "
                    />
                
                    <div class=" flex flex-col lg:w-4/5">
                        <p class="text-slate-400 text-sm text-center lg:font-bold">{{ feedback.feedback }}</p>
                        <div class="flex gap-2 items-center justify-center my-2">
                            <Star  :size="20"
                            class="text-yellow-400 font-normal"/>
                            <Star  :size="20"
                            class="text-yellow-400 font-normal"/>
                            <Star  :size="20"
                            class="text-yellow-400 font-normal"/>
                            <Star  :size="20"
                            class="text-yellow-400 font-normal"/>
                            <Star  :size="20"
                            class="text-gray-400 font-normal"/>
                        </div>
                        <p class="text-blue-500 text-center lg:font-semibold">{{ feedback.user }}</p>
                    </div>
                </div>
            </div>

            <!-- <div class="espaco-depoimentos">

                <div class="depoimento">
                    <img src="img/avatar1.png" alt="primeiro cliente" style="scale: 0.8;">
                    <p class="feedback-cliente">
                        Destinize me ajudou em busca de novos pontos turísticos na br Indonésia facilmente!
                    </p>
                    <p class="avaliacao-cliente">
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <span><i class="fa-solid fa-star" alt="estrelas de avaliação"></i></span>

                    </p>
                    <p class="nome-cliente">
                        Sandro Sardinha
                    </p>
                </div>

                <div class="depoimento">
                    <img src="img/avatar2.png" alt="segundo cliente" style="scale: 0.8;">
                    <p class="feedback-cliente">
                        Destinize me ajudou e encontrar uma alma gêmea! Juntos, viajamos para diversos lugares do mundo.
                    </p>
                    <p class="avaliacao-cliente">
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <span><i class="fa-solid fa-star" alt="estrelas de avaliação"></i></span>

                    </p>
                    <p class="nome-cliente">
                        Roberto Rubéns
                    </p>
                </div>

                <div class="depoimento">
                    <img src="img/avatar3.png" alt="terceiro cliente" style="scale: 0.8;">
                    <p class="feedback-cliente">
                       Minha primeira viagem eu fiz atraves da Destinize. Todo o processo foi muito tranquilo!
                    </p>
                    <p class="avaliacao-cliente">
                       <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <i class="fa-solid fa-star" alt="estrelas de avaliação"></i>
                        <span><i class="fa-solid fa-star" alt="estrelas de avaliação"></i></span>
                    </p>
                    <p class="nome-cliente">
                        Patrick Sesat
                    </p>
                </div>

            </div> -->
        </section>
</template>

<script setup>
import { ref } from 'vue';
import { Star } from "@lucide/vue";

const feedbacks = ref([
    {
        id: 1,
        img: "../src/img/avatar1.png",
        feedback: 'Destinize me ajudou em busca de novos pontos turísticos na  Indonésia facilmente!',
        user: "Sandro Sardinha"
    },
    {
        id: 2,
        img: "../src/img/avatar2.png",
        titulo: 'Favoritos perto de você!',
        feedback: 'Destinize me ajudou a encontrar uma alma gêmea! Juntos, viajamos para diversos lugares do mundo.',
        user: "Roberto Rubéns"
    },
    {
        id: 3,
        img: "../src/img/avatar3.png",
        feedback: 'Minha primeira viagem eu fiz atraves da Destinize. Todo o processo foi muito tranquilo!',
        user: "Patrick"
    }
]);
</script>