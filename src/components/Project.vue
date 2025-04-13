<template>
  <section id="project" class="relative py-28 overflow-hidden">
    <!-- Background elements -->
    <div class="absolute inset-0 z-0">
      <div class="absolute top-20 -right-32 w-96 h-96 bg-green-500/10 rounded-full blur-[110px]"></div>
      <div class="absolute bottom-20 -left-28 w-80 h-80 bg-amber-500/10 rounded-full blur-[90px]"></div>
    </div>
    
    <!-- Section content -->
    <div class="container mx-auto px-6 relative z-10">
      <!-- Section header -->
      <div class="mb-16 text-center">
        <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 animate-in fade-in slide-in-from-bottom-5 duration-700">
          Proyek Komunitas
        </h2>
        <div class="w-20 h-1 bg-gradient-to-r from-blue-400 to-indigo-500 mx-auto rounded-full"></div>
        <p class="mt-6 max-w-2xl mx-auto text-lg">
          Beberapa proyek komunitas kami.
        </p>
      </div>
      
      <!-- Projects grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="(project, index) in communityProjects" :key="index" 
             class="bg-black/5 dark:bg-white/5 backdrop-blur-sm rounded-xl border border-black/10 dark:border-white/10 overflow-hidden animate-in fade-in slide-in-from-bottom-5 duration-700"
             :style="{ animationDelay: `${index * 100}ms` }">
          <div class="relative">
            <img :src="project.image" :alt="project.title" class="w-full h-48 object-cover" loading="lazy" />
            <div class="absolute top-3 right-3">
              <span class="bg-black/60 text-white text-xs px-3 py-1 rounded-full backdrop-blur-sm">
                {{ project.status }}
              </span>
            </div>
          </div>
          
          <div class="p-6">
            <h3 class="text-xl font-bold mb-2">{{ project.title }}</h3>
            <p class="text-current/70 mb-4">{{ project.description }}</p>
            <div class="flex flex-wrap gap-2 mb-4">
              <span v-for="(tag, idx) in project.tags" :key="idx"
                    class="text-xs px-3 py-1 rounded-full bg-black/5 dark:bg-white/5">
                {{ tag }}
              </span>
            </div>
            <div class="flex justify-between items-center">
              <div class="flex -space-x-2">
                <div v-for="(contributor, idx) in project.contributors.slice(0, 3)" :key="idx" 
                     class="w-8 h-8 rounded-full border-2 border-black/5 dark:border-white/5 overflow-hidden">
                  <img :src="contributor" alt="contributor" class="w-full h-full object-cover" />
                </div>
                <div v-if="project.contributors.length > 3" 
                     class="w-8 h-8 rounded-full bg-black/10 dark:bg-white/10 flex items-center justify-center text-xs">
                  +{{ project.contributors.length - 3 }}
                </div>
              </div>
              <a :href="project.repoUrl" target="_blank" rel="noopener" 
                 class="text-sm flex items-center gap-1 text-current/70 hover:text-current transition-colors">
                <i class="ri-github-fill"></i> Repository
              </a>
            </div>
          </div>
        </div>
      </div>
      
      <!-- GitHub button -->
      <div class="mt-12 flex justify-center animate-in fade-in slide-in-from-bottom-5 duration-700" style="animation-delay: 300ms;">
        <a 
          href="https://github.com/orgs/IMPHNEN/repositories" 
          target="_blank" 
          rel="noopener noreferrer" 
          class="inline-flex items-center gap-2 px-6 py-3 bg-black/10 dark:bg-white/10 hover:bg-black/20 dark:hover:bg-white/20 text-current rounded-full transition-all border border-black/10 dark:border-white/10 backdrop-blur-sm"
        >
          <i class="ri-github-fill text-xl"></i>
          Lihat lebih banyak di GitHub
          <i class="ri-arrow-right-line"></i>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const communityProjects = [
  {
    title: "IMPHNEN OS",
    description: "Distribusi Linux Dari Programmer Malas Ngoding",
    image: "/static/projects/imphnen-os.png",
    status: "Alpha Release",
    tags: ["Arch", "Linux"],
    contributors: [
      "https://avatars.githubusercontent.com/u/118181082?s=96&v=4"
    ],
    repoUrl: "https://github.com/IMPHNEN/ImphnenOs"
  },
  {
    title: "IMPHNEN Gacha",
    description: "Web Gacha Merchandise IMPHNEN",
    image: "/static/projects/imphnen-gacha.png",
    status: "In Progress",
    tags: ["React", "Typescript", "Vite"],
    contributors: [
      "https://avatars.githubusercontent.com/u/73023445?s=96&v=4",
      "https://avatars.githubusercontent.com/u/53475078?s=96&v=4",
      "https://avatars.githubusercontent.com/u/109430358?s=96&v=4"
    ],
    repoUrl: "https://github.com/IMPHNEN/imphnen-gacha"
  },
  {
    title: "Web Kamus Gen Z",
    description: "Kamus yang berisikan koleksi bahasa gaul Gen Z beserta artinya. Dari \"santuy\" sampai \"mager\", semua ada disini.",
    image: "/static/projects/kamus-gen-z.webp",
    status: "Completed",
    tags: ["NextJS", "ExpressJS", "Prisma"],
    contributors: [
      "https://avatars.githubusercontent.com/u/89193581?s=96&v=4", 
      "https://avatars.githubusercontent.com/u/77146709?s=96&v=4",
      "https://avatars.githubusercontent.com/u/45933947?s=96&v=4",
      "https://avatars.githubusercontent.com/u/85545297?s=96&v=4",
      "https://avatars.githubusercontent.com/u/109430358?s=96&v=4",
      "https://avatars.githubusercontent.com/u/118181082?s=96&v=4"

    ],
    repoUrl: "https://github.com/orgs/IMPHNEN/repositories?q=gen+z"
  }
];
</script>