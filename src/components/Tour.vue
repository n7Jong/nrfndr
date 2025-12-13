<template>
  <section id="tour" class="py-24 px-6 lg:px-12">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl font-bold mb-16 text-center tracking-wider uppercase">Tour Dates</h2>
      <div class="bg-card border border-border">
        <div 
          v-for="(show, index) in shows" 
          :key="index"
          class="border-b border-border last:border-b-0 p-5 flex flex-col md:flex-row md:items-center justify-between gap-4 hover:bg-muted/30 transition-colors"
        >
          <div class="flex flex-col md:flex-row md:items-center gap-4 md:gap-8 flex-1">
            <div class="flex items-center gap-3 text-sm text-muted-foreground">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/>
              </svg>
              <span class="font-medium">{{ show.date }}</span>
            </div>
            <div class="flex-1">
              <h3 class="text-base font-semibold mb-1">{{ show.venue }}</h3>
              <div class="flex items-center gap-2 text-sm text-muted-foreground">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
                </svg>
                <span>{{ show.location }}</span>
              </div>
            </div>
          </div>
          <button 
            :class="[
              'px-6 py-2 text-xs font-medium tracking-wider uppercase transition-colors',
              show.soldOut 
                ? 'bg-muted text-muted-foreground cursor-not-allowed' 
                : 'border border-white text-white hover:bg-white hover:text-background'
            ]"
            :disabled="show.soldOut"
          >
            {{ show.soldOut ? 'Sold Out' : 'Tickets' }}
          </button>
        </div>
      </div>
      <div class="text-center mt-8">
        <p class="text-xs text-muted-foreground">
          Book <span class="font-semibold">NRFNDR</span> for your event →
        </p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const shows = ref([
  { date: 'SOON', venue: 'El Union Coffee Shop', location: 'Baguio City', soldOut: true },
])
</script>
   