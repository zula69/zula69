```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Nihara Sulochana — Cybersecurity Portfolio</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet" />

<link rel="icon" type="image/png" href="favicon.png">

<style>

*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

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

html {
  scroll-behavior: smooth;
}

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Syne', sans-serif;
  min-height: 100vh;
  line-height: 1.6;

  overflow-x: hidden;

  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

/* ───────── LAYOUT ───────── */

.wrap {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 2rem 5rem;
}

/* ───────── NAV ───────── */

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

.nav-links {
  display: flex;
  gap: 1.5rem;
  list-style: none;
  flex-wrap: wrap;
}

.nav-links a {
  font-family: 'Space Mono', monospace;
  font-size: .72rem;
  color: var(--muted);
  text-decoration: none;
  letter-spacing: .5px;
  transition: color .2s;
}

.nav-links a:hover {
  color: var(--c1);
}

/* ───────── HERO ───────── */

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
  width: 6px;
  height: 6px;

  background: var(--c1);

  border-radius: 50%;

  animation: pulse 2s infinite;
}

@keyframes pulse {
  0%,100% { opacity: 1; }
  50% { opacity: .2; }
}

h1 {
  font-size: clamp(2.4rem, 6vw, 3.6rem);

  font-weight: 800;

  line-height: 1;

  letter-spacing: -1.5px;

  color: white;

  margin-bottom: .4rem;
}

h1 span {
  color: var(--c1);
}

.subtitle {
  font-family: 'Space Mono', monospace;

  font-size: .75rem;

  color: var(--muted);

  letter-spacing: .8px;

  margin-bottom: 2rem;

  line-height: 1.8;
}

.hero-btns {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
}

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

.btn-outline:hover {
  border-color: var(--c2);
  color: var(--c2);
  background: rgba(0,212,255,.06);
}

.btn-primary {
  background: var(--c1);
  color: #0A0D12;
}

.btn-primary:hover {
  background: #0de08e;
}

/* ───────── AVATAR ───────── */

.avatar-wrap {
  position: relative;
  flex-shrink: 0;
}

.avatar {
  width: 120px;
  height: 120px;

  border-radius: 50%;

  background: linear-gradient(
    135deg,
    rgba(11,247,160,.15),
    rgba(0,212,255,.15)
  );

  border: 2px solid var(--border);

  display: flex;
  align-items: center;
  justify-content: center;

  font-size: 2.8rem;
  font-weight: 800;
  color: white;

  position: relative;
  z-index: 1;
}

.avatar-ring {
  position: absolute;
  inset: -8px;

  border-radius: 50%;
  border: 1px solid rgba(11,247,160,.15);

  animation: rotate 10s linear infinite;
}

.avatar-ring2 {
  position: absolute;
  inset: -16px;

  border-radius: 50%;
  border: 1px dashed rgba(0,212,255,.1);

  animation: rotate 16s linear infinite reverse;
}

@keyframes rotate {
  to {
    transform: rotate(360deg);
  }
}

/* ───────── RESPONSIVE ───────── */

@media (max-width: 600px) {

  .hero {
    grid-template-columns: 1fr;
  }

  .avatar-wrap {
    display: none;
  }

  nav {
    padding: .8rem 1rem;
  }

  .wrap {
    padding: 1.5rem 1rem 4rem;
  }

  .nav-links {
    gap: 1rem;
  }

}

</style>
</head>

<body>

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

<div class="hero fade-in">

<div class="hero-left">

<div class="tag">
  <span class="tag-dot"></span>
  OPEN TO OPPORTUNITIES
</div>

<h1>
NIHARA<br>
<span>SULOCHANA</span>
</h1>

<p class="subtitle">
NETWORKING & CYBERSECURITY UNDERGRADUATE<br>
ETHICAL HACKING · PENETRATION TESTING · NETWORK SECURITY
</p>

<div class="hero-btns">

<a
href="https://www.linkedin.com/in/nihara-sulochana-samaranayake/"
target="_blank"
rel="noopener noreferrer"
aria-label="LinkedIn Profile"
class="btn btn-outline">

LinkedIn

</a>

<a
href="https://github.com/zula69"
target="_blank"
rel="noopener noreferrer"
aria-label="GitHub Profile"
class="btn btn-outline">

GitHub

</a>

</div>
</div>

<div class="avatar-wrap">

<div class="avatar-ring2"></div>
<div class="avatar-ring"></div>

<div class="avatar">
NS
</div>

</div>
</div>

<footer>

<span class="footer-name">
© 2026 NIHARA SULOCHANA SAMARANAYAKE
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
```
