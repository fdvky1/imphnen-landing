<template>
  <section class="relative min-h-screen flex items-center justify-center py-32 overflow-hidden hero-section">
    <!-- Gradient circles in background -->
    <div class="absolute inset-0 z-0">
      <div class="absolute top-1/4 -left-28 w-96 h-96 bg-blue-500/20 rounded-full blur-[100px]"></div>
      <div class="absolute bottom-1/3 -right-28 w-80 h-80 bg-purple-500/20 rounded-full blur-[100px]"></div>
      <div class="absolute top-2/3 left-1/4 w-64 h-64 bg-cyan-500/20 rounded-full blur-[80px]"></div>
    </div>
    
    <!-- Background repeating quotes -->
    <div class="absolute inset-0 quotes-background">
      <span v-for="(quote, i) in quoteElements" :key="i" 
            class="absolute text-current/15 whitespace-nowrap font-medium"
            :style="{ 
              left: `${quote.x}%`, 
              top: `${quote.y}%`,
              transform: `rotate(${quote.rotate}deg)`,
              fontSize: `${quote.size}rem`
            }">
        {{ quote.text }}
      </span>
    </div>
    
    <!-- Bottom fade effect -->
    <div class="absolute bottom-0 left-0 right-0 h-32 bg-gradient-to-t from-[var(--bg-primary)] to-transparent z-10"></div>
    
    <!-- Hero content -->
    <div class="container mx-auto px-6 relative z-20">
      <div class="flex flex-col lg:flex-row w-full items-center gap-8 lg:gap-12">
        <!-- Text content -->
        <div class="text-center w-full">
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 leading-tight animate-in fade-in slide-in-from-bottom-10 duration-1000">
            Ingin Menjadi <br class="hidden md:block lg:hidden"><span class="underline">Programmer Handal</span> Namun <br class="hidden xl:block"><span class="underline">Enggan Ngoding</span> 
          </h1>
          <p class="text-xl md:text-2xl text-current/80 mb-6 animate-in fade-in slide-in-from-bottom-5 duration-1000 delay-300">
            Ngoding? Malas, Besok aja.
          </p>

          <div class="flex flex-col sm:flex-row justify-center gap-4 mt-4 animate-in fade-in slide-in-from-bottom-5 duration-1000 delay-500 text-xs sm:text-base">
            <a href="#community" class="px-6 py-3 bg-indigo-500/70 dark:bg-indigo-500/90 text-white rounded-xl shadow-md hover:bg-indigo-500/90 dark:hover:bg-indigo-500/70 transition">Gabung Komunitas</a>
            <a href="#about" class="px-6 py-3 border border-current/20 text-current rounded-xl hover:bg-black/10 dark:hover:bg-white/10 transition">Pelajari Lebih Lanjut</a>
          </div>
        </div>
        
        <!-- <div class="lg:w-1/2 animate-in fade-in slide-in-from-right-10 duration-1000 delay-200">
          <div class="relative bg-black/70 text-white/70 dark:text-current/70 font-mono p-6 rounded-xl shadow-lg border border-green-400/20">
            <p class="mb-2">$ sudo jadi-programmer --handal</p>
            <p class="mb-2">Password: ********</p>
            <p class="mb-2">Access granted<i class="ri-check-line"></i></p>
            <p class="mb-2">$ ngoding?</p>
            <p class="mb-2 text-yellow-300">> Malas</p>
            <p class="mb-2">$ node ai-helper.js</p>
            <p class="mb-2 text-cyan-300">> Buatkan saya landing page menggunakan VueJS</p>
            <p class="mt-4 font-bold">// Certified Vibe Coder™</p>

            
            <div class="absolute inset-0 rounded-xl bg-gradient-to-tr from-blue-500/30 to-purple-500/30 blur-xl -z-10 scale-105"></div>
          </div>
        </div> -->
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const quotes = ['Malas', 'Besok aja', 'Mending scroll pesbuk', 'Suruh AI aja', 'Di gw jalan kok', 'koneksi.php', 'Duh ada PHP bete gw', 'Certified Vibe Coder', 'Nunggu deadline', 'Ngoding php dapet lambo', 'King JS'];
const quoteElements = ref<{ text: string; x: number; y: number; rotate: number; size: number; }[]>([]);

function getRandom(min: number, max: number) {
  const array = new Uint32Array(1);
  crypto.getRandomValues(array);
  return min + (array[0] / 2**32) * (max - min);
}

// Generate random quote elements
for (let i = 0; i < 50; i++) {
  quoteElements.value.push({
    text: quotes[Math.floor(getRandom(0, quotes.length))],
    x: getRandom(0, 100),
    y: getRandom(0, 100),
    rotate: getRandom(-30, 30),
    size: getRandom(0.8, 2),
  });
}
</script>

<style scoped>
.quotes-background {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 0;
  overflow: hidden;
}

.hero-section {
  position: relative;
}
</style>