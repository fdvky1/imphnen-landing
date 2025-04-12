
<template>
  <button 
    @click="toggleTheme" 
    class="rounded-lg bg-black/5 dark:bg-white/5 py-2 px-4 hover:bg-black/10 dark:hover:bg-white/10 backdrop-blur-md transition-all duration-300"
    :aria-label="isDark ? 'Switch to light theme' : 'Switch to dark theme'"
  >
    <i v-if="isDark" class="ri-sun-line text-lg"></i>
    <i v-else class="ri-moon-clear-line text-lg"></i>
  </button>
</template>

<script setup lang="ts">
import { ref, onMounted, watch } from 'vue';

const isDark = ref(true); // Default to dark theme

function toggleTheme() {
  isDark.value = !isDark.value;
  updateTheme();
}

function updateTheme() {
  if (isDark.value) {
    document.documentElement.setAttribute("data-theme", "dark");
    localStorage.setItem('theme', 'dark');
  } else {
    document.documentElement.removeAttribute("data-theme");
    localStorage.setItem('theme', 'light');
  }
  console.log(localStorage.getItem('theme'));
}

// On component mount, check for saved preferences
onMounted(() => {
  // Check for saved theme preference or use user's system preference
  const savedTheme = localStorage.getItem('theme');
  if (savedTheme) {
    isDark.value = savedTheme === 'dark';
  } else {
    // Use system preference as fallback
    isDark.value = window.matchMedia('(prefers-color-scheme: dark)').matches;
  }
  updateTheme();
});
</script>