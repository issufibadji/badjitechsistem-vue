<template>
  <div id="app" class="flex">
    <NavBar />
    <main class="flex-1">
      <router-view />
    </main>
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
</script>
