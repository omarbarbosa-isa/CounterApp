<template>
  <q-page class="flex flex-center">
    <!-- Cabeçalho com o número e o texto "Contados" -->
    <div class="absolute-top bg-primary text-white text-center q-pa-lg">
      <div class="text-h2 text-weight-bold">{{ contador }}</div>
      <div class="text-subtitle1">Contados</div>
    </div>

    <!-- Botões de Decrementar (-) e Incrementar (+) -->
    <div class="row q-gutter-md absolute-center items-center">
      <q-btn color="red" icon="remove" @click="decrementar" />
      <div class="text-grey-7 text-weight-bold">·</div>
      <q-btn color="green" icon="add" @click="incrementar" />
    </div>

    <!-- Botão de RESET no fundo -->
    <div class="row q-mb-xl absolute-bottom justify-center">
      <q-btn round color="blue" icon="refresh" size="25px" @click="reset" />
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const contador = ref(0)

function incrementar() {
  contador.value++
}

function decrementar() {
  contador.value--
}

// Função de Reset
function reset() {
  contador.value = 0
}
</script>
