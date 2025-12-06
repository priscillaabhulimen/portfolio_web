<script setup>

import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Work from './components/Work.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'

import { onMounted } from 'vue'

onMounted(() => {
  const navLinks = document.querySelectorAll('nav a')

  navLinks.forEach(link => {
    link.addEventListener('click', (e) => {
      e.preventDefault()
      const targetId = link.getAttribute('href').substring(1)
      const targetElement = document.getElementById(targetId)

      if (targetElement) {
        targetElement.scrollIntoView({ behavior: 'smooth' })
      }
    })
  })
})
</script>

<template>
  <Navbar />
  <Hero />
  <Work />
  <Projects />
  <Contact />
  <a href="#about" class="sr-only focus:not-sr-only fixed top-2 left-2 bg-black text-white p-2">
    Skip to content
  </a>
</template>