<template>
  <section id="planos" class="py-20 bg-white text-center">
    <div class="mb-10">
      <h5 class="text-sm text-blue-600 font-bold uppercase">PLANOS</h5>
      <h1 class="text-3xl font-bold text-gray-800 mt-2">Escolha o plano ideal para você</h1>
    </div>

    <div class="grid gap-8 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 px-6 max-w-7xl mx-auto">
    <div
      v-for="(plano, index) in planos"
      :key="index"
      class="group relative transition-all duration-300 ease-in-out"
    >
      <!-- Sombra azul inferior centralizada -->
      <div
        class="absolute bottom-0 left-0 right-0 mx-auto -mb-1 h-2 w-[92%] bg-blue-700 rounded-b-xl z-0 group-hover:mb-0 group-hover:bg-transparent transition-all duration-300 ease-in-out"
      ></div>

      <!-- Conteúdo padrão do card -->
      <div
        class="relative z-10 border border-blue-400 rounded-xl shadow-md hover:shadow-xl transition p-6 max-w-sm mx-auto flex flex-col gap-4 min-h-[440px]"
        :class="{ 'bg-blue-50 border-2': plano.destaque }"
      >
        <h3 class="text-xl font-bold text-blue-700">{{ plano.title }}</h3>
        <p class="text-sm text-gray-500">{{ plano.description }}</p>
        <ul class="text-left text-sm text-gray-700 space-y-1">
          <li v-for="(item, i) in plano.features" :key="i">
            <span class="text-blue-600 font-bold">✓</span> {{ item }}
          </li>
        </ul>
        <p class="text-2xl font-bold text-gray-800">{{ plano.price }}</p>
        <a
          :href="plano.link"
          class="mt-auto inline-block px-6 py-2 border border-blue-600 rounded-full font-bold text-blue-600 hover:bg-blue-600 hover:text-white transition"
          :class="{ 'bg-blue-600 text-white': plano.destaque }"
        >
          {{ plano.cta }}
        </a>
      </div>
    </div>

    </div>
  </section>
</template>


<script setup>
const planos = [
  {
    title: 'Básico',
    description: 'Ideal para protótipos e projetos simples',
    features: [
      'Até 16 horas de dedicação',
      'Design & Protótipos',
      'Testes & Deploy (32h)',
    ],
    price: 'R$ 720,00',
    cta: 'Contratar',
    link: '#contact',
    destaque: false,
  },
  {
    title: 'Profissional',
    description: 'Para desenvolvimento web completo',
    features: [
      '200 horas de desenvolvimento',
      'Suporte Mensal (20h)',
      'Testes & Deploy (32h)',
    ],
    price: 'R$ 12.060,00',
    cta: 'Contratar',
    link: '#contact',
    destaque: true,
  },
  {
    title: 'Enterprise',
    description: 'Projetos sob medida e suporte avançado',
    features: [
      'Horas ilimitadas',
      'Suporte prioritário',
      'Integrações & Automação',
    ],
    price: 'Sob consulta',
    cta: 'Solicitar Orçamento',
    link: '#contact',
    destaque: false,
  },
]
</script>
