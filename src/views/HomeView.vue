<template>
  <div>
    <NavBar />
    <main class="pt-20 lg:pt-0">
      <HeroSection />
      <ServicesSection />
      <PlanosSection />
      <AboutSection />
      <PortfolioSection />
      <TeamSection />
      <ContactSection />
      <FooterSection />
    </main>
  </div>
</template>

<script setup>
import NavBar from '@/components/NavBar.vue'
import HeroSection from '@/components/HeroSection.vue'
import ServicesSection from '@/components/ServicesSection.vue'
import PlanosSection from '@/components/PlanosSection.vue'
import AboutSection from '@/components/AboutSection.vue'
import PortfolioSection from '@/components/PortfolioSection.vue'
import TeamSection from '@/components/TeamSection.vue'
import ContactSection from '@/components/ContactSection.vue'
import FooterSection from '@/components/FooterSection.vue'
</script>
