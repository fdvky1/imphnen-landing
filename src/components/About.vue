
<template>
  <section id="about" class="relative py-28 overflow-hidden">
    <!-- Background elements -->
    <div class="absolute inset-0 z-0">
      <div class="absolute top-20 -left-32 w-96 h-96 bg-indigo-500/10 rounded-full blur-[110px]"></div>
      <div class="absolute bottom-20 -right-28 w-80 h-80 bg-cyan-500/10 rounded-full blur-[90px]"></div>
    </div>
    
    <!-- Section content -->
    <div class="container mx-auto px-6 relative z-10">
      <!-- Section header -->
      <div class="mb-16 text-center">
        <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 animate-in fade-in slide-in-from-bottom-5 duration-700">
          Tentang IMPHNEN
        </h2>
        <div class="w-20 h-1 bg-gradient-to-r from-blue-400 to-indigo-500 mx-auto rounded-full"></div>
      </div>
      
      <!-- Main content -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <!-- Image column -->
        <div class="order-2 lg:order-1 animate-in fade-in slide-in-from-left-10 duration-700 delay-100">
          <div class="relative">
            <div class="absolute inset-0 rounded-xl bg-gradient-to-tr from-blue-500/20 to-indigo-500/20 blur-xl -z-10 scale-105"></div>
            <div class="bg-black/5 dark:bg-white/5 backdrop-blur-sm rounded-xl p-5 border border-black/10 dark:border-white/10">
              <img 
                src="/static/banner.png" 
                alt="IMPHNEN" 
                class="w-full h-auto rounded-lg"
              />
              <div class="mt-6">
                <blockquote class="italic text-lg border-l-4 border-blue-500/50 pl-4">
                  "Ngapain ngoding, mending scroll pesnuk."
                </blockquote>
                <p class="mt-2 font-medium text-right text-current/70">— IMPHNEN Philosophy</p>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Text content -->
        <div class="order-1 lg:order-2 space-y-6 animate-in fade-in slide-in-from-right-10 duration-700">
          <p class="">
            IMPHNEN (Ingin Menjadi Programmer Handal Namun Enggan Ngoding) adalah komunitas yang lahir dari keresahan bersama. Kenapa harus ngoding kalau bisa rebahan dan scroll fesnuk?
          </p>
          
          <p>
            Kami bukan komunitas yang mengajarkan cara cepat jadi fullstack dalam 7 hari.
            Kami adalah tempat berkumpulnya para pejuang <code>Ctrl + C</code> dan <code>Ctrl + V</code>, yang lebih jago ngeles  ke klien daripada ngetik <code>;</code> dengan benar.
          </p>
          
          <!-- Feature cards -->
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-5 mt-8">
            <div class="bg-black/5 dark:bg-white/5 backdrop-blur-sm p-5 rounded-xl border border-black/10 dark:border-white/10">
              <div class="text-blue-500 mb-3"><i class="ri-code-ai-line text-2xl"></i></div>
              <h3 class="font-bold text-lg mb-2">AI Slave Master</h3>
              <blockquote class="italic border-l-4 border-blue-500/50 pl-4">
                "Memperbudak AI demi kemalasan yang maksimal."
              </blockquote>
              <p>
                Tidak perlu paham algoritma, cukup ketik: “Buatkan sistem autentikasi dengan dark mode dan animasi.”
              </p>
            </div>
            
            <div class="bg-black/5 dark:bg-white/5 backdrop-blur-sm p-5 rounded-xl border border-black/10 dark:border-white/10">
              <div class="text-indigo-500 mb-3"><i class="ri-calendar-todo-line text-2xl"></i></div>
              <h3 class="font-bold text-lg mb-2">Procastination Master</h3>
              <blockquote class="italic border-l-4 border-blue-500/50 pl-4">
                "Menunda adalah seni. Besok aja ngodingnya."
              </blockquote>
              <p>
                Master to-do list, tapi lebih sering nambah task: “Nanti aja.”<br/>Scroll reels 3 jam? Biasa. Deadline? Masih ada waktu... katanya.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>