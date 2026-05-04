
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Angela Leng | Business Partner Contable & RRHH</title>
  <meta name="description" content="Angela Leng – Intrapreneur, Contadora & HR. Business Partner estratégico para empresas del sector agro en Perú." />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />
  <style>
    /* ─────────────────────────────────────────────
       VARIABLES & RESET
    ───────────────────────────────────────────── */
    :root {
      --matcha-dark:   #3B4A28;
      --matcha:        #5C6E35;
      --matcha-mid:    #7A8E4A;
      --matcha-light:  #A8BC6F;
      --matcha-pale:   #D4DFB0;
      --cream:         #F4F1E8;
      --cream-dark:    #E8E3D0;
      --soil:          #7B5E3A;
      --soil-light:    #A07D55;
      --white:         #FAFAF5;
      --text-dark:     #1C2410;
      --text-mid:      #3D4A2A;
      --text-light:    #6B7A52;
      --shadow-sm:     0 2px 12px rgba(60,74,40,.10);
      --shadow-md:     0 8px 32px rgba(60,74,40,.15);
      --shadow-lg:     0 20px 60px rgba(60,74,40,.20);
      --radius:        14px;
      --radius-sm:     8px;
      --transition:    .35s cubic-bezier(.4,0,.2,1);
    }
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; font-size: 16px; }
    body {
      font-family: 'Inter', sans-serif;
      background: var(--white);
      color: var(--text-dark);
      overflow-x: hidden;
    }
    img { max-width: 100%; display: block; }
    a { text-decoration: none; color: inherit; }
    ul { list-style: none; }

    /* ─────────────────────────────────────────────
       SCROLLBAR
    ───────────────────────────────────────────── */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: var(--cream); }
    ::-webkit-scrollbar-thumb { background: var(--matcha-light); border-radius: 3px; }

    /* ─────────────────────────────────────────────
       UTILITY
    ───────────────────────────────────────────── */
    .container { width: 100%; max-width: 1140px; margin: 0 auto; padding: 0 1.5rem; }
    .section-tag {
      display: inline-flex; align-items: center; gap: .5rem;
      font-size: .75rem; font-weight: 600; letter-spacing: .12em;
      text-transform: uppercase; color: var(--matcha);
      background: var(--matcha-pale); border-radius: 20px;
      padding: .35rem .9rem; margin-bottom: 1rem;
    }
    .section-tag svg { width: 14px; height: 14px; }
    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1.8rem, 4vw, 2.6rem);
      color: var(--matcha-dark);
      line-height: 1.22;
      margin-bottom: 1rem;
    }
    .section-subtitle {
      font-size: 1.05rem; color: var(--text-light);
      line-height: 1.7; max-width: 540px;
    }
    .btn {
      display: inline-flex; align-items: center; gap: .5rem;
      padding: .85rem 2rem; border-radius: 50px;
      font-size: .95rem; font-weight: 600;
      cursor: pointer; transition: var(--transition);
      border: none;
    }
    .btn-primary {
      background: var(--matcha); color: var(--white);
      box-shadow: 0 4px 20px rgba(92,110,53,.35);
    }
    .btn-primary:hover {
      background: var(--matcha-dark);
      box-shadow: 0 6px 28px rgba(92,110,53,.45);
      transform: translateY(-2px);
    }
    .btn-outline {
      background: transparent; color: var(--matcha);
      border: 2px solid var(--matcha);
    }
    .btn-outline:hover {
      background: var(--matcha); color: var(--white);
      transform: translateY(-2px);
    }

    /* ─────────────────────────────────────────────
       LEAF DECORATION (SVG inline)
    ───────────────────────────────────────────── */
    .deco-leaf {
      position: absolute; pointer-events: none;
      opacity: .12; z-index: 0;
    }

    /* ─────────────────────────────────────────────
       NAVBAR
    ───────────────────────────────────────────── */
    #navbar {
      position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
      padding: 1.1rem 0;
      transition: var(--transition);
    }
    #navbar.scrolled {
      background: rgba(250,250,245,.96);
      backdrop-filter: blur(18px);
      box-shadow: 0 2px 20px rgba(60,74,40,.10);
      padding: .75rem 0;
    }
    .nav-inner {
      display: flex; align-items: center; justify-content: space-between;
    }
    .nav-logo {
      display: flex; align-items: center; gap: .7rem;
    }
    .nav-logo-icon {
      width: 40px; height: 40px; border-radius: 10px;
      background: linear-gradient(135deg, var(--matcha), var(--matcha-light));
      display: flex; align-items: center; justify-content: center;
      flex-shrink: 0;
    }
    .nav-logo-icon svg { width: 22px; height: 22px; color: #fff; }
    .nav-logo-text { line-height: 1.2; }
    .nav-logo-name {
      font-family: 'Playfair Display', serif;
      font-weight: 700; font-size: 1.1rem; color: var(--matcha-dark);
    }
    .nav-logo-sub {
      font-size: .7rem; color: var(--text-light); font-weight: 500;
      letter-spacing: .06em; text-transform: uppercase;
    }
    .nav-links {
      display: flex; align-items: center; gap: 2rem;
    }
    .nav-links a {
      font-size: .9rem; font-weight: 500; color: var(--text-mid);
      position: relative; transition: color var(--transition);
    }
    .nav-links a::after {
      content: ''; position: absolute; bottom: -4px; left: 0;
      width: 0; height: 2px; background: var(--matcha);
      transition: width var(--transition);
    }
    .nav-links a:hover { color: var(--matcha); }
    .nav-links a:hover::after { width: 100%; }
    .nav-cta { display: none; }
    @media(min-width: 768px) { .nav-cta { display: inline-flex; } }

    /* Hamburger */
    .hamburger {
      display: flex; flex-direction: column; gap: 5px;
      cursor: pointer; padding: .4rem; border: none;
      background: none;
    }
    .hamburger span {
      width: 24px; height: 2px;
      background: var(--matcha-dark);
      border-radius: 2px;
      transition: var(--transition);
      display: block;
    }
    .hamburger.open span:nth-child(1) { transform: rotate(45deg) translate(5px, 5px); }
    .hamburger.open span:nth-child(2) { opacity: 0; }
    .hamburger.open span:nth-child(3) { transform: rotate(-45deg) translate(5px, -5px); }
    @media(min-width: 900px) { .hamburger { display: none; } }
    @media(max-width: 899px) { .nav-links { display: none; } }

    /* Mobile menu */
    #mobile-menu {
      display: none;
      position: fixed; top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(244,241,232,.98);
      z-index: 999;
      flex-direction: column;
      align-items: center; justify-content: center;
      gap: 2.2rem;
    }
    #mobile-menu.open { display: flex; }
    #mobile-menu a {
      font-family: 'Playfair Display', serif;
      font-size: 1.8rem; color: var(--matcha-dark);
      transition: color var(--transition);
    }
    #mobile-menu a:hover { color: var(--matcha); }
    .mobile-close {
      position: absolute; top: 1.5rem; right: 1.5rem;
      font-size: 1.5rem; cursor: pointer;
      background: none; border: none;
      color: var(--matcha-dark);
    }

    /* ─────────────────────────────────────────────
       HERO
    ───────────────────────────────────────────── */
    #hero {
      min-height: 100vh;
      background: linear-gradient(160deg, var(--matcha-dark) 0%, var(--matcha) 45%, var(--matcha-mid) 100%);
      position: relative; overflow: hidden;
      display: flex; align-items: center;
      padding-top: 80px;
    }

    /* Decorative SVG terrain */
    .hero-terrain {
      position: absolute; bottom: 0; left: 0; right: 0;
      pointer-events: none;
    }
    .hero-circles {
      position: absolute; top: -80px; right: -80px;
      width: 500px; height: 500px;
      border-radius: 50%;
      border: 1px solid rgba(255,255,255,.08);
      pointer-events: none;
    }
    .hero-circles::before {
      content: '';
      position: absolute; top: 60px; left: 60px; right: 60px; bottom: 60px;
      border-radius: 50%;
      border: 1px solid rgba(255,255,255,.06);
    }

    .hero-content {
      position: relative; z-index: 2;
      display: grid;
      grid-template-columns: 1fr;
      gap: 3rem;
      padding: 4rem 0 8rem;
      align-items: center;
    }
    @media(min-width: 900px) {
      .hero-content { grid-template-columns: 1fr 1fr; padding: 3rem 0 6rem; }
    }

    .hero-badge {
      display: inline-flex; align-items: center; gap: .5rem;
      background: rgba(255,255,255,.12);
      border: 1px solid rgba(255,255,255,.2);
      color: var(--matcha-pale);
      border-radius: 30px; padding: .4rem 1rem;
      font-size: .78rem; font-weight: 600;
      letter-spacing: .1em; text-transform: uppercase;
      margin-bottom: 1.5rem;
    }
    .hero-badge span { width: 6px; height: 6px; border-radius: 50%; background: var(--matcha-pale); }

    .hero-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.4rem, 6vw, 4rem);
      color: var(--white);
      line-height: 1.15;
      margin-bottom: 1.2rem;
    }
    .hero-title em {
      font-style: normal;
      color: var(--matcha-pale);
    }

    .hero-description {
      font-size: 1.05rem; color: rgba(255,255,255,.75);
      line-height: 1.75; margin-bottom: 2rem;
      max-width: 480px;
    }

    .hero-actions {
      display: flex; flex-wrap: wrap; gap: 1rem;
      margin-bottom: 2.5rem;
    }
    .btn-hero-primary {
      background: var(--white); color: var(--matcha-dark);
      font-weight: 700;
      box-shadow: 0 4px 20px rgba(0,0,0,.2);
    }
    .btn-hero-primary:hover {
      background: var(--cream); transform: translateY(-2px);
      box-shadow: 0 8px 30px rgba(0,0,0,.25);
    }
    .btn-hero-outline {
      background: transparent; color: var(--white);
      border: 2px solid rgba(255,255,255,.4);
    }
    .btn-hero-outline:hover {
      background: rgba(255,255,255,.1); border-color: rgba(255,255,255,.7);
      transform: translateY(-2px);
    }

    .hero-stats {
      display: flex; gap: 2rem;
    }
    .hero-stat { text-align: center; }
    .hero-stat-num {
      font-family: 'Playfair Display', serif;
      font-size: 1.8rem; font-weight: 700;
      color: var(--white);
    }
    .hero-stat-label {
      font-size: .72rem; color: rgba(255,255,255,.6);
      font-weight: 500; letter-spacing: .06em;
      text-transform: uppercase; display: block;
    }
    .hero-divider {
      width: 1px; background: rgba(255,255,255,.2);
      align-self: stretch;
    }

    /* Card avatar side */
    .hero-visual {
      display: flex; justify-content: center;
    }
    .hero-card {
      background: rgba(255,255,255,.10);
      backdrop-filter: blur(20px);
      border: 1px solid rgba(255,255,255,.18);
      border-radius: 24px;
      padding: 2.5rem 2rem;
      width: 100%; max-width: 360px;
      text-align: center;
      position: relative;
    }
    .hero-avatar {
      width: 100px; height: 100px; border-radius: 50%;
      background: linear-gradient(135deg, var(--matcha-pale), var(--matcha-light));
      display: block;
      margin: 0 auto 1.2rem;
      border: 3px solid rgba(255,255,255,.3);
      overflow: hidden;
      position: relative;
    }
    .hero-card-name {
      font-family: 'Playfair Display', serif;
      font-size: 1.35rem; color: var(--white);
      font-weight: 700; margin-bottom: .3rem;
    }
    .hero-card-role {
      font-size: .82rem; color: rgba(255,255,255,.7);
      line-height: 1.5; margin-bottom: 1.5rem;
    }
    .hero-tags {
      display: flex; flex-wrap: wrap; gap: .5rem;
      justify-content: center;
    }
    .hero-tag {
      background: rgba(255,255,255,.12);
      border: 1px solid rgba(255,255,255,.2);
      color: var(--matcha-pale);
      border-radius: 20px; padding: .3rem .8rem;
      font-size: .75rem; font-weight: 500;
    }
    .hero-card-badge {
      position: absolute; top: -14px; right: 20px;
      background: var(--matcha-pale);
      color: var(--matcha-dark);
      border-radius: 20px; padding: .3rem .9rem;
      font-size: .72rem; font-weight: 700;
      letter-spacing: .06em;
      box-shadow: var(--shadow-sm);
    }
    .lang-row {
      margin-top: 1.5rem; padding-top: 1.2rem;
      border-top: 1px solid rgba(255,255,255,.12);
      display: flex; gap: .8rem; justify-content: center;
    }
    .lang-pill {
      background: rgba(255,255,255,.08);
      color: rgba(255,255,255,.8);
      border-radius: 20px; padding: .25rem .7rem;
      font-size: .72rem; font-weight: 500;
      display: flex; align-items: center; gap: .35rem;
    }
    .lang-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--matcha-pale); }

    /* scroll indicator */
    .scroll-hint {
      position: absolute; bottom: 2rem; left: 50%;
      transform: translateX(-50%);
      display: flex; flex-direction: column; align-items: center;
      gap: .4rem; z-index: 2;
      color: rgba(255,255,255,.5); font-size: .72rem;
      letter-spacing: .1em; text-transform: uppercase;
      animation: bounce 2s infinite;
    }
    .scroll-hint svg { width: 20px; height: 20px; }
    @keyframes bounce {
      0%,100% { transform: translateX(-50%) translateY(0); }
      50% { transform: translateX(-50%) translateY(6px); }
    }

    /* ─────────────────────────────────────────────
       SERVICES
    ───────────────────────────────────────────── */
    #servicios {
      padding: 6rem 0;
      background: var(--cream);
      position: relative; overflow: hidden;
    }
    .services-header {
      text-align: center; margin-bottom: 3.5rem;
    }
    .services-header .section-subtitle { margin: 0 auto; }

    .services-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.8rem;
    }
    @media(min-width: 640px) {
      .services-grid { grid-template-columns: 1fr 1fr; }
    }
    @media(min-width: 1024px) {
      .services-grid { grid-template-columns: repeat(3, 1fr); }
    }

    .service-card {
      background: var(--white);
      border-radius: var(--radius);
      padding: 2.2rem 1.8rem;
      border: 1px solid var(--cream-dark);
      transition: var(--transition);
      position: relative; overflow: hidden;
    }
    .service-card::before {
      content: '';
      position: absolute; top: 0; left: 0; right: 0;
      height: 4px;
      background: linear-gradient(90deg, var(--matcha), var(--matcha-light));
      transform: scaleX(0); transform-origin: left;
      transition: transform var(--transition);
    }
    .service-card:hover {
      box-shadow: var(--shadow-md);
      transform: translateY(-6px);
      border-color: var(--matcha-pale);
    }
    .service-card:hover::before { transform: scaleX(1); }

    .service-icon {
      width: 56px; height: 56px; border-radius: 14px;
      background: linear-gradient(135deg, var(--matcha-pale), var(--cream-dark));
      display: flex; align-items: center; justify-content: center;
      margin-bottom: 1.4rem;
      transition: var(--transition);
    }
    .service-icon svg { width: 26px; height: 26px; color: var(--matcha); }
    .service-card:hover .service-icon {
      background: linear-gradient(135deg, var(--matcha), var(--matcha-light));
    }
    .service-card:hover .service-icon svg { color: var(--white); }

    .service-title {
      font-family: 'Playfair Display', serif;
      font-size: 1.2rem; color: var(--matcha-dark);
      margin-bottom: .7rem; font-weight: 600;
    }
    .service-desc {
      font-size: .9rem; color: var(--text-light);
      line-height: 1.7; margin-bottom: 1.4rem;
    }
    .service-list { display: flex; flex-direction: column; gap: .5rem; }
    .service-list li {
      display: flex; align-items: flex-start; gap: .5rem;
      font-size: .82rem; color: var(--text-mid);
    }
    .service-list li::before {
      content: '';
      width: 6px; height: 6px; border-radius: 50%;
      background: var(--matcha-light);
      flex-shrink: 0; margin-top: .45rem;
    }

    /* Featured card */
    .service-card.featured {
      background: linear-gradient(160deg, var(--matcha-dark) 0%, var(--matcha) 100%);
      border-color: transparent; color: var(--white);
    }
    .service-card.featured .service-title { color: var(--white); }
    .service-card.featured .service-desc { color: rgba(255,255,255,.75); }
    .service-card.featured .service-list li { color: rgba(255,255,255,.85); }
    .service-card.featured .service-list li::before { background: var(--matcha-pale); }
    .service-card.featured .service-icon {
      background: rgba(255,255,255,.15);
    }
    .service-card.featured .service-icon svg { color: var(--matcha-pale); }
    .service-card.featured:hover { transform: translateY(-6px); }
    .service-card.featured::before { background: rgba(255,255,255,.25); }
    .featured-badge {
      position: absolute; top: 1.2rem; right: 1.2rem;
      background: var(--matcha-pale); color: var(--matcha-dark);
      border-radius: 20px; padding: .25rem .75rem;
      font-size: .7rem; font-weight: 700; letter-spacing: .05em;
      text-transform: uppercase;
    }

    /* ─────────────────────────────────────────────
       ABOUT
    ───────────────────────────────────────────── */
    #sobre-mi {
      padding: 6rem 0;
      background: var(--white);
      position: relative; overflow: hidden;
    }
    .about-grid {
      display: grid; grid-template-columns: 1fr;
      gap: 3.5rem; align-items: start;
    }
    @media(min-width: 900px) {
      .about-grid { grid-template-columns: 1fr 1.1fr; }
    }

    /* Left: visual */
    .about-visual { position: relative; }
    .about-photo-wrap {
      border-radius: 20px;
      overflow: hidden;
      aspect-ratio: 4/5;
      background: linear-gradient(160deg, var(--matcha-dark), var(--matcha));
      position: relative;
      width: 100%;
    }
    .about-photo-initials {
      font-family: 'Playfair Display', serif;
      font-size: 5rem; color: rgba(255,255,255,.25);
      font-weight: 700; user-select: none;
    }
    .about-photo-overlay {
      position: absolute; inset: 0;
      background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.03'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    }

    /* floating cards */
    .about-float-card {
      position: absolute; background: var(--white);
      border-radius: var(--radius-sm);
      padding: .9rem 1.1rem;
      box-shadow: var(--shadow-md);
      display: flex; align-items: center; gap: .7rem;
      border: 1px solid var(--cream-dark);
      animation: float 4s ease-in-out infinite;
    }
    .about-float-card.card-1 {
      bottom: 2rem; left: -1.5rem;
      animation-delay: 0s;
    }
    .about-float-card.card-2 {
      top: 2rem; right: -1.5rem;
      animation-delay: 1.5s;
    }
    @media(max-width: 640px) {
      .about-float-card { display: none; }
    }
    @keyframes float {
      0%,100% { transform: translateY(0); }
      50% { transform: translateY(-8px); }
    }
    .float-icon {
      width: 38px; height: 38px; border-radius: 10px;
      background: var(--matcha-pale);
      display: flex; align-items: center; justify-content: center;
      flex-shrink: 0;
    }
    .float-icon svg { width: 18px; height: 18px; color: var(--matcha); }
    .float-label { font-size: .72rem; color: var(--text-light); }
    .float-value {
      font-size: .9rem; font-weight: 700;
      color: var(--matcha-dark);
    }

    /* Right: content */
    .about-content {}
    .about-intro {
      font-size: 1.05rem; color: var(--text-mid);
      line-height: 1.8; margin-bottom: 2rem;
    }
    .about-intro strong { color: var(--matcha-dark); }

    /* Timeline */
    .timeline { position: relative; margin: 2.5rem 0; }
    .timeline::before {
      content: '';
      position: absolute; left: 20px; top: 0; bottom: 0;
      width: 2px; background: var(--matcha-pale);
    }
    .timeline-item {
      position: relative; padding-left: 3rem;
      margin-bottom: 1.8rem;
    }
    .timeline-item:last-child { margin-bottom: 0; }
    .timeline-dot {
      position: absolute; left: 12px; top: 4px;
      width: 18px; height: 18px; border-radius: 50%;
      background: var(--white);
      border: 3px solid var(--matcha);
      transition: var(--transition);
    }
    .timeline-item:hover .timeline-dot {
      background: var(--matcha); transform: scale(1.2);
    }
    .timeline-period {
      font-size: .72rem; color: var(--matcha);
      font-weight: 600; letter-spacing: .05em;
      text-transform: uppercase; margin-bottom: .25rem;
    }
    .timeline-company {
      font-weight: 700; color: var(--matcha-dark);
      font-size: .95rem;
    }
    .timeline-role {
      font-size: .85rem; color: var(--text-light); margin-bottom: .2rem;
    }
    .timeline-loc {
      font-size: .76rem; color: var(--text-light); opacity: .7;
    }

    /* Certifications */
    .certs-title {
      font-size: .78rem; font-weight: 700;
      letter-spacing: .08em; text-transform: uppercase;
      color: var(--text-light); margin: 2rem 0 .8rem;
    }
    .certs-grid {
      display: flex; flex-wrap: wrap; gap: .5rem;
    }
    .cert-badge {
      background: var(--cream);
      border: 1px solid var(--cream-dark);
      color: var(--matcha-dark);
      border-radius: 6px; padding: .35rem .75rem;
      font-size: .75rem; font-weight: 500;
      display: flex; align-items: center; gap: .4rem;
      transition: var(--transition);
    }
    .cert-badge:hover {
      background: var(--matcha-pale); border-color: var(--matcha-light);
    }
    .cert-badge svg { width: 12px; height: 12px; color: var(--matcha); }

    /* ─────────────────────────────────────────────
       VALORES / WHY
    ───────────────────────────────────────────── */
    #valores {
      padding: 5rem 0;
      background: var(--matcha-dark);
      position: relative; overflow: hidden;
    }
    .valores-inner {
      display: grid; grid-template-columns: 1fr;
      gap: 2rem;
    }
    @media(min-width: 640px) {
      .valores-inner { grid-template-columns: 1fr 1fr; }
    }
    @media(min-width: 1024px) {
      .valores-inner { grid-template-columns: repeat(4, 1fr); }
    }
    .valor-card {
      background: rgba(255,255,255,.06);
      border: 1px solid rgba(255,255,255,.1);
      border-radius: var(--radius);
      padding: 2rem 1.5rem; text-align: center;
      transition: var(--transition);
    }
    .valor-card:hover {
      background: rgba(255,255,255,.1);
      transform: translateY(-4px);
    }
    .valor-icon {
      width: 52px; height: 52px; border-radius: 14px;
      background: rgba(255,255,255,.1);
      display: flex; align-items: center; justify-content: center;
      margin: 0 auto 1rem;
    }
    .valor-icon svg { width: 24px; height: 24px; color: var(--matcha-pale); }
    .valor-title {
      font-family: 'Playfair Display', serif;
      font-size: 1.05rem; color: var(--white);
      margin-bottom: .5rem;
    }
    .valor-desc {
      font-size: .83rem; color: rgba(255,255,255,.6);
      line-height: 1.6;
    }

    /* ─────────────────────────────────────────────
       CONTACT
    ───────────────────────────────────────────── */
    #contacto {
      padding: 6rem 0;
      background: var(--cream);
    }
    .contact-grid {
      display: grid; grid-template-columns: 1fr;
      gap: 3rem;
    }
    @media(min-width: 900px) {
      .contact-grid { grid-template-columns: 1.1fr 1fr; }
    }

    .contact-info {}
    .contact-item {
      display: flex; align-items: flex-start; gap: 1rem;
      margin-bottom: 1.5rem;
    }
    .contact-icon {
      width: 44px; height: 44px; border-radius: 12px;
      background: var(--matcha-pale);
      display: flex; align-items: center; justify-content: center;
      flex-shrink: 0;
    }
    .contact-icon svg { width: 20px; height: 20px; color: var(--matcha); }
    .contact-item-label { font-size: .75rem; color: var(--text-light); margin-bottom: .2rem; font-weight: 500; text-transform: uppercase; letter-spacing: .05em; }
    .contact-item-value { font-weight: 600; color: var(--matcha-dark); font-size: .95rem; }

    .contact-form-card {
      background: var(--white);
      border-radius: var(--radius);
      padding: 2.5rem;
      border: 1px solid var(--cream-dark);
      box-shadow: var(--shadow-sm);
    }
    .form-title {
      font-family: 'Playfair Display', serif;
      font-size: 1.4rem; color: var(--matcha-dark);
      margin-bottom: .4rem;
    }
    .form-subtitle {
      font-size: .85rem; color: var(--text-light);
      margin-bottom: 1.8rem;
    }

    .form-group { margin-bottom: 1.2rem; }
    .form-row {
      display: grid; grid-template-columns: 1fr 1fr;
      gap: 1rem;
    }
    @media(max-width: 500px) { .form-row { grid-template-columns: 1fr; } }

    label {
      display: block; font-size: .8rem; font-weight: 600;
      color: var(--text-mid); margin-bottom: .4rem;
      letter-spacing: .02em;
    }
    input, textarea, select {
      width: 100%;
      background: var(--cream);
      border: 1.5px solid var(--cream-dark);
      border-radius: var(--radius-sm);
      padding: .75rem 1rem;
      font-size: .9rem; font-family: 'Inter', sans-serif;
      color: var(--text-dark);
      transition: var(--transition);
      outline: none;
    }
    input:focus, textarea:focus, select:focus {
      border-color: var(--matcha);
      background: var(--white);
      box-shadow: 0 0 0 3px rgba(92,110,53,.1);
    }
    textarea { resize: vertical; min-height: 110px; }

    .btn-submit {
      width: 100%; padding: .95rem;
      background: linear-gradient(135deg, var(--matcha-dark), var(--matcha));
      color: var(--white);
      border: none; border-radius: var(--radius-sm);
      font-size: 1rem; font-weight: 700;
      cursor: pointer; transition: var(--transition);
      display: flex; align-items: center; justify-content: center; gap: .6rem;
    }
    .btn-submit:hover {
      box-shadow: 0 6px 24px rgba(92,110,53,.4);
      transform: translateY(-2px);
    }
    .btn-submit:active { transform: translateY(0); }

    .form-success {
      display: none; text-align: center; padding: 1.5rem;
    }
    .form-success svg { width: 48px; height: 48px; color: var(--matcha); margin: 0 auto .8rem; }
    .form-success h4 { font-family: 'Playfair Display', serif; color: var(--matcha-dark); font-size: 1.2rem; margin-bottom: .4rem; }
    .form-success p { font-size: .85rem; color: var(--text-light); }

    /* ─────────────────────────────────────────────
       FOOTER
    ───────────────────────────────────────────── */
    footer {
      background: var(--text-dark);
      color: rgba(255,255,255,.7);
      padding: 3.5rem 0 2rem;
    }
    .footer-grid {
      display: grid; grid-template-columns: 1fr;
      gap: 2rem;
    }
    @media(min-width: 640px) {
      .footer-grid { grid-template-columns: 1.5fr 1fr 1fr; }
    }

    .footer-brand-name {
      font-family: 'Playfair Display', serif;
      font-size: 1.3rem; color: var(--white);
      margin-bottom: .5rem;
    }
    .footer-brand-desc {
      font-size: .83rem; line-height: 1.6;
      color: rgba(255,255,255,.5);
      max-width: 260px; margin-bottom: 1.2rem;
    }
    .footer-socials {
      display: flex; gap: .8rem;
    }
    .footer-social {
      width: 36px; height: 36px; border-radius: 8px;
      background: rgba(255,255,255,.07);
      border: 1px solid rgba(255,255,255,.1);
      display: flex; align-items: center; justify-content: center;
      transition: var(--transition);
    }
    .footer-social:hover {
      background: var(--matcha);
      border-color: var(--matcha);
    }
    .footer-social svg { width: 16px; height: 16px; color: rgba(255,255,255,.7); }

    .footer-col-title {
      font-weight: 700; color: var(--white);
      margin-bottom: 1rem; font-size: .85rem;
      text-transform: uppercase; letter-spacing: .07em;
    }
    .footer-links { display: flex; flex-direction: column; gap: .55rem; }
    .footer-links a {
      font-size: .83rem; color: rgba(255,255,255,.5);
      transition: color var(--transition);
    }
    .footer-links a:hover { color: var(--matcha-pale); }

    .footer-bottom {
      border-top: 1px solid rgba(255,255,255,.07);
      margin-top: 2.5rem; padding-top: 1.5rem;
      display: flex; flex-wrap: wrap;
      align-items: center; justify-content: space-between;
      gap: .8rem;
    }
    .footer-copy { font-size: .78rem; color: rgba(255,255,255,.3); }
    .footer-flag {
      display: flex; align-items: center; gap: .4rem;
      font-size: .75rem; color: rgba(255,255,255,.4);
    }

    /* ─────────────────────────────────────────────
       ANIMATIONS ON SCROLL
    ───────────────────────────────────────────── */
    .reveal {
      opacity: 0; transform: translateY(30px);
      transition: opacity .7s ease, transform .7s ease;
    }
    .reveal.visible {
      opacity: 1; transform: translateY(0);
    }
    .reveal-delay-1 { transition-delay: .1s; }
    .reveal-delay-2 { transition-delay: .2s; }
    .reveal-delay-3 { transition-delay: .3s; }
    .reveal-delay-4 { transition-delay: .4s; }

    /* back to top */
    #back-top {
      position: fixed; bottom: 1.5rem; right: 1.5rem;
      width: 44px; height: 44px; border-radius: 50%;
      background: var(--matcha);
      display: flex; align-items: center; justify-content: center;
      box-shadow: var(--shadow-md); cursor: pointer;
      transition: var(--transition);
      opacity: 0; pointer-events: none; z-index: 500;
      border: none;
    }
    #back-top.show { opacity: 1; pointer-events: all; }
    #back-top:hover { background: var(--matcha-dark); transform: translateY(-3px); }
    #back-top svg { width: 18px; height: 18px; color: #fff; }

    /* progress bar */
    #progress-bar {
      position: fixed; top: 0; left: 0; height: 3px;
      background: linear-gradient(90deg, var(--matcha), var(--matcha-pale));
      z-index: 9999; transition: width .1s linear;
      width: 0%;
    }
  </style>
</head>
<body>

<!-- Progress bar -->
<div id="progress-bar"></div>

<!-- ═══════════════════════════════
     NAVBAR
═══════════════════════════════ -->
<header id="navbar">
  <div class="container">
    <div class="nav-inner">
      <!-- Logo -->
      <a href="#inicio" class="nav-logo">
        <div class="nav-logo-icon">
          <!-- leaf icon -->
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M11 20A7 7 0 0 1 9.8 6.1C15.5 5 17 4.48 19 2c1 2 2 4.18 2 8 0 5.5-4.78 10-10 10z"/>
            <path d="M2 21c0-3 1.85-5.36 5.08-6C9.5 14.52 12 13 13 12"/>
          </svg>
        </div>
        <div class="nav-logo-text">
          <div class="nav-logo-name">Angela Leng</div>
          <div class="nav-logo-sub">Business Partner · Perú</div>
        </div>
      </a>

      <!-- Desktop links -->
      <nav class="nav-links">
        <a href="#servicios">Servicios</a>
        <a href="#sobre-mi">Sobre mí</a>
        <a href="#valores">Valores</a>
        <a href="#contacto">Contacto</a>
      </nav>

      <!-- CTA + hamburger -->
      <div style="display:flex;align-items:center;gap:1rem;">
        <a href="#contacto" class="btn btn-primary nav-cta" style="padding:.65rem 1.4rem;font-size:.85rem;">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="16" height="16"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          Conversemos
        </a>
        <button class="hamburger" id="hamburger" aria-label="Menú">
          <span></span><span></span><span></span>
        </button>
      </div>
    </div>
  </div>
</header>

<!-- Mobile menu -->
<div id="mobile-menu">
  <button class="mobile-close" id="mobile-close">✕</button>
  <a href="#servicios" class="mobile-link">Servicios</a>
  <a href="#sobre-mi" class="mobile-link">Sobre mí</a>
  <a href="#valores" class="mobile-link">Valores</a>
  <a href="#contacto" class="mobile-link">Contacto</a>
</div>

<!-- ═══════════════════════════════
     HERO
═══════════════════════════════ -->
<section id="inicio" style="position:relative;">
  <div id="hero">
    <!-- Decorative circles -->
    <div class="hero-circles"></div>

    <!-- Decorative leaf SVG top-left -->
    <svg class="deco-leaf" style="top:-40px;left:-60px;width:340px;" viewBox="0 0 200 200" fill="none">
      <path d="M10 190 Q80 10 190 10 Q190 100 10 190Z" fill="#A8BC6F"/>
    </svg>
    <svg class="deco-leaf" style="bottom:60px;right:100px;width:180px;opacity:.07;" viewBox="0 0 200 200" fill="none">
      <path d="M10 190 Q80 10 190 10 Q190 100 10 190Z" fill="#D4DFB0"/>
    </svg>

    <div class="container">
      <div class="hero-content">
        <!-- Left text -->
        <div>
          <h1 class="hero-title">
            Impulsando tu empresa con <em>estrategia contable</em> y talento humano
          </h1>
          <p class="hero-description">
            Soy Angela Leng, Intrapreneur, Contadora & especialista en RRHH. Con experiencia en el sector agroindustrial peruano, ayudo a empresas a crecer con orden financiero y equipos de alto rendimiento.
          </p>
          <div class="hero-actions">
            <a href="#contacto" class="btn btn-hero-primary">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="17" height="17"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
              Trabajemos juntos
            </a>
            <a href="#servicios" class="btn btn-hero-outline">
              Ver servicios
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="17" height="17"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
            </a>
          </div>
          <!-- Stats -->
          <div class="hero-stats">
            <div class="hero-stat">
              <div class="hero-stat-num">7+</div>
              <span class="hero-stat-label">Años de<br>experiencia</span>
            </div>
            <div class="hero-divider"></div>
            <div class="hero-stat">
              <div class="hero-stat-num">3</div>
              <span class="hero-stat-label">Empresas<br>agro líderes</span>
            </div>
            <div class="hero-divider"></div>
            <div class="hero-stat">
              <div class="hero-stat-num">3</div>
              <span class="hero-stat-label">Idiomas de<br>trabajo</span>
            </div>
          </div>
        </div>

        <!-- Right card -->
        <div class="hero-visual">
          <div class="hero-card">
            <div class="hero-card-badge">🇵🇪 Lima, Perú</div>
            <div class="hero-avatar"><img style="position:absolute;inset:0;width:100%;height:100%;object-fit:cover;object-position:center top;display:block;" src="data:image/jpeg;base64,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" style="width:100%;height:100%;object-fit:cover;object-position:center top;display:block;" alt="Angela Leng" /></div>
            <div class="hero-card-name">Angela Leng</div>
            <div class="hero-card-role">Intrapreneur · Contadora & HR<br>Gestión Estratégica</div>
            <div class="hero-tags">
              <span class="hero-tag">Contabilidad</span>
              <span class="hero-tag">RRHH</span>
              <span class="hero-tag">Agro</span>
              <span class="hero-tag">IA aplicada</span>
              <span class="hero-tag">Business Partner</span>
            </div>
            <div class="lang-row">
              <span class="lang-pill"><span class="lang-dot"></span>Español</span>
              <span class="lang-pill"><span class="lang-dot"></span>English</span>
              <span class="lang-pill"><span class="lang-dot"></span>Português</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Terrain bottom wave -->
    <div class="hero-terrain">
      <svg viewBox="0 0 1440 80" preserveAspectRatio="none" style="display:block;width:100%;height:80px;" fill="none">
        <path d="M0,60 C240,10 480,80 720,40 C960,0 1200,70 1440,30 L1440,80 L0,80 Z" fill="#F4F1E8"/>
      </svg>
    </div>

    <!-- Scroll hint -->
    <div class="scroll-hint">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="6 9 12 15 18 9"/></svg>
      scroll
    </div>
  </div>
</section>

<!-- ═══════════════════════════════
     SERVICIOS
═══════════════════════════════ -->
<section id="servicios">
  <div class="container">
    <div class="services-header reveal">
      <div class="section-tag">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg>
        Servicios
      </div>
      <h2 class="section-title">Tu aliada estratégica para<br>crecer con solidez</h2>
      <p class="section-subtitle">Combino expertise contable con visión de recursos humanos para ofrecer soluciones integrales al sector agroindustrial peruano.</p>
    </div>

    <div class="services-grid">

      <!-- Card 1: Business Partner -->
      <div class="service-card featured reveal reveal-delay-1">
        <div class="featured-badge">⭐ Principal</div>
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
        </div>
        <div class="service-title">Business Partner Estratégico</div>
        <p class="service-desc">Soy tu aliada dentro del negocio: conecto la estrategia con la operación para que tu empresa escale con orden y claridad.</p>
        <ul class="service-list">
          <li>Diagnóstico financiero y operativo</li>
          <li>Planificación estratégica de recursos</li>
          <li>KPIs e indicadores de gestión</li>
          <li>Mejora de procesos internos</li>
          <li>Reportes gerenciales ejecutivos</li>
        </ul>
      </div>

      <!-- Card 2: Contabilidad -->
      <div class="service-card reveal reveal-delay-2">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="3" width="20" height="14" rx="2" ry="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>
        </div>
        <div class="service-title">Business Partner Contable</div>
        <p class="service-desc">Gestión contable precisa y estratégica orientada a los resultados del negocio agroindustrial, con visión de futuro.</p>
        <ul class="service-list">
          <li>Contabilidad general y tributaria</li>
          <li>Análisis de costos agrícolas</li>
          <li>Cumplimiento SUNAT y NIIF</li>
          <li>Control de activos y inventarios</li>
          <li>Auditoría interna preventiva</li>
        </ul>
      </div>

      <!-- Card 3: RRHH -->
      <div class="service-card reveal reveal-delay-3">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="8" r="4"/><path d="M4 20c0-4 3.6-7 8-7s8 3 8 7"/></svg>
        </div>
        <div class="service-title">Business Partner de RRHH</div>
        <p class="service-desc">Gestión del talento humano alineada a los objetivos del negocio, con enfoque en cultura organizacional y productividad.</p>
        <ul class="service-list">
          <li>Reclutamiento y selección especializada</li>
          <li>Gestión de planillas y beneficios</li>
          <li>Evaluación del desempeño</li>
          <li>Clima laboral y engagement</li>
          <li>Capacitación y desarrollo de equipos</li>
        </ul>
      </div>

      <!-- Card 4: Inteligencia Comercial -->
      <div class="service-card reveal reveal-delay-1">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="18" y1="20" x2="18" y2="10"/><line x1="12" y1="20" x2="12" y2="4"/><line x1="6" y1="20" x2="6" y2="14"/></svg>
        </div>
        <div class="service-title">Inteligencia Comercial</div>
        <p class="service-desc">Datos convertidos en decisiones. Análisis del mercado agroindustrial peruano para identificar oportunidades de crecimiento.</p>
        <ul class="service-list">
          <li>Análisis de mercado agro</li>
          <li>Seguimiento de competencia</li>
          <li>Dashboards de ventas y proyecciones</li>
          <li>Estrategia de precios y márgenes</li>
        </ul>
      </div>

      <!-- Card 5: IA & Productividad -->
      <div class="service-card reveal reveal-delay-2">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
        </div>
        <div class="service-title">Productividad con IA</div>
        <p class="service-desc">Implementación de herramientas de inteligencia artificial para optimizar procesos contables, administrativos y de RRHH.</p>
        <ul class="service-list">
          <li>Automatización de reportes</li>
          <li>Herramientas Google AI y similares</li>
          <li>Workflows de eficiencia</li>
          <li>Capacitación en IA aplicada</li>
        </ul>
      </div>

      <!-- Card 6: Consultoría -->
      <div class="service-card reveal reveal-delay-3">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg>
        </div>
        <div class="service-title">Consultoría Integral Agro</div>
        <p class="service-desc">Acompañamiento personalizado a empresas del sector agroexportador para estructurar su gestión financiera y de personas.</p>
        <ul class="service-list">
          <li>Startups y pymes agroindustriales</li>
          <li>Estructuración de áreas clave</li>
          <li>Manual de procedimientos</li>
          <li>Mentoring a equipos contables y HR</li>
        </ul>
      </div>

    </div>
  </div>
</section>

<!-- ═══════════════════════════════
     SOBRE MÍ
═══════════════════════════════ -->
<section id="sobre-mi">
  <div class="container">
    <div class="about-grid">
      <!-- Visual -->
      <div class="about-visual reveal">
        <div class="about-photo-wrap">
          <img style="position:absolute;inset:0;width:100%;height:100%;object-fit:cover;object-position:center top;display:block;" src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAYEBAUEBAYFBQUGBgYHCQ4JCQgICRINDQoOFRIWFhUSFBQXGiEcFxgfGRQUHScdHyIjJSUlFhwpLCgkKyEkJST/2wBDAQYGBgkICREJCREkGBQYJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCQkJCT/wAARCAOEA4QDASIAAhEBAxEB/8QAHQAAAAcBAQEAAAAAAAAAAAAAAAECAwQFBgcICf/EAFUQAAEDAgQCBgUHBgoJAwUAAwEAAgMEEQUSITEGQQcTIlFhcRQygZGxFSNCUnKhwSQzYnOS0QgWJTQ1Q1NjgvAXJjZEk6KywuFkdPEnRVWD0lSj4v/EABoBAAMBAQEBAAAAAAAAAAAAAAABAgMEBQb/xAAqEQEBAAIDAQACAgMAAgMBAQEAAQIRAyExEgRBEyIyUWEjQgUUM3FSgf/aAAwDAQACEQMRAD8A9MIIggtmQ0EEEwCCACMBLY0ARgWQCNSrQIIIwEASCUj0S2CLFEnBoiIRsEII7IWTAkaIhBAGgEESDGhZC6F0AEEDZBAAHVKukowkQIIIIAIIWRgBAEjRgXR2HdcoPRI1R2SgD5I7ao2NEgWCFksBHZLZ6NWR2TlkVkbGiLIZUvKgQjZaIsjA70drIwjZkG10EohJtZGxoSJGUlNI73QRAo7oAIIXRXQB7IXRXRXQC0PakXQzIBd+a5h/CIP/ANOav7bP+pdOuuX/AMIk/wD06qh/eR/9SrH1OfiPwALcLUH6sfBV/St/sjUeYVnwGP8AVbD/ANUPgqvpWNuEqgd7gry8Z4uH+xORG0cvkka2TkV+qlGmoXO6UOkPzbvNW2pnp797fiFUUg+bd5q4LctRTAAj1d/MIK+PYOFG2G036tvwUq/ioWFH+Tqb9WPgpRd3qyl6KuhdIzIs3igbOZkRdbRIzBFmRoFk32SboroZvBMgLkRKBKCACCF0Wh5IILor+CCK6egUTqhmSUEaA7oXRIIAXRc0PahogBdDuQQQAO6NEEaACCCNAEgh5hBIFZghdJQCAVfVC6Ln3IIMd0ESNBwaF0SCDGSgSiQQB3KznH7rcKYif7ly0SzXSKbcJYib/wBUU56jPx5EiPzJ8aj/ALl3LDhaggH6AXD6cXhbpvU/9y7jQ6UUP2At8XNTrfWNkbiiZue9GVRUip0pJvsFcPnN6mX7bviu3VptRza/QK4hLczSEfXd8VlyteJEf/SEPkrimA9HnKqD/SMX2VbU4JpZvNYtnp3ohZl4Awsf3d/vK2dj3LJ9FEeXgLCQP7AFa6yDIvbkgnEEwaSgk3Sm7qkQeVHZKtokqVBZC1kWZDMgFIkWZFdAKSgUi5QuUA5dC6bv4o76IGy73Q8kgEo7pAtEiBSkARRWRoIBNkVktEQjYJAQ2SrIrJmG6CCMBICCUEAErZA0IhADRDRC6B0NABEjSMYFkpECgkCgjSQUd0jGghdBABABBHfRACyIjkjuiJugCIQARkICyYEdUVkHJJQBFIO6UUhxVRNC6InxRXsiKZDzIZte5JJRXugbKLkV0SJPQ2WChdJujujQ2VmXL/4RDv8A6e1HjJH/ANS6aSuW/wAIt/8AqBKO+aP/AKk8Z2jPw9wKLcL0H6ofBVHSuf8AVOfX6YVxwR/szQfqh8FS9K5/1Tm+2FWScXFOSWzSGXXkkJcf5iU25LndCFSaRHzVxY+kU1ydS3fzCp6X82deauDb0im23b8QielfHrvCzbDqfX+rHwUm91Fwz+j6f7A+Ck3WiQOiCBKI3QCvNC6SDZC90wO4QuiuhujRDv4ororoXQBor+KIlESgDJRXRX5oXT0Wx38ULlFdC6NDZV+9FdFdGkYE2CK6FkVigisyF0mxSgEzGChe6FvBHZIAgha6OyNnoSOyFgjSPQgELII0DQrI0ELIMEEYCMNQWyUdkq1uSGvckCcvihlS7IIBNvALL9JXZ4PxE/3RWqWT6UDl4MxH9UU5e05ePJVLbqovGpH/AFLuNFpSQ/ZC4dRi7KfxqB8V3GkFqWL7IXRi56cbuUZ3RM3KBVEaxE5aCc/oFcRdrI8/pH4rteKaYbU/YK4nu53mfiseX1txI5/pFn2VbU/8znN+aqgB8pD7KtodKKbUb7WWTR6n6MBl4Fwgf+natTdZro4GXgrCR/6dnwWkugxoIkEAiyU0IrJTd1dTDgGiIhOAaIEKFGCLJKfy+SS6NPZGrokstIRJ7LQckEEAEjFZGjsjsgC2GqMbIJQagCCUELWRpGCCFkEHAKJGUSCoWQARhBAFZBGiQQ0ESCDBGgAjQIII0EEGCO6JBAC6O5RIJGUCjukjRGkRV0LpKCAVcoEpKCAUgkoIMZSSgSiumQHmm3BLKQdUyJKIhGiTIlEjO6JMgCCGyLMgDRjREChdAGVyj+EcbcBuA5zx/FdVK5R/CN/2GH/uI/iqx9Rn4m8FXHDVB+qb8FSdK/8AspKP0wrvgwW4bof1Q+Co+lb/AGWk+2E74WNcWOycZ+Yl22SCEtukEndZc7oQqX817VcAflNLrfVvxCqKX82e66uQfyulHO7fiEFfHrfDT+QQD9AKSouHn8hg+wPgpF1qiD3QuivogSgDRXRXQv3IA73QRIiUApEiujQA5JKNFZMUELoWRht09kJDcpQCOyWz0SAjslAIW1UnoQCPLojAR2QZOUI8qMI0tgnKjyo0dkbBNkAEqyFkAmyMDmlWQsgyct+SPKlWKOyNgnKhZKQS2NCsjAR80ftQCbI7IwUR0SMLI7IkV0wPQLH9KzsvBOIn+7WvusX0uutwTiH2E8fUZePKVBqKP/3A+K7hTfzeP7IXEMPH8xtzqB8V2+m/MR/ZC6cXLS2i9/NC2qJh1NtUZOqoI+Lm2F1J/QK4pfU+Z+K7RjRy4RUn9Ari4tdYcvrbinRhuuI+TFbRm1BN5qqj/pE/ZVtFYUEg5klZNXq7gBuXg/Ch/wCmZ8FoLKl4IZl4Twtv/po/+kK8sjZiQSrII2DaNu6SD3pTd1dRD+ayF7pouS2nRSosBAhEEdylRBFt005hCeRFEo0YshY3S3NsiVECCCJAL0RhIR3SBSFknNZDMg9lIIsyF0HsaK6Iu8UV9EEUCEd0i6AKAWSiBSSggiroJN+5C6DLBQuEi6F0EXdC4SLoXQey7o03dC+iBs4gEi6GZB7Lv3JV/EJvMhmSLZaF9E3mR5k9DZd/FC6RmQzI0eyroXScyGZBbGTZEXIrhESgBdAokEwIhFZGiQCSiIS7IrI2RBCJLISSEyEiSrXRWTGhLk/8I4/6kxjvqY/iusWXJf4R/wDsbD/7mP4pxnn4s+Dhbhyh/VD4Kh6V/wDZeS/1x8Vf8If7PUX6pvwVB0rm3DDv1g+KeRY/pxk7pTBenl22SCnGkmCXTSy53ShUv5v2q4j/AJ7TC1rOZp7Qqil/Nb81cR9qspftM/6gielfHrWg/mUP2ApCj0GlFD9gJ6/itmYyUV9N0V0EaGx3RIIJkO6F0SCWj2MXR+SIIwEqcBHZGNkdkjFZHZLDe9KDfBLZ6N2RgJzL3oZUbPRAahlTlkeUpbGjeVDKU7lQyhGxo3lQypzKELBGwRlQypVkEAmyOyNHZGzJQRkWRIAIIIJECCCCDBBBEgBdHdEjCCBEjQKYBYfpjdk4HrrfVW4WD6aTbget+yqx9Tn48uYbq7Dh3zhdtg0hZ9kLimGj5zDNvzwK7ZDpEz7IXRi5qVHpfxRkXKJnNHdUSFjptg9V9grjDdl2XiF1sEqj+gVxtuoBWHL634jEX9IO8Gq3jP5A9uly5VMP8/f9lWzbigOmhdZYta9d8Ity8NYa3up2f9IVtzVbwyMuAUA7oGf9IVkmYEoIkEA0jGqQDojabK2cp0alGCkt1CVzSMoOSrpvZKBSMpDYogb6o0HAJuEhzbJaI6pFo1eyGZBwsiVEPMhdJQvZAHdGDZIujBQNlgowUjMhm5IBaBScyIlAGUV0EO9A2O6F0nZBA2VdC6TdC/cgbKuhdJJ7kLoGyroXSb+KF0Hsq6F0m4RZkFsu5QzapGfxRZkaLZzMhm8E3mR5vFGhsvMhdIzBDMjR7OXQum8yO6D2XfyQukZghmCCLuiuk5kWbwRobKvqhfxSboro0C7+KCRm8UdygFjZAhEChcFIAisjQumCbIrWSroXQCCuSfwkLfxOpx/6qP4rrhXIf4SJtwlS+NXH+KrFGfi24S04eov1Tfgs90sf7MO/WD4rR8KC2AUX6pvwWc6WD/qw639oPinknH9ONHZG0n0eXuSTqEtoPo0tgsHQh0o+a9quYgBXUtvrMv8AtBU1L+b9qu4m3r6PvLmf9QRPSvj1lQ/zOH7ITx3sm6IWpIvshPkLbbPRCCdZEXbJfo7kvo/lHNzyQAKkdQUYhPcl9HMTAajyp/qUYi8Evo/kyGJQYnRGRyR5fBLZ6NiMDdKyhLyosqNjQrWR3R5QURskYkEEEAoAI0QKO6QBBBEUyC6CCJABBBC6AGyF/FC90SDGggEEECCNBAEhZBAoAWQsjAujsgE2QsjRoBKJK0RG3JABc+6bzl4Gqz4LoK5106uy8DVSrH1OfjzRhY/KMLHLrAu1R/m2+QXGMJN6rCxf6a7NH6jfILpxctKjNwjukxnRAkbphX8Sm2BVX2CuPMPZGmi69xO7+QarX6JXIWbBY8vrfi8Nwf0hLy7KtW60LRcevt7VU02tdN4BXMTPyGK43ePisq1ewOH25cEoh3Qs+AVhlUHBNMIpAD/VN+AU2/ikYW8EEM3iUEBFB0QadUTSCL3SgNVrWUOt2SkQGiOylYAIwggOaRDBNkoapIKANkHCrpNyUL6JKDB2qbdonCUlwuERJvNzQzBEQULK09juLoXRWKFkAdwhfuRWQsgx3KMORWQsUgVdDMiRIBWYIr2RXRE9xRoFXSc3giud0Sei2VmQukoXT0Wx5kMyJESgbKuSiuiuhdBbKuiuiQQB3QBRIXQCkEV7obFAGhmIREhC6NGVmQuk3Qulo9juhcpN0E9DZV/FC6SiRobLQLikXKF0aGzmdAOTaF0tDZ3MO9DOm90SNHs7mQv4pu6MG6WgUTpuuRfwkBfhOk8KqNdcXJP4Rn+ydN/7qP4p4+pz8XHC2mA0X6pvwWa6Wjbhk/rB8VpeGNMCo/1Tfgs10s/7M6/2g+KrLxOLjR8ktv8AN5SkHZKb/NpVzuhGpfzY81d0wvilHtq+P2doKkpfzQHiryiH8rUQvf5yP/qCJ6K9a0Y/JYvshPW1TVJpTR/ZCeVoOxvACc6wKMjS0raSXiyLOL6qPdGEtDaRcFC7Uxc96FzbdHycqQCELjuTFz3oAkI+QeuERcAmwSgj5LY7okVyhe6rQGgiRpAEd7IroX8EjHmQzFJuhdPRFXQuklFc9yNGXdEiuULo0BoIroXRoiroXSb+aK6NAu6F0m6CNAd0aSjvZGgO9kLlJugjQKuhdJQRoFXQukoI0YyeS5r09PtwRUDxXSVzDp+dl4Km8Sqx9Rn488YPrX4UP0l2VnqDyXGsD1xPCh4rsrT2fYt8XNQZtdAmyJu3JB3KyolXxWbYBU/ZXJG7BdX4tNuH6nyXKGbBYcvrfi8NU388nPgryJo9FptrmQae0KipT+Vzq+gaOro+90refiFm1evsI0wymH9234KXeyiYZph9OP0B8FKTGx38UEnRBB7ZaLH2OeGXNyrunqg8DVYaD8+1aSmLgW2Krly+UcWP1NtI1wIR7qJDPZoupLJA5RMtquOikEaFky0JC6OyFkDQii5I7IWQNEkoX0QIRWTAiEQHtSkk3QQX7kL7puR2VpKqZ8YZDIWF2oVTHabdLq6FwqP5bj+sEpmMMc4DMNU/kfcXV9ELqEK5gZclBldE/wCkEvk/pLvok31TIqYz9II+vj+sEaLZ0m6IlN+kR7BwTl8wuE9FsL6IXuise5HlKNnoEEYahlACWy0K6K9gjLUVrIGg53RokEyGgi96HsQB3NkSCCDBBBBBDvoiQQQAQQQQYe1C6IoaoIeyO/eiQKDAoIaoZfBA0FkEYHhZDKls5BWuglWQACWz0JGEaOyR6JsuTfwiwP4pU3/uo/iut2XJP4RptwnSjvq4/ininPxbcNf0HR/qm/BZnpZNuGh4yD4rS8OaYJSD+6b8FmOlk/6ts/Wj4qsvE4/px07pxo/JpT4JsjTmlg/ksuq526NTWyAeKvqAB2M0IH9rH/1BUFLcxjzWgw4EY3QC1iJov+oJivWtMLQR+ScO6bg/MR+SWVadDGxR2SQbI7hMhoIroXSBQR3SboXQeyiUV0nMEAUEVdC5SboXQZSANkV7oXQeyroX8EV/FC6Bsq6K6TdC6C2VdESkoIGyvehdF7URKBsolBJQQRV0LohqggDugiRSOyMJQewc8NFyVHdXxsOpsqmuxQteWNuSqeepmc++cjVVMUXJrxXxnmlemR96x4qJW7PKUKqb65T+T+2qnxCOJl7pFLiTJtiFmHzyStyucSEUMj4BZhsEfI+mwNWwcwjbVsPMLJGrmP00GVk7dnXS+B9tealneg2VrjoVkfT5z9JW2BzyTOOc80XHRzLa8XLP4QbrcGPHe5dULVyb+ES7Lwf5uSx9LOdOB4Dri+FC67GNreC47w9rjeGDuBXYB6p8lvGFGw9lApLD2UZsmlTcYm2AVHkuVsvoupcaG2ATLlzNgseX10cXhil/nNR5haCls99Ayx1mYP8AmCz9Ifn6jzWjoGk1OFjTWePT/EFk0euqDs0UIP1QpF7pqkFqaLT6ITtvBPY0I6ckEqyCNjTnLLRua42VvS4g0uaLhUNSXBo32RUTj1zbk7rXkwlZcednTYmuYGjWydpsUYPpBZiulcxgsSobZ5QDZxCxxwbZZuhw10cpsHBSg4HZYPA6uYTEF5OuxWtp6u4AJ1ToWAKBCbZIH7JaQAokaLmnAFkVrI9tUAU06Fa6ItSr6oig9GJmfNlY3FG2rHLayi8ZWNxUfljlrxseRCDRZOwj5xpHekgap2MDrG+a0rKI/EmKTYdh75Ixew0WSpeNqyO+ZtxfkVo+NLHCpfJc3AspxXWuj47qW3vGT7U6ePai2kJ96x7U63VVqE1dNxxUvqmNdGQ0nXVdJwetbVwNcHXuFxGkZeqZpzXVuDnO6gNJOmiz5GnHGryoWTgGiFh7VntoQAhZLyhDKEtjRBCItJTlghZPY0ZLdUWUp7IgGeKNlozl80MqfyBDIEfQ+TOUoZSnso7keUdyPofKPkKGUp/KO5DKEfQ+TGQ8wjEadyBHZGx8mciGXzTpaiICNjRvL5oZdE5bXZC3kjY0QGjuQypYCIo2eiLI7XRoWQBEFJsl20RWCACSTqjRb8kFoL6I7+KTsggFXXJf4RX+y1IP/Vx/FdZXJf4Rf+zNEP8A1caePqc/Frw/pg1J+qb8Fmelg/6ux/rR8VpsB/omk/VN+Cy/SwbcPxfrAqy8Tj+nIClX/JpdEknVLFvRJdQudui0h+bGvNaPDDmxyhFv66Ll+kFnKYdhvPVaPCf6foBa3z0Q1+0E56L49XwOPUM+ylk3Kbg/MM+yEJpOqbmWqBvlDBqUx6cy9r6qnxLFt2s1KpGV87pyLp4zacstNr6Yy18ybOIsB9ZZr0yW1sxTTp3k3uVXwj+RqvlFn1ktlc153CyJnePpFKZWSRbEp/xj+RsDVMbuUuOYSbahYeXGpi4NGhWpwR7pYGucblRljppjntZ270EdkdrKFaFeyO/egjsEDQaIkdghbwQNCQANkdvBHZGz0TZCyVZCyWxomyOyOyFkbGhWQtqjsgjY0FkLII7I2NCsm6gfNFO2TdR+aKAyVU38ofpzUWRvaU2pt17/ADUSWzStowvoraow1HcHZHZAFbwQypYCAsgyMh7kMqWXhqMOaUAjL4K5wAC5PiqaZwDNCioMZbQvIe6wSym4eN1W6BXIf4RzwOEmi+71sxxjSl2USDzXMf4QOLCs4eZG03FwfvUTGyqyylnTkvDg/l7DvBpXXht7FyPhkf6w0A/QK64RoVviwpMfqI/NEzZGVRKLjcgYBLbvXMmbLpXHLgMBePFc1ZsLLn5PW/H4YotZajzWnwpofiODs2vUx+3tBZiiPzlR9parA2l2N4K21wamL/qCyrV63phanj+yE7ukQfmWeSUjYD3IIaHkEEBzKrlaIhc20TVFK3rm3PNQauXrLNBOyRSNcyZpuV15TpzY5SVfV8gcBZR2nsn4pD5A6wJTkYa/sgrKNr2m4IQZ3ea0brgXCzmEROhqSHLRk6aLKrSsPlc4kOOytOSqsO9cq1CIQE6pN9EaIpgLokaCNmJBBBMqTL+bKx+K29MNyBotfNpGVzXiWvlgxNzQDay044x5LqLAED6QSmuHWN7Q3WZ+VJSNAUQxiVhBIOnettMJktuMXNOFy6jZc4Zd17BaDH8bNXTmJrr35JPDeGNqI87+9RJprcpVKGOv6p9yUAWjYraOw+ka4sIF0T8OpAPop7DL4a0msj0O66vwmwCL2rIwUdLE8PGW4WiwnFIaXQuaFjnLa148pJpt9kVwFRHiKA7SN96T/GGH+0b70tU/poAboKuoMRZVC7SDdT8yStl6IXSM3ggTdGhsZKGZJuiv4oIvMhmSLjvR3QRd0Ei6GZBw4isk5kWZB7LQSboZkFsq9k0+oYw6kJTnaLJcQYnNSztDDonjNpuWptqxMwi91BlxBrZxHmGpssozid0TAJDupsEpnHpBN7aoz/r6eGX142DGgxg3TNRI2FpJIWWn49oaO8MmYPGm2iiVHFceIwn0cu10uow+re15XGT1qm4iw80sVzCQAQsEKyVv9YfenYcTlZK0mQkXW/ww/kdBa7MLoHfks/Dj0bYRmcAUk8RxfXCj5X9xodO9Jztva+qzx4kj+sErD8XNXUFo2R80vuNAgAjaCWgo7JLJ5Lkf8Iw/6uUA76yNdetouP8A8I3TAcOH/rGJz1Oc6XWB6YTS/qm/BZPpZP8AIEX6wLW4PphdN+qb8Fkelg/yDF4yBPLxOLkZSy78jkAACSUv/cpTvqsGyLS3yN81o8IBPEeHjn18X/UFnKa2RvmtNgjf9ZcN03ni/wCoJj9PVsDfmmeShYsTHA4juVhDYRsHgFBxn+bv8lcvab4wzJnSySZjcgoonflLvNJpwM8h/SRxC9S61t10Yxz5W6TnHxQIR5TzQymypBBSD53TmUjkklh1TJWSH58ea32AAejN8lhZIiZgfFbvANKZo8Fjyt+JbIa+CNBYNhI0EEbMESNBAADvQsgjQAQQuhdGwCCCLVGwNAAIBHYJbAtELI7IHQXKNgE1UuHVlM1NcyEakBVFZjTSMrSFUlqbZEGq/PPPiokrC7komJ4qIbuJAUOLG8wvmC3krC2LhsJsl5CqN3EDWuyl4v5qSMZblvmHvRqj6izyaIspVU3HI3OsHpTsaYPpi/mjQ+oexGoMDbqqbjuU2JHvTOL4oJm2DhqqWKIvBJKuY9ds7l300fy6HC2iYmxBslxYXKqGwHxRPhcHAAlOSDdWDJ42u2asT0zVjZsFaW7dkfetOKV51JKwnSw3q8CaCb3kb8UZToY2s7wqb8R0X2F1zkVyPhIf6yUnhGut37JURdBpsECblE21gUDqqTpnuPDbA3W+sFzlmwXQ+PTbBf8AEFzuPay5+T1vx+GKH1p/tLX8NtvxJgTSb3qY/ishQf15/TWz4Tbm4rwEf+pjP3rKtY9ZQj5lvkj1QjHzTfJKIQZOqCVbwQRsOQeiHrGkjkpbKLXZLkcG5CRyCfhqQTZdtrhnqrq4pGSWF1OwWF76ntg2tojnewydq11Owt8ZnAHcue104zxbMhZG8HYqW7XZQqhxEjSNk+6YMAWO22lhhvrlW9gqfDJA51wre9wnKVC10LeCF0LpkLzREIzqUEwSggTdBAIl/NuXPeJWx+nvLgL2XQZnWjcuccTPBr39oDsrXj9Y8viDTRxE6hR8ShY1hLU5ROzDcBFiDbRk3W7mjJygGZwNt1pMAIFO7KVmMQaWlxbfdXfCj3upnA335oqpO0XFqqtZXvEbtAUieorhDmDjt3qfWxh1c4EJyoiaKc6ckFtU0tXXvb62qW+rxCPmrfB6Bs0WbKkY1A2kZe1kblE2iUFZWPYS8o/Tazr8t9FGo6xuU5dU9TTtkqPFGlNtwriL2Na2U2NluYZRIwG659h0BMUcjBY2W2wnN1ADguT/ANnX/wCqcgggqILoXQ0QPggwzIrjuQI1RIIdwhfxRWQylAKv4oIrIxdBjugiQSAE6FYrig/lDL95W1I7PsWG4tHz8evMrTj9ZcvjO1oDstu9amgeGYedforLTAlrT3Kc/FmwUbm5uSX5GFy1ovxuSYb2yvEEzflJ4uDqrzBGB1OLELG4nKamse+97laLCKzqoA032W8w1jI57nvK1fOjIO4Q6okjYqufX3OhNks4k1jQS6yPkfS2NMSzVJbTAKrbjzH9kOVnTy9azMos0qWURiF1bcPMtVFVzRfVW3Dzb1Z1UW9LxnbXsHYHkjslMHYCNZbdRGVce/hH6YFhmn++MXZLdy47/CQ/oPC//esRKjPxcYR/RtP+qb8Fjulgj5Dh/WhbHCf6Np/1Tfgsb0sE/IlP+tCrK9FI5Qb+xLv+QyjQG6QdUst/IpXLKNEWl0Y3z3WpwJ2fifDLnN+URf8AUsvSj5tvmtTw2B/GrDB/6iL4opvV0Q+bb5KsxxwbTv8AJWkY+bb5Kp4g/m7/ACVY+pvjAyT9QXeJul4fN1szj4qPiGhS8DOaQ+a68XLkvLI8uiWTbkgD3hUk2QiI3ThN0Q2SCHIyxzLTcNVHWR2PIqgkAy7K74VYMjiO9Y8ldHHjppeWwRexHqENfBYNRWQSXSNabEoCRjjYFLZl2QsUdwOYQuEbArIW8kdx3hAEHmjYFZH7EduYRao2NBqhr3Iaoe9GwK1kY0ShqhYJbAkmQdkpyyS/RpRsMfj0z45yNbWVKx75Mp2uVb8QuDqkgb2VVECwNFl04+OfL1V4tSvnzANJ1UWHDntb6quJ5GhxueaR17GjcLWVllJtmqrDpjUfmzuphopRFbKdlOkrIeuDS9t7qTJPGI73CLaJIoqSgkEly0pFfA6J+oIV9TTRuPZIVXjsmvZIulKNRXPGYC3cpFM0hh0VeZZLgWVxSu+ZudFZa0bBJdaycYwdYMyeiYHm9tQo1fN6P2uak+08xtyGwB0XLOl4EYPFf+2b8VvafE3OcQSsH0uuzYPB3mZvxRfBJ2z3B+vElP4Rrq+bslcr4Qb/AKywjuiXU7dkqIsppu0Ijug31QgeSraWa4+NsIaO94XPW8lv+kA/yVH4vCwLTosOT1vxzoxh9sk2v0itxwa3PxlgI0/Ps5LD4ePmpfF5W74Fbm43wIAadcPgVjWkerYx823yQQabMb5I9UlaFZBDXvQQNVyiQh/VtvbshOwQNDrh2qP0Q5Y3fohPxwFpuQu21xa7QquFxeCHaKwwmPLMCTc2VdWueJA0A7qdhGfrxe9lhlXRiu5zZ7UKoXDUua123SKsHK22q59t5E/CCWv3V8NQFn8GBz63WgGwWmPiL6CCCGqrZAiKNBGwbkdkbdQX4mxriLjRSqw5YXHwWDqsRtVyNz2s5VjNpyumtqMRaYXEOGy5dxJWOkxQ2vY6K8qcXdGwjMNVlK2XrqoOOuq2445+XIXpzqUDdSJKp00BJvsq6t1A0UlptS7clrYyiolcZXloHNabhqLq4XX77rMxyNZMS4Ddavh6Vs0TrW9inLxePqJiVSyKtdsE3LiTDHYOBR4vhwkrXuN/eok+GsZFcgj2oFXWC4i0MsCEjG6psjDmIUXBoGMZsUWMwtkFtR5I12W0KldHrsn6Z7GTX0UOjw/NcAuOvepTMKe2W93IVps8IkD4mN7xotrh35oLCYG3qoWMO/Ilb3DNYRca2XJv+zrk6SLaok7lCKwHNVsiLeCFkrTvQAB5pbGibIrJeVDKjY0RZGAlZULI2NCsEVkuyJGxonQckfsR2Rgao2NEOGhXPeNZSypjGvNdEeCAfJYHi1jH1bA7xVY5apZY76ZB9SSOZUCtneWkC+q0JpYQNlT1tODIcuy3wz+mHJx/DOOjmMu3NXlJmbGAQnYcNMnaDbjdOhjY3WK1l2xuOi2i7RdRqk3aQpjS23ikGnMx0CpNU8d2SA20utTh1WeoFu5VEuHuiNyDZWmHRAQXUZ9nh1U5lWdrq94Zkz1brrMMLc+y0fCrgaxw02XPn1HRhrbdNHZCNBg7AR2XPt0iK4//AAjW3wLC/wD3rF2GwXIP4RotgGGf+9YnKnKdLTCtMOgH9234LGdLP9CU4/vQtphQ/k+n/VN+CxfS1/QtP39aE8qI5Qe5LIPoUp5JB3S3H8hl05qIpHpPzbLd61fDf+12Fgj/AHiL4rKUfqM81q+GBfjDCh/6iL26opx6uZ6rfJVGPi9PJ5K4YOyPJVGPj8nk8k8fSs6c6xIXcncAb23HxTeIi7u5PYCQ17h4rux8ceXq/LEktsN07lvZEYzdLZaM2RgJzqigIyE9loxM0ZSrnhdzWRG5tqqaqtFC5x5Kii4yiwt7w87HQBc/JLfHVhdeupSVcbDq4KO7FIWg9sLjmLdJVXNKfRmNawfWOpVJU8cYrMbiRrR3Dmpx4cqd5ZHVMe4vjopQ1jr33sdknBOLW1chDibX71xWpx6rqpM0rrqbhmP1NI8vYR5Fa/w9aZfy3bv3y7COaHy7DyK4oeN6/uZ7kP4713cxL+FX8rtRx6LvRxY7E+UNzbriR42rj9RA8Z1weHDKLI/hKcrv8dfG5t8w96V6bH9YLhsXSJiDGhoayw8Uv/SNX79W33qP4Ml/zR3D0yM/SCUKqM65guIN6Sq4D8033p0dJlaP6lv7SX8OQ/lxdrFQzvCU2djjYEFcS/0oVrR+YH7S0XA/GtTjuKOp5IgwBt7g3U5cWU7VjyS9OnghInNoylM9UXSJx82VC9sDjE38oPBKRGczW2FtNUvFsra6RR2uIa031K6cfHPfTM9Owu7RvqmX0sZ70zXVMjXEMaSQUwysqMpuy61njHKzZt+GxuqM4J0Kny0THQ2ub2VQcQqfSgOrNrq2bUSZNWoqZoVDh7YybklVmOsjY6/crL0yRh9QhUONzvmky5UlTRIMZAOmylwysbERdQIKdzrCxVuMLe6nuGlT9NLL6KnnZe11FxMtk1LlIgw2UP1aU3iFI5rQC06ppnqHSQxlxI7lh+l1uTDKUd8zfit3QwuDjusF0wOtR0bf75vxTt6GrvtS8Hj/AFmZ4RrqF+yVzPg4f6zbbRBdMt2SphlN2CGt90bdtkSY0yvSCf5NhH6awbdluukI2oINfprCt9X2LDP1th4aw4fNP+0V0HgBofx3gdr6SX/5Suf4aPmHfbK6J0btz9IODDuJOv2SssmkepAOyPJCyMbDyQUq0LLdBGUEG5SytJbED9UJ2PEQ5+W+qrWaNjP6Asmox+UDVdn6cX7TqmcZwd1YYXOHztAFlTyhptc6qywiVgqGtBWWTefpoahuYtINkmrzNY0jWyOrLgGlqbnqAGNLly2uqTpY4Obv7lfgDKFQYQ9rnCyvmnQLTDxlnOyrBFZBBWkLIrI0EbJFr/5u7TkuSYqXtxOfLf1l1yvv6O7yK5Fib8uJTj9JacbPkQKp7y9oLnJsQkyMNiUmZ7zUNFrq+pIGOiBdvZb+OfLtQYhEGtB1BUiNrTSi/ck41G4O7Ovkk07XuiAIN7Ktp0o6qE5zY21Wk4Ojc2J1zcXVJUwlsmovcrRcPNdFTuIHPZTlf0vHH9pmIRk1J1aoGIxP6jsubeyTX1UprHNDHKLWVMvV/m36BETekzBIZCztubfwR4zTyhhLC26gYViEgdlEbxfwU7FKl3VXLHHTknopTGCxyuJ6zLur91OAOWyzuCzufIbMcPMK+6x19ipqtrTDYx1bbjYra4c5vVN15LFYW4ll+YVgcadQAZrlveFy2f2dk/x22VxZVOI4kKaQN71Ah4phdHq8AnvUOprW1j8wIIVzC77Rc5rpOONeas8OqxUtBF1ly4XV3gLxawTzmpuDC7q+yoZUqyB3WO2ujeVDLqloABH0NE2RZUuwQt4IGiLeKAslFqGVBEPHZXNOPZHQ1MTm95XTXDslc447gMlREPNa8XeWmfLdYsezEJrgXTj5czLndGMOOneluwWoe0ua7xXVfnBzT6zWFFLF6OL7gKoqnl8jywHdORUVQ0HtO0SY2EEgnVTxa2vl38zaJDM7PlddXeGyMaBmVO6ItmunS90VsrrLbLxzY+rfFZordnuRUUzBTgX2VFLUPlIBcpNI8ltg7RZ6aftYvma2+uyvOC5TJXP8llpGOvutLwKCK59+4KOX/FfH/lHTWeoEdggz1NkdvBcTu0Ky49/CPNsCwkd9cxdjyrj/APCNbfAsKv8A/wCcxG05TpaYWL4fB+qb8FiulvTBab9aFt8MFqGC39k34LD9Lh/kam/WhFp66cpS3G1DIPHdISnEegyCw3QlGpPVb5rW8KAu4zwoW/3iPbzWTpD2WW3uthweC7jXCQRb8ojSyVHqxg7I8lTcQfzeTyV2wdkeSp+IG/k0nkqxO+ObYm4h2iPh9xNQ7zS6+LO9KwZgglJPeu7G9OHOdtO06BHdMCrjta6DaqPvU9ns/dAapoVUZcADclSBYtuEjVOOPLKKQt3suO180klXIXEntbLsWPMPoT+WhXHq/SrkF9bp4qQpTruiJ7KKfQpN9FrGeXpskZtVIhdYKM697p1jlUSkOdZESE2ASy/cgDomDotlRnkmwSlg3sig4OSBNjuiBvb/ADZJvqkDgPNKabpoGx3TjD70gN3ktv0SC+Oy/qx8Vitcq3fRKwHGpjrowfFZc3WLTi/ydrZ6oSZx80U4wdkJM4+aK4duyuc42x76+QAkBNwRBrG3N7BSMZka2tk11UeNxe1thYWXTjenPZ2YnDATe26bBYBySaqkkfcZud0w6glI0etIxy3ssCIyXs1S3SMa3Syoxh1R11zKbX11U2SgmMVhJr5ooiY0sfe1ln8bIElxZTqeiqIz65KrsTpXdaM7j5IgNUlUTI0Ea81s6OWM0wvZYyKFrJBYqzbUTNjAaVOtr+ummb1NrgNVJjswA7ICYjmqcp7RUepJmsHuPkgb2Ypqi19Fzjpgkzx0I75W/FdKip2WNnLmfS83K6gaD/WtT/QqHwY3/WV36oLpR9Q8lzfgto/jJL4RhdIPqlEBQ0CST3oDuRHdBMp0hO/IqcX+ksOPUJHctt0hH8mphf6SxO0Z5aLDP1th4RhusB29ddJ6MWX6RMJ8A87form2GfzcfbXT+ilufpEw7nljef8AlWOda4vTVuyPJElW0HkgNEKJQRoIDjcTetigLecbfgijo5G1IdyCVhkobSUrjr823T2Kx61jnE6XXVa5FdVREO3CfwgZa5mqi4lOWnQp7AiXV0bri6wzbY/prqm9m6XUKvPYZfvVjO4NDLqFiLWujafguW12SLLA7XFlo2+qFmsDblcLHuWlb6q147uMeSao0ELoBaMwQQQskNI9drA7yXJcTyfK1QDvmXW6zWB3kuQY7G75WqC36y24vUcnhMsEZs4WUWXEHQSMYHaHRNVFVLGGtFjdMGPrHse7kV0T/rlyXLIBVNDnaqXHhzWgaWVd6Z6NGO5TIsT+aza2spu9nIqMepRBZwte6l8NS54Hlx5qvxTEBVvDQNLqz4ciyxPFuaVXDNbURtrnAkBN1k8XVauGyexCFja1zy0XUeqbFIwAtCqFlKbw+eIu7LmqbVysdHq4KHh8UTZLNa2/krGuhYIdWhO1Gu0XDJo2uOVwOverE1g60DMNVW4ZFHncA1vuU70ZhmDso0U2nI0WFdqIPCj42/IwnkU/g4DYgANLJGLtBaWOGhGi5Zf7u2z/AMbPSSFzQRcaq4w17zEFXyRAMHmrCklZGzy5LtscMTdVccPSfPlpWc+UGZw3xV7gkojnznYhYcnjfj7rYDZB24TLKqMtGoShUscd1zOgtHbVGLHVCyYBEjshYoMEVkdtEdkgSdlzrjqURVMNyBcnddFdYArmHSOCZ4PMrXhv9mPNP6qRtey41G6uY33ps9hayx8bMr2OJ0vqtR8pUrKOznNFgr/K31pP4kk3s2KuIMNwFUiaN8ryNrqLU17CHlp3JTdGHOaTfdacOGrtPPnuaTHuY56iVT25rcgja13WHtJupppH3IK6q4p6jPAvdTsPI0uq58Up0BUzDw5vZJ1CzaLGVwvoFpeBTevfpyCzBBJWo4Gbauf5BZcv+LXi/wAo6Yz1RZKSWHsBC64ncUuQfwjdcDwnX/fmLroJuuP/AMI8kYLhHjWt+CVTfFxhv9HwH+6b8Fhels/yRS/rVuMNP8nwfqm/BYXpbP8AJVL+tS/atdOWHdLeB6BIfFNuSn39BkN9LrRmYo75I/NbHgqx44wkXv8AlDFjqM9iPzWz4JAPHeEa/wC8MU5KxerGeqFTcQm1NJ5K5bsFTcQi9NJ5Il8VfHP6pt5NUy53Um7U7WSZJFAfOXHXQLv45a4s8sZOzzqmUD1kj0yUfTTRkBCTbMuiRy3JJpK2V1UwF5IutjSkGFtzyWIomA1cfLVbiCLLA0juWXLqNeHdV2OkeiuHguYy4OZqmSTKbErpmMtvEQdrLPCFjWE3AXPctOnHHbnmMUXozgFBiZmcBzWh4qa3rRbvVTh7Wdb2rWWsz62nLj3TbqJ1gcqMUbg3ZX5bDYJMzYgLaKJzLvApG0rsuycipCd1aiOOwT0MUQOveneYpwqf0MgXsibTG+y0UscIYdtlELYtdglObYvDFT1GuyJ9PY3srMtjvySZ2s0tZXOTabxIDKfPsNU4KW243VhRsjza2UqSKM2tZTeXV0c4lR6PcWst10TRFuMVGn0Asw2NjRc2Wz6Lg35VqLfVCz5eTeLTDj1XWmjQJE7fmynG7JM35srl/TXTneNMa3EJLjUpljw1rdhoi4hc52JyNabDRIgg0aSb2C6cb1GNnaLU1zGkHxsjjroywnVKnpowPV53SYWRNaRlC0njKy7U9VjkUM2UgqXT4tHM0bo5sKgleXZG6p2Khhhb6oCrpNlOsqorX1VBi9QHyANvur9kcJBsBos/i5YyYEAbo6TuipaVznB2pWhpqBvUjNZUdLXNaQLFXTawiEEN0U2nE2OljLbWCq8WpGx6ge5SIa52+U6KDiWIF2ljqp20iJTAkkLmXS//ADvDWa6yhdOo57Em265j0uO6zEsLHfKnsaNcGMtxHUeEYXQzoxYHg9tuIqvwYFvj6hThUfMIHdDSwQJ8E0sd0hk9VTDTdYz+qPkVsukM9mlHmsaT807yKwz9b4eEYWPyZv2l1fohbm6RKTnaGT4Bcqwsfk7Ptfiut9DTM/SDGTyp3n4LDkbYvR42Qt5oDZBMhEDuQRoJm4nQNvQ0mv8AVN+CkSuELwcygYS9xoaP9U34KVXwzPLbbc10W6jm1uoGJVY9Y7p/h6sL6+IDvULEKa7NRcp7hyJzcRhFrarLJrjO46LK8ZWA6+ag40Q2mBZobqZPCHMZckWKh4xGRSt1vYrhuXbvk6WHDrnH1lqGjshZjh27tSFqWg5QtuK9MOWBbVCyOyFlqyJsUNUrL7EMpQDFULwuHguR452cXnG+q69VD5l3kuMcTTvbjc7QLbLTivaOXxFnja8tUmOhc9rS0aBVEz5euj105rVUE8QgFyBpzXRtzKbEmBjQClRAOpSAOSVjoB1BFkKFg9G17kbORTMa2Oa7+RWowN8bmOIWZrW3kNjrdXHDzHtid2tb81Kz+KQRyVLhc7d6rnYe0j1nn2qRXsnNY4hwAtzCNzZepNntvbuVaRbtFoqJsc2bM4+ZVjiDGPp7B7veolFFOSczmnXuS66GdrdC32hCf2LCKZrHO7Tj7Va9U3Ne5VNhQnMhzuaBfkrp7HgjUbIonq8wVgEdtTdMY+4MjF9LFScCv1QzAX5KLxZFnpTycNbhcf1rkejMd8ahfJmivnSYZvm9ZFBa95iItdOQyHq7Ftl3SuC49ldcRUN7fNbYOy4eJGaENuCFz2VhZKHAra0Ej5cLAdcjKufmvcdXBj1VNJxnXQvczLfKbbqRg/G1VNiEUUrey91r32WarnBtTKPEqLSTmKqZIPoOB0Wl4pYw+7K9AUkokia6+4T6w+DcXQSiGHPZ7rNAJWzp3GRgK5bNXVdEsp1BHlQypGJBHlQtZA0S7Y7LmnSGPn4dOZXTDsVznpAb89DfvK04v84jln9WHlLWRk2VXNUkvIF1b1DAWnuVXlYJnAgLtym3LhdIuZznnMbBXFBI3LYaqA9rLGwUnCmC5CeKc7tLYfnDoVKc1vVnRGyNt+SRUvbGLXVWstIbXsu6/JPUuV0hsFBlO+XmrPAoDI0uOpuot120x76h1zbnZafghv5Y891lTSQNa83C0XBsY9MksO5YcuX9W/Fh/ZvmizQlW8UbW2aEdh3LkdRK5D/CMZfA8JceVcxdgAHcuRfwjdOHsL/98xTlQnYf/MIR/dN+CwnSy7+S6UafnVuqD+Yw/qm/BYLpZP8AJtL+tRL2rX9XMCjk/mL/ADRckcjv5Pkb3lasjFH6kfmttwI0P46wnf8AnDfgViqLRsVu9bno+bm4+wkW/rxf3FRnejxepxoAqbiAXpn+Su2t0VPxAPyZ6X+lf7c6ro88qrpYXAq5qB89bmoNRG7rRYaL0uK9OHkxlqEIHmwsnm07swBUvqzHHndz5JDahpcLclrMtscsJiTBTujrIrDS62DHltO245LNQSgzsNtir81DTCAN1lydtOPU8VmNSExG3cs1lke1wuVo8XflizcwqD0vsusAubk96dXFNsZxO17Jhm2uqikkPWgK24oqDJOB4qjp35ZRZb4z+rPK6yaNjHOaCbhRql7xIAn4esfCDc6IpIXktLllNSt7dwpgdkCUC4oZXNj3UczFvsT1tO9JL5JMu6jvkcdrpDqq+iR14vsqmJXKHLvRvzEJ+lppKu+QCw5pFSx8DixwsQnL3pNn7FE5zdlOYXObc7qtZNY+KmRVDndkKcorGnS1xC3XRVARX1Lzf1WrFObIxgLgt90TkvmrCdxlHxXNy3+rbDW3T2gkJE4+bKeGyRMAWFZ3wpe3McelDcRlNtQmoal3Vsyt3UzGqcOxSa4BukiERRggWsFvjeozynaBM2eUaC2qq5WVkTyACQrV2IxsvdwBUGbFIMxvIAfFbYxjbNmYn1e5abpdS+r6gkA3SYsVgdJYSNKkurIXM9YEKk2qelmrw9wc02VfiEkzpvnBbVaZk8IBOYKgxd4fN2SCUJ0fw9jZHMAGp71qosOLqcENGqyGFvfHO0uIyrbwYgyKnFyApyn+l46/ZmDDCL3CqcZourdsAtDHiMbho7dZziGpMruyfaokrTr9IlJDa4XL+lUfy3hTD/arpVGXlpu4rmXSdc8Q4S06/OKtJtPcIf7Q1h7mhbonsLDcH649XHwC3DvVTx8Iu6SSh3Ije4VFpjekI3dSi3ese7806/cVrukE3lphvoVknD5h/kVz5+tsfCsKHzEX2vxXYuheIfx+c4fRpXfELkGFD5mG/wBZdk6Ehm42nPdSnn+kFz8jbB6BQRoLRArIIWQQHDMEA+TqFx/sh8FczTx6DRUeEEjBKJ390NVCqK6X0prc5st8sdspdVZVvbfysrLAIY/SoLWvm1VK8vewOurHh4PFdCS7d2yw5Oo2wvboNRTNMbfBVeN9imBtcXF1cVAcYmkaqk4hkMVLc7Lzfa9L/wBU/h2VrnZQtUwdlc84RqzLiZYCbBuy6JH6oXXxzTj5KOyGVKQWu2ROXwQLUq9kWYIBmdvzTvJch4rhYMcl7I1AXYJiDG5cb40m6rHZLa9kKuK/3Tyz+qong7YI2slxOkbIwX7Kgz15MrW62KnNktG11l2Ry5FYgXdXbmpNEw+h69yq6yZ5AT9FWO6ktKBFfNmFS8EnQrS8OxfM95OqzNe6zy5p1K0PCrnmI5ibKas7iuZkriIydFVipnDTeL71OxmtbHVlhdy2VXUVzI48wKcT4k0VTLmN4iPapdZM4w36snRVFFXNkOYO0Umrrg2PV1k9J62PD55OsPzThqrN08n1DdU+FVjJJSMwJWjZE1wBFtUr0qerjh15lgu64PcUnilgdSuAcQQFKwNjRALKu4sL2wlzXaDcLhv/AOj0Mf8A82bZdsTgRfRN3szTvSY5zJGdLHZGx1oz2ea9CdRwZd1GlkcHai4W5wkA4ULi12rDyyBx2t4rcYaSMKFvqrm57rTr/HnVYfEWNNbKCfpJqKlY7UFQsYqpBiMzQCe0nKKSVzbkELrxvTjzndWmEOEWNUt9s4XcKAfMt8lwrCnOfjVK07mQLu9ELQt8lx/kf5x0cP8AjUlFYowEdlnpRJCFkoBCyNDZBGi5x0jWY+AnvK6URouX9KhLWwEadoqsLrOJz7wrGSyMc21wqyenc2UuF7FRI6qT0sMLuytBljdTtJsu+1xydqdsb3OtqrbDqYhug1T1EyFwcbNvfmrCARtJDbWUY57rTPj1EQkRnXRVeI1rWqfiUga0kLCYzXSiY5Sd1drmvTT09qhtwtLwzEBKWG1gsPgleerGYrQ4fiD2zh7HWUZz6x1GvDlJlutTjFOG5JI9CdDZXXAkLjUSude9gs2ytfWkB2w5LXcEtAnl8guXPcw1XXLLnuNq1tmjRDLryR8kFCwt5Lkf8Itl+G8OJ5V8a66uT/wiG5uGcOPMYhF+Kjk8PGlUH8wh/Vt+CwXSwf5Ppefzq31ALUUX6tvwWA6WL+gUn6xTj61y/wAXMTzRyH8hfvuhySnn+TpBbnutmEMUeoj05rfdG7c3SBhN9+u/7SsFR6Nj8wugdGjv/qHhXL53/tKz5PFY+vUgVPxA38lefBXAVTj/APNZB4J5daGLATC0+qQ9ovmvyQrNJ90v0Z8jAQu3HKSdubLG29INVVNLco8k3Q07nnNbdWEfD75RnuSe6yl01I2ma5rtwnjzY61inLhyt3kgNjySgK0iHYCrZaqIVWS4JVlC67N07luJmOqjYmxphIPcs24QsDiVpMSIMRHgshVaPI5Ln5PXVw9RmeI2skqGZO9UcUZZNfxV3iYvNr3qC2MZx5rbC9M88d3a3oqgNhsQlTVTbgAKPG1obuEgkdZYlR8ze170lmUGLZRJMpdopNm5E0xgfM1pNgSqnRXtGdH4BIcPBX01HH1WwFlUVAax9gnjntOWGltgdVFDA9jyGkm9youKyNnqi5jrgC2irw5wcNfYpcQa5pJ3S+ZL9K39TRhjBfmpFORG8EhLbE3NuEfVNzgXCLlKcx0tJamIwW0Wz6Jngz1p78q57k7NrroPRJHaatP2Vy8s1j03wu66mCky+oUsBIm9QqL4ieue44XenSlo1um8jpKcXJ23T2MuDa6XMdMyIn5kWGmW6uXo7j3VBNhrXOcS4qtkwONzj84VYVtbJDYBl7qtOKT3deJdmHnTizs+iIMAYx9+scp3yYGttnNgoEONTOnsYip1RiT2xXDPuTTbCvk9obo/ZUNdGIp7E31VozFpMhvGqCtqzNU2sRqiQ9xa0AbLUNbotS3DxJCNVjsNeY5WuAJN1qxiEjYBZhSsVLKlRYYGtuHbKnxaJkLwXferOmxJ5abtPtVLjcrqh9gFPatz9DpTDlLrbrlHSWQ/ijCQB9NdNpIniM7rmHSCL8W4UD9Yp1MqTwh/TtfptZbZx7KxfCIIxvET4hbI+r7Up4o5c3REobojqmTFdIB/KKb7JWUefmH+RWo4/J9Mpx3NKy0mlO/yWGfrbHxKwkDq4Lj6QXZ+hEX4zq3WGlKdvtBcZwgfN0/mF27oMiB4nxB/dTgf8y5uVtg7mUNkqyFlrpmQgl5UE9BwTAniTh2htziCfZggkkEhVVw7Pl4coHf3QVi3iFkTg0kd266P0w/9grmmmbk7k/w9NK/EoQL2zKNV1jalubTVSMBq2RYhALD1rLm5fK6eP2OmyOIhBsqfiPK6gNwrZ04MTdFU8Qva+hLTpcLzML/Z6OU/qrOD2BuLgt+quksPZC5xwlGI8TBHNq6LGeyF3S9uPKdHL+KGZIJtzSRIL7qto+Tj3dlUVbj7KSpMJBJAvorlz25d1hOJCRiZLfqp4yZXQtuMXs3EUZhJFwVy7iKpFZiMsxNidFopqk9Q5t9bLL1VI+aoc7vXRhhJXPnnbNVVSBhkbdXUFK6eEWuqyoo3CRpVpR1wpmhjitWVFJhjnG3JFNReixZvBSn4mxnaJABTVVWMqaewIOii3L6VPnTMz1fWP0Wo4Ulc+JwI0CycsOR581ouF6ljQ9vcrqZez+NuYysuQNuagTvhkhy3apeORQ1NTd2+XkVVPoInM0+KIdKgqIIBu1SpJ4Zor3abqoGGRPcQPipTcOZGyx+KpnascJbCJriy0dP29BsFlMLp4YZT+9aWiqoI7tJAvtqs+TcnTTj7vbSYSwNi00VLxkZG07iG5vwVzgzw+MOaRZU/GrjHTF2UkW5Lhx//AE7ehr/xstTgmAlOsYTAdeag08+aIgFT6YZ4SNV6P6effUCUuz2BFr6rd4c+2EjX6PJYmWDI651W1w2zsKAA+iuT8n9O/wDGczxR9sUmJP0lIpKlobYG6j4rHfEpxr6yco6QkXs4rswy/rHFyS7ultgnax2kP94Piu8Uf5kLguCAx45SA/2g3XeqI/MtXJz3+8bcU1hUlEiuUApA0CiuUl7iGpb0cB0gA3XMulAektgjjILsxV3xHxLUYdV9RGxpFr3JWMrqqXEqkPmN/DuV8WNtmSeTKTGxi/kmdkvWXt7E9JNJG0MLtVq6ilY2Amw0WPrpLVTm2XbLtx022rnjk0dutBh8r5I7udcrOuaXvBFlpsHo3OhaSSiSRVtqtxl0gBssvU4e+oBcd10Kuwjrt76qI3h9uW2qfTK41i6Sllibubq5wsyRk5r6q9j4eYDsVIbgrGa2S6OYlYM9xccxK33Bv5+b2LEU1F1JuCVsODJOrnmzHuXN+RP67dXBe9N2OSPyUGfEI4WZnOFvNKgr45gC0iy5ZyR0fFS1yn+EKf8AVigF98Qh/FdRM7e9ci/hE1Q+QsJiv61fGfclnlL0JjYnUWlHHy+bHwWA6Wf5hSfrPwW8oz+Sx/qx8Fgulk/kFH+sPwSx/wAmuX+LmJPelvI9BfbvSXeaEulC8+K3jmNUrtI/Nb7o1eG9IeEkneW2v2Suf0Z/NnxC1XDdY+i4tw6dju0ydhUZY29RWN129dmVrW3JVHjdWx8T2A3NlQ4lxHUZcrH2uFXUtbLM3515cbp/xZ30fyYzpHq7CovZTaeojDWNNlDqG55CQmDHICCDsum4bx0xnJqtnh8kJgvoqLGHh9VI2KwFlGgqZ4mENdoeSKLM4uc83J5rHh4rjlutOblmWMkZaQyQ4qC/ULT0VWxzAL6qFU4b19RmsnIqJ8DgQupypOIRulbZp3VUMDdJcu5q1dVNZodSOQ1USp4qw+gf1c08LJBrkBzu/ZalcYuZVEfwlFLq5gJ8lmeJeHm0LWyMFjeyvcS6VMBwf+fVohJ+gI7u/ZvdYXiXps4br2ZIBVyAbu6kN+4lK5aVJs7QwvnvuAEUtM+Opa3cFZek6VMHguQ2qDCdzGP3qZD0i4RX1DTFUWP1ZGlpKy+7tp89Nd6CREDzso76VzO1bVO02PQ1cDCxzQHbEnQ+1HUVNmJYZZVeUxNB88zhE3mbKcOGjKzOZD2d1UNrxDK13MG6u6fiWLqnMtYnmUZ/c/xPD4v+ShrqV1FUdWTfTQpkVDmmxOikYnVirq87dgLX71EBBdqunHudufLq9JUT3yu0Oyddna66bp+xqBung/rD5LO+tJ4djc42XT+iaMhla4j6TfguYMdlIsul9FuIRMbVQudZ+cOseYsufnv9WnH66gAkT/mykiobbcJiesZkOqyyzmjxxu2FxpgfVy35FHGMsAB2sm8YJfPI5mxclSAup7C4OVVj5FX2qyobHIbEAhRssOtw1F6HLr2/vVZLQVHWuyyaE967uOdODO/2WEUVOZNm3UmWGIt2FlRU2G1IqMxlNvNWdRSzGOwf96ei2cMEXVGwCy2IMa2qNgN1oaegnbG7NISs9WU7oq0l7r6ohbTMKa41LQQFs4qaN0IvqsfRvYyRpzC6vPTsrAM6nKbXjlpbiniDTYBZvFXNilNgrGKtvGbvVNiDhJLq7VLw97LgnAiOnJco47eJeM8MHdddPa5rISMw2XK+MnX43w/usUDSz4P1xXET+mte89n2rIcGdrEMQd/eLXP28UTwFX1Rg6pIvfdGEww/Hx/L4B+gsxL/ADd/fZaXjw3xKIdzFmpv5q/yWGfrbHxPwbRtN5hdy6CGXx7FXchCwa/aK4Zg/q0+nNd26BWkYri5vcCOMfeVy8nsbY+V2tBBBdLILIIIIDzTgEn+q1Dz+aGiq6vM6rba+6s+FYzLw5h7eRjAVpLgTTIJNNFv+mO9VDZIGwAHTRSsELflCE/phM1FMGODTsrjAKKJs0L+ZcFz8uptvxby1p0js9Qy/cqTikZcPc5hOgV5IwGnbY8ln+JnZcPdc6ALysZ/Z6lv9UDgupdJijWuH0SunxeoFyXg2dpxlluYK6zCRkC7f/ZxW7xJqnFkZIWGquOmUtbLTvY67HWW1rpWsgcSdLLiHEMkfy1UOzWu66vDCZXtGWdxnTfx8asmabMcFVVtb6ZI6ZxtcLO0EjOpa7MpZrGCLSxW845j4z+7l6TUVVnGx5clCdXNukvqmPjcRYKoMx64nktMWWev0sJ6i5CY6p8szXNBsFGfK50jdLrS4ZBG6EF1tloxqmqoHvZlaDdOUtLJHAA4K4EEQlIJCeqI4uqs0BLfZaY+raGk3FlOwBjZHvDDr3qJjQsCABvyS+Ey8SyAjXzTp4peK08rqjSYjTuTJgkMQ+eN7dyk431wqAWNB071Ei690RvHr5pno3S0szpTaUn2KRUU0zBrIR7FJwSGV8xL2bHvVljcDmwdiME270bSy9NHP1xHXaeSlthqxOD1vZ8kxh/pBqnXi0v3q86tzS3sa+aVpz1pOFXSiGzjmCb4ynYKV4cbXCc4cmIZZzSFD41mj9HIdYhcNn/kejjf/Gx0LmhhIsFOpJTkJLtFWwduM5bKRTB1iO5ehPHDT1TMXu7JAstvghzYU2/1Vz6drmm5IF1vMCucJBJ+iuP8qdR3fisZiVMw4jK+wPaUujjaIyALFQcSqQyvlBI0KepKyMgXNlEuWlXHHY6V3V47TabSBdzw+QOgafBcLY9rsVgc364+K7VhLyaVl+5Ry2/UTjj1VrmCGYJnMUYJ70fSfk7cJEp7BQzJEh7BRb0JO3LePKsw4q37KoqauEkl7hWfSG0uxO/6KzNC21ybLr4J/SObnn9qu6ytvBlBCoHUBqHOl71KqZAWWCiRVvVgtJXRr/THHX7V7onNqMt7WK3WCAeiN0WFc/58uJOput3gZzUzfJRluNMZNrBwBHqpIaD9EBPFqKwus91eoTlaNmhIcQPohOkBJLUbo1DYt9UJ6mqn0kmeLQpAA70WXyRe/SnSXU4rUVLcr3aeCRTYlU01sjzbuKaDLhAtsLBR8Y+NJlfU5/EVYR6wHkFhun+qdJQ8ONJ1dOHFaZ40WL6epDk4Yb+mFhyYSWaa45W43bZUZ/JY/wBWPgsD0sH8iov1h+C3dC+9HH+rHwWC6Vjeioh/eH4LLH/Jpl/i5ubWRSn8hf5oydEU38xee4rojmMUjrCM72IV9hc9+KKImwtMy9hZZ6lJDY/NXWDHPxNRH++Zy8U56MvHfZ3teRcckjrWRcwEzUkh7bdypsRqZWyhoNl1xy2tLG5rxdIfVQxGzrKPhbi6mBJubLP49USxznK4iyZNN8oQeCP5QhHPRYOKtmMzQXlSKitdAM8kmVjRmPgjRStw3EIBuQAo1djEEML3vcWsaNxzPd4nwC59PxMKWN9TPUspoG7X9cjvtyPcN1gOJ+PKjGWSQsmlpqMWAja7tOA+sfwCjLKRpjja3HFfSrhVBDLF1vXPbe1LS+sT+m8beIC5LjPSRjeKMMNKBQUhOsdMMt/Nx1Kp6mdrzmbJAMx9U30VbUPlf9OKQDYNNgPYs7lttMZCpaom+bM9zt9dymXyOPaLbJPWy3N3XI70PSJHAj5tpHgoMk1Eg0a24slCqjaAXhxPO42SS92hzNI8AmXPDrltr+BRo1/hHFEmHPzQVU0dtbA3B8CDoVvcG6QKepa2Ksc0C3rs2Hs3C4/2Xc7crpUUslOQ4O5+sEdzwO/ueyRrXxyNe14uHNNwQpNMRbW1lyDhvjGWgnbDO89U46tB08x3LqWGV0NbA2aGUPjdrfu8F0YZ/XrLLHV6WBc3P3poFvWlPxRNc7UpMkOV9wU/Bq1NpzHlG10GlmY6JNDFnIueeykz07YwSCAsbe2s8IBaNNFYYNVvhqs0T3NcOYNlWAXN7qXhzRHUXBuSnJv0Wuk03E9QykbES5z7WzEoqWqleDmleb8iVQRuJA0KsqIONtFF48ZOoUzyt7WL5GF2UkFPzBohJG1lENOD2ydSVMkI6gg6iyx7221NMtX4uylNspN1TycSQkk5Xe5X9ZRwSmzmBVj8KpDvGF2YeOLP1HpsdiebgH3J+bH4mDUGyegw+lYbZAEqow6mePVCaTNPjsMjSAVR4vWMkn7JWhgwynYxxawBZrF4o2VY0FrpGcwxjpZ2i9x3LROoZMjSAVV4C6I1YLQDYWW4AhETbgKLlYuYys8ykkDT2SqXESYpRcELoAbAWHbZY/iDqmTjTdG9n86VoYXQZgN1zDjA5eNqHXZpXVo6hvUZcq5Nxu//AF3o7aWYdkaO1c8DvzVWIH+8K17th5rGcA6vrTf+sK2ZO1+9VPEUu6IFD2Ir63TDC8cu/lVg27CzVQ61I/yWi44IOLN8GLN1P81f5LDL1tj4ssJOlMF3joC1rcYPPLGD964NhOno1tV23oGr2Q4ni0LnjM9rCAdza65eXrVbYd9O6oJhlUyTQOBToctsc5l4zss9KQSSQgq2Wnm3hF2XhmgdbURhXrq7NYWVDwhY8I0JvrkUiesETgNbkronjnzxtvRyveSbje6kYLWS+mQM1tnAUOUunZcA+aLCpJG1sZsbB45LHlkrfi3i65JK4UrbalUXEmb5MeTtl2U/0txp2KDxJIXYS897SvNwmsnqZd4KDgotOLx23sV1+E/NjyXHOCSPleKx5Fdhh/Nhdmc/s4sP8VFxhXvo8NlezcBcMrJ6ioqpJHalxuuy8f3GDzEX9VccYJHknKbeS14J1tlz+rKgMvog5GykU0ckkBF9dUqiI9EttYJ6ilEcRJstd9o/SDHTujY64uq+oe2OTUEK8lqonhwFtlS1YzyAKqzKgljcRpyVpT1zogG6gKhfKKctGxKlSVJMNxcp49pzmosquuexmdh1SqOtlqIgXaIqKj9NiANyCpkmGtoqYkA6BO2b0iKWtj60uF9bqbw5ThkjzbVUfpj56nq7kXcQtLgMeR7iL696WVk6XhjbNouP1Biq2tLXHs8gkRVI6i+R23cpuNOj9JbmcAcvNQTWRRMylzbeacK05QYkY5HWY7TwTuIY3nblLH+5MUVTFI82LfepFcIRHclu3enpG+0GhrWGRzg1w9iXUY0GTNaWv18ExBUxROcS5vvShVQSzN9Um6VVGx4WrRJHY3HmFE45fHJTZSB4KXw46JzMoLVXcdQNNOS0kG265Mv/ANHoYf8A5srQuaIjlU6jfqdFU4VnyOzHmrqlbZtwNSu39OO+m6kNktcLaYJI0YQB3NWNkB8FrMJNsMN7bLk/I7jt/H6rB4y8fKUxOmqTSygDv1TGMyfylNv6yapn681vhh/WMM8+6vKUh1fDp9MfFdxwgfkrPJcLw7tVsGv0wu6YR/NWeS5PyJ/aOji/xqfZGNEV0V1mRaTJ6hQuQkSvAYblKnPXL+PGZsS2v2Vj79U11gQVseNXg4jobjKshP6jiu38fyOXn9qtfUSyXsDooIqH9YQQpsc7ACCoMj2mYltu8rqch0yFzhpzXQcAF6Rnkuc9a0kLo3DrvyRmw0WebXD1bnkia0JTh3JAIbuVk2KLbckgpy9wkEd6UMghFY32R3RgWGqadDFwEnUpxouENAdUj0aeLNNwsB0+yDrOGGj6wXQZbZSuadPMoNXw0O4j4rLObsXjdSt3QuvRx3/s2/BYTpVI9Eovtn4LcUR/I2fq2/BYPpUdelodfpn4Lnxn9nRl/i54dEJSfQH92ZEdkUxHye7vzLdzmKUG0YAvcq6wgiPiOjJ5TM2VPR9rqhrurigbbiGnG/zrUT0Xx3AyiZ4tyCra+HNNtorClYWkX7kmofH1liuqOWyJeG9mmA8FnsfZmlJAWlpQ3qriyocVF5iLA3GitNZ+OJwmabWVRjGIRRzzSyy9XTUv0idHyfuHxV5iNY2kg61mjiLDw/8AhcZ4xravEJxS0/ZpInmxe6zXne9+ZUZ5L48CeIOJhiUxdC1zmNJI1sAe9ZeoxSZzrmNtjvre6bfI2Jj2ySAuGzWNII9+6gOmc7UOPuWNdCRJUvewjqAG8yEw4Ntc7HRCOqtu0g94SnPuO0BZIC1I2Itz5InWB2SWnITbZB5Ph4EDRANvcAdOymnPObQXS3PuCCOXJNubYXGo70wIyXJQZM6M94O4Sb3+KF9LJA/ma8adnuPctRwjxJNhtQ2F7z1btD4ePisg12VSYHkP0JsdvAo87J6Cw+r9Iia7s3yg3abi3IjwTsk5a7XdYDgDiV0krcOlcxrtTA5x3PNh8Dy8VvJCyYBzb67g7jwXThZlGdmkuiqXF9mlSZnyOtclVdFL1M2qsXVLX2ASuOqqXoLEa6qwwVpkqNddVAEl9lZ4AM9QSDpdSbYwwDIDdSqXsyADVQJKkQgCyn4fK10ecjdY239r1P0kS1DhJlA2TlS94piWjWyZa4SS7i6dqphHGbnQBZ2dtJemWrjiDnu6sECyqbYsHHdaSbEIGXzPATLa2ndd2cd67MfHDnO1G35UBGhSqh+KBote6uoqymkfYPaU7U1FOxoJc1PabFThz8QMZ6waKixkzCqBtz1WuirITE7K4LJ43UMNSLG4ujQ/azwAF0oDAMxtdaOtZW9UOrAuslw5WNZWAEgXW/bXwGNuYjZZXGtZZVZT/KAj7Y1sqbFWyPmAetY+vp2xntLH43WZpgWEGyUxqtyQzJG5sOllyTjRxPGtP3hhXTXVlxlJXL+L3340i20YVetRH1tfdHurKs98hWydbRY/o8/MVR75CteeSJ4VLugD4IkQ3TNguNTfF/8AAs5VfzV60HGZvjJ8GrPVhtSuWGXrbHxZYWe1T3W66PJZG8QSuY9zSGnbdYPDLZoL9y3vRm4HHKku+qssptpjXauC56iSqqBI9zm6est23YLD8J1Ecc0guLkrYtq2WGoXNhZhldtuTG2RIv3oJj0lh5hBb/y4svivNvBcpdwhRgG9mlO1eHzTStcL7qL0fEO4QpM3cfitfCYcrb22XZJuOXLLVVMLPR4rPHvKXQzRMm001ulY2y8V4zZVVAHukGZ53WWeHbXDO2OlRVIdFGLXCRxHM0YW8EfQKTRuYynjJdyCY4lljOGPAN+yV5+v7vTt/ozXBc5ixmEuOhuu1007XRA35Lz9gU0jKuItcBY7rqVLjktPStzO5br0M+Lfcedhya6qTx5I35KmBOllzGlfB1VzvZaPi/iH0ijfGXAh2i5zHieUltza6rhx1Ec13WoikHVHLskNa58NgTzTGFStmiHirCPLHGSq12N9KaOnmjLi5xOqSbF7e9TnzNe1wGirJnBsgN+fJVZtmOqw8vDXa6KTBAHNyEBPCriZCA46qP6SyE3zWuU8Ijkq2pqz0Bo7gpEuKtrIC0dypaqRs0Fw42sk4ew9X2blX8/tn9aQpIRBUdaBsVo+Ha0TyvZayz1YHMuHgtF7qw4VdG6rfldfTXwWeWMt23wyutLbGaeOSpaS0HTmoM2GwmLMWNVli0TTOxxc4ad6jy07X09s7veiVOUQKGKnik9RoN1LrRBJGRlbsquLDHGYnrpLX2upNVQObHrI8e1aSs7O0WKkp3OcMjUbKKBs7SGC90xDRkyH5+T3p8UVpWfPP370rFRs+HaRjQHNFr8woXG8JNMcjyCBqrDhtmWIAPcbd6gcaRS+juLXA965LP8AyO7D/wDNi6EuYCFfUN3REk7qgpnZbjmragqcjLA7ldmunJb2Oe4O/NajCXk4Xr3LI1TiHBwN7labB5M2G69y5eedO3gvbBY0HHEprH6SZpw4d+ikYxpiMp1HaS6aIGO5/wDhdGF6jm5J/apWGTEV9OCdM4+K77hBvSs15LzzRSdXiMOo9cfFegMCfno2H9Fcn5P+UdH493jVtdC6RmuhdYNNF3VDxNixwukdKAT4BXd1kePHfyc8eIRJu6PybYaorxic0ksu97AX2UCanY7PZxAQggdI45TzTWKCop2uEYubLvxmvHJneu1ZJQRNcRncUmkwdskpykm6hTT4kO0YgrfhupeX/PAB11pbWEk2RLw2c4IvvdanD81HTBuugS3TREfRTsLmTN0Iss8ra0wxkT6KYyR3cSotfUPjeA0lORSMjFs1kbhHKb6FZy3bWyaO0shfGMyOoeQ3RNtc2PQFKDmyaXTLRMN3DW6arJnQtGVSWuazS4TUjWSb2Key0coZS+PtFR8RqHREBuida9kXZBASZBHMdSDZIaLpXmaHVcw6dHZsQ4eA5OA+9dPY5sQsuU9Nb8+JYHt+cR6WtOi0brUjB/dt+CwfSi69NQj9Mra0T/yRn6sfBYbpON6eh+0VzydujK/1YElHKR8mvbzLu5EdkcwHye/vurZGaE6xc9dloMFAk4opLi15m6Kgoxd0V+9aHh/TiujB/tWpz0Xx292VpAtyVNWi8411urmRoc4EFV1TSZpb3XU5cljQi9NYG2iz+OufE8uHLQLQ0kLhFbMLKsxijc8F4ddp0IIvonfCjlPF+PGGlj6p1i92VwdytffuXN6utqq6dzQTFDe972BWq4tp6jFcX9HZlfd2UFoVZiGFnCaU07XOcbXcC3S/eufLLt1YY9MNiUj3zOF72O/M+agOPMbc/BWGIN6uZ3cdzyCgObr3hKUAwkkHW/d3p5vqm2/imGC/Z7vvT9wWgaFFAjfS3usmy4g8x5pbm6aXsdifgm3yEnK72IApDmBdz+KbEha4keRHeiLiNAdO5IO6AN4AN27FFfkUnMgDdBFbhLikyu12TbdxyRuTNaUc74ZWvicczTdhG7SF1vh/HxitDHVl13utHMO6Qc/aFxWCUxuv3LZ8E4l6PiJhJPVVIyuAOzuRRjl80Wbjp7cxdcbKZS3J1TVIMzQXCx2PmprYw0khdNrHSQxrbKzwKzZyAeapOsINgVc8P260knmoVtcYnI8yMaAVdYc1xpW66qorZY87FaUVSI4G3PNZ5NMZ+0uGFzJb3T1bF1sZBKiNrwHgW5oVVc7qy5rQSOSj57VvpV1ODRynV7kUeCRtjIzFIGITyObaPmn31s7YSRFddUnThys2Yp8FiikvnN796kVWExysALj71Vw4xUGfKYdLq1bWSFtzGlYLYZiwiOGJ1nFZbFqQNnIaLrVPqpHNdaMrP1besqLuBBVQkHD4nRTB1rFXclU8NaA4j2qBSQOdVWAvorGooZhlyhKnKJs8jmG5cVFla0+sTdWVJQTBhJCo8ZkkgnDcpv4KVQDTNcRrzXLOMOzxoBvaMrpcFQ4hoLTuuYcXuvxo4j6iMvDnrU9HQ/Iqg98hWuJ1Hmsj0d64dKe95WtJ2UzxVLKSN0De6IJhgOLzfGX67BZ6t0pD5q+4uP8ALUnkqCuP5J43Cwy9bY+LLDdXw627K2/Rtc4zUn9FYjDSOsi29Vbjo1NsUq7H6Kzq566XSTy08hfG8tKnjH8R2FR9yqmXFyUBJZynLjl9bY8uluMdxIj+cf8AKgqwTgBBR/Dj/pf8rnnR/c8I01jyKtKiqnikYGEkXWe4BqyzhamZ42WokZmjbJa/cvQx8eZn6clc+eIB19Qmqel6pwcLpmorerj0NiE3TV7prXdcKMpbV4ZSRrDWllM0AgAKFjuJOfhzmhw1amuvaYLG17KnxSYdVbkspxTe295rrRGCSFs8d+9bqeX8iGvJYTCnDrWaW1W0zZqPU8l1SdOXfbL4yzroyL6qgGF59QDdaDGH5IyNL3VRBUljDdxU4KzWWFQmnhGh08VY08zXR9rbVVdHOZIybkJ5jX9Ucp70v2f6JkqIrua0i11U1ufrRZwAukM60TOLiDqk1cjgR2VbOiqJZCA3MBqjrWSNgBz66KDIZjK020JWhdA2SkaS0E6c050nLRmMO9Eu53LuVrgDm5LPc0lVdaSym7LL6d6j4ZUTMjJyke1VtGlvxA6NwIY4XUPgqOT02Uki11W1E8j5DmBVzwnmbUvOVRZ0vFfY02QysDHgG3NRJGVAp9HtScdqZ46lmSMu0TDKyaSOxhI8Ejvo8OZU9cc72Wv3KXjLZ+o+bc29lApqicSG0LrqTUyzOZZ0Z2T2Wu2cY3ERMQHsN1JZFiXXMOZhF1NgDjNbqnKY4Oa9vzTkj3poOGRM2LtlpUXjCaUwOAYCPNO4bVOhaDkNlB4jrA+F1wRpZY3H+23Thn/TTK0zAcxJ1R+l9U7s2tfVQ3VDo3uDdQVHdI/mN10xkuTUmVgItdanAXuNAQ7uWKgdZouFpMOreooiBvZY8+O434c9XtQ4zrXyeaRTzdWwhMVU3X1zyeZTgjs3ayvCdMs72TC/8uiP6Q+K9A8MSiSgjIP0QvO5OWZpG4K7DwJjokoGMc7VuhWHPx29xpwckm46ChdVMmMRs3cEUeLxuFw8LD+PL/TecmK2JWP4+v8AJ71efK0d7ZllOM8RbLTOjB3Rjx5b2LySzTEQ1LoQT3FWNDJFXAl1nKI+EGjkdY3TGA3jjfvuV1Sua7WNXDSvu0ZbrI4xUnDJgYhzVs2pdJiLm30VJxawiZu+qvxlbuCjx6d7SRf3rT8N1z56XO7eywkPYaRdbDhY/kZseSMoWF7FiGNzw1Lmt2CsMCxOWqvn71n8TAFS4396tOGCBmN+aWpo8cr9aXU0kplNrqRQve5xGoUGprWQvsTZS8IqmVDyQVP6GNv3pX45iUtC/sk7pOC4w+rc699O9HxDAyWcA7bhNYLTxxSHKd1nL230bxfGZKapyg+8oYRjUlTOWlwKg8RU/WViLhyn6urOgW/zNOf7v0v66ufE8AErnHSxK6WuwNx+uPiuh4lAXyAjkub9Kji2twNp36wfFK49H9d6dKonH0Vn6sfBYrpKJMNFrs4rZ0h/JGfYHwWK6R9YqP7RXPY6d9MM5uiOb+jna80bropz/JzrfWSSaogbxW71cYdIYeIqeTmJAVTUQuYh4q1orfL0Lf7wKp6WXUdkw2udUvuTsoOMYvJBVNjbzNk7gthLlBVfj2Fz1Fex7NgV1acmNtjV4bUOfSZ3dyz+N4q+N7mNdYfgr7DIXR0AadwFmsdw6SaU5WklzrAIqkLhHh2GpqKrFqxjXAfNxbe2yy3G9NG6eWzWsY0WyN2JsusSU7cHwiOkaR2GdrTc7lck4tzVUswtq9efyZdvU4uP+rkeMQAzucABc7clSPY5juf7wtdjFN1RlBbppqVl6qLK+19DqFfHltjyY6qOQQA4bjn3hKtpmB0KJpLQNNL80hzurcbeqfuWjMbnFp3SXESNPMjkjcRe3I7JhxIdcbogBwJsQkJRcAeXkkEpkBQGqHND3JAPil3O/wBybRgoBeXTMCrPCqh0U7XBxBbqq1h1v71JiAhc2QHsg6juRfDld34bnNdRRyF1y5gcbHmND+CuACefgsP0a4j806mc6+V4Iv3OH7wFunEdojYrbDLcRnjqkOab3Vhgz3B++l1XB5KsMGd857VaY0c8ebK48lPpXtFP2trqvnMgaNQn44XTUwDTZRe6veomidp1GXRK9LjsQSFSNwycyG8xA7ko4VLn/Om3mr+YwudXcb4mtzdlE6vp7FpcxVwwmUwaTm6qncPVWckzu96fSKvutpmuzHInWV8DgQC2yzz8CqXMyic3TMXD1XGe1OUSQttOaqHK49nZZTEa9oquyQpT8GqmxE9eT7Vm62hnbU+v7U5o2l4fq4XVhLt1sRUUzgPV2XMsPbLBJfMfO6s/TZw8fOOt5qMu1zqN86anbESA3ZYbHZ431otZOvr5DAfnDsqF7Jp6guJv5oh29JhkbdosN1ynis34ymJ5RrpYgkbKwk7EX1XL+KXZuMKjwYjLxOPrZdHgAwl5HN5WqO41WW6PRbByf0itQ7cJTxdKCIFDkiHuQTnnFZvjUvkqKu/m3tCu+KDfGZlR1/8ANx9oLC+t54ssPBEsdraNW66MG3xGsPgsLQm0zbfUW96LYi+qrHDSyieqjpBDQwqLlu5PvicRYINp3AK9w9ECLTkgpTYHEckEfUDkXABaeGqa5vZy38DoXU7WusbjZc74Cbm4Zp9bWctPI6cFga8ALox8cefqVjEcTGEgKDh8ketrH2IYk97ou0+6h4c1rQSSQnZ2Jel+WhwIudlAxOFvVaE3ASzUFrbZlFq5XyNuSLWU2NJ4cwkBrm67FbOMh1IPJYrDiA4d61kE4NOBfkrnjOes7jrbxktBuCqKGYgWc0rQY45zYnEtuO9ZQ1TdsrlGLStJh8rTCbaWUmKob1R79VT4TKXwmwKsqSMyscANbm6Wu1b6UktUDVuGo1S6uUNjDrKRJQlszrjTe6jVJb2WlaRhmhTVYu2wO/ctBSB9RTC1wCqSqjZDlcVbUtU6OlGU2VItO4gz0eDW7hZSMApmVMTnZb+ajV8rpKfMSAbI8FxH0eJ3aCek7oY1SNgLnBoFkfCFUZK57bKFXYqK2Z7L31VtwixgrHADkorTFbY09jZo78woD6qOOLMb+5W2OkCWPQbc1WyyR9VY2tZSq+o2GYtDJU5bnQ9ytcTrYYob+HcqWimhjnuMu/crKorI6hgabbJ2F+1XDjEXW8z7FcU1bFUObYE+NlXwU8T59AFZwBtM4A21UXf6XLN9pL6uOGwF1W45UtfTO8QrSVzHMzEC6g4lSmejcWtvpyCP/wCqw73pjHdpwRSNtZJmc5koZlNx4Jby4ht2u9y2BwOc1oV1SOzUpBPJUoeMuUgqzpH5YbLPPs8FVLaOpcfFO9dmYTdO1MLXOLrXKiloZ2QEY08sQZCZXhy3fCDSyOwWIjm6kAEFbjg+duS5Tlu0ZSa6aSQm/NJY8g7lLnqYwCbqEK1mffRXpl2nCQ33PtVJxDra/Mq5ZMwi+iz/ABHOLab3UZzpph6TCxnobwSotEwCKTLruoEmKOip3C17dyfweuZJEcwsTyXN/j66d/XUUlM+VuNSBwNuRUfi57nujsLqfV1UUOIXG50UfGLThj7Xstpd9sLjrpmDHMW3Fwtlwk14oyD3Kid3ZVquGIrQajkjK9FhO1RidDVSTueyNxb3qbw0ySMPDwQb81tIKOmlpu0Be2yrm0LIHOLQAFycf5Nyy+bHXn+NMZ9RjMeqnsqy0PICuuDagujvmuqDiKFxrHWaSrXg5j443BwIXVfHLj/kZ4pxgw1mXNaxPNDhXEDU1DjmJVPxZSy1GKiwNrq34RoTDM4ltrpTpWrae4hqAyqGtikcPVYfV2zXTXE1NJJWAtFxYprhmnkjrSXNIC030y1/ZrqyRjSCSuU9LMgOKYLbXt/iul4s3UakLlnSpcYpgo/TG3ml+hr+zqVG/wDI2fYHwWM6RHXjo/MrW0TvyNv2B8FjukF146TzKxynTeVjnFFMAcPcbbuQdvdKnAGGk31zbLNRij06q2pup9LIGY7E6+zwq+jF3Qi25CnQxOdjbGW1zpz0s/HUsCrQ6quDsFdVmKQslaHWuVneH6RzJz5JzGI5BVs0JF+QXW4eO6ja0crZae42so8ccctbHcXyuzW8kWGktoQSNcqhUlWTib4u6MuUcl1HRxTeUhXElUS02PsXPcUpfScx+kRp3XWyxqQucbm/es3UsDiQvG5c+30PFhPlgsfwls1PfLlNrEdxWBxLD5GRmzb5N9F2LEaYTscNGubse7wWIxbDepJ7PZWnFnrpz8/FtzqUloNte8JouDhYkeBVpi2Hup3l7dY3bHu8FUOte33Luxu3nWauhk2OU+wpBPeEM9xZwCI6b+8JpJOmiRslkaHuSD3pgEPNFdGkB7oW70XsSgfemAacrvBTaazgYzrcc1FDQ/Q9k8ktuZtm3sWnQpBteAK40mKspySTJZvucF15z2tZluuF8PTCHH8PqHnsmVrXW777rtkoNrk3O5V8UGd6OMkaTZWmCND5iQdLqhhkaHHW9jsrvAHkynTc8loj9NPVXDBZHFWdRD2hfTkm6qYhouCl0uR7AXC6n9nfCH4qG6hhPgiOMt+obqaIqcGxa26akhpy71Wrb1zXZdLjDZGDsFOTYjG2MuylOU0NM2P1Wp4w07mEFjUk9qmhxuOeUtyu0S8QxeOnF7FTIKOkifcMalVdHSzN1Y1LatVSfxghkiIyuVDU1LJahxBWqmw+mZE7LG0FZmqZFHVOAARVzRzDg2aQ+GiuDhsZN7hUlPOyCS7ArBmMAkAgIicr/pLNBHGwlU9S+OGQ6qzfXGSM5Qqt7WSP7Y18UHjejPXB0jbFcn4jcf431h3sxdg6qIWsACFxviB1+La49zUsjxb7o/8A6EB/SWmJ1CzXAQtgbCe9aTW4KUO+l3BSb2KMnRIugOd8Sm+MT+apK8/k7ftBXHEJvi9QfFUuIH5ln2gsMm88WlDbrRf6i6N0TEA1rjbcLnFD+d1v6nJb3oxmMbay2l3BRJvo96dPErSbWCeDm2VEKp4c7zTkde8yhir+Kj+SLsPFtBdBV/Xu7kEfxUfyRyDgeQs4XhIGzyrWpxd0Dw0g+5ROjWmbVcNEE7PPxWp/iyypYHOFyF04+OTO9qj0k1cXLZR488ZtoBdWmJYX8nxHKCLKmgbI92oda6otrR+bq725JLrujsbJ8tywnyUeS/VXAOymrlKo3ZHgEhaal1pwdwsbSmR0zRbmtzRwkUYJ7k54U9UuOPYadw0WREIc+zRZabH3ExuFh4LMUrnMecxJCnFpausLj6uIjZSqSYx5rO+kVBpphkNrp6jk0cSOaY/Q3VhfM5pdyTNU1pcw2CJro3zuIAGiXVR3a0hxsFcZZGayhNRAHACwKezshpgC0KTHVRNpsriL7KuroxJHo8i6aFi97JKPRo2TFHCx0brNFkmKO1LYvOycoG2iPbKZVWGFjKl1gL3Wl4SjDK11xrZZ6pjInc8OO+yuOFZi6vIzclGS40uOxRvkjDhrZVD8OjkjPZuPNWOORufJFaQjRR44nCnI60qYrJT0+GQ9cWtb96spMJjijzZbe1MYfSyCtL3TEi+xCvcRjD6QgSW07lSLe1LQRQMmJt96sJ/R3Pb3+aoIqWcSutUH3Jfo1QZW/PnTwSPTQSNhDBz9qsaUwGmyusPC6oG00rmi8xT9TDKylJjkdcDRRlGvFdJMeB0tXUOc1rd+Slv4VhLD2RoFX8JyTuJ61xJvzWyuOrd5I2r1ybHKYUVUWNCFK8dVtbRWPEmGzVNeXMAsokeGTMZ2tlXsKVDlfZ510QZGHG53TFbeneQ5IhrBsnIq5a9KqyGuAWp4ZbKY7sBIWPqJC+VuvNdE4UkiioxfeydvzESfVOzPfqCSCmQxxFw43Umrd10pLNVFdMYnAObZVKzs70m073tZq5U2NyFzhc31Vj6TmbYKlxRxLx5qbemmpL0XS0cVQwZrAfFSaeiiguGkWVLNiD6ZtmqIMamJ3ssbjtf8nyt6nC4n1HWHKpsWDsnjAOoWYlxiYkWWtwCodPS5jfZGtHMpaYfgUDTrYKxoKJlMzskbLPY1i80FSWM5KwwXEJZ6Qvfe9kXehLN6WTqowOLRILJ6mkbOLFwN1zzG+IKmKucxg0Ct+FcYmqr5xaxWf8cna/5LemkqsDjneXGxJTlDhjKUkNaETsTY12UlSaeqbNfKUv5P0cw/aurMGjmmzkApyiw1sDyQUdTWZJSL6oqeqc96qVPWzlThsc0mZ1vam4cLjhkzNA9iXPVFrwL2TUdS5xOt1UpXWy6xkbjYkXC5L0vhrcXwRo+v+K2+K4lNFVFovZc76UJXT4nghO+f8VUqL66dSnLRs+wPgsfx867aXzK11KfyNn2B8Fj+PDpS+ZU5eKxZMpNR/MD9pG42Sp2j5OJG+bvWLQzRNuYvNW2Fsa3iGIONwHqqoBeSEeKsG3Zi4I0IcnPU5eOv4L1T5jlsrOppIZJASNVmeDnvc4lxKuMQqZY6gBu1117ckmlwxjY4C0bWVRTxBuITSgC+TL7ypEVUXQG/cq6Gub18oGpsD7FjzX+rp/Hm84axaxkygbKklZcnusp9diUMTnSzPDWDUlZWp4zonzuELC5oO68fPG5Xce9M5j1U2qgD232NrXVDWU2e7ZIw+M6Gw28VbR4vQ4lGBFK3Nf1DoVEqphGSDmy945KJuKusoxeNcP8AzbupAkYRy3HsXO8SoX00pu02XbZ2smaRYEEXVHifD1NXNIkZy35j2rp4+bXrj5vx/rxyInTtD2pN7bC4Wjx3hk4fITESW9x71nXsMbrOC7scplOnBljcbqgRfZEWX5aoFwPfdLhbJUPbHGx0jjsANU9phggjlzQ3GmiekjLTZwIIOoPJJ6sEdm/kjY0Tpz0Q15IiORRi/tCZFscO5SZGF8PXMN7b94UYWO+hUulzXMdwXEeqdnIB+hm7McjbF0T2uIv3G4XZa7iJvyfSyQFr6mrytiYdru/cuH0khgnNiLbEHmFe4XWVdfXYbQU4c+SKQthF+839iX18+Kkl9dcihdSxMjzF793OP0jzK2HBdL18hJItdc8peJqOChc7EJcs8ZtoMxfbuAVvwv0rYHh1Q0VENXHE4/nOruPuWmPJijPDJ03HaYQsFlX0zXTRgNdZSa3GKLHMNZW4dUxVNPILtkjNwVU01c6mJuCQq32jXXae+iqiSRIbpiWjrRoHXS24y0WJa4JZxqCwzEhbbYahFPSYiW6O+9O+iYlb1irKhxGCSK7SnJcRgjaSXWRtOoozBiYdo4qRFDiJbZzlOixKnl1DkUuK08TtXhTs7Irp6avbGTmNll6xkwqHXaStrUYnBLA6ztFmZ5myTuIsnvZSaQcLoaquqHMAIG2q0LeEKkvBFrKPhFfHR1BLufNadvFVMLAlLL/jTHX7VruG54ac96oHU1QydzXAaLaTcSU0kDgHLLVFU2epc5h9ynapIrZYpxM2+gvquQY+f9acQ8rLs8src7QTquK44b8TYkboyLF0fgUWwKMeK0N7EaLP8EC2Bx+JWgO6U8OjPkknUjRGbohuEBzfH9cXqPtKnxAjqox+mFcY7ritQR9ZU+IerF9pYX1vPFlRayO7snct10aD5qqJ+ssJRkiR1h9Bb3o30pKo/pJY+jLxtjLEL3tdIiqIhUA6KAWOfKe1unYKK0ufMdluxXIqobbD3oKtdHY2DigmW2B6LagR4DK0/XK6HR1N4gN1zPox/oabwkXRKSQRxXNlWE6ZcnqLxBKDHcrPQTMJ7J17lc49MHwEghZOlqSychwGpVaKeNC6YCM37k3JUN6rLdKGV8dyBsok5Ab2e5RWk8HTyNEgcNSCtNBi1qcNItyWPpHkn2qzp7PO5RpWPp/Fm9dGXjzWdvYuF7FaGvkbHTOaN7LICR8kzrnS6Idi6w0F7Td19VPiiyRvu4jVV+F9hp1VjTvEwcD3oP8ASpjlPpjgXc9lbVT2+jixF7KA6lYyd5573UTEKqSMAAXBVRlnDc4nL7teA1SXulfDZtjpuob5nvivk181osDp21ELS5uttVbLekOTrW0uhaDZM4e6o6s9ppVzjFMIqc5W+4JnhqBs9w9p9oS0f0q5TIc4cAPFS+ES9uKO1Fsqssco2QRuyt1sqfg+UnFyHAiynJWNa3HhUZozGGnTvVaJa1rNGt8rqdxFiAp3xdlxBHIKA2tbJDmDXbdyUVdCp5awPvlYD5oYjXYh1dgGkeaaoq0STEBr9N9EvE6nqxfI8jyTlK6V8c9eBfI258U4yoxAvA6ptvNMtxHtBvVye5SmVwaASx/uTOreF1UY9Q0K3oaV00NpH7qkiri9gAjft3KwoKydptkIBU2bVjlpY01EaJxcDopBxyKMFrni+yYlqy+PKPWKz9dhU8xzhxGvJT86VMrfF96VR1LybtKiV81OwdkA6KkpMIrI33D3WPepFXSTxNJeSdFQ3WbxV4fIeWuigRxgOvfRWFZQulkBFwFFfSOYDbNdVuFZaRNYOBG60eG1EjYGhry3yKycjntkDTcFaXCndhgPMqc/FcfrR0FTlAzXcfFSZntlscl1f4JgcM9I15aCSO5SZsDEQuGiymWCs1HG0Mvkt7FSYwcrrgLV1VFOCcjNPBZnGYZGG0jCLlX+ix9Z+pjmkGbKSN1BcyXUhp9y1sBp20/bsDbmmmmjJsS1Rs7jtknzShwGU+5b3hm/ofaFjb3Krcyi6waMWgwt0Qisy1rclGV2rHHVZbGIXvxA6EgnuV1hsAio3WHJP1XovXHOG3UmF0Rp3ZLWtyRvoTHvbm+NtvXuuFbcK6ONrhFjEUTqtwIF1M4ciY2U5bKr4WM/sRik08VQcpNrKz4WqZZQ4PuplVFSud2yL+KkYVBAwnq7exZ6jXtR41VSxVvZBsiwTEJJalzXg3Cv66khe8lwBVbTwRQ1TiLC6csRce9q3HcVkpagBrXG6GBYnJVSuD2kKwr20j5fnbX8UKFlIx56q3sVfpOu1Ri8jW1pBG4WE6TAPlPBHC/rj4roeIxxyVl3W0WF6Uo2trsDtb85yTkK3tv4Xfkrfsj4LH8c7U3mVrYD+Sst9UfBZHjg3FN5lRl4rH1lHXRzi2HX/SSrGyTUgjD9T9JYtSKI3khHiFYw2+W2B2vaVbRHLJCRvdT4AX4y25+kielfHVOFDHn0AWhqooHSAki6yfC7Xxude90nGcWqoK5sbBdt9SuuRy7a91MwQOy2WPxaaXC62GotmpXOMc9hqy+zvIHdauhkfLQhzty25WfxOdrXuY9ocx2hB2IU8mP1NNOPP5srlfG2KV8uMnD4SS0kAAK5wPhCgjoBJXZpZH6k3IV7jWEUcr4awRNz5Rbw5KHWVLYqGJwDzcuAymwsF5Gedn9Y9vj45l/a/tV1/C1E0iSkllhcNhmuo0EdbGernc2Vo2cNypRxAZTdrte9wTlJK2qkyg6lZb363+ZPDbIiLEi6RKy7trK5dRZBmsbeCrqhmVxtuotXjGWx6jbI1xc3Q6FYHE8MLJC5guO5dMxVhc0jvvbwWNxGmOe4DhrqF1cPJXF+RxTbHilkkkyNbdxK1/CmBmkp6ite28xYRH4DmmaDDg+b1bAnU+C1NEWQ2Y4BrANddLK+XlutRHBwTe6zmG8PDF4XCpF3uPYmG7Se9Z7GMDqsGqHMkFw02JA2W8wN9dgeIvhiayehleXgb2HgVccZ4bHVQQYhHG1lxYi26yx57je2+f40zx69cYktcG2p3SdvJXHFOGxYdWRtiGVsjA/L3FU17c16GGUym48vPG45apbTcjvHNPOGdg1s5uoN/uTTWk7f/KRI97LtBNiqQVnd1hzaOtupFBWPpJTIyRzDlIBaddQoLTre6ejbdw00KRyruixSoY1oBBNjqpMmKzNAsGPcB2gR6zfLv8Rqs42RzAWteQOetkcVU+NwOY6ag7kFTcVfTpfAXHJwrF2wB8goashk8biLBx0bIByPI9+67dhjIpr5wCvLVKesqIpmgXP0QO/mvRPDcs1VhcErXnMYmki/OwV8V70nknW2tbQ0znHshNTYPTSHa11Djiro2Xz3KbkqsRjcLNLvYulyf/8AF9Q4VBDFbkhUYdTyAglVRxDEGw36s3UM4niZJJiPuTRbF7TYVTxXSZ8IppDe5VA7FsTsfmiPYm24xihNjCbDwQc00E2F07Kc2KzctLkncA7mpjsVrzCc0Rt5bKHDO6Z7jIEjuk/B8JZVTHM64Wj/AIs09xdyzuG1hpZCWg2VlJxDMHaBFlp45SJ8/D0DIHWcsy6GKlqHtzKfUcSyuic233rLuqpaqvKPii5yzpZzRAvDwdFxHGXX4ixM+K7fIwsjGp2XDcTdfHcTd+kpyPCuocFi2CQq9J1CpODrDA4fJXZOqUVRlFe2qPRJTEc1xk3xOo+2qmv2h59pWmKm+JVH2yqyu/qPtLnvreLOjiMj5LW0Zdbno/Jbh9Rb6yw1GXgy5dsuuq6D0cRg4dOT9dLH0WLelkldI7QjVTWGfNvon4ImgmzU667D6q3ZVVTuqusNnFBLnqHCQ/NkoJo0wPRfJbB6jX+sWsxLEDTU92mwAWL6NHn5Kqbf2i1WKnPRO7PJVjek5+owrTVwHM42IVYIWicEO5qZRMcae2W2ijGmk6y+m6vaNLkN+Z35JPVNMeqJkb+rAvyRSsIh1d7lFXDMDGNdYW3VvTwm1xYKkpm9rcq6ilyRh5BS2rGCxOklNMX2BsCsW27pXAM1uuiyTMqMNOnaIPNYimiy1kgeABdKLtTMJhkyklhAup0BczP2T6ylULoxEdRomnFtpLHmgfpXGdz6l7SPanKqlY9jdNVXhsorC/MbX2V8wNdA0mxK0xY5qSojyANa1WdFiHodOOWickgY9hdomo6Q1Lcobp3qmaTLiIqqb1xbdNYTiQgLi13NIlphRw2LdlHw98ZDtG6lGz0k1+MiqkdGXXNuaTw69kOJB5NtEmKkZPKXWGvcpbaFlMOsGht3LO1pMau8WljqTHlcCQFXS1UdOwAuAuFAixSMVTWOdb6OyvanDIp6PrC0HTuSxylul5cdxm6rKPEoWvJLxbvU+eqp6mG+ceCqBSU7QR1bVIhZCxgYGNVVH7NQTQuqcmduhV6aSJzWm7VSwUkMc2fI3U9yum1kLWNbZt9khkdcyOJmhGyTHiEEA7TgClyTwmO+gVRiFF6XC+SM7JXo5Ft8pwucHZgfaprMTpnx6EXK5/IZYYH9s3aE3w9WSzscJJCdSst29t5JOm+GPUkNwSLjdV1fj0VSckRBuFhsXke2oNnkC/epWAMdJUbl11rPELearc0huQknwTTJJHk/NustHDhLXFriBtzUh2FxAX7KBusFijcsgJFtVZYeS5sZHeEzxNAyObQ87J6gu2naUZeHh67HgFdFFhrLuANgrqB0VUy+huuUUGLyuphHqCBa91vMDqTHQNzOuQ25JWO9tbjZ6v20MBOwWI46pYYWAtte6vI8eb15Zm5LIcY4j6Q9rQ6+qc2npiMTnkjaQ1xCoRV1WfR62MmDOrWB1r3VXLw1K2TsjRXKzyl2oZamqc4WeR7VvuE5Huo+2bm26o4eHpMwLmA2WqwSiNPEW2tolloYb2zGNNq3Yg7JI4N7ldYGyZlG7rHEmyl1eHGSYvyKTDSujpnAttoldKm9sDjD3Gvf2iParLhYHrHdolQMVo5XV7yGq44VpXxyOz6XKd8KX+x/EIKh0pcJCApmAGZhIe4lWclJcns3COkpMjnWFlN1o5btVYjWubOW3IUakLpag2J9qk4jQufU3AS8PpXMlvlSmIuV3pQ49R1b5gY3OA8EzgUFXHUO6xziPFbSaiEu7bqN6CIHFwar/SO/pk8ZleyusHEbLJdJUl6zAmk/TWyxqhfPW5m94WK6T4TDiWAgnXMn+h+3RKcn0Vv2B8FlONhpS6961lMPyVn2B8FlONmi1N36qMvF4+ss7RJqh/JtwPpJTgjq7DCxz7SxaI9CPnIfNWlCAceZtbPuquk0fEfFWNECcYaW/WTnovjqPD4b1pAsrGtwiCeYPda6p+F8/WOLk/imJTQ1zWC9iV1OVo4Yuqpi0cgsrjlPMS58bczhs29rrTUk2eku462VNX1LMxabJ2DbOukqpcAE9RRGF7ZHtZHnDnOAtrfbclcy4ixbi2L5x1PHBSh1mRCz8gPeuv448M6qlboI2BpHjufvKzmI4SK+HqXEgBweW8jbvXi5ck/kr6DHiy/ijltQzHaiZrBVZS4AkRCxFxsV0DgvBX0kDXTdY57tXFxuSplNw22AgkMIJv2ea0tHRCFg7NrBRyZ76jTi4r7TVXFaGwKzVebPNiLlaPE5sjbXssvVzBzidFi38VlY3ML3CztW27jcbLQ1DrDzVTUwZpC5aYXTHkmyMGpWSuFwACVbcTYVDDw7PMDleQLW81EwlnVvIvYjYKVxPT1uM0NHQ0LWl73XfmdYBoRlezwx6UPDc74ntY4XYSNDyWz4ipicMpGtAb1huG9yXhGDwYRRQUgij6xw+cmLbuc79yPiurioqF8z5M8rW2ZfvWVu8unRJJj245xjKKjFpiw9mK0Y9iz7tB3q2xK7pHkm7nEknvKqnbHwXr8X+Ongc/edo2OtbU2+CKYZwDm1Hgki+43SXPJ8lqx2Ibp8OLW+SZbrqU6BmaSN0gS/UOPeUGjZENW+1ONGg9yAl0cro3tAuPq+C9J8KH0LDKdsgAyxNabd9tVwvgLBHYrjlM58QkggcHuBIaHHkLnxXfqfMyFrTHEANhnvfysNVXHOxnf6rZ+NU2QRhwzv7Nv8+Clmup3WOdtuSpaXD6eV2eQnrDsANvBWnyHAQ05yuhzbqyZUU+QDMy/mgXwZb3Yq4YGS7MJDZOvwVz47ZyE9ou0jrqW2pZdJ66l3vGqp/DcribSmyZPDMwF+udp3FKK2tKurp+pIDmAqijfH1ry3Y9yRVcOzxMLhK4jzTNDTPizNcbkd6KN7WMETp3ENKWaF4dYk6qz4comvcXOcNTzWiOExFwJDUTJNxv6YmTB3dWX62VdHAIKjN3LpNVQRMpTbLssLXxhs8gBAR9n86MTVrHx5b6gFcNxA5sXxN3e8rsXorusc7NsCuN1xviWIn+8KnI8I6vwiMuBwb7K43IsqrhUWwWn+yrbn3JRdH7Uk7JRSXaNPkgnM8TN8QqPtlVlb68H2lZYj/P5/tlVtb+dpx4rC10RZUm0xH1e5dB4Bk6vCJSNLvK5/S+rNpy71vOBw1uDvLj9Ioxm6MrqNbQ1Ocb31U0lp5hVeGujINu9Ti8MJ8Fvpz7pEgZnNzqgostXHnNiggbc76J4hJQ1rSNnray07HNLXLDdF9QIKOvPPOtRV4nlZmJsU8PE5+pVRBHDTnKPcqZkuZ5AadE/DiXpERBN09T05kDnNt5rTW2fYmTkiwBvZNymV7NBZPNb1b+0Eb3AxkgLPJtjrSPSt7QBVnVuy0wtvbRVceYSi5sFYVulM2+uiUVD1FpQEk3WVrp8lU8gc1eMqSyhIaNFnHyNklcXDW6cCzwmqkkDhbS6nRk3kuDuq/CZ4m5gLXurKOQOe62uqBFlQYK6shc5oAO+ybPDdfms06XWu4WjaYNQr8U8f1AsP5rjW94ZnHOm8O1eWzvaVLp8EdQw536ncrcvhiA0aq3GY2ihdYW0Kf/2Lekf/AFpIwOKujq2Oa1lyNNFV0GFvZE8mNw15qzw6ZoqJWyuFsxVnJVU7KdwBafauje445NVncOEgmc0E7q0rRI2n1PJVtJWRtxB+nZurevq4ZaWw5rPW46fqSxkXuIqL+K3EUslRhdml3q8lhqgfPkja63HC9bA+hDX6kaFZcd1k35tXBno4JTIQXvvfa6lOoJWt6wmSw8VZOhBxFxaW5Lq1qmM9FIGW9l1OCVkmk7Z3gjxRCN5kac77eaRNHKydxB0ulioMdsxCILU57XCLdx9qVSVjI6Z7HEi1/agKgSU/K9lFa9gicCNeazznTTjvaBiEuaGQgbhQuF2SOLwARqVdxYeayMhgJuNErD8HnwvM8s0Ouyzksjo6rO47GY59e9SOHq0R1TRqmsfl62cgjW6HDseetA8FtPGeXrf/ACk0Rgtvt3KOMWa8EDMpTKEOjGnJJiw9jXnRSTHY+90k4JBtdT6PSkZ4JHFcQheCO9JopL0YsdbIvi8PVvRTAR+KvWcUCnpst9Q1Y+CfLpfVFLI887LOY9r5OT+q7j4jcZrkW8VDxDFRUyt12UGNrTrbVRXP/KWgK4xxtaimxmOnhAdbbmo0nEUDX62GqieiGWMONrBQuqhdUZXWRZorndrR/E8TT2Qr7A8QFVDn5LMMpaO4DiLlanAooWw2YRaym3asL2Yr8aEE+TVSqfEBUUrneCaqaCGaYki5TzaZlPA4N7kqeOXbF4piAZWPFlY8OVYleTroqnFgz019wLqw4cyhxAAVXwTLtf1eNCnflzJzC8YbUl1jdUOJujExDgpnD7GEOc0AKVb70ViWLthq8pKfwrEmzyWus1xDUthrzf3qVwzWsnmcG2T10W+2qnxZkDspdZRflVkxIvcKhxqu6msDTzR4VMyqeQEfPQ+u9F1lcxlVYn3rBdKkrZcYwQt+stbjDAyrAssZ0iN/lXBCeblX6R+3SaY/kjPsD4LJ8a2Po2g5rVwaUzfsD4LJ8af7t7VGfi8fWYchV2+Sx35kHFJqiPk8Ab5li0NUTSXwgb3Vnhgy44zPr291Bw63XQ6c1OhsMWvt2+SePovjqOAFjpTltqp9bg/XziQnYqh4Skc5znE7KdiWPmCsbFYm5surTl+l42DqqYtvyWWmie7GIzIfmY7yv8m6/uWpp5TPTZjzCqMZYyCgkdbtzHL45Rv99llz5/OFrb8fj/k5JGbqMQFRWOe/dzrqXDkfr36LJ1VS5tS7uB0Cs8GxQSv6t2jvNeFP9vp/1pqqaka2926N1BSZpg24HJSGOvT35c1VVbjZ1tOfmqonSpxSZzr67LOzusXXvcq8rruBIKoKmwJS0m1GkOYHmo8jNNQpAbroEmUbKmVMwXjJuNeatMDfJU4pDTxQSzuyuJETC5wA1LrDkFVvNu+ydwbibEOFcXbX4e6ITOjdAetvlyutvbu39ickt7T9WTpuONcGdw9G6qp5/SKeARmSRwDfzl8thz29l1yfHsYlxOTtOPVMNwDz8V0bjjEOF6yTFqabEoKurFOJqeWkLi3r7gFt9nE7m+wOi5PWjLCQd1d45L0y/lyuPbPVzi57iNuSrD+cVhVHtEHZQJG2cu/j6jzuT03qCkOAudEs+sjawEi61Y6IGh0TkbspSCNzzQbqL9yDLcLC7fVJS4ml1m7a79yQwgjVONIaLpB1bgdkHyfnw9uURZesgleCHn61+XPUe1dCwp8dY13VMcyRjrPiLu0w/D27Fcn6O6sxyNjY0Oe5wMY7+RYfA/iF0+8YczE6XNBa7XADVvePYeXuT4hyeLdoqo5Rk6zyJVnFVVTWjOw6dxSqGvgqI2SHKX27XmrT0qnLRbKV07clhqLEC2O7o3E+aX8rWb+aKnsZC+PRrT7El8MIb6rbITqq/wCWrC3VmyhVXEGQ26onyVzFTwSbMCRNh9NfWNt/JM9VSS4t11ObxuCpXVXzjnWPkthVUkDabssCy4p2STOaGg6pH4lYPjMlOSGsc4A6WVhNxbUNdb0aT3KVw5h9O3R7QDdaB+GURds1Sc3WSl4sqJYspgkHsVJNVGVznuDhfVb7EcLo2UxIDVh6wxskkba4CJ2d6QYqtrs7dfVcuMVRvX4gf74rsLA0GRw+oVxyU5quuN95j8U8hi7DwyLYPTj9FWn0lWcOXGE09z9FWdtVJ0ZSX2DHeRSuSRJ+bf5FAnrmNcQa2Y/plV1Z+fp++6sKwA1cxt9Mquq9amnHisK6ItaN3zU+htZbrhGHPgZNyLkrC0wAim7lv+EmO/i+LGxJKeHoy8XmERtjYSXHdT3yMkLhdVmHxydWRdOQRTNkJL1u5qamow6Qm5QT5Y6+sgQTLTm/RkQabEGnbMFrJcJNWy7QbLF9Gzw2LEL94XU8HfE+EEgbJY+Dkuqyz8LNFHmINgncOro2McOav8dbGaZ2UarJ0kHzji4rWMt7Wz5Gk38EQmb1dgASkShuQWcNk1GAGW38lnk1x8TKLDZa2TM3QeSn4hg04pQSNknDMWipGBryBZaKLEYK+m9UeCJOlxjYYWikc0jUGyzc0P5Q5rRe5W+lwPrjI5hIa43VbHwlkqhI5zjrcqZVZRTYXg84zPewhp2sp8dKYy+/IrfYZhsDqbKGt0GqalwilL3AsaU9JlL4TJ6mxWizNGirsNpY6VlmADySn1Fp8t+a4s5/au3DLpNdqFCr6c1MBYOamEaJiolEQuSp/ar4wkvAxlne8PcC430KH8R3tB+cefatQ7H4GPLLsvdWVNOypiziy2vLlI55wY1hafgsQZ3ak2WZxZ0lDUmHObdy7DMxpieG2vbkuPcV4VWzYs58eYMvyTwztGXFMYgBpkF7qxwx76eUAOIB5JNHgtS2MF179xVnT8OVDwH5iO5X/wDxKZ1rW2dpmSzWZgWk3Cq6ukqoHgalIjiqpbnKRZaTPpleObW1JBDLI4vA8k87DaWWYCzfJZ7r6uF5Y0ODlNwilxCacyPc4Dkj7H8a+bhlMLN0B7goOMYVFFHdht5KPitRV4c8SEnKq+fGpKyEC9rKLn0ucXbQ8P8AURtAfuFf1ApZqd2UA6LnUdfVMbaDUq7wGqrpYZPSRbeyrC7hZ/1umV4oa2OtLWgKNw28sxEEdykcRgvryOdkfDlKWV7XHuWm+i06FHMRE3yTDqktJKmQQAxN8kzNTs1vbZZqkY7iyo6wgc7pvDQXU7R4JXFkQjfp3pGGTNZC0HuTvcVj6cqPmQCmnVBLbgp2ueHx6JvDqZtW7LuSbAKdzGbrTDgy5MvnExHVvDiLomTl9S26uqnhk00LpGvzaX8lnmjLU28UY5zLxHLwZ8WXzk1UVQz0exsNFQVEbjUlzH27k6+Woy2jaSFGLa069VqqrHXZ5zJSRaUracLlwprOdfRYMmuH9UttwiJTTfOCxsll4rCdrV8ZEubMlSO+Zdc8kiZ7g+1imJ5X9S63cs9r12xuL05fWOIcArDhuEseQ517qhxKrqWVjxkNr7qfw5V1D5S4tsAVpvpnJ20mIYEah/WF+VOYLQCmc5uclQq/HKqK7GxE6JWCVlVOHPkZlUz/AKv9kY3w/HXTl2exSMAwIYfO8573Kr8exivpqnLHGXNQwLGaupqCHtsqnjO3+y3xPh2SvqQ4HRSMN4ffQEucd1a0tVlF3EX8UdXiGcENHLko+v00+ZvbL4nSNkqjcrA9JjBFjGCNb9dajG8QqY67sbFYvpBnfLjOCFx1zK/0j9uowj8mbz7A+CyXGuhpvatdB/NW/ZHwWS42OtN7VGXi8fWYcEVWB8mN01zI3c0ms/o1p2IcsWpOHm00OnNT6ZpkxsM11cVXUJ+ch7rhWeFODcfaT9Ypz1N8dG4YpTEXAhScQwQzVTZrHQ3TuBvaSSplTWAShpXU5OkiFpgpLcwFluJ8RcyGI2NmXBPdqtWHZ4D5LN4pFG5xa8Nc12hadiFnzcX8mOnR+PzfxZ/TB/KmEV8z46esjdUf2ZuCT4X0Kh0dQ+nxWEDm+xC2LOB8LkYaqjhEcjTmcy92uH4KviwGP0zrixrS02bb4rx+XivHdV7/AAc85sdxraeS9ILm+irau5JINgOXepUUoZCG320UOqcCNNFm2qnrdGOVLJCXnUXur6WMuaRooJpwx9ze4CE1WOhtoo0w1torORurlX1GguiIyQZXAHRVta4SXBtsplRIQdCq+d4JNibq2eVQoYvnNBpyUbF5BEw8zyVjTi8hVfi8V39Y4aNGg8VWPrPLxmnxOLiXDUnX9yZqILO07lcspXOcXPaCe48k3UUeY2sfYuqZuTLj3GfERfI1jRcuNh4q2rcAqqKhNS9jgQbObb1R3k7JmaiynMBbVa7DcYwOughw+aSSCZ7cjs7iWOJ5HlqVvjltz5Y6c/J0ISdlo8b4MxHCaqbq4HzU7O01wsTl8R4LPkEHZWkTTlG2pTsDXTPbE3VznADzSGRyTOyRsc5x5AXW84H4LkEzauua5ryQ2FgGrSfpHyF0jkMcKRy0Qc92YPppo5Ry0dobfcu44bGyaJsjtY6yIPtbTrLa/wCfNczq6JtFX1sUYcb00eXTYaj4aro+GRzT4bS9V2eqDHWHi0D8U+P0cniwwPCopqBrm3Dg4tLe8Db7vgpkuEOIBilc0+JVXgk1dDS5iy7S53/UVPbjL2OAljcF1SXTjys2uYKGpZAQZTeyjz0NaYzlmN09T41E5moKFRjMEbCTdNHVN4ZRVjL55SUqvpawusyQpqDiWnNwL3CRU8S04cLk+5LZ6hyWCqjpBnff2qkoZPyt+axsVZ1eNwzUtgSs16dllc5rraplpopsQfSyAsPuQHEE5PrFVlB1le4m5dY2U52HStfbKgjlRjc8kJBJ1VG90kudxK0UmEPFJnIOyzTpDHLJGXjTRJSE0Sgyk7ZCuQ7zVmv9efiuzSPb1E2oNoyuMNv1lUe+c/FRmvB2jAf6Kp/sBWF9SoOBi2GU/wBgKd3hKKBIkI6p/wBkpZTcx+Zk+yUCOY1RvUyn9MqvqtayAKfUfn5NL9oqBUm9dBc6WWFdK1pgeonIBXROFA4cPMsO9c8pv5tPddI4X7PDkWifHO0Z+LDDzIGElqec59yQxDD3B0Z0UyONtzcBbudTOnqMx7CCtzAy+jQgnoOQdG7C/wBPaDuuoYPSmOnJJ2XNei+3XYgF0qhmOQsB3CWPhcnqFjLnODmhyzhEjSQHFaPFXdUC4jMs+6oa5zrNAKtMk0l4TSvrpi3V1tLLXwcNERjsW0We4XqmRVH0W66lbb5Yj260Ln5MrK6uLDcUsnDGd/qlTaXCHwNAANhpZT/leDnIFLgqY548zHgqJy1peKGoadzI7BvvRSQOLD2LexOGtsbXTjagFhc52iPuj4iNh8T4WPFyLnRQZYqt1dnDjkUx+L0zHEdYE2cWpze0gTnLR/FFjSyuaAEmQOE+bSyrGYpFmvnTjsWhvq9Rva/nXS5lncIyQOSo8RnqZ25WFOuxOPq/XTBr4XNvdTFe9M7U4JXSzGTNbyV/hz6qmpgxzrlI+V6fNlLwl/KMJbo7RXbv9Jxx1dyrGhmmfIc5uEdZhcUxzuYLqJTYjEdQ7ZOy4vGzd6Uy0Msd30n5KjNuwNFNhpGRx5SzyTVPXNmjzh2iT8oAm2ZOZ2JvHEeowtkji4sRQYTEAezupj6trYc5cqx/EEEbiDIAn90fxw0/BWCpzhmqtKaijjYOzsoAx2CQgCQXTsuLNipy8P5KbnVTjiFxjDCaBxaBcDdc3oHHqnAm+q0fEOLy1cLmgkN5rMQkRxkt3unj4WXq/wAPnig/OWHitHhtfBURPERBssfTU3pzcpNlpMAwhlBDIAb31W2HjDk9ZbiA5cRJtonMFn/Km2SOIRfED5IsEa4VYOtlZRv6eZzoxa6bqHysOYtNrbqRhLA4xh1stxe6vMbjiFBI2zdG6Ll5eb4ykdfDwfcuW/HKuKZy9wBPNRaV3zTD4J/iKnfI4OzBQ6c2jaL7Lo9jnk1VlI0GLQpnCpZqXEWZWZgXbJwTN6nVS+F2x1ONRBwBbdRnNy7bcfLlhlMsfW1qaGWbDHy5ct26Cy5pURPhrCxwsQ5ehammgjwcizQMi4LjLmvxiXKLAPIWHB1dRv8AmZZcms8lvhLYzlz7K4e2kA+iss+d8EQLDZQ5sSny+suvW3nXLVaWokpQ6wDfBXuAyMMJLQLLlb8QkfKLkroPCMxkoillOjwy3VnW18ETiCRdMw1UU7HWIssvxC6U1ZDXkBTcCY8Uzi5xJsps1FTLd0RWUsNRUuFm3upuFUMUD7AALM4hiZpq17e1pzVngWKGpe7Um3ejV0JZtpJ4KYm5slUD4WlwYQs9iddK2bIL6qRgZku4vJ70auj3NncWMRmNwExg0cRqHFtlX8QTEzENOqVwv1pqXXdcKp4m/wCTWPmiiIDrBNGqheS1uW6pMflmbI0MJsoWEsqHyvc5xIU6/Z/U3oxjLc1baw3WJ6QGFuO4IDtdazGpzHiLWk2usp0gPD8cwPXmq/SNdupxC1M37A+CyPG189Ny3WtYfyZv2R8FkuNvWph4FRl4vH1mHHTdFWk/JrNbjMg7vR1xJwtgOwcsWhqgA6yHXW6scOF8dbc/TOygYaLzQc9Qpmc0+Ll+mj08fRfHT+HndtzbqznpHOlvbZZnhOsdLI5x71aVnEkdNVthc4AuNl16clkXZvHAfALB49iMsdUWi63bJmz0pd3hZHGKWGSe7jqmKe4YrXzQEPvd2ibmd1biRyKkYNTsZEQw+FwsBj0XEPDdQ5sL5J6Z7jlcBmBHlyK4PzOK5ar1f/i8p3jvtrn1Z2vYoF/WsN9xyXOxxTjRGZ1PELHQk2JWzwioqqigimq4mRzlt3tabi3IrzcsLHr2WepHPKTYlMTtDQbbopKm0lhpZInku0m+hSiUCoIbe3NVVZKG89lNq5gAVQ11RruU5GeVRaqa7j3qA95JtdHLKXvOqTHGZHc1UZVNoIi8k+CbxKlzM1F+0Lq0w6nDWXt703WxXDhbmlvs9dKAwtibtrfVNvgJHdfdWT4ASNNtSmamPKzusrmSPln8SyQRkgarOkl77ncq0xqozzdWDsbnwVaQV3cM1HBzXd6dp4Qrqfi3hyMz5XV1HaKUBuo07L9O8D3gpNRwxhtTI70ikppHOPr5MpsuccG8Rz8NYxFVx3dEexPHt1jDuPxHiuzVVTSVlPHPRlkkUgD2vaeS6JNsN6U1LwvhlC0tp2NjDiOy0XJ8zv7Ff0eGmmlJYAH5bMF9ieXuN1VRBrSXOvodFbUtdBhtNPXVbnZI22a3cvceQHeTpZFmlTLbNSRh+M4rM8/MwUzGAHvyk/8AlbbBJn0eCxFzbksAPtAsszUYVLR4DO+oYxtdWyZni/qveQA0eTVtcHp434cyKQ3Fgb+I2RhOy5L0k4VWQ08EcBcDlHNTiKaYg2Y66iuwSnl9U2cAoEuGVcLvmZSQD3rpjjy21ENBTFgIaEqbDaaRmrQoNC2tEQDiShWvr44yW38kVM1/o5FgVHqcgRTYBRPcCWKPQT1722cClVUmIg9kOS7PcFiGF00VNZrbaLIvpoxM4dxWhrJK/qfnA5U0dPJIXOIKpLT8FwU/Vkm3rLYejUZd9G/ksDw7TVjXO6sHLdX3V4kJOdlnWuPU8X9fHTMpCBbZcxr6VhrpXNBtdbSpZW+j9rayzzmsD3ZmjNfVGJZVRVFN1dLUPDderK4o3efxnPxXe8ZLW4bUFoA+bK4JGb5/Go/FTmrCO2YOAMNg+wFM5lRMKFsPg+wFKG6IYzfdNVBtBL9kp0pmq0p5fslAnrmM355555ioFRrXw+Sny/nH/aKgzWOIxfZWFdK0gB9Fmtrr3rofDkpZgMLbjZc8g/mstu9dDwKINwKBx+qqw9Rn4u6OTLDfRGytF3doJumcw04FkxG1mY3C2n/XPT/p5+sEEzZlzayCrZOe9FTA+uxEX0DVs21Xos9rrF9Erv5ZxFn6H4rW4xTyMnzNGltlnhl+mvJhubSahwq2Eh2/K6o5aIh5AcAmn4lJThzQxxUF2LyFxPVOK0Y6/TQYbD6ORr7ldUj+smDTfVZXC8UfO8NdGRyutTQHK4ODb2XPy+u3hn9FjidOIYmkAqw4blD6a7vEaqurqozQhpY7RS8Gv6NZo17ln+1a/qsJamBriOzug6rjdSHKAfJVHos0sziWO3U2GldHAQWlXayxll7ZuKR888hLfpEKfHT6EliDIBC9xynU3UgTgsIylTvppZ/ZAjdeoDMpU2qjbG1pybqGwuE+YNKkVE8j2gZDoljVZzdibSQNqGEFuybxOFtDTlwZyTVJWywjRqaxOtlq4+ryGxVSzSbLtjKvGzHO6191pMIq21FCHOtmIvdVU/D7pLuyBSqCCakiLMuyu2aTrtd4bLG3Nmbe5TuJSxCMljbKvpnlrNk88GVtnNvdRLNCy7XfD7mz0YJCmR07DIbtCrsJD4abKwJ0zVAvZjt0Yw8vUzE2MbRkAclznE5XMdoFu6qWR1LZwOyzT6JsxNy2yP2ev6qygc57Q4tIVm6dz2BngnYYGQNtdpTbixhzcgFGV7a8fipxKLq6JxcbLN0TnS5+660OM1ImpiwFZ+iBiJbbnurx/wAWd9WsE0lKwFgzeC0vD1ZPVxOdIwsG2qo8OMZeOs28VrMOkgbA4MAutMPGPJ6x3EQDcQVrglJGWNdYEqk4hc9+JaXNuascErXMyxuNlpZ0mVsKSRsTd0qsrDUtyZnEdyj0bBKzcJTG5JS1w8lz5479dGGemS4lmEbg0hUsEgy6laDiqic94cGrPClm5NK1x8ZZXsc9R9FpWl4Owyf0iOrI0BuBzKzkdBK94zBdWwGk9HpoiG3AYNvJYfkclxmo9P8A+M/F4+a5XO+NFXSSvwvq+ssS3ZcYr4j8pSAntZzc+1dDxzidtLCWZX5m6DxXOTM6orC93rOdcqPx8bLtP52eN1jP0uIsHfUwjW3NMzcPSEEK1jrxR0rXHuVfVcTRtXZ28rKTfaqk4ZeHA35ra8M0JpqXIe5ZCTiplwMpWt4cxUVtMXgWFkstnhraPi2DGefOCU9h9A6npi23JQ8V4phpKowucLqdhWKtroC5tlNt0qSbZHGsOc6rebJ7hqke2Yg6C6sMVqYhUEOslYLKwykjkq30nX9llNgpmkD+Sl01CKdpAAVdiHEzKGTI4pzCcdbiJdYqe9K1NqzFqUvqD2bqTw9Tlk5u2yTidQ2OoN0rB61r5yBdV+ka/ss8Qw30mQOshT4b1DDYDVRq/iGOklDXEglCl4jjqnFguUt9K+ZvbO47hj5sRDhpYrF9IcHUcQYGw8z+K3+K4k1lbYjdYHpHlMvEmBnXdP8ARft1CO4p2/ZHwWS42vmpfIrWxn8nb9kfBZPjUdumPmoy8Vj6y7girbDDWag9pKeRbZJr2gYYw8y5YtCcNt18FzbUKaI+uxfqxrd51ChYeAZoB3kc1Np5CzGQ7ucdk56L433ClEYS4JnFsAkqMSZML9k3VhwrN1mZx2VpV4nBDPkdluV1OYUeenoLHcBc/wAdr5/TcmuVdHkkbNTEjYhY/EsPZJUZtFSbQ4erZBTnMT7VXcXVk81LkpyXWJDwDyPNXFHRhkBAVRV4fMZ3Oa4hRy4/WOmn43L/ABZzNlcJw57p2yTsLQDoDzWuinETWg7DRO02EF9OZnAAttewTEtNlIBBAuvF58LhdV9Dx/kfzT6iPVjLIXD1Sok09wQDZWFSGti15KkrJg26xjSoVdOQN7LP1UxLjrzU6uqi4nVVTgXvvZWypLWXKs6GjLiDbRR6eG7gLeC0WGUwsNErUydlQ04YwDwUWqi35q6kiDGGw9irZ47mw2KmVpYqXRi1/uVPj1U2ipHP+ls3xK0MsdgVzzibEfTK90cbrxQktFtieZW/Dj9ZMOfKY4qZznPeXOJJJuT3oe1GAg4WXpSPLKicL2vsui9H2LySk4Y+7mOBdGLeqdz7CucsGt7rTcI427BMQZVtYyTQsc1w3B38j4p43VKul1AlD7Bo9psFNwWgbPXMq62XrDASY2fRjPeB3+JUdlVBi8LKmlJLHcju09xVzhOAV0wzRrf532z+9dCxCT5SxVoABgpAXk23kIsPcNfar6lp5H0rDEQNNu5UtVh9Rh8nVyNyh3cptJi3ooa14JaiY9pzymksz19LKbtLmg8lc4PUNq/XY4a22UekxakqRYubc96u8LbCW3aAdVWV6ZyH42NiNr/cnJKXr4//AAnQ0OkAtzVm0RwxgusFhc9NMePbPspTCbAJmpkEPadstI0wTHs2KiYpQRSxbNF0Tk7O8f8ApmsSqInUmYOFllhXNY5wBGpWoxLDY2UuUOWOqKHLI6zxuuieOe/9bPhjFqeOIBzm371dnH6PP67VkOHcD9LhuXkKxdwe3rL9Y7yul0uW6XdZjVNPTEMcCsNVGd073NJsTotC/h4UkRJe4+1Vz5IGBzTa4SiMrf2osVe84ZUh7r2jK4jTm7Rcbz/iu546Y/kyqc3+yK4ZSaiMd8/4qc2mHjuGGi1BCP0ApA33TGHaUcI/QCkcygw8ExWfzWb7JT9lHrv5nN9koEczeO27zKhSf0lGP0VOf6zvMqA/XEm/ZXO6FtEQKN+n0l0fBA04DAC7XKucRgeguObXNst9hbJBgkAb3K+P1HJ4vKaJvU+um/Rrg2dZJoxK2EZk/ETlJJWzFFbTOH0igpQeO8jyQTDlfRVMY+IMSBNuwd/NdRnhZUwF5tey5J0fOMOP4l9h3xW5p8beY3M1WUjpwzk6qFWljJ3NNrhQcsbidlJcx1XMXFNmieMwGq3x8cnJdZdLHDqOPRwHJX+FM6+YtG4VfhmEVU0YyiwsFfYRg9RS1LnPGh2XPnN5OrDLWIVzWwuDDoSFPwFwbCb96j12E1NVWtcNGhWkOHvgpzZtkrj2eOW8SDiVJG9wc4XvqLpxlfDNA4sPOwWSrMFrZMRc8XyE96ktjqaFmXXU7K7j0zxyTJ2ntubdVUNUXOeBm0K0FIzPS2ee0RqVC+TWRRyv7zdTMNn9Xaugq2vmy5jc7qVLI3MAH7qghkccVcwGwvZXYoXOna4vSxxXnn3EylpesOjil1NH1BuSdBfVTsMEcT7OIKPHpY+rJZa4HJLRXK7Z6proowAHbplk7XNda6qnddNP6hsDzV5R0L5IjoAbbp2HOqfw6kbURF7nW8VLdRxsiJD7lV4jq6ZpYxt7eKRTvrJew5ttU5j0m2/TQYRMxsJL9gU9NilLHcF43TVHh720Zb9IrPVvDtbPUPc17rE7Ixmhne2iqqlktEXs1GW6yMlW5uY5SthheEyNoBHIbkC2qgT8Llzzl2S12f10z0cz3m5aQLJU2bIdOS0DOGHN5pX8XSwEvNxuoznbTiz67YiqppDAXZSquhhfIXXGxst5itNDDCRpcrPU9M1rnWGl08fEZXszFRPmOVugHNaTA8LNPA7M4knvUBoEDM9rq0wWvNS1wDCANFeNZ591SYrRg1RO/eozqf0duYHW11eYlBecuOwVNXODwWttcKt1GS94cq+vFjuFZ1Vo5Q7vWd4ZJY8q8qrvcEqrju4ZxCBlRHcqq9HiYLWCtah1oSPBRKCmM1YzMLt1NjzKVy1NtMcPvOYoIjZn0HNb7CiGYe0ZtA3RZ+twkyBjwLPvb2K5gZJFRhttQ2y58r9yV3Y4f/XyuNrK8T1DHylgWcpoy6cENJF1fYnQvknc5yVhtDG0gkC63x6jgyv1kj1bHPp8oadlnaqmeHG7SujtpqcABzQmajDKN+uRq0mTPPHtzaKmzzNblK6FwxQOgpCLWuE3FhlGyYENGi0+GtgbHZtrIzyHHj3tzvHMAfLiBkLSQeausAoH0lKQQbWWqqYaVzrutdNsFOyM5bJb6XMe9ueY01zq1xAN1L4fY7O4FTcWbA6pNrFLwVrHTENCe+kSf22rcaw4TVFy0lP4BSGmzWaQtrHgVPUgOeNVGrMLjo79W1PXRW/22ylezrKg31TuEQhkpNtUKyWNtQ4HQp/CiZpyI23Rop3krMdpDLVtsLpeHYf6M4uIsVbV8IZUtzsNx4INY0Xvp5qG2u2axMB2INzDRZDpGyjiDArDmFt65rDWG9liekYA8R4FbvHxVa6ZW9umxn8mH2R8Fk+NNX03kVrW6U4+yPgshxmfnKbyKzy8aY+s08CyTXW+TYwPrJTtkVff5Mj10zFZNAwwDr4NxqFLpgZMaI0HbKi4YbTweYUmml6rGi7kHFPH/IZeOi8NMMYIScTwyWeuD9bJvhas655Pir+eugZIGutmXXI5L2aYx0NGQdwFjMUxQQ1WVxK3c7mSUzi3mFgsYw9ktXmKqJsWVDiDXQXOybkxSDOb20TVFh94C1hOipaugmjqH6m10b0UbfBZo6ynkY21nN081U4gB1hLeW4T3CsMscYvfZKxLDqued5giLieQXD+Zw3P+2L0vwfyJh/XJnsQnDYjc62WUr60Zi0Faur4dxqr7EVBMTtc2A+Kj0/RpiMrg+unjhF/VZ2nfuXFh+Nlf07uT8rCfti+rfUvADSXO0AA1KkDCponhssb2kbhwII966zw7wpS4S8GCnAeN5X6vPt5exWWP0FJiNL1NRGM7fUk+k0/uW9/E1j725J+bLl/xyGnoxnADVe02HiWAszvZexzM0IsbpyTDDTykFvqlWlJT2YBa3NcGcsr0sLLNoFTFvZVk8YvoFoKpgB5KqniLQ7moaVkOK8SGF4bI5p+ek+bj8zz9gXNLLQ8b4l6bi7qdjrxU3zY8XfSP4exUDRdep+Ph84vJ/I5PrIANrJLgnCLpuRxvlZq74LdzivrlaLu8FJpao0xs+MOB3BCaiYIhfcncqQ0GUWtfw3QGv4R4jGGVkcrM0sVwJYHHVzfDxXprhiow+ooIaqneySGZgcxw5j968fU4bCbjMx4NwRqCutdE/FzmvODVEoayY5oLnaTu9vxWmOX6Rljvt1PjeOOSLNCAXDayz2G0balgEjdSreo6x4cZCTpzWfZXS0lU7L6t9lrjWGcSqrAHRy5oSR4K94aFRCA2VxIuq+DHY5BZ+6vcEkjqDdhCM/Cxna8gcHStSOJqiWDDyYG3cBsjZGWTNKnzQtqYw14uFzX10zuMrwvX1crPn2FpvtdaLEaoR09+dkoYdFBGTG0BUGMVEvWNibrm0S9o8imxTGJHMLcul7LNy1ZJIy63W0l4dfU043vuq7+JUpc7UldeOU048pdl8NYuIILFugVrHxK0zWy281DpOE5YAbF2qQ7hmZ8tw5wT6o/sn4ljjJaY2GqxkzpHue6x3WpdwvUZQC9xSBwu8DUolkFlrHYi53yRVF1x82VxyhF3QeM/wCK7vxfhbsOwOqfyyHdcIw03lph3zfioza4eO50ItSRfYHwTw3KbpBali+yE59JIxlRMRI9BnP6JUsqFipth8527BRRHODbMfNQDrigH6KnblQt8U/wrndC1jA9CPeXarouHSFmD0wA+iudMNqEXG710iibbBqb7AWnGjPxLEhdALA2SGPe2ImxT9G0mIXspBYA21lsw2pmVEttnboK1ZAwDZBPpG3JeB2j+MeJDT1XfFaRjGtLvasrwk4xcUYg39F/xWsgYZGnXdZY3p0ydtPwnww3EYBJJchyt6jhGKkLnBpuNk3wnjAw+lEbiLjvVlVY+2rzhqr6L+Pd2rqDE6ajkLJCGlumqmv4mpM3ZeNVi8TLhVOcNzqoEMoFQ2+19llLbk2zxmOO3SBjsDQHuIA8Uv8AjBTvbbMPJZarymlBG6iU9S2OUZyAErb9aVMZ87a819OH5s4JVTieKxdcxm9+5NGsgcBq26rsScwvY4EE3WjHGytJSkyxtLTlHcrSOkz0zi6xVNhczXQsAK0EbvyN1kXwp6xU1JHFXOc217lInxCWKQBo0HNNySmPEpM7jq4pmuqGuI5C+4S2rW+6kvxiaMhwTb8bdNIBJcpoxNfEXajTdQ4qR8sgeGnIDups0qataGjp2SXeW762S310dIDdpspFGYBAG5u1ZUmMZmh5ab9yCxu7pe4fXwVYd2D7Ucc0Uc/qWbzWOw7FJadxYCdFOhrp5S4kGxT/AEV/y027cTp4ovW3RQYrDUvytF1jmuqJ2luawCvOHYyyYF4v4qJarPqLipxhlGO1cBJpsbZUjsNJVfxIQR2RZI4ayAAPbqHJ770X/rtcvxQRjtNNkzPirZIuyixh8TIbtFlQNlc8WGyWd0ri7M4m90jXO8VWU7HEE+KtqhloHFyrYZmguAPNPHxPJ6sKaES2Dtlc4ZRwx3y2VRROL3AK+o4eqBddVGdqp4iLKaMm4uszCwzPLjzVrxZJJM4Bu3Mqsw5jmjUqv0yt7aLBKJrGhys5YG5rlVNDWOjAapktS8tupbYeFPhY7QoRxsiIIsLKqnrpI3jzRzVbywEHVKn99tRSSNmIzOzEd6nSOYGWuqHhlj6zMS6wbupeLyOonBua4I0WW5Lpt/a4/dNuwtuI1JZmLWgXcQq3E8O+S548jyY37X3CcpsZfSTGQNLwRYi6gYxjD8QljIZkjZsCdbrK3P8Aln+mn1w/wX//AEsJc3UB7XbBVs9XLlPbKsaRhqaYNJTM2EkA6rux8cOW6om1lQ2YDOVqsCqJXRG7rkqnOCOMgObRaTBKFsTQCU7oYSyoOIMqhctKg0EtU8ua8k2W4kwcTRXsdVHh4cZG64YdVnVy9sazDjLUky3Kt8PwyKnfmNldVeAsY3rLEHzVVJSvjJDS66rGFllFnFWMjNg7RQq7E4XuLMwufFUVbLNTFwL+SytVW1Elex4e/K3ey13Iz9bCXh4V8hmzG3glYZFHhNSWSHsnmUxhOOySgRMDibaqvx8Vjpw4B+U6lLcptY2ooqmua3MwnzUrF8IY+nEkdrjmFyWvqKuhljnjMjSDddRwHGmYhhLDKbkt1BU5RWOXbB4qDBWEb6rFdIZvj2AnnmHxXRcWw01Ne4x6tBWA6Taf0fH8AB+sPilPCv8Ak6Q0g0zfshZLjL85T+S1bP5u37IWT4yPzlPtsVGXjTH1m3bJFcT8mx6G2Y+SW46aJOI/0XEb/SWLQnDj8/B5jVSqcZ8XI3u4qLhus0GttVLoGl2OWP1iqnpZeN5wrTlmfTmmsVbUfKDS1xDbqy4eDW300UysNKZRmAzLqclhDJS2hNzyWCxrFnx1hbfRb6cB1M7La1lgMbwsTVJcqC54axETREvO6k4g6n60kkXVJhNG+miIaVCrJKs1Dxc7o3opHQMAfEWty2sFetlo2O7RAKyPCrZTSku3VdjdXiMdY5sV8oCZS6dGhmo3HSxRyvpAdguf8PV1e/8APZhrzVpWT1BOjzZRZD+2ljmprnLZYfpD4pbhFM2KlLfTaglsV/oAes8+AH32VthplIkfK/K1oJJOwA5ri/EWMOxvFqnECT1bz1cAP0YgdP2jc+1Telcc+l/wljAnnfh0zy7Pd8Bebkn6QPnv71taWK7LlcLlxaXDqkVsJ7VKRIz7V9Au54XVR4jh9PWU5vFUxNmZ5EXXlfl8eruPa/Ez3PkzVM7R18VnOJcRbguD1NYdXsbZg73nQfv9i0tS03N+/bwXK+lPFs9RT4VG64iHXS2+sdGj3a+1c3Fh9ZadPLn842ufSOc+QvccznG5J5lKaARoiITjRovWjx6RI4RtvuTsEljcoJJu46lG35x/WH1Ro3z5lLy6oBsbp+EajR1vBJaA02FinWAuO5smFhThjxZ7yR+nuParCkp5KSdk9NIQ5hzAtOoIO6qIoW3BD3fsqypZsgDXHNbS4OoVB3vg3iaPinCb1BaK+AATgC2ccnjz5+Ks5cCimBfYLiOB41V4HiEVdTOLsvrNB0e3mCu1YTj0OJ0EVXTuvHIL2J1aeYPiFOWVl6L4l9V9VgphDiy6u+Do3xiz76FNyv69hsbFWeAQOjjJ5qpyXKarP+OStC3KZQFKvawuqmkmPpRB5KVNVBsgF1GUXEyX1NVn6qFpqQ823UzE610cXY10WVxfGZYI84BuEsfVWN7RdSYBexTxZCOQK5fS8aVDIh2XaKZTcYz1Dj827RdHywtdGAgy62TLBAHjQWXO6njKohlDMrlMrOJJ4qUzC97C3irmFRc46CWwG3qpp7ILfRXNafjOrkZeztE3JxrVA2yuR8UfcW/SiI2cMVRba+UrzLhWtRRj++/Fds4px2bFOH6tsgIa1q4pg4/LaMf3qnKaVLt3Wm/m8f2R8EoblFB+YYP0QlWQVE5QsXFsNqPsqad7qDjOmGzn9FFE9c5OhUJlzibvBqmqHDrib7/VWDoi2F/Q2faXSqWRrcJpgfqBc1t+RR92ZdDhscOph+gFfEz5PFtTyN6sWsjkqWsjvomqRg6saJU8LHRG9lswMtxJpGhQTUVJFl2CCZbcu4TAdxfiA/Rf8VqmzdSCLLKcKnJxnWj9B60MswJIWM8dePq5w6Z0w3Ku6EWus9hDwCMx3WioXtJOwWf/ALOmyfKuxBv5Qb9yjspbva5rM3ipOKgCW9+SXSljI2ucdBvqlP8ALpOevjs9NJeHKdCq+WIyEBo1Uuqkjy9ki/cClUNOKqYMuUXf0Us+UZsUjCLtCTUnM9rNLrXUvBdRXAPyuY0feoWLcIPpCXhjhbW61+bWEzm+hYXaKNocQtPTvY+jN3Bc4dV1EMhizHs6KZTYxVNZ1eZ2qrXTP67P1tB6RWyAfWOoUim4fbUNIeSFNwKnMhJkJJPa1TeL4mcKqAWtNjyS3pr7D54fayLIZDtZP0OBwCHJmvZZ2q4wJGgIuocPGkzZOyzRH1C+a0nyEWVQtKSzuUubhmGojykn3rMu4ymJuGBPs40qDplHml9Q/ixeUvA9EDd2p77qWeE6GCMmx96zf8dKpp0aEh/GdW9pBAR9TRfFtT6psFE4xsCdw2paLkaFZoVVRiM93E2J3WuwWhb1YzD2rPe70q9eomJTCbc3TNBM6N5DCp+MUGUEsCzlRiDsPOoOiJLsbny0FQ2SoZlLkIaRkMV3EKhp8fdNo0EKRNXzSR2F7JZL4510XiMuaNzWmwVNRwkuJzX1TVbVysYQSoNNiEjXH9yrGdMuSXbW03zdiDqp8dZI97Y+9ZaixKR8oabq/pnEEPKEyJ9fhbaiLxIVO/DvRiQFpaV5ljBPcq7ERdxACJVZ4TW1fSQ3de6sJmZYtFGpgGndP1EnzapnjdRVSx53+SU6EllkWbt96ksN2qUz1bcJuNN1jXNNncwEviMuqHNyg2ap/Dhj6kWAvzUnGWxZDo3ULH/2d9lvFrbDlhsRYpsxF3JTJXsbIdRZCnyyS2WsxcGyqOqNM2zgn34n4FJq6dwaCxhPkksoZHMuW2W0K2w3LimXUNVxgeIGV8QtuVSSYbLJeyn4dDJSZHn6JT0mZ102nyinbsnBkPcseMem6nLGC63gnIcenG7Xe5Q1+lrxBXR0cJJIAWXpa6Oqm9cG5VdxdU4hiEWWEOCzOEw4tS1AfIC5t9rK50wzttbHivDstE6WMa2usbRMBBzWut/XzPnwuzmnVnNYuKjvc2tqss8nTx4SnqOvjw+a5sAeal1mN09UwAOFwqWroXZtAUwKCQ20Smdka3CHa8NqgGgggJVBXS4e3qw4gdyXSUDmuu4J2ooQTcNRc6XxEyixBsr7ndc+6WZhJxJgNuTwVq2SGB5vcarEdJj+t4hwI3vd4+K0ncZZTt02P+bt1+iFlOMfztOPBa1g/J2/ZCyXGP56n8ksvDw9ZpyRiOb5NivtmKXIdE3iJPyZCP0isWoYcM08A317lZYXHfHbW+kVW4afyiDS+qnUkvU4s597HMU8f8iy8dFwcZQ+xVZiPXuxBuVzg26d4ZqTNmLjcXVnN6MZxcjMuyOSlAObQ6725rE4zWSR1BA2W/mjHopsdLLD4xTMdOdUUWDwmr6yI3TpZA+W5dzUKip3MjJYoMstSyZ1u9TvRR0jh2KPqgBtZWUuF0z35nEXPgs/wlPI6mBde4CVieLzQzljQbBPY2vYsNpYj2SEqWmpyNS1ZalxuokF3A7pisx6djrAOS2COkvFmYNw4aSB+WbEH9Tdu4jAu8+6w/xLilfU5IxawJ2A5LVdI+NOrcTpoS8nqYAC3uLjc/h7liSx+IV8dPFvzJ2A5lZ5ZOjjnSvxQuho2MJ7UpLz5DQfiuvdDGJuxDg8U7jd9BUOh1+o7tN+LvcuP49K19W9rDdrey3yC610B0EkeBYpUPack1QzJ45QRf3n7lyfkauPbs/G3M2xxFzIWyTSuyxxtL3u7gBc/cvO2NYm/F8Uqq99wZ5C8DubyHusu09LmJ/JXDUkDTlmr39Q22+Xdx92ntXCw3Tw7lj+Lx63k1/Lz3ZiAAISZ3GzYmntv0HgnWtDWl7tA3dFQx9a51S4aHRg8F1uM42NrWhrdm6IOFk68BqadtuLBMzet+5OQlxd2Wk252TL5ANG+9NGRx5n3oJcRlpsMrmX31Twid60bswPLmqJkz2G7XuFvFTqXFSxwEuo+sBqmFzT1bqfe+U7gracH8RNw2pDTJ+RzkB/6DuTv3rDtkjqmXBvfYhOUU5ppbPJLHGxF9vFGylegI6lzLXsR3hXeF4vHE2xIC59wXjXyjhppJnXnpbN1+kzkfwV87QGxTka3HcbSkr4nzZrhQ8TxK0wLDzWXjqpYHZw4lOR1ElQ8FyWULHDtoHYh6QLFV1dGydmUpULeyolY2QEkErntdWPDKR6FTRx8tEqhgiEpDbaqE8zEW1SqMvjfqSqw5Lscn400tp8IjqXhwsFJrsGdLSCPMLKLFWuiOtynzixLbZXWXVjzacN/Fv6Kw3BWU8T8xaSfBUmI0IbUk6WJVs/E9NC4KvmmEh5m6d54mfiZKniWFkXDNW5lrlq41gfaxCiH94uvcVuycP1gF7ZTouQ8PgnE6H9Yl9fXacsPi6d1i0ib5BHY6oR/m2+QR73t3qmYiq/HOzhc5vyVgVXY9phU9+5F8OeuedyhQH+U5LnkpwUKmF8Rm8lg3i4sfRYR+kugxxE0UFnWswLnw0hgHe73LoQcG0kIuL5Aq46nKbibTzNjjAcbpb5RKzKDZU0szhsVIgms0XctbdMflNZTOy7+9BBlW0N1Iugl/IXw5Nw9pxzVi27XrUPgbm9qz/CNG+v6SJKaP1pM4C6zJ0YV7AZDUMsP0Up4232xtOTG4AclYQ1j47lPzYK7DqnLK69vBHUxQNhu0+amRtc/wBI0tT1w7W6lvpRPR3bobJvCMPgxAvMj3BrTyVhWGnwwZMxLeV0pNXYyss0pm0ssLLuN1qOBqUTV2aUXA2VDUYjBJHZpBWh4NnaXEtJBv7ka72VusdOu0r4I4mjTZV+NNgnhc2zdQqjr5frlE57nDVxWjnZiThyOetLgwWJ7kiuwiKke0BoC1MbQH3CzuLVRfiDIvFK5aPHHZsv9FaCzQ2VRXH0ioHW2NzbVWOKStjYzz5Kukjjkc2R5tqidqy6h7FMBhFC5zYWgtbe9lzl7Hx1bmBrrB2mi6vHJHPCInyl2movyTDsDpHuzNibZVcUzOxzxkMztRG4nyTjQ+LVzS3zC6TS4VTts0RtCgcRYMx9O8RRjMBpZRcF48rCmobfdTsMonYhJoOymafhivmmF2ENutrheBPoYm5Wa2UfJ3P/AEYpsKZT2AGquqWORgAbzRxUUrnXyaq2pKPKza55p+MpblVfVj5qz9Ss7W4RFUkl7D7Fqa+Gw0371XCNxHclvbSzUU1JgcERuGlTDQxNZ6oVh1Lgy4smHscW6hTkrjvShrcMicCbKoZQRB5AAOq1NVTO6kmxuqSKmf1p05q8fGXJex0lBGHg2VqGWs0BMU8EmbY2U9sTwASEUscllRtZHDqdbKrrXgyEhOvlkyhrUxLTvew96JNNMstxAinzTBo18FKqwRHsk4Xhr+uLnbqyqqAvcweKdYY9qg4TVNh64gWtfLfWyfoWNlZZa+ahhdRkgHMGLN0WGmN2h5rLDK310cnHjjr5S6NvowNnWUTEat0nZBOvirN9C7JoSojsLJNyblVPdoyt1qM/JTPkOl1LoqYxOZcndWrMPLZBfZLloLvYG94VsdaX1Lhcb6MSFo2WexKuipnPjaQbaLawtEeGAforneI0Lqirkcy9i4o3pWZdBiLHusQN1Nnmj6o2VfHhD4WB+twie2Rwyi6vG7ZW6azh+kiqKbO4XurR2HQ8gFWcPv8AR8PF97Kyo6r0nbkVNnbXGzRD8MheNWgpl+G0zD6o9ytC02VZXMk6xtjzSPwWK0rG4ebAbLBZbXsuh4gxzsOtfksQaF7ibHmpzi8ckTIHb6oxGwclLbQORnDyOajS/pFDWgGwTbwFO9BcOaT6A4o0X0qKmhbJqOa5z0kwuix/Ahyzj4rrklA8NuuadKcJZjmBk79Y34rbHxFu637QeoH2Qsjxl+fp/IrYC5px9kfBY7jM/PwfZRl4ePrNv1um8SJGGw6m2Ypb9QU3iZvh0I09buWLUML/AJzBe26kAh2JuA+sVGw02qICT7U/G8NxVzyLDOU8f8ivjdcKwlsTreKiYg+rZiseS+S+qn8IztkabcyVZ1ENO6cFxF+5dblH6S5uHkuJvZc4x7FZBWuY0ro1cwCkc1pFrLm+M4a+WtLmhO0Lvh+YT095CpU1HC+Qm43VPhsNRTQ2A2TMtfNG92Zrt+9Rv/ZadF4dgYyPK3ZWEuDRTPzGxWc4Xrz6MXm+yFbxcaapLCTotP0lom4FCz1bKBXYLCwOleQGMBc6/cNSoGH8VmseRcqr484odRcM4k5jyJHwmJp7i7s/ioqo4li+JuxHEauucR87I5w8r6fdZDCHmGlqKo6E6A/581WzuyQAbKXI40uDxMJ7T+2fbqsHVFJWPL5nHc3969U9HnDrcD4Uo6UsLXhjMwP1rXP3krzNwxh5xnijDKAC/X1UbT5Zrn7gvYFLJDTYcaiU5YYw+Vx7mC5P3BcnPd9Oz8aa3XnrpvxMVfFgw+Mgx0EIYQP7R3ad92ULnsUeZW3EWISYzjNZiMnr1Uz5iO65uB8FGpohFE+aQaN2HeVvhjrHTDky+srVdWtdJJHRx+s86lWjImxRhjRZrRYKHhbDPUzVbuXYb581OqT1Y1OgGpVIQ5n2O2nxUOaQknUI55i4nXRRycx8EAL3KBRgIE680ESiujRFASaGtdTPsTeM7t/FXYeHszNNwdQVm7+wqxwuqJPUPN7+qfwTKVtOE8ddhuJQTuccgPVSgc2Hn7N/YuuF401uFwelc1kng7Rdb4bxE4hgELybywfMv8xsfdZEaTLTQ5Q9qkUcYaQqmmrCSQVOp69rX5QUVpjdrpoACPqg9pumo5MzA4J1swaNVzV243UMmlHcocjAyQ2ViJ2G9lBnIMhRjDuW+hssd0s5bW0TdxG27ikdfGfpBUXQ5LWOyjhvcnM7Xm2YFKLAwXOimwTTP8Zdnh2rP6BXJeGxmxWgH6a6zxxIBw3V217BXKeFm5sXoPtrq4/8XmfkX+9dyZ6g8giCNnqjyQHNauagfNVnEGmFznwVoQLKq4j0wmZF8PH1z8FQ6TWvqPJTbBQqK3plQSsK3W5/NwHxWtiq3PjjbqbABZN2rKcDmfxW6w/CZQxjyBqAq4yypqVnZBI5Jtr3BptdW1bQPjhvpsq+mibL6y1naLdRFdUSA7lBS3Ubb6EoJ/KN1kuj2VlL0uQvkIDc7xqvR2L8TUNLAWZg55GwXmXAb/6SwBuXOsV2ODBpZ3Oc+S5vuVniuxHxWB2KyGVvZvsoTMAaYyJXXsFfMwqpacgeAFExLCa5kTjHKAtZE21SxUvyXndDb281V17qmtJc7J4C2y0GHYJV1UZbNJcqdFwaLElxJ807E/VlZbBOH5KqS8mo7lt8HwQYdJ2b96rJmNwMEgkm/elUXFgebOB9a2qlVrY5UG6Kn/jJAG3JCQziWBxNnDRTottBG0HVYbierbS4gxzSM2ZWx4qYwkBZ6vpn4zUiYmwGwU5ReKVDO2siDnW8u5SjTxyQkaXVdBh8sFhnOqtqOhkBsXGyJ0d7QqehkfKWtJAV7TYW9rACfvT9NQshOYnVSOtY11rlLYkR24Yb7p35NDh2jdSBO0DdRa/E20rcx2sjZaSYaCCHXKLpbzECALBZqfiqJ4AY770iDEpal4Id2e9LKyLnHa18TY8tm280p0zGtsCAOZVEcSMMWYmwH3qjxHiORhOV2ncsrlttjxNLW1LHaXACr+tj17QKxtZj1UO1mNioVNjtTI4gP5q8PGXLx3bpTXx9XYkbJr5s31CxJxmqa3WS/gktxypDScyMqXHx1rq6WGNhBcAqZs8GY9oLM1+K11RE4tdeyz8WL1rJCHP1BV4+M+XC7dPiqogfWannVkeX1gucMxWqfaz91a1dTUinJD7dm6LZKMOK2Vq3VkQN8wTsdbE5ujtFzT5Xqy7L1hurbD6qrMZcXp6TMK3UFXHEbhwUl2IROIJIXPH4nVMlsXGwUn5SqC0WcUi1Y6E7GfmCzOMqhYvjtHw5h1PUVXaqKp7XNj5xxX1efP4C6osE+cE+IYk8tw6jb1kxJt1h+jGPEn7rrF8RcQy8T4i+uqD2ZHOblH0W7WHhZGtNJL+3ahVROHZIIOx7wg94azMWmyxXCOKy1OCQGR95YQad9/rM0v7RY+1W1djZigvmFg3W6w5OS43p6n4v/wAfObG5W6WM2IQMF8w0TNLikVRUNYCCbrmVRj9XI5+V+l07guMVEdcxz3m110SddvK5MNZajucN6mEMB0sqfEMLFHeTcblFwxiDqt4JdornGqbrYHWN9E9IyjI1GKQNiLcwuFBgrYZX2DgSdFm+J4quje4Rk6lVeAS1orLyudbxVyMrja69TkRUF9hZSuH5WOjJBG6pDMXYXYO1ypPDdQ+KGznc0q0k02xlZ3qJVSs0OiqpK/UjOmH1mYDtpSKtXtdIz5PLj3LECvgzkZhv3q8xit/kpwa76K5LNWzNkeOscNSoyXhjt0NtfB9YISYhA0auCwdNWzaXkcjqa+YkNEjlO204m4GIwEesEttdARo4LDR1MwbfrCg6rmt+ccEtj+FuH10BZYuC5b0sTNfjOBlpB+dHxVnPXztbpI5ZTj6Vz8VwDMSSZB8VrPHPlNZOqN1pgf0Qsbxp/OKf7K2bP5qPsj4LHca/n6f7KWfh4+sw86JOJH+S4fFyXIbBNYk7+TYftLGthYafyiG5tqpUMBnxRzAN3FRcMv6RDbVW2CNzcQZXd50Tx/yLLxquF4TTROHMEqtxLE6pmKMjaDYu3WjwmFoc8DvSajBGOqutIF11xyldY44fmdrpzWMr69rKogtut7NTAUhYO5Y7EMKBmc4hFCVhk0dRHqLKPX0DHvNrC5SqGAwt02ChVeJGGVwIKXX7LtruGaACAtHcnqzhVlTMXkanwUbhStD4Q6/K6sqjiFsLy2+yr9EZouGWUh0CwXTNEKLCKWnHrVNR7w0X+JC38XEbZPpLl3THinpuIYdFe4hge+3i53/gKMvF4eud01D6W8veD1TDa31j3eSb4gmyvZEOQ1srujjEdO1vJgzHzWTxJ76yuysu58jg1o8SbLHLqOiN50H4Oa3i2Ouc27aaN0g89h+K7F0j438i8AzRtcWzVobSsI7jq4+4FZXocwcYdS1s9tcxiBPcxtviSoXTRi/X4jh2EsfdlJTiV4/Tft7mgftLin9+R33/AMfG5h1PWyM2souL1keRtNB2tbC3MpOMYi+ma2GNuUub63eo2EUjjN6TN2izUX7+S7HCtqKnFLA1hserHaPe47qDiE1zkBvzPmrGpkEFOObj2j+CopX53klFMyTcoEhu6D3tbvumC90r7DZIjjpL7JTWnclJs2MakXSHSl/q6BMFueAkZ0nKeaMNQQ8yXG8scHA6g3ScvkEe1kBo45BJG2QbuF9O/mtx0e4nmqpqFx0qGZwP0m/+Pgub4bPmhMevZNx5FX/DeJHD8XpZ72EcoJ8jofuRL2qOwxxZHFNAEVAIvupAkDjpqO9KZAHSAp1pIvaS/UNVtTUXWwud3Kqp22iAV7h8zWwOGbksuLX122/It+OlfQ0LpZXaaAqLiEHUVBHirygcGyOJNgqnFrvqSQbrXOTXTn4bl9dqDGKowsOXeyoPlSW4FlocSoH1QIGiqP4vSF25CWGtdq5rl9dH8MrHTS6qwxKpMUJI3so9HhppNTuna6nNVHlb3KMtfTXD6+O2W4kq3VHDFa53IWWE4TaTjFBb6y6BxZQmi4UqgeawfCQ/lmg81vrrpwXe7t2tmgCII2jQIC9lSKO2iqeJtMJlVsqjij+iZEr4ePrBAcrKDQ/zqoPipwCh0FjNUHx3WNbxdR2L6MfpD4rrbOqjpY9D6oXI2fn6S31h8V0x8rxTssb9kLTj8Rmk4jNGaU2BvZZqldIxxIbcKdVVJdEWuPJM0+URb8lrGW6b9K1N22QRGEuJNkEyYTCpOp6TI3n65XZoOJooS8WJtuuKwnL0jx/aK35kHXSALn3rx04SWtDNxzEyWwa5Nz8cxSxWym58FjKuTJLchIEmZugvon9U7hjtrKXjAQX0IuVp8Mxp9XFmaCbhcpzuLh57LpnCjR6K2/cj7tRljDldQuxF3abYKIeGIwbgEFabKAiI8UW0tM47h0OaW3ckQ8MiI7ustG51ijBvoluiSKJvD0QdmIJVhT4fHALBgUwokbVrRo0rCQclrJbWlp0CcAQsgiSXu0SRE6+qct4pRJAQDBzNPNQcVp3VMLm+CnOIzb6lIlbdh8kzjmFVSyQ14iDyBfZa/DQ2npmudqB96p8WpSMRD9gCnJa7q4bX8lzZevQwn9dpeJYpbc+QVUGOq5Q52rbJqIPrpbXPircxx0sIvYCyek+1VYzTMipxYWNlV8OwiactI1vopWLVhnZlBNlEwKZtNUF7j7Vpxseaf6aGvoOqZmy8lTNGYlgGt9lb4jikckYa030TGDUgkkdO8X17IV5xjxdelCjbFSEO33KxtfGPSXuGxOi22JyaGJm/PyWSr2WmygKsUchFLfshaCqN6M3N9FSxRuGWw1UjEa10UHVkG5Gqdx3VY3UVDifSQeV1q6Et9Gv4LJU7xLNqDa61dKWtprDuTqIg1Di+UhrSeeiuuH8OfiNSyINu5xsAtDwrQQOw8yhrTI5xzki9gq/jjiCj4Cw6R0ZY3E8QGRjRvDGdz5u+Hmuacu87jpveH5xmdql49xuABnDuHyB1FSk9dI3+vlO7vIbDyWJpQ65a7VoOvmnw4VUIkac2bW/eUtzDB2TutmLZcGStFVUUpsG1UInZc/TZ2XfcWn2JWNQ5S4XO/esvh+Kuw2opasbU0wc7xY7su+439i1OLOtOM9y2+p7wiRrMrqSVUDCZOpMxieGfWtooUbRFONdiul1VRSHC3ODmdR1Z2OlrLmQa6We4BOqjj5Lnvcb/AJX4+PD86u9t9geLPw6nbINeat6LjM4g9zC0tA0WThD24eB4KJhby2RxNwbq92OP520WMyw1UwuBYKAwU8WrQLqHVlxcTmKiEvOzin9n8NNDi7TBkvsEiHFuoBANlR08UhPPVOS0z2gnVH0n4i2+Xbk3JQ+XAOf3rOPa5p3KjyOcNiUfQ/ijT4hxBnpDHc7LIvvI6/K6Q+R7jqSpDGjqwpyu2nHjroumGqRKC6YDvKfhZ7k3L2ZmuHIqW/6TDTvijDnc0xJsrKoqo5KVrG2uq54zGykGXRZ7C25WV6QxkxzAGDYyD4rZNyix7lkOkdwOPcPaa9aPit8fHJyTt1aMWpdb+qPgsZxrYz0/2VsWkGl0+qFjeND+UU/2UZ+Jw9ZuTUaJrEyfkyDX6WycedCmsSJ+T4LnTN3LCth4XpUQ30U7D5+oxsv7iVAw/wDPQ3tvz2TzH5cSc7lcp4/5Fl46Jw7UGbO7XUqzmmPXWLSqfhGzoiRzV1NAOtvmC63HYEzvmCTsshi2IdVMWha2r0p3arF19EKioJJTNNwt4qGHxUbEMH6x5IapeHRCkjudkc2Lw5i24uEWSlKseHqEw0+UdyKpwN80rnEusrDA5mviD+VlMkxWGNxBAuEyUUWAmMc7LlXSS0Hiw0+4iijafdf8V2w4rFKw5QLrhXG1YK/jTE5G+qJBGPYAFnm14vUCpeKfDJHHd2gVZwZQDEOJ4HPGaOma+pf5MbcffZPcRzGOGKC/K5C0XRbhLpaHE64jtTujoYz9ogu+6y5ObLUdnDjvKR1fhGmOFcKse8tY90XWOLwbXe7W9vNcX4ixV2OY/iFedppjkHc0aNHuAXceM8Rbw9wTiUsXZfJGKSG3e7T7hdcBpo7C4F+5ZfjY9bbflZd6UfEMeWrgsNLBqnRRlkkVPpdurvPmmawg4iHv1FOM2vNx2H4pdPJlimnJ1DdPMrprmIxKp6zY6E6eQ0VTLLlF07VS6N12AUQNdPJlB0GpPcEiJa187/AbnuTpc2MZYxr3o3EAdXGLAc+9GyMN33QDYYTq5KDe5LO6Q49yYDREXW0CFkRQVC5KCGyNBH6KTJOO52is2PLZgRe5VRE4MkaTrYqyLicrh70lO5YFUemYVRzk6viaT57fgraB/wA60brM9HtQKvhuAE3dDI+M/EfFaGFwFSBdP9NZfGjiAEYSTWGG7QbBJYTkGvJUuJ1xilDcyxxlt6dXJlJjurtuJFl7EhJE3XvzErNurnuIDSSrrDSXNBJVZY2Rjx545XUS3Oa3cJozszbexWlJRtn35pcuFRtm0VYYWxPJzY43SkqJgWk2ygC5J0Cw2MdKGHYdI+ChiNZI05S+9mA/EqV0vcQNw6FmBUb7Tytz1BGpazk3v13XHiLkOJ8iT8D+9VOPV7Rlz2zUbqv6SH43SOosRw6F9PJyieWO9h5pvBJ+G6WugqmvxCnMJ9U2kb7diFjGtucvlpb4jn7FMieRY3Hde/wPL2rSOax3Gix/B61jTDiMAzbCTsqwZGZGZo7SN+swhw+5cMZM9hsCQTra2p8xsfYrLDscraFwkhqpY7aXY42/ePaq2nTsORU/FQthT1RYd0hV7bNqmRVQPJ7bPt5jdWtZj+EcQULqczPoJHGwe8Z47+JGoRZuCdVirBQsOBL6g/pLRVPDeIU8RnZG2rpx/X0zusb7baj2hUOHNt1/2lhZY3l2t4/z9L4ELo0T2vjaCeQXOGO+fg15hbKOqOQDnZXxs+RKxCIHayVTRNbTgqFNUPLdd7IhVkRBut1qy0sWubbcBBQGyG249qCey0587s9I0Pi8reOOWqk81gKt2TpGg/WLeyazyeax06cbqo1VTiUX3JUalAY14cdQlzVBjeRe1lBc4kuIvc6q+kW20uaQCUAEbrqHCLr0bD4Lkga4EE3Oq6vwe+9AzyUWLiVj2MjDWlzjYBPYNibcQhD2m4IWf47YH0rtFI4I7NE0eCP0n96aCslMMLn7WVDRcRtmrXQZ9QdQr7EouspHtHNYfDcHnhxl8p1bdEN0AOuwO7wqDHMa+T3+tbVXrBaFg8FiOM2gv9qMfSyuo1WDV3psIfe+l1KrZOqiLhdVHChtSN8lbV7c8JFka7OKeixUy1JYSdFfOf2LjuWapKN7awuy2F91onC0P+FFEZutxoQVgjLtzZXdPUCWnzXvdYXHnPbirLNv2lrsLJdRAnuTs6GN7Z7iB5bUCw5qpDZKh+QAm6tsdYZKprbAm6lUWHRwxZ9zuSua+vQxv9ZEKkpRSWcbi41JUTF6t7y1rdu4KfiNS3RrDt96rhEZXtc4XSg/5FbVMcIgSCqxkxjccpAKvsWbaEBgubdyzbWPjLs7TfxW/HNubmuk5tRK4i7gtDhtUWU4tY81lIBK+UNDStPhdO5kQzixVZRjx5ddpno5dG6V57R1N1ksVJZUEg6X3W1lJMDhyAWJxc3mLR3p4J5D2Hyh0gzchok4taQgA+xNUjMjQT3JqSQyTWKtNvRVFSkSC4WhiYGR2uq2mc2MG+4UuGoL5A0e5KhqcAyYVRVONV0jm0VNo2G9vSZbdlnlzK5JxzLV8VV0+JTyF87nZgOXsWr4olLaCDNK8GOYODCezlcMpPvI9yz5YXWaBck28llfW36UfDOKOp2dTVaAOygnvWsnjE8Qe3UjUW5qhx7BxNSk07bTMObTS6c4XxszNbR1BtKBYX5q0eJoia9rmP1Y8FrvI6LYwPOI8NUlS83mazqpPtNOU/C/tWYq4uqfcDsnVW3C9Y51PX0F76tqGDz7LvvDfekf/Caanmma4AuLb7X0S6Gld6cIy3dW+FRuZmD4yNe5JPzWLRuaw2utNTXTKZ3fa5qKB0NK221lVtg6s3sFqal4fTMBYRoq2ppgISWt18llY1+oo6iaMWBIRw04lAItZVWJiVk4GU7q2oJC2lOhvZGlXLpIFVT0uhy3SmV0E5IBasni7p31Jyh1vBOYM2frhfPZVpn9Lmtja1xI5qrnNgratY4NHZJVXMx1iMhKnTSZTSuM1n2J0U6F4LBqAoUsLifVUmGJwaE8oeF7ToiAE3NYORx5mtUGeR3WEXUybXllqJrJB3paq2ucHbqzhBcwJ5Y6LHPZt84BDeayXSG++P8AD3d1g+K0tU0teD4rKdIDj8vcOt/TB+9XJ0wzvbrzT+SjxaPgsdxoPyiA3+itgwH0UfZCx/Gf84p/soz8Th6zMmyaxJx9Ah7syek2UXEZ4zRxw5PnA71lhWx7Dj+UQ+ace29fJ9opiieIpI3u2CssHhbX4qRydchPH/IsvGx4RJbTEpNfjpjr2w76q0wHD+pjcwCyFTw82SqEpYLrrclg3TmSjzHuWYqqlkc5u4brWVNG+OlLGjksJieGVbqoluydC8p7VEPZI1VPU4PJ6Q5wJsSp+ERVEEVpBqpYe50li3mleyi1wCneKQNtyTFZhFQ+Vzm5rFXuDRhsLTbSymS1ETDYsF0DW2QbSfJlHNV1Ly2KBjpXk8gBdcPjmdW1slTJcOlkdK6/ibrrfS9xE2Dh9mFQANmr5A12u0TdT7zYe9cjjPUU0sp3sbLPOtuLHUVGM1PpNY430vYeS7Z0eYKaHhfhuKRmV9XPJWuFtbWJb9wauI4bh8uOY3R4dCCZKudkIt+kdfuuvThEUPElFQQ2EVJSvYwcgLtYPuC4fyL1p6H40/tti+mvE7fJmDsd6jXVUoB5nst+4OPtXN2FtPTPleRlY0lW3GeKnHuK8QrGnNGZTHGP0G9kfBZzHpvm4MPadZjmfbk0brbinzix5cvrKqWWRz253etK7rD7dh7vinKiTq8OAB9d1/cmJpOtmc4DQnQdwQxN2WCFl/o3VIQ53Fxa0ak2AS8vUt6pup+kRzKOmbe8x5DK3zTsLGudrrbUlAIjisLoONtNEp773Ddk2RqgE3JReaUUkoAigTY7oJJ1TSF90AD3IAbJQQNABrorJrrxtPeFXgWU5htC0c7JKdN6Kqw+j19KXDslkoHncE/cFuqdl5gdyuU9GFWY8cmh/tad33EH966pSuJlAVfpWPsaBn5u1tbKgxXD5aiYOBIC0cEZMYKakyB2oBKxwuq6eTH6x0oKPDHxlpfqrmlbkdZLdIAPVCKI5nK889xnw8XzdrSkmMQFiNUqXELSuc54DWi58BzVY6d0ZtyVLxhifyfw1Xz3s90XVN83afC6rjz60y5+Hd245xHisuPY5WYjK4uE8xcLm4a3YC+40sq8Mv33I30ufwKWBexv4Xv8HfvRtZqLNIJ5W39mx9i00wJEeUWtcDkL/eNwnYwA+5JudL319h2PtSomda7bQHQ3/HceRT7KbrLDY7X29/IoIcbcrfC+1tPaNx5hSWkPOhINtDfX2Hn7UT6SaBwa6M3tcDnb9EpENxe1721FtfaOaZJLDYFu+uot8Ry8wpTHOacxeQTsQdfYdneRUOK9817Ac76ew8vapkZB0ynQa6fEc/MIgWuGYxV4e8S000kRbzZfTzby+C1EOKYZjcYGM0EPWv09KpgGSeZto73FYoENF2a/Vsf+l3LyKdhky6g2I9Y5dvNv4hMNhXcGTNEWIYTKMSoA4AyRjts+00KS2mkY7Vp0VVw9xBVYTUiaCd0bn2Fy+7H+HcfI+9dCoauk4jpTJFGyPEIxeWEbPHIjz1+B70pJPDt2zPUl/ZylJloja9rWWmgpop7OY0bdymNwpkjSAAr0jbHRU92Db2hBbWDh9mTUW1QRoODYiy/SRTAi15LLsFJwq+oLpLWv3rkmMWj6RqRx/tgu3s4jhoomscQDbRZ4ryrJ4tw86nm7TWmyiRYSCSHNHgAtFPWuxioywx5nXtpyV/w/wm5jjLUauOwI0CfQlc1xPCzSM1Zbnqtjwe+1IGnuUrjXBRZrYrF50TfDtDJSxZXKaqXtLxegFawtIuEvCKIUbcrW2AT9Q57dGlTMMoKiq1IsClo9wl4zCxFwmWUkYfmDRdXj+H5i3R9vYmouG6hr7mQnwsiDavdoLLJ8Qw9bKOyCLrow4ecdC4qhx7AxT9rn4okKq3AGBkAG2it7Aix1SMEwZ8+gJHfZaBnDZ5klOwSqAQsabgBKe27dFoP4uAAk3VXX0fo2jQg9sxW4KyaYSEAkKXBF1MJYLbKJiVVJDIALp+mbI+PM6+oRRLNs/i9hVtJ70uautT5AbaJrG4X+kAjvUIRPeQPBc9nbuxusdmhmnk11ClOLYwB4WTrKRzY2uAHmo80T3SEWQeJoFksvb2G10+KCklcy4aSolXBJFEHjQhVsU9TnJDrLbj8c35HrUxYbRsIIa3bVNy5etZGwAgm2ip2TVI3cptEXmVrnm9ld8YY9LSth6qjdbuWCnifJVuLgbX0W+q5utiDLKBJhjXx9lgJRjEZZM7BTdY4NAKTNhjonh1jqVpqTC3RPD3NsE5XUjXDQKvBbKzsFCXuOhsp+H0FqkEqfFTdW25HJNCXqpUr4vDGW9meMsIbPhAe21xdh8nafGyx2GO66BkrrAlva89j9639VL6bSSQO2kaWi/Jc/gjdTVdVTkW7XWNHg7f8A5gVndtbJPDzrl1yN1QY3hnolSyupmluuoHetKxgIBtohNCyRpY4Ag6G6Gd7M0FazFKGxsJWjUJ/AqtuG47RVEmkZk6iX7L9PuOVZlkkmCYqL36snXxCvq6JtRE7KbdY2wI5Hkfeq0UrrTmUsYsALqukEHyhEbC2ZUeF4hLiOGUtWXHM+MZx3OGjh7wU89shkDy46IguPe22qZYBGwAjuSZI4nxaWKyE1bM4DtnRWeH173R2c4qbCqFjNPEJb5eabgdE1mXwR4sTI8lV9LFJNUxwtOr3Bov4myap4kywwudewS6aOFjrtygrox6PKTDYIgyiOK1Dh25JH2iafBoPxU6m4ar2CzIqClHcyJun3IuRTDbmc3zjdBfyCiPhGt228wuzQ4DWt1fWst3BqmDB3kdqaN3fmjBS3/wAVMdPP9RA2+gv5JoNDR3LveIcJ4TVxO9Oo6Rw3zhvVkeNxZcf4qwqlwrF5KahldNTWDmPcb3B3F+du9HqopwBZQp4AZLgFWLITbzRGnF7qsYWSp6vtWVlTgCMBNyU4z6BSYIzl2VZQsbpCq4rnZY/pDjy8Q8OkfWHxXQRSmZ4BasX0nQGDiTh8EbOHxR+meXrpwuKQfZHwWL4ycfSIPsraOP5IOXZHwWJ40/nFPp9FLPwYes85Qa8D5v7SmuKh139X9pYtjrQMg7lb8LENxaMnuKqmC7ArXhlmfFQ39Ep4+wsvHTsKnbZzgdLpwYxCanqTa5UbCqYNgcM2uqqKalvju50XVXHa1FU9nV3tos5WyRNeSWrTzU3zQ7rLO4lRFxNgnBUAV8IZsAFCGKQddYHW6cmw92S1iAqcYZae+u+6VJ0XCKyM0oI2soVdVh0jrOIA3R4JSltIBrsqXjmR2C8OYhXZiH5OrYf0nafiUjnblXEmM/xgxypqMxdFEDHEDybew9+pVLjL/R6IMGmbklYWwmIE7yvLj5DRROJJg6URN2bosbXVJprOgPB/lTj1ta9oMWGwPqDfk49lvxJ9i3+NYx6FimMV2bK6nw6zD+m95t+Cjfwf8JOHcGY3jb29uqkMUZ/RYLf9RKzfHtY5ldV0oJHXyRh32WN297vuXJyT6ykdnFfnC1l6OMB2Z523JWbqKv0ytrK2/ZFoY/b/AOArjGaz5Owt9jaSbsN/FZ5o6mhhYfWfeQ+3b7h966f+OUhpu/dFihu5o7mgIo/WScQN3JAoAmOOOPcjVG54jb1bDfvd3omg9W2Nt7kAuPf4J1lMWt1CDMNa4oyzKNU49zWHTdNOu43KASSL6IilWtqkmyCEQElH3I7WQBWKMFE42Sb3OqYOB+qlNN4hZRmt5p9ps0eAQNtT0eyZeLKFv1y9nvaV2WnjLZwVw3gyXqOKcKk0t6SwG/ibfivQ8OGyCXVuyqeCXuJ8L3dT42VNW1DmzW1WjjpnNisRyVVVYc58tw0e9Z4Ybvbo5s9Y9Kp1S630lYYeS8a7ojhj3bge9T6CiLBrlv5qs8Jrplw8tt7R6iBz7kLn3SnWOioKOivrLIZXC3JosPHc7rp0sJaCMzfeuKdKFV6RxQ+G4LaSNkemoBOp21G4V44yRHLnblpmIzc5r+Ga+p8L7HyKcDQBksPFtvi3l5hIjadDbV3PTX27OTobcciG7jXT2bj4JskiBnVxl4vdwsDv7jz8k7Rk5wTYWPfa3t5e1G8EwMtY37xe/wCB+KXACyxG5Ht/8+RTJPExByWBadS0t382/i1OgUczGtkYL8ng3se4O/Byhgkg6gBp5AgA/FvwSmuJdYXDnDwuR8HJGD4XxS6AvHeBZwHlzS2tGS4LcoPsB+LSlxHKL6ZQe45R7N2lPu7TgQ0l5bodMx/Bw+9URLXkvcCDcjU27R8xzHiFIjaBkygeBDtvsu/ApiNoaW89TlymwJ/RP0T4FTYxmDyQL/TOX/qb+IQC4xkLiG6n1rDUj9Jh39itsLxabCKinq2PY3qXZnMzkFzCbObYjYjW3eAVVhudzWNGa2unbA8j+9U7cairccp6YvyUzH3LiLdkesTqeQRsd16Jno4nOdPDYdY0SEDkT+/dQ6Gpe2YscDuqrhPjLD6+nrKqrlbC2SVrImE7Ma395KuI8ewEOzCqjv5hH0VxWzKjI0DRBUs3F2BskI9Li/aCCX1Bpw/iENPSDRN01nA1XZXcMifJIebQdVwvjieSl4whrYhdsEgefeu24P0m8PVtBCXVkTH5Bma4gEFTKv8AbTcNYDDTPJs2991payVlHCS0arGUPSFw9CdcSgsf0keJdIfD00dhiUB/xJ+jZOIVIq6kueNBslRVMUQAAF1npOM8BLr+mx6/pKRhfGfDLKlrpqqMgHcnRNO2voKL0t7SY9N9QtRSUTKdtwAsvD0l8HwMFsUpWkcs2qRP0xcJxiwxGJ3kppyxrZqtrCBlulRz5hoxYQdL3CbnXNYz3FS4+mThBo/no/ZKR/UbZhLiBlsqjiSj62HQarPu6bOE2ns1bj/gKrcS6a+GZhZksrx4RlOQWzTY8N0piGq0JFtVyqi6a+G6cevP7Iinajp44cynKakn9UUWUTKR0Kvr2QNIusxVzOqXF3JYLEemfDKqS7IZy37BUYdL9ARlFJUH/AUtU5lGhxCIunuG3AKsKeP5m1rLEv6UqJ5zChqD39hKHSrT5cow+o/YVaR9Te1njNOHTA3tqmmUrMmbuWdq+khkrr/JU5HK7U2ekZxbZuD1FvsrO8d26cefHWmokIbGMvcmWQZn5lnG8fSvFvkaf3J1nHlQNsEluU/gTmxW2Jx2isqiCn3SZuNa6ew+RJLKO/izEAbMwJ/uV4zTHk5JksRCQn6VpDlUDinGXaDAjr/nuS28SY8NW4Jb/PkrZfUbuPCmPpxdt3EXzKBSxltUI3AkA2VFDxjxSI8jcI9uun3JLcf4rcbswloPfYqcdwWyttiMUbKQlo1tyWehD5XG4KrJsb4zmZl+TGW8iooq+NQTlw+Mewqi6aWeBwZ6p9yr/QZHyXyuVW+o45lFvQYx7Ckxx8eE6Ukf7JQqZND6BIGgBpWP4mojQYrDMWlokOQ+Ttv+YfergU/H7v6iIf4CoeM4LxLNh082MwgNaAI3tbbK7cfeAoyi8c5bpVsNtSOSJxuRolRStnhjmaLCRodZC13aqGmlbjVCKmHOB2mfBNYJUGaJ1G/149Wk8wtDSYbNiT+ribodC47f+VnsXwuq4cxX51mV8ZuQNiCql/SLP22XBUBldWYffVjhUMB+q7R3/MPvWtfgzi3kuf0jKqunoZcJqvRp55BAXg7B+wP+ID3rUu4B45N82KP96cibkelwd7H7j3qRBQujGhHvVK/o341kdrisl/NLZ0Y8XuPbxaUf4lWkfSyqMPfKSS4e9W/BfDNPX4nI+qk0pmiVkbTbrHX017gs63op4ocNcWl/bWt4D4Sxrhmeq9MlZVQ1DRd7nHPGRfbwN9VOU6Xjl2vqqrqKeV2SSSMg30JCiv4jxSMWZWyW8bFKr3uaTaR7fBwuqKpqntJtNB7Wrgzys8rv45LO1lNxbjTBpWf8gVXUcY4+67flKRg/RAH4KBPWzAaSUvtCqqmuqrm1VSM8mXUfWX+1/OP+licQrq+cdfUVFQb/AEnF33K+xzCMPl4YbU1Lmw4hC4dXc6uYTqCO7msM2vqHvAdiMxvyiAb8FsMI4fnx/AK+iheyEVLRDLLJ2n5TroTsV0cO9ufm68Zbq6Ru9XEP8QTcjKMf77D+0FZH+D7BzxKoP+JGP4PtGfWxCcj7RXa5PqqkRUV/57B+0FLiFABrXQD/ABBT2fwfsNb61XM7/EU6zoDwdu88p/xFGylpimdhUbruroD/AIguYdKGI0mI8YYU2klbIyAjMQbgarrw6DcEjaLSS/tFZzGuinBcNxSLKHHY6lSdqy6+E0rbOB7A2WI4ycHVMGU6ZV0UcPwRQ2abDKsJx9RMo6umDTcFiWfgw9ZN9lDrTrH5qa7yUOtGsfmsW6TGOwFb8NVdJh+IiorZAyINILlUx+oPJano/wCH6LiTH2UNcwPhyF2U808fSy8X1PxzwzT5gK4a+KKDjPhYVPXemNutqOhvhUH+YRn2J5nRFwuw3+T4vcujbm0y8vSLwzlt6YD5KDNx7ww8/wA4J9i38fRXwwy38nQ+5PN6M+Gh/wDboP2UbGrXLpuNuGHaCZx/wlRXcZ8LtdcdY7/CuwDo64cboMOp/wBkJTOj3h1u2HU/7ARsfLlVP0m8O07cobN+wViulrpEosZwKHC8OieHTyh73PFjYbAeZK7T0h0vDHAPCtXjcuGU0kkYDIIS0DrZXeqPLmfALyfiFZUYti/plU9r5bGZ5AsL8gByGwA8FOWSsMe1jQWjYTyjblF/BUGIzdbUvduN1bl5hoXd5ULh3DXY7xJh2HNBJqqqOM+RcL/cs8m8eneEsG/i/wBFWF0RblkfFG6T7TjnK4hxZOaziaqA1DH5PbzXo7i6WLDcAL9Gw0rHyHuDWtsF5cq6sxRVWIykZzmfrzcTp8VjhN5ba5Zaw0zePz/KOMMpGE9XGRHp95UeqkbJUPy+qOyPIJOFsc99TWO1yNOv6RUe/bWlZHGGz0it1cnBo8JE46yQNGtyAg1lSwtbF1jhqddU1UzfRbspcxyMyjkNlBktbuToR8vegdPNGSkHbZIhOKQUokBJzIAbJLnpLnlyMNJTAAXSsqMANGqIu5BBUsHSydYRdR26m6dYe0UCLTCJTFiFPINHMlYQfG4svQQ4a46Ly4Ph11vqvO1M7I/ODqNV7wwCpFdgWG1eUfP0kMnvYFeFRnK40/hbj9w/nEQ9hTR4L47k9asjHsXerA/QHuR5G/UHuVyxFlv7cHj4C42dq7EWD2KW3o74wIv8ptHkF27KB9EIwbch7kWwTCz9uIHo34qALpsWsxoJccvJcRxRxqMQqKhzi8ukcc5Pj38vavXfSJi/yLwVjFYDlcKZ0bNPpP7I+JXkOQ63PkDm/wC78ClvY1o3E0agg3Otrau9mx9icYwue0DvAGps327j2pIABLbX7xb/ALfxCssAiEtfG5zmDIC5pfJlFxsA+2hv9ZJQ5qGSN/Vm5P1RbtW5jk4eIRQUxBBBsD7bnu8/Aqyq4eqfZwsTcvBZa3iW8vtNUckONr5iRYWNyR57P8t0ES6ItGa/hmBtbwvyPgdE5HA4tPZ8SLfeW/iEqNrnOFhbk3tanwBO/wBlyUSxrd+w095aAfiw/cnAIMdcEkm/quDt/BrufkU40ODSLgC+oIs0Hx5tPih2nBxcLadoZbkD9JvP7QRMuHCwcXW7Ivc28D9IeBTB1rHAm+bPbtZhd1vEfSHiE615ytGbb1XZtB9l3LyKbt2bnKG30INm38Du0+CUz1rdrPz0Ad7RsfNARscrzhuGSSWu+T5tlzzO5s1YegqHSV5toXWj07tz+CtOOa1vXQ0wyWY0vPzeTU8lU8OwOnrI2NaS82AA+s42CyzvbTGdPSnA/QphvEXCuH4xiHW9dVMLwA8gBlyG6eQWji6BeHmaOjc7zeV0bBKBmD4JQYa2wFLTxw28WtAP33UzOBzCUyp/Ec0/0DcNHX0Vp9qC6YHt7/vQR9UfEeYsR4HZXVrutOd0lgSQrOg6BqIgS9dICVpiwenM7PNb+hJ9HZpyW3zIx3b65jD0H4eBZ0zypbOhHCub32XTmk9ycBPIIPTmrOhLBQNQ4pbOhXBALZX+9dLbcjZKDSgac4j6F8CB1jcfan29DPD4/qD710IB3LdOCGUj1HI2Xy58zog4fZ/u6eb0T8PN/wB1W79HlP0HIClm+qUbP5YgdFnD4/3RqW3ou4fH+5tW09Fn+qUXos/1CjY+WQHRrgDNBRM9yUejfAP/APBj9y13o0/1Ch6NP9Uo+h8xkm9HWAt2oY/cnG9H+BN2oYh7FqPRZ+TSi9Fn+oUbHyzo4GwRv+4xfspxvBuDDaih/ZCvvRpvqOQ9Fmt+bcjY+VH/ABRwe1vQodP0QgOFMJG1HD+yFeeizH6BReizD6BRsfKmbw1hjdqSLT9EJY4fw4bU0X7IVt6LN/ZlD0aYfQKNlpWDA6Aainj/AGQljBqEf7vH+yFYCml/syh6PL/ZORs9IPyRRDaBn7KMYZSD+pZ7lO9Hl/snIejzD+rcjY+UMYfSjaJnuShSU7f6tvuUnqJv7NyHUTf2T/clsaRvRIP7NvuRimh/s2+5SOom/snIupmH9S/3I2ejQp4f7NvuRiGIHRg9yXllH9RJ7kRMo/qJf2UbEgdXH9QKBjuGx4tg9ZQZReaItabbPGrT7wFNMkv/APjTexqbM0o/3Wf9lAeZoGmA1NI8ZTDKSG9zXa29hzD2KfQUD6xwdY5O7v8A/Ct+OMEZh/Hwzg09LXOJJeMts3aH/MHD2pqWsjY4wUmkXN3N/wD4WGeXz06Mcfpc4YIqJrWxgZ9sw2A7h+9TcXwehx+jNLOxgmcLNmt2oh3qhp6sx2ayxeRseSsqGczODL3b9In6Syxyp5yObYVVS4TiM1J1o9YtY8HQPabtcPaAvUmE4rFjWFUeIxepVQsmA7iRqPYbj2LzPxrghwjEjLC09RL24z3d49hXUuiHiad/DkmGsoqmrfQyktMQvaOTtC/+LMuuXbns06hlafooZR3Ko+W68bYDiJ/wD96I47iA24dxM/4R+9NC7HkjflETi4hotqSqB3EGKNv/AKt4kf8ACP3pMuPYlUQSQv4dxFjXtLS5zRYDvU5XppjrYV8Op02WYxKmabktCq67HcSonuENU7ID6r+0PvVBXcbYo11nNp3i4v2bGy8vLllr08eHKRMr6Zgv2QFTvjbnOguqjE+Nq8uI9Hp7G+uqoJeLMSeTlMLNeTbpTOC4VvaOC8gsOa61wE6I4fUMY9rntlGYA7aaLzhh+LYrWlzTVvsBrl0+C6zwXiHEOB4Jkwjh+fE2TPL3ytcAGuGltefNdPBluubnx1HXi025JOU+C59/G/jw7cGVA83hJdxT0g/R4QkHm5du3I6GQe9II8Vzp/E/SKb24UcPao8nEnSSb24XcP8APmlsOjyXA3WH4waTiEJF9lTScRdJbr34cLfYqDE5+kSuqBJLg0zbbAM/8pylZuNyYDJTdm97LmvSPG4VlLmH0CrRsnSDkyjC5gLfU/8AKqMWwDjDF5WPrMJqXOYLCzbJZXc0eM1WReFDrPWi81qZOCeI7f0RVX8lBquBeJZHMy4PVdk66LPVabisaewFu+iAX4tae6Fyzo4K4jygHB6n3BT8N4Y4zw2f0jDsNq4pgLZgBsiSylbLHosHXcInH9L71wxtP0puH5rEPc1G7DulOQfmsQ18WrT6Zu5dYPrj3odY36w964O/B+lC+seJftNVVjFTxvgHV/KlRX0vW3yFz/Wt5IuUOPRvWt+uPeh1rQfXb715jbxPjz98Wqz/AI0ip4vxCja/rMYndK0XEXW9rwuETKU7Fj/CY4sGIYxScPwS5oaBvWTAHQzO/c23vXIDHaQ97yAPIBLxytkr6qSomkMkkjy5zybkkpbrGZuujWj3oohvFJMlOGAmwWv/AIPmDHFOkCOrc28eHwvm15OPZb8SfYsJibySdV37+DfgHyfw1UYvI20mIS9gn+zZoPvus8q0xaPpsxUUPCMlM02krZWU7R+jfM77m29q80cXVfU0tPRtPaf848eGwXZ+nPEjU8QYZhgfdsELp3t7nPNh/wArfvXAcWqflLGnuBuzNlb9kIx8GSS1gpMIay1nPNye9VdzmVtijsscbO4KnOhQSQ06DVKpWdZWRg7A5j7EzFd2m99lcsoo6KPrCQ6UixJ5eCATOSQbNOihSB3d96dnkc7dxKjOCKCXAnn5JDmnvRlIdcIAi094SS3X1vuQJKTY96YH2G95KBl7rAJNijyoIeYnmjaBzQFkB/4QWyxYalHE4A3N0h5tt5JLTqg0kz2vbexXrLhnpewPCuGMIonde59PRQxOPVncNF15FJJuuq0120sA10iYP+UI3oa27qenHBR6sNQf/wBaS7p0woerS1B/wLh5PcEYuj6pfLtbunTD/o0VR7kj/TnSnbD5z7lxkE9yWwnuJR9UfLa9KHSl/GfhxmFQ0r4BLUNkeXa3a0GwsPErkjnNPavvoXA+t4X2PkVYY5MX1TYtCI2i4IvYnXXmPMKv1ve5u7Tca+R2d7Vpii+gGA6ZRob2t6v+HceYUvDquSkcZI5PXaWO1B6wHkb6EeBUXQgAbNO1jYfi34J+JlidNSL7C5/B3xTCTNXOlcLkWj0Gps38W/BHHLe40BOtret4kbHzGqikEOadRyBvb3Hl5FG0aHTQHW7fi3l5hAS/SS/MXOuDo4u1Bt39489QnY3l2UAnMBuNXW8PrN8N1EY4Eg3cXHYg6+w8/Ip+EjKASLX8m/8A/JQSUJMzWEWuPVymw/wHl5FLDg27srbE/SFmk+I+i7xUbrGtcbjn2rj/AKh+IUh/aBLswLRrzIH/AHNTBzMesc4l17dq4u7/ABD6Q8QnGAANJyZeQJ7J+y7l5KOwjM1ot3tAP/Q78Ciqqo0lFPOM/ZYSSwag/pNPxSNgeIqo4hi0tnkh0mUXdm023VrwfI+nxGCrja0vZO2RmYXHZNxcexZsyF9Q+Qm5aCbkWuTp+K23B2EySgljS7qoxfTYuWVaOmv6XeLpCSa+MX7ogm3dKXFb/wD7pY+EbVnBhFU7aMpYwSs+olqBenpN4r//ACzv2G/uQVH8h1h+ignqBqncfVRkEgpowQe9W8XTBiMbAwUUWml8xXPQ4d6PNyuj7o+I6KOmHE+VHD+0UR6YMX5UsA9pXPWvHfsnGm50up+6fzG+HTBjR/qKce9WWCdIPFPEFayioKOGWZ3cDZo7yeQWU4R4IxLi6sEdMwx0zT87UOHZaPDvPgvQHC/CmG8KUQpqCEAn85IfXkPeSqm6myJmC4bUUtKx1fMyapI7RYLNB7grHkhe6F1R6HdC/tRIIA7oIkY0CANBFdBABGiuhdAC9+SNJQugFeSHLZJv4o8yAVZFZAFBAFZGgiv3IA/YiQ1QugDQQRDRBjQ0RIIIaBRXshdABJcEZKJBuV9PfD7q/A6bEoW/OwOMVxyPrMP7QI/xLklPVCWGOVtryMDh+jdenuJ8J+W+Ha+gABfJETH4Pbq37wvLJgNO6am1aGSXA7mu1A9mo9iy5Z1trx1Y09R1hyNJtzd3q9w+bq7DRZiCRsQsDZvio1bxAX/k9M4huznjn4BYW6X87aTGquLHL0Qs6NrSA630lP6EcQkwbjCOjlOWOujfSOHLOO2z4OHtWTwqqDi25s4K0qKv5HqocUgIbMyVk8Y73sINvba3tWnBybtlRzYaksen7lDMe9MUtbFX0sFZTnNDURtmjP6LgCPinbroYl5j3pDhnaW94IQQG480r4bg2Px5J3tOlnEe4rF4mz1hfKdLLe8WRGPEqtndK8fesLip9dzuTbn3rxc/8q9nDvGMtiT80rjltYZfaqvV0jha3ieas67XNzPraqA2w92qrG6TlFlgrJ8kj2SNjIeA4kgdnXReneiCNsXA1JkeXh8kjsx56gX+5eZ8MpGyQRzN6sgPcSZCQNu7mvUvRzD1HBeFAW7URfoLXu48l38Dg5mnt3IIt0Wq6nMUklDxQJQDMw0UKYbqbLsoUuqCpkuICYkeU4/dMSEhUkhziU24m6M3CIlBCablTqawsobQCpUBypksGuFk4HhR2HRIqquCip31NVNHBBGLvkkdla0eJKNKTPW5rnvTZhkNXwgamSSKOWklbIzO4NzDYgX335LN8Z/wiKLDespOGqM104u30ucFsTT3tbu722C8/wDFPEuJcW1r6zF8RqKmqds6R1g3waBoB4BLRrWqxh8EloI2FjTq95vm8gsPi+LNqql9TG0tmLvnORd5qHM6op5SDI6/I3UaZ2cmQ2ufW/eo8NK601DmAEnMQFZiQF7nb3O6pMMNqprTs27vuVmHjLols9GKoGVwa25c42HmvYvB+DtwLhnDsOjbl6imZGR+lbX7yV5R4Ow4Yxxjg9CRdstXHmHgDc/cF68xivZhOD11e6wbTQSS+4G332UZLxeaelPHfSuI8exBrrgzeiw2PJoy/gVzPCWdZWBx2Ct+Mqx5njpXuvI0GSU973alV+DN3d43VkdxGTO881Wu3Uyrdd581EduUiSMMjEtUwO9VvbcfAKVU1nXSEC9lFpz1FM930peyPsj/wAp2lpzK7MUA5l+aumHGwUyoHVReJ2Ve4oMlySUZOqJAJsiSr6oimQrXQsULouXgkQ+VkAbexFcIE2HmmRLnEkI280nU6o2lB6ONGh8ivQ2HcP00mH0kpYO1BG73tC89R8/Ir07hrCzCqFp5U0X/QFOVVihDh6k2yD3JbeH6Uf1YVmjCjatK4YFSfUCUzBaRhuWCw38lYhV3EVYKDBK2e+oiLW+JOg+KILNRyHE6gVWKVU7TZhkcW66NF9PEfBM3O1jd3LS58xs74pAFtbjTmSdPbuPbonLC9u/lbf2bHzC6o5tnIySdCABpcX7P4t+CkxstlBabnWx5+Nufs1UeBt+1YWB3vt7dx5FSc2pb4agjfzH4hFAnds6XN+Y1J/f5boNFiDy5dq37J5eRRne5G/Mnf28/ig61ze5J3uP+rv8wkZUbNT3X100P2hy8wn2kB1zcnw1Nv8AuCbZoRvt2dbkeR+kPBLaAbEC4J0sbAnw+q7wTIsOJc3LcfVy/wDb3jwKczjK0C1uQadCe9vcfBMEknKbG5sb6XPj9U/FKc/Q315G4tfwd3eaAea+9x2S1x1vo1x8fqlVnFdUIsKMd+28hoD7hwHnzCntkIeSbm2ji4X5bOHMeKzXGdVmfBACQGsvo/M3VLK9KnrOQMMjw3nJIB7Au29G1C1uCzVLhrNMQPJosuN4ZH8/GSPzbC72ld/4VpDQcO0EJFndUHu83a/isa0iy6hrRsEOrTl76ckLW2Shm8gQS7WQQBN4ZoR/Vj3Jz+LlCN4grS/3ob7brLda6iq+QaJv9UPctHwr0dxYzKyeeHqqNp1dzf4D96vuGuC3VRbV4k0si3bCd3eJ8PBaTGOIKbA4xTwBrqi1mxjZg7z3Lbjwt9ZZ5yeJssmG8LYY2GCKOGNgtHEwWLj/AJ5rM1PG2IvkPUNhhbyGXMVQ1VfPXzumqZTI8/d4BJBb3ErqmEjnuW123jLGAfz0X/DTjeMsW5yR/sKiaWnkldkdyr5hbq+HGWKbZoj/AIEQ45xJsoY1kEtvXuLALOS1Ic4wxO7X0nD6KVGWQsysHn4pfMG60snGmIuddohYO7LdI/jliv14f2FnzL3BDOTyCPmD6rQDjDFbetD+wh/HHFfrRfsKizkDVNumPcn8wS1oDxnif1of2EiTjfFGAC8TnO2GRUT52sbctuToANyUUYyXkkIMjt/AdyXzButBJxlij2tAMLDzytvdNHi/F/7ZnsYFSma+gASmuu26fzBbVv8AxuxYn8+P2Als4rxV7taiw+yFTsaSdb2UTF8Qjw+BxJF9rd57krIU26BwrxK7Fqyejmla6SOMSDSxIvYnyWmuuW9EMTKyrxHF5JQ6awgYy+zb3J+C6dnWFbTw4SUV9EQKF7oXB3QuUSNAGCjBukoDRBDvdC6K/chdA0NAiyK6GiDEgjKSgUoPLQCNxqvNXSphI4e4xqMoDKeZxc0nQBr+233HOF6SK5L0/cPHEcJp66Nt3ZXU5P6Q7bPvDh7VOU3Dwuq4FiWMuqD1MDi2K+rhu5NU8m33KvjaLE205KU13VvFydQuLJ24r+gqA17TstPT0cGMx09PPJ1bRM1xdzAvqPaFi6aXKdVocLqzbLe2m6nG6uxlNzT0H0cVQGAvwsuu/C53U7QTr1R7cZ/ZcR/hWsC5Z0Z4qDi0GZ1ziFO6nk/Wxdpp8ywu/ZXU16Eu5tw61dBdADQoIbIDjvH0XU43XAC15Cffquc4pYhzfrWHvK6n0kRBuOVF/pta4X8ly3FOy9mmup8rLyOWazr1+G7wjK1tnOce8lV5OS9yG9xIVlWWuRoLHdQ2sDnatB8wpxPL/i5wn0b0endKXyyauAaLXBPNereFYep4awuPKG2pmG3dcX/FeVcHjIdB2WggWzHUjU6Bet6BvUUFLCRqyFjPc0BejwV53Mf2QTdVUw0UDqipkbFEwXLnLIV3SII570tLGKVvrTVDi2/kB8Fvc5PWWOGWXjaJJWGpek6mrqkwxyQs1t+bJPuJ1Wipa2or256bEaWUf3cYJHsuiZy+DLDLH2LKTuUSUeCPqa4jWraD+qC5Dx/0j8T8OcUSYVR1NKYQ1pDnQC+qqM66q9qjSiywI4s4gdSskdXMzFtzliCxfEHSRxhTV4gpq8FtrkCAHVV4ne3a3FJC4DN0i8Xtbmnx3qba2DGX91lU1nS3xNEcsWOVLj9YtaPusjY09KTVFPQ08lVVzxwQRjM+SR1mtHmuacRdPNPQTSRYNhoqmM0E9Q4tDz4NGtvNcLxXpC4ixOS9fjE9YwG7WTWLQfAbKrdxBPXSNbJYeA0BRsad14e/hN05mkp+JMH9FcATHLSOzNceQIdtfvWD496VcU4xqbVExhomm8VLEbMaO8/WPiudYoGuu1xIPcVXw4hNSjL2ZYucbxdv/j2I2el/U4nK1nWDtDxUCauiqxcmz/EJENTQzC7ah0Duccuo9hH4qNUtieS6F4JG4Gl0tiG6h+fsu17ioDxYkXS5pTmt9yaLhqD71NOHKAfOSk7hlr+ZU0vsAFEoyAJSBqbBPOJtopU3nQdSit6RqJztRBHLL7Q234runS9ijcM4IqgX5fSJGRHxbfM77m/euJfwfXW4+kPdRSH72rX/AMJXH+roMMwiN/bkL53gHYeqPg5T+1Tx5/xOrfXVs1Q/eRxcrGgb1VMTsbKpY3PI0W5q5b2KfzKukgzm7kwddAnptSUimbnqYxyvc+xIksxGWVsLNcoDVbPiioIQ11s1tQmqBjKVrqyUD9Ad5UCrq3VDyXG9yjwG6mcyuJJ0UdyWdURCDN7IFGQisggSSjJRFMCJFkLhEhdBbDwSXm5R3sEjMb3QB2KU1iISW3CWJAUA7TtzTMadnOA+9eobNjaxjfVYxrR5AALzBAYy7taLv3A+PjiDAIJnOvPAOol82jQ+0WUZKx9aIaox4JIPsShuoWWAsf0m1vVYTT0YPaqJcxHeGju56lbAeS5l0jVgqccbTgkiniDbb6nU6c+W2qvCbqM7qMpG7Y92gdf8eXkU4fpNsLDUjLoPG3LzCQDqDc66XB+6/PyKUTYfZPiMv4t+C6GCRATYE89jfU+TufkU96nd2TrpbL+LfgkQC7Tcknfb1vZsfMI3OuRrbk05tvI/gUjLa4l+lwSPafwciBsQdLX0tpby7j4FIdo06tAB7QIsP8Q5eYSmW1JLr87i5A8RzHimDoOVrhpbS4IsB5jkfEJbXm5LrNvvm1/a7x4ptrrbA7aWNzbw7x4Jbbdkghp3Abrp+j3jvakCnaON+Vg4nXTx7x4oy6wB1GUc9bD8WpF9QBe24y/Fv7kCSALebcvxH4hMi4iQ/Ygix7JuQPDvCw+P1Iq8SmLCCC7ICG2v7O9bGWXqYHv0OVpc0A2v4tPLyWBfIXzl5JJ1eSVGS8Yt8BpDWVjIWAkzzMhHley9DNY2NoY0dloDR4AaLjPRtRekcQ4e0i4hDqh3sGn3kLs6zyXA0KP4IgfBH4pGBvy1QQ18EEGto45JpBFG1z3uNg0aklbrhvhJlDlqq5rZJ9wzcR/vKdwTA6fB2Z9JJ7dqQ8vLuCpOJONXTl9BhMhDPVkqR9LwZ+/3KuPi/wBpz5F1xDxhHRF1HQESVA0fINWx+A7z8FjH1DpXOe/M5zjcuJuSVDgB5KU25XVMdObK7Ka51wRp5p1jncykWaR62qW2x0sD7VQLDncio8lS6d/UwEG3ryd3gEUkhqiYYNGfTeOfgEtkLYWCONpsPvSBcbGRNys07z3oy4DQlARO3PxRtY4n1QAgFNe3uujMnigY3Acgi6t3NqASZCfFNyTOjbmO3xTrg2JjnP7LW6kpqOIyuE8oygeow8h3nxT2ComPv10o+cOw5NCcAJ1O6Tz0df2pbXd6AU3RK1dpqiGvKyc0ibnedByHM9yW9AieZlHAXudlNri/Id659jmLTYnVtpqckuebMH1R3lT+K+IB242OvsDl5nkB4K16N+D5Kmf5QrG3e7UA8vBZZXa5NNr0WcOuwShzOBzPFzddBaFFoaZtPGGgAaKWBooaSACjBQ+5BBgSjBRIIAwjSboEoBSCTdGDdABGiQugwO6JA7ockEJUvGWFfLPDVfStbeXq+ti+2ztD4K6QBsQd9dkB4nxehFDilTCG2bmzsvya4Zh8SPYoj3DMGEB2bcFb/pfwA4JxNJ1bbRiR0VtrsPbZ9xI9i5/USNpzoCXPdkaOdua5OTHVdeGXWjtHK1oLA4ktJ1PPyV3QTZXB3is5lLJxNcFvMW27ytDgdFJidWyKIkM3c/k0fvWVjWX/AG6Twe+ogjficQJFLJHUxgfScw3cB5tLh7V3tkjJmNkidmje0OaRzaRcH3LjeAMipY4qaNvzQGXL8b+a6TwXUOkwJlM83fQyOpT4tGrD+yR7l2cf+OnFn/lteoDVBGAtEs5xdhVJiLY/SoGv7NgdiPauZYxwDRSuL4KqeI6ixs4LrfEDb08ZtsSFja0bhcnNjNujiysjlFb0dG5Pyl//AKv/ACosHAEbX/O173fZjAXQK8alVE7nsjkcwgOa0kE8j3rCYz/Tb6yLwXBME4dlgraxhlbG4O+dN7210bsrTiPpqqpXlmExNpYzftk5nn28vYuWY3jjpC7NK7qo9Bc7+J8VJwqmpoaWKuxS0heA+KlB3HIv8PBF5L5i6MPx8Z/bPutXS41i+Ps9Lrq6SKjBN55XE38Gjn8FCxfiamDRBRtcWs0EkmrnHv8ABZvFseqcRk7T8sbdGsboAO6yp6rEmMIDnC5KzuV8jbHCTurebEX9aJWuLHDUEFX+BcaVEEjeuecw0D2mzveuevxZrgCSO0dFObUBrtHagbpS3FWWGObvuD9I8xa1sswlFtpRf7xqsrxtwtW8W4zLjNDLRCVzAGQyyOYLjvcAdFz3D8ZkY8ND9FoqLiSqpLFr8zL6sJXRhz3Thz/GiHjPA3Svi7I4nYrgtDTAerS1Dm6eJy3Kpqjow4toIS+XjCCSTnEGOcD7SVtpOKn1MV2OOm4vqFR12NSSk9pxJ3unl+RSw/Gx/blmMvr8LqTTV4Al5PYey/y7lRzV+dxJK3HHFJ8oUEj7XkYMzTzuFzHOV0cPL9xy8/F8ZaiXLUZimxK4g94Ucu8dUYkPK602x0so65tZF1FQ8CQepIfgVHkjcwEPFrKGT7Et8znDtPJ02TIl2jkkvI5lJcfNA7JHoL6+KS496MpJQNJNGey/zCkOIyqLRH1/ZZSJDpolTjoPQA+3Hzm31fRSge9qpemjHnY3x/iJa68NM4U0eulmCx++6X0Q4xHgnGfp0psyKhqnn/DGXf8AasPWVUlbUy1Mzi6SV5e4nmSbn7ylPT/RVIM0t+5WcxyxMCr6EC5KmVLrFuvgmSLNqLp/CYOsnfM+4iibdx89gm3MdLII2Auc42AHMqyqWCjhZRxalur3fWdz/cmEarq3TvPJoFg0bAKOBmTrYHO1RujyDUJGaIsBpqkEJbzfySXOACAbOiSjc66QggJASTrsjPvRAploO5EUe6BsOaAS/YBJCO9yjQIKyGXXmlAoA+CZAF2foap3M4cqp3A/PVRAJ7mtAXG2Nu8Bd96NadlPwVhuXeQPlPmXlRn4rH1p0sW0SNwlN7lm0OXAGZ2gGp8lxXGa35RxWrqiLiSVzgCNhy0/ELq3ElcMOwGtqLgO6ssbrbV2n4rjx7It3a2OlvHvHmNFtxT9seS96FrbxcO+9x8HfFKa29u4bG9vYDy8jokM7ZsRe4udL5vG3PzGqfabAEO1Olwd/AHn5Fasz4aGMyiwtuLbeY5eYRZS43O59tx8HfFDKA29gMvsDfxb8EmV+pDh4kH4kD4hIFkjQgkHZuU/An4FBtgQBbQ6WNtf0e4+BTbXakEDUXN9bjx7x4jVOWPOw07VxfTx7x4pmcF+8anloCf+133FKO5B11s6+lz4/Vd4pt9ib87ak66ePePHkl5tLdw1vrYeP1moIokm+m556a+PcfHmgbnQnc27iT+DviiJcNToALG+oA7j3jx5IEC9vYQT9xPd3FAVuPzCHDnjU9Ybbb+PgfBY+MF7iN7uDAtBxZMOsijvcgFxvvfx8VTULAZIrjkXlZ5NMfHUeiijvVV9YRpHG2FvmTc/ALpAusp0Z0fo/DTZyLOqZXSX8BoPgVqx9yyvq4MIAIgfejQA9qCLU66oIDTcS8UT4s59HRh8dENHO2dN59zfDmqSKKQAANPuXEqbGKv0ww1mJVUbTo17ZLC/irYNqneri1fa3KQLonJIyuG3YI45rABjvcpbBKNMp9y4u2Ottb5XxH/iD9yjisrWPe0V+NAtJFw9tj5Kv5R/G7s1r9y37k3IZKh3UxNcGfTdbdcQixbE6aZk0WJY0HMu4EvaQLeBUl2K4zKc7sbxDta2zgW+5L+Ufxu0tgfG3IxtgPBORwSA3IJXE/lPFdjj2ID/APYP3JufF8Tp2CQ41ikl3BpEb23F+eyP5S/jd1EMh1NwPJLEbhqCfcvP7eIsRe6xxHHGi/rOc2w8VIhxGvniY92NVxuL/nB+5H8o/jd46pxJ7R9yMwkNuXEAC5JC4UairOpxitP/AOwKPPX1tM+MtxHE5Te945G9kja90fyD+N3QROqnh8jSImasaeZ7ynnxOcP/ACF5/lxGrqpnzS1WMPc92p61ov4+Scpy+bNmrcSitb85M3teSP5D/jd3MRB2HvRBoadSB/iC4caRp3xKq/4wVVjVT6AwMhxCqknfs0yAtA7yj+Uv43olk8DCOsqIWeLnjT71U8SY5FDTuZDKwuFwS1wPVjnfuJ+C87Mrq+YjrKyXfUN7K2vAOF1OJxS07Q7qp587nH6QAt96LnsTHTX8KYFPxJiraiRpMDHdgd/iu/YHhTKCmZG1oFgqPgvhuPDKVnYAIAWxYANLaKVSHG6Jd0gJSShoaIIIMaCJHdBAggggBZDZEjQBhEdBqgh5oAIIIeaALki2RoigOQfwgMCNTh0WIxtu5zCwkfXZ2m+8ZgvP9ZSPgmY94OXICzyOoPtuvX3HeFfK/C1dA1uaWNnpEY/SZrb2i4XAKHh6DHsEfStcG1VBI6AE/TjPaZ/ykD2KM8PqLxy0wNHTyVcwijbue0TsB4reYDBFh8bYohYcyeZVbBhjcMzU4jLS09rNuT4qdTy5HArl1pvctt1hkwu1w5LccHYg2PF5aXMA2qp87RfUvjNj/wArh7lzHDKuw3sOZ7lYYXjLx0g4CIXhrGyOiNz9Asdm/et+K7umPJ07eZEYl5XWblxyZ8p6gsDB5EnxUOv4mqMOhM00jGNGl8l10fLH6jQY3IXUoAtoViq4PJOgUHFOkKQxvaKqmJYC4tMdyAN9ishV9JUjrgVNGDe3ahI/Fc/Lx21vx5yL6sikcTt7lmuLJnYbhTu0BJN2QNrN5qLU9INTHKWyS0TXNNiDEdD71RcSY1UcQzwRtDJpC0MY2EWDiddAufPC4zbp4MvvJj6zNiGIQUMRN5XWd4Dmfcr/ABOVrHAteSALW7uSnYHwb6FUT1NfilFHO8BjGRZpXRjc3IFr+1WjeGeHWyNfVV2JVYBuWNjbG1/gdSbe1YXWtO+b9c/krKyYuFPS1E4vlvFG5494CvcK6LsUxiNtXitW/C4yLtiMWeZw77XAb7dfBdMp8XwynhZFT+lxRtFmRQhsTGjwsj/jE+mjJp6aId5kJe4+0p/WOKLjnl651jHQ/VM6uowPEJaoxuBdT1bAxzgPqvGnsIHmqQ4TiENcaOqpp6dze1J1jS0uPh4LrNPxaKh5jqWmEjZ8Z0PsVoKmDFIjBVMgroLWyvF3AeB3CrcynRTeF7cngpYYgdfVG6UKnWzXG3itli/R5BVxukwSsdC7c09QczfIOGo9oPmsRieB4vgriK+imhZykAzMPk4aLP4sVeSXxKZUhjc2Yh3moz6u7zqTrqoZms2x1UGqro4fWeAT4qvnbK5SJWNTh9LJc3u1coeLPcOVytpieMMfEQ11zZYouzOJ7yurgwuMcn5OcysDxRovghe66HKIot0o6pJ02QBEBEe5HfREfBAC90lwRoFBU9Reu8eCkSnsqNSaSnxCemPZSOEU8r4OulY4tPVuZoeTtCPddQlIfpTO19Z4HuH/AJUcbJhMoRofNOVZsRrsmqE6keKdqtUgt+H6YESVzx6nYjB+tzPsCU5jHPLn6i6EFW0YXTxxaAN18+agTTuOg0VeQtHJ6loNmAABQnylyJxuUm1goUIuJF0k6oyNNkZbYJkRa6IhKKQUAlEgdUCmQInHkjvbdIJQARtdyKJApg5lB5oBtikNdZLDu9IaOMFiCu/9HBLuCMKOn5t4/wCcrz813aC710WTddwRRC+sckzPc+/4qcvDwasb8kBujtdAalZtGO6TK4w0FJRtdYzSF5A3Ibt4HU7Lne4HIN9lvxb8FoukGuNXxE+FpuynYIgN7nc6c9T5rNB4tob8gQfuB/Arpwmo5s72cFrOGveRb8PxClRMuATz9t//AOviocRFhezQ3v0DT8Wn7lMZ6pFieZBH3kc/MKknXOHZNyeQsdfYfwKaGo7O19ABbXw+qfuKD3E337XtLh/3D70RN767jl2rjw7x94QosdmwJ0vy018O4+GxSmAG2t9dCNNfDuPhzTQsQLgaje1wR+I+8JwXF9N7Zs2unK/ePHkgjgcNLC/dl018O494RtcdC2/eMot7W/iEThcEnfQHNzHce8dzkLuvsSTy5kj/ALh96AMm9jcAW5ahoPMfonn3IZCDbTs6WPLw8W9ySXOvcHne428/LvCJ0gijc8kMyXN+TfA+Hcg2T4hqOvr5QDcNswG9/Yk0UZPWOHKzQok8hmqi9wGpLjbZX3ClD6dieHUhFxNO3N5XufuBWVaSO44FRjD8FoaW1uqgYD52ufvJU7bzQ3Jtsk3WSh/FC6I933orJgrfvQRe0oJhjuJeh6sqcRmlwmWGCBzrtjkzHL7VTf6GOIwbCspQPAvXqc4bGT6g8dEYwuIj1Aq1R08sDoY4j/8AyFMPa9H/AKFeIDr6fTf869UDCIz9H7koYNF9Qe5GqNx5WHQlj5/+40w/bSh0I48d8TgHkHr1SMGjvfKEoYNH9Qe5GshuPKn+hDHP/wAnAf8AC9H/AKD8bIt8p0/7D16q+Ro/qhH8jx/VCNU9x5T/ANB+Nj/7jT/sPR/6EMb/APydP/w3r1V8jR/VCP5Gi+oEfNG5/p5VHQhjJ/8AucP/AA3JX+g7GOeKQ/8ADcvVPyNH9QIfI0f1Aj5y/wBluPK/+g3F/wD8nB/w3Iv9BuLf/k4f+E5eqTg0f1Qh8ix/VR85DceWB0HYqDriUP8AwnJxvQfi1wPlKH/hOXqT5Gj2yojg7B9EImNG484YZ0F1TpWuqsSzNvchsZC7FwTwFS4NGxrG5i3dzhutczCmtPqhWdHSiJuyqb/abo9TwCJoaALBPgaoAWCUEwFkLBGEEAEEAggwQCCCACCCCAHgghuggtAgghdAHyRIIIMER1CCCAKw5gEc781wJ+Hnhrj+vww3ENRmZH5t7cZ9rHEexd90XJOm3D30VTQcQU7TnZYuI5uiOb72FwQIzPFWEdaz06FvaYPnAOY71lIzfUmwGpK1WKYzLibHU+FAFj23dMdAGkfcub4zXPp3mmppSQ0kFwGruRWOWG70vDLUaN2LhtNO+FwywgNFvpPOwWr4Fw5tQX11YGvA1LncgBr79Vz6CnMUNBh41frUSgczs3710XGaocM8C1OU5JZWCnafF25911rx46Z53aB0U4c7GON8e4lF2UzAYYmNJyZnm+g20a0ftLdcWBz4o6dkbpS46tbCZtPFgIuNO9MdFmEfJHBdFmZlmq81XJ39r1R+yAmuKpY5awMkELmsBNpWz6crgxg8gdD3raM9MNjMcvUVjhTOZI90cGWOmFNIGjtuNiTfdupWQjoi6tgbN6Y1jpszjK9paWjU3tryWvx6KF1DTQuFIA+8/VywTStBe4kFp3HZA9bXyWbFNHC6qliZSgxwlgMcbobuecti53hm9ymxUyZmqHpNS+QteHSvLi1s5F7nu9qvKCnkwzrq2oIMsvZhb9Rm2bzOw8PNR6KDJVxvlbI2JhuXelNkytHLvN9lcUoNRI7FZ2t6kH5mM/TcOdvqj4ri/JsnT0Pwsbd1Y0tFZoM9XDTSOAd1bgXOA8bbHwRy0cIuW4mwnxhcAqhtSOvdLLJd7jf2qV6XE4WzNuvPr1J0k03WtkyuqKd7e9lwfcQpktzGQDf2qtgljz3BHgpomAbe26jJc7Q8gDk5HU1EJvE8gjYXSAG9ZdztTvqie4C9tu9KUriuaLiSoa4CphLg3aRjrOH71o6PHY5Y8ri2VjtCbfELBxSPdtsE+2odC4OaLHe40WmPLZ6wy4ZfF/jPBmA441z4Yzh87v62nGl+8sOnusuU8SdCvFkLpamir6PE4GguNpOpe1o11a7TbxXSaTGqguA7IHPRZ7pR449GwUYHTyFtRXN+ecPoQ31Hm46eQK6uLk+rqOXn4vnHdc1wVsdDH2XMfIfWeRcnwHgpdS2hqbekUNLIfrFoB+5UzLMAySNt4FIdK8uuX+a7482pkmFYQ89miy+LZXBRJ8Gw1rbiKdndaW/xCDJnk93clPlc5tsubTvTSr3YbSEkMqpGfbZce8Izw5UvjMlPNBP+i0kE+9GSHSXIsFOhrQxt/uS0GdfSVIeY/Rps3MZDdS6fhzFKm2Wlc0fpaLUUXEZpyLySgcxYOB9hTGLdIFW13V0UMENvp9UMxU2X9LmkOk6PcVqLFxYwHu1VzS9GFiDPO53gNExgXStitBKBXUtLiEJ3a5mR48nD8QurcNcZ8JcRxAmf5PqALuhqhlt5OGhWWVyjXHHGshi/COFYd0c1kkeHQtrqSVn5Tl7bmlw3Ptt7FyqpFgu6cccR8MOwXEcOpMSinlqqcxARtJaHhwLST7CuRRcPmuaXelNYwbuyGw9qvC2ztGUkvTPE3prdz/wTK0x4Wp2st6e94JuS2P4aqPV8PU0DMzJp3eYC00hV0XrqTLBLKC5kbnNG5A0UnCsFfUSlwkyQt1e9w28lJbPHPRS0sYPzbjlJOpvzS0EaktBhrHObYulc255bWTD9ylVF4sJigd+ddIZCOYGwTETy+PX1giiDLdUMvek5t0RfySMZFklxSHPSCSUFspzkgu1QNyi5JgEDqhcor2QBON9EVkYRFMtAEaF0LoGhIxuj80OaQ0UF3Hoel6zhFzL36uqkFu64BXDmLr/QlKTh2KxX0bNG63m3/wAKcvDx9dKROe2JjpHmzWAuPkNUd1S8Y1/ydw3Wyh2V72iJuttXaLOd1pl1HJcQqTVVlRUO1MsjpHX53PMfiEwDe3Mkb6G4+Dvims2tuTT5Zf3HxGiPMdRbfWxF7+JHPzC645Nn43AEWFtbA328j+BU4AZSTYAG/dY/9vwUGmOdwO4Ol983t5+R1U1zrMAFgRpcG1vAd3kUHCXkZiLd1za2vj3faCIk3I27ydNfHuPiNEi9jcG1jbTv7vA+GyU0WtbfYWH3C/8A0lAOA687377G/wCB8diltubctTa29+du4945psZdLEW2ta4tz/w945JWhFybiwvfu5XPd3FBlgAAG40Fxl1FvDw7xySstza3IC1/uv8AApAOpuTmJ8jf/wDr4o79xBuPYQfwP3FBAXHMXab3v+P71ExaYQ4dKSQ02yC+o+z+4qU42INzpz8f87ql4jqQImQgtFzcjuH+dkqqM+0ZnPIA1IaF0Powouv4kbLa7aWFz/Insj4lc/pW3fHz1LyuudElFloa+tI1kkbE3yAufvKxt6aN+ELoIKFCJ1RIzsiTIPOyCSbjuQRsO6BidaxBosU40LZJTWBLbGEbUtqAIR+CPqwlgI7IMgRiyHVpy2tkdvFBGur8EfV+CdtZCyAb6sdyGQdycQQDfVjuQ6sdycR28EA1k8ERjHcnkRQZoRgck40WRpQCAACCNBBaBEjQQAJQugiugx30RXQRoINUSPkiQBhDkgggAiKF0LpGFz4IsyG6JMDuhdEgSgDJWZ6Q8M+VeE61gbmkpwKlg78vrD2tJWkTUjGvaWOGZjgQ4HmDoQgnlnC8TfFQS4M02NM57DY2LmbtueQykXJ7rBZ91EanGII23yOs6w5jnceJstDxRhUvDnGFTRu0Y5z4jfZxZqw25ksOg71W0L3RursTc0AxsLIhzvtvzNzvzsgeLXhOD5V4klmteNr+z9hmg+9XXSM6TFMRwLhqE9qplaXAd73Bo+65T/RphHU0bpiNXkMB8Bv96a4W/wBZeluqr/Wgw2N7mdwP5tn/AHn2K4jfbr4EdNTiOIWjjYGMA5ACwHwWFxirMzqpsE9N10ruqjDMUeyQk2aLRNPreHOy1uKVHo9I4gEm17Dc+A9tljZJ6mnlp/S566CKBrqhzqylhhjbkGhL2kkWe5qrSdoWJ0lXJUv6qHFHRg2YYatjI3ADKHBnK4F9dVk8XzQQPjmfPE6WoyWqm+lWDG97dAMz/uV5JBhYZI8y8HOB9Z4lcBpue9QKnDZRSULGU9fE0wda5tBlbDmkcXkC5udwmIx2IxwF0FPDLCX1DrPfDB1eVo381IqsYYyCwIyRtDWNGzQNk7xGxtM5rr1LCyIhraggvFyBy5aFY10Fbjs7qajLY447dbM89ll/ifBeX+RN5vZ/FvzxkYhxDVz1TW0cEkxL8gDASSe4d5VrBw9j1c0GaSGhLvouJe8eYGgWk4ewXDuG6O0JL5yLvmkN3uPh3DwCDMSjE7zqDfQlc9znmMdOOH7zqPhnD1RQ5TNick57urDfxV9G0BvM+agR4jG9+rhopLa5nvWWUtvbXHLGeCsXykWA10TpjzXAOijPqczjl+5OiRzG5lPzTuSTGAxulkTy1zraW8FBNSQSDdJjrAZ7d2iPml9RdQMGlm+N1xnpFrHT8Y4i06CFzYWjuDWj8SV2SGqDW8vauH8dzNm4vxaRp0NQR7gAun8Sf2cf51/pFR1zrb7JYqniyjXujB8F6Lykz0t1th5JcdWWuvooOayGco3TT5Hh3baAkCbSwG6jskLfLxRhwKeykPuks023VbO0yVFlMcbBRJiGzB3elsLvCnU9CzOYI5Hnm8Xsjq8RnqXZGuytJ0a0WCgxTXaE7G/K4u5hPYTKWhhjHXVcpP6AOpS6ivfVlsMQEcLdmjSwVbLM6V/aJsjfMQ3INL7+KBpYPqc5ayNxDG6X70mepBZleTZQo35I73Tb3l4N/NPY0lvxQQ0hpYLnP6zjp7FVwymKqtqA/T2pV+1yTE4+cadjdTsH6gZibplt49U/KO0mn2sjYFIb6jYptGDu0+YSb20QBEaIWPmjLkWawTEEUklGXXRHW6ABKQTcoybIgghjfZAoct0LIMAEOaHJC6CHdAIroxsgDBsV0/oVxFkVbiFA5wDp42yt8S24I9x+5cvurXhnGZMDxujr4zbqpRmHe06Ee66VnQl7elbrCdKleGUtFRBxBkeZXeQ0HxK3DXBwBaeyRceS5N0kV3pXE0kQ1FOxsVu87nz32U8c7VyXpmWyZToAADYcrfu8jonBc6WsBra3325eYTAJvdvfpr91/wACnGFwGulvZl/FvwXQ50yG4H2txa+b/wDrzGqkakF1/WHncfj5bpimBscwtbU35eJA+ITsrrNI99xf2nv8whRLXZmkDXTz0/Hy3CUCLG9iALkk3uPxHjuE209k5ie/X4n/APoe1K8SXam+uhB/A+OxSI6CTqe8c9zyufgefNKY4+ta2/L3m3xamwbG1yQb/R9+nd3j2hOXtrfmNL+7Xv7j7EAokN0ygi1rX0Hhfu7jyR5r3vbzI/z7fek5tzpYg35D/Pf3IE2ve4I7+Xn5c+8IMRJBsPIDx/f8Qsxj8/W1T2jUM7IBFiPBaSVwY0kjQDXnt/nRZCpldUVWZxDruzEgKcqrE5Ssylx+qA0LufANF6DwpQtIs6UOmd/iOn3ALiVDC+fq4m3L5Xhot3k2C9EU1O2kpoaZmjYY2xjyAss8mkPe9HdFdDmoOgk890Z7gi8kyBBEggO9AJ1qbanAtiOtHsSxZIalhALA2Sh4pLSlaHmEAYGiCCMIAWRhDxQQQkEZQsgAghZGAgCR7oIIAIIboe9IAgghdMAiKO6JADUokdkSANC6IWQQBoIroXQBoIroE6oA0RQuiJSMECgggB5Iij2O6I6apkSQkkpRSCgOL9PWCujqKfGYIg5zmBxuNC+Pv82E+5cylafRaWmb2nTHrCfrch7ybr0d0iYOMY4WqhlzPpvyho7wNHD9kn3LzLNjbeH6mKqqKb0n0SVsAhzZMzWX1v5WKcF8dajLeGeFJZhYOp6c28XkafeQonQthZiwivxaQHPW1PVtcebIxb73FxWX4h4txHinh+mpqHh/EoX1GWoIDDIC0A2Gg5my6xwjhPyFwzhmHOGWSnp2tkH6Z1d95K0jJF4prImMbBLNSxNkdYiqkLGPDe04XbrfbZZZ1TQQmSYVNDTRyPZAyoY+Wsifb5xwLXE6+oLbd6vcXqKh2InqZMRia1l3vpKMTixJO52O2gVZBVSxQQPdiOLwPnYah76WhDzJncSM9mkNIaG9kJg3UYu2SmdHBxDQvlltG1rcON3l2mUdxN1FxHC5XYhKWYZWObms17MQytcGgNBDfo6DZWcte99RSxDFcZnaJOtfDPSCJjwwFw7WUa3DdAq6fA7HtcNYcZHG7g2tdud9cveiBzvj+I0A62oE1JG+ZsL43uMrmdnMXl3d2tlX1dfhmG0fU4fZsIOZr76vJ3cT3rTcRcPHFMIgp208Ja8zziN0rvmczyGhp+lo3muV4nwnU0NSKdz3nIHOLQ67bBtzqPYuTl4Pq7dvD+T8zS3HEFRiDy2nkblGmZ7wB/5Tz4ZhTOkdWyueZQxvVR5gBludBfw1WGhgqaZ2gBtqWkXWjw3E30tDCCJoxI97yILC+wF9D3KceLGDLnzyHVTYhE09XUSkt+tEQrhvy3SMu9pkaALm1tbJqHFI5wxvW1oMhDT80MpJPM2XQjNRzUjiSzVzvLuWn8OFZ/zZ4+MbR4+IhkmBa4HmrVuNRStGV4PkVX44MOgY4uykjuWBxLFKkTEUV4mg7jmsM/x5PHRh+Tf26Y/EGMaXXUaCuHXXzajVc2hxvFG+u4P81YU3E1VBcupQ7ycsbwtpzx1Ble0MZd2ui45xHJ12PYhINnVDz96uZ+MKl7bMpXMP21m6mQzTSSvFnPcXEdxWnBx/NY/kckymjXtRF+1ig5I5rqcheYpQ7024PDWvLXBhOjraFKv2TYoBd0YdZNhHySM5nzHdM1Iuy45JQ370cgzNsghQPGUap/ObWuoURyOIKkNN9EjOtdrqUZdr3pAuEXIoBbnkjdEHaJJ2RAkBAA73KDwHFrjyN0CECgiTJnnfrodQkOPjsknR2YI5NQCDuqBtx1BHJLcLi6bGpTh9UIBs6FDkg7dEUEJGiOiJxQKI73KLeyBRoABH5IrC6MIAxzRWRhKtdAIshZKIQtZA0LSyUG9yIDVOAaG3cgaencPsKGmLthDHe/2QuF4tX/KGK1lU4366Z7u+4vp5/FdenxP0bgj0+9iMPDgR3lgC4UwucMptc+G/j4+zVLjLkSg+7t730vf7vHyKkQgZrkgW0Gtre07eR0UNjhffU6d9/wB/kdVKhGYggnu/8a/ArZks4nBjCRoBr3WP4fBNu56Wsb2JtY/9p+4pUNhFkvqDbTS3h4eR0SHvGgBsQbaaX8PDyOhSMoNty56ctfwP3FKAtqQO4WHLnp8W+5Iab2Fxta2+nlzH6O4TjCHE66WHP3G/wdy5oBYIOhtra9j7tfg72FE0hoI5a8vf/wCR7UZJDbHvP0ffp8Rz3CSL39vL9/PT3hAOEkDW9+d99P3feELgMuCWke21v3fBJubgAgEDz/z+4pewAFhbkTt/nbyITCFiU/VUUrr5bjKL638PYsq3V7z3ANWg4glyQMYA4ZjcnlpyKoaZuct8SXFZ5etMY1PA1CK3ijDobXax/WuHg0X+Nl3Hc3XLeiWi6zFKytIuIYQwHxcf3BdRH+Qssr2uFIFFuhe6RgklGi+KCC/kgk+1BMO+jy0TjU2PanGrYjrUsbBNtKWEAsbpQ3SW6JSCKRgJIPijQY/ajGySjBQRSHJEhfTVAHdBFdDVAGgk3KCAPyKCSjugDugiuizIAzqUNkV0LoA0SF0V0AfJC6Sd0EArmhySboXQCroJKO6ANDRDQIXSMaL2ororoBRsiRXKK6YA7JNkZKInxQCXMZIx0cjQWPBa4HYgixC8idJGF0uA8Yw0OKOMdD6WG1Dg2/YadTbxbYr1091guO9MnRseK8UoMVgqaeBkLw+qbLe78o0y23uLA+SCX2G19BJCx0FZTiPKMgEgADbaaeSs2VVM4FoqodRbSRv715/rOIaTDppI6t8jC0kE9WSD7VWVXFeCVMjXtxeensLFrIjY+Oyf8ukzjd9qeHMOqppp/lbEITNo9sNfkYRa3q8tEmo4eo5JC6LGK+kjytaIaeqa2NuVoaLCx5ALhx44wD0V0IxBweWFok6l1wbb7LPUWO01PWQyzcWzzxxuBdGaZwzjuS/l/wCL/jeiX8P0uWRsuK19SXMLGPlqWl0VyCSwgCx0Gvcoh4Vjc4vHEGOZr30rWnX3LhmNcX4ZXMiFDjr6FzHEvIp3Ozi2g2R4JxfhlDHK2vx59c5zgWONO5uQW22T/m/4X8f/AF2ms4NpqgRMjxDEKdsUTYQ2KdtnBt7E3G+upVLV9GdK8yvdX18rnxOiu+Rps02vbTfQLm9NxnhEWJz1MuOSSUzwBHT+juHVnvvbXn71YHpB4fG1c/8A4T/3JXm/4Jx/9WdV0UQxPe6OsqgXNLTct1HuVZU9GLGtY2OqmbkGXlrrf8UTukPABtWyX8In/uUaTpFwE3Ppk3/Cepuc/wBKmP8A0X+jueNzC2slcI3BwaWgA2U04BiMcQja8kaqu/0j4EN6qf8A4LkY6R8Bcf51U/8ABcp+v+K0j1nB2JVT7veT4WUV3R7Wu3t+yrP/AEg4EbH0iq/4LkR6QsDH9fWf8JyW5/o91Wjo/q2nWx/wlK/iFV9zT7CpEvSJgjTfrK0//rP7023pHwd7rR+nvPc2Mn8Uuv8AQ3f9mZeBapjblo9xWGx+kOG4i+DIWkAErqFNxDNiLfyXCcamvzEBA95KdNBWVJLpsMfF+uLSfxVzH/UTll/uuM9aCNbogQ69iuzOwkgWfSwX8WA/gqPGuHKTETH15gphESfmiGk371UxrP6jn0IMzCwns21B2Cap42yNdmc6+zbd/eVqpMAwKmJa6tjce7rCfuCSzCqFwtSU1TKe9kRt7yn8D6jMNY7N1ZaS8G1hrqiab3BuLaLQTcO1TX9bFBJFprncPwVRiNNJTiMyscyQmxuLXSuNhzKVGRjU7otChzSM29uVwPcnGOSnNzi6bAskZ8G4/civ3omusgfNIFH2ovaUV796B20TgHoAkkC+6GYc0nNzQCH280katt3JT+aSy5JTI2d0403bZIfvdGw7hBAdtERtdAmyJBgdOaTyQOp8EXNBDQuiR80GCO+qK2qOyCGjBsgEN0GO6GiK3JAIIZCW06BIv5INOqA6HTcUGq6MKnDnyD0illjgGu8Tjce6xCxYkJ0/yf8APgmIJXBj2ZiA4bd9k5HbTn/n/OyeM0nJMiF3Xvv9/h4+3VTYnAagn6unw1+BVfE7M4DvPnf9/wAVMYRca8rDnf37+R1VoqW1+bvGlrAfdr8ClAXbsTfSwF/Z4+W4TMT2DtXJvoLC9/3+R1TzXCw109//AM+e4QRdyRewPO5PLkb93juOacBNxYG/lrfy7/DYpu/b0Bvfy1/f47FKvYH1bW8QLfuv7QgzrXZhpYWttppyt4dx5bFHsBz17rc/u19x80hrjcnXTvF/PT4941SnDUHXxv8Aj/nUeSYGQL3B13uP8+33pZy+Qtaw2H+dvck2HLXz/wA/51QuGM7gBcjc+X4exI4zvENQJKlzRmJYMp13KjUsYFzf1QGpurlNRU5i6+Z17ne3ipFMLR3PO5Wf7aOvdFlF6Pw7JUkWdUzuN/BosPxWxVVwtR/J/DuHU5FnNgaXebu0firTms76qDQuUSGyRgUm9/BKJukoIDqghoN0EB30eaW1ICWFuRbdE4E20JYugHBslJDfFKHmEAoFHqUnVGCUEUgiR3QY9eSCK6CCGiQQQA5oItO9FdAKRE2RXJQQYXQQugggRokEAaJBBABDVEhdBhqjRXQQWxoIkCUGF0L6ovahcoIaK6JDySMdz4IiSgSiQAzJBKURuiKYNPJsszxHSSVpEbNmgkhad9rFR46dsjnlwBuErNiOQYjwHR1z3GeiY4k68lVu6K8HJ1wyM/4iu2SYWwm+UJs4RGT6oWf8f/Wn3/xxUdE+CO/+1N/bKSeiLBCdMLb+2V2v5Ij+qEBhLAdkv4r/ALH8k/04oeh/BCf6Kb+0UTeh/BQf6KH7ZXbxhjAPVCbqaampIusqHsjaTYFx3PcO8o/iv+x/JP8ATix6IcDP/wBr/wCcpf8AoiwT/wDGf85XSqzGaOI2ihfJ7LBUddxnFSX6x1HTgD+tkFwnODL/AGX80/0yB6IMDI/o23+Mpt3Q5gdtcOI//YVLxPpgwWivnxZjj3QM/FZ2p6baKouKGgr607C1zf8AZBVTgv8Asv5p/pOf0RcPNPao2j/9hQZ0XcN8qO/2SVTP4544xQH5L4UniYdnyRZfvcfwUSpwjpTxkASVlPh7DuDPe3saLKpwpvK0j+jTheHWSlZG3+8lDfiq6r4a6O8OJNZUUrANwJi74Kkj6IMfq+1inFTvERMLvvJVjT9B+Btsa2uxGsPPNJlB9yucX/EXlQ6jGuiPDO0KVlU8f3bnD71Cd0s4JTnq+H+FDIdmlsQHwatvhXRpwthMrZqfB4nSsN2ulu8/etNFRU0I+Zp4o+8NYG/BaTCs7yRyf+N/SBjLbYfwqIGHZ84IA/aKWOHukPEgTWYnh9Cw65WDMR7hb711OVrdQRr3qK9um6r5L7czPR1Wym9fxHXz94hAjH4p6LgDBqfWWmkqXd88rn/ct9LFmGgHmorqU31sU/mJuVZePA6Klb+T0cEQG2WMBKfhhds13uWlFJy1Pgl+gZgLt+9BMi/BhzYVDq+HIaundFPTNljO4d8Vuzhmo0aj9AYBYtv5aI0HGazoskc8uoqpzG/Ulbmt7QoE/RnjsQzRmlntya8tP3hd1bh7Abhp96V8mMfe4IKxz4/3i2w5P9vOlRwvjVFfrsNnsObBmH3KrlidHcPa5h/SBC9Ly4XGTlkAF9Ae9VtdwdS1gIfGPaAVy3PXVdUw3Nx52B0SweRK67ifQ9R1Ti6Cokgf+iAR7lSz9DGIsv1GJQP/AFkZb8LomcTcMnOyLag3CLNqtlP0UcRQg5fRJB4SHX3hZbGsHrcCqvRa6Lq5CMwANwR5q5ZU2Weoj9DoUkFJz3ARZlRFE3HihGO0k31uja/LyQNkvGpSQUZRIIEknkjJskoMEEL+SPmgCRoWQ3QAR9yJGAgh6I0QQBQZQRX05IXt+5AG/kgCQFwj25IIB2JwcR3hODR9lGBI1GhT4eJGg/SGhTSkxvF+RJ077/v+KmRyFwt6xIt33/f8VXRkX2vf/PtU2NwPIG423v8Av+IVRFTIWlw5a6cze3xH3hPi5G4uTe9/vv8Aj70y14DAQR9Y6/j+O/enGSWOvf8AH7vwKojrSR5C4tb3i3xHtCcYT+lckHe58Ne/uPPZNDKQbO2F/d/nzHkjDresQdCNvf8A/HtCAeadNDbbY+7/AMdx0ThA0tt4/u9/3ps6AWI8b63/AM/+UvW+t/if8/iPFAOt8ee3+f8AO6i4lJ6PSSn1btsDzupTRcG3Ztv/AJ/zyVXjs+WFkV7lxueV7JXxU9Z46yuO9hv5q3wukNbXUtG0X62RkdvMi6qYBnfqb5nX9y2XRzR+mcV0riLtgDpzp3DT7ysmjs7WhoDG2yt0A8kL27kEPErNQeKFwhzRexAC/vReSF+5EUECCK6CBp38JYSQUoLcjjUsJASxugFNSgkj2JV0AoIwbJI1RoBSCK6CCHdAXKJAFAGTZFdAlEgDQRI0GK6NAIigDRHdBC6CBAIroIA0EVwLIEoA0EV0OSAO6G6FkEAOaIo0SALyCP2IBGgyba7I0aFgkBbIWtdHoiKAS4JBKU5IKYIelQtsEki52TkQQCi2/JFk8Eu3ijsgG8ngEMgCXsiIQRuwVXxJg9PjWEvp6jM3I4SxvYbOjeNnAq0cLBZzjriGXhrBRXspjUR9c2OYA2LIze7h3kaaJZeHJ289Uox7i6orJsS4grMPw6OYwCSCPs5+5xvZtxzKtB0RYHcSVlXidffU9bUWDv2bK16EquOvocdidaWN1ZctcLggg7hamu4fnwkGbCw6ekGrqInVnjGT/wBKjj/Jkvzkrk4LreLM4fwBwtQWdDgdHmH0pGZz7zdaCmpKanaGQU8UQGwY0NH3JNNNDWxdZC8kA2c0izmHucORTzYi06Eacl2yy+OO732eZa1soCS7UWsAe9C7ggGki9rJkZMNze9kGMse1qE8AB9JpCIk62A0QCMpGotYJDpM92kWtzTjnEN56JmVzb3JAQCJHHLawKjSRg6uFgnJZg0kNIITD5S4E3uCgGnAHUaIhY7hKAvpZFJLBAC6WWOMd73gfFIimsHJPxwkkXFgqOr404dw/s1GLU1xu1jsx+5VFZ0y8O0wLYI6upI+q0NH3pfUiphW5jpQSddu9D0aO5zNJXJ63p1mJtRYTE3xmkJ+4KiremPieqFo6iClaeUMQv7ypvJFTjrvHUsb2ms08VDrcTw2jZ+VVlNCB9Z4XnKu4xx7EifScUrJAeXWED3KslqZ5tZJJHnvc4lTeVU4noCv4+4UpbsfiLJj3RsJUfhfjrDOI8ZOE0wlzOYXxOd9K249y4HleTt71pujunfPxnhUHWyRdbKWF0TsrgC03sVjyf3jbj/renoU0R5hIfSnuRQ8NugIMeMYoPObMPc4EJ6SHEaRt/S6SqA/t29U79pun3Ll+K6ftG9GA5Bcs6csCD8OpsVjZ2oH5XkD6J0+Nl0Os4zw/Dn9XXU8sTr2vC5sw/5dUOK8Ih4l4Wq4I7PZPCXRuHlonj1Sz7jymSRohdLmifE90cgs5hLXDuI0KRddTnGCULhEgkAKF0SCACJGfJA7IAkfigEEAEEaLfZACyUk3Rgf5KAPdDzufAIwDfdC9kANeWiO1tUL3tohvokAFkdknzShZMBsg0WdpzQOuyO1wO8IKnGGxsp0H+fH/PvVeNCplOe/VVEWLFpFtSLd9/v/APPvSgNhcnw7v/nu2KjMJ8b77/f/AOfenBIfIbW/C34e5Uk8yQh1zt4fv/H2FSMwLbg5bDYaW/d+B8FGY4OB0OmoI7/8+/bdLZcENuLaba+X+fYmEpuhAFwed/8AP/xfuT0QN9CQO/8Az/nRMREWuAPaP8/58lIj53v+KAdBt3W+CzfEE+eqI1AYwA6c1owA0XPIX1+9Y+ulNRVFxcDnd5aKcl4jpWZd/otXSuiOi+cxGtI2ayFp8zc/Bc6gFmEnTMbrsPRnRml4XZKRY1Mz5L94HZHwKyy8XPWtzdwQuiGqHgFCtjKInVA3Re1BBdESgTp4JJJ7kAd0EnNZBBvQQSwkBLC3SWClhNg6JYKAW0pSSEpAKF0YSbowUEUgiQ5IA0EnwR3QAQ9iIFHcJAEEQKNMC3sjJQshdAEURRnVCyAJGB3obckaAICyNBGkYkLI0EECKyNEgwQQRpkJGghZBgiJRkeKSWpANN0kmyUQkEBMCJSEojVEQgCtqnGBIATre5AKAQIQsbc0fPdIiTZEUsjwScoTM07uVNxNhcOL4XJSztzMdrp3q7c0Hko1THeNwSvgjzicDxPowx2bE8OzVGHzn56PkRfn3HxXUOHuIqHiSibU0Uod9dh9aM9xVhiOGsqM7JGBzXaEEaFc5xHhSv4Tr34rw+5zWXvJByI56fguHkw26uPLTbYrw9HWyel0knotaB+cA0kHc8cwqNtU9lQaStjNNVj6BPZkHe08wrLhjjOj4hhy3ENYz14Xb+xTcawqlxun6ioabjtMkbo6N3eCnw/kZcd1l4nl4JnNxUCeNtw97Qmn1TGn1rrF8V8RVHA9THSYnA2odIC6GovYSNHeO/vWRr+mKUEtp6eLwNiV6k5cbNx5/wDFlLp1/wBOaDdrQfJMyV0gGY5WDxK4HWdKGP1BIjqOqafqgBUdVxHi1efn6+oeDyLzZK8sOcVeharimhpA4VOI0sVuRkF1n6/pR4dpz/On1Lh/ZNJXC3Z3klziSddSiDCeai8tXOOOrV3TLSNJ9DwuR/cZX2HuCoqzpgxye7aeOmphyyszEe0rECIb72QyAc1NzqviLus484jr9JMUqADyY7KPuVPPWVVS6808sh/TcSkEtBSesaPFTtUgsjjuUBCeaBqAdBqfBPwUVfVkCGiqJL7WYUtno11QHcjDWAcldUfAvEVbbLRGMd8hsryj6IcVmsaiqjjB5NF1P3D+axBe0IjM0eC6tRdDdC0D0momlPPXRaCg6McFpbZaIPd3uF1N5IcwrhcfWzuDYopHk/VaSt10ZYLXR8S0+I1ERgbShz2CQavcRYAe8rrNLwnSwACKjiZbT1VdYTw+0VMd4wGg32RM7vo/iT2oUUmKVfZjBaDzUuLhbr+1Wyvk/Rvote3D2RABrQETqfwWlx36nbOx4BQUv5ujhB78oJT8lKDGWZRYi1gFbPh8Ey6EKfkfTyN0pYCcC4xrYw3LFORUM7rHf7wVjyu9/wAIzh4OpKHGY26xvMMhA+i7b7x964KR7FePiKJC2u6CCYgkEEEjCyCCAQA2QKOxQsgCsPFHY96FkO4oAWRokYQBoWRI9tLIINEftQsgkYc0LabojugNQmBglGDlIPei2Qd6qCOp+FxHio0Trp5uhsqRU5rjz8yb80tjmnQ/5/z/APCYY/uGu6cabt5BNJ9pyczr4b3/AM+3zTrXBwu22vM6/wCfx8wo7ZCdN/8AP+f/AJTjDy1Pif8AP+d+9MJsZIA7+R/z/nVTIm5gS6+1x/n3qDEbjbXvCnUzM9gDr3pgnEZHQ0Uz9AcuUDvJ2+Kx7jebQ6NG3ctNxHLko2MsfnH791lmYG55jru7fyUZXtpj4nNblYB3Bd74fo/QMCw+lAsY6dgPna5+8lcQwmmNdidLTAX62ZjPYSL/AHLvhsNOQ0CyzViNDX2IvwQuoUNFfkiPeiv7UxRk96TdA7or+SCGgk3ugmHoMG3klBNhLB8Vqk41LCbaUsJg4N0YSAlAoMsIx5pKF0EX7USLZC90GVdFdBEgir+SCJBAH70Y2RE8kAUAaCARAoA9kEEEAEEEaRiujRIc0yGgiRBAKuiQAQQY0YF0SHuQQeSMhEN0ZKAJEe+6O90RKASd0kpRKSSgxFJtqlFC6QAJweaQ1OBAHzRouaCZAUSO6JBknyTUgu0hO8kkoCpqaQG5sqiqpLhwLVqHtDgoVRTBwKzyw2rHLTkXFfAz5ZjiWDSGmrWHN2dA9O8I8bGqk+TMbHo1ezs3eLB66BVUe+iyPE3CNLjUBJb1VS31JWjUFcufHv10YZuY/wAIl0slVhTH0xZEwPDJswIlvYkW5WXGnRDmuj9JdJxPJDQ4dWU09W2kkd1cjAXXBHf7FjqfgziOtd2MOkYO9+i14/646rLk7vSmyNB1OyLMwbLZ0XRJjlTrUSRwjuGqvaLoWhuDV1kjzzDVd5ImYVy4zNHNE18krrRMe8/otJXc8P6KMEpbH0TrT3u1WkouDKGmFoaGJgH6Kn+Q/wCOvOtNgWMVpHU0E5vzLbBXFH0acRVdi6JkTT9Y3XoiDAAz1Y2t8gpsWBjmEvu0/iT9uEUXQ1UPsaqucO8NFloaHogwiGxkY+Y/pErsEOCN+opceEAfRCNZU94xzWg4Awukt1WHx3HMtV5T8OsiAEdPGweDVto8LAFrKSzDBpp9yc47fSuc/TIRYIe5TIsDH1Fq48PaOSkMomg7KpxRN5Ky8eC20DAFKiwX9FaVtM0ck42Fo2CuYRP1VHFgzR9EKXDhzYiCAFZ9WByRZB7FUmiQXx35Jp8dlYOZrsmHstyTCufGo72KwlbdRZGJGxnSZgI4g4MxKjDbydUXM8HDUfeF49kaQ6xFjzHcV7qqYhLE9hFwQRZeOekTAzgHGGJUQZlj60yx/ZdqEoVZgoko73RKiEgj3RJCD3QCLkggx+9D2orI0iAIWRoIMWqUESPQboAe1Hok5xy1Rdo80gWTbW6SX66XRZfvSgLJgVu9GEENO5BAgdkAUDqEDQojZw1UvQFQr2KlxnMwH2JxOUPxu00KdBBFgblR2nTT3p0Hu3ITiTwN7En7/wDP+fFOxu9nmozTmFt07G69tr35JhPp32cDYNB2J5K1oxqSDfS9lTQakAg2V3hwJzDYka+aslJxRKPSI4wT2GX01tc7FU9E27gfAlSsfnMuIVB19bKNdCBomqRoDXewLG+tZ41XR7Sek8U0ZOoizTHws3/yuxLmXRTTZ8UrJyPzcAaD4ud+4Lph3Hcs8vVSFIrhFp3oiUjGUROiI29qCCC/uRG10V9ESABDSdboIs3igmHoMJYSLXS22AWySwUsJsbJYQCwlXSOSUNkGWCgk38EoIA7+CHLZEhdAKQRIxsghoIkaANBEggDvuiQujKDDXkj5JKPyQQxoEESFj3oAyQNESB1CAQBoBFdAbIA0EAdULoMEaK6F7oIaJC5QJNkjBEgSUWqAJEdEZOqSUwFrokDfkhdIFBLCQD3pQTBSNJ1SkFA8UR2shsgdUGSkkJVkki6CJNk29oITpAukEeCAhT04eDoqiroTYrRFvgo80IcNlOWO1S6YPFMLMtrtB8wq/5DJNxotzU0Iedk23D2j6Ky/iXOSslFgdtxdS48EaPorTtoQOScFIByTnFCvJaz0eEgW7NvYpDMMAtorsU7RySuqA5K5hE3KqpmHtH0U62iA5KwyAIsqchbRG0wHJLEAHJP5UoNTBpsQ7k4IwlAJQCYANslhqDQlgIAg0JVu4IwEYbyQCS3wRFvinLaFERogGXNTEjQpThpsmHhAQZWjVRZW+F1PlCiyjwSCC8arz1/CM4f6mtocZjZo+8EhHvb+K9EyBYPpe4e+XuC62JrM0sTeujt9Zuqmm8jnySOadeEgjwVJ0SiRlAoEEUEECg6P2lDZJBshcnZBFIZgAk2vuUbRbkkY7k7aI8neSUNUfvSAAaoIIJlBao/YgB4oAHmgeBsh7kZRIPYu9KCJBBEOFipFO67S3u1TLxql07rSW79EQXxJBsb21slZknNr3o91TM6w35XTjHa35FMMJt3ck6y5128E4E2ncMwvf3q/wAOIb1jyLFous7AdRqFd00uTDax975Y3H7kyZGsf1s7nkAZ3k6G4Oqk07fmx4klQXntt0t5KxhbZjBzssmrpXRVAW0uIzWHakjZ7gT+K3RPgsh0YMy4DUO+tUn7mtWvcs76ueCvqgTvbdEdkRugDJ/z3pNwdtEV0EACURRH70V7aoIZdbkgk5kE9G9DgpYOqSEbVqgsJXNIFkvmmCmpQSR4JSQKCMJIShqmB+aCCMWQBo0N0SANBAlBBgggggAh4IIIAbFGPJEhZAGUOWqLVBAHsgiQQCkLeCLfmjQQrdyFijQQBIXQO6CAGZAu8kLBAkIMV7IibI+SSTogATdEggdEgFwgisEAgFBK2SUd0wUEZSQe5HcoAtUChdC6AIokZRFBAPJEfJBBIyfYkOF04klMkd8QJ2SeqA5KQQN0lAM9WAiyAck8QiO6AZLfBEQO5OHXZINkGbI8ERSykEIBPsRoIeKAMJQCSClBALaEoBJCWNdLoAwNbpQ1RBGPuQA8ER5JSSTYIBBCZkGieJF00/ZARJRuo0g0UyTW6iP0QER/koVbTtqaeWFzbhzSLKwlGl7qK/RTTeK+M8HOBcTYjQFpaIpnFn2TqPiqS2q67/CGwEUfENNikbbNqozG4/pDUfcuReSIkkovFKO6T8ExsRuja0uNgEFIoXtbIQ8XaRZANdWOdylZG/VUuanyG4N2nYprJqkDQjHcEoRg7J0M79ksRgoBoRHcJbI+ZTzY+7bmnGQ62AThCjgB5AqSyiDrXYCfJOQQkHwKsIYdre5VIm1Hgw5hIvCx3sVjT4LSSevRwuPkpNNAXHvVxSwhoH1lWoVqrHB+FTDtUeUn6riEr/R5hcvqiqZfm197e9aqnZGbXA9qtoGwNbYEXPenqJ3XP3dFNNMCYsQqI/B7Af3KLUdEdU0EwYnC/wDWRlvwuuqZYPWzWO1wo07wDo+4GyfzB9Vx6r6NMegByNp5wPqS2+NlVVHCuO0TryYZUaHdgzD7l2ySW53uE090btwPCyXxDmdcTlp6iE/O08sZ/SYQmzqdOS7NK1jrh2vffVVldgeGVzD1tNHc6B7G5XD3IuBfTlwJ8Etpy6ferPG8Dkwea4d1sBNmv2t4HxVVcgeKin6kxO9U81Zvltg9YLjVlhbfcKnidqLmysJCRhVX2rXa24/xBGz/AGoH/nRpbRWsY1b4BVZHz2x25q1YCHDRZtXVejP/AGflHdUu/wClq1TzbZY/owkvhNZHzbUA+9o/ctg7W1lnfVfon2IidNVInoainggnkZljnBdGb7gGyYIJCBsi90lKt4i6I25uHvSBN0ROqBewbvb70h08DdTKwe1Mii63cUEwa2mB/PM96CDekAlBICUPNbILCUkDZLG6YLCUkA6pSAUEoHUJIRhALCA8UQRoA0d0SCACNBA6IMEEQR9yACCCCQHe43QvpZEgmBjwREoA2QQARg2RIJAd9UAUSO6ZDJ0Q3RX70L2QAQ21QuhcFAAm3JESgggxJKUdOaSggQQOmqK+iDBGkoxogDSkmyOyAUh7ULIJALIWRoIIg3RWsErXzRE8kxBIt0aF0ARCIoydUXNIElEjKJMySklKcklAJKQUspJSBs80khKd3JJumCSEEPahzQCtEoJASggFg3SwkBLG6AUEfgiQQRR0STshfRESgCITT0txTbibINHkUaRSpOajPSCNIOaiyDUqVKFFf70qbmnTnw/8scHTTRtvLSETN0103+5eWiBfde38ZomV+HT08jQ5j2FpHgQvGOP4W/BsaraCQEGCVzBfuvp9yIVVhRapTt9Uki3emkSNrspuEW6CDixpqwMHaaHs5tKkzT0Du1FHI0ncE3sqZri03BTnXXG1krAsBUwA6MKL0qK/5tV/XWPJDrz4e5LRrD0xnJiP04X0bZVvXnw9yMSkphaNxNzdiVIjxx7NnD2hUmck7IZ7aWS7JpoeKJothGfMKfDxs9g7VPE7yJCxecIw8eKe6NRv4ukCNpAfQjTukUtnSFRG2aknHk8Fc26waalDOPrFP6pfMdSb0hYa7Usqm/4QdUr+PGEyXvPM37UZXLBJ+kj6xw+knM6XxHVW8V4TJa1a0eYITjcdw940r4PeuT9Y76yV1rhzun90viOrnEqV4u2qhOn1wm31jBfLKw+RC5b1zhrdF6VINnEe1H2XxHRK4R10EkUgBa4WXP5oXU1TJA8jMxxaT3o4q+drgGyOt5o6t5kqXvJ1da59iW9n86CNxsD3Ka5xNDUjnkv94UBhIBtqpTJD6PK218zC2yBrtVH875hW7N2qnce003ureM3bG7wClbS8McTv4dZUtEedsxafIi/71ocJ4xxHHcUgw+jhHWTO3OzG83HwAWOwrBa/Hp/RsPpnzP0uQOy3xcdgF2Lgzgyn4UpHEvE9bMPnZraAfVb3D4qbDi54uqKup4cMWHsvNRtD4m83ACxb5kLjMvHmJOFgWhdxtquccc9Gz6yaTFMEYDK8l01KLDMebmePgjRsZJxnib/623kmH8VYm/8A3hwVVLC+CR0crHRyNNnMe0gg+IKQUtBYu4gxB51qX+9MvxisdvPJ71DNtURT0SQcRqifzz/ego3u9qCYe/glbpKUFRFBKB5JA70sFAKCWEgJQQC7o+SSEYQChqjCJGDdBjRpKCZFIblAHRDMgxIwfFFzRoIaCSUOSDHcIXRIIId0aSjCANBEEEGP2oIkBokB35IIItkwNBFfVC4QBoj5oXQKCFe/O6JBEUjAoighqUyBGEQRpGV7UYF0lKCYAeaNEj0SAIXRIteSZDuiO6FkXNBBeyK/tQQQYiiKNF7UARREozuiIQCTskk3KURzSUDZBSCE4kOQZBCSdkp2qTZAJQQ070AgFAowUSUEApqUCkjdKQCgUaSEEAZsiJCNJKCJcQm3pbrJtyDMvTD7J5/mmH87ICPLrzUZ4UmTZRnqaZl4DgW8iF5l6e8AGG8UMr2Msyrj7R/Sb/4XpwrlvT3w/wDKfCrqyNgMtK4SC29uaRPMZ9yQUt26SVSSUEaIIEBBFbxQQYIkaJIwuhdBBAKDrc0eba6QjQCw4eKPTvSB4pQCCGEYCKyW0X3SAgxE+zdOadA1so7jckplOgzHvR5ja90lGBe6DASEkAusL6qfW4ZPRjOHdbHuXAbKtstlSt9Mwunk3uwAjy0KeM2nK6ZWN9iD3J4vLjcndPYjhrqdzpIxcDcKGx+109aG0i+ifgfqAdjoojXX/BORPykDexQaI/T/AAlaDAKympJ6eorKJlfCy4dA95aHd2o7lRVDbTSiw3uDdTsNdngc3mDcKTd74R404fxOKOho42YbJs2mc0MDj+iRoT961B+C83QG7bXXTej7jmWpqG4LisueUj8mmcdXaeo49/cUWHK6GkTzRU8L5ppGRxsGZz3mwA8SimnjgifNK8MjjaXvc7ZoGpJXD+NON6jierdHE98WHRn5qLbP+k7vPhyUm0/GHHXDFeXwMwlmKygECd46to8nesVzPkERcSiJPJAHfXmkknvQue5EQSEAkm5QQI11ugmT6AgpWwSdEaoimlLCQEpqDLCUCkhKQRXJKSAlXQCroAot0YQCgULogUaAO9kSG6NMxFGiQuggR8kESDGhdEgghoIXQ5oAIXQNkCgAhdEggFAobokEGFkAh4oIIECiQQARG2yMlJJQYIIXQvoghoAohdHud0ApDmiCNBjG6CCF/YggJshdEhZAApN0eySgUaCCJBAklKvuklAgkR5JSSUGIpJSiklBElIJ9yUUkoUQbXSUopN0AndBC6AKAMJbUkIxZALBR3SQUYJ80Au6K6HNC6CC6Io0XJBm3apB8068pp2osgGXpiTZPyJh+qVCPJeyjv8AFSHqO9BmXKr4iw9mKYNVUrxdsjC2x8QrNyQ5uZpadbiygPEWLUMmG4nVUcgIdDI5hv4FQrLo3TfgBwji59SxhEVW3N/iG65yQriaSdERRlEUEJAlBBABEjRW0QYIIIJALoIuaO6DKbq5LATYNinQbJEAS2pHgljyTGj0YFwokoyyvHcVKYbEJisFpr/WAKAZ33QvqghqgwO62PDUcnyOwPblu9xYTzasvh9G6vrIadt+2bE9w5ldBDWRxtia2zGANaLaAKsYzzvWlbU0981gDfUrNV9AYXF7RZhOoHIrXyx2uN+arqinGotdpBv4qrNoxumUa63mnGnUbqRiGHvp7SNBLO/wURjgQpa7OVI7bH6dpttu5Lwt+SoLNNQQkyduDvLTdMxydVUMeORHKymnF9A7LJz1V3Q4U/EMPq6uhc5uIYblqWhm74uZHi02PldUV7OuFouEMW+SeIaOdxAjkPUyd2V+mvtsqhVpOO+MmYhwfhjIJGh+JtzzNadmt0cP2vgua5mNAut1xTwbS4RiLnwQBtPOS+PuaebfZy8FBp8Npi0h0LblZ3q6VO4yXXMO1z7EbSXus1hJ8AtKMKihkJDG+VkGU8ULy4saPYls2aeJBvG4W8EOqqMod1TrHY2WtMcU4t1bQD3BE6BuYdnst020RsaZZtBVSNzBgF+9BavqYxawKCNh7MHilApA1RrRJYKWCmwUsIBYRg6pIR3QZxuyMHVICUEAq6NJR3QRWyMFJugmC7gaoXSboBAKQQRXQY0EV0aQBGisggDRI72RXTAIIIIA0SCCANDvRIIAwgiQQWgRXRoie5AEiRlEgDQsgShdA0AQsgEEAYRgk8kVyhzQCifBC+wCShcoIq6LMiujBCAF/BEULojsg6F0V/BAHvRIIZsLouaCCAGySUZOlkW6AIpBKUdAkEoOCKQUpJKDJO3ekoyi5oAighyRXCAO/ejRBHdAKCUNEm6MIBSO6SChdAHdEdELoiUATim3FKOibcUA28ph6fcUw7VAR37KPIpMijvGqmmZcE2SQU45NlIOR/wgMA9OwEV7GXfSuD7+HNecSD3L2lxbhbMYwOppntBD2Fpv4heN8Ron4fXVFJILPhkcw+wpwqhlEUo/ciPJNJJRWSiiKAK1kLI7e5BBiRFGgUGIot0dkBokATrNWhNbJxh7KAUlN28UkpQPckUONOqKuFxG/wAwgw3KVUjNT/ZKYQke6JLYx0jgxjS5x2AQa04ZcW4tHbm1wPuWzJdlGunLW6z+B4e2gBmlLXTOFtNQ0dyuw+4F91pj4wzu6UQMpFyABbzTEjDqXXuQntRbMWnuSXAEabW0CpG1fLEMrswzMI1Flm8SoH4bMw2+YmBdG7yNiPYtdJGS2w2Peq/FIH1eHuowMxa/rIvB3Me0fAKMo1wyZ6I3u3kdCo72kNIIN2lKjcQcjgQ4aapUgGe/JwU1fizpZOtpY3720KmxXfHbZVGEyW6yE+YVpA6xyogdjogOLuD4XnWpEdwe6VmhHt/FYhjXGQ5Ta24Vx0V4t1dVUYW8iz/n4x4jRw91im+I6I0OMVjYhYdYXADuOv4o5JubLC6ukB7C5t2uueajvpS9xcddNVIitoCbXTpjsbrGVqrGN6m9j2D4bKSbuhszUlIDHCd12fNnn3Jl0zoJib/MhMH2U7sou6x7kE82oa9ocHCx20QQHr8OPglXNkEFqgbXHVLDjZBBMywdEA4lBBALDilZjcIIIBV0AdUEEAq6F0EEiAkgpV+SCCDFdBBBMhg6oySgglQLMUeYoIIMV0LoIIA8xsUMxQQTAZiiDiggkB31QuggghZihmQQQYXQuggghX0QuggmQDVAlBBIx3QuggmKF0AgggASjQQQBE6IX0QQQQr6oE6IIIOiuiJQQQUC+yIlBBAF3oroIIEJJ1SCUEEHBEpJKCCQJJSCUEEwLMULoIIMAdUq9kEEEAOyVmKCCDHmKBdqgggCLjZFdBBBEuKQ4oIIOGnahMPPwQQQDL3HVMSGx9qCCRmXFNk2KCCmgUjQ+JzTsQvJvS5RQ0fGVUIWlokAe7zQQTg/TEWuLoiBZBBCRW0CIhBBBisiQQQBFGUEEgCCCCABFkqPYoII/QOAIxuUEEEWNE44B1NJf6t0EEwgKbhI/KHHmGoIJT0svGjivlGvK6sICbAoILWMafDRZ3hqnHRtubaWQQVEZfGMp8FEqIxc76WQQUrnrO8QU0cNe17AQZGB7vNRHNBiB5hyCCzahSdmvZbna6uGsAeN90EEQVdYBUSUGOYfUQOs8TsbrzBNiPcVu+LGAY/Ui2lmfBBBVf8AFM/yUEsYa/S4sVKiYHRgnuQQXPGp3qWFhbbQhVstOyxbbS6CCcIw6BjXEC4AQQQVB//Z" style="width:100%;height:100%;object-fit:cover;object-position:center top;display:block;" alt="Angela Leng" />
        </div>
        <!-- Floating cards -->
        <div class="about-float-card card-1">
          <div class="float-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="18" height="18"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><polyline points="22 4 12 14.01 9 11.01"/></svg>
          </div>
          <div>
            <div class="float-label">Especialización</div>
            <div class="float-value">Sector Agro · Perú</div>
          </div>
        </div>
        <div class="about-float-card card-2">
          <div class="float-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="18" height="18"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
          </div>
          <div>
            <div class="float-label">Disponibilidad</div>
            <div class="float-value">Inmediata · Remoto</div>
          </div>
        </div>
      </div>

      <!-- Content -->
      <div class="about-content reveal reveal-delay-2">
        <div class="section-tag">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>
          Sobre mí
        </div>
        <h2 class="section-title">Contadora con corazón<br>de intrapreneur</h2>
        <p class="about-intro">
          Soy <strong>Angela Leng</strong>, contadora con enfoque en talento humano, apasionada por la organización, la mejora de procesos y la gestión eficiente del talento. Disfruto trabajar en entornos dinámicos donde puedo aportar <strong>orden, estructura y soluciones</strong> que generen impacto real.
        </p>
        <p class="about-intro" style="margin-top:-.8rem;">
          Me caracterizo por ser proactiva, detallista, optimista y con fuerte orientación a resultados. Creo en el trabajo en equipo, la comunicación clara y en la <strong>mejora continua</strong> como base para construir organizaciones más eficientes y humanas.
        </p>

        <!-- Timeline -->
        <div class="timeline">

          <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-period">Ago 2024 – Presente</div>
            <div class="timeline-company">Inka Select Fruit</div>
            <div class="timeline-role">Analista Contable y de RRHH</div>
            <div class="timeline-loc">🇵🇪 Lima, Perú</div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-period">Ene 2022 – Jul 2024</div>
            <div class="timeline-company">Fission Lab</div>
            <div class="timeline-role">Asistente · Inteligencia Comercial</div>
            <div class="timeline-loc">🇵🇪 Perú</div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-period">Nov 2018 – Dic 2021</div>
            <div class="timeline-company">Fission Lab</div>
            <div class="timeline-role">Asistente · Contabilidad</div>
            <div class="timeline-loc">🇵🇪 Lima, Perú</div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-period">May 2018 – Oct 2018</div>
            <div class="timeline-company">PROCAMPO S.A.</div>
            <div class="timeline-role">Asistente de Contabilidad y Auditoría</div>
            <div class="timeline-loc">🇵🇪 Lima, Perú</div>
          </div>

        </div>

        <!-- Educación -->
        <div class="certs-title">🎓 Educación</div>
        <div class="certs-grid" style="margin-bottom:1rem;">
          <span class="cert-badge">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="12" height="12"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/></svg>
            CENTRUM PUCP
          </span>
          <span class="cert-badge">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="12" height="12"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/></svg>
            Univ. Inca Garcilaso
          </span>
          <span class="cert-badge">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="12" height="12"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
            Denver Community College
          </span>
        </div>

        <!-- Certificaciones -->
        <div class="certs-title">📜 Certificaciones</div>
        <div class="certs-grid">
          <span class="cert-badge"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="12" height="12"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>Google AI Essentials</span>
          <span class="cert-badge"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="12" height="12"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>Maximize Productivity AI</span>
          <span class="cert-badge"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="12" height="12"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>Introduction to AI</span>
          <span class="cert-badge"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="12" height="12"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>Accountability & Engagement</span>
          <span class="cert-badge"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="12" height="12"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>Value Creation</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════
     VALORES
═══════════════════════════════ -->
<section id="valores">
  <!-- Decorative top wave -->
  <svg viewBox="0 0 1440 60" preserveAspectRatio="none" style="display:block;width:100%;height:60px;margin-bottom:-2px;" fill="none">
    <path d="M0,30 C360,60 720,0 1080,30 C1260,45 1380,20 1440,10 L1440,0 L0,0 Z" fill="#FAFAF5"/>
  </svg>

  <div class="container" style="padding-top:1rem;padding-bottom:1rem;">
    <div style="text-align:center;margin-bottom:3rem;">
      <div class="section-tag" style="background:rgba(255,255,255,.1);color:var(--matcha-pale);">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="14" height="14"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/></svg>
        Mi forma de trabajar
      </div>
      <h2 class="section-title" style="color:var(--white);">Lo que me define como<br>profesional</h2>
    </div>

    <div class="valores-inner">
      <div class="valor-card reveal">
        <div class="valor-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
        </div>
        <div class="valor-title">Proactividad</div>
        <p class="valor-desc">Anticipo necesidades y propongo soluciones antes de que los problemas escalen.</p>
      </div>
      <div class="valor-card reveal reveal-delay-1">
        <div class="valor-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>
        </div>
        <div class="valor-title">Detallismo</div>
        <p class="valor-desc">La precisión en los números y en la gestión de personas marca la diferencia.</p>
      </div>
      <div class="valor-card reveal reveal-delay-2">
        <div class="valor-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
        </div>
        <div class="valor-title">Trabajo en equipo</div>
        <p class="valor-desc">Construyo relaciones de confianza y comunicación clara dentro de cada organización.</p>
      </div>
      <div class="valor-card reveal reveal-delay-3">
        <div class="valor-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="23 6 13.5 15.5 8.5 10.5 1 18"/><polyline points="17 6 23 6 23 12"/></svg>
        </div>
        <div class="valor-title">Orientación a resultados</div>
        <p class="valor-desc">Cada proceso que diseño tiene un impacto medible en la operación y las personas.</p>
      </div>
    </div>
  </div>

  <!-- Bottom wave -->
  <svg viewBox="0 0 1440 60" preserveAspectRatio="none" style="display:block;width:100%;height:60px;margin-top:-2px;" fill="none">
    <path d="M0,10 C360,50 720,0 1080,30 C1260,50 1380,40 1440,50 L1440,60 L0,60 Z" fill="#F4F1E8"/>
  </svg>
</section>

<!-- ═══════════════════════════════
     CONTACTO
═══════════════════════════════ -->
<section id="contacto">
  <div class="container">
    <div style="text-align:center;margin-bottom:3.5rem;" class="reveal">
      <div class="section-tag">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Contacto
      </div>
      <h2 class="section-title">¿Listo para dar el siguiente paso?</h2>
      <p class="section-subtitle" style="margin:0 auto;">Cuéntame sobre tu empresa y conversemos cómo puedo ser tu Business Partner estratégico.</p>
    </div>

    <div class="contact-grid">
      <!-- Info side -->
      <div class="reveal">
        <h3 style="font-family:'Playfair Display',serif;color:var(--matcha-dark);font-size:1.4rem;margin-bottom:1.5rem;">Conectemos directamente</h3>

        <div class="contact-item">
          <div class="contact-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          </div>
          <div>
            <div class="contact-item-label">Email</div>
            <div class="contact-item-value">angelaleng17@gmail.com</div>
          </div>
        </div>

        <div class="contact-item">
          <div class="contact-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          </div>
          <div>
            <div class="contact-item-label">LinkedIn</div>
            <div class="contact-item-value">linkedin.com/in/angelaleng</div>
          </div>
        </div>

        <div class="contact-item">
          <div class="contact-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
          </div>
          <div>
            <div class="contact-item-label">Ubicación</div>
            <div class="contact-item-value">Lima, Perú · Remoto disponible</div>
          </div>
        </div>

        <div class="contact-item">
          <div class="contact-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
          </div>
          <div>
            <div class="contact-item-label">Idiomas de trabajo</div>
            <div class="contact-item-value">Español · English · Português</div>
          </div>
        </div>

        <!-- Specialization box -->
        <div style="background:var(--matcha-pale);border-radius:var(--radius);padding:1.5rem;margin-top:1rem;border-left:4px solid var(--matcha);">
          <div style="font-size:.78rem;font-weight:700;text-transform:uppercase;letter-spacing:.06em;color:var(--matcha);margin-bottom:.5rem;">🌿 Sector Especializado</div>
          <p style="font-size:.88rem;color:var(--matcha-dark);line-height:1.6;">Agroindustria, agroexportación y empresas del sector primario en Perú. Experiencia directa en empresas como <strong>Inka Select Fruit</strong> y <strong>PROCAMPO S.A.</strong></p>
        </div>
      </div>

      <!-- Form side -->
      <div class="reveal reveal-delay-2">
        <div class="contact-form-card">
          <div id="form-container">
            <div class="form-title">Envíame un mensaje</div>
            <p class="form-subtitle">Respondo en menos de 24 horas 🌿</p>

            <form id="contact-form" novalidate>
              <div class="form-row">
                <div class="form-group">
                  <label for="nombre">Nombre *</label>
                  <input type="text" id="nombre" placeholder="Tu nombre" required />
                </div>
                <div class="form-group">
                  <label for="empresa">Empresa</label>
                  <input type="text" id="empresa" placeholder="Tu empresa" />
                </div>
              </div>

              <div class="form-group">
                <label for="email">Email *</label>
                <input type="email" id="email" placeholder="tu@email.com" required />
              </div>

              <div class="form-group">
                <label for="servicio">Servicio de interés</label>
                <select id="servicio">
                  <option value="">Selecciona un servicio...</option>
                  <option value="business-partner">Business Partner Estratégico</option>
                  <option value="contable">Business Partner Contable</option>
                  <option value="rrhh">Business Partner de RRHH</option>
                  <option value="inteligencia">Inteligencia Comercial</option>
                  <option value="ia">Productividad con IA</option>
                  <option value="consultoria">Consultoría Integral Agro</option>
                </select>
              </div>

              <div class="form-group">
                <label for="mensaje">Mensaje *</label>
                <textarea id="mensaje" placeholder="Cuéntame sobre tu empresa y lo que necesitas..." required></textarea>
              </div>

              <button type="submit" class="btn-submit">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="18" height="18"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
                Enviar mensaje
              </button>
            </form>
          </div>

          <!-- Success state -->
          <div class="form-success" id="form-success">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" style="display:block;margin:0 auto .8rem;">
              <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/>
              <polyline points="22 4 12 14.01 9 11.01"/>
            </svg>
            <h4>¡Mensaje enviado! 🌿</h4>
            <p>Gracias por escribirme. Te responderé muy pronto.</p>
            <button onclick="resetForm()" class="btn btn-outline" style="margin-top:1rem;font-size:.85rem;">Enviar otro mensaje</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════
     FOOTER
═══════════════════════════════ -->
<footer>
  <div class="container">
    <div class="footer-grid">
      <!-- Brand -->
      <div>
        <div class="footer-brand-name">Angela Leng</div>
        <p class="footer-brand-desc">Business Partner Contable & RRHH para el sector agroindustrial del Perú. Estrategia, orden y talento humano.</p>
        <div class="footer-socials">
          <!-- LinkedIn -->
          <a href="https://www.linkedin.com/in/angelaleng/" target="_blank" class="footer-social" aria-label="LinkedIn">
            <svg viewBox="0 0 24 24" fill="currentColor" width="16" height="16"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          </a>
          <!-- Email -->
          <a href="mailto:angelaleng17@gmail.com" class="footer-social" aria-label="Email">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="16" height="16"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          </a>
        </div>
      </div>

      <!-- Links -->
      <div>
        <div class="footer-col-title">Servicios</div>
        <nav class="footer-links">
          <a href="#servicios">Business Partner Estratégico</a>
          <a href="#servicios">Contabilidad</a>
          <a href="#servicios">Recursos Humanos</a>
          <a href="#servicios">Inteligencia Comercial</a>
          <a href="#servicios">Productividad con IA</a>
        </nav>
      </div>

      <!-- Quick links -->
      <div>
        <div class="footer-col-title">Navegación</div>
        <nav class="footer-links">
          <a href="#inicio">Inicio</a>
          <a href="#sobre-mi">Sobre mí</a>
          <a href="#valores">Valores</a>
          <a href="#contacto">Contacto</a>
          <a href="https://www.linkedin.com/in/angelaleng/" target="_blank">LinkedIn</a>
        </nav>
      </div>
    </div>

    <div class="footer-bottom">
      <div class="footer-copy">© 2026 Angela Leng · Todos los derechos reservados</div>
      <div class="footer-flag">
        <svg viewBox="0 0 20 14" width="20"><rect width="7" height="14" fill="#D91023"/><rect x="7" width="6" height="14" fill="#F5F5F5"/><rect x="13" width="7" height="14" fill="#D91023"/></svg>
        Hecho con 🌿 en Lima, Perú
      </div>
    </div>
  </div>
</footer>

<!-- Back to top -->
<button id="back-top" aria-label="Volver arriba">
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="18 15 12 9 6 15"/></svg>
</button>

<!-- ═══════════════════════════════
     JAVASCRIPT
═══════════════════════════════ -->
<script>
  /* ── Navbar scroll ── */
  const navbar = document.getElementById('navbar');
  const progressBar = document.getElementById('progress-bar');
  const backTop = document.getElementById('back-top');

  window.addEventListener('scroll', () => {
    const scrolled = window.scrollY;
    const total = document.body.scrollHeight - window.innerHeight;
    const pct = total > 0 ? (scrolled / total) * 100 : 0;

    progressBar.style.width = pct + '%';
    navbar.classList.toggle('scrolled', scrolled > 50);
    backTop.classList.toggle('show', scrolled > 400);
  });

  backTop.addEventListener('click', () => {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  });

  /* ── Hamburger ── */
  const hamburger = document.getElementById('hamburger');
  const mobileMenu = document.getElementById('mobile-menu');
  const mobileClose = document.getElementById('mobile-close');
  const mobileLinks = document.querySelectorAll('.mobile-link');

  hamburger.addEventListener('click', () => {
    hamburger.classList.toggle('open');
    mobileMenu.classList.toggle('open');
    document.body.style.overflow = mobileMenu.classList.contains('open') ? 'hidden' : '';
  });
  const closeMenu = () => {
    hamburger.classList.remove('open');
    mobileMenu.classList.remove('open');
    document.body.style.overflow = '';
  };
  mobileClose.addEventListener('click', closeMenu);
  mobileLinks.forEach(l => l.addEventListener('click', closeMenu));

  /* ── Scroll reveal ── */
  const revealEls = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        observer.unobserve(e.target);
      }
    });
  }, { threshold: 0.12 });
  revealEls.forEach(el => observer.observe(el));

  /* ── Active nav link ── */
  const sections = document.querySelectorAll('section[id], div[id="inicio"]');
  const navAnchors = document.querySelectorAll('.nav-links a');

  const sectionObserver = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        const id = e.target.getAttribute('id');
        navAnchors.forEach(a => {
          a.style.color = a.getAttribute('href') === '#' + id
            ? 'var(--matcha)' : '';
        });
      }
    });
  }, { threshold: 0.4 });
  document.querySelectorAll('section[id]').forEach(s => sectionObserver.observe(s));

  /* ── Contact form ── */
  document.getElementById('contact-form').addEventListener('submit', function(e) {
    e.preventDefault();
    const nombre  = document.getElementById('nombre').value.trim();
    const emailV  = document.getElementById('email').value.trim();
    const mensaje = document.getElementById('mensaje').value.trim();

    if (!nombre || !emailV || !mensaje) {
      // Shake invalid fields
      [['nombre', nombre], ['email', emailV], ['mensaje', mensaje]].forEach(([id, val]) => {
        if (!val) {
          const el = document.getElementById(id);
          el.style.borderColor = '#e05252';
          el.style.animation = 'shake .3s ease';
          setTimeout(() => { el.style.animation = ''; }, 400);
        }
      });
      return;
    }

    // Show success
    document.getElementById('form-container').style.display = 'none';
    document.getElementById('form-success').style.display = 'block';
  });

  function resetForm() {
    document.getElementById('contact-form').reset();
    document.getElementById('form-container').style.display = 'block';
    document.getElementById('form-success').style.display = 'none';
  }

  /* ── Shake keyframe (injected) ── */
  const style = document.createElement('style');
  style.textContent = `
    @keyframes shake {
      0%,100%{transform:translateX(0)}
      20%{transform:translateX(-6px)}
      60%{transform:translateX(6px)}
    }
  `;
  document.head.appendChild(style);
</script>

</body>
</html>
