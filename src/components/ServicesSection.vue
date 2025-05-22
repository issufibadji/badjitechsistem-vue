<template>
  <section id="services" class="py-20 border-t border-b border-blue-100">
    <div class="text-center mb-10">
      <h5 class="text-sm text-blue-600 font-bold uppercase">SERVIÇOS</h5>
      <h1 class="text-3xl font-bold text-gray-800 mt-2">
        Soluções tecnológicas <br />sob medida para o seu negócio
      </h1>
    </div>
    <div class="grid gap-8 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 px-6 max-w-7xl mx-auto">
      <div v-for="(service, index) in services" :key="index" class="bg-white p-6 border border-blue-300 rounded-xl shadow-xl hover:shadow-2xl transition">
        <i :class="service.icon" class="text-4xl text-blue-600 mb-4 block"></i>
        <h3 class="text-xl font-bold mb-2 text-center">{{ service.title }}</h3>
        <p class="text-gray-600 text-sm">{{ service.description }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    icon: 'fa-solid fa-layer-group',
    title: 'Web Site',
    description:
      'Criação de portais, intranets e sistemas web responsivos, com foco em performance, segurança e escalabilidade para suportar o crescimento da sua empresa.',
  },
  {
    icon: 'fa-solid fa-window-restore',
    title: 'Design e UX',
    description:
      'Projeto de interfaces atraentes e intuitivas, que garantem ótima experiência ao usuário e fortalecem a identidade visual da sua marca.',
  },
  {
    icon: 'fa-solid fa-mobile',
    title: 'App Mobile',
    description:
      'Desenvolvimento de apps nativos e híbridos para iOS e Android, conectados aos seus sistemas, para levar sua solução na palma da mão do cliente.',
  },
  {
    icon: 'fa-solid fa-cogs',
    title: 'Automacão & Integração',
    description:
      'Integração de APIs, automação de processos e orquestração de serviços que aumentam produtividade e reduzem erros operacionais.',
  },
  {
    icon: 'fa-solid fa-chart-bar',
    title: 'Análise de Sistemas',
    description:
      'Mapeamento de requisitos, levantamento de processos e elaboração de arquiteturas, garantindo soluções alinhadas aos objetivos do seu negócio.',
  },
  {
    icon: 'fa-brands fa-rocketchat',
    title: 'Chatbox',
    description:
      'Atendimento 24/7 e chatbots inteligentes para responder dúvidas, registrar chamados e oferecer suporte ágil aos seus clientes.',
  },
]
</script>
