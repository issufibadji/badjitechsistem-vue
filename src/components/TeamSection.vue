<template>
  <section id="team" class="py-20 bg-white">
    <div class="text-center mb-10">
      <h5 class="text-sm text-blue-600 font-bold uppercase">EQUIPE</h5>
      <h2 class="text-3xl font-bold text-gray-800 mt-2">Conheça nosso time</h2>
    </div>

    <div class="flex flex-wrap justify-center gap-6 px-4">
      <div
        v-for="(member, index) in team"
        :key="index"
        class="bg-white border border-blue-300 rounded-lg w-72 p-4 shadow-lg relative overflow-hidden"
      >
        <img
          :src="member.cover"
          :alt="member.name"
          class="w-full h-52 object-cover rounded-t-lg mb-16"
        />

        <div class="w-36 h-36 bg-blue-100 border-2 border-blue-200 rounded-full mx-auto -mt-20 relative z-10 overflow-hidden">
          <img :src="member.photo" :alt="member.name" class="w-full h-full object-cover rounded-full" />
        </div>

        <div class="text-center mt-4">
          <h3 class="text-lg font-bold uppercase">{{ member.name }}</h3>
          <span class="text-xs text-gray-500">{{ member.role }}</span>
          <p class="text-sm text-gray-600 mt-2">{{ member.description }}</p>
        </div>

        <div class="absolute inset-0 bg-black bg-opacity-60 flex items-center justify-center gap-4 opacity-0 hover:opacity-100 transition">
          <a href="#" class="text-blue-400 text-xl"><i class="fab fa-facebook-f"></i></a>
          <a href="#" class="text-blue-400 text-xl"><i class="fab fa-twitter"></i></a>
          <a href="#" class="text-blue-400 text-xl"><i class="fab fa-instagram"></i></a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const team = [
  {
    name: 'Issufi Badji',
    role: 'CEO',
    description:
      'Com mais de 12 anos de experiência em liderança de equipes de tecnologia, John orienta nossa visão estratégica e garante a excelência dos projetos.',
    photo: '@/assets/images/tem1.png',
    cover: 'https://images.unsplash.com/photo-1464823063530-08f10ed1a2dd?auto=format&fit=crop&w=1199&h=799&q=80',
  },
  {
    name: 'IssufiBadji',
    role: 'CTO',
    description:
      'Arquiteta de software com 10+ anos de atuação, Barbara lidera nosso time de inovação e design de sistemas de alta complexidade.',
    photo: '@/assets/images/tem2.png',
    cover: 'https://images.unsplash.com/photo-1464823063530-08f10ed1a2dd?auto=format&fit=crop&w=1199&h=799&q=80',
  },
  {
    name: 'Issufi Badji',
    role: 'Eng.Software && Developer',
    description:
      'Focada em experiência do usuário, Sammy cria wireframes e protótipos que tornam o uso dos sistemas intuitivo e eficiente.',
    photo: '@/assets/images/tem3.png',
    cover: 'https://images.unsplash.com/photo-1464823063530-08f10ed1a2dd?auto=format&fit=crop&w=1199&h=799&q=80',
  },
]
</script>
