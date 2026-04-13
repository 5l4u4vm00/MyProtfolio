<template>
  <section id="about">
    <div class="section-label reveal">About Me</div>
    <h2 class="section-title reveal">A developer who cares about the craft</h2>

    <div class="about-grid">
      <div class="about-text reveal">
        <p>I'm a full-stack developer with a passion for building clean, scalable web applications. My experience spans
          across frontend frameworks like Vue.js and backend technologies including Python and .NET.</p>
        <p>I believe great software comes from understanding both the technical architecture and the people who use it.
          I write code that's maintainable, testable, and built to last.</p>
        <p>Currently seeking full-stack opportunities in Australia, where I can contribute to innovative teams and grow
          alongside passionate engineers.</p>
      </div>
      <div class="about-highlights reveal">
        <div class="highlight-card">
          <div class="highlight-icon">&#9889;</div>
          <div>
            <h4>Full-Stack Capability</h4>
            <p>From pixel-perfect UIs to robust API design and database architecture — I own the entire stack.</p>
          </div>
        </div>
        <div class="highlight-card">
          <div class="highlight-icon">&#9881;</div>
          <div>
            <h4>Production Mindset</h4>
            <p>CI/CD pipelines, testing, monitoring, and documentation are part of my standard workflow, not
              afterthoughts.</p>
          </div>
        </div>
        <div class="highlight-card">
          <div class="highlight-icon">&#9734;</div>
          <div>
            <h4>Continuous Learner</h4>
            <p>Actively exploring AI integration, cloud architecture, and modern development patterns to stay ahead of
              the curve.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
#about {
  max-width: var(--max-w);
  margin: 0 auto;
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 60px;
  align-items: start;
}

.about-text p {
  font-size: 16px;
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 20px;
}

.about-highlights {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.highlight-card {
  display: flex;
  gap: 16px;
  padding: 20px;
  background: var(--bg-alt);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  transition: var(--transition);
}

.highlight-card:hover {
  border-color: var(--text-muted);
}

.highlight-icon {
  width: 44px;
  height: 44px;
  border-radius: 10px;
  background: var(--accent-light);
  color: var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  flex-shrink: 0;
}

.highlight-card h4 {
  font-size: 15px;
  font-weight: 700;
  margin-bottom: 4px;
}

.highlight-card p {
  font-size: 13px;
  color: var(--text-secondary);
  line-height: 1.6;
}

@media (max-width: 900px) {
  .about-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}
</style>
