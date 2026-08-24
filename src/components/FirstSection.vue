<template>

    <section class="w-full h-fit py-10 flex flex-col-reverse items-center justify-center md:justify-evenly md:flex-row">

        <div class="w-fit flex flex-col items-center gap-8 md:items-left">
            <h1 class="
            text-4xl text-center font-bold text-blue-950
            md:text-8xl md:text-left md:ml-12">
               Viaje pelo mundo, <br><span class="text-blue-600">aproveite</span> os melhores destinos!
            </h1>
            <p class="text-gray-400 text-center md:ml-12 md:text-left">
                Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda architecto vitae porro dignissimos in inventore, 
                atque ut et enim nulla qui iste dolorem, quidem eveniet quasi suscipit beatae, quod id!
            </p>
            <div class='flex flex-col gap-2 items-center md:w-full md:flex-row md:gap-4'>
                <button class=
                "bg-blue-500 p-4 w-44 rounded-md font-semibold text-gray-50 cursor-pointer transition duration-200 hover:bg-blue-600
                hover:shadow-xl
                md:ml-12
                "
                >
                    Cadastre-se
                </button>
                <div class="flex w-full items-center justify-evenly gap-2 md:w-fit ">
                    <button class=
                    '
                    border border-blue-600 shadow-xl w-14 h-14 group rounded-full cursor-pointer flex items-center justify-center
                    '>
                        <Play :size="20"
                        class="text-gray-400 transition duration-200 group-hover:text-blue-500"
                        />
                    </button>
                    <p class="font-semibold text-blue-400">Veja como funciona</p>
                </div>
            </div>
        </div>

        <img src='../img/viajante.png' 
        class="
        w-80 
        md:w-1/2 md:mr-12"
        />

    </section>

    
</template>

<script setup>
import { Play } from '@lucide/vue'

</script>