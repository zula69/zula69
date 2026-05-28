
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Nihara Sulochana — Cybersecurity Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --c1: #0BF7A0;
    --c2: #00D4FF;
    --c3: #FF4C7A;
    --bg: #0A0D12;
    --bg2: #10141C;
    --bg3: #151B26;
    --border: #1E2535;
    --text: #C8D6EF;
    --muted: #5A6B85;
  }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    min-height: 100vh;
    line-height: 1.6;
  }

  /* ── LAYOUT ── */
  .wrap { max-width: 900px; margin: 0 auto; padding: 2rem 2rem 5rem; }

  /* ── NAV ── */
  nav {
    position: sticky;
    top: 0;
    z-index: 100;
    background: rgba(10, 13, 18, 0.9);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: .8rem 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .nav-logo {
    font-family: 'Space Mono', monospace;
    font-size: .85rem;
    color: var(--c1);
    letter-spacing: 1px;
    text-decoration: none;
  }
  .nav-links { display: flex; gap: 1.5rem; list-style: none; }
  .nav-links a {
    font-family: 'Space Mono', monospace;
    font-size: .72rem;
    color: var(--muted);
    text-decoration: none;
    letter-spacing: .5px;
    transition: color .2s;
  }
  .nav-links a:hover { color: var(--c1); }

  /* ── HERO ── */
  .hero {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 2rem;
    align-items: center;
    padding: 4rem 0 3rem;
    border-bottom: 1px solid var(--border);
  }
  .tag {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(11, 247, 160, 0.08);
    border: 1px solid rgba(11, 247, 160, 0.25);
    color: var(--c1);
    font-family: 'Space Mono', monospace;
    font-size: .7rem;
    padding: 5px 14px;
    border-radius: 2px;
    margin-bottom: 1.4rem;
    letter-spacing: 1.5px;
  }
  .tag-dot {
    width: 6px; height: 6px;
    background: var(--c1);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }
  @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: .2; } }

  h1 {
    font-size: clamp(2.4rem, 6vw, 3.6rem);
    font-weight: 800;
    line-height: 1;
    letter-spacing: -1.5px;
    color: #fff;
    margin-bottom: .4rem;
  }
  h1 span { color: var(--c1); }
  .subtitle {
    font-family: 'Space Mono', monospace;
    font-size: .75rem;
    color: var(--muted);
    letter-spacing: .8px;
    margin-bottom: 2rem;
    line-height: 1.8;
  }

  .hero-btns { display: flex; gap: 10px; flex-wrap: wrap; }
  .btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border-radius: 3px;
    font-family: 'Space Mono', monospace;
    font-size: .72rem;
    font-weight: 700;
    text-decoration: none;
    letter-spacing: .5px;
    cursor: pointer;
    border: none;
    transition: all .2s;
  }
  .btn-outline {
    background: transparent;
    border: 1px solid var(--border);
    color: var(--text);
  }
  .btn-outline:hover { border-color: var(--c2); color: var(--c2); background: rgba(0,212,255,.06); }
  .btn-primary {
    background: var(--c1);
    color: #0A0D12;
  }
  .btn-primary:hover { background: #0de08e; }

  /* ── AVATAR ── */
  .avatar-wrap { position: relative; flex-shrink: 0; }
  .avatar {
    width: 120px; height: 120px;
    border-radius: 50%;
    background: linear-gradient(135deg, rgba(11,247,160,.15), rgba(0,212,255,.15));
    border: 2px solid var(--border);
    display: flex; align-items: center; justify-content: center;
    font-size: 2.8rem; font-weight: 800; color: #fff;
    position: relative; z-index: 1;
  }
  .avatar-ring {
    position: absolute; inset: -8px;
    border-radius: 50%;
    border: 1px solid rgba(11,247,160,.15);
    animation: rotate 10s linear infinite;
  }
  .avatar-ring2 {
    position: absolute; inset: -16px;
    border-radius: 50%;
    border: 1px dashed rgba(0,212,255,.1);
    animation: rotate 16s linear infinite reverse;
  }
  @keyframes rotate { to { transform: rotate(360deg); } }

  /* ── OBJECTIVE ── */
  .objective {
    margin: 2.5rem 0;
    padding: 1.5rem 1.8rem;
    background: var(--bg2);
    border-left: 3px solid var(--c1);
    border-radius: 0 6px 6px 0;
  }
  .objective p { font-size: .95rem; line-height: 1.9; color: var(--text); }

  /* ── SECTION ── */
  section { margin: 3rem 0; }
  .sec-header {
    display: flex; align-items: center; gap: 12px;
    margin-bottom: 1.6rem;
  }
  .sec-label {
    font-family: 'Space Mono', monospace;
    font-size: .68rem;
    color: var(--c1);
    letter-spacing: 2px;
    background: rgba(11,247,160,.1);
    padding: 3px 9px;
    border-radius: 2px;
    flex-shrink: 0;
  }
  .sec-title { font-size: 1.1rem; font-weight: 700; color: #fff; }
  .sec-line { flex: 1; height: 1px; background: var(--border); }

  /* ── SKILLS ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
    gap: 10px;
  }
  .skill-item {
    display: flex; align-items: center; gap: 10px;
    padding: 12px 16px;
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 4px;
    font-size: .84rem;
    color: var(--text);
    transition: all .2s;
  }
  .skill-item:hover { border-color: rgba(11,247,160,.3); color: #fff; background: var(--bg3); }
  .skill-dot { width: 5px; height: 5px; background: var(--c1); border-radius: 50%; flex-shrink: 0; }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 14px;
  }
  .card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1.4rem;
    transition: all .25s;
    position: relative;
    overflow: hidden;
  }
  .card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, var(--c1), var(--c2));
    opacity: 0; transition: opacity .25s;
  }
  .card:hover { border-color: #1E2D45; transform: translateY(-3px); }
  .card:hover::before { opacity: 1; }
  .card-type {
    font-family: 'Space Mono', monospace;
    font-size: .68rem; color: var(--muted);
    letter-spacing: 1.2px; margin-bottom: .7rem;
  }
  .card-title { font-size: 1rem; font-weight: 700; color: #fff; margin-bottom: .5rem; }
  .card-desc { font-size: .82rem; color: var(--muted); line-height: 1.7; margin-bottom: 1.1rem; }
  .card-link {
    display: inline-flex; align-items: center; gap: 7px;
    font-family: 'Space Mono', monospace; font-size: .7rem;
    color: var(--c2); text-decoration: none;
    border: 1px solid rgba(0,212,255,.25);
    padding: 6px 14px; border-radius: 3px;
    transition: all .2s;
  }
  .card-link:hover { background: rgba(0,212,255,.1); border-color: var(--c2); }
  .card-link svg { width: 12px; height: 12px; }

  /* ── LABS ── */
  .labs-list { display: flex; flex-direction: column; gap: 8px; }
  .lab-row {
    display: flex; align-items: center; justify-content: space-between;
    padding: 13px 18px;
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 5px;
    transition: all .2s;
  }
  .lab-row:hover { border-color: rgba(11,247,160,.25); background: var(--bg3); }
  .lab-name { font-size: .87rem; color: var(--text); display: flex; align-items: center; gap: 10px; }
  .lab-badge {
    font-family: 'Space Mono', monospace; font-size: .65rem;
    background: rgba(11,247,160,.1); color: var(--c1);
    border: 1px solid rgba(11,247,160,.25);
    padding: 2px 8px; border-radius: 2px; letter-spacing: .5px;
    flex-shrink: 0;
  }
  .lab-link {
    font-family: 'Space Mono', monospace; font-size: .7rem;
    color: var(--c2); text-decoration: none;
    display: flex; align-items: center; gap: 5px;
    opacity: .7; transition: opacity .2s;
  }
  .lab-link:hover { opacity: 1; }

  /* ── TOOLS ── */
  .tools-section { display: flex; flex-direction: column; gap: 1.4rem; }
  .tool-group { display: flex; flex-direction: column; gap: .8rem; }
  .tool-group-label {
    font-family: 'Space Mono', monospace; font-size: .65rem;
    color: var(--muted); letter-spacing: 2px;
  }
  .tool-pills { display: flex; flex-wrap: wrap; gap: 8px; }
  .pill {
    display: flex; align-items: center; gap: 8px;
    padding: 9px 16px;
    background: var(--bg3);
    border: 1px solid var(--border);
    border-radius: 3px;
    font-size: .82rem; font-weight: 600; color: var(--text);
    white-space: nowrap;
    transition: border-color .2s;
  }
  .pill:hover { border-color: #2E3D55; }
  .pill-dot { width: 7px; height: 7px; border-radius: 50%; flex-shrink: 0; }

  /* ── CERTS ── */
  .certs-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
    gap: 12px;
  }
  .cert-card {
    display: flex; align-items: center; gap: 14px;
    padding: 1.2rem 1.4rem;
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 7px;
    transition: border-color .2s;
  }
  .cert-card:hover { border-color: #2E3D55; }
  .cert-icon {
    width: 44px; height: 44px;
    border-radius: 5px;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .cert-name { font-size: .9rem; font-weight: 700; color: #fff; }
  .cert-issuer {
    font-size: .7rem; color: var(--muted);
    font-family: 'Space Mono', monospace;
    margin-top: 3px; letter-spacing: .5px;
  }

  /* ── CONTACT ── */
  .contact-box {
    text-align: center;
    padding: 3rem 2rem;
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 10px;
    position: relative;
    overflow: hidden;
  }
  .contact-box::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, var(--c1), var(--c2), var(--c3));
  }
  .contact-box h2 { font-size: 1.8rem; font-weight: 800; color: #fff; margin-bottom: .5rem; }
  .contact-box p { font-size: .9rem; color: var(--muted); margin-bottom: 1.8rem; }

  /* ── FOOTER ── */
  footer {
    margin-top: 4rem;
    padding-top: 2rem;
    border-top: 1px solid var(--border);
    display: flex; align-items: center; justify-content: space-between;
    flex-wrap: wrap; gap: 1rem;
  }
  .footer-name {
    font-family: 'Space Mono', monospace; font-size: .72rem; color: var(--muted);
  }
  .footer-status {
    display: flex; align-items: center; gap: 7px;
    font-family: 'Space Mono', monospace; font-size: .72rem; color: var(--c1);
  }
  .footer-status-dot {
    width: 6px; height: 6px;
    background: var(--c1); border-radius: 50%;
    animation: pulse 2s infinite;
  }

  /* ── SCROLL FADE IN ── */
  .fade-in {
    opacity: 0; transform: translateY(18px);
    transition: opacity .6s ease, transform .6s ease;
  }
  .fade-in.visible { opacity: 1; transform: translateY(0); }

  /* ── RESPONSIVE ── */
  @media (max-width: 600px) {
    .hero { grid-template-columns: 1fr; }
    .avatar-wrap { display: none; }
    nav { padding: .8rem 1rem; }
    .wrap { padding: 1.5rem 1rem 4rem; }
    .nav-links { gap: 1rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">NS://PORTFOLIO</a>
  <ul class="nav-links">
    <li><a href="#skills">Skills</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#labs">Labs</a></li>
    <li><a href="#tools">Tools</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<div class="wrap">

  <!-- ── HERO ── -->
  <div class="hero fade-in">
    <div class="hero-left">
      <div class="tag">
        <span class="tag-dot"></span>
        OPEN TO OPPORTUNITIES
      </div>
      <h1>NIHARA<br><span>SULOCHANA</span></h1>
      <p class="subtitle">
        NETWORKING &amp; CYBERSECURITY UNDERGRADUATE<br>
        ETHICAL HACKING · PENETRATION TESTING · NETWORK SECURITY
      </p>
      <div class="hero-btns">
        <a href="https://www.linkedin.com/in/nihara-sulochana-samaranayake/" target="_blank" class="btn btn-outline">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          LinkedIn
        </a>
        <a href="https://github.com/zula69" target="_blank" class="btn btn-outline">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0020 4.77 5.07 5.07 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 005 4.77a5.44 5.44 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg>
          GitHub
        </a>
      </div>
    </div>
    <div class="avatar-wrap">
      <div class="avatar-ring2"></div>
      <div class="avatar-ring"></div>
      <div class="avatar">NS</div>
    </div>
  </div>

  <!-- ── OBJECTIVE ── -->
  <div class="objective fade-in">
    <p>To become a skilled cybersecurity and networking professional by gaining hands-on experience in vulnerability assessment, penetration testing, and secure network design — while contributing to real-world security solutions.</p>
  </div>

  <!-- ── SKILLS ── -->
  <section id="skills" class="fade-in">
    <div class="sec-header">
      <span class="sec-label">01</span>
      <span class="sec-title">Core Skills</span>
      <div class="sec-line"></div>
    </div>
    <div class="skills-grid">
      <div class="skill-item"><span class="skill-dot"></span>Networking Fundamentals</div>
      <div class="skill-item"><span class="skill-dot"></span>Cybersecurity Fundamentals</div>
      <div class="skill-item"><span class="skill-dot"></span>Project Management</div>
      <div class="skill-item"><span class="skill-dot"></span>Programming Fundamentals</div>
      <div class="skill-item"><span class="skill-dot"></span>Network Troubleshooting &amp; Config</div>
      <div class="skill-item"><span class="skill-dot"></span>Endpoint Security</div>
      <div class="skill-item"><span class="skill-dot"></span>Linux</div>
    </div>
  </section>

  <!-- ── PROJECTS ── -->
  <section id="projects" class="fade-in">
    <div class="sec-header">
      <span class="sec-label">02</span>
      <span class="sec-title">Projects</span>
      <div class="sec-line"></div>
    </div>
    <div class="projects-grid">

      <!-- ADD / EDIT PROJECTS HERE -->
      <div class="card">
        <div class="card-type">SQL INJECTION · ANALYSIS</div>
        <div class="card-title">Simple SQL Attack Simulation</div>
        <div class="card-desc">Hands-on simulation and analysis of SQL injection vulnerabilities, exploring attack vectors and mitigation strategies in a controlled environment.</div>
        <a href="https://github.com/zula69/Simple-SQL-attack-simulation-and-analysis/tree/main" target="_blank" class="card-link">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0020 4.77 5.07 5.07 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 005 4.77a5.44 5.44 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg>
          View on GitHub
        </a>
      </div>

      <!-- DUPLICATE THE BLOCK ABOVE TO ADD MORE PROJECTS -->

    </div>
  </section>

  <!-- ── LABS ── -->
  <section id="labs" class="fade-in">
    <div class="sec-header">
      <span class="sec-label">03</span>
      <span class="sec-title">Hack The Box Labs</span>
      <div class="sec-line"></div>
    </div>
    <div class="labs-list">

      <!-- ADD / EDIT LABS HERE -->
      <div class="lab-row">
        <div class="lab-name"><span class="lab-badge">HTB</span>Meow — Starter Lab</div>
        <a href="https://github.com/zula69/Meow-HackTheBox-Starter-Lab" target="_blank" class="lab-link">GitHub ↗</a>
      </div>
      <div class="lab-row">
        <div class="lab-name"><span class="lab-badge">HTB</span>Fawn — Starter Lab</div>
        <a href="https://github.com/zula69/Fawn-HackTheBox-Starter-Lab/tree/main" target="_blank" class="lab-link">GitHub ↗</a>
      </div>
      <div class="lab-row">
        <div class="lab-name"><span class="lab-badge">HTB</span>Redeemer — Starter Lab</div>
        <a href="https://github.com/zula69/Redeemer-HackTheBox-Starter-Lab/tree/main" target="_blank" class="lab-link">GitHub ↗</a>
      </div>
      <div class="lab-row">
        <div class="lab-name"><span class="lab-badge">HTB</span>Dancing — Starter Lab</div>
        <a href="https://github.com/zula69/Dancing-HackTheBox-Starter-Lab/tree/main" target="_blank" class="lab-link">GitHub ↗</a>
      </div>
      <div class="lab-row">
        <div class="lab-name"><span class="lab-badge">HTB</span>Cap — Lab</div>
        <a href="https://github.com/zula69/Cap-HackTheBox-Lab/tree/main" target="_blank" class="lab-link">GitHub ↗</a>
      </div>

    </div>
  </section>

  <!-- ── TOOLS ── -->
  <section id="tools" class="fade-in">
    <div class="sec-header">
      <span class="sec-label">04</span>
      <span class="sec-title">Tools &amp; Technologies</span>
      <div class="sec-line"></div>
    </div>
    <div class="tools-section">

      <div class="tool-group">
        <div class="tool-group-label">NETWORK</div>
        <div class="tool-pills">
          <div class="pill"><span class="pill-dot" style="background:#1679A7"></span>Wireshark</div>
          <div class="pill"><span class="pill-dot" style="background:#EF3B2D"></span>Suricata</div>
          <div class="pill"><span class="pill-dot" style="background:#777BB4"></span>Zeek</div>
        </div>
      </div>

      <div class="tool-group">
        <div class="tool-group-label">ENDPOINT</div>
        <div class="tool-pills">
          <div class="pill"><span class="pill-dot" style="background:#00A4EF"></span>Microsoft Defender for Endpoint</div>
          <div class="pill"><span class="pill-dot" style="background:#8B5CF6"></span>Velociraptor</div>
        </div>
      </div>

      <div class="tool-group">
        <div class="tool-group-label">SIEM</div>
        <div class="tool-pills">
          <div class="pill"><span class="pill-dot" style="background:#0078D4"></span>Microsoft Sentinel</div>
          <div class="pill"><span class="pill-dot" style="background:#65C637"></span>Splunk</div>
          <div class="pill"><span class="pill-dot" style="background:#00BFB3"></span>Elastic</div>
        </div>
      </div>

    </div>
  </section>

  <!-- ── CERTIFICATIONS ── -->
  <section id="certs" class="fade-in">
    <div class="sec-header">
      <span class="sec-label">05</span>
      <span class="sec-title">Certifications</span>
      <div class="sec-line"></div>
    </div>
    <div class="certs-grid">
      <div class="cert-card">
        <div class="cert-icon" style="background:rgba(29,161,242,.12)">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="#1DA1F2"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 14.5v-9l6 4.5-6 4.5z"/></svg>
        </div>
        <div>
          <div class="cert-name">Networking Academy</div>
          <div class="cert-issuer">CISCO</div>
        </div>
      </div>
      <div class="cert-card">
        <div class="cert-icon" style="background:rgba(255,60,60,.1)">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#FF4444" stroke-width="2" stroke-linecap="round"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg>
        </div>
        <div>
          <div class="cert-name">Networks Training</div>
          <div class="cert-issuer">PALO ALTO NETWORKS</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── CONTACT ── -->
  <section id="contact" class="fade-in">
    <div class="sec-header">
      <span class="sec-label">06</span>
      <span class="sec-title">Get In Touch</span>
      <div class="sec-line"></div>
    </div>
    <div class="contact-box">
      <h2>Let's Connect</h2>
      <p>Open to internships, collaborations, and cybersecurity opportunities.</p>
      <div style="display:flex;gap:12px;justify-content:center;flex-wrap:wrap">
        <a href="https://www.linkedin.com/in/nihara-sulochana-samaranayake/" target="_blank" class="btn btn-primary">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          Message on LinkedIn
        </a>
        <a href="https://github.com/zula69" target="_blank" class="btn btn-outline">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0020 4.77 5.07 5.07 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 005 4.77a5.44 5.44 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg>
          View GitHub
        </a>
      </div>
    </div>
  </section>

  <!-- ── FOOTER ── -->
  <footer>
    <span class="footer-name">© 2025 NIHARA SULOCHANA SAMARANAYAKE</span>
    <span class="footer-status">
      <span class="footer-status-dot"></span>
      AVAILABLE FOR INTERNSHIPS
    </span>
  </footer>

</div>

<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        observer.unobserve(e.target);
      }
    });
  }, { threshold: 0.1 });
  document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
</script>

</body>
</html>
