<template>
  <section id="merch" class="relative py-28 bg-grid overflow-hidden">
    <!-- Background elements -->
    <div class="absolute inset-0 z-0">
      <div class="absolute -top-20 right-20 w-80 h-80 bg-purple-500/10 rounded-full blur-[90px]"></div>
      <div class="absolute bottom-40 -left-20 w-72 h-72 bg-blue-500/10 rounded-full blur-[100px]"></div>
    </div>
    
    <!-- Section content -->
    <div class="container mx-auto px-6 relative z-10">
      <!-- Section header -->
      <div class="mb-16 text-center">
        <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 animate-in fade-in slide-in-from-bottom-5 duration-700">
          Merchandise
        </h2>
        <div class="w-20 h-1 bg-gradient-to-r from-blue-400 to-indigo-500 mx-auto rounded-full"></div>
        <p class="mt-6 max-w-2xl mx-auto text-lg">
          Official Merchandise IMPHNEN. Dapatkan merchandise kami di Shopee.
        </p>
      </div>
      
      <!-- Merchandise grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Merchandise cards -->
        <div v-for="(item, index) in merchandiseItems" :key="index" 
             class="bg-black/5 dark:bg-white/5 backdrop-blur-sm rounded-xl border border-black/10 dark:border-white/10 overflow-hidden animate-in fade-in slide-in-from-bottom-5 duration-700 transition-all hover:shadow-lg hover:shadow-purple-500/10 group"
             :style="{ animationDelay: `${index * 100}ms` }">
          <div class="relative">
            <img :src="item.image" :alt="item.title" class="w-full h-60 object-cover transition-opacity duration-300" />
            <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
              <a :href="item.shopeeLink || '#'" target="_blank" rel="noopener noreferrer"
                 class="rounded-full bg-orange-500 hover:bg-orange-600 text-white px-6 py-3 flex items-center gap-2 transition-colors duration-300">
                <i class="ri-shopping-bag-3-line"></i>
                <span>Beli di Shopee</span>
              </a>
            </div>
            <span v-if="item.discount" 
                  class="absolute top-3 right-3 text-xs px-3 py-1 rounded-full bg-orange-500 text-white font-medium">
              {{ item.discount }}
            </span>
          </div>
          
          <div class="p-6">
            <!-- Price tag - simplified version -->
            <div class="flex justify-between items-start mb-4">
              <h3 class="text-xl font-bold line-clamp-2 pr-4 flex-1" :title="item.title">
                {{ item.title }}
              </h3>
              <span class="text-lg font-bold text-blue-500 dark:text-blue-400 whitespace-nowrap">
                {{ item.price }}
              </span>
            </div>
            
            <p class="text-current/70 mb-4 line-clamp-3 h-[4.5rem]">{{ item.description }}</p>
            
            <div class="flex items-center gap-2 mt-auto">
              <span class="text-xs px-3 py-1 rounded-full bg-black/5 dark:bg-white/5">
                {{ item.category }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const merchandiseItems = [
  {
    title: "OFFICIAL LAST MERCHANDISE IMPHNEN 2025",
    price: "Rp 325.000",
    description: "Kami hadirkan exclusive merchandise terakhir dari IMPHNEN di tahun ini—ini last call banget buat kalian yang hobinya bilang \"ntar mulai ngoding\" tapi ujung-ujungnya cuma scroll Facebook sampe pagi. Pre-order sekarang, stoknya super limited dan gak ada restock buat yang telat gerak. Pilih paketmu sekarang, atau siap-siap nyesel sambil stalking postingan grup FB!",
    image: "https://down-id.img.susercontent.com/file/id-11134207-7rbkd-m7v43qo1x8pce8.webp",
    category: "Apparel",
    shopeeLink: "https://s.shopee.co.id/7AQBRP5CbI"
  },
  {
    title: "Official Paket 4 Last Merchandise IMPHNEN 2025",
    price: "Rp 550.000",
    description: "Yang katanya cuma mau Apparelnya aja, gass sikat.",
    image: "https://down-id.img.susercontent.com/file/id-11134207-7rbk3-m7xcvcwlqgem19.webp",
    category: "Apparel",
    shopeeLink: "https://s.shopee.co.id/3VWt4upwWm"
  },
  {
    title: "Official Paket 5 Last Merchandise IMPHNEN 2025",
    price: "Rp 200.000",
    description: "Yang katanya udah punya Apparel tahun lalu, tapi pengen merchandisenya doang, sikattt.",
    image: "https://down-id.img.susercontent.com/file/id-11134207-7rbka-m7xcvcwlw2oe0e.webp",
    category: "Aksesoris",
    shopeeLink: "https://s.shopee.co.id/60EE3XsxEm"
  },
  {
    title: "Official Paket 6 Last Merchandise IMPHNEN 2025",
    price: "Rp 575.000",
    description: "Yang katanya pengen Hoddie plus Longsleeve Gasskeun.",
    image: "https://down-id.img.susercontent.com/file/id-11134207-7rbke-m82zo2pxz9qaba.webp",
    category: "Apparel",
    shopeeLink: "https://s.shopee.co.id/9f7WQg9Rrp"
  },
  {
    title: "OFFICIAL Merch IMPHNEN 2024",
    price: "Rp 175.000",
    description: "Yo, bro sis! Akhirnya merch pertama dari komunitas paling relate sejagat Facebook: IMPHNEN (Ingin Menjadi Programmer Handal Namun Enggan Ngoding). Cocok buat kamu yang pengen tampil kece tanpa harus ngoding berlebihan.",
    image: "https://down-id.img.susercontent.com/file/id-11134207-7rasa-m2z0j9avytw5e9.webp",
    category: "Apparel",
    discount: "Best Seller",
    shopeeLink: "https://s.shopee.co.id/5KyXGeIh0h"
  },
  {
    title: "Official Mini Merch IMPHNEN",
    price: "Rp 90.000",
    description: "MINI MERCH BUNDLING MALES-NGODING LEGEND udah READY!\nBuat lo yang mau flex merch keren, tapi urusan ngoding… yaudah gapapa, kita saling mengerti :3",
    image: "https://down-id.img.susercontent.com/file/id-11134207-7rasi-m5qx623qjtom80.webp",
    category: "Aksesoris",
    shopeeLink: "https://s.shopee.co.id/9zkMonp5Tl"
  },//2
];
</script>