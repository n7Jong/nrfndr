<template>
  <section id="gallery" class="py-24 px-6 lg:px-12 bg-black/20">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-4xl font-bold mb-16 text-center tracking-wider uppercase">Gallery</h2>
      <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <div 
          v-for="i in 8" 
          :key="i"
          class="aspect-square bg-muted border border-border hover:border-white/50 transition-colors cursor-pointer overflow-hidden group"
        >
          <div class="w-full h-full flex items-center justify-center text-muted-foreground/30 group-hover:text-muted-foreground/50 transition-colors">
            <span class="text-xs">Image {{ i }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Gallery component
</script>
