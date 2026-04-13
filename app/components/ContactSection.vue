<template>
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
</template>

<style scoped>
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

@media (max-width: 900px) {
  .contact-box {
    padding: 40px 28px;
  }
}
</style>
