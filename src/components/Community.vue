<template>
  <section id="community" class="">
    <!-- Heading content -->
    <hgroup class="flex flex-col px-3 text-center items-center mt-20 animate-in fade-in slide-in-from-bottom-5 duration-700">
      <h1 class="mb-6 text-3xl md:text-4xl lg:text-5xl font-bold">Bergabung dengan Komunitas</h1>
      <p class="mb-7 text-current/70 sm:text-lg ">
        Dihuni oleh kaum rebahan, vibe coder, sepuh, haters PHP
      </p>
    </hgroup>
    <div class="flex flex-wrap justify-center gap-6 px-4 w-full max-w-4xl mx-auto animate-in fade-in slide-in-from-bottom-5 duration-700">
      <!-- Facebook Card -->
      <div class="social-card flex-1 min-w-[280px] bg-blue-500/20 backdrop-blur-sm rounded-lg overflow-hidden border border-white/10">
        <div class="p-6 flex flex-col items-center">
          <svg viewBox="0 0 24 24" class="h-10 w-10 text-blue-400 transition-transform duration-300 hover:scale-125">
            <path fill="currentColor" d="M12 2.04c-5.5 0-10 4.49-10 10.02c0 5 3.66 9.15 8.44 9.9v-7H7.9v-2.9h2.54V9.85c0-2.51 1.49-3.89 3.78-3.89c1.09 0 2.23.19 2.23.19v2.47h-1.26c-1.24 0-1.63.77-1.63 1.56v1.88h2.78l-.45 2.9h-2.33v7a10 10 0 0 0 8.44-9.9c0-5.53-4.5-10.02-10-10.02Z"></path>
          </svg>
          <h3 class="mt-4 text-xl font-bold">Group Facebook</h3>
          <p class="mt-2 text-sm text-center opacity-80">Komunitas resmi IMPHNEN di Facebook. Ngegoreng, share meme, atau sekadar numpang rebahan bareng.</p>
          <a href="https://www.facebook.com/groups/programmerhandal/" target="_blank" rel="noopener" class="mt-4 px-6 py-2 rounded-full bg-blue-500/40 hover:bg-blue-500/60 transition-colors">
            Gabung
          </a>
        </div>
      </div>

      <!-- Instagram Card -->
      <div class="social-card flex-1 min-w-[280px] bg-gradient-to-br from-purple-500/20 to-pink-500/20 backdrop-blur-sm rounded-lg overflow-hidden border border-white/10">
        <div class="p-6 flex flex-col items-center">
          <svg viewBox="0 0 24 24" class="h-10 w-10 text-pink-400 transition-transform duration-300 hover:scale-125">
            <path fill="currentColor" d="M7.8 2h8.4C19.4 2 22 4.6 22 7.8v8.4a5.8 5.8 0 0 1-5.8 5.8H7.8C4.6 22 2 19.4 2 16.2V7.8A5.8 5.8 0 0 1 7.8 2m-.2 2A3.6 3.6 0 0 0 4 7.6v8.8C4 18.39 5.61 20 7.6 20h8.8a3.6 3.6 0 0 0 3.6-3.6V7.6C20 5.61 18.39 4 16.4 4H7.6m9.65 1.5a1.25 1.25 0 0 1 1.25 1.25A1.25 1.25 0 0 1 17.25 8A1.25 1.25 0 0 1 16 6.75a1.25 1.25 0 0 1 1.25-1.25M12 7a5 5 0 0 1 5 5a5 5 0 0 1-5 5a5 5 0 0 1-5-5a5 5 0 0 1 5-5m0 2a3 3 0 0 0-3 3a3 3 0 0 0 3 3a3 3 0 0 0 3-3a3 3 0 0 0-3-3Z"></path>
          </svg>
          <h3 class="mt-4 text-xl font-bold">Instagram</h3>
          <p class="mt-2 text-sm text-center opacity-80">Konten santai seputar coding dan update dari IMPHNEN.</p>
          <a href="https://instagram.com/imphnen.dev" target="_blank" rel="noopener" class="mt-4 px-6 py-2 rounded-full bg-gradient-to-r from-purple-500/40 to-pink-500/40 hover:from-purple-500/60 hover:to-pink-500/60 transition-colors">
            Ikuti
          </a>
        </div>
      </div>
    </div>
    <div class="relative flex h-[calc(100dvh-15rem)] min-h-max max-w-[900dvw] w-full flex-col items-center overflow-hidden">

      <div class="absolute inset-0 z-0">
        <div class="absolute top-20 -left-32 w-96 h-96 bg-purple-500/10 rounded-full blur-[110px]"></div>
        <div class="absolute bottom-48 -right-28 w-80 h-80 bg-cyan-500/10 rounded-full blur-[90px]"></div>
        <div class="absolute top-1/3 left-1/3 w-64 h-64 bg-indigo-500/10 rounded-full blur-[80px]"></div>
      </div>
      
      <!-- Discord button -->
      <div class="group mt-20 flex flex-col items-center z-10 animate-in fade-in slide-in-from-bottom-5 duration-700 delay-300">
        <a class="p-4 mb-3 text-indigo-400 hover:text-indigo-300 transition-colors" 
           href="https://discord.gg/MuWtSaGm" target="_blank" rel="noopener" aria-label="Bergabung di Discord">
          <svg viewBox="0 0 24 24" width="1.2em" height="1.2em" class="h-10 w-10 transition-transform duration-300 hover:scale-125">
            <path fill="currentColor" d="M18.59 5.89c-1.23-.57-2.54-.99-3.92-1.23c-.17.3-.37.71-.5 1.04c-1.46-.22-2.91-.22-4.34 0c-.14-.33-.34-.74-.51-1.04c-1.38.24-2.69.66-3.92 1.23c-2.48 3.74-3.15 7.39-2.82 10.98c1.65 1.23 3.24 1.97 4.81 2.46c.39-.53.73-1.1 1.03-1.69c-.57-.21-1.11-.48-1.62-.79c.14-.1.27-.21.4-.31c3.13 1.46 6.52 1.46 9.61 0c.13.11.26.21.4.31c-.51.31-1.06.57-1.62.79c.3.59.64 1.16 1.03 1.69c1.57-.49 3.17-1.23 4.81-2.46c.39-4.17-.67-7.78-2.82-10.98Zm-9.75 8.78c-.94 0-1.71-.87-1.71-1.94s.75-1.94 1.71-1.94s1.72.87 1.71 1.94c0 1.06-.75 1.94-1.71 1.94m6.31 0c-.94 0-1.71-.87-1.71-1.94s.75-1.94 1.71-1.94s1.72.87 1.71 1.94c0 1.06-.75 1.94-1.71 1.94"></path>
          </svg>
        </a>
        
        <a href="https://discord.gg/MuWtSaGm" target="_blank" rel="noopener">
          <div class="relative max-w-max">
            <button role="button" class="animate rounded text-sm font-bold hover:scale-[1.01] active:scale-100 fancy min-w-[5.5rem] px-4 py-2.5">
              Gabung Discord
            </button>
            <span class="fancy-bg absolute inset-0 -z-10 h-full w-[80%] min-w-[1rem] scale-y-75 bg-cyan-500/90 px-4 py-2 blur-xl" style="--easing: x; --duration: 8s;"></span>
            <span class="fancy-bg absolute inset-0 -z-10 h-full w-[80%] min-w-[1rem] scale-y-75 bg-indigo-500/90 px-4 py-2 blur-xl" style="--easing: y; --duration: 8s;"></span>
            <span class="fancy-bg absolute inset-0 -z-10 h-full w-[80%] min-w-[1rem] scale-y-75 bg-purple-500/90 px-4 py-2 blur-xl" style="--easing: z; --duration: 8s;"></span>
          </div>
        </a>
      </div>
      
      <!-- Community profile images -->
      <div class="absolute -mt-[18rem] md:-mt-[14.5rem] w-[1024px] select-none">
        <div class="flex h-full origin-bottom-right select-none flex-wrap gap-4">
          <div v-for="(profile, i) in profilePositions" :key="i"
               class="absolute left-0 top-0 touch-none select-none transition-opacity"
               :style="{
                 width: `${profile.size}px`, 
                 height: `${profile.size}px`, 
                 '--delay': `${profile.delay}ms`,
                 translate: `${profile.x}px ${profile.y}px`
               }">
            <button class="group absolute inset-0 h-full w-full touch-none select-none opacity-0"
                    :class="{'_animate': i < 8}">
              <div>
                <img class="group aspect-square h-full w-full touch-none select-none rounded-[50%] object-cover outline outline-4"
                     :class="profile.outlineColor"
                     :src="profile.image"
                     alt="community profile picture"
                     loading="lazy"
                     :width="profile.size"
                     :height="profile.size">
              </div>
            </button>
          </div>
        </div>
      </div>  
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue';

// Define outline colors
const outlineColors = [
  'outline-blue-500', 'outline-purple-500', 'outline-cyan-500',
  'outline-indigo-500', 'outline-amber-500', 'outline-red-500',
  'outline-yellow-500', 'outline-orange-500', 'outline-lime-500',
  'outline-pink-500', 'outline-green-500', 'outline-sky-500'
];

// Helper function to get a random outline color
const getRandomOutlineColor = () => {
  const randomIndex = Math.floor(Math.random() * outlineColors.length);
  return outlineColors[randomIndex];
};

// Separate profile images
const profileImages = [
  "https://cdn.discordapp.com/avatars/757213657229819934/e5ef2156b2ea2123d55756a2590f4ac3?size=1024",
  "https://cdn.discordapp.com/avatars/858646962131828756/5e880fa2eb37f669619a613d2a0a956b?size=1024",
  "https://cdn.discordapp.com/avatars/610798958016724992/cb83396ab2b54d34189c63efa7dafb01?size=1024",
  "https://cdn.discordapp.com/avatars/989866107496198144/d62a8021aa6fa34526d0acfef1fce6c5.png?size=1024",
  "https://cdn.discordapp.com/avatars/717738246490030200/7586ac528dc97d0768d80e0b25e3f628.png?size=1024",
  "https://cdn.discordapp.com/avatars/499021389572079620/411267db755d8fef2915362213897063?size=1024",
  "https://cdn.discordapp.com/avatars/799838753752743968/53bdd6d2c9d3174050bc99bb1dcbcedb.png?size=1024",
  "https://cdn.discordapp.com/avatars/368289267941900298/9e158e3789576871693d4a78b092b59c.png?size=1024",
];

// Shuffle function
const shuffleArray = <T>(array: T[]): T[] => {
  const newArray = [...array];
  for (let i = newArray.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [newArray[i], newArray[j]] = [newArray[j], newArray[i]];
  }
  return newArray;
};

// Define position data without images
const positionsData = [
  { x: 187, y: 296, size: 172, delay: 0 },
  { x: 735, y: 441, size: 164, delay: 150 },
  { x: 391, y: 615, size: 149, delay: 300 },
  { x: 648, y: 709, size: 128, delay: 450 },
  { x: 568, y: 594, size: 120, delay: 200 },
  { x: 736, y: 277, size: 101, delay: 250 },
  { x: 284, y: 533, size: 90, delay: 350 },
  { x: 147, y: 553, size: 87, delay: 400 },
];

// Combine shuffled images with position data
const shuffledImages = shuffleArray(profileImages);
const profilePositions = ref(
  positionsData.map((position, index) => ({
    ...position,
    image: shuffledImages[index],
    outlineColor: getRandomOutlineColor(),
  }))
);
</script>

<style scoped>
.fancy {
  position: relative;
  color: white;
  background-color: rgba(79, 70, 229, 0.3);
  backdrop-filter: blur(4px);
  border-radius: 0.375rem;
  border: 1px solid rgba(255, 255, 255, 0.1);
  overflow: hidden;
}

.fancy-bg {
  pointer-events: none;
  animation: moveBlur var(--duration, 8s) ease-in-out infinite alternate;
}

@keyframes moveBlur {
  0% {
    transform: translateX(-30%) translateY(10%) scale(0.8);
  }
  100% {
    transform: translateX(30%) translateY(-10%) scale(1.2);
  }
}

/* Animation for profile pictures */
._animate {
  animation: fadeInScale 0.7s ease-out forwards;
  animation-delay: calc(var(--delay, 0) * 1ms);
}

@keyframes fadeInScale {
  from {
    opacity: 0;
    transform: scale(0.8);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

/* Add this to ensure images don't get cropped by overflow */
section {
  padding-bottom: 100px;
}

/* Add social card hover effect */
.social-card {
  transition: transform 0.3s ease-out;
}

.social-card:hover {
  transform: translateY(-5px);
}
</style>
