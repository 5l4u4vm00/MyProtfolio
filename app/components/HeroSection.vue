<script setup lang="ts">
function scrollTo(href: string) {
  const target = document.querySelector(href)
  if (target) {
    target.scrollIntoView({ behavior: 'smooth', block: 'start' })
  }
}
</script>

<template>
  <section class="hero">
    <div class="hero-badge"><span class="dot"></span> Open to work in Australia</div>
    <h1>
      Building modern web<br>
      experiences with<br>
      <span class="gradient-text">precision &amp; craft</span>
    </h1>
    <p class="hero-desc">
      Full-Stack Developer specializing in Vue.js, Python, and .NET — crafting performant, scalable applications with
      clean architecture and thoughtful design.
    </p>
    <div class="hero-actions">
      <a href="#projects" class="btn btn-primary" @click.prevent="scrollTo('#projects')">
        View Projects
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
          <path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"
            stroke-linejoin="round" />
        </svg>
      </a>
      <a href="#contact" class="btn btn-secondary" @click.prevent="scrollTo('#contact')">
        Contact Me
      </a>
    </div>
    <div class="hero-visual"></div>
  </section>
</template>

<style scoped>
.hero {
  padding: 160px 32px 100px;
  max-width: var(--max-w);
  margin: 0 auto;
  position: relative;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 6px 14px;
  border-radius: 100px;
  background: var(--accent-light);
  color: var(--accent);
  font-size: 13px;
  font-weight: 600;
  margin-bottom: 28px;
  animation: fadeUp 0.8s ease both;
}

.hero-badge .dot {
  width: 7px;
  height: 7px;
  background: var(--accent);
  border-radius: 50%;
  animation: pulse 2s infinite;
}

.hero h1 {
  font-family: 'Fraunces', serif;
  font-size: clamp(42px, 5.5vw, 68px);
  font-weight: 700;
  line-height: 1.08;
  letter-spacing: -2px;
  color: var(--text-primary);
  margin-bottom: 24px;
  animation: fadeUp 0.8s ease 0.1s both;
}

.hero h1 .gradient-text {
  background: linear-gradient(135deg, var(--gradient-1), var(--gradient-2), var(--gradient-3));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-desc {
  font-size: 18px;
  color: var(--text-secondary);
  max-width: 520px;
  line-height: 1.7;
  margin-bottom: 40px;
  animation: fadeUp 0.8s ease 0.2s both;
}

.hero-actions {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  animation: fadeUp 0.8s ease 0.3s both;
}

.hero-visual {
  position: absolute;
  right: -60px;
  top: 100px;
  width: 420px;
  height: 420px;
  background: radial-gradient(circle at 30% 40%, rgba(99, 91, 255, 0.12), transparent 60%),
    radial-gradient(circle at 70% 60%, rgba(128, 233, 255, 0.1), transparent 50%);
  border-radius: 50%;
  filter: blur(60px);
  pointer-events: none;
  animation: float 8s ease-in-out infinite;
}

@media (max-width: 900px) {
  .hero-visual {
    display: none;
  }
}

@media (max-width: 640px) {
  .hero {
    padding: 130px 20px 60px;
  }
}
</style>
