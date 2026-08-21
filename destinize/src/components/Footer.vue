<template>
    <footer class="w-full flex flex-col items-center justify-evenly 
    h-screen py-12 lg:h-screen lg:items-start">
        <div class="flex sm:flex-col sm:items-center lg:items-start">
            <img
            src="../img/logomarca2.png"
            class="w-24 mb-2 mr-24 lg:ml-6"
            />
            <p class="text-gray-400 w-1/2  lg:ml-6">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Doloribus veritatis totam libero provident placeat distinctio explicabo dignissimos quis, voluptas dolorem, veniam cum nihil tempore aspernatur sit reiciendis repellendus aperiam eveniet.
            </p>
            <div class="w-1/2 py-4 lg:ml-6">
                <div
                v-for="information in informations"
                :key="information.id"
                class="flex items-center"
                >
                    <component :is="information.icone" size="12" class="w-4 h-4 text-gray-400"/>
                    <p class="text-gray-400 ml-2">
                        {{ information.texto }}
                    </p>
                </div>
            </div>
        </div>

        <p class="text-gray-400 flex items-center justify-center text-center w-full h-44">
            © 2021-2024, todos os direitos <br> são reservados
        </p>

    </footer>
</template>

<script setup>
import { ref } from "vue"
import {Phone, MapPin, Mail} from "@lucide/vue"

const informations = ref([
    {
        id: 1,
        icone: Phone,
        texto: '(81)3616-2840'
    },
    {
        id: 2,
        icone: Mail,
        texto: 'contato@destinize.com'
    },
    {
        id: 3,
        icone: MapPin,
        texto: 'Ibura, Recfie/PE'
    }
]);

</script>