<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-background border-b border-border">
    <div class="max-w-7xl mx-auto px-6 lg:px-12 py-5 flex items-center justify-between">
      <a href="#" class="text-xl font-bold tracking-wider">NRFNDR</a>
      <div class="hidden md:flex gap-10 text-sm font-medium tracking-wide">
        <a href="#" class="hover:text-white/70 transition-colors uppercase">Home</a>
        <a href="#about" class="hover:text-white/70 transition-colors uppercase">About</a>
        <a href="#music" class="hover:text-white/70 transition-colors uppercase">Music</a>
        <a href="#gallery" class="hover:text-white/70 transition-colors uppercase">Gallery</a>
        <a href="#contact" class="hover:text-white/70 transition-colors uppercase">Contact</a>
      </div>
      <button 
        @click="toggleMenu"
        class="md:hidden p-2"
        aria-label="Toggle menu"
      >
        <svg 
          class="w-6 h-6" 
          fill="none" 
          stroke="currentColor" 
          viewBox="0 0 24 24"
        >
          <path 
            stroke-linecap="round" 
            stroke-linejoin="round" 
            stroke-width="2" 
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
      </button>
    </div>
    <div v-if="isMenuOpen" class="md:hidden border-t border-border bg-background">
      <div class="px-6 py-4 flex flex-col gap-4 text-sm font-medium">
        <a href="#" class="hover:text-white/70 transition-colors uppercase">Home</a>
        <a href="#about" class="hover:text-white/70 transition-colors uppercase">About</a>
        <a href="#music" class="hover:text-white/70 transition-colors uppercase">Music</a>
        <a href="#tour" class="hover:text-white/70 transition-colors uppercase">Tour</a>
        <a href="#gallery" class="hover:text-white/70 transition-colors uppercase">Gallery</a>
        <a href="#contact" class="hover:text-white/70 transition-colors uppercase">Contact</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>
