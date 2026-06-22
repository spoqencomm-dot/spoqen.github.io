<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Alim — MC · Host · Speaker</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=DM+Sans:wght@300;400;500&family=Space+Mono:wght@400;700&family=Dancing+Script:wght@600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --white:      #FFFFFF;
    --off-white:  #F5F5F5;
    --navy:       #0D0D5E;
    --blue:       #2D2FB5;
    --blue-mid:   #3D3FCC;
    --blue-light: #5658E0;
    --black:      #111111;
    --gray-text:  #555566;
    --border:     #E0E0F0;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--white);
    color: var(--black);
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 1.1rem 2.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(255,255,255,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }

  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    font-weight: 900;
    letter-spacing: 0.08em;
    color: var(--navy);
    text-decoration: none;
  }

  .nav-links { display: flex; gap: 2rem; list-style: none; }

  .nav-links a {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gray-text);
    text-decoration: none;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--blue); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    background: var(--white);
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 0 2.5rem 5rem;
    position: relative;
    overflow: hidden;
  }

  /* Blue corner accent — mirrors PDF style */
  .hero::before {
    content: '';
    position: absolute;
    top: 0; right: 0;
    width: 220px; height: 220px;
    background: var(--navy);
    clip-path: polygon(100% 0, 0 0, 100% 100%);
  }

  .hero::after {
    content: '';
    position: absolute;
    top: 0; right: 0;
    width: 130px; height: 130px;
    background: var(--blue-mid);
    clip-path: polygon(100% 0, 0 0, 100% 100%);
  }

  .hero-eyebrow {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.28em;
    text-transform: uppercase;
    color: var(--blue);
    margin-bottom: 1rem;
    opacity: 0;
    animation: fadeUp 0.7s 0.2s forwards;
  }

  .hero-name {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: clamp(5rem, 18vw, 15rem);
    line-height: 0.88;
    color: var(--navy);
    opacity: 0;
    animation: fadeUp 0.7s 0.35s forwards;
  }

  .hero-script {
    font-family: 'Dancing Script', cursive;
    font-size: clamp(2rem, 6vw, 4.5rem);
    color: var(--blue-mid);
    line-height: 1;
    margin-top: 0.3rem;
    opacity: 0;
    animation: fadeUp 0.7s 0.5s forwards;
  }

  .hero-tagline {
    margin-top: 2rem;
    max-width: 460px;
    font-size: 1rem;
    line-height: 1.7;
    color: var(--gray-text);
    opacity: 0;
    animation: fadeUp 0.7s 0.65s forwards;
  }

  .hero-roles {
    margin-top: 2rem;
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
    opacity: 0;
    animation: fadeUp 0.7s 0.8s forwards;
  }

  .role-pill {
    padding: 0.4rem 1rem;
    border: 1.5px solid var(--blue-mid);
    font-family: 'Space Mono', monospace;
    font-size: 0.6rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--blue-mid);
    border-radius: 2px;
  }

  .hero-scroll {
    position: absolute;
    right: 2.5rem; bottom: 3rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.58rem;
    letter-spacing: 0.2em;
    color: var(--gray-text);
    text-transform: uppercase;
    opacity: 0;
    animation: fadeUp 0.7s 1.1s forwards;
  }

  .scroll-line {
    width: 1px; height: 55px;
    background: linear-gradient(to bottom, var(--navy), transparent);
    animation: scrollAnim 2s 1.4s infinite;
  }

  @keyframes scrollAnim {
    0%   { transform: scaleY(0); transform-origin: top; }
    50%  { transform: scaleY(1); transform-origin: top; }
    51%  { transform-origin: bottom; }
    100% { transform: scaleY(0); transform-origin: bottom; }
  }

  /* ── STATS BAND ── */
  .stats-band {
    background: var(--navy);
    padding: 2.8rem 2.5rem;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }

  .stat { text-align: center; }

  .stat-number {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: clamp(2.5rem, 6vw, 4rem);
    color: var(--white);
    line-height: 1;
  }

  .stat-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.6rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.45);
    margin-top: 0.4rem;
  }

  /* ── SECTION SHARED ── */
  section { padding: 6rem 2.5rem; }

  .section-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--blue);
    margin-bottom: 3rem;
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .section-label::after {
    content: '';
    flex: 1;
    max-width: 100px;
    height: 1px;
    background: var(--border);
  }

  /* ── WORK GRID ── */
  .work-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
  }

  .work-card {
    background: var(--white);
    padding: 2.5rem 2rem;
    position: relative;
    overflow: hidden;
    transition: background 0.25s;
  }

  .work-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0;
    height: 3px;
    width: 0;
    background: var(--blue-mid);
    transition: width 0.35s ease;
  }

  .work-card:hover { background: #F8F8FF; }
  .work-card:hover::after { width: 100%; }

  .card-lang {
    font-family: 'Space Mono', monospace;
    font-size: 0.58rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--blue);
    margin-bottom: 0.7rem;
  }

  .card-role {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: 2rem;
    color: var(--navy);
    line-height: 1.1;
    margin-bottom: 0.4rem;
  }

  .card-event {
    font-size: 0.9rem;
    font-weight: 500;
    color: var(--blue-mid);
    margin-bottom: 1.2rem;
  }

  .card-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; }

  .tag {
    font-family: 'Space Mono', monospace;
    font-size: 0.52rem;
    letter-spacing: 0.08em;
    padding: 0.2rem 0.55rem;
    border: 1px solid var(--border);
    color: var(--gray-text);
    text-transform: uppercase;
    border-radius: 2px;
  }

  /* ── ABOUT ── */
  #about { background: var(--off-white); }

  .about-inner {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: start;
  }

  .about-headline {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: clamp(2.2rem, 4.5vw, 3.5rem);
    color: var(--navy);
    line-height: 1.1;
    margin-bottom: 2rem;
  }

  .about-headline em { color: var(--blue-mid); font-style: italic; }

  .about-body { font-size: 1rem; line-height: 1.8; color: var(--gray-text); }
  .about-body p + p { margin-top: 1.2rem; }

  .skills-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
  }

  .skills-list li {
    padding: 1rem 1.4rem;
    background: var(--white);
    font-family: 'Space Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: var(--navy);
    transition: background 0.2s;
  }

  .skills-list li:hover { background: #EEEEFF; }

  .skills-list li span {
    color: var(--blue);
    font-size: 0.55rem;
  }

  /* ── MENTORING ── */
  .mentor-inner {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 4rem;
    align-items: center;
  }

  .mentor-number {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: clamp(6rem, 14vw, 11rem);
    color: transparent;
    -webkit-text-stroke: 2px var(--blue-mid);
    line-height: 1;
    opacity: 0.2;
  }

  .mentor-content h2 {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: clamp(2rem, 3.5vw, 2.8rem);
    color: var(--navy);
    line-height: 1.15;
    margin-bottom: 1.2rem;
  }

  .mentor-content h2 em { color: var(--blue-mid); font-style: italic; }

  .mentor-content p {
    font-size: 1rem;
    line-height: 1.78;
    color: var(--gray-text);
    max-width: 500px;
  }

  .pillars {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-top: 2rem;
  }

  .pillar {
    background: var(--off-white);
    padding: 1.2rem 1.4rem;
    border-top: 3px solid var(--blue-mid);
  }

  .pillar-title {
    font-family: 'Space Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--blue);
    margin-bottom: 0.4rem;
  }

  .pillar-desc {
    font-size: 0.85rem;
    color: var(--gray-text);
    line-height: 1.5;
  }

  /* ── PODCAST ── */
  #podcast { background: var(--navy); }

  #podcast .section-label { color: rgba(255,255,255,0.4); }
  #podcast .section-label::after { background: rgba(255,255,255,0.1); }

  .podcast-inner {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
  }

  .podcast-inner h2 {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: clamp(2rem, 4vw, 3rem);
    color: var(--white);
    line-height: 1.1;
    margin-bottom: 1.2rem;
  }

  .podcast-inner h2 span { font-style: italic; color: rgba(255,255,255,0.45); }

  .podcast-inner p {
    font-size: 0.95rem;
    color: rgba(255,255,255,0.55);
    line-height: 1.8;
    margin-bottom: 1.5rem;
  }

  .podcast-link {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--white);
    text-decoration: none;
    border-bottom: 1px solid rgba(255,255,255,0.4);
    padding-bottom: 2px;
    transition: border-color 0.2s, color 0.2s;
  }

  .podcast-link:hover { color: var(--off-white); border-color: var(--white); }

  .podcast-rows { display: flex; flex-direction: column; gap: 1px; }

  .podcast-row {
    background: rgba(255,255,255,0.05);
    padding: 1.1rem 1.4rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.4);
    border-left: 2.5px solid rgba(255,255,255,0.12);
    transition: background 0.2s, border-color 0.2s;
  }

  .podcast-row:first-child { border-left-color: var(--blue-light); color: rgba(255,255,255,0.75); }
  .podcast-row:hover { background: rgba(255,255,255,0.09); }

  /* ── CONTACT ── */
  #contact { background: var(--white); text-align: center; }

  .contact-headline {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: clamp(3rem, 10vw, 8rem);
    line-height: 0.9;
    color: var(--navy);
    margin-bottom: 1.5rem;
  }

  .contact-headline em { font-style: italic; color: var(--blue-mid); }

  .contact-sub {
    font-size: 1rem;
    color: var(--gray-text);
    margin-bottom: 3rem;
  }

  .contact-links {
    display: flex;
    justify-content: center;
    gap: 3rem;
    flex-wrap: wrap;
  }

  .contact-link { display: flex; flex-direction: column; align-items: center; gap: 0.35rem; text-decoration: none; }

  .contact-link-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.58rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--gray-text);
  }

  .contact-link-value {
    font-size: 0.95rem;
    color: var(--navy);
    font-weight: 500;
    transition: color 0.2s;
  }

  .contact-link:hover .contact-link-value { color: var(--blue-mid); }

  .cta-button {
    display: inline-block;
    margin-top: 3.5rem;
    padding: 1rem 2.8rem;
    background: var(--navy);
    color: var(--white);
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: 700;
    transition: background 0.2s, transform 0.2s;
  }

  .cta-button:hover { background: var(--blue-mid); transform: translateY(-2px); }

  /* ── FOOTER ── */
  footer {
    padding: 2rem 2.5rem;
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-family: 'Space Mono', monospace;
    font-size: 0.58rem;
    letter-spacing: 0.12em;
    color: var(--gray-text);
    text-transform: uppercase;
    background: var(--white);
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .reveal {
    opacity: 0;
    transform: translateY(28px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.2rem; }
    .nav-links { display: none; }
    .hero { padding: 0 1.2rem 4rem; }
    .hero::before, .hero::after { width: 100px; height: 100px; }
    section { padding: 4rem 1.2rem; }
    .stats-band { grid-template-columns: 1fr; padding: 2rem 1.2rem; }
    .about-inner { grid-template-columns: 1fr; gap: 2.5rem; }
    .mentor-inner { grid-template-columns: 1fr; gap: 1rem; }
    .mentor-number { display: none; }
    .pillars { grid-template-columns: 1fr; }
    .podcast-inner { grid-template-columns: 1fr; gap: 2rem; }
    .work-grid { grid-template-columns: 1fr; }
    footer { flex-direction: column; gap: 0.6rem; text-align: center; }
  }

  @media (prefers-reduced-motion: reduce) {
    .scroll-line, .hero-eyebrow, .hero-name, .hero-script, .hero-tagline, .hero-roles, .hero-scroll { animation: none; opacity: 1; }
    .reveal { opacity: 1; transform: none; transition: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">Alim</a>
  <ul class="nav-links">
    <li><a href="#work">Work</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#mentoring">Mentoring</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-eyebrow">MC · Host · Speaker · Mentor</div>
  <h1 class="hero-name">ALIM</h1>
  <div class="hero-script">Portfolio</div>
  <p class="hero-tagline">Bilingual presence that turns events into experiences — from international symposiums to grassroots talkshows.</p>
  <div class="hero-roles">
    <div class="role-pill">English</div>
    <div class="role-pill">Bahasa Indonesia</div>
    <div class="role-pill">2022 – 2026</div>
  </div>
  <div class="hero-scroll">
    <div class="scroll-line"></div>
    Scroll
  </div>
</section>

<!-- STATS BAND -->
<div class="stats-band reveal">
  <div class="stat">
    <div class="stat-number">100+</div>
    <div class="stat-label">Students Mentored</div>
  </div>
  <div class="stat">
    <div class="stat-number">8</div>
    <div class="stat-label">Podcast Episodes</div>
  </div>
  <div class="stat">
    <div class="stat-number">2</div>
    <div class="stat-label">Languages</div>
  </div>
</div>

<!-- WORK -->
<section id="work">
  <div class="section-label">Selected Work</div>
  <div class="work-grid">

    <div class="work-card reveal">
      <div class="card-lang">English</div>
      <div class="card-role">MC</div>
      <div class="card-event">International Symposium &amp; Exhibition</div>
      <div class="card-tags">
        <span class="tag">Engaging</span>
        <span class="tag">Collaborative</span>
        <span class="tag">Spectacular</span>
        <span class="tag">Executives</span>
        <span class="tag">Long-prep</span>
      </div>
    </div>

    <div class="work-card reveal">
      <div class="card-lang">Bahasa Indonesia</div>
      <div class="card-role">MC</div>
      <div class="card-event">HIPMI Goes to School</div>
      <div class="card-tags">
        <span class="tag">Fun</span>
        <span class="tag">Engaging</span>
        <span class="tag">Euphoria</span>
        <span class="tag">Short-prep</span>
      </div>
    </div>

    <div class="work-card reveal">
      <div class="card-lang">Bilingual</div>
      <div class="card-role">Host</div>
      <div class="card-event">International Talk with Halim</div>
      <div class="card-tags">
        <span class="tag">Casual</span>
        <span class="tag">Deep Dive</span>
        <span class="tag">Inspirational</span>
        <span class="tag">Soft-selling</span>
      </div>
    </div>

    <div class="work-card reveal">
      <div class="card-lang">English</div>
      <div class="card-role">Speaker</div>
      <div class="card-event">OSPEK — International School, Telkom University</div>
      <div class="card-tags">
        <span class="tag">Friendly</span>
        <span class="tag">Interactive</span>
        <span class="tag">High Energy</span>
        <span class="tag">Inspirational</span>
      </div>
    </div>

    <div class="work-card reveal">
      <div class="card-lang">Bahasa Indonesia</div>
      <div class="card-role">Speaker</div>
      <div class="card-event">Cafladoepa University Fair Talkshow</div>
      <div class="card-tags">
        <span class="tag">Casual</span>
        <span class="tag">Sharp Delivery</span>
        <span class="tag">Audience-Centered</span>
        <span class="tag">Inspirational</span>
      </div>
    </div>

    <div class="work-card reveal" style="display:flex; align-items:center; justify-content:center; min-height:220px; background:#F8F8FF;">
      <a href="https://wa.me/6282283504397" style="text-decoration:none; text-align:center;">
        <div style="font-family:'Playfair Display',serif; font-weight:900; font-size:1.5rem; color:var(--navy); margin-bottom:0.5rem;">Your Event Next?</div>
        <div style="font-family:'Space Mono',monospace; font-size:0.62rem; letter-spacing:0.16em; color:var(--blue); text-transform:uppercase;">Get in touch →</div>
      </a>
    </div>

  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">About</div>
  <div class="about-inner">
    <div class="reveal">
      <h2 class="about-headline">Stage presence is a <em>craft</em>,<br>not a gift.</h2>
      <div class="about-body">
        <p>Alim is a bilingual MC, Host, and Speaker who brings commanding energy to international symposiums and intimate talkshows alike. With years of experience across English and Bahasa Indonesia, he adapts his delivery to the room — whether that's boardroom executives or university freshmen.</p>
        <p>From high-stakes international exhibitions to spontaneous campus events, Alim's signature is reading the audience and elevating the moment. Every event gets his full attention, long before the microphone is live.</p>
      </div>
    </div>
    <div class="reveal">
      <ul class="skills-list">
        <li>Persona Building <span>Core Skill</span></li>
        <li>Communication Psychology <span>Core Skill</span></li>
        <li>Mentality Awareness <span>Core Skill</span></li>
        <li>Technical Development <span>Core Skill</span></li>
        <li>Bilingual Delivery <span>EN / ID</span></li>
        <li>Audience Reading <span>Live Adaptation</span></li>
      </ul>
    </div>
  </div>
</section>

<!-- MENTORING -->
<section id="mentoring">
  <div class="section-label">Public Speaking Class</div>
  <div class="mentor-inner">
    <div class="mentor-number reveal">100+</div>
    <div class="mentor-content reveal">
      <h2>Training the <em>Next</em> Generation of Communicators</h2>
      <p>Alim runs a bilingual Public Speaking class that has shaped over 100 students. The curriculum goes beyond microphone technique — it builds confidence, mental resilience, and a personal communication identity.</p>
      <div class="pillars">
        <div class="pillar">
          <div class="pillar-title">Persona Building</div>
          <div class="pillar-desc">Define your authentic voice on stage</div>
        </div>
        <div class="pillar">
          <div class="pillar-title">Comm Psychology</div>
          <div class="pillar-desc">Understand how audiences receive you</div>
        </div>
        <div class="pillar">
          <div class="pillar-title">Mentality Awareness</div>
          <div class="pillar-desc">Own your nerves, don't fight them</div>
        </div>
        <div class="pillar">
          <div class="pillar-title">Technical Skills</div>
          <div class="pillar-desc">Diction, pacing, breathing, presence</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PODCAST -->
<section id="podcast">
  <div class="section-label">Podcast</div>
  <div class="podcast-inner">
    <div class="reveal">
      <h2>International Talk <span>with Halim</span></h2>
      <p>8 episodes featuring globally experienced guests. Deep conversations designed to trigger insights, inspire action, and challenge perspective — in a casual, long-form bilingual format.</p>
      <a class="podcast-link" href="mailto:halimdwiputra00@gmail.com">Watch Episodes →</a>
    </div>
    <div class="reveal">
      <div class="podcast-rows">
        <div class="podcast-row">Casual · Bilingual Format</div>
        <div class="podcast-row">Deep Dive Conversations</div>
        <div class="podcast-row">Global Guest Speakers</div>
        <div class="podcast-row">8 Episodes Released</div>
        <div class="podcast-row">Inspirational · Soft-selling</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-label" style="justify-content:center;">Contact</div>
  <h2 class="contact-headline reveal">LET'S <em>WORK</em><br>TOGETHER</h2>
  <p class="contact-sub reveal">Available for MC, Hosting, Speaking &amp; Mentoring engagements.</p>
  <div class="contact-links reveal">
    <a class="contact-link" href="https://wa.me/6282283504397">
      <span class="contact-link-label">WhatsApp</span>
      <span class="contact-link-value">082 2835 04397</span>
    </a>
    <a class="contact-link" href="mailto:halimdwiputra00@gmail.com">
      <span class="contact-link-label">Email</span>
      <span class="contact-link-value">halimdwiputra00@gmail.com</span>
    </a>
  </div>
  <a class="cta-button reveal" href="https://wa.me/6282283504397">Book Alim for Your Event</a>
</section>

<footer>
  <span>© 2026 Alim</span>
  <span>MC · Host · Speaker · Mentor</span>
</footer>

<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((e, i) => {
      if (e.isIntersecting) {
        setTimeout(() => e.target.classList.add('visible'), i * 80);
        observer.unobserve(e.target);
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
</body>
</html>
