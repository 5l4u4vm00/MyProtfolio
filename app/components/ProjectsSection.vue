<template>
  <section id="projects">
    <div class="section-label reveal">Selected Work</div>
    <h2 class="section-title reveal">Projects I've built</h2>
    <p class="section-desc reveal">Each project represents a real-world problem solved with modern technologies and best
      practices.</p>

    <div class="projects-grid">
      <!-- Featured Project -->
      <div class="project-card featured reveal">
        <div class="project-preview">
          <div class="project-preview-mock">
            <div class="mock-topbar"><span class="mock-dot"></span><span class="mock-dot"></span><span
                class="mock-dot"></span></div>
            <div class="mock-body">
              <div class="mock-sidebar">
                <div class="mock-sidebar-item"></div>
                <div class="mock-sidebar-item"></div>
                <div class="mock-sidebar-item"></div>
                <div class="mock-sidebar-item"></div>
              </div>
              <div class="mock-content">
                <div class="mock-line"></div>
                <div class="mock-line"></div>
                <div class="mock-line"></div>
                <div class="mock-cards">
                  <div class="mock-card-item"></div>
                  <div class="mock-card-item"></div>
                  <div class="mock-card-item"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="project-info">
          <div class="project-number">01 — Featured Project</div>
          <h3>TaskFlow — SaaS Project Management</h3>
          <p>A multi-tenant project management platform with real-time collaboration, Kanban boards, Gantt charts, team
            analytics, and role-based access control.</p>
          <div class="project-tags">
            <span class="tag tag-vue">Nuxt 3</span>
            <span class="tag tag-python">FastAPI</span>
            <span class="tag tag-ts">TypeScript</span>
            <span class="tag tag-db">PostgreSQL</span>
            <span class="tag tag-devops">Docker</span>
          </div>
          <div class="project-links">
            <a href="#" class="project-link">
              <svg width="14" height="14" viewBox="0 0 16 16" fill="none">
                <circle cx="8" cy="8" r="6.5" stroke="currentColor" stroke-width="1.5" />
                <path d="M3 8h10" stroke="currentColor" stroke-width="1.5" />
                <ellipse cx="8" cy="8" rx="3" ry="6.5" stroke="currentColor" stroke-width="1.5" />
              </svg>
              Live Demo
            </a>
            <a href="#" class="project-link">
              <svg width="14" height="14" viewBox="0 0 16 16" fill="currentColor">
                <path
                  d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0016 8c0-4.42-3.58-8-8-8z" />
              </svg>
              Source Code
            </a>
          </div>
        </div>
      </div>

      <!-- Project 2 -->
      <div class="project-card reveal">
        <div class="project-preview">
          <div class="project-preview-mock">
            <div class="mock-topbar"><span class="mock-dot"></span><span class="mock-dot"></span><span
                class="mock-dot"></span></div>
            <div class="mock-body">
              <div class="mock-content">
                <div class="mock-line" style="width:50%"></div>
                <div class="mock-line" style="width:80%"></div>
                <div class="mock-cards">
                  <div class="mock-card-item"></div>
                  <div class="mock-card-item"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="project-info">
          <div class="project-number">02</div>
          <h3>Enterprise HR System</h3>
          <p>A comprehensive HR management platform with employee onboarding, leave management, payroll integration, and
            reporting dashboards.</p>
          <div class="project-tags">
            <span class="tag tag-vue">Vue 3</span>
            <span class="tag tag-dotnet">ASP.NET Core</span>
            <span class="tag tag-db">SQL Server</span>
          </div>
          <div class="project-links">
            <a href="#" class="project-link">Live Demo</a>
            <a href="#" class="project-link">Source Code</a>
          </div>
        </div>
      </div>

      <!-- Project 3 -->
      <div class="project-card reveal">
        <div class="project-preview">
          <div class="project-preview-mock">
            <div class="mock-topbar"><span class="mock-dot"></span><span class="mock-dot"></span><span
                class="mock-dot"></span></div>
            <div class="mock-body">
              <div class="mock-content">
                <div class="mock-line" style="width:70%"></div>
                <div class="mock-line" style="width:40%; background: var(--accent-light)"></div>
                <div class="mock-line" style="width:90%"></div>
                <div class="mock-cards" style="margin-top:auto">
                  <div class="mock-card-item" style="background: var(--accent-light)"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="project-info">
          <div class="project-number">03</div>
          <h3>AI Document Assistant</h3>
          <p>An intelligent document analysis tool powered by LLM APIs with streaming responses, PDF parsing, and smart
            summarization.</p>
          <div class="project-tags">
            <span class="tag tag-vue">Nuxt 3</span>
            <span class="tag tag-python">Python</span>
            <span class="tag tag-ts">TypeScript</span>
          </div>
          <div class="project-links">
            <a href="#" class="project-link">Live Demo</a>
            <a href="#" class="project-link">Source Code</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
#projects {
  max-width: var(--max-w);
  margin: 0 auto;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
}

.project-card {
  background: var(--bg-alt);
  border-radius: var(--radius);
  border: 1px solid var(--border);
  overflow: hidden;
  transition: var(--transition);
  cursor: pointer;
  position: relative;
}

.project-card:hover {
  border-color: var(--text-muted);
  box-shadow: var(--shadow-lg);
  transform: translateY(-4px);
}

.project-card.featured {
  grid-column: span 2;
  display: grid;
  grid-template-columns: 1.1fr 1fr;
}

.project-preview {
  aspect-ratio: 16/10;
  background: var(--surface);
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.featured .project-preview {
  aspect-ratio: auto;
  min-height: 360px;
}

.project-preview-mock {
  width: 85%;
  height: 72%;
  border-radius: 8px;
  background: var(--bg-alt);
  border: 1px solid var(--border);
  box-shadow: var(--shadow-md);
  position: relative;
  overflow: hidden;
}

.mock-topbar {
  height: 32px;
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  display: flex;
  align-items: center;
  padding: 0 12px;
  gap: 6px;
}

.mock-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
}

.mock-dot:nth-child(1) { background: #FF5F57; }
.mock-dot:nth-child(2) { background: #FEBC2E; }
.mock-dot:nth-child(3) { background: #28C840; }

.mock-body {
  padding: 14px;
  display: flex;
  gap: 10px;
  height: calc(100% - 32px);
}

.mock-sidebar {
  width: 50px;
  background: var(--surface);
  border-radius: 6px;
  display: flex;
  flex-direction: column;
  gap: 8px;
  padding: 8px 6px;
  align-items: center;
}

.mock-sidebar-item {
  width: 28px;
  height: 28px;
  border-radius: 6px;
  background: var(--border);
}

.mock-sidebar-item:first-child {
  background: var(--accent-light);
}

.mock-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.mock-line {
  height: 8px;
  border-radius: 4px;
  background: var(--surface);
}

.mock-line:nth-child(1) { width: 60%; }
.mock-line:nth-child(2) { width: 90%; }
.mock-line:nth-child(3) { width: 45%; }

.mock-cards {
  display: flex;
  gap: 6px;
  margin-top: 8px;
  flex: 1;
}

.mock-card-item {
  flex: 1;
  background: var(--surface);
  border-radius: 6px;
  border: 1px solid var(--border);
}

.project-info {
  padding: 28px;
}

.project-number {
  font-family: 'JetBrains Mono', monospace;
  font-size: 12px;
  color: var(--text-muted);
  margin-bottom: 10px;
  font-weight: 500;
}

.project-info h3 {
  font-size: 20px;
  font-weight: 700;
  margin-bottom: 10px;
  letter-spacing: -0.3px;
}

.project-info p {
  font-size: 14px;
  color: var(--text-secondary);
  line-height: 1.65;
  margin-bottom: 18px;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  margin-bottom: 20px;
}

.project-links {
  display: flex;
  gap: 10px;
}

@media (max-width: 900px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }

  .project-card.featured {
    grid-column: span 1;
    grid-template-columns: 1fr;
  }
}
</style>
