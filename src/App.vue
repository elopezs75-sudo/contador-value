<script setup lang="ts">
import { ref } from 'vue'

const contador = ref<number>(0)

function incrementar(): void {
  contador.value++
}

function decrementar(): void {
  contador.value--
}
</script>

<template>
  <div class="min-h-screen flex items-center justify-center bg-gradient-to-br from-purple-500 via-pink-500 to-orange-400">
    <div class="bg-white/90 backdrop-blur rounded-3xl shadow-2xl p-10 flex flex-col items-center gap-6">
      <h1 class="text-2xl font-bold text-gray-700">Contador Vue + TS</h1>

      <p class="text-7xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-purple-600 to-pink-600 transition-all duration-300">
        {{ contador }}
      </p>

      <div class="flex gap-4">
        <button
          @click="decrementar"
          class="px-6 py-3 rounded-full bg-red-500 hover:bg-red-600 active:scale-95 text-white text-2xl font-bold shadow-lg transition-transform"
        >
          −
        </button>
        <button
          @click="incrementar"
          class="px-6 py-3 rounded-full bg-green-500 hover:bg-green-600 active:scale-95 text-white text-2xl font-bold shadow-lg transition-transform"
        >
          +
        </button>
      </div>
    </div>
  </div>
</template>