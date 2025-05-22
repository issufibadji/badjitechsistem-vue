<template>
  <header class="fixed top-0 right-0 h-screen w-[12.5vw] bg-blue-700 text-white z-50 hidden lg:grid">
    <nav class="flex flex-col items-center justify-between py-10 h-full">
      <a href="#home" class="text-center">
        <img src="/src/assets/images/logotipo.png" alt="Badji Tech System" class="h-24 mx-auto" />
        <div class="text-xs font-light">Badji <b>Tech</b><br /><b>System</b></div>
      </a>

      <div class="flex flex-col gap-6 text-xl">
        <a href="#home" class="hover:text-blue-300 transition">
          <i class="fa-solid fa-house"></i>
        </a>
        <a href="#services" class="hover:text-blue-300 transition">
          <i class="fa-solid fa-business-time"></i>
        </a>
        <a href="#about" class="hover:text-blue-300 transition">
          <i class="fa-solid fa-circle-info"></i>
        </a>
        <a href="#portfolio" class="hover:text-blue-300 transition">
          <i class="fa-solid fa-window-restore"></i>
        </a>
        <a href="#team" class="hover:text-blue-300 transition">
          <i class="fa-brands fa-dev"></i>
        </a>
        <a href="#planos" class="hover:text-blue-300 transition">
          <i class="fa-solid fa-clipboard-list"></i>
        </a>
        <a href="https://thebest-blog.vercel.app/" target="_blank" class="hover:text-blue-300 transition">
          <i class="fa-solid fa-blog"></i>
        </a>
      </div>

      <div>
        <a
          href="#contact"
          id="schedule"
          class="border border-white p-3 rounded-full hover:bg-white hover:text-blue-700 transition"
        >
          <i class="fa-solid fa-calendar-day"></i>
        </a>
      </div>
    </nav>
  </header>
</template>

<script setup>
import 'scrollreveal'
import { onMounted } from 'vue'

onMounted(() => {
  const sr = ScrollReveal({ origin: 'top', distance: '50px', duration: 800, reset: false })
  sr.reveal('.nav-logo', { delay: 100 })
  sr.reveal('.nav-links', { delay: 100 })
  sr.reveal('.nav-link', { delay: 200, interval: 100 })
  sr.reveal('#schedule', { delay: 700 })
})
</script>

<style scoped>
/* NavBar responsiva para mobile pode ser criada como componente separado */
</style>
