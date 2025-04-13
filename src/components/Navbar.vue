<template>
  <header class="fixed inset-x-0 top-0 z-50 flex items-center justify-between px-6 pt-4 text-sm duration-1000 animate-in fade-in-0 slide-in-from-top-1 fill-mode-backwards [animation-delay:0ms]">
    <div class="container mx-auto flex w-full justify-between items-center">
      <a href="#" class="flex items-center gap-3 rounded-xl px-5 py-2.5 text-black bg-black/5 dark:bg-white/5 font-bold tracking-wider dark:text-white backdrop-blur-md transition-all duration-300 hover:shadow-md hover:shadow-[#d1e5f4]/10">
        <div class="text-xl font-yuruka">IMPHNEN</div>
      </a>
      
      <nav class="flex items-center">
        <ul class="flex flex-col md:flex-row items-center gap-1 md:rounded-xl backdrop-blur-md md:bg-black/5 md:dark:bg-white/5 md:px-4 md:py-1.5 font-medium absolute md:static transition-all duration-300 transform-gpu
                   md:mt-0 overflow-y-auto
                   md:opacity-100 md:pointer-events-auto"
            :class="mobileMenuOpen ? 'inset-0 top-0 h-screen bg-white/80 dark:bg-black/80 px-6 py-10 translate-y-0 opacity-100 z-40' : 'md:translate-y-0 opacity-0 pointer-events-none -translate-y-10'">
          <li v-for="(item, index) in navItems" :key="index" class="w-full md:w-auto">
            <a :href="item.href" 
               class="relative block px-3 py-3 md:py-1.5 transition-all duration-300 dark:hover:text-[#d1e5f4] rounded-lg hover:bg-black/5 dark:hover:bg-white/5 w-full text-center my-2 md:my-0 text-lg md:text-sm"
               @click="mobileMenuOpen = false">
              {{ item.label }}
            </a>
          </li>
          <li class="md:hidden mt-6 md:mt-0">
            <ThemeToggle />
          </li>
        </ul>
        
        <div class="hidden md:block ml-2">
          <ThemeToggle />
        </div>
        <button class="ml-4 h-10 w-10 rounded-lg bg-black/5 dark:bg-white/5 flex flex-col justify-center items-center md:hidden z-50" @click="toggleMobileMenu">
          <div class="w-6 h-0.5 bg-current transition-all duration-300"
               :class="mobileMenuOpen ? 'rotate-45 translate-y-1.5' : ''"></div>
          <div class="w-6 h-0.5 bg-current my-1.5 transition-all duration-300"
               :class="mobileMenuOpen ? 'opacity-0' : 'opacity-100'"></div>
          <div class="w-6 h-0.5 bg-current transition-all duration-300"
               :class="mobileMenuOpen ? '-rotate-45 -translate-y-1.5' : ''"></div>
        </button>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';
import ThemeToggle from './ThemeToggle.vue';

const mobileMenuOpen = ref(false);
const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
};

const navItems = [
  { label: 'Tentang', href: '#about' },
  { label: 'Proyek', href: '#project' },
  { label: 'Komunitas', href: '#comunity' },
  { label: 'Merchandise', href: '#merch' },
];
</script>