<script setup lang="ts">
import { useScrollReveal } from '~/composables/useScrollReveal'
useScrollReveal()
</script>

<template>
  <AppNav />
  <HeroSection />
  <ProjectsSection />
  <TechStackSection />
  <AboutSection />
  <BlogSection />
  <ContactSection />
  <AppFooter />
</template>
