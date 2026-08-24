<template>
    <section class="w-full h-fit py-12 flex flex-col items-center justify-center">
        <div class="w-full">
            <h3 class="font-semibold text-blue-500 text-center
            lg:text-left lg:ml-16 lg:text-2xl 
            ">
                CONHECER O DESTINO
            </h3>
            <h1 class="font-bold text-blue-950 text-3xl text-center mt-2
            lg:text-left lg:ml-16 lg:text-5xl lg:mt-6 
            ">Galeria de Turismo e Blog de Viagens</h1>
        </div>

        <div class="gap-4 w-full flex flex-wrap items-center justify-center h-fit py-6 lg:">

            <div class="flex flex-col shadow-xl rounded-xl w-2/3 pb-4 lg:w-96">
                <img src="../img/destino4.png" class="object-cover w-full h-64 rounded-t-xl lg:h-72 "/>
                <div class="flex flex-col gap-2 ml-2 mt-2">
                    <p class="text-gray-400 font-semibold">26 | DEZEMBRO 2021</p>
                    <p class="text-blue-950 font-semibold">Dicas para escalar o Monte Bromo<br> sem se cansar</p>
                    <p class="text-gray-400">Então, você conhece o Monte Bromo?<br>Sim, uma montanha né!</p>
                    <p class="text-blue-500 font-semibold">Leia mais...</p>
                </div>
            </div>

            <img src="../img/video.png" class="w-2/3 rounded-xl shadow-sm lg:w-1/2 lg:ml-16"/>

            <div class="relative flex bg-black/30 flex-col items-center justify-center w-2/3 h-80 rounded-md bg-cover bg-center bg-no-repeat lg:w-3/4 lg: items-start"
            :style="{ backgroundImage: `url(${Begijnhof})`}">

            <div class="absolute inset-0 rounded-md bg-black/45"></div>

                <h2 class="text-2xl text-gray-200 font-bold ml-2 z-10">Dicas para consumo de água nos locais mais remotos</h2>
                <p class="ml-2 text-gray-200 z-10">
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                </p>
            </div>
        </div>

    </section>
</template>

<script setup>

import Begijnhof from '../img/destino5.png'
</script>