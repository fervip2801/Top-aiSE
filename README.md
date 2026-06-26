<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Compramos tu Casa y Departamento | Grupo AISE Real Estate</title>
  <meta name="description" content="Vende tu propiedad rápido, fácil y seguro con Grupo AISE. Recibe una oferta sin compromiso o publica gratis en Durango, México." />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />
  <style>
    /* ─── TOKENS ─────────────────────────────────────────── */
    :root {
      --navy:        #0B1F3A;
      --navy-mid:    #122848;
      --navy-light:  #1A3560;
      --gold:        #C9A84C;
      --gold-light:  #E2C47A;
      --gold-pale:   #F7EDD0;
      --emerald:     #1A7A5E;
      --emerald-mid: #22997A;
      --emerald-pale:#E6F4EF;
      --white:       #FFFFFF;
      --off-white:   #F8F6F1;
      --gray-100:    #F2F2F2;
      --gray-300:    #D1D1D1;
      --gray-600:    #6B6B6B;
      --gray-800:    #2A2A2A;
    }

    /* ─── RESET ──────────────────────────────────────────── */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      font-family: 'Inter', sans-serif;
      background: var(--white);
      color: var(--gray-800);
      line-height: 1.6;
    }
    img { display: block; max-width: 100%; }
    a { color: inherit; text-decoration: none; }
    button { cursor: pointer; border: none; background: none; font-family: inherit; }

    /* ─── NAV ────────────────────────────────────────────── */
    .nav {
      position: sticky;
      top: 0;
      z-index: 100;
      background: var(--navy);
      border-bottom: 2px solid var(--gold);
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 5%;
      height: 68px;
    }
    .nav-logo {
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .nav-logo-mark {
      width: 38px;
      height: 38px;
      background: var(--gold);
      border-radius: 6px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Playfair Display', serif;
      font-size: 18px;
      font-weight: 900;
      color: var(--navy);
    }
    .nav-logo-text {
      display: flex;
      flex-direction: column;
      line-height: 1.15;
    }
    .nav-logo-text span:first-child {
      font-family: 'Playfair Display', serif;
      font-size: 15px;
      font-weight: 700;
      color: var(--white);
      letter-spacing: 0.05em;
    }
    .nav-logo-text span:last-child {
      font-size: 10px;
      font-weight: 300;
      color: var(--gold-light);
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }
    .nav-links {
      display: flex;
      gap: 28px;
      list-style: none;
    }
    .nav-links a {
      font-size: 13px;
      font-weight: 500;
      color: rgba(255,255,255,0.75);
      letter-spacing: 0.04em;
      transition: color .2s;
    }
    .nav-links a:hover, .nav-links a.active { color: var(--gold-light); }
    .nav-cta {
      background: var(--gold);
      color: var(--navy) !important;
      font-weight: 600 !important;
      padding: 8px 20px;
      border-radius: 4px;
      transition: background .2s !important;
    }
    .nav-cta:hover { background: var(--gold-light) !important; color: var(--navy) !important; }

    /* ─── HERO ───────────────────────────────────────────── */
    .hero {
      background: var(--navy);
      position: relative;
      overflow: hidden;
      padding: 90px 5% 80px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: center;
    }
    .hero::before {
      content: '';
      position: absolute;
      inset: 0;
      background:
        radial-gradient(ellipse 60% 80% at 80% 50%, rgba(201,168,76,0.08) 0%, transparent 70%),
        radial-gradient(ellipse 40% 60% at 10% 80%, rgba(26,122,94,0.06) 0%, transparent 60%);
    }
    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(201,168,76,0.12);
      border: 1px solid rgba(201,168,76,0.3);
      color: var(--gold-light);
      font-size: 11px;
      font-weight: 600;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      padding: 6px 14px;
      border-radius: 20px;
      margin-bottom: 24px;
    }
    .hero-badge::before { content: '●'; font-size: 8px; color: var(--emerald-mid); }
    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(32px, 4vw, 54px);
      font-weight: 900;
      color: var(--white);
      line-height: 1.1;
      margin-bottom: 20px;
    }
    .hero h1 em {
      font-style: normal;
      color: var(--gold);
    }
    .hero-sub {
      font-size: 16px;
      color: rgba(255,255,255,0.65);
      max-width: 480px;
      margin-bottom: 36px;
      line-height: 1.7;
    }
    .hero-ctas {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }
    .btn-primary {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--gold);
      color: var(--navy);
      font-weight: 700;
      font-size: 14px;
      padding: 14px 28px;
      border-radius: 5px;
      letter-spacing: 0.02em;
      transition: background .2s, transform .15s;
    }
    .btn-primary:hover { background: var(--gold-light); transform: translateY(-1px); }
    .btn-secondary {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: transparent;
      color: var(--white);
      font-weight: 600;
      font-size: 14px;
      padding: 14px 28px;
      border-radius: 5px;
      border: 1.5px solid rgba(255,255,255,0.3);
      transition: border-color .2s, background .2s;
    }
    .btn-secondary:hover { border-color: var(--gold); background: rgba(201,168,76,0.07); }
    .hero-visual {
      position: relative;
      display: flex;
      justify-content: center;
    }
    .hero-card-stack {
      position: relative;
      width: 100%;
      max-width: 420px;
    }
    .hero-card {
      background: var(--navy-mid);
      border: 1px solid rgba(201,168,76,0.2);
      border-radius: 14px;
      padding: 28px;
      position: relative;
    }
    .hero-card-label {
      font-size: 10px;
      font-weight: 700;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 10px;
    }
    .hero-card h3 {
      font-family: 'Playfair Display', serif;
      font-size: 20px;
      color: var(--white);
      margin-bottom: 6px;
    }
    .hero-card p {
      font-size: 13px;
      color: rgba(255,255,255,0.55);
    }
    .hero-stat-row {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 1px;
      margin-top: 18px;
      background: rgba(201,168,76,0.15);
      border-radius: 8px;
      overflow: hidden;
    }
    .hero-stat {
      background: var(--navy-light);
      padding: 14px 10px;
      text-align: center;
    }
    .hero-stat strong {
      display: block;
      font-family: 'Playfair Display', serif;
      font-size: 22px;
      color: var(--gold);
    }
    .hero-stat span {
      font-size: 10px;
      color: rgba(255,255,255,0.5);
      letter-spacing: 0.06em;
    }
    .hero-floating-tag {
      position: absolute;
      top: -14px;
      right: 20px;
      background: var(--emerald);
      color: var(--white);
      font-size: 11px;
      font-weight: 700;
      padding: 6px 14px;
      border-radius: 20px;
      letter-spacing: 0.06em;
    }

    /* ─── SECTION SHARED ─────────────────────────────────── */
    section { padding: 80px 5%; }
    .section-eyebrow {
      font-size: 11px;
      font-weight: 700;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 12px;
    }
    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(26px, 3vw, 40px);
      font-weight: 900;
      color: var(--navy);
      line-height: 1.15;
      margin-bottom: 16px;
    }
    .section-title em { font-style: normal; color: var(--emerald); }
    .section-sub {
      font-size: 15px;
      color: var(--gray-600);
      max-width: 560px;
      line-height: 1.7;
    }
    .section-header { margin-bottom: 56px; }
    .section-header.center { text-align: center; }
    .section-header.center .section-sub { margin: 0 auto; }
    .divider-gold {
      width: 48px;
      height: 3px;
      background: var(--gold);
      border-radius: 2px;
      margin-bottom: 20px;
    }
    .center .divider-gold { margin-left: auto; margin-right: auto; }

    /* ─── 3 OPTIONS ──────────────────────────────────────── */
    .options { background: var(--off-white); }
    .options-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
    }
    .option-card {
      background: var(--white);
      border-radius: 14px;
      overflow: hidden;
      border: 1px solid var(--gray-300);
      transition: box-shadow .25s, transform .2s;
      display: flex;
      flex-direction: column;
    }
    .option-card:hover {
      box-shadow: 0 12px 40px rgba(11,31,58,0.12);
      transform: translateY(-4px);
    }
    .option-card.featured {
      border: 2px solid var(--emerald);
    }
    .option-img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      background: var(--navy-mid);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 56px;
    }
    .option-tag {
      font-size: 10px;
      font-weight: 700;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      padding: 4px 10px;
      border-radius: 3px;
      display: inline-block;
      margin-bottom: 12px;
    }
    .tag-fast  { background: rgba(201,168,76,0.15);  color: var(--gold); }
    .tag-safe  { background: rgba(26,122,94,0.12);   color: var(--emerald); }
    .tag-easy  { background: rgba(11,31,58,0.08);    color: var(--navy); }
    .option-body { padding: 28px; flex: 1; display: flex; flex-direction: column; }
    .option-body h3 {
      font-family: 'Playfair Display', serif;
      font-size: 20px;
      color: var(--navy);
      margin-bottom: 10px;
      line-height: 1.25;
    }
    .option-body p {
      font-size: 14px;
      color: var(--gray-600);
      line-height: 1.7;
      flex: 1;
      margin-bottom: 24px;
    }
    .btn-option-primary {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      background: var(--emerald);
      color: var(--white);
      font-weight: 600;
      font-size: 13px;
      padding: 13px;
      border-radius: 6px;
      transition: background .2s;
    }
    .btn-option-primary:hover { background: var(--emerald-mid); }
    .btn-option-secondary {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      background: transparent;
      color: var(--navy);
      font-weight: 600;
      font-size: 13px;
      padding: 12px;
      border-radius: 6px;
      border: 1.5px solid var(--navy);
      transition: background .2s, color .2s;
    }
    .btn-option-secondary:hover { background: var(--navy); color: var(--white); }
    .btn-option-gold {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      background: var(--gold);
      color: var(--navy);
      font-weight: 700;
      font-size: 13px;
      padding: 13px;
      border-radius: 6px;
      transition: background .2s;
    }
    .btn-option-gold:hover { background: var(--gold-light); }

    /* ─── PROCESO PASOS ──────────────────────────────────── */
    .proceso { background: var(--navy); }
    .proceso .section-title { color: var(--white); }
    .proceso .section-sub   { color: rgba(255,255,255,0.55); }
    .proceso .section-eyebrow { color: var(--gold-light); }

    .steps-container {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 40px;
      align-items: start;
    }
    .steps-nav {
      display: flex;
      flex-direction: column;
      gap: 6px;
    }
    .step-tab {
      display: flex;
      align-items: center;
      gap: 16px;
      padding: 18px 20px;
      border-radius: 10px;
      cursor: pointer;
      transition: background .2s;
      border: 1px solid transparent;
    }
    .step-tab:hover { background: rgba(255,255,255,0.05); }
    .step-tab.active {
      background: rgba(201,168,76,0.08);
      border-color: rgba(201,168,76,0.25);
    }
    .step-number {
      width: 38px;
      height: 38px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Playfair Display', serif;
      font-size: 16px;
      font-weight: 700;
      flex-shrink: 0;
      background: rgba(255,255,255,0.08);
      color: rgba(255,255,255,0.4);
      transition: background .2s, color .2s;
    }
    .step-tab.active .step-number {
      background: var(--gold);
      color: var(--navy);
    }
    .step-tab-text span {
      display: block;
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: rgba(255,255,255,0.35);
      margin-bottom: 2px;
    }
    .step-tab-text strong {
      font-size: 14px;
      color: rgba(255,255,255,0.55);
      font-weight: 500;
    }
    .step-tab.active .step-tab-text strong { color: var(--white); }

    .step-panel { display: none; }
    .step-panel.active { display: block; }
    .step-panel-inner {
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(201,168,76,0.18);
      border-radius: 16px;
      padding: 40px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 36px;
      align-items: center;
    }
    .step-panel h3 {
      font-family: 'Playfair Display', serif;
      font-size: 26px;
      color: var(--white);
      margin-bottom: 14px;
    }
    .step-panel p {
      font-size: 14px;
      color: rgba(255,255,255,0.6);
      line-height: 1.8;
      margin-bottom: 16px;
    }
    .step-checklist {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    .step-checklist li {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      font-size: 13px;
      color: rgba(255,255,255,0.65);
    }
    .step-checklist li::before {
      content: '✓';
      width: 20px;
      height: 20px;
      background: var(--emerald);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 10px;
      color: var(--white);
      font-weight: 700;
      flex-shrink: 0;
      margin-top: 1px;
    }
    .step-visual {
      background: var(--navy-light);
      border-radius: 12px;
      height: 240px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 80px;
      border: 1px solid rgba(201,168,76,0.1);
    }

    /* ─── FAQ ────────────────────────────────────────────── */
    .faq { background: var(--white); }
    .faq-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
      max-width: 960px;
      margin: 0 auto;
    }
    .faq-item {
      background: var(--off-white);
      border-radius: 10px;
      overflow: hidden;
      border: 1px solid var(--gray-300);
    }
    .faq-question {
      width: 100%;
      text-align: left;
      padding: 20px 24px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      font-size: 14px;
      font-weight: 600;
      color: var(--navy);
      cursor: pointer;
      transition: background .2s;
      font-family: 'Inter', sans-serif;
    }
    .faq-question:hover { background: rgba(11,31,58,0.04); }
    .faq-question.open { color: var(--emerald); }
    .faq-icon {
      width: 24px;
      height: 24px;
      border-radius: 50%;
      background: var(--navy);
      color: var(--white);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 16px;
      flex-shrink: 0;
      transition: background .2s, transform .3s;
    }
    .faq-question.open .faq-icon {
      background: var(--emerald);
      transform: rotate(45deg);
    }
    .faq-answer {
      max-height: 0;
      overflow: hidden;
      transition: max-height .35s ease;
    }
    .faq-answer.open { max-height: 300px; }
    .faq-answer p {
      padding: 0 24px 20px;
      font-size: 14px;
      color: var(--gray-600);
      line-height: 1.75;
    }

    /* ─── CONTACTO CTA ───────────────────────────────────── */
    .cta-banner {
      background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%);
      padding: 80px 5%;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    .cta-banner::before {
      content: '';
      position: absolute;
      inset: 0;
      background: radial-gradient(ellipse 70% 70% at 50% 50%, rgba(201,168,76,0.06) 0%, transparent 70%);
    }
    .cta-banner h2 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(28px, 3.5vw, 46px);
      color: var(--white);
      margin-bottom: 16px;
      position: relative;
    }
    .cta-banner h2 span { color: var(--gold); }
    .cta-banner p {
      font-size: 15px;
      color: rgba(255,255,255,0.6);
      max-width: 520px;
      margin: 0 auto 36px;
      line-height: 1.7;
      position: relative;
    }
    .cta-buttons {
      display: flex;
      gap: 16px;
      justify-content: center;
      flex-wrap: wrap;
      position: relative;
    }
    .btn-whatsapp {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: #25D366;
      color: var(--white);
      font-weight: 700;
      font-size: 14px;
      padding: 15px 30px;
      border-radius: 6px;
      transition: background .2s;
    }
    .btn-whatsapp:hover { background: #1DAE55; }
    .btn-whatsapp svg { width: 20px; height: 20px; fill: currentColor; }
    .btn-gold-lg {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: var(--gold);
      color: var(--navy);
      font-weight: 700;
      font-size: 14px;
      padding: 15px 30px;
      border-radius: 6px;
      transition: background .2s;
    }
    .btn-gold-lg:hover { background: var(--gold-light); }

    /* ─── FOOTER ─────────────────────────────────────────── */
    .footer {
      background: var(--gray-800);
      padding: 56px 5% 28px;
    }
    .footer-top {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr 1fr;
      gap: 40px;
      padding-bottom: 40px;
      border-bottom: 1px solid rgba(255,255,255,0.1);
      margin-bottom: 28px;
    }
    .footer-brand p {
      font-size: 13px;
      color: rgba(255,255,255,0.45);
      line-height: 1.7;
      margin-top: 14px;
      max-width: 280px;
    }
    .footer-col h4 {
      font-size: 11px;
      font-weight: 700;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 16px;
    }
    .footer-col ul { list-style: none; display: flex; flex-direction: column; gap: 10px; }
    .footer-col li a {
      font-size: 13px;
      color: rgba(255,255,255,0.5);
      transition: color .2s;
    }
    .footer-col li a:hover { color: var(--gold-light); }
    .footer-contact-item {
      display: flex;
      align-items: flex-start;
      gap: 8px;
      font-size: 13px;
      color: rgba(255,255,255,0.5);
      margin-bottom: 10px;
    }
    .footer-contact-item span:first-child { color: var(--gold); font-size: 14px; }
    .footer-bottom {
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 12px;
    }
    .footer-bottom p {
      font-size: 12px;
      color: rgba(255,255,255,0.3);
    }
    .footer-bottom p span { color: var(--gold); }
    .footer-links {
      display: flex;
      gap: 20px;
    }
    .footer-links a {
      font-size: 12px;
      color: rgba(255,255,255,0.35);
      transition: color .2s;
    }
    .footer-links a:hover { color: var(--gold-light); }
    .social-row {
      display: flex;
      gap: 10px;
      margin-top: 16px;
    }
    .social-btn {
      width: 34px;
      height: 34px;
      border-radius: 50%;
      background: rgba(255,255,255,0.08);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 14px;
      color: rgba(255,255,255,0.5);
      transition: background .2s, color .2s;
    }
    .social-btn:hover { background: var(--gold); color: var(--navy); }

    /* ─── SECCIÓN CEO ────────────────────────────────────── */
    .ceo-section {
      background: var(--off-white);
      padding: 80px 5%;
    }
    .ceo-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 64px;
      align-items: center;
      max-width: 1100px;
      margin: 0 auto;
    }
    .ceo-video-wrapper {
      position: relative;
      border-radius: 20px;
      overflow: hidden;
      box-shadow: 0 24px 64px rgba(11,31,58,0.18);
      aspect-ratio: 9/16;
      max-width: 340px;
      margin: 0 auto;
      background: var(--navy);
    }
    .ceo-video-wrapper video {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }
    .ceo-video-badge {
      position: absolute;
      bottom: 18px;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(11,31,58,0.82);
      backdrop-filter: blur(8px);
      border: 1px solid rgba(201,168,76,0.35);
      border-radius: 40px;
      padding: 8px 20px;
      white-space: nowrap;
      text-align: center;
    }
    .ceo-video-badge strong {
      display: block;
      font-size: 13px;
      font-weight: 700;
      color: var(--gold-light);
      letter-spacing: 0.04em;
    }
    .ceo-video-badge span {
      font-size: 10px;
      color: rgba(255,255,255,0.55);
      letter-spacing: 0.1em;
      text-transform: uppercase;
    }
    .ceo-play-ring {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background: rgba(201,168,76,0.15);
      border: 2px solid rgba(201,168,76,0.5);
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: background .2s, transform .2s;
      pointer-events: none;
    }
    .ceo-video-wrapper:hover .ceo-play-ring { transform: translate(-50%, -50%) scale(1.08); background: rgba(201,168,76,0.25); }
    .ceo-video-wrapper.playing .ceo-play-ring { display: none; }
    .ceo-play-ring svg { width: 22px; height: 22px; fill: var(--gold); margin-left: 4px; }
    .ceo-content {}
    .ceo-quote-mark {
      font-family: 'Playfair Display', serif;
      font-size: 96px;
      line-height: 0.6;
      color: var(--gold);
      opacity: 0.25;
      margin-bottom: 8px;
    }
    .ceo-content h2 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(24px, 2.8vw, 36px);
      font-weight: 900;
      color: var(--navy);
      line-height: 1.2;
      margin-bottom: 20px;
    }
    .ceo-content h2 em { font-style: normal; color: var(--emerald); }
    .ceo-text {
      font-size: 15px;
      color: var(--gray-600);
      line-height: 1.85;
      margin-bottom: 14px;
    }
    .ceo-text strong { color: var(--navy); font-weight: 600; }
    .ceo-signature {
      margin-top: 32px;
      display: flex;
      align-items: center;
      gap: 16px;
      padding-top: 24px;
      border-top: 1px solid var(--gray-300);
    }
    .ceo-avatar {
      width: 52px;
      height: 52px;
      border-radius: 50%;
      background: var(--navy);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Playfair Display', serif;
      font-size: 20px;
      font-weight: 700;
      color: var(--gold);
      flex-shrink: 0;
      border: 2px solid var(--gold);
    }
    .ceo-info strong {
      display: block;
      font-size: 15px;
      font-weight: 700;
      color: var(--navy);
    }
    .ceo-info span {
      font-size: 12px;
      color: var(--gray-600);
      letter-spacing: 0.05em;
    }
    .ceo-pillars {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-top: 28px;
    }
    .ceo-pillar {
      background: var(--white);
      border: 1px solid var(--gray-300);
      border-left: 3px solid var(--gold);
      border-radius: 6px;
      padding: 12px 14px;
    }
    .ceo-pillar strong {
      display: block;
      font-size: 12px;
      font-weight: 700;
      color: var(--navy);
      margin-bottom: 2px;
    }
    .ceo-pillar span {
      font-size: 11px;
      color: var(--gray-600);
    }
    @media (max-width: 900px) {
      .ceo-container { grid-template-columns: 1fr; gap: 40px; }
      .ceo-video-wrapper { max-width: 280px; }
    }

    /* ─── RESPONSIVE ─────────────────────────────────────── */
    @media (max-width: 900px) {
      .nav-links { display: none; }
      .hero { grid-template-columns: 1fr; padding: 60px 5% 50px; }
      .hero-visual { display: none; }
      .options-grid { grid-template-columns: 1fr; }
      .steps-container { grid-template-columns: 1fr; }
      .step-panel-inner { grid-template-columns: 1fr; }
      .step-visual { height: 160px; font-size: 56px; }
      .faq-grid { grid-template-columns: 1fr; }
      .footer-top { grid-template-columns: 1fr 1fr; }
    }
    @media (max-width: 600px) {
      .hero h1 { font-size: 30px; }
      .hero-ctas { flex-direction: column; }
      .footer-top { grid-template-columns: 1fr; }
      .footer-bottom { flex-direction: column; align-items: flex-start; }
    }
  </style>
</head>
<body>

  <!-- ═══ NAV ═══════════════════════════════════════════ -->
  <nav class="nav">
    <a href="#" class="nav-logo">
      <div class="nav-logo-mark">A</div>
      <div class="nav-logo-text">
        <span>Grupo AISE</span>
        <span>Real Estate · Durango</span>
      </div>
    </a>
    <ul class="nav-links">
      <li><a href="#">Inicio</a></li>
      <li><a href="#">Propiedades</a></li>
      <li><a href="#opciones" class="active">Vender</a></li>
      <li><a href="#">Servicios</a></li>
      <li><a href="#">Blog</a></li>
    </ul>
    <a href="https://wa.me/526181056298" class="nav-cta">Contactar</a>
  </nav>

  <!-- ═══ HERO ═══════════════════════════════════════════ -->
  <section class="hero">
    <div class="hero-content">
      <div class="hero-badge">Grupo AISE Real Estate</div>
      <h1>Compramos <em>tu casa</em> o te ayudamos a venderla</h1>
      <p class="hero-sub">Somos tus aliados estratégicos en Durango. Recibe una oferta sin compromiso y descubre cómo podemos maximizar el valor de tu propiedad.</p>
      <div class="hero-ctas">
        <a href="#opciones" class="btn-primary">Recibir oferta →</a>
        <a href="https://wa.me/526181056298" class="btn-secondary">
          <svg viewBox="0 0 24 24" width="16" height="16" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51a12.8 12.8 0 0 0-.57-.01c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413Z"/></svg>
          Hablar por WhatsApp
        </a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hero-card-stack">
        <div class="hero-floating-tag">✓ Sin compromiso</div>
        <div class="hero-card">
          <div class="hero-card-label">Tu propiedad en Durango</div>
          <h3>Valuación gratuita en 24 horas</h3>
          <p>Conoce el precio real de tu propiedad con nuestros expertos locales</p>
          <div class="hero-stat-row">
            <div class="hero-stat">
              <strong>+500</strong>
              <span>Propiedades</span>
            </div>
            <div class="hero-stat">
              <strong>15+</strong>
              <span>Años exp.</span>
            </div>
            <div class="hero-stat">
              <strong>98%</strong>
              <span>Satisfacción</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══ CEO / PRESENTACIÓN ════════════════════════════ -->
  <section class="ceo-section">
    <div class="ceo-container">

      <!-- Video -->
      <div>
        <div class="ceo-video-wrapper" id="ceoVideoWrap" onclick="toggleCeoVideo()">
          <video id="ceoVideo" loop muted playsinline preload="auto"
                 src="aise-ceo-video.mp4"></video>
          <div class="ceo-play-ring">
            <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
          </div>
          <div class="ceo-video-badge">
            <strong>Fernando Gutiérrez</strong>
            <span>CEO &amp; Broker — Grupo AISE</span>
          </div>
        </div>
      </div>

      <!-- Contenido -->
      <div class="ceo-content">
        <div class="ceo-quote-mark">"</div>
        <h2>En Grupo AISE convertimos<br>tu propiedad en<br><em>resultados reales</em></h2>

        <p class="ceo-text">
          En Durango, el mercado inmobiliario está en constante evolución. Por eso en <strong>Grupo AISE</strong> trabajamos con un enfoque estratégico y personalizado: analizamos el valor real de tu propiedad, diseñamos el plan de venta más efectivo y te acompañamos en cada paso del proceso.
        </p>
        <p class="ceo-text">
          Ya sea que necesites <strong>vender rápido con pago de contado</strong>, contar con un asesor experto que gestione todo por ti, o publicar y conectar directamente con compradores calificados — tenemos la solución que se adapta a tu situación.
        </p>
        <p class="ceo-text">
          Nuestro equipo combina <strong>tecnología, datos de mercado y trato humano</strong> para garantizarte una venta transparente, segura y al mejor precio posible.
        </p>

        <div class="ceo-pillars">
          <div class="ceo-pillar">
            <strong>Oferta en 24–48 hrs</strong>
            <span>Compra directa de contado</span>
          </div>
          <div class="ceo-pillar">
            <strong>Asesoría integral</strong>
            <span>Legal, notarial y fiscal</span>
          </div>
          <div class="ceo-pillar">
            <strong>Valuación gratuita</strong>
            <span>Precio justo de mercado</span>
          </div>
          <div class="ceo-pillar">
            <strong>+15 años en Durango</strong>
            <span>Conocemos cada colonia</span>
          </div>
        </div>

        <div class="ceo-signature">
          <div class="ceo-avatar">FG</div>
          <div class="ceo-info">
            <strong>Fernando Gutiérrez</strong>
            <span>CEO &amp; Broker — Grupo AISE Real Estate</span>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- ═══ 3 OPCIONES ═════════════════════════════════════ -->
  <section class="options" id="opciones">
    <div class="section-header center">
      <p class="section-eyebrow">Elige tu camino</p>
      <div class="divider-gold"></div>
      <h2 class="section-title">Vende <em>rápido, fácil y seguro</em></h2>
      <p class="section-sub">Tres opciones adaptadas a tus necesidades. Tú decides cómo quieres vender tu propiedad en Durango.</p>
    </div>
    <div class="options-grid">

      <!-- Opción 1: Compra directa -->
      <div class="option-card">
        <div class="option-img">🏡</div>
        <div class="option-body">
          <span class="option-tag tag-fast">Rápido</span>
          <h3>1. Compramos tu propiedad</h3>
          <p>Si necesitas <strong>vender rápido</strong>, te hacemos una oferta justa, te <strong>pagamos de contado</strong> y garantizamos una compra segura, sin trámites complicados ni largas esperas.</p>
          <a href="https://wa.me/526181056298?text=Hola%2C%20quiero%20vender%20mi%20propiedad%20rápido" class="btn-option-primary">
            <svg viewBox="0 0 24 24" width="15" height="15" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51a12.8 12.8 0 0 0-.57-.01c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413Z"/></svg>
            Hablar por WhatsApp
          </a>
        </div>
      </div>

      <!-- Opción 2: Asesor -->
      <div class="option-card featured">
        <div class="option-img">🤝</div>
        <div class="option-body">
          <span class="option-tag tag-safe">Seguro</span>
          <h3>2. Un asesor la vende por ti</h3>
          <p><strong>Nuestro equipo de expertos inmobiliarios hará todo por ti</strong>: desde la valuación y promoción de tu propiedad hasta la negociación y cierre de la venta al mejor precio.</p>
          <a href="https://wa.me/526181056298?text=Hola%2C%20quiero%20un%20asesor%20para%20vender%20mi%20propiedad" class="btn-option-primary">
            Solicitar asesoría →
          </a>
        </div>
      </div>

      <!-- Opción 3: Publicar -->
      <div class="option-card">
        <div class="option-img">📋</div>
        <div class="option-body">
          <span class="option-tag tag-easy">Fácil</span>
          <h3>3. Publica tu propiedad gratis</h3>
          <p>Si prefieres gestionar la venta tú mismo, te ofrecemos una <strong>plataforma confiable</strong> donde cientos de compradores en Durango buscan propiedades todos los días.</p>
          <a href="https://wa.me/526181056298?text=Hola%2C%20quiero%20publicar%20mi%20propiedad" class="btn-option-gold">
            Publicar gratis →
          </a>
        </div>
      </div>

    </div>
  </section>

  <!-- ═══ PROCESO 3 PASOS ═══════════════════════════════ -->
  <section class="proceso" id="proceso">
    <div class="section-header">
      <p class="section-eyebrow">Proceso simple</p>
      <div class="divider-gold"></div>
      <h2 class="section-title">Así de fácil es vender<br>tu propiedad</h2>
      <p class="section-sub">Tres pasos claros para que el proceso sea ágil, seguro y sin complicaciones desde el primer contacto.</p>
    </div>

    <div class="steps-container">
      <div class="steps-nav">
        <div class="step-tab active" onclick="showStep(1)">
          <div class="step-number">1</div>
          <div class="step-tab-text">
            <span>Paso uno</span>
            <strong>Cuéntanos tu propiedad</strong>
          </div>
        </div>
        <div class="step-tab" onclick="showStep(2)">
          <div class="step-number">2</div>
          <div class="step-tab-text">
            <span>Paso dos</span>
            <strong>Analizamos y valuamos</strong>
          </div>
        </div>
        <div class="step-tab" onclick="showStep(3)">
          <div class="step-number">3</div>
          <div class="step-tab-text">
            <span>Paso tres</span>
            <strong>Recibe ofertas y vende</strong>
          </div>
        </div>
      </div>

      <div>
        <!-- Panel 1 -->
        <div class="step-panel active" id="panel-1">
          <div class="step-panel-inner">
            <div>
              <h3>Cuéntanos sobre tu propiedad</h3>
              <p>Compártenos los datos básicos de tu inmueble para que podamos darte la mejor orientación desde el primer momento.</p>
              <ul class="step-checklist">
                <li>Ubicación: colonia y dirección en Durango</li>
                <li>Características: m², recámaras, baños, estacionamiento</li>
                <li>Precio estimado (si no lo sabes, lo calculamos gratis)</li>
                <li>Tu disponibilidad de tiempo para la venta</li>
              </ul>
            </div>
            <div class="step-visual">📍</div>
          </div>
        </div>
        <!-- Panel 2 -->
        <div class="step-panel" id="panel-2">
          <div class="step-panel-inner">
            <div>
              <h3>Analizamos tu propiedad</h3>
              <p>Con los datos proporcionados, nuestros asesores realizan un análisis de mercado para asegurarnos de que todo esté en orden.</p>
              <ul class="step-checklist">
                <li>Avalúo comparativo de mercado en tu zona</li>
                <li>Revisión de documentación y situación legal</li>
                <li>Te mostramos las 3 opciones de venta disponibles</li>
                <li>Propuesta personalizada según tu necesidad</li>
              </ul>
            </div>
            <div class="step-visual">📊</div>
          </div>
        </div>
        <!-- Panel 3 -->
        <div class="step-panel" id="panel-3">
          <div class="step-panel-inner">
            <div>
              <h3>Recibe ofertas y vende</h3>
              <p>🚀 ¡Así de fácil! Tú decides la opción que más te convenga y nosotros nos aseguramos de un proceso ágil y seguro hasta el cierre.</p>
              <ul class="step-checklist">
                <li>Oferta directa de AISE en 24-48 horas</li>
                <li>Compradores calificados de nuestra cartera</li>
                <li>Acompañamiento notarial y legal completo</li>
                <li>Pago de contado o crédito hipotecario</li>
              </ul>
            </div>
            <div class="step-visual">🏆</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══ FAQ ════════════════════════════════════════════ -->
  <section class="faq" id="faq">
    <div class="section-header center">
      <p class="section-eyebrow">Preguntas frecuentes</p>
      <div class="divider-gold"></div>
      <h2 class="section-title">Resolvemos todas tus <em>dudas</em></h2>
      <p class="section-sub">Encuentra respuestas claras sobre cómo vender tu propiedad en Durango con Grupo AISE.</p>
    </div>
    <div class="faq-grid">

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          ¿Cómo vender mi casa con Grupo AISE?
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-answer">
          <p>Puedes hacerlo de tres maneras: recibir una oferta directa de AISE en contado, contar con un asesor experto que gestione todo el proceso por ti, o publicar tu propiedad en nuestra plataforma y conectarte directamente con compradores calificados en Durango.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          ¿Cuánto tiempo tarda la oferta de compra directa?
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-answer">
          <p>Si tu propiedad califica, podemos hacerte una oferta en 24 a 48 horas hábiles y completar el proceso de compra-venta en un plazo de 2 a 4 semanas, incluyendo trámites notariales.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          ¿Cuánto cuesta publicar o la asesoría?
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-answer">
          <p>La publicación de tu inmueble en nuestra plataforma es totalmente gratuita. La asesoría con broker funciona bajo una comisión al cierre exitoso de la venta, sin costos anticipados. Solo ganas cuando tú ganas.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          ¿Qué tipos de propiedades compran?
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-answer">
          <p>Compramos y comercializamos casas habitación, departamentos, terrenos, locales comerciales y naves industriales en Durango y zonas metropolitanas aledañas. Contáctanos para evaluar tu caso específico.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          ¿Cómo saben el precio justo de mi propiedad?
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-answer">
          <p>Realizamos un Análisis Comparativo de Mercado (ACM) con propiedades similares en tu zona, considerando metros cuadrados, antigüedad, estado de conservación y tendencias del mercado inmobiliario local en Durango.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          ¿Ayudan con los trámites legales y notariales?
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-answer">
          <p>Sí. Grupo AISE cuenta con un equipo de asesores legales y alianzas notariales para acompañarte en todo el proceso: revisión de escrituras, liberación de hipotecas, pago de impuestos y firma ante notario.</p>
        </div>
      </div>

    </div>
  </section>

  <!-- ═══ CTA BANNER ═════════════════════════════════════ -->
  <section class="cta-banner">
    <h2>¿Listo para <span>vender tu propiedad</span>?</h2>
    <p>Contáctanos hoy y recibe una valuación gratuita sin compromiso. Nuestro equipo en Durango está listo para ayudarte.</p>
    <div class="cta-buttons">
      <a href="https://wa.me/526181056298?text=Hola%2C%20quiero%20vender%20mi%20propiedad%20con%20Grupo%20AISE" class="btn-whatsapp">
        <svg viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51a12.8 12.8 0 0 0-.57-.01c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413Z"/></svg>
        Contactar por WhatsApp
      </a>
      <a href="mailto:Grupoaise25@gmail.com" class="btn-gold-lg">
        ✉ Enviar correo
      </a>
    </div>
  </section>

  <!-- ═══ FOOTER ═════════════════════════════════════════ -->
  <footer class="footer">
    <div class="footer-top">
      <div class="footer-brand">
        <div class="nav-logo">
          <div class="nav-logo-mark">A</div>
          <div class="nav-logo-text">
            <span>Grupo AISE</span>
            <span>Real Estate · Durango</span>
          </div>
        </div>
        <p>Somos la empresa inmobiliaria de mayor confianza en Durango. Conectamos a propietarios y compradores de forma ágil, segura y profesional.</p>
        <div class="social-row">
          <a href="https://www.facebook.com/share/18sqGHxzZy/" target="_blank" class="social-btn">f</a>
          <a href="#" class="social-btn">in</a>
          <a href="#" class="social-btn">ig</a>
          <a href="https://wa.me/526181056298" class="social-btn">w</a>
        </div>
      </div>
      <div class="footer-col">
        <h4>Empresa</h4>
        <ul>
          <li><a href="#">Acerca de AISE</a></li>
          <li><a href="#">Nuestro equipo</a></li>
          <li><a href="#">Casos de éxito</a></li>
          <li><a href="#">Blog inmobiliario</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>Servicios</h4>
        <ul>
          <li><a href="#">Comprar propiedad</a></li>
          <li><a href="#">Vender propiedad</a></li>
          <li><a href="#">Rentar inmueble</a></li>
          <li><a href="#">Avalúo gratuito</a></li>
          <li><a href="#">Asesoría legal</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>Contacto</h4>
        <div class="footer-contact-item">
          <span>📍</span>
          <span>Durango, Dgo., México</span>
        </div>
        <div class="footer-contact-item">
          <span>📞</span>
          <span>+52 (618) 105-6298 / 517-3594</span>
        </div>
        <div class="footer-contact-item">
          <span>✉</span>
          <span>Grupoaise25@gmail.com</span>
        </div>
        <div class="footer-contact-item">
          <span>🕐</span>
          <span>Lun–Sáb 9:00 am – 7:00 pm</span>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <p>© 2026 <span>Grupo AISE</span> — Todos los derechos reservados.</p>
      <div class="footer-links">
        <a href="#">Términos y condiciones</a>
        <a href="#">Aviso de privacidad</a>
        <a href="#">Política de cookies</a>
      </div>
    </div>
  </footer>

  <!-- ═══ SCRIPTS ════════════════════════════════════════ -->
  <script>
    // ── CEO Video toggle
    function toggleCeoVideo() {
      const video = document.getElementById('ceoVideo');
      const wrap  = document.getElementById('ceoVideoWrap');
      if (video.paused) {
        video.muted = false;
        video.play();
        wrap.classList.add('playing');
      } else {
        video.pause();
        wrap.classList.remove('playing');
      }
    }
    // Autoplay silencioso al cargar
    window.addEventListener('load', () => {
      const v = document.getElementById('ceoVideo');
      v.muted = true;
      v.play().catch(() => {});
    });

    // ── Paso a paso tabs
    function showStep(n) {
      document.querySelectorAll('.step-tab').forEach((t, i) => {
        t.classList.toggle('active', i === n - 1);
      });
      document.querySelectorAll('.step-panel').forEach((p, i) => {
        p.classList.toggle('active', i === n - 1);
      });
    }

    // ── FAQ accordion
    function toggleFaq(btn) {
      const answer = btn.nextElementSibling;
      const isOpen = answer.classList.contains('open');
      // Cerrar todas
      document.querySelectorAll('.faq-answer').forEach(a => a.classList.remove('open'));
      document.querySelectorAll('.faq-question').forEach(b => b.classList.remove('open'));
      // Abrir la seleccionada si estaba cerrada
      if (!isOpen) {
        answer.classList.add('open');
        btn.classList.add('open');
      }
    }

    // ── Nav scroll effect
    window.addEventListener('scroll', () => {
      document.querySelector('.nav').style.boxShadow =
        window.scrollY > 10 ? '0 4px 24px rgba(0,0,0,0.35)' : 'none';
    });
  </script>

</body>
</html>
