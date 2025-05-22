<template>
  <section id="portfolio" class="py-20 bg-blue-100 text-center">
    <div class="mb-10">
      <h5 class="text-sm text-blue-600 font-bold uppercase">PORTFÓLIO</h5>
      <h1 class="text-3xl font-bold text-gray-800 mt-2">Conheça nossos trabalhos</h1>
    </div>

    <div class="grid gap-8 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 px-6 max-w-7xl mx-auto">
      <div
        v-for="(projeto, index) in portfolio"
        :key="index"
        class="bg-white border border-blue-400 rounded-xl shadow-xl overflow-hidden text-left"
      >
        <img :src="projeto.img" :alt="projeto.title" class="w-full h-auto object-cover rounded-t-xl" />
        <div class="p-6 space-y-2">
          <h3 class="text-xl font-bold text-blue-700">{{ projeto.title }}</h3>
          <p class="text-sm text-gray-600">{{ projeto.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const portfolio = [
  {
    title: 'GooFood',
    img: '/src/assets/images/img/goofood1.png',
    description:
      'Plataforma de delivery sob demanda, com painel administrativo para gerenciamento de restaurantes, pedidos em tempo real e integração com gateways de pagamento.',
  },
  {
    title: 'SalonPro',
    img: '/src/assets/images/img/salon.png',
    description:
      'Sistema de agendamento e CRM para salões de beleza, com notificações automáticas e relatórios de desempenho de atendimentos.',
  },
  {
    title: 'DoctorCare',
    img: '/src/assets/images/img/doctorcare.png',
    description:
      'Solução para clínicas e consultórios: agendamento de pacientes, histórico médico e teleconsulta integrada.',
  },
]
</script>
