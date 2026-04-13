<script setup lang="ts">
const navOpen = ref(false)

function toggleNav() {
  navOpen.value = !navOpen.value
}

function scrollTo(href: string) {
  const target = document.querySelector(href)
  if (target) {
    target.scrollIntoView({ behavior: 'smooth', block: 'start' })
    navOpen.value = false
  }
}
</script>

<template>
  <nav>
    <div class="nav-inner">
      <a href="#" class="nav-logo" @click.prevent>Yi Hsuan Chao<span>.</span></a>
      <button class="nav-toggle" aria-label="Menu" @click="toggleNav">
        <svg viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round">
          <line x1="3" y1="6" x2="21" y2="6" />
          <line x1="3" y1="12" x2="21" y2="12" />
          <line x1="3" y1="18" x2="21" y2="18" />
        </svg>
      </button>
      <div class="nav-links" :class="{ open: navOpen }">
        <a href="#projects" @click.prevent="scrollTo('#projects')">Projects</a>
        <a href="#stack" @click.prevent="scrollTo('#stack')">Tech Stack</a>
        <a href="#about" @click.prevent="scrollTo('#about')">About</a>
        <a href="#blog" @click.prevent="scrollTo('#blog')">Blog</a>
        <a href="#contact" class="nav-cta" @click.prevent="scrollTo('#contact')">Get in Touch</a>
      </div>
    </div>
  </nav>
</template>

<style scoped>
nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  background: rgba(250, 250, 250, 0.82);
  backdrop-filter: blur(20px) saturate(1.4);
  -webkit-backdrop-filter: blur(20px) saturate(1.4);
  border-bottom: 1px solid var(--border);
  transition: var(--transition);
}

.nav-inner {
  max-width: var(--max-w);
  margin: 0 auto;
  padding: 0 32px;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  font-family: 'Fraunces', serif;
  font-weight: 700;
  font-size: 22px;
  color: var(--text-primary);
  text-decoration: none;
  letter-spacing: -0.5px;
}

.nav-logo span {
  color: var(--accent);
}

.nav-links {
  display: flex;
  gap: 32px;
  align-items: center;
}

.nav-links a {
  text-decoration: none;
  color: var(--text-secondary);
  font-size: 14px;
  font-weight: 500;
  transition: var(--transition);
  position: relative;
}

.nav-links a:hover {
  color: var(--text-primary);
}

.nav-links a::after {
  content: '';
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 2px;
  background: var(--accent);
  transition: var(--transition);
  border-radius: 1px;
}

.nav-links a:hover::after {
  width: 100%;
}

.nav-cta {
  background: var(--text-primary) !important;
  color: #fff !important;
  padding: 8px 20px !important;
  border-radius: 8px !important;
  font-size: 14px !important;
  font-weight: 500 !important;
  transition: var(--transition) !important;
}

.nav-cta::after {
  display: none !important;
}

.nav-cta:hover {
  opacity: 0.85;
}

.nav-toggle {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px;
}

.nav-toggle svg {
  width: 24px;
  height: 24px;
  stroke: var(--text-primary);
}

@media (max-width: 640px) {
  .nav-links {
    display: none;
  }

  .nav-links.open {
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 64px;
    left: 0;
    right: 0;
    background: var(--bg-alt);
    border-bottom: 1px solid var(--border);
    padding: 20px 32px;
    gap: 16px;
    box-shadow: var(--shadow-md);
  }

  .nav-toggle {
    display: block;
  }
}
</style>
