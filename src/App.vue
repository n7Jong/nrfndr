<template>
  <div class="min-h-screen bg-background">
    <Navigation />
    <Hero />
    <Music />
    <Tour />
    <Gallery />
    <About />
    <Contact />
  </div>
</template>

<script setup>
import Navigation from './components/Navigation.vue'
import Hero from './components/Hero.vue'
import Music from './components/Music.vue'
import Tour from './components/Tour.vue'
import Gallery from './components/Gallery.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
</script>
