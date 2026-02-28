---
layout: null
title: ARETE — The Focus App That Asks Why Before What
permalink: /
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ARETE — The Focus App That Asks Why Before What</title>
  <meta name="description" content="Stop managing lists. Start managing attention. ARETE limits you to 2–3 tasks and asks WHY, HOW, and what makes each one worth doing." />
  <meta name="apple-itunes-app" content="app-id=6759307580" />
  <meta property="og:title" content="ARETE — The Focus App That Asks Why Before What" />
  <meta property="og:description" content="2–3 intentional tasks. Three questions. One focused day." />
  <meta property="og:url" content="https://aretetodo.com" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;0,9..40,700;1,9..40,400&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --blue: #2B4AFF;
      --purple: #B794F6;
      --cyan: #7DD3FC;
      --dark: #111418;
      --hero-bg: #080C18;
      --off-white: #F8FAFF;
      --gray: #64748B;
      --light: #F1F5F9;
      --border: #E2E8F0;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', -apple-system, sans-serif;
      background: #fff;
      color: var(--dark);
      overflow-x: hidden;
    }

    /* ── NAV ── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      height: 64px;
      padding: 0 48px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      transition: background 0.3s, border-color 0.3s;
    }
    nav.scrolled {
      background: rgba(8, 12, 24, 0.88);
      backdrop-filter: blur(24px);
      -webkit-backdrop-filter: blur(24px);
      border-bottom: 1px solid rgba(255,255,255,0.07);
    }
    .nav-logo {
      font-size: 15px;
      font-weight: 700;
      letter-spacing: 0.16em;
      color: #fff;
      text-decoration: none;
    }
    .nav-cta {
      display: flex;
      align-items: center;
      gap: 8px;
      background: #fff;
      color: var(--dark);
      font-size: 13px;
      font-weight: 600;
      text-decoration: none;
      padding: 9px 18px;
      border-radius: 100px;
      transition: opacity 0.2s, transform 0.2s;
      letter-spacing: 0.01em;
    }
    .nav-cta:hover { opacity: 0.9; transform: translateY(-1px); }

    /* ── HERO ── */
    .hero {
      min-height: 100vh;
      background: var(--hero-bg);
      display: flex;
      align-items: center;
      padding: 100px 48px 80px;
      position: relative;
      overflow: hidden;
    }
    .orb {
      position: absolute;
      border-radius: 50%;
      filter: blur(110px);
      pointer-events: none;
    }
    .orb-a { width: 680px; height: 680px; background: var(--blue); opacity: 0.28; top: -160px; left: -220px; }
    .orb-b { width: 520px; height: 520px; background: var(--purple); opacity: 0.22; bottom: -120px; right: -120px; }
    .orb-c { width: 320px; height: 320px; background: var(--cyan); opacity: 0.1; top: 35%; left: 42%; }

    .hero-inner {
      max-width: 1160px;
      margin: 0 auto;
      width: 100%;
      display: grid;
      grid-template-columns: 1fr 440px;
      gap: 64px;
      align-items: center;
      position: relative;
      z-index: 1;
    }
    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(43,74,255,0.18);
      border: 1px solid rgba(43,74,255,0.35);
      color: #93A8FF;
      font-size: 11px;
      font-weight: 600;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      padding: 5px 14px;
      border-radius: 100px;
      margin-bottom: 28px;
    }
    .hero-badge::before { content: ''; width: 6px; height: 6px; background: #93A8FF; border-radius: 50%; }
    h1 {
      font-family: 'DM Serif Display', Georgia, serif;
      font-size: clamp(40px, 4.5vw, 60px);
      font-weight: 400;
      line-height: 1.08;
      color: #fff;
      margin-bottom: 22px;
      letter-spacing: -0.01em;
    }
    h1 em {
      font-style: italic;
      background: linear-gradient(130deg, #6B8CFF 0%, var(--purple) 100%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .hero-sub {
      font-size: 17px;
      line-height: 1.7;
      color: rgba(255,255,255,0.55);
      max-width: 480px;
      margin-bottom: 40px;
      font-weight: 400;
    }
    .hero-actions { display: flex; align-items: center; gap: 20px; flex-wrap: wrap; }
    .btn-store {
      display: flex;
      align-items: center;
      gap: 12px;
      background: #fff;
      color: var(--dark);
      text-decoration: none;
      padding: 13px 22px;
      border-radius: 14px;
      box-shadow: 0 4px 28px rgba(0,0,0,0.35);
      transition: transform 0.2s, box-shadow 0.2s;
    }
    .btn-store:hover { transform: translateY(-2px); box-shadow: 0 10px 36px rgba(0,0,0,0.45); }
    .btn-store svg { width: 30px; height: 30px; flex-shrink: 0; }
    .btn-store-text { display: flex; flex-direction: column; }
    .btn-store-eyebrow { font-size: 10px; font-weight: 500; color: #94A3B8; line-height: 1; margin-bottom: 3px; }
    .btn-store-name { font-size: 16px; font-weight: 700; color: var(--dark); line-height: 1; }
    .hero-note { font-size: 12px; color: rgba(255,255,255,0.28); }

    /* ── PHONE MOCKUP ── */
    .phone-wrap {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .phone {
      width: 272px;
      height: 564px;
      background: #13161F;
      border-radius: 46px;
      border: 1.5px solid rgba(255,255,255,0.1);
      box-shadow:
        0 48px 96px rgba(0,0,0,0.55),
        0 0 0 1px rgba(255,255,255,0.04),
        inset 0 1px 0 rgba(255,255,255,0.07);
      position: relative;
      overflow: hidden;
      animation: float 5s ease-in-out infinite;
    }
    @keyframes float {
      0%, 100% { transform: translateY(0px) rotate(-1deg); }
      50% { transform: translateY(-14px) rotate(-1deg); }
    }
    .phone-island {
      position: absolute;
      top: 13px; left: 50%;
      transform: translateX(-50%);
      width: 94px; height: 28px;
      background: #000;
      border-radius: 18px;
      z-index: 5;
    }
    .phone-screen { position: absolute; inset: 0; padding: 54px 14px 18px; overflow: hidden; }

    .p-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 3px; }
    .p-wordmark { font-size: 10px; font-weight: 700; letter-spacing: 0.14em; color: rgba(255,255,255,0.85); }
    .p-circles { display: flex; gap: 3px; align-items: center; }
    .p-circle { width: 9px; height: 9px; border-radius: 50%; border: 1.5px solid; }
    .p-circle.b { border-color: var(--blue); background: rgba(43,74,255,0.35); }
    .p-circle.p { border-color: var(--purple); background: rgba(183,148,246,0.3); }
    .p-circle.c { border-color: var(--cyan); background: rgba(125,211,252,0.25); }

    .p-date { font-size: 8px; font-weight: 700; letter-spacing: 0.1em; color: var(--blue); margin: 4px 0 10px; }
    .p-title { font-size: 15px; font-weight: 700; color: #fff; margin-bottom: 3px; line-height: 1.25; }
    .p-sub { font-size: 9px; color: rgba(255,255,255,0.38); margin-bottom: 14px; line-height: 1.5; }

    .p-card {
      background: rgba(255,255,255,0.055);
      border: 1px solid rgba(255,255,255,0.09);
      border-radius: 12px;
      padding: 10px 11px;
      margin-bottom: 7px;
    }
    .p-card-title { font-size: 11px; font-weight: 600; color: #fff; margin-bottom: 7px; line-height: 1.3; }
    .p-rows { display: flex; flex-direction: column; gap: 4px; }
    .p-row { display: flex; align-items: flex-start; gap: 5px; }
    .p-badge {
      font-size: 6px; font-weight: 700; letter-spacing: 0.07em;
      padding: 2px 5px; border-radius: 3px; white-space: nowrap; flex-shrink: 0; margin-top: 1px;
    }
    .p-badge.why { background: rgba(43,74,255,0.22); color: #93A8FF; }
    .p-badge.how { background: rgba(183,148,246,0.2); color: #C4A8FF; }
    .p-badge.ful { background: rgba(125,211,252,0.18); color: #87CEEB; }
    .p-val { font-size: 8.5px; color: rgba(255,255,255,0.48); line-height: 1.45; }

    .p-add {
      display: flex; align-items: center; justify-content: center; gap: 6px;
      border: 1.5px dashed rgba(255,255,255,0.12);
      border-radius: 10px; padding: 9px; margin-top: 4px;
    }
    .p-plus {
      width: 15px; height: 15px; background: var(--blue);
      border-radius: 50%; display: flex; align-items: center; justify-content: center;
      font-size: 11px; color: #fff; font-weight: 600; line-height: 1;
    }
    .p-add-label { font-size: 9px; color: rgba(255,255,255,0.3); }

    /* ── SHARED SECTION STYLES ── */
    section { padding: 100px 48px; }
    .wrap { max-width: 1100px; margin: 0 auto; }
    .s-label { font-size: 11px; font-weight: 700; letter-spacing: 0.14em; text-transform: uppercase; color: var(--blue); margin-bottom: 14px; }
    h2 {
      font-family: 'DM Serif Display', Georgia, serif;
      font-size: clamp(30px, 3.5vw, 46px);
      font-weight: 400;
      line-height: 1.12;
      color: var(--dark);
      margin-bottom: 14px;
      letter-spacing: -0.01em;
    }
    h2 em { font-style: italic; color: var(--blue); }
    .s-intro { font-size: 17px; color: var(--gray); line-height: 1.7; max-width: 520px; margin-bottom: 60px; }

    /* ── HOW IT WORKS ── */
    .how { background: var(--off-white); }
    .steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 40px; }
    .step { position: relative; }
    .step-n {
      font-family: 'DM Serif Display', Georgia, serif;
      font-size: 80px; font-weight: 400; line-height: 1;
      color: rgba(43,74,255,0.07); display: block; margin-bottom: -28px;
    }
    .step-icon {
      width: 46px; height: 46px; border-radius: 13px;
      display: flex; align-items: center; justify-content: center;
      font-size: 20px; margin-bottom: 18px;
    }
    .step-icon.si-blue { background: rgba(43,74,255,0.1); }
    .step-icon.si-purple { background: rgba(183,148,246,0.14); }
    .step-icon.si-cyan { background: rgba(125,211,252,0.14); }
    .step-pill {
      display: inline-block;
      font-size: 10px; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase;
      padding: 3px 10px; border-radius: 100px; margin-bottom: 12px;
    }
    .sp-blue { background: rgba(43,74,255,0.1); color: var(--blue); }
    .sp-purple { background: rgba(183,148,246,0.15); color: #9B72E8; }
    .sp-cyan { background: rgba(125,211,252,0.15); color: #0EA5E9; }
    h3 { font-size: 19px; font-weight: 700; color: var(--dark); margin-bottom: 10px; line-height: 1.3; }
    .step-desc { font-size: 14px; color: var(--gray); line-height: 1.7; }

    /* ── FEATURES ── */
    .features-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
    .feat {
      background: var(--light);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 30px;
      transition: transform 0.25s, box-shadow 0.25s, border-color 0.25s;
    }
    .feat:hover {
      transform: translateY(-4px);
      box-shadow: 0 20px 48px rgba(43,74,255,0.07);
      border-color: rgba(43,74,255,0.18);
    }
    .feat-icon {
      width: 50px; height: 50px; border-radius: 14px;
      background: #fff; border: 1px solid var(--border);
      display: flex; align-items: center; justify-content: center;
      margin-bottom: 18px; font-size: 22px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    }
    .feat-title { font-size: 16px; font-weight: 700; color: var(--dark); margin-bottom: 8px; }
    .feat-desc { font-size: 14px; color: var(--gray); line-height: 1.7; }

    /* Circles SVG inside feature card */
    .rings-svg { margin-bottom: 18px; }

    /* ── QUOTE ── */
    .quote-section {
      background: var(--dark);
      padding: 80px 48px;
      text-align: center;
    }
    .quote-glyph {
      font-family: 'DM Serif Display', Georgia, serif;
      font-size: 96px; line-height: 0.75;
      color: rgba(43,74,255,0.25); display: block; margin-bottom: 20px;
    }
    blockquote {
      font-family: 'DM Serif Display', Georgia, serif;
      font-size: clamp(22px, 3vw, 38px);
      font-weight: 400; line-height: 1.35;
      color: #fff; max-width: 760px; margin: 0 auto;
    }
    blockquote em {
      font-style: italic;
      background: linear-gradient(130deg, #6B8CFF 0%, var(--purple) 100%);
      -webkit-background-clip: text; background-clip: text; color: transparent;
    }

    /* ── CTA ── */
    .cta-section {
      background: var(--hero-bg);
      text-align: center;
      padding: 120px 48px;
      position: relative;
      overflow: hidden;
    }
    .cta-orb {
      position: absolute; border-radius: 50%;
      filter: blur(100px); pointer-events: none;
      width: 500px; height: 500px;
      background: var(--blue); opacity: 0.18;
      top: 50%; left: 50%;
      transform: translate(-50%, -50%);
    }
    .cta-label { font-size: 11px; font-weight: 700; letter-spacing: 0.14em; text-transform: uppercase; color: rgba(255,255,255,0.35); margin-bottom: 18px; position: relative; z-index: 1; }
    .cta-title {
      font-family: 'DM Serif Display', Georgia, serif;
      font-size: clamp(32px, 4vw, 50px);
      color: #fff; line-height: 1.12;
      margin-bottom: 14px; position: relative; z-index: 1;
    }
    .cta-sub { font-size: 16px; color: rgba(255,255,255,0.42); margin-bottom: 40px; position: relative; z-index: 1; }
    .cta-actions { display: flex; justify-content: center; gap: 16px; flex-wrap: wrap; position: relative; z-index: 1; }

    /* ── FOOTER ── */
    footer {
      background: var(--hero-bg);
      border-top: 1px solid rgba(255,255,255,0.06);
      padding: 28px 48px;
      display: flex; align-items: center; justify-content: space-between;
      flex-wrap: wrap; gap: 12px;
    }
    .f-logo { font-size: 13px; font-weight: 700; letter-spacing: 0.14em; color: rgba(255,255,255,0.35); text-decoration: none; }
    .f-links { display: flex; gap: 24px; }
    .f-links a { font-size: 13px; color: rgba(255,255,255,0.3); text-decoration: none; transition: color 0.2s; }
    .f-links a:hover { color: rgba(255,255,255,0.65); }

    /* ── REVEAL ANIMATIONS ── */
    .reveal { opacity: 0; transform: translateY(20px); transition: opacity 0.65s ease, transform 0.65s ease; }
    .reveal.in { opacity: 1; transform: translateY(0); }
    .d1 { transition-delay: 0.08s; }
    .d2 { transition-delay: 0.16s; }
    .d3 { transition-delay: 0.24s; }
    .d4 { transition-delay: 0.32s; }

    /* ── LOOP SECTION ── */
    .loop-section { background: var(--dark); }
    .loop-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 0;
      position: relative;
    }
    .loop-grid::before {
      content: '';
      position: absolute;
      top: 27px;
      left: 12.5%; right: 12.5%;
      height: 1px;
      background: linear-gradient(90deg, rgba(43,74,255,0.5), rgba(183,148,246,0.5), rgba(125,211,252,0.4), rgba(125,211,252,0.1));
      z-index: 0;
    }
    .loop-step { text-align: center; padding: 0 16px; position: relative; z-index: 1; }
    .loop-icon {
      width: 54px; height: 54px; border-radius: 50%;
      display: flex; align-items: center; justify-content: center;
      margin: 0 auto 20px; font-size: 20px;
    }
    .li-1 { background: rgba(43,74,255,0.2); border: 1px solid rgba(43,74,255,0.4); }
    .li-2 { background: rgba(255,255,255,0.06); border: 1px solid rgba(255,255,255,0.1); }
    .li-3 { background: rgba(183,148,246,0.18); border: 1px solid rgba(183,148,246,0.3); }
    .li-4 { background: rgba(125,211,252,0.12); border: 1px solid rgba(125,211,252,0.25); }
    .loop-tag { font-size: 10px; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; color: rgba(255,255,255,0.3); margin-bottom: 8px; }
    .loop-title { font-size: 16px; font-weight: 700; color: #fff; margin-bottom: 8px; line-height: 1.3; }
    .loop-desc { font-size: 13px; color: rgba(255,255,255,0.42); line-height: 1.7; }
    @media (max-width: 800px) {
      .loop-grid { grid-template-columns: 1fr 1fr; gap: 40px; }
      .loop-grid::before { display: none; }
    }

    /* ── MOBILE ── */
    @media (max-width: 800px) {
      nav { padding: 0 20px; }
      .hero { padding: 80px 20px 60px; }
      .hero-inner { grid-template-columns: 1fr; gap: 52px; }
      .phone-wrap { order: -1; }
      .phone { width: 230px; height: 476px; border-radius: 38px; }
      section { padding: 72px 20px; }
      .steps { grid-template-columns: 1fr; gap: 44px; }
      .features-grid { grid-template-columns: 1fr; gap: 14px; }
      .quote-section, .cta-section { padding: 64px 20px; }
      footer { padding: 24px 20px; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav id="nav">
  <a href="/" class="nav-logo">ARETE</a>
  <a href="https://apps.apple.com/app/id6759307580" class="nav-cta" target="_blank" rel="noopener">
    <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.32-3.14-2.53C4.25 17 2.94 12.45 4.7 9.39c.87-1.52 2.43-2.48 4.12-2.51 1.28-.02 2.5.87 3.29.87.78 0 2.26-1.07 3.8-.91.65.03 2.47.26 3.64 1.98-.09.06-2.17 1.28-2.15 3.81.03 3.02 2.65 4.03 2.68 4.04-.03.07-.42 1.44-1.38 2.83M13 3.5c.73-.83 1.94-1.46 2.94-1.5.13 1.17-.34 2.35-1.04 3.19-.69.85-1.83 1.51-2.95 1.42-.15-1.15.41-2.35 1.05-3.11z"/></svg>
    Download
  </a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="orb orb-a"></div>
  <div class="orb orb-b"></div>
  <div class="orb orb-c"></div>

  <div class="hero-inner">
    <div class="hero-copy">
      <div class="hero-badge">iOS App · Free Download</div>
      <h1>The focus app that asks <em>why</em> before <em>what.</em></h1>
      <p class="hero-sub">Stop managing lists. Start managing attention. ARETE limits you to 2–3 intentional tasks, asks WHY, HOW, and what makes each one fulfilling — then checks in after, so you don't just complete work, you understand it.</p>
      <div class="hero-actions">
        <a href="https://apps.apple.com/app/id6759307580" class="btn-store" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" fill="#111418"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.32-3.14-2.53C4.25 17 2.94 12.45 4.7 9.39c.87-1.52 2.43-2.48 4.12-2.51 1.28-.02 2.5.87 3.29.87.78 0 2.26-1.07 3.8-.91.65.03 2.47.26 3.64 1.98-.09.06-2.17 1.28-2.15 3.81.03 3.02 2.65 4.03 2.68 4.04-.03.07-.42 1.44-1.38 2.83M13 3.5c.73-.83 1.94-1.46 2.94-1.5.13 1.17-.34 2.35-1.04 3.19-.69.85-1.83 1.51-2.95 1.42-.15-1.15.41-2.35 1.05-3.11z"/></svg>
          <div class="btn-store-text">
            <span class="btn-store-eyebrow">Download on the</span>
            <span class="btn-store-name">App Store</span>
          </div>
        </a>
        <span class="hero-note">Free · iOS 17+</span>
      </div>
    </div>

    <div class="phone-wrap">
      <div class="phone">
        <div class="phone-island"></div>
        <div class="phone-screen">
          <div class="p-header">
            <span class="p-wordmark">ARETE</span>
            <div class="p-circles">
              <div class="p-circle b"></div>
              <div class="p-circle p"></div>
              <div class="p-circle c"></div>
            </div>
          </div>
          <div class="p-date">SATURDAY, FEBRUARY 28</div>
          <div class="p-title">Your high-impact work</div>
          <p class="p-sub">Enter 2 or 3 tasks that truly matter.</p>

          <div class="p-card">
            <div class="p-card-title">Deep work on Q1 strategy</div>
            <div class="p-rows">
              <div class="p-row">
                <span class="p-badge why">WHY</span>
                <span class="p-val">Sets direction for the whole team</span>
              </div>
              <div class="p-row">
                <span class="p-badge how">HOW</span>
                <span class="p-val">Block 3h, close Slack</span>
              </div>
              <div class="p-row">
                <span class="p-badge ful">FULFILLMENT</span>
                <span class="p-val">Clarity and momentum</span>
              </div>
            </div>
          </div>

          <div class="p-card">
            <div class="p-card-title">Call with mentor</div>
            <div class="p-rows">
              <div class="p-row">
                <span class="p-badge why">WHY</span>
                <span class="p-val">Get unstuck on the hiring decision</span>
              </div>
            </div>
          </div>

          <div class="p-add">
            <div class="p-plus">+</div>
            <span class="p-add-label">Add high-impact task</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- HOW IT WORKS -->
<section class="how">
  <div class="wrap">
    <div class="s-label reveal">How it works</div>
    <h2 class="reveal">Three questions.<br>One intentional task.</h2>
    <p class="s-intro reveal">Before you add anything, ARETE asks you to slow down for 30 seconds. That pause is the whole product.</p>

    <div class="steps">
      <div class="step reveal d1">
        <span class="step-n">01</span>
        <div class="step-icon si-blue">🎯</div>
        <span class="step-pill sp-blue">WHY</span>
        <h3>Write your purpose</h3>
        <p class="step-desc">Why does this task actually matter? Tasks with a clear purpose get done. Tasks without one get postponed forever.</p>
      </div>
      <div class="step reveal d2">
        <span class="step-n">02</span>
        <div class="step-icon si-purple">🗺️</div>
        <span class="step-pill sp-purple">HOW</span>
        <h3>Define your approach</h3>
        <p class="step-desc">What's your first move? Removing the decision of how to start eliminates the friction that causes procrastination before it begins.</p>
      </div>
      <div class="step reveal d3">
        <span class="step-n">03</span>
        <div class="step-icon si-cyan">✨</div>
        <span class="step-pill sp-cyan">FULFILLMENT</span>
        <h3>Connect to meaning</h3>
        <p class="step-desc">What will make this worth doing? Linking effort to personal meaning is what separates tasks you finish from tasks you avoid.</p>
      </div>
    </div>
  </div>
</section>

<!-- THE LOOP -->
<section class="loop-section">
  <div class="wrap">
    <div class="s-label reveal" style="color: rgba(255,255,255,0.35);">The complete system</div>
    <h2 class="reveal" style="color: #fff; margin-bottom: 14px;">Most apps end when you check the box.<br><em style="color: var(--cyan);">ARETE starts there.</em></h2>
    <p class="s-intro reveal" style="color: rgba(255,255,255,0.45);">Every task is part of a loop — intention, action, reflection, growth. That loop compounds. Over weeks, it reveals more about how you work than any other tool can.</p>

    <div class="loop-grid">
      <div class="loop-step reveal d1">
        <div class="loop-icon li-1">🎯</div>
        <div class="loop-tag">Plan</div>
        <div class="loop-title">Add with intention</div>
        <p class="loop-desc">Choose 2–3 tasks. Answer WHY it matters, HOW you'll approach it, and what makes it FULFILLING — before it goes on your list.</p>
      </div>
      <div class="loop-step reveal d2">
        <div class="loop-icon li-2">⚡</div>
        <div class="loop-tag">Do</div>
        <div class="loop-title">Execute with clarity</div>
        <p class="loop-desc">Your first move is already planned. The purpose is clear. Starting is the easiest part — because you've already done the thinking.</p>
      </div>
      <div class="loop-step reveal d3">
        <div class="loop-icon li-3">💬</div>
        <div class="loop-tag">Reflect</div>
        <div class="loop-title">Close the loop</div>
        <p class="loop-desc">30 seconds after each task. How was your energy? Did the approach work? That signal compounds into patterns no other app collects.</p>
      </div>
      <div class="loop-step reveal d4">
        <div class="loop-icon li-4">◎</div>
        <div class="loop-tag">Grow</div>
        <div class="loop-title">Watch practice build</div>
        <p class="loop-desc">Three circles — WHY, HOW, FULFILLMENT — fill as you show up consistently. Not streaks. Not points. Visible evidence of your practice.</p>
      </div>
    </div>
  </div>
</section>

<!-- FEATURES -->
<section>
  <div class="wrap">
    <div class="s-label reveal">What makes it work</div>
    <h2 class="reveal">Designed around the loop.<br><em>Not around the list.</em></h2>
    <p class="s-intro reveal">Every feature exists to close the gap between intention and understanding — not to add more things to track.</p>

    <div class="features-grid">
      <div class="feat reveal d1">
        <div class="feat-icon">⚡</div>
        <div class="feat-title">Energy Reflection</div>
        <p class="feat-desc">After every task, rate your energy and whether your approach worked. 30 seconds. The data that makes everything else possible — and that no competitor collects.</p>
      </div>
      <div class="feat reveal d2">
        <div class="feat-icon">📊</div>
        <div class="feat-title">Weekly AI Insights</div>
        <p class="feat-desc">After 5 active days, AI surfaces your patterns: what energized you, which approaches stuck, and what conditions bring out your best work — personalized, every week.</p>
      </div>
      <div class="feat reveal d3">
        <div class="feat-icon">
          <svg width="28" height="28" viewBox="0 0 28 28" fill="none">
            <circle cx="14" cy="14" r="11" stroke="#2B4AFF" stroke-width="2.5" stroke-dasharray="48 21" stroke-linecap="round" transform="rotate(-90 14 14)"/>
            <circle cx="14" cy="14" r="7.5" stroke="#B794F6" stroke-width="2.5" stroke-dasharray="32 15" stroke-linecap="round" transform="rotate(-90 14 14)"/>
            <circle cx="14" cy="14" r="4" stroke="#7DD3FC" stroke-width="2.5" stroke-dasharray="18 7" stroke-linecap="round" transform="rotate(-90 14 14)"/>
          </svg>
        </div>
        <div class="feat-title">Practice Circles</div>
        <p class="feat-desc">Three rings — WHY, HOW, FULFILLMENT — fill as you build the habit of intentional work. Consistency over perfection. Showing up is the practice.</p>
      </div>
    </div>
  </div>
</section>

<!-- PULL QUOTE -->
<div class="quote-section">
  <span class="quote-glyph">"</span>
  <blockquote>Other apps track what you did.<br><em>ARETE helps you understand how it felt</em> — and builds from there.</blockquote>
</div>

<!-- CTA -->
<section class="cta-section">
  <div class="cta-orb"></div>
  <p class="cta-label">Free on the App Store</p>
  <h2 class="cta-title">Start doing less.<br>Accomplish more.</h2>
  <p class="cta-sub">Join thousands building intentional focus habits with ARETE.</p>
  <div class="cta-actions">
    <a href="https://apps.apple.com/app/id6759307580" class="btn-store" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="#111418"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.32-3.14-2.53C4.25 17 2.94 12.45 4.7 9.39c.87-1.52 2.43-2.48 4.12-2.51 1.28-.02 2.5.87 3.29.87.78 0 2.26-1.07 3.8-.91.65.03 2.47.26 3.64 1.98-.09.06-2.17 1.28-2.15 3.81.03 3.02 2.65 4.03 2.68 4.04-.03.07-.42 1.44-1.38 2.83M13 3.5c.73-.83 1.94-1.46 2.94-1.5.13 1.17-.34 2.35-1.04 3.19-.69.85-1.83 1.51-2.95 1.42-.15-1.15.41-2.35 1.05-3.11z"/></svg>
      <div class="btn-store-text">
        <span class="btn-store-eyebrow">Download on the</span>
        <span class="btn-store-name">App Store</span>
      </div>
    </a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <a href="/" class="f-logo">ARETE</a>
  <div class="f-links">
    <a href="/privacy-policy">Privacy Policy</a>
    <a href="/terms-of-service">Terms of Service</a>
  </div>
</footer>

<script>
  // Nav frosted glass on scroll
  const nav = document.getElementById('nav');
  window.addEventListener('scroll', () => {
    nav.classList.toggle('scrolled', window.scrollY > 24);
  }, { passive: true });

  // Scroll reveal
  const obs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) { e.target.classList.add('in'); obs.unobserve(e.target); }
    });
  }, { threshold: 0.12 });
  document.querySelectorAll('.reveal').forEach(el => obs.observe(el));
</script>
</body>
</html>
