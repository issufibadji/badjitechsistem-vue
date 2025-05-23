<template>
  <div>
    <!-- Botão para abrir drawer (mobile only) -->
    <div class="fixed top-2 left-2 z-50">
      <button @click="toggleSidebar" class="text-white bg-blue-700 p-2 rounded-md shadow hover:bg-blue-800">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>
    </div>

    <!-- Sidebar / Topbar responsivo -->
    <aside
      :class="[
        'fixed z-40 bg-blue-700 text-white transition-all duration-300 ease-in-out w-full',
        'flex flex-row items-center justify-between p-2',
        'top-0 left-0 h-16 md:h-screen md:w-64 md:flex-col md:items-center md:justify-between',
        sidebarOpen ? 'translate-y-0' : '-translate-y-full',
        'md:translate-y-0 md:translate-x-0'
      ]"
    >
      <div class="p-2 md:p-6 w-full flex justify-between md:flex-col md:items-center md:justify-start">
        <div class="text-center mb-4 hidden md:block">
          <img src="/src/assets/images/logotipo.png" alt="Badji Tech System" class="h-20 mx-auto" />
          <p class="text-xs font-light mt-2">Badji <b>Tech</b><br /><b>System</b></p>
        </div>

        <!-- Nav icons -->
        <nav class="flex gap-4 md:flex-col md:gap-6 text-xl w-full justify-center md:justify-start">
          <router-link to="/login" class="hover:text-blue-300 transition">
            <i class="fa-solid fa-user"></i>
          </router-link>
          <router-link to="/#home" class="hover:text-blue-300 transition">
            <i class="fa-solid fa-house"></i>
          </router-link>
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
        </nav>

        <div class="hidden md:block mt-10 text-center">
          <a href="#contact" class="border border-white p-3 rounded-full hover:bg-white hover:text-blue-700 transition">
            <i class="fa-solid fa-calendar-day"></i>
          </a>
        </div>
      </div>
    </aside>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import 'scrollreveal'

const sidebarOpen = ref(false)

function toggleSidebar() {
  sidebarOpen.value = !sidebarOpen.value
}

onMounted(() => {
  const sr = ScrollReveal({ origin: 'top', distance: '50px', duration: 800, reset: false })
  sr.reveal('.nav-logo', { delay: 100 })
  sr.reveal('.nav-links', { delay: 100 })
  sr.reveal('.nav-link', { delay: 200, interval: 100 })
  sr.reveal('#schedule', { delay: 700 })
})
</script>

<style scoped>
</style>
