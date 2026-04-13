<template>
  <section id="blog">
    <div class="section-label reveal">Blog</div>
    <h2 class="section-title reveal">Writing &amp; thinking</h2>
    <p class="section-desc reveal">Sharing what I learn along the way — technical deep-dives, architecture decisions,
      and lessons from the field.</p>

    <div class="blog-grid">
      <a href="#" class="blog-card reveal">
        <div class="blog-date">2026-04-08</div>
        <h3>Designing Multi-Tenant Architecture with FastAPI &amp; PostgreSQL</h3>
        <p>How I structured a SaaS application to support multiple tenants with isolated data, shared infrastructure,
          and row-level security.</p>
        <span class="blog-read">Read article →</span>
      </a>
      <a href="#" class="blog-card reveal">
        <div class="blog-date">2026-03-22</div>
        <h3>Real-Time Collaboration in Vue 3 with WebSockets</h3>
        <p>Building a collaborative Kanban board with optimistic UI updates, conflict resolution, and smooth state
          synchronization.</p>
        <span class="blog-read">Read article →</span>
      </a>
      <a href="#" class="blog-card reveal">
        <div class="blog-date">2026-03-10</div>
        <h3>Integrating LLM APIs: Streaming, Caching &amp; Cost Control</h3>
        <p>Practical patterns for building AI-powered features — from handling streaming responses to managing token
          budgets in production.</p>
        <span class="blog-read">Read article →</span>
      </a>
    </div>
  </section>
</template>

<style scoped>
#blog {
  max-width: var(--max-w);
  margin: 0 auto;
}

.blog-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.blog-card {
  background: var(--bg-alt);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 28px;
  transition: var(--transition);
  text-decoration: none;
  color: inherit;
  display: flex;
  flex-direction: column;
}

.blog-card:hover {
  border-color: var(--text-muted);
  box-shadow: var(--shadow-md);
  transform: translateY(-2px);
}

.blog-date {
  font-family: 'JetBrains Mono', monospace;
  font-size: 12px;
  color: var(--text-muted);
  margin-bottom: 12px;
}

.blog-card h3 {
  font-size: 17px;
  font-weight: 700;
  margin-bottom: 10px;
  letter-spacing: -0.2px;
  line-height: 1.35;
}

.blog-card p {
  font-size: 13px;
  color: var(--text-secondary);
  line-height: 1.65;
  flex: 1;
}

.blog-read {
  margin-top: 16px;
  font-size: 13px;
  font-weight: 600;
  color: var(--accent);
  display: inline-flex;
  align-items: center;
  gap: 4px;
}

@media (max-width: 900px) {
  .blog-grid {
    grid-template-columns: 1fr;
  }
}
</style>
