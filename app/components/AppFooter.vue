<template>
  <footer>
    <span>&copy; 2026 YourName. Built with Nuxt 3 &amp; Tailwind CSS.</span>
    <span>Made in Taiwan, heading to Australia</span>
  </footer>
</template>

<style scoped>
footer {
  max-width: var(--max-w);
  margin: 0 auto;
  padding: 32px 32px 48px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: var(--text-muted);
  font-size: 13px;
}

@media (max-width: 640px) {
  footer {
    flex-direction: column;
    gap: 8px;
    text-align: center;
  }
}
</style>
