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
    <img 
