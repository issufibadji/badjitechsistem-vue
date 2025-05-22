<template>
  <section id="home" class="bg-blue-50 py-16">
    <div class="wrapper flex flex-col lg:flex-row items-center gap-10 px-4 max-w-7xl mx-auto">
      <div class="flex-1 space-y-6">
        <h5 class="text-sm text-blue-600 uppercase font-bold">
          <img src="/src/assets/images/logo-azul-sem-fundo.png" alt="Badji Tech System" class="h-48 mx-auto lg:mx-0" />
        </h5>
        <h1 class="text-4xl font-bold text-gray-800">SOLUÇÕES COMPLETAS EM SOFTWARE</h1>
        <p class="text-gray-600">
          Na Badji Tech System, desenvolvemos, construímos e mantemos sistemas sob medida para sua empresa, garantindo performance, segurança e escalabilidade – sempre dentro do seu orçamento.
        </p>
        <a
          href="#contact"
          class="inline-flex items-center gap-2 bg-blue-600 text-white px-6 py-3 rounded-full font-bold hover:bg-blue-700 transition-all"
        >
          <i class="fa-brands fa-whatsapp text-xl"></i>
          <span>INICIE SEU PROJETO</span>
        </a>
      </div>
      <div class="flex-1 flex justify-center items-end">
        <img src="/src/assets/images/develop.gif" alt="Desenvolvimento de software em ação" class="max-w-md rounded-3xl p-4" />
      </div>
    </div>

    <div
      class="mt-12 bg-blue-100 border border-blue-400 rounded-xl max-w-5xl mx-auto flex flex-col md:flex-row items-center justify-center text-center gap-8 px-6 py-10 shadow-lg"
    >
      <div>
        <h2 class="text-3xl font-bold text-gray-800">+10</h2>
        <p class="text-blue-700">Clientes satisfeitos</p>
      </div>
      <div class="hidden md:block w-px h-10 bg-blue-500"></div>
      <div>
        <h2 class="text-3xl font-bold text-gray-800">+5</h2>
        <p class="text-blue-700">Especialistas dedicados</p>
      </div>
      <div class="hidden md:block w-px h-10 bg-blue-500"></div>
      <div>
        <h2 class="text-3xl font-bold text-gray-800">+7</h2>
        <p class="text-blue-700">Anos de experiência</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import 'scrollreveal'
import { onMounted } from 'vue'

onMounted(() => {
  const sr = ScrollReveal({
    origin: 'top',
    distance: '50px',
    duration: 800,
    reset: false,
  })

  sr.reveal('h5', { delay: 100 })
  sr.reveal('h1', { delay: 300 })
  sr.reveal('p', { delay: 600 })
  sr.reveal('a', { delay: 900 })
  sr.reveal('img', { delay: 1200 })
})
</script>

<style scoped>
.wrapper {
  padding-left: 2rem;
  padding-right: 2rem;
}
</style>
