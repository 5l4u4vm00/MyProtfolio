<template>
  <section id="stack">
    <div class="section-label reveal">Tech Stack</div>
    <h2 class="section-title reveal">Tools &amp; technologies</h2>
    <p class="section-desc reveal">My go-to technologies for building production-ready applications.</p>

    <div class="stack-grid">
      <div class="stack-card reveal">
        <div class="stack-icon" style="background: var(--tag-vue); color: var(--tag-vue-text);">&#9670;</div>
        <h3>Frontend</h3>
        <div class="stack-items">
          <span class="stack-item">Vue 3</span>
          <span class="stack-item">Nuxt 3</span>
          <span class="stack-item">TypeScript</span>
          <span class="stack-item">Tailwind CSS</span>
          <span class="stack-item">Pinia</span>
        </div>
      </div>
      <div class="stack-card reveal">
        <div class="stack-icon" style="background: var(--tag-python); color: var(--tag-python-text);">&#9679;</div>
        <h3>Backend</h3>
        <div class="stack-items">
          <span class="stack-item">Python</span>
          <span class="stack-item">FastAPI</span>
          <span class="stack-item">C#</span>
          <span class="stack-item">ASP.NET Core</span>
          <span class="stack-item">Node.js</span>
        </div>
      </div>
      <div class="stack-card reveal">
        <div class="stack-icon" style="background: var(--tag-db); color: var(--tag-db-text);">&#9644;</div>
        <h3>Database</h3>
        <div class="stack-items">
          <span class="stack-item">PostgreSQL</span>
          <span class="stack-item">SQL Server</span>
          <span class="stack-item">Redis</span>
          <span class="stack-item">Prisma</span>
        </div>
      </div>
      <div class="stack-card reveal">
        <div class="stack-icon" style="background: var(--tag-devops); color: var(--tag-devops-text);">&#9651;</div>
        <h3>DevOps</h3>
        <div class="stack-items">
          <span class="stack-item">Docker</span>
          <span class="stack-item">GitHub Actions</span>
          <span class="stack-item">AWS</span>
          <span class="stack-item">Vercel</span>
        </div>
      </div>
      <div class="stack-card reveal">
        <div class="stack-icon" style="background: var(--tag-ts); color: var(--tag-ts-text);">&#9733;</div>
        <h3>Testing</h3>
        <div class="stack-items">
          <span class="stack-item">Vitest</span>
          <span class="stack-item">Cypress</span>
          <span class="stack-item">Jest</span>
          <span class="stack-item">Playwright</span>
        </div>
      </div>
      <div class="stack-card reveal">
        <div class="stack-icon" style="background: var(--accent-light); color: var(--accent);">&#9881;</div>
        <h3>Other</h3>
        <div class="stack-items">
          <span class="stack-item">Git</span>
          <span class="stack-item">Linux</span>
          <span class="stack-item">REST API</span>
          <span class="stack-item">GraphQL</span>
          <span class="stack-item">Agile</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
#stack {
  max-width: var(--max-w);
  margin: 0 auto;
}

.stack-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.stack-card {
  background: var(--bg-alt);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 28px;
  transition: var(--transition);
}

.stack-card:hover {
  border-color: var(--text-muted);
  box-shadow: var(--shadow-md);
}

.stack-icon {
  width: 40px;
  height: 40px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 18px;
  margin-bottom: 16px;
  font-weight: 700;
}

.stack-card h3 {
  font-size: 16px;
  font-weight: 700;
  margin-bottom: 8px;
  letter-spacing: -0.2px;
}

.stack-items {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.stack-item {
  font-size: 13px;
  color: var(--text-secondary);
  padding: 4px 10px;
  background: var(--surface);
  border-radius: 6px;
  font-weight: 500;
}

@media (max-width: 900px) {
  .stack-grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 640px) {
  .stack-grid {
    grid-template-columns: 1fr;
  }
}
</style>
