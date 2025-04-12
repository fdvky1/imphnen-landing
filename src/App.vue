<script setup>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import About from './components/About.vue';
import Project from './components/Project.vue';
import Community from './components/Community.vue';
import Merchandise from './components/Merchandise.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Navbar/>
  <Hero/>
  <About/>
  <Project/>
  <Community/>
  <Merchandise/>
  <Footer/>
  
  <!-- Copyright section -->
  <div class="py-6 text-center text-sm text-current/70 border-t border-black/10 dark:border-white/10">
    <div class="container mx-auto px-6">
      © 2025 IMPHNEN. All rights reserved.
    </div>
  </div>
</template>

<style scoped>
</style>
