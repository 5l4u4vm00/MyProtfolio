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

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible')
        }
      })
    },
    { threshold: 0.1, rootMargin: '0px 0px -40px 0px' },
  )

  document.querySelectorAll('.reveal').forEach((el) => observer.observe(el))
})
</script>

<template>
  <!-- NAV -->
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

  <!-- HERO -->
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

  <!-- PROJECTS -->
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

  <!-- TECH STACK -->
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

  <!-- ABOUT -->
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

  <!-- BLOG -->
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

  <!-- CONTACT -->
  <section id="contact">
    <div class="contact-box reveal">
      <div class="section-label">Get in Touch</div>
      <h2 class="section-title">Let's build something great together</h2>
      <p class="section-desc">I'm actively looking for full-stack developer roles in Australia. Whether you have a
        position open or just want to connect, I'd love to hear from you.</p>
      <div class="contact-links">
        <a href="mailto:your@email.com" class="contact-link">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
            <rect x="1" y="3" width="14" height="10" rx="2" stroke="currentColor" stroke-width="1.4" />
            <path d="M1 5l7 4 7-4" stroke="currentColor" stroke-width="1.4" stroke-linejoin="round" />
          </svg>
          Email
        </a>
        <a href="#" class="contact-link">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="currentColor">
            <path
              d="M13.6 2.4A7.95 7.95 0 002.4 13.6 7.95 7.95 0 0013.6 2.4zM8 14.4a6.36 6.36 0 01-3.2-.86V12.2c0-.72.36-1.4.96-1.8A6.24 6.24 0 018 9.6c.8 0 1.56.28 2.24.8.6.4.96 1.08.96 1.8v1.34A6.36 6.36 0 018 14.4zM8 8.4a2 2 0 110-4 2 2 0 010 4z" />
          </svg>
          LinkedIn
        </a>
        <a href="#" class="contact-link">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="currentColor">
            <path
              d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0016 8c0-4.42-3.58-8-8-8z" />
          </svg>
          GitHub
        </a>
        <a href="#" class="contact-link">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M13 1H3a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2V3a2 2 0 00-2-2z" stroke="currentColor"
              stroke-width="1.4" />
            <path d="M5 7v4M8 6v5M11 9v2" stroke="currentColor" stroke-width="1.4" stroke-linecap="round" />
          </svg>
          Resume
        </a>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <span>&copy; 2026 YourName. Built with Nuxt 3 &amp; Tailwind CSS.</span>
    <span>Made in Taiwan, heading to Australia</span>
  </footer>
</template>

<style>
:root {
  --bg: #FAFAFA;
  --bg-alt: #FFFFFF;
  --surface: #F4F4F5;
  --border: #E4E4E7;
  --text-primary: #18181B;
  --text-secondary: #52525B;
  --text-muted: #A1A1AA;
  --accent: #635BFF;
  --accent-light: #EBE9FF;
  --accent-dark: #4B45C6;
  --gradient-1: #635BFF;
  --gradient-2: #80E9FF;
  --gradient-3: #7A73FF;
  --tag-vue: #42B88320;
  --tag-vue-text: #3BA676;
  --tag-python: #30699820;
  --tag-python-text: #306998;
  --tag-dotnet: #68217A20;
  --tag-dotnet-text: #68217A;
  --tag-ts: #3178C620;
  --tag-ts-text: #3178C6;
  --tag-db: #33699920;
  --tag-db-text: #336999;
  --tag-devops: #FF613320;
  --tag-devops-text: #D94A27;
  --radius: 12px;
  --radius-sm: 8px;
  --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.04);
  --shadow-md: 0 4px 16px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 12px 40px rgba(0, 0, 0, 0.08);
  --shadow-glow: 0 0 60px rgba(99, 91, 255, 0.15);
  --transition: 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  --max-w: 1120px;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--bg);
  color: var(--text-primary);
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
  overflow-x: hidden;
}

/* --- NAV --- */
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

/* --- HERO --- */
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

@keyframes pulse {

  0%,
  100% {
    opacity: 1;
  }

  50% {
    opacity: 0.4;
  }
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

.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 14px 28px;
  border-radius: 10px;
  font-size: 15px;
  font-weight: 600;
  text-decoration: none;
  transition: var(--transition);
  cursor: pointer;
  border: none;
  font-family: inherit;
}

.btn-primary {
  background: var(--accent);
  color: #fff;
  box-shadow: 0 2px 12px rgba(99, 91, 255, 0.3);
}

.btn-primary:hover {
  background: var(--accent-dark);
  box-shadow: 0 4px 20px rgba(99, 91, 255, 0.4);
  transform: translateY(-1px);
}

.btn-secondary {
  background: var(--bg-alt);
  color: var(--text-primary);
  border: 1px solid var(--border);
}

.btn-secondary:hover {
  border-color: var(--text-muted);
  box-shadow: var(--shadow-sm);
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

@keyframes float {

  0%,
  100% {
    transform: translateY(0) scale(1);
  }

  50% {
    transform: translateY(-20px) scale(1.03);
  }
}

@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(24px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* --- SECTION COMMON --- */
section {
  padding: 100px 32px;
}

.section-label {
  font-size: 13px;
  font-weight: 600;
  color: var(--accent);
  text-transform: uppercase;
  letter-spacing: 1.5px;
  margin-bottom: 12px;
}

.section-title {
  font-family: 'Fraunces', serif;
  font-size: clamp(28px, 3.5vw, 40px);
  font-weight: 700;
  letter-spacing: -1px;
  margin-bottom: 16px;
  line-height: 1.15;
}

.section-desc {
  font-size: 16px;
  color: var(--text-secondary);
  max-width: 540px;
  line-height: 1.7;
  margin-bottom: 48px;
}

/* --- PROJECTS --- */
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

.mock-dot:nth-child(1) {
  background: #FF5F57;
}

.mock-dot:nth-child(2) {
  background: #FEBC2E;
}

.mock-dot:nth-child(3) {
  background: #28C840;
}

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

.mock-line:nth-child(1) {
  width: 60%;
}

.mock-line:nth-child(2) {
  width: 90%;
}

.mock-line:nth-child(3) {
  width: 45%;
}

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

.tag {
  padding: 4px 10px;
  border-radius: 6px;
  font-size: 12px;
  font-weight: 600;
  font-family: 'JetBrains Mono', monospace;
}

.tag-vue {
  background: var(--tag-vue);
  color: var(--tag-vue-text);
}

.tag-python {
  background: var(--tag-python);
  color: var(--tag-python-text);
}

.tag-dotnet {
  background: var(--tag-dotnet);
  color: var(--tag-dotnet-text);
}

.tag-ts {
  background: var(--tag-ts);
  color: var(--tag-ts-text);
}

.tag-db {
  background: var(--tag-db);
  color: var(--tag-db-text);
}

.tag-devops {
  background: var(--tag-devops);
  color: var(--tag-devops-text);
}

.project-links {
  display: flex;
  gap: 10px;
}

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-size: 13px;
  font-weight: 600;
  color: var(--accent);
  text-decoration: none;
  padding: 6px 14px;
  border-radius: var(--radius-sm);
  border: 1px solid var(--accent-light);
  transition: var(--transition);
}

.project-link:hover {
  background: var(--accent-light);
}

/* --- TECH STACK --- */
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

/* --- ABOUT --- */
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

/* --- BLOG --- */
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

/* --- CONTACT --- */
#contact {
  max-width: var(--max-w);
  margin: 0 auto;
}

.contact-box {
  background: var(--text-primary);
  border-radius: 20px;
  padding: 64px;
  color: #fff;
  position: relative;
  overflow: hidden;
}

.contact-box::before {
  content: '';
  position: absolute;
  top: -100px;
  right: -100px;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(99, 91, 255, 0.3), transparent 65%);
  pointer-events: none;
}

.contact-box .section-label {
  color: var(--gradient-2);
}

.contact-box .section-title {
  color: #fff;
}

.contact-box .section-desc {
  color: rgba(255, 255, 255, 0.65);
}

.contact-links {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  position: relative;
  z-index: 1;
}

.contact-link {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 14px 24px;
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.15);
  color: #fff;
  text-decoration: none;
  font-size: 14px;
  font-weight: 500;
  transition: var(--transition);
  backdrop-filter: blur(10px);
  background: rgba(255, 255, 255, 0.05);
}

.contact-link:hover {
  background: rgba(255, 255, 255, 0.12);
  border-color: rgba(255, 255, 255, 0.3);
  transform: translateY(-2px);
}

/* --- FOOTER --- */
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

/* --- MOBILE NAV --- */
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

/* --- RESPONSIVE --- */
@media (max-width: 900px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }

  .project-card.featured {
    grid-column: span 1;
    grid-template-columns: 1fr;
  }

  .stack-grid {
    grid-template-columns: 1fr 1fr;
  }

  .blog-grid {
    grid-template-columns: 1fr;
  }

  .about-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .hero-visual {
    display: none;
  }

  .contact-box {
    padding: 40px 28px;
  }
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

  .stack-grid {
    grid-template-columns: 1fr;
  }

  section {
    padding: 64px 20px;
  }

  .hero {
    padding: 130px 20px 60px;
  }

  footer {
    flex-direction: column;
    gap: 8px;
    text-align: center;
  }
}

/* --- SCROLL REVEAL --- */
.reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.7s ease, transform 0.7s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
</style>
