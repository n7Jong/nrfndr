<template>
  <section id="music" class="py-24 px-6 lg:px-12 bg-black/20">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-4xl font-bold mb-16 text-center tracking-wider uppercase">Music</h2>
      <div class="grid grid-cols-2 lg:grid-cols-4 gap-6 mb-12">
        <div 
          v-for="(album, index) in albums" 
          :key="index"
          class="group cursor-pointer"
        >
          <div class="aspect-square bg-muted border border-border mb-4 flex items-center justify-center group-hover:border-white/50 transition-colors">
            <span class="text-muted-foreground/30 text-xs">Album Cover</span>
          </div>
          <h3 class="text-sm font-semibold mb-1">{{ album.title }}</h3>
          <p class="text-xs text-muted-foreground">{{ album.type }}</p>
          <p class="text-xs text-muted-foreground">{{ album.year }}</p>
        </div>
      </div>
      <div class="text-center">
        <button class="px-10 py-2.5 border border-white text-white text-xs font-medium tracking-wider uppercase hover:bg-white hover:text-background transition-colors">
          View All Releases
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const albums = ref([
  { title: 'Nocturnal Echoes', type: 'Album', year: '2024' },
  { title: 'Digital Dreams', type: 'EP', year: '2023' },
  { title: 'Infinite Horizons', type: 'Album', year: '2023' },
  { title: 'Sunset Frequencies', type: 'Single', year: '2022' },
])
</script>
