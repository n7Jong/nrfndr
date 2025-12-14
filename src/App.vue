<template>
  <div class="min-h-screen bg-background relative">
    <!-- Video Background -->
    <div class="fixed inset-0 z-0 overflow-hidden">
      <video 
        autoplay 
        muted 
        loop 
        playsinline
        class="absolute min-w-full min-h-full w-auto h-auto object-cover"
      >
        <source src="https://res.cloudinary.com/YOUR-CLOUD-NAME/video/upload/YOUR-VIDEO.mp4" type="video/mp4">
        <!-- Fallback for browsers that don't support video -->
        Your browser does not support the video tag.
      </video>
      <!-- Dark overlay for better text readability -->
      <div class="absolute inset-0 bg-black/60"></div>
    </div>
    
    <!-- Content -->
    <div class="relative z-10">
      <Navigation />
      <Hero />
      <Music />
      <Tour />
      <Gallery />
      <About />
      <Contact />
    </div>
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
