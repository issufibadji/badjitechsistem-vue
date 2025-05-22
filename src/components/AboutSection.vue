<template>
  <section id="about" class="py-20 bg-blue-50">
    <div class="flex flex-col-reverse lg:flex-row items-center justify-between gap-10 max-w-7xl mx-auto px-6">
      <div class="flex-1 space-y-6">
        <h5 class="text-sm text-blue-600 font-bold uppercase">SOBRE NÓS</h5>
        <h1 class="text-3xl font-bold text-gray-800">
          Quem somos <br />e por que existimos
        </h1>
        <p class="text-gray-600">
          Fundada em 2018, a Badji Tech System é especializada em desenvolvimento, construção e manutenção de software sob medida. Nossa missão é entregar produtos confiáveis, escaláveis e alinhados aos objetivos dos nossos clientes, promovendo inovação, eficiência e crescimento sustentável.
        </p>
      </div>
      <div class="flex-1 flex justify-center">
        <img
          src="/src/assets/images/webdeveloper.gif"
          alt="Desenvolvedor trabalhando"
          class="max-w-md rounded-3xl p-4"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import 'scrollreveal'
import { onMounted } from 'vue'

onMounted(() => {
  const sr = ScrollReveal({ origin: 'top', distance: '60px', duration: 800, reset: false })
  sr.reveal('#about h5', { delay: 100 })
  sr.reveal('#about h1', { delay: 300 })
  sr.reveal('#about p', { delay: 500 })
  sr.reveal('#about img', { delay: 700 })
})
</script>
