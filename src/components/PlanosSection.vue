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
        class="group pricing-wrapper w-full relative rounded-2xl bg-gradient-to-t from-blue-100 to-white p-0.5 shadow-[0_0px_25px_0px_rgba(0,0,0,0.1)] transition-all duration-300 ease-in-out hover:shadow-[0_0px_25px_0px_rgba(0,0,0,0.2)]"
        :class="{
          'from-blue-200': plano.destaque,
          'from-blue-600': plano.title === 'Enterprise'
        }"
      >
        <div
          class="relative bg-white rounded-2xl p-8 text-center w-full z-0 overflow-hidden hover:-translate-y-1 transition-all duration-300 ease-in-out h-full flex flex-col justify-between"
        >
          <div>
            <h3 class="text-xl font-bold text-gray-800">{{ plano.title }}</h3>
            <span class="text-xs text-blue-600">{{ plano.description }}</span>
            <p class="text-3xl my-2 font-extrabold text-blue-700">{{ plano.price }}</p>
            <ul class="text-sm text-gray-800 mt-4 text-left space-y-1">
              <li v-for="(item, i) in plano.features" :key="i">
                <span class="text-blue-600 font-bold">✓</span> {{ item }}
              </li>
            </ul>
          </div>
          <a
            :href="plano.link"
            class="checkout-button flex items-center justify-center bg-blue-700 text-white border-none py-2.5 px-5 text-md rounded-md w-full hover:bg-blue-800 transition-colors duration-300 mt-6"
          >
            {{ plano.cta }}
          </a>
          <svg
            v-if="plano.title === 'Básico'"
            xmlns="http://www.w3.org/2000/svg"
            class="absolute top-8 left-8 text-[500px] z-[-1] pointer-events-none text-blue-100 transition duration-1000 delay-500 group-hover:-translate-y-8 group-hover:-translate-x-8"
            width="1em"
            height="1em"
            viewBox="0 0 20 20"
          >
            <path
              fill="currentColor"
              fill-rule="evenodd"
              d="M6 2a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V7.414A2 2 0 0 0 15.414 6L12 2.586A2 2 0 0 0 10.586 2zm5 6a1 1 0 1 0-2 0v3.586l-1.293-1.293a1 1 0 1 0-1.414 1.414l3 3a1 1 0 0 0 1.414 0l3-3a1 1 0 0 0-1.414-1.414L11 11.586z"
              clip-rule="evenodd"
            />
          </svg>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const planos = [
  {
    title: 'Básico',
    description: 'get it anywhere',
    features: [
      'Até 16 horas de dedicação',
      'Design & Protótipos',
      'Testes & Deploy (32h)',
    ],
    price: 'Free',
    cta: 'Free Download',
    link: '#contact',
    destaque: false,
  },
  {
    title: 'Profissional',
    description: 'starting at',
    features: [
      '200 horas de desenvolvimento',
      'Suporte Mensal (20h)',
      'Testes & Deploy (32h)',
    ],
    price: 'R$ 12.060,00',
    cta: 'Get it!',
    link: '#contact',
    destaque: true,
  },
  {
    title: 'Enterprise',
    description: 'contact us for info',
    features: [
      'Horas ilimitadas',
      'Suporte prioritário',
      'Integrações & Automação',
    ],
    price: '~',
    cta: 'Solicitar Orçamento',
    link: '#contact',
    destaque: false,
  },
]
</script>
