
<style>
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Syne:wght@400;500;700;800&display=swap');

* { margin: 0; padding: 0; box-sizing: border-box; }

:root {
  --bg: var(--color-background-primary);
  --bg2: var(--color-background-secondary);
  --bg3: var(--color-background-tertiary);
  --txt: var(--color-text-primary);
  --txt2: var(--color-text-secondary);
  --border: var(--color-border-tertiary);
  --border2: var(--color-border-secondary);
  --accent: #1D9E75;
  --accent2: #0F6E56;
  --mono: 'JetBrains Mono', monospace;
  --display: 'Syne', sans-serif;
}

.profile-wrap {
  font-family: var(--mono);
  padding: 2rem 0 3rem;
  max-width: 680px;
}

.header {
  border: 0.5px solid var(--border2);
  border-radius: var(--border-radius-lg);
  padding: 2rem;
  margin-bottom: 1.5rem;
  position: relative;
  overflow: hidden;
}

.header::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
  background: linear-gradient(90deg, #1D9E75, #5DCAA5, #9FE1CB);
}

.header-top {
  display: flex;
  align-items: center;
  gap: 1.25rem;
  margin-bottom: 1rem;
}

.avatar {
  width: 64px; height: 64px;
  border-radius: 50%;
  background: #E1F5EE;
  display: flex; align-items: center; justify-content: center;
  font-size: 22px;
  font-weight: 700;
  color: #0F6E56;
  font-family: var(--display);
  flex-shrink: 0;
  border: 2px solid #5DCAA5;
}

.name-block h1 {
  font-family: var(--display);
  font-size: 22px;
  font-weight: 800;
  color: var(--txt);
  line-height: 1.2;
}

.name-block .role {
  font-size: 12px;
  color: var(--accent);
  font-weight: 500;
  margin-top: 3px;
  letter-spacing: 0.05em;
}

.badges {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  margin-top: 0.75rem;
}

.badge {
  font-size: 11px;
  padding: 3px 10px;
  border-radius: 99px;
  font-family: var(--mono);
  border: 0.5px solid var(--border2);
  color: var(--txt2);
}

.badge.green {
  background: #E1F5EE;
  border-color: #5DCAA5;
  color: #0F6E56;
}

.bio {
  font-size: 13px;
  color: var(--txt2);
  line-height: 1.7;
  margin-top: 0.75rem;
}

.links {
  display: flex;
  gap: 12px;
  margin-top: 1rem;
  flex-wrap: wrap;
}

.link-btn {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-size: 12px;
  font-family: var(--mono);
  color: var(--txt2);
  text-decoration: none;
  padding: 5px 12px;
  border: 0.5px solid var(--border2);
  border-radius: var(--border-radius-md);
  transition: border-color 0.15s, color 0.15s;
}
.link-btn:hover { border-color: var(--accent); color: var(--accent); }

.link-btn svg { width: 13px; height: 13px; fill: currentColor; }

.section {
  margin-bottom: 1.5rem;
}

.section-label {
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.12em;
  color: var(--txt2);
  text-transform: uppercase;
  margin-bottom: 0.875rem;
  display: flex;
  align-items: center;
  gap: 8px;
}

.section-label::after {
  content: '';
  flex: 1;
  height: 0.5px;
  background: var(--border);
}

.about-card {
  border: 0.5px solid var(--border);
  border-radius: var(--border-radius-lg);
  padding: 1.25rem;
  display: grid;
  gap: 8px;
}

.about-item {
  display: flex;
  gap: 10px;
  font-size: 13px;
  color: var(--txt);
  align-items: flex-start;
}

.about-item .dot {
  color: var(--accent);
  font-weight: 700;
  margin-top: 1px;
  flex-shrink: 0;
}

.tech-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.tech-pill {
  display: flex;
  align-items: center;
  gap: 7px;
  padding: 6px 12px;
  border: 0.5px solid var(--border);
  border-radius: var(--border-radius-md);
  font-size: 12px;
  color: var(--txt);
  background: var(--bg2);
}

.tech-pill img {
  width: 16px; height: 16px;
  display: block;
}

.projects-list {
  display: grid;
  gap: 10px;
}

.project-card {
  border: 0.5px solid var(--border);
  border-radius: var(--border-radius-lg);
  padding: 1rem 1.25rem;
  display: grid;
  gap: 6px;
  transition: border-color 0.15s;
  cursor: pointer;
  text-decoration: none;
}

.project-card:hover { border-color: var(--accent); }

.project-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 8px;
}

.project-name {
  font-family: var(--display);
  font-size: 15px;
  font-weight: 700;
  color: var(--txt);
}

.project-arrow {
  font-size: 13px;
  color: var(--txt2);
}

.project-desc {
  font-size: 12px;
  color: var(--txt2);
  line-height: 1.6;
}

.project-stack {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
  margin-top: 4px;
}

.stack-tag {
  font-size: 10px;
  font-family: var(--mono);
  padding: 2px 8px;
  border-radius: 99px;
  background: #E1F5EE;
  color: #0F6E56;
  border: 0.5px solid #9FE1CB;
}

.footer-note {
  text-align: center;
  font-size: 12px;
  color: var(--txt2);
  margin-top: 1.5rem;
  padding-top: 1.5rem;
  border-top: 0.5px solid var(--border);
  font-style: italic;
}
</style>

<div class="profile-wrap">

  <div class="header">
    <div class="header-top">
      <div class="avatar">YA</div>
      <div class="name-block">
        <h1>Yousry Abdelrazek</h1>
        <div class="role">// backend developer · asp.net core · c# · sql server</div>
      </div>
    </div>
    <div class="badges">
      <span class="badge green">open to opportunities</span>
      <span class="badge">Cairo, Egypt</span>
      <span class="badge">CS Graduate 2026</span>
    </div>
    <p class="bio">Building scalable REST APIs with ASP.NET Core and modern backend practices. Turning complex requirements into simple, reliable systems.</p>
    <div class="links">
      <a class="link-btn" href="https://www.linkedin.com/in/yousry-abdelrazek-18bb7827a/" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a class="link-btn" href="mailto:yousryabdelrazek726@gmail.com">
        <svg viewBox="0 0 24 24"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
        Email
      </a>
      <a class="link-btn" href="https://github.com/Yousry-Abdelrazek" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
        GitHub
      </a>
    </div>
  </div>

  <div class="section">
    <div class="section-label">about me</div>
    <div class="about-card">
      <div class="about-item"><span class="dot">▸</span><span>Currently working on: <strong>Microservices Architecture &amp; System Design</strong></span></div>
      <div class="about-item"><span class="dot">▸</span><span>I enjoy turning complex requirements into simple, reliable APIs</span></div>
      <div class="about-item"><span class="dot">▸</span><span>Goal: Build and contribute to large-scale backend systems</span></div>
      <div class="about-item"><span class="dot">▸</span><span>Education: B.Sc. Computer Science — Fayoum University (2023–2026)</span></div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">i code with</div>
    <div class="tech-grid">
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" alt=""/>C#</div>
      <div class="tech-pill"><img src="https://skillicons.dev/icons?i=dotnet" alt=""/>.NET / ASP.NET Core</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/microsoftsqlserver/microsoftsqlserver-plain.svg" alt=""/>SQL Server</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" alt=""/>C++</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt=""/>Python</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt=""/>Java</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt=""/>JavaScript</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt=""/>HTML</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt=""/>CSS</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" alt=""/>Docker</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt=""/>Git</div>
      <div class="tech-pill"><img src="https://skillicons.dev/icons?i=visualstudio" alt=""/>Visual Studio</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/datagrip/datagrip-original.svg" alt=""/>DataGrip</div>
      <div class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postman/postman-original.svg" alt=""/>Postman</div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">featured projects</div>
    <div class="projects-list">

      <a class="project-card" href="https://github.com/Yousry-Abdelrazek/SurveyBasket" target="_blank">
        <div class="project-header">
          <span class="project-name">Survey Basket API</span>
          <span class="project-arrow">↗</span>
        </div>
        <p class="project-desc">Production-grade survey REST API with JWT auth, refresh tokens, role/permission-based authorization, response caching, rate limiting, audit logging, and background job processing via Hangfire.</p>
        <div class="project-stack">
          <span class="stack-tag">ASP.NET Core</span>
          <span class="stack-tag">SQL Server</span>
          <span class="stack-tag">Hangfire</span>
          <span class="stack-tag">Serilog</span>
          <span class="stack-tag">FluentValidation</span>
          <span class="stack-tag">IIS</span>
        </div>
      </a>

      <a class="project-card" href="https://github.com/Yousry-Abdelrazek/Water-Analysis" target="_blank">
        <div class="project-header">
          <span class="project-name">AquaProject</span>
          <span class="project-arrow">↗</span>
        </div>
        <p class="project-desc">Water quality analysis API with an integrated FastAPI ML microservice for real-time potability predictions based on nine physicochemical parameters. Includes a frontend for visualization.</p>
        <div class="project-stack">
          <span class="stack-tag">ASP.NET Core</span>
          <span class="stack-tag">FastAPI</span>
          <span class="stack-tag">SQL Server</span>
          <span class="stack-tag">EF Core</span>
          <span class="stack-tag">Machine Learning</span>
        </div>
      </a>

      <a class="project-card" href="https://github.com/Yousry-Abdelrazek/Search-Engine" target="_blank">
        <div class="project-header">
          <span class="project-name">Search Engine</span>
          <span class="project-arrow">↗</span>
        </div>
        <p class="project-desc">Web crawler and ranking engine using word frequency analysis and the PageRank algorithm. Built with an inverted index, SQL Server storage, and fully containerized with Docker.</p>
        <div class="project-stack">
          <span class="stack-tag">C#</span>
          <span class="stack-tag">SQL Server</span>
          <span class="stack-tag">Docker</span>
          <span class="stack-tag">PageRank</span>
        </div>
      </a>

      <a class="project-card" href="https://github.com/Yousry-Abdelrazek/library-Management-System-" target="_blank">
        <div class="project-header">
          <span class="project-name">Library Management System</span>
          <span class="project-arrow">↗</span>
        </div>
        <p class="project-desc">Library management system in C++ using OOP principles, custom data structures, and file-based storage for data persistence.</p>
        <div class="project-stack">
          <span class="stack-tag">C++</span>
          <span class="stack-tag">OOP</span>
          <span class="stack-tag">Data Structures</span>
          <span class="stack-tag">File I/O</span>
        </div>
      </a>

    </div>
  </div>

  <p class="footer-note">Always open to interesting projects and backend engineering roles.</p>

</div>
