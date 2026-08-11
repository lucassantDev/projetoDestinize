<template>
    <section class="w-full h-fit py-6
    lg:h-screen flex flex-col items-center justify-center
    ">
            
           <div class="w-full">
            <h3 class="font-semibold text-blue-500 text-center
            lg:text-left lg:ml-16 lg:text-4xl 
            ">
                Destinos favoritos
            </h3>
            <h1 class="font-bold text-blue-950 text-3xl text-center mt-2
            lg:text-left lg:ml-16 lg:text-5xl lg:mt-6 
            "><span>✈️</span> Venha escolher o destino da sua próxima viagem</h1>
           </div>

           <div class="
            h-fit flex flex-col items-center gap-4 py-6
            lg:flex-row lg:w-full lg:justify-evenly lg:h-1/2
           ">

                <div 
                v-for="lugar in lugares"
                :key="lugar.id"
                class="rounded-xl w-68 overflow-hidden shadow-lg
                lg:scale-125
                "
                >

                <img
                :src="lugar.img"
                :alt="lugar.destino"
                class="w-68 h-48 object-cover
                "
                />
                <div class="p-3 bg-white/50">
                    <h2 class="text-lg font-semibold">{{ lugar.destino }}</h2>
                    <p class="text-sm text-gray-500">{{ lugar.pais }}</p>
                </div>

                </div>

                

            </div>
        </section>
</template>

<script setup>
    import {ref, computed} from 'vue';

    const lugares = ref([
        {id: 1, img: './src/img/destino1.png', destino: 'Fernando de Noronha', pais: 'Brasil' },
        {id: 2, img: './src/img/destino2.png', destino: 'Montanhas Atlas', pais: 'Marrocos' },
        {id: 3, img: './src/img/destino4.png', destino: 'Valparaíso', pais: 'Chile' },
        {id: 4, img: './src/img/destino5.png', destino: 'Begijnhof', pais: 'Holanda' }
    ])

</script>