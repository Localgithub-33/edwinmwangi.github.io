<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Edwin Mwangi — Ecosystem Builder, Kenya</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500;600&family=Playfair+Display:ital,wght@0,700;1,400&display=swap" rel="stylesheet">

<style>
:root {
  --navy: #0D2B55;
  --gold: #C9A84C;
  --gold-light: #E8C97A;
  --cream: #FAF8F3;
  --warm-white: #FFFEF9;
  --text: #1a1a1a;
  --text-muted: #6b6b6b;
  --text-light: #9a9a8a;
  --border: rgba(201,168,76,0.2);
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--warm-white);
  color: var(--text);
  overflow-x: hidden;
}

/* ── NAV ── */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  padding: 18px 48px;
  display: flex; align-items: center; justify-content: space-between;
  background: rgba(255,254,249,0.92);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border);
  transition: all 0.3s;
}

.nav-logo {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.3rem;
  font-weight: 600;
  color: var(--navy);
  letter-spacing: 0.02em;
  text-decoration: none;
}

.nav-logo span { color: var(--gold); }

.nav-links {
  display: flex; gap: 36px; list-style: none;
}

.nav-links a {
  font-size: 0.82rem;
  font-weight: 500;
  color: var(--text-muted);
  text-decoration: none;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  transition: color 0.2s;
}

.nav-links a:hover { color: var(--gold); }

.nav-cta {
  background: var(--navy);
  color: #fff !important;
  padding: 8px 22px;
  border-radius: 2px;
  font-size: 0.78rem !important;
  letter-spacing: 0.1em !important;
  transition: background 0.2s !important;
}

.nav-cta:hover { background: var(--gold) !important; color: var(--navy) !important; }

/* ── HERO ── */
#hero {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 1fr 1fr;
  position: relative;
  overflow: hidden;
}

.hero-left {
  background: var(--navy);
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 120px 64px 80px 72px;
  position: relative;
  overflow: hidden;
}

.hero-left::before {
  content: '';
  position: absolute;
  top: -100px; right: -100px;
  width: 400px; height: 400px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(201,168,76,0.12) 0%, transparent 70%);
  pointer-events: none;
}

.hero-eyebrow {
  font-size: 0.72rem;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 24px;
  display: flex;
  align-items: center;
  gap: 12px;
}

.hero-eyebrow::before {
  content: '';
  display: inline-block;
  width: 32px; height: 1px;
  background: var(--gold);
}

.hero-name {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(3.2rem, 5vw, 5.2rem);
  font-weight: 300;
  color: #fff;
  line-height: 1.05;
  margin-bottom: 8px;
}

.hero-name em {
  font-style: italic;
  color: var(--gold-light);
  font-weight: 300;
}

.hero-title {
  font-size: 1rem;
  font-weight: 400;
  color: rgba(255,255,255,0.6);
  margin-bottom: 40px;
  letter-spacing: 0.03em;
}

.hero-statement {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.35rem;
  font-weight: 300;
  font-style: italic;
  color: rgba(255,255,255,0.85);
  line-height: 1.7;
  border-left: 2px solid var(--gold);
  padding-left: 20px;
  margin-bottom: 52px;
  max-width: 460px;
}

.hero-actions {
  display: flex; gap: 16px; flex-wrap: wrap;
}

.btn-primary {
  background: var(--gold);
  color: var(--navy);
  padding: 14px 32px;
  font-size: 0.82rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  text-decoration: none;
  border-radius: 2px;
  transition: all 0.25s;
  display: inline-block;
}

.btn-primary:hover {
  background: var(--gold-light);
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(201,168,76,0.3);
}

.btn-ghost {
  border: 1px solid rgba(255,255,255,0.3);
  color: rgba(255,255,255,0.8);
  padding: 14px 32px;
  font-size: 0.82rem;
  font-weight: 400;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  text-decoration: none;
  border-radius: 2px;
  transition: all 0.25s;
  display: inline-block;
}

.btn-ghost:hover {
  border-color: var(--gold);
  color: var(--gold);
}

.hero-right {
  position: relative;
  overflow: hidden;
  background: #0a1f3d;
}

.hero-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center top;
  opacity: 0.75;
  mix-blend-mode: luminosity;
  filter: contrast(1.1);
}

.hero-img-overlay {
  position: absolute; inset: 0;
  background: linear-gradient(135deg, rgba(13,43,85,0.5) 0%, transparent 60%);
}

.hero-scroll {
  position: absolute;
  bottom: 40px; left: 72px;
  display: flex; align-items: center; gap: 12px;
  color: rgba(255,255,255,0.4);
  font-size: 0.72rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
}

.hero-scroll::after {
  content: '';
  display: block;
  width: 1px; height: 48px;
  background: rgba(255,255,255,0.2);
  animation: scrollPulse 2s ease-in-out infinite;
}

@keyframes scrollPulse {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 0.8; }
}

/* ── TICKER ── */
.ticker {
  background: var(--gold);
  padding: 12px 0;
  overflow: hidden;
  white-space: nowrap;
}

.ticker-inner {
  display: inline-flex;
  animation: ticker 30s linear infinite;
}

.ticker span {
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--navy);
  padding: 0 40px;
}

.ticker span::before {
  content: '◆';
  margin-right: 16px;
  opacity: 0.5;
}

@keyframes ticker {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}

/* ── SECTIONS SHARED ── */
section { padding: 100px 0; }

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 48px;
}

.section-label {
  font-size: 0.68rem;
  font-weight: 600;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 12px;
}

.section-label::after {
  content: '';
  display: block;
  width: 48px; height: 1px;
  background: var(--gold);
  opacity: 0.5;
}

.section-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(2rem, 3.5vw, 3rem);
  font-weight: 300;
  color: var(--navy);
  line-height: 1.2;
  margin-bottom: 24px;
}

.section-title em {
  font-style: italic;
  color: var(--gold);
}

/* ── ABOUT ── */
#about {
  background: var(--cream);
  position: relative;
  overflow: hidden;
}

#about::before {
  content: '"';
  font-family: 'Cormorant Garamond', serif;
  font-size: 30rem;
  color: rgba(13,43,85,0.03);
  position: absolute;
  top: -80px; left: -20px;
  line-height: 1;
  pointer-events: none;
  user-select: none;
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1.4fr;
  gap: 80px;
  align-items: start;
}

.about-photo-wrap {
  position: relative;
}

.about-photo {
  width: 100%;
  aspect-ratio: 3/4;
  object-fit: cover;
  object-position: top;
  display: block;
  border-radius: 2px;
}

.about-photo-accent {
  position: absolute;
  top: 24px; left: 24px;
  right: -16px; bottom: -16px;
  border: 1px solid var(--gold);
  border-radius: 2px;
  z-index: -1;
  opacity: 0.4;
}

.about-badge {
  position: absolute;
  bottom: 24px; right: -20px;
  background: var(--navy);
  color: #fff;
  padding: 16px 20px;
  border-radius: 2px;
  text-align: center;
  box-shadow: 0 8px 32px rgba(13,43,85,0.25);
}

.about-badge strong {
  display: block;
  font-family: 'Cormorant Garamond', serif;
  font-size: 2rem;
  font-weight: 300;
  color: var(--gold);
  line-height: 1;
}

.about-badge span {
  font-size: 0.68rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  opacity: 0.7;
}

.about-text p {
  font-size: 1.05rem;
  line-height: 1.85;
  color: #333;
  margin-bottom: 20px;
  font-weight: 300;
}

.about-text p strong {
  color: var(--navy);
  font-weight: 600;
}

.about-pull {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.5rem;
  font-style: italic;
  color: var(--navy);
  border-left: 3px solid var(--gold);
  padding-left: 20px;
  margin: 32px 0;
  line-height: 1.55;
}

.about-links {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 32px;
}

.about-link {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px 16px;
  border: 1px solid var(--border);
  border-radius: 40px;
  font-size: 0.78rem;
  color: var(--navy);
  text-decoration: none;
  font-weight: 500;
  transition: all 0.2s;
  background: white;
}

.about-link:hover {
  border-color: var(--gold);
  background: var(--navy);
  color: white;
}

/* ── WHAT I DO ── */
#what {
  background: var(--warm-white);
}

.what-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2px;
  margin-top: 56px;
  background: var(--border);
}

.what-card {
  background: var(--warm-white);
  padding: 48px 36px;
  position: relative;
  transition: background 0.3s;
}

.what-card:hover { background: var(--cream); }

.what-card:hover .what-num { color: var(--gold); }

.what-num {
  font-family: 'Cormorant Garamond', serif;
  font-size: 3.5rem;
  font-weight: 300;
  color: rgba(13,43,85,0.08);
  line-height: 1;
  margin-bottom: 20px;
  transition: color 0.3s;
}

.what-icon {
  width: 40px; height: 40px;
  margin-bottom: 20px;
  color: var(--gold);
}

.what-card h3 {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.4rem;
  font-weight: 600;
  color: var(--navy);
  margin-bottom: 14px;
  line-height: 1.2;
}

.what-card p {
  font-size: 0.9rem;
  line-height: 1.75;
  color: var(--text-muted);
  font-weight: 300;
}

/* ── EXPERIENCE ── */
#experience {
  background: var(--navy);
  color: white;
}

#experience .section-title { color: white; }
#experience .section-label { color: var(--gold); }

.exp-list {
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  gap: 0;
}

.exp-item {
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 0 48px;
  padding: 40px 0;
  border-bottom: 1px solid rgba(255,255,255,0.07);
  position: relative;
  cursor: default;
  transition: all 0.3s;
}

.exp-item:hover { background: rgba(255,255,255,0.02); padding-left: 16px; }
.exp-item:first-child { padding-top: 0; }

.exp-meta {
  padding-top: 4px;
}

.exp-period {
  font-size: 0.78rem;
  color: var(--gold);
  font-weight: 500;
  letter-spacing: 0.05em;
  margin-bottom: 6px;
}

.exp-company {
  font-size: 0.8rem;
  color: rgba(255,255,255,0.4);
  font-weight: 300;
  letter-spacing: 0.03em;
}

.exp-role {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.5rem;
  font-weight: 400;
  color: white;
  margin-bottom: 14px;
  line-height: 1.2;
}

.exp-desc {
  font-size: 0.9rem;
  color: rgba(255,255,255,0.6);
  line-height: 1.8;
  font-weight: 300;
  margin-bottom: 16px;
}

.exp-tags {
  display: flex; flex-wrap: wrap; gap: 8px;
}

.exp-tag {
  font-size: 0.68rem;
  font-weight: 500;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--gold);
  border: 1px solid rgba(201,168,76,0.25);
  padding: 4px 12px;
  border-radius: 2px;
}

/* ── SKILLS ── */
#skills {
  background: var(--cream);
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 40px;
  margin-top: 56px;
}

.skill-group h3 {
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 20px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--border);
}

.skill-items {
  display: flex; flex-wrap: wrap; gap: 10px;
}

.skill-item {
  background: white;
  border: 1px solid var(--border);
  color: var(--navy);
  padding: 8px 18px;
  font-size: 0.82rem;
  font-weight: 400;
  border-radius: 2px;
  transition: all 0.2s;
}

.skill-item:hover {
  background: var(--navy);
  color: white;
  border-color: var(--navy);
  transform: translateY(-2px);
}

/* ── PROJECTS ── */
#projects {
  background: var(--warm-white);
}

.projects-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 56px;
}

.projects-grid {
  display: grid;
  grid-template-columns: 1.3fr 1fr;
  gap: 24px;
}

.project-card {
  background: var(--cream);
  padding: 44px 40px;
  border-radius: 2px;
  border: 1px solid transparent;
  transition: all 0.3s;
  position: relative;
  overflow: hidden;
}

.project-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0;
  width: 3px; height: 0;
  background: var(--gold);
  transition: height 0.3s;
}

.project-card:hover { border-color: var(--border); }
.project-card:hover::before { height: 100%; }

.project-card.featured {
  background: var(--navy);
  color: white;
  grid-row: span 2;
}

.project-label {
  font-size: 0.68rem;
  font-weight: 600;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 16px;
}

.project-card h3 {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.6rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 16px;
  line-height: 1.25;
}

.project-card.featured h3 { color: white; font-size: 2rem; }

.project-card p {
  font-size: 0.88rem;
  line-height: 1.75;
  color: var(--text-muted);
  font-weight: 300;
}

.project-card.featured p { color: rgba(255,255,255,0.65); }

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  margin-top: 24px;
  font-size: 0.78rem;
  font-weight: 600;
  color: var(--gold);
  text-decoration: none;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  transition: gap 0.2s;
}

.project-link:hover { gap: 14px; }

/* ── LOGOS ── */
#associations {
  background: var(--cream);
  padding: 60px 0;
}

.logos-label {
  text-align: center;
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-light);
  margin-bottom: 40px;
}

.logos-row {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 64px;
  flex-wrap: wrap;
}

.logo-item {
  opacity: 0.5;
  transition: opacity 0.3s;
  filter: grayscale(1);
}

.logo-item:hover { opacity: 1; filter: grayscale(0); }

.logo-item img {
  height: 48px;
  width: auto;
  display: block;
  object-fit: contain;
}

/* ── PRESS ── */
#press {
  background: var(--warm-white);
}

.press-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-top: 56px;
}

.press-card {
  border: 1px solid var(--border);
  padding: 32px 28px;
  border-radius: 2px;
  text-decoration: none;
  display: block;
  transition: all 0.25s;
  background: var(--warm-white);
  position: relative;
}

.press-card:hover {
  border-color: var(--gold);
  transform: translateY(-4px);
  box-shadow: 0 12px 40px rgba(13,43,85,0.08);
}

.press-source {
  font-size: 0.68rem;
  font-weight: 600;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 14px;
}

.press-card h3 {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.15rem;
  font-weight: 400;
  color: var(--navy);
  line-height: 1.4;
  margin-bottom: 12px;
}

.press-card p {
  font-size: 0.82rem;
  color: var(--text-muted);
  line-height: 1.6;
  font-weight: 300;
}

.press-arrow {
  position: absolute;
  bottom: 24px; right: 24px;
  font-size: 1rem;
  color: var(--gold);
  opacity: 0;
  transition: opacity 0.2s, transform 0.2s;
}

.press-card:hover .press-arrow { opacity: 1; transform: translate(4px,-4px); }

/* ── CONTACT ── */
#contact {
  background: var(--navy);
  padding: 120px 0;
  text-align: center;
  position: relative;
  overflow: hidden;
}

#contact::before {
  content: '';
  position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  width: 600px; height: 600px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(201,168,76,0.08) 0%, transparent 70%);
  pointer-events: none;
}

#contact .section-label {
  justify-content: center;
}

#contact .section-label::after { display: none; }

#contact .section-title { color: white; }

.contact-sub {
  font-size: 1.05rem;
  color: rgba(255,255,255,0.55);
  font-weight: 300;
  max-width: 520px;
  margin: 0 auto 48px;
  line-height: 1.7;
}

.contact-actions {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
  flex-wrap: wrap;
  margin-bottom: 64px;
}

.contact-email-btn {
  background: var(--gold);
  color: var(--navy);
  padding: 16px 40px;
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  text-decoration: none;
  border-radius: 2px;
  transition: all 0.25s;
}

.contact-email-btn:hover {
  background: var(--gold-light);
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(201,168,76,0.3);
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 24px;
  flex-wrap: wrap;
}

.social-link {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 10px 20px;
  border: 1px solid rgba(255,255,255,0.15);
  border-radius: 40px;
  font-size: 0.78rem;
  color: rgba(255,255,255,0.65);
  text-decoration: none;
  letter-spacing: 0.05em;
  transition: all 0.2s;
}

.social-link:hover {
  border-color: var(--gold);
  color: var(--gold);
}

/* ── FOOTER ── */
footer {
  background: #060f1e;
  padding: 32px 48px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.footer-name {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1rem;
  color: rgba(255,255,255,0.3);
  font-style: italic;
}

.footer-copy {
  font-size: 0.72rem;
  color: rgba(255,255,255,0.2);
  letter-spacing: 0.05em;
}

/* ── FADE IN ANIMATIONS ── */
.fade-in {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.7s ease, transform 0.7s ease;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}

.fade-in-delay-1 { transition-delay: 0.1s; }
.fade-in-delay-2 { transition-delay: 0.2s; }
.fade-in-delay-3 { transition-delay: 0.3s; }
.fade-in-delay-4 { transition-delay: 0.4s; }

/* ── MOBILE ── */
@media (max-width: 900px) {
  nav { padding: 16px 24px; }
  .nav-links { display: none; }
  
  #hero { grid-template-columns: 1fr; min-height: auto; }
  .hero-left { padding: 100px 32px 60px; }
  .hero-right { height: 50vw; min-height: 260px; }
  .hero-scroll { left: 32px; }
  
  .about-grid { grid-template-columns: 1fr; gap: 48px; }
  .about-photo-wrap { max-width: 320px; }
  
  .what-grid { grid-template-columns: 1fr; gap: 2px; }
  
  .exp-item { grid-template-columns: 1fr; gap: 8px; }
  
  .skills-grid { grid-template-columns: 1fr; }
  
  .projects-grid { grid-template-columns: 1fr; }
  .project-card.featured { grid-row: span 1; }
  
  .press-grid { grid-template-columns: 1fr; gap: 16px; }
  
  .container { padding: 0 24px; }
  section { padding: 72px 0; }
  
  footer { flex-direction: column; gap: 12px; text-align: center; }
}
</style>
</head>

<body>

<!-- NAV -->
<nav>
  <a href="#hero" class="nav-logo">Edwin <span>Mwangi</span></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#press">Press</a></li>
    <li><a href="#contact" class="nav-cta">Work With Me</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-left">
    <div class="hero-eyebrow">Nairobi, Kenya</div>
    <h1 class="hero-name">Edwin<br><em>Mwangi</em></h1>
    <p class="hero-title">Ecosystem Builder · Business Development · Startup Strategist</p>
    <p class="hero-statement">
      "I build systems that turn raw founders into revenue-generating companies — 
      before they ever talk to a VC."
    </p>
    <div class="hero-actions">
      <a href="#contact" class="btn-primary">Work With Me</a>
      <a href="https://www.linkedin.com/in/edwin-mwangi-103272342" target="_blank" class="btn-ghost">LinkedIn ↗</a>
    </div>
    <div class="hero-scroll">Scroll</div>
  </div>
  <div class="hero-right">
    <img src="data:image/jpeg;base64,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
