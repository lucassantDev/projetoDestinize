
<template>
  <header class="border-b border-gray-200 h-22 flex items-center justify-between">
        <img src="../img/logomarca (1).png" alt="logo do cabeçalho" 
        class="ml-14 w-28 md:w-44">
        
        <div class="flex items-center justify-evenly gap-4 mr-14">
          <div class=" p-2 rounded-full bg-gray-100 ">
            <User :size="18"
            class="text-blue-400"
            />
          </div>

          <p class="hidden md:font-semibold md:text-sm md:flex ">
            Minha conta
          </p>
        </div>
  </header>
</template>

<script setup>
import { User } from '@lucide/vue';
</script>
