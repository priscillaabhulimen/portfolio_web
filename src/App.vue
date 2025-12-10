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

      const id = link.getAttribute('href')?.slice(1)
      const target = document.getElementById(id)

      target?.scrollIntoView({ behavior: 'smooth' })
  target?.focus({ preventScroll: true })
    })
  })
})
</script>

<template>
  <a href="#about" class="sr-only focus:not-sr-only fixed top-2 left-2 bg-black text-white p-2 z-[100]">
    Skip to content
  </a>
  <Navbar />
  <Hero />
  <Work />
  <Projects />
  <Contact />
</template>