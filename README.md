<DOCTYPE html>
<html lang="ar" dir="rtl" translate="no">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="google" content="notranslate">
    <title>Babylon Web | هندسة منصات الذكاء الاصطناعي وتطوير المواقع</title>
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 48 48'%3E%3Crect width='48' height='48' rx='12' fill='%230E121B'/%3E%3Cpath d='M12 34H36M15 28H33M18 22H30' stroke='%23D9B36C' stroke-width='3' stroke-linecap='round'/%3E%3Cpath d='M24 11L30 17L24 22L18 17L24 11Z' stroke='%2338BDF8' stroke-width='2.5' fill='none'/%3E%3C/svg%3E">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@300;400;500;600;700&family=Space+Grotesk:wght@600;700&display=swap" rel="stylesheet">
    <style>
        /* إخفاء أي عنوان تلقائي يضيفه GitHub Pages */
        .markdown-body > h1:first-child,
        .markdown-body > hr:first-of-type {
            display: none !important;
        }

        :root {
            --bg-primary: #06070A;
            --bg-surface: rgba(14, 17, 24, 0.88);
            --bg-card-hover: rgba(22, 27, 38, 0.96);
            --gold-primary: #D9B36C;
            --gold-light: #F0D59B;
            --gold-dark: #9E7B3B;
            --tech-cyan: #38BDF8;
            --text-primary: #F8FAFC;
            --text-secondary: #94A3B8;
            --border-subtle: rgba(217, 179, 108, 0.16);
            --border-strong: rgba(217, 179, 108, 0.45);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'IBM Plex Sans Arabic', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.75;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 50% 0%, rgba(217, 179, 108, 0.12) 0%, transparent 55%),
                radial-gradient(circle at 85% 30%, rgba(56, 189, 248, 0.06) 0%, transparent 45%),
                linear-gradient(rgba(255, 255, 255, 0.018) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255, 255, 255, 0.018) 1px, transparent 1px);
            background-size: 100% 100%, 100% 100%, 44px 44px, 44px 44px;
        }

        .en-font {
            font-family: 'Space Grotesk', sans-serif;
            letter-spacing: 0.5px;
        }

        /* Header */
        header {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(6, 7, 10, 0.92);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid var(--border-subtle);
            padding: 12px 4%;
        }

        .nav-container {
            max-width: 1120px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 10px;
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
        }

        .brand-title {
            display: flex;
            flex-direction: column;
            line-height: 1.15;
        }

        .brand-title .en-name {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.15rem;
            font-weight: 700;
            color: var(--text-primary);
            letter-spacing: 0.6px;
        }

        .brand-title .en-name span {
            color: var(--gold-primary);
        }

        .brand-title .ar-sub {
            font-size: 0.7rem;
            color: var(--text-secondary);
            font-weight: 500;
        }

        .header-controls {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Language Switcher */
        .lang-switcher {
            display: inline-flex;
            align-items: center;
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid var(--border-subtle);
            border-radius: 10px;
            padding: 3px;
            gap: 2px;
        }

        .lang-btn {
            background: transparent;
            border: none;
            color: var(--text-secondary);
            font-size: 0.76rem;
            font-weight: 600;
            padding: 5px 9px;
            border-radius: 7px;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .lang-btn.active {
            background: linear-gradient(135deg, var(--gold-light), var(--gold-primary));
            color: #06070A;
        }

        .lang-btn:hover:not(.active) {
            color: var(--text-primary);
        }

        /* Buttons */
        .btn-primary {
            background: linear-gradient(135deg, var(--gold-light), var(--gold-primary), var(--gold-dark));
            color: #06070A;
            padding: 12px 22px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 700;
            font-size: 0.92rem;
            border: none;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            transition: transform 0.25s, box-shadow 0.25s;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(217, 179, 108, 0.25);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.03);
            color: var(--text-primary);
            padding: 11px 22px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            border: 1px solid var(--border-subtle);
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            transition: all 0.25s;
        }

        .btn-secondary:hover {
            border-color: var(--gold-primary);
            background: rgba(217, 179, 108, 0.08);
        }

        .header-cta {
            padding: 8px 16px;
            font-size: 0.84rem;
        }

        /* Hero */
        .hero {
            max-width: 1120px;
            margin: 0 auto;
            padding: 50px 5% 60px;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .status-pill {
            display: inline-flex;
            align-items: center;
            gap: 9px;
            background: rgba(217, 179, 108, 0.08);
            border: 1px solid var(--border-subtle);
            padding: 6px 16px;
            border-radius: 100px;
            font-size: 0.82rem;
            color: var(--gold-light);
            margin-bottom: 24px;
        }

        .status-dot {
            width: 7px;
            height: 7px;
            background-color: #10B981;
            border-radius: 50%;
            box-shadow: 0 0 10px #10B981;
        }

        .hero-logo-emblem {
            margin-bottom: 20px;
            filter: drop-shadow(0 12px 30px rgba(217, 179, 108, 0.22));
        }

        .hero h1 {
            font-size: clamp(1.85rem, 4.8vw, 3.2rem);
            font-weight: 700;
            line-height: 1.32;
            max-width: 820px;
            margin-bottom: 18px;
        }

        .hero h1 span {
            background: linear-gradient(135deg, var(--gold-light), var(--gold-primary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-bio-desc {
            color: var(--text-secondary);
            font-size: 1.03rem;
            max-width: 650px;
            margin-bottom: 30px;
        }

        .hero-actions {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            justify-content: center;
            width: 100%;
            max-width: 480px;
            margin-bottom: 44px;
        }

        .hero-actions a {
            flex: 1;
            min-width: 190px;
        }

        .trust-strip {
            width: 100%;
            max-width: 880px;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            background: var(--bg-surface);
            border: 1px solid var(--border-subtle);
            border-radius: 16px;
            padding: 20px 15px;
            backdrop-filter: blur(12px);
        }

        .trust-item {
            padding: 0 14px;
            border-inline-end: 1px solid var(--border-subtle);
        }

        .trust-item:last-child {
            border-inline-end: none;
        }

        .trust-item strong {
            display: block;
            font-size: 1.1rem;
            color: var(--gold-light);
            font-weight: 700;
            margin-bottom: 3px;
        }

        .trust-item span {
            font-size: 0.82rem;
            color: var(--text-secondary);
        }

        /* Sections */
        section {
            max-width: 1120px;
            margin: 0 auto;
            padding: 60px 5%;
        }

        .section-head {
            margin-bottom: 38px;
            text-align: center;
        }

        .section-tag {
            color: var(--gold-primary);
            font-size: 0.82rem;
            font-weight: 600;
            letter-spacing: 1px;
            text-transform: uppercase;
            margin-bottom: 8px;
            display: block;
        }

        .section-head h2 {
            font-size: clamp(1.6rem, 3.5vw, 2.2rem);
            font-weight: 700;
            margin-bottom: 10px;
        }

        .section-head p {
            color: var(--text-secondary);
            max-width: 580px;
            margin: 0 auto;
            font-size: 0.96rem;
        }

        /* Flagship Project (VoltAI) */
        .flagship-card {
            background: linear-gradient(145deg, rgba(16, 21, 32, 0.96), rgba(9, 12, 18, 0.98));
            border: 1px solid var(--border-strong);
            border-radius: 22px;
            padding: 32px;
            margin-bottom: 32px;
            position: relative;
            overflow: hidden;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.45);
        }

        .flagship-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--tech-cyan), var(--gold-primary), var(--tech-cyan));
        }

        .flagship-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 20px;
        }

        .live-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(56, 189, 248, 0.12);
            border: 1px solid rgba(56, 189, 248, 0.35);
            color: var(--tech-cyan);
            padding: 5px 14px;
            border-radius: 8px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .flagship-title-row {
            display: flex;
            align-items: center;
            gap: 14px;
            margin-bottom: 12px;
        }

        .volt-icon {
            width: 50px;
            height: 50px;
            border-radius: 14px;
            background: linear-gradient(135deg, rgba(56, 189, 248, 0.2), rgba(217, 179, 108, 0.2));
            border: 1px solid var(--gold-primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gold-light);
            flex-shrink: 0;
        }

        .flagship-title-row h3 {
            font-size: 1.55rem;
            font-weight: 700;
        }

        .flagship-desc {
            color: var(--text-secondary);
            font-size: 0.98rem;
            margin-bottom: 24px;
            max-width: 820px;
        }

        .flagship-specs {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 16px;
            margin-bottom: 26px;
        }

        .spec-box {
            background: rgba(255, 255, 255, 0.025);
            border: 1px solid var(--border-subtle);
            border-radius: 12px;
            padding: 16px;
        }

        .spec-box span {
            display: block;
            font-size: 0.78rem;
            color: var(--gold-primary);
            font-weight: 600;
            margin-bottom: 4px;
        }

        .spec-box p {
            font-size: 0.88rem;
            color: var(--text-primary);
            line-height: 1.6;
        }

        .flagship-actions {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        /* Grid 3 */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
            gap: 22px;
        }

        /* Service & Project Cards */
        .service-card, .project-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-subtle);
            border-radius: 18px;
            transition: all 0.3s ease;
        }

        .service-card {
            padding: 28px 24px;
        }

        .service-card:hover, .project-card:hover {
            transform: translateY(-5px);
            border-color: var(--border-strong);
            background: var(--bg-card-hover);
        }

        .icon-box {
            width: 46px;
            height: 46px;
            border-radius: 12px;
            background: rgba(217, 179, 108, 0.1);
            border: 1px solid rgba(217, 179, 108, 0.25);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gold-primary);
            margin-bottom: 18px;
        }

        .service-card h3 {
            font-size: 1.18rem;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .service-card p {
            color: var(--text-secondary);
            font-size: 0.92rem;
        }

        .project-card {
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }

        .project-visual {
            height: 145px;
            background: linear-gradient(145deg, #0D121D, #151C2C);
            border-bottom: 1px solid var(--border-subtle);
            padding: 16px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .mockup-bar {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .mockup-dots {
            display: flex;
            gap: 5px;
        }

        .mockup-dots span {
            width: 7px;
            height: 7px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.2);
        }

        .project-category {
            font-size: 0.74rem;
            color: var(--gold-light);
            background: rgba(217, 179, 108, 0.12);
            border: 1px solid rgba(217, 179, 108, 0.25);
            padding: 3px 10px;
            border-radius: 6px;
            font-weight: 600;
        }

        .mockup-wireframe {
            display: flex;
            flex-direction: column;
            gap: 7px;
        }

        .wire-line {
            height: 7px;
            border-radius: 4px;
            background: rgba(255, 255, 255, 0.08);
        }

        .wire-accent {
            height: 24px;
            border-radius: 7px;
            background: linear-gradient(90deg, rgba(217, 179, 108, 0.22), rgba(56, 189, 248, 0.12));
            border: 1px solid rgba(217, 179, 108, 0.2);
        }

        .project-info {
            padding: 22px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .project-info h3 {
            font-size: 1.15rem;
            margin-bottom: 8px;
        }

        .project-info p {
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-bottom: 18px;
        }

        /* FAQ Section */
        .faq-list {
            max-width: 820px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .faq-item {
            background: var(--bg-surface);
            border: 1px solid var(--border-subtle);
            border-radius: 14px;
            padding: 18px 22px;
        }

        .faq-item h4 {
            font-size: 1.02rem;
            color: var(--gold-light);
            margin-bottom: 6px;
            font-weight: 600;
        }

        .faq-item p {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* Smart Brief Builder & Direct Contact */
        .cta-panel {
            background: linear-gradient(145deg, rgba(18, 22, 33, 0.96), rgba(9, 11, 16, 0.98));
            border: 1px solid var(--border-strong);
            border-radius: 22px;
            padding: 40px 24px;
            text-align: center;
        }

        .cta-panel h2 {
            font-size: clamp(1.5rem, 3.5vw, 2.1rem);
            margin-bottom: 10px;
        }

        .cta-panel > p {
            color: var(--text-secondary);
            max-width: 580px;
            margin: 0 auto 28px;
            font-size: 0.96rem;
        }

        .brief-builder {
            max-width: 680px;
            margin: 0 auto 34px;
            background: rgba(255, 255, 255, 0.025);
            border: 1px solid var(--border-subtle);
            border-radius: 16px;
            padding: 22px;
            text-align: start;
        }

        .brief-label {
            display: block;
            font-size: 0.85rem;
            color: var(--gold-light);
            font-weight: 600;
            margin-bottom: 10px;
        }

        .type-pills {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 16px;
        }

        .type-pill {
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid var(--border-subtle);
            color: var(--text-secondary);
            padding: 8px 14px;
            border-radius: 9px;
            font-size: 0.85rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
        }

        .type-pill.selected {
            background: rgba(217, 179, 108, 0.16);
            border-color: var(--gold-primary);
            color: var(--gold-light);
        }

        .brief-input {
            width: 100%;
            background: rgba(6, 7, 10, 0.7);
            border: 1px solid var(--border-subtle);
            border-radius: 10px;
            padding: 12px 14px;
            color: var(--text-primary);
            font-size: 0.9rem;
            margin-bottom: 14px;
            outline: none;
        }

        .brief-input:focus {
            border-color: var(--gold-primary);
        }

        .contact-channels {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 14px;
            max-width: 820px;
            margin: 0 auto;
        }

        .channel-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid var(--border-subtle);
            border-radius: 14px;
            padding: 16px;
            text-decoration: none;
            color: var(--text-primary);
            display: flex;
            align-items: center;
            gap: 14px;
            transition: all 0.25s ease;
            text-align: start;
        }

        .channel-card:hover {
            border-color: var(--gold-primary);
            background: rgba(217, 179, 108, 0.08);
            transform: translateY(-3px);
        }

        .channel-icon {
            width: 42px;
            height: 42px;
            border-radius: 11px;
            background: rgba(217, 179, 108, 0.12);
            border: 1px solid rgba(217, 179, 108, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gold-light);
            flex-shrink: 0;
        }

        .channel-meta strong {
            display: block;
            font-size: 0.94rem;
            font-weight: 700;
        }

        .channel-meta span {
            font-size: 0.84rem;
            color: var(--gold-primary);
            font-family: 'Space Grotesk', sans-serif;
            direction: ltr;
            display: inline-block;
        }

        /* Footer */
        footer {
            border-top: 1px solid var(--border-subtle);
            padding: 30px 5%;
            text-align: center;
            color: var(--text-secondary);
            font-size: 0.85rem;
        }

        footer strong {
            color: var(--gold-primary);
            font-family: 'Space Grotesk', sans-serif;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(3, 4, 7, 0.88);
            backdrop-filter: blur(8px);
            z-index: 999;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal-card {
            background: #0E121B;
            border: 1px solid var(--border-strong);
            border-radius: 18px;
            max-width: 500px;
            width: 100%;
            padding: 28px 24px;
            text-align: start;
        }

        .modal-card h3 {
            color: var(--gold-light);
            font-size: 1.28rem;
            margin-bottom: 10px;
        }

        .modal-card p {
            color: var(--text-secondary);
            font-size: 0.94rem;
            margin-bottom: 22px;
            line-height: 1.75;
        }

        .modal-actions {
            display: flex;
            gap: 10px;
            justify-content: flex-end;
        }

        @media (max-width: 640px) {
            .brand-title .ar-sub { display: none; }
            .header-cta { display: none; }
            .trust-strip {
                grid-template-columns: 1fr;
                gap: 14px;
            }
            .trust-item {
                border-inline-end: none;
                border-bottom: 1px solid var(--border-subtle);
                padding-bottom: 12px;
            }
            .trust-item:last-child {
                border-bottom: none;
                padding-bottom: 0;
            }
            .flagship-card {
                padding: 22px 18px;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="nav-container">
            <a href="#" class="brand">
                <svg width="36" height="36" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect x="2" y="2" width="44" height="44" rx="11" fill="#0E121B" stroke="url(#goldGrad)" stroke-width="2"/>
                    <path d="M12 34H36M15 28H33M18 22H30" stroke="url(#goldGrad)" stroke-width="2.4" stroke-linecap="round"/>
                    <path d="M24 11L30 17L24 22L18 17L24 11Z" stroke="#38BDF8" stroke-width="2" fill="rgba(56,189,248,0.12)"/>
                    <defs>
                        <linearGradient id="goldGrad" x1="4" y1="4" x2="44" y2="44" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#F0D59B"/>
                            <stop offset="0.5" stop-color="#D9B36C"/>
                            <stop offset="1" stop-color="#9E7B3B"/>
                        </linearGradient>
                    </defs>
                </svg>
                <div class="brand-title">
                    <span class="en-name">BABYLON <span>WEB</span></span>
                    <span class="ar-sub" data-i18n="brandSub">هندسة الذكاء الاصطناعي والويب</span>
                </div>
            </a>

            <div class="header-controls">
                <div class="lang-switcher" role="group" aria-label="Language Switcher">
                    <button class="lang-btn active" onclick="setLanguage('ar')" id="btn-ar">العربية</button>
                    <button class="lang-btn" onclick="setLanguage('en')" id="btn-en">EN</button>
                    <button class="lang-btn" onclick="setLanguage('ku')" id="btn-ku">کوردی</button>
                </div>

                <a href="#contact" class="btn-primary header-cta" data-i18n="navCta">ابدأ مشروعك</a>
            </div>
        </div>
    </header>

    <section class="hero">
        <div class="status-pill">
            <span class="status-dot"></span>
            <span data-i18n="statusPill">متاحون لاستقبال مشاريع المواقع ومنصات الذكاء الاصطناعي</span>
        </div>

        <div class="hero-logo-emblem">
            <svg width="72" height="72" viewBox="0 0 74 74" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect x="3" y="3" width="68" height="68" rx="18" fill="rgba(14, 18, 27, 0.9)" stroke="url(#heroGold)" stroke-width="2.2"/>
                <path d="M18 52H56M22 43H52M26 34H48" stroke="url(#heroGold)" stroke-width="3" stroke-linecap="round"/>
                <path d="M37 16L47 25L37 34L27 25L37 16Z" stroke="#38BDF8" stroke-width="2.4" fill="rgba(56, 189, 248, 0.15)"/>
                <circle cx="37" cy="25" r="2.5" fill="#F0D59B"/>
                <defs>
                    <linearGradient id="heroGold" x1="6" y1="6" x2="68" y2="68" gradientUnits="userSpaceOnUse">
                        <stop stop-color="#F0D59B"/>
                        <stop offset="0.5" stop-color="#D9B36C"/>
                        <stop offset="1" stop-color="#9E7B3B"/>
                    </linearGradient>
                </defs>
            </svg>
        </div>

        <h1 data-i18n="heroTitle">نحول أفكارك إلى <span>منصات ذكاء اصطناعي</span> ومواقع رقمية متكاملة</h1>
        <p class="hero-bio-desc" data-i18n="heroDesc">
            في Babylon Web نصمم ونطور مواقع إلكترونية عالية الأداء، منصات مدعومة بالذكاء الاصطناعي، ومشاريع رقمية مخصصة تمنح عملك حضوراً موثوقاً وتجربة استخدام استثنائية.
        </p>

        <div class="hero-actions">
            <a href="#contact" class="btn-primary">
                <span data-i18n="heroBtnPrimary">اطلب بناء مشروعك</span>
            </a>
            <a href="#projects" class="btn-secondary">
                <span data-i18n="heroBtnSecondary">شاهد أعمالنا الحقيقية</span>
            </a>
        </div>

        <div class="trust-strip">
            <div class="trust-item">
                <strong data-i18n="trust1Title">برمجة مخصصة</strong>
                <span data-i18n="trust1Desc">أكواد نظيفة وسريعة بدون قوالب مكررة</span>
            </div>
            <div class="trust-item">
                <strong data-i18n="trust2Title">تكامل الذكاء الاصطناعي</strong>
                <span data-i18n="trust2Desc">ربط الأنظمة الذكية والأتمتة بمشروعك</span>
            </div>
            <div class="trust-item">
                <strong data-i18n="trust3Title">ملكية كاملة للعميل</strong>
                <span data-i18n="trust3Desc">تسليم المشروع مع الكود المصدري بالكامل</span>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="section-head">
            <span class="section-tag" data-i18n="projectsTag">معرض الإنجازات</span>
            <h2 data-i18n="projectsTitle">مشاريع ومنصات من تطويرنا</h2>
            <p data-i18n="projectsSub">اطلع على مشاريعنا الفعلية والحلول البرمجية الجاهزة للتخصيص حسب نشاطك التجاري</p>
        </div>

        <div class="flagship-card">
            <div class="flagship-header">
                <div class="live-badge">
                    <span class="status-dot"></span>
                    <span data-i18n="voltBadge">مشروع حقيقي مُطلق | Live Platform</span>
                </div>
                <span class="en-font" style="color: var(--gold-primary); font-size: 0.85rem; font-weight: 700;">AI PLATFORM ARCHITECTURE</span>
            </div>

            <div class="flagship-title-row">
                <div class="volt-icon">
                    <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
                </div>
                <div>
                    <h3 class="en-font">VoltAI Platform</h3>
                    <span style="font-size: 0.85rem; color: var(--tech-cyan);" data-i18n="voltSubtitle">منصة ذكاء اصطناعي متكاملة للأتمتة والإنتاجية</span>
                </div>
            </div>

            <p class="flagship-desc" data-i18n="voltDesc">
                منصة VoltAI هي أحد مشاريعنا الهندسية المتكاملة في مجال الذكاء الاصطناعي؛ تم تطويرها لتوفير أدوات ذكية سريعة الاستجابة تساعد المستخدمين وأصحاب الأعمال على إنجاز المهام المعقدة، توليد المحتوى، وتحليل البيانات عبر واجهة عصرية فائقة السرعة.
            </p>

            <div class="flagship-specs">
                <div class="spec-box">
                    <span data-i18n="voltSpec1Label">الفئة المستهدفة</span>
                    <p data-i18n="voltSpec1Val">رواد الأعمال، صناع المحتوى، والفرق التقنية الباحثة عن أدوات ذكاء اصطناعي موحدة وسريعة.</p>
                </div>
                <div class="spec-box">
                    <span data-i18n="voltSpec2Label">أبرز ميزات المنصة</span>
                    <p data-i18n="voltSpec2Val">معالجة فورية للأوامر، واجهة مستخدم متجاوبة بالكامل مع الهواتف، وتجربة استخدام سلسة بدون تعقيد.</p>
                </div>
                <div class="spec-box">
                    <span data-i18n="voltSpec3Label">دور Babylon Web في المشروع</span>
                    <p data-i18n="voltSpec3Val">تصميم الهوية البصرية، هندسة الواجهة الأمامية (UI/UX)، وربط نماذج الذكاء الاصطناعي وتحسين الأداء.</p>
                </div>
            </div>

            <div class="flagship-actions">
                <a href="https://volt-ai.std24341059.workers.dev/" target="_blank" rel="noopener noreferrer" class="btn-primary">
                    <span data-i18n="voltBtnVisit">زيارة منصة VoltAI مباشرة</span>
                    <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"/><polyline points="7 7 17 7 17 17"/></svg>
                </a>
                <a href="#contact" class="btn-secondary">
                    <span data-i18n="voltBtnOrder">اطلب بناء منصة مماثلة</span>
                </a>
            </div>
        </div>

        <div class="grid-3">
            <div class="project-card">
                <div class="project-visual">
                    <div class="mockup-bar">
                        <div class="mockup-dots"><span></span><span></span><span></span></div>
                        <span class="project-category" data-i18n="p1Cat">مساعد ذكي للشركات</span>
                    </div>
                    <div class="mockup-wireframe">
                        <div class="wire-line" style="width: 65%;"></div>
                        <div class="wire-line" style="width: 45%;"></div>
                        <div class="wire-accent"></div>
                    </div>
                </div>
                <div class="project-info">
                    <div>
                        <h3 data-i18n="p1Title">نظام خدمة العملاء الذكي</h3>
                        <p data-i18n="p1Desc">ربط موقعك بمساعد ذكاء اصطناعي مدرب على بيانات شركتك للرد على استفسارات الزبائن وحجز المواعيد تلقائياً.</p>
                    </div>
                    <button class="btn-secondary" onclick="openProject('p1')" data-i18n="btnDetails">تفاصيل البنية البرمجية</button>
                </div>
            </div>

            <div class="project-card">
                <div class="project-visual">
                    <div class="mockup-bar">
                        <div class="mockup-dots"><span></span><span></span><span></span></div>
                        <span class="project-category" data-i18n="p2Cat">منصات تجارية وعقارية</span>
                    </div>
                    <div class="mockup-wireframe">
                        <div class="wire-line" style="width: 75%;"></div>
                        <div class="wire-line" style="width: 50%;"></div>
                        <div class="wire-accent"></div>
                    </div>
                </div>
                <div class="project-info">
                    <div>
                        <h3 data-i18n="p2Title">مواقع الشركات والمراكز الطبية</h3>
                        <p data-i18n="p2Desc">واجهات تعريفية رسمية عالية الثقة تعرض الخدمات والمشاريع مع ربط مباشر بقنوات التواصل والحجز.</p>
                    </div>
                    <button class="btn-secondary" onclick="openProject('p2')" data-i18n="btnDetails">تفاصيل البنية البرمجية</button>
                </div>
            </div>

            <div class="project-card">
                <div class="project-visual">
                    <div class="mockup-bar">
                        <div class="mockup-dots"><span></span><span></span><span></span></div>
                        <span class="project-category" data-i18n="p3Cat">أنظمة إدارة سحابية</span>
                    </div>
                    <div class="mockup-wireframe">
                        <div class="wire-line" style="width: 55%;"></div>
                        <div class="wire-line" style="width: 70%;"></div>
                        <div class="wire-accent"></div>
                    </div>
                </div>
                <div class="project-info">
                    <div>
                        <h3 data-i18n="p3Title">لوحات التحكم وإدارة المشاريع</h3>
                        <p data-i18n="p3Desc">تطبيقات ويب مخصصة لمتابعة المبيعات، المهام، وتقارير الأداء من الهاتف أو الحاسوب بواجهة سهلة.</p>
                    </div>
                    <button class="btn-secondary" onclick="openProject('p3')" data-i18n="btnDetails">تفاصيل البنية البرمجية</button>
                </div>
            </div>
        </div>
    </section>

    <section id="services">
        <div class="section-head">
            <span class="section-tag" data-i18n="servicesTag">مجالات التخصص</span>
            <h2 data-i18n="servicesTitle">ماذا نقدم لمشروعك؟</h2>
            <p data-i18n="servicesSub">حلول هندسية تجمع بين قوة الذكاء الاصطناعي وتصميم الويب الاحترافي</p>
        </div>

        <div class="grid-3">
            <div class="service-card">
                <div class="icon-box">
                    <svg width="23" height="23" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
                </div>
                <h3 data-i18n="s1Title">بناء منصات الذكاء الاصطناعي</h3>
                <p data-i18n="s1Desc">تطوير تطبيقات ومنصات ويب مدعومة بالذكاء الاصطناعي (مثل منصة VoltAI) لأتمتة الأعمال وتقديم خدمات رقمية مبتكرة.</p>
            </div>

            <div class="service-card">
                <div class="icon-box">
                    <svg width="23" height="23" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>
                </div>
                <h3 data-i18n="s2Title">تطوير المواقع وصفحات الهبوط</h3>
                <p data-i18n="s2Desc">تصميم وبرمجة مواقع سريعة ومتجاوبة بالكامل مع الهواتف تعكس قوة علامتك التجارية وتزيد من ثقة عملائك.</p>
            </div>

            <div class="service-card">
                <div class="icon-box">
                    <svg width="23" height="23" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><polygon points="12 2 2 7 12 12 22 7 12 2"/><polyline points="2 17 12 22 22 17"/><polyline points="2 12 12 17 22 12"/></svg>
                </div>
                <h3 data-i18n="s3Title">تحويل الأفكار إلى مشاريع رقمية</h3>
                <p data-i18n="s3Desc">نرافقك من التخطيط الأولي إلى إطلاق النسخة الكاملة على الإنترنت مع تسليم كافة الأكواد والملفات البرمجية.</p>
            </div>
        </div>
    </section>

    <section id="faq">
        <div class="section-head">
            <span class="section-tag" data-i18n="faqTag">إجابات واضحة</span>
            <h2 data-i18n="faqTitle">الأسئلة الشائعة</h2>
        </div>

        <div class="faq-list">
            <div class="faq-item">
                <h4 data-i18n="q1Title">كم يستغرق تصميم وبناء الموقع أو المنصة؟</h4>
                <p data-i18n="q1Desc">تتراوح مدة التنفيذ بين 3 إلى 7 أيام للمواقع التعريفية وصفحات الهبوط، ومن أسبوع إلى أسبوعين لمنصات الذكاء الاصطناعي والأنظمة المخصصة حسب حجم الميزات المطلوبة.</p>
            </div>
            <div class="faq-item">
                <h4 data-i18n="q2Title">هل يعمل الموقع بسلاسة على هواتف الآيفون والأندرويد؟</h4>
                <p data-i18n="q2Desc">نعم، جميع مشاريعنا تُبنى بمنهجية التوافق الكامل مع شاشات الهواتف الذكية أولاً، مع سرعة تحميل عالية وتجربة تصفح مريحة.</p>
            </div>
            <div class="faq-item">
                <h4 data-i18n="q3Title">هل أستلم ملكية الكود والمشروع بالكامل؟</h4>
                <p data-i18n="q3Desc">بالتأكيد، عند الانتهاء من المشروع يتم تسليمك كافة الأكواد المصدرية وربط الموقع بالاستضافة والدومين الخاص بك بملكية كاملة 100%.</p>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="cta-panel">
            <h2 data-i18n="contactTitle">تواصل معنا مباشرة لبدء مشروعك</h2>
            <p data-i18n="contactDesc">حدد نوع مشروعك لإرسال طلب سريع عبر واتساب، أو تواصل معنا مباشرة عبر حساباتنا الرسمية.</p>

            <!-- نموذج تحديد المشروع السريع -->
            <div class="brief-builder">
                <span class="brief-label" data-i18n="briefSelectLabel">1. اختر نوع المشروع المطلوب:</span>
                <div class="type-pills" id="projectTypeGroup">
                    <button type="button" class="type-pill selected" onclick="selectType(this, 'ai')" data-i18n="typeAI">منصة ذكاء اصطناعي</button>
                    <button type="button" class="type-pill" onclick="selectType(this, 'web')" data-i18n="typeWeb">موقع شركة / عيادة / صفحة هبوط</button>
                    <button type="button" class="type-pill" onclick="selectType(this, 'custom')" data-i18n="typeCustom">نظام خاص / مشروع متكامل</button>
                </div>

                <span class="brief-label" data-i18n="briefInputLabel">2. نبذة قصيرة عن فكرتك (اختياري):</span>
                <input type="text" id="projectIdeaInput" class="brief-input" placeholder="مثال: أرغب ببناء موقع تعريفي لعيادتي مع نظام حجز..." data-i18n-placeholder="briefPlaceholder">

                <button type="button" onclick="sendWhatsAppBrief()" class="btn-primary" style="width: 100%;">
                    <span data-i18n="briefSendBtn">إرسال تفاصيل المشروع عبر واتساب</span>
                    <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"/><polyline points="7 7 17 7 17 17"/></svg>
                </button>
            </div>

            <div class="contact-channels">
                <a href="https://wa.me/9647850772200" target="_blank" rel="noopener noreferrer" class="channel-card">
                    <div class="channel-icon">
                        <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round" stroke-linejoin="round"><path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z"/></svg>
                    </div>
                    <div class="channel-meta">
                        <strong data-i18n="chWhatsapp">واتساب مباشر</strong>
                        <span>+964 785 077 2200</span>
                    </div>
                </a>

                <a href="https://t.me/mzr_eng" target="_blank" rel="noopener noreferrer" class="channel-card">
                    <div class="channel-icon">
                        <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round" stroke-linejoin="round"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
                    </div>
                    <div class="channel-meta">
                        <strong data-i18n="chTelegram">تليجرام</strong>
                        <span>@mzr_eng</span>
                    </div>
                </a>

                <a href="https://instagram.com/0dst" target="_blank" rel="noopener noreferrer" class="channel-card">
                    <div class="channel-icon">
                        <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
                    </div>
                    <div class="channel-meta">
                        <strong data-i18n="chInstagram">إنستغرام</strong>
                        <span>@0dst</span>
                    </div>
                </a>
            </div>
        </div>
    </section>

    <footer>
        <p data-i18n="footerText">جميع الحقوق محفوظة &copy; 2026 <strong>BABYLON WEB</strong> — تطوير منصات الذكاء الاصطناعي والحلول الرقمية | العراق</p>
    </footer>

    <div id="projectModal" class="modal" onclick="closeProject()">
        <div class="modal-card" onclick="event.stopPropagation()">
            <h3 id="mTitle"></h3>
            <p id="mDesc"></p>
            <div class="modal-actions">
                <button class="btn-secondary" onclick="closeProject()" data-i18n="modalClose">إغلاق</button>
                <a href="#contact" class="btn-primary" onclick="closeProject()" data-i18n="modalOrder">اطلب نموذجاً مشابهاً</a>
            </div>
        </div>
    </div>

    <script>
        let currentLang = 'ar';
        let selectedProjectType = 'ai';

        const i18n = {
            ar: {
                dir: 'rtl',
                brandSub: 'هندسة الذكاء الاصطناعي والويب',
                navCta: 'ابدأ مشروعك',
                statusPill: 'متاحون لاستقبال مشاريع المواقع ومنصات الذكاء الاصطناعي',
                heroTitle: 'نحول أفكارك إلى <span>منصات ذكاء اصطناعي</span> ومواقع رقمية متكاملة',
                heroDesc: 'في Babylon Web نصمم ونطور مواقع إلكترونية عالية الأداء، منصات مدعومة بالذكاء الاصطناعي، ومشاريع رقمية مخصصة تمنح عملك حضوراً موثوقاً وتجربة استخدام استثنائية.',
                heroBtnPrimary: 'اطلب بناء مشروعك',
                heroBtnSecondary: 'شاهد أعمالنا الحقيقية',
                trust1Title: 'برمجة مخصصة',
                trust1Desc: 'أكواد نظيفة وسريعة بدون قوالب مكررة',
                trust2Title: 'تكامل الذكاء الاصطناعي',
                trust2Desc: 'ربط الأنظمة الذكية والأتمتة بمشروعك',
                trust3Title: 'ملكية كاملة للعميل',
                trust3Desc: 'تسليم المشروع مع الكود المصدري بالكامل',
                projectsTag: 'معرض الإنجازات',
                projectsTitle: 'مشاريع ومنصات من تطويرنا',
                projectsSub: 'اطلع على مشاريعنا الفعلية والحلول البرمجية الجاهزة للتخصيص حسب نشاطك التجاري',
                voltBadge: 'مشروع حقيقي مُطلق | Live Platform',
                voltSubtitle: 'منصة ذكاء اصطناعي متكاملة للأتمتة والإنتاجية',
                voltDesc: 'منصة VoltAI هي أحد مشاريعنا الهندسية المتكاملة في مجال الذكاء الاصطناعي؛ تم تطويرها لتوفير أدوات ذكية سريعة الاستجابة تساعد المستخدمين وأصحاب الأعمال على إنجاز المهام المعقدة، توليد المحتوى، وتحليل البيانات عبر واجهة عصرية فائقة السرعة.',
                voltSpec1Label: 'الفئة المستهدفة',
                voltSpec1Val: 'رواد الأعمال، صناع المحتوى، والفرق التقنية الباحثة عن أدوات ذكاء اصطناعي موحدة وسريعة.',
                voltSpec2Label: 'أبرز ميزات المنصة',
                voltSpec2Val: 'معالجة فورية للأوامر، واجهة مستخدم متجاوبة بالكامل مع الهواتف، وتجربة استخدام سلسة بدون تعقيد.',
                voltSpec3Label: 'دور Babylon Web في المشروع',
                voltSpec3Val: 'تصميم الهوية البصرية، هندسة الواجهة الأمامية (UI/UX)، وربط نماذج الذكاء الاصطناعي وتحسين الأداء.',
                voltBtnVisit: 'زيارة منصة VoltAI مباشرة',
                voltBtnOrder: 'اطلب بناء منصة مماثلة',
                p1Cat: 'مساعد ذكي للشركات',
                p1Title: 'نظام خدمة العملاء الذكي',
                p1Desc: 'ربط موقعك بمساعد ذكاء اصطناعي مدرب على بيانات شركتك للرد على استفسارات الزبائن وحجز المواعيد تلقائياً.',
                p2Cat: 'منصات تجارية وعقارية',
                p2Title: 'مواقع الشركات والمراكز الطبية',
                p2Desc: 'واجهات تعريفية رسمية عالية الثقة تعرض الخدمات والمشاريع مع ربط مباشر بقنوات التواصل والحجز.',
                p3Cat: 'أنظمة إدارة سحابية',
                p3Title: 'لوحات التحكم وإدارة المشاريع',
                p3Desc: 'تطبيقات ويب مخصصة لمتابعة المبيعات، المهام، وتقارير الأداء من الهاتف أو الحاسوب بواجهة سهلة.',
                btnDetails: 'تفاصيل البنية البرمجية',
                servicesTag: 'مجالات التخصص',
                servicesTitle: 'ماذا نقدم لمشروعك؟',
                servicesSub: 'حلول هندسية تجمع بين قوة الذكاء الاصطناعي وتصميم الويب الاحترافي',
                s1Title: 'بناء منصات الذكاء الاصطناعي',
                s1Desc: 'تطوير تطبيقات ومنصات ويب مدعومة بالذكاء الاصطناعي (مثل منصة VoltAI) لأتمتة الأعمال وتقديم خدمات رقمية مبتكرة.',
                s2Title: 'تطوير المواقع وصفحات الهبوط',
                s2Desc: 'تصميم وبرمجة مواقع سريعة ومتجاوبة بالكامل مع الهواتف تعكس قوة علامتك التجارية وتزيد من ثقة عملائك.',
                s3Title: 'تحويل الأفكار إلى مشاريع رقمية',
                s3Desc: 'نرافقك من التخطيط الأولي إلى إطلاق النسخة الكاملة على الإنترنت مع تسليم كافة الأكواد والملفات البرمجية.',
                faqTag: 'إجابات واضحة',
                faqTitle: 'الأسئلة الشائعة',
                q1Title: 'كم يستغرق تصميم وبناء الموقع أو المنصة؟',
                q1Desc: 'تتراوح مدة التنفيذ بين 3 إلى 7 أيام للمواقع التعريفية وصفحات الهبوط، ومن أسبوع إلى أسبوعين لمنصات الذكاء الاصطناعي والأنظمة المخصصة حسب حجم الميزات المطلوبة.',
                q2Title: 'هل يعمل الموقع بسلاسة على هواتف الآيفون والأندرويد؟',
                q2Desc: 'نعم، جميع مشاريعنا تُبنى بمنهجية التوافق الكامل مع شاشات الهواتف الذكية أولاً، مع سرعة تحميل عالية وتجربة تصفح مريحة.',
                q3Title: 'هل أستلم ملكية الكود والمشروع بالكامل؟',
                q3Desc: 'بالتأكيد، عند الانتهاء من المشروع يتم تسليمك كافة الأكواد المصدرية وربط الموقع بالاستضافة والدومين الخاص بك بملكية كاملة 100%.',
                contactTitle: 'تواصل معنا مباشرة لبدء مشروعك',
                contactDesc: 'حدد نوع مشروعك لإرسال طلب سريع عبر واتساب، أو تواصل معنا مباشرة عبر حساباتنا الرسمية.',
                briefSelectLabel: '1. اختر نوع المشروع المطلوب:',
                typeAI: 'منصة ذكاء اصطناعي',
                typeWeb: 'موقع شركة / عيادة / صفحة هبوط',
                typeCustom: 'نظام خاص / مشروع متكامل',
                briefInputLabel: '2. نبذة قصيرة عن فكرتك (اختياري):',
                briefPlaceholder: 'مثال: أرغب ببناء موقع تعريفي لعيادتي مع نظام حجز...',
                briefSendBtn: 'إرسال تفاصيل المشروع عبر واتساب',
                chWhatsapp: 'واتساب مباشر',
                chTelegram: 'تليجرام',
                chInstagram: 'إنستغرام',
                footerText: 'جميع الحقوق محفوظة &copy; 2026 <strong>BABYLON WEB</strong> — تطوير منصات الذكاء الاصطناعي والحلول الرقمية | العراق',
                modalClose: 'إغلاق',
                modalOrder: 'اطلب نموذجاً مشابهاً',
                modals: {
                    p1: { title: 'نظام خدمة العملاء الذكي', desc: 'بنية برمجية متكاملة تتيح تضمين مساعد ذكي داخل موقعك الإلكتروني للإجابة الفورية على أسئلة العملاء وتوجيههم لحجز الخدمات على مدار 24 ساعة.' },
                    p2: { title: 'مواقع الشركات والمراكز الطبية', desc: 'تصميم هندسي سريع التحميل يركز على إبراز هوية المؤسسة، عرض الخدمات والأطباء أو المشاريع، وتسهيل التواصل الفوري من الهواتف الذكية.' },
                    p3: { title: 'لوحات التحكم وإدارة المشاريع', desc: 'تطوير واجهات ويب تفاعلية لإدارة البيانات والفرق التجارية بوضوح تام وسرعة استجابة عالية على جميع الأجهزة.' }
                }
            },
            en: {
                dir: 'ltr',
                brandSub: 'AI Platforms & Web Engineering',
                navCta: 'Start Project',
                statusPill: 'Available for Web & AI Platform Development',
                heroTitle: 'We Transform Ideas into <span>AI Platforms</span> & Digital Experiences',
                heroDesc: 'At Babylon Web, we architect high-performance websites, AI-powered platforms, and custom digital products engineered to build trust and scale your business.',
                heroBtnPrimary: 'Build Your Project',
                heroBtnSecondary: 'Explore Live Work',
                trust1Title: 'Custom Engineering',
                trust1Desc: 'Clean, fast codebases without bloated templates',
                trust2Title: 'AI Integration',
                trust2Desc: 'Smart automation & LLM integration built-in',
                trust3Title: '100% Ownership',
                trust3Desc: 'Full source code and deployment handover',
                projectsTag: 'Proven Track Record',
                projectsTitle: 'Platforms & Systems We Built',
                projectsSub: 'Explore our live flagship platform alongside customizable digital architectures',
                voltBadge: 'Live Production Project',
                voltSubtitle: 'All-in-One AI Productivity & Automation Platform',
                voltDesc: 'VoltAI is one of our flagship AI engineering projects, built to deliver ultra-responsive intelligent tools that help entrepreneurs and teams automate workflows, generate content, and process data seamlessly.',
                voltSpec1Label: 'Target Audience',
                voltSpec1Val: 'Entrepreneurs, content creators, and tech teams seeking fast, unified AI tools.',
                voltSpec2Label: 'Core Capabilities',
                voltSpec2Val: 'Real-time prompt processing, mobile-first responsive UI, and frictionless user workflows.',
                voltSpec3Label: 'Babylon Web Scope',
                voltSpec3Val: 'Brand visual identity, full UI/UX front-end architecture, AI integration, and speed optimization.',
                voltBtnVisit: 'Visit VoltAI Live',
                voltBtnOrder: 'Request Similar Platform',
                p1Cat: 'Enterprise AI Assistant',
                p1Title: 'Smart Customer Support System',
                p1Desc: 'Custom AI assistants trained on your business data to answer inquiries and book appointments 24/7.',
                p2Cat: 'Corporate & Medical Web',
                p2Title: 'Enterprise & Clinic Portals',
                p2Desc: 'High-trust corporate websites designed to showcase services and convert visitors directly via mobile.',
                p3Cat: 'Cloud Management',
                p3Title: 'Project & Operations Dashboards',
                p3Desc: 'Tailored web applications to track sales, team workflows, and analytics from any device.',
                btnDetails: 'Architecture Details',
                servicesTag: 'Core Expertise',
                servicesTitle: 'What We Build For You',
                servicesSub: 'Engineering solutions combining modern AI capabilities with precision web design',
                s1Title: 'AI Platform Development',
                s1Desc: 'Building AI-powered web applications and SaaS tools (like VoltAI) to automate workflows and launch innovative products.',
                s2Title: 'Websites & Landing Pages',
                s2Desc: 'Fast, responsive websites engineered to elevate your brand credibility and maximize client conversions.',
                s3Title: 'Idea-to-Launch Execution',
                s3Desc: 'End-to-end development from initial blueprint to live cloud deployment with complete source code handover.',
                faqTag: 'Clear Answers',
                faqTitle: 'Frequently Asked Questions',
                q1Title: 'How long does it take to build a website or platform?',
                q1Desc: 'Corporate websites and landing pages take 3 to 7 days, while custom AI platforms and dashboards take 1 to 2 weeks depending on required integrations.',
                q2Title: 'Are all websites fully optimized for mobile devices?',
                q2Desc: 'Yes, every project is engineered mobile-first for iOS and Android browsers with fast load speeds and clean responsive layouts.',
                q3Title: 'Do I receive full ownership and source code?',
                q3Desc: 'Yes, upon completion we hand over 100% of the source code and connect everything to your domain and hosting.',
                contactTitle: 'Connect Directly to Start Your Project',
                contactDesc: 'Select your project type to send a structured inquiry via WhatsApp, or reach out through our direct channels.',
                briefSelectLabel: '1. Select your project type:',
                typeAI: 'AI Platform',
                typeWeb: 'Company / Clinic Website / Landing Page',
                typeCustom: 'Custom System / Full MVP',
                briefInputLabel: '2. Brief note about your idea (optional):',
                briefPlaceholder: 'Example: I need a clinic website with online appointment booking...',
                briefSendBtn: 'Send Project Brief via WhatsApp',
                chWhatsapp: 'Direct WhatsApp',
                chTelegram: 'Telegram',
                chInstagram: 'Instagram',
                footerText: 'All Rights Reserved &copy; 2026 <strong>BABYLON WEB</strong> — AI Platforms & Web Engineering | Iraq',
                modalClose: 'Close',
                modalOrder: 'Request Similar Build',
                modals: {
                    p1: { title: 'Smart Customer Support System', desc: 'A custom web architecture embedding an AI assistant trained on your company knowledge base to handle customer inquiries and bookings 24/7.' },
                    p2: { title: 'Enterprise & Clinic Portals', desc: 'Fast-loading corporate and medical websites focused on authority, clear service presentation, and instant mobile conversion.' },
                    p3: { title: 'Project & Operations Dashboards', desc: 'Interactive web dashboards built to manage operations, teams, and performance metrics smoothly across mobile and desktop.' }
                }
            },
            ku: {
                dir: 'rtl',
                brandSub: 'ئەندازیاری ژیری دەستکرد و وێب',
                navCta: 'پڕۆژەکەت دەستپێبکە',
                statusPill: 'ئامادەین بۆ دروستکردنی ماڵپەڕ و پلاتفۆرمی ژیری دەستکرد',
                heroTitle: 'بیرۆکەکانت دەگۆڕین بۆ <span>پلاتفۆرمی ژیری دەستکرد</span> و ماڵپەڕی پێشکەوتوو',
                heroDesc: 'لە Babylon Web ماڵپەڕی خێرا، پلاتفۆرمی پاڵپشتیکراو بە ژیری دەستکرد، و پڕۆژەی دیجیتاڵی تایبەت دروست دەکەین کە متمانە لای کڕیارەکانت دروست دەکات.',
                heroBtnPrimary: 'داواکردنی پڕۆژە',
                heroBtnSecondary: 'بینینی کارەکانمان',
                trust1Title: 'پڕۆگرامسازی تایبەت',
                trust1Desc: 'کۆدی خاوێن و خێرا بەبێ قاڵبی دووبارە',
                trust2Title: 'ژیری دەستکرد (AI)',
                trust2Desc: 'بەستنەوەی سیستەمی زیرەک بە پڕۆژەکەتەوە',
                trust3Title: 'خاوەندارێتی تەواو',
                trust3Desc: 'ڕادەستکردنی تەواوی کۆد و فایلەکانی پڕۆژە',
                projectsTag: 'پێشانگای کارەکانمان',
                projectsTitle: 'پڕۆژە و پلاتفۆرمە دروستکراوەکانمان',
                projectsSub: 'سەیری پڕۆژە ڕاستەقینەکانمان و نموونە ئامادەکانمان بکە کە بەپێی کارەکەت دەگونجێنرێن',
                voltBadge: 'پڕۆژەی ڕاستەقینە | Live Platform',
                voltSubtitle: 'پلاتفۆرمی ژیری دەستکرد بۆ خێراکردنی کارەکان',
                voltDesc: 'پلاتفۆرمی VoltAI یەکێکە لە پڕۆژە ئەندازیارییە تەواوەکانمان لە بواری ژیری دەستکرد؛ دروستکراوە بۆ دابینکردنی ئامرازی زیرەک و خێرا کە یارمەتی خاوەنکاران دەدات بۆ جێبەجێکردنی کارەکان بە شێوەیەکی مۆدێرن.',
                voltSpec1Label: 'بۆ کێ گونجاوە',
                voltSpec1Val: 'خاوەنکاران، دروستکەرانی ناوەڕۆک، و تیمە تەکنیکییەکان کە بەدوای ئامرازی خێرای AI دەگەڕێن.',
                voltSpec2Label: 'تایبەتمەندییە سەرەکییەکان',
                voltSpec2Val: 'وەڵامدانەوەی خێرا، ڕووکارێکی گونجاو لەگەڵ هەموو مۆبایلەکان، و بەکارهێنانی ئاسان.',
                voltSpec3Label: 'ڕۆڵی Babylon Web لە پڕۆژەکەدا',
                voltSpec3Val: 'دیزاینی ناسنامەی بینراو، ئەندازیاری ڕووکاری پێشەوە (UI/UX)، و بەستنەوەی مۆدێلەکانی ژیری دەستکرد.',
                voltBtnVisit: 'سەردانی پلاتفۆرمی VoltAI',
                voltBtnOrder: 'داواکردنی پلاتفۆرمی هاوشێوە',
                p1Cat: 'یاریدەدەری زیرەک',
                p1Title: 'سیستەمی خزمەتگوزاری کڕیاران',
                p1Desc: 'بەستنەوەی ماڵپەڕەکەت بە یاریدەدەرێکی زیرەک بۆ وەڵامدانەوەی کڕیاران و حجزکردنی کات بە شێوەی ئۆتۆماتیکی.',
                p2Cat: 'ماڵپەڕی کۆمپانیا و کلینیک',
                p2Title: 'ماڵپەڕی کۆمپانیا و سەنتەرە پزیشکییەکان',
                p2Desc: 'ڕووکاری فەرمی و متمانەپێکراو بۆ نمایشکردنی خزمەتگوزارییەکان و پەیوەندیکردنی خێرا لە ڕێگەی مۆبایلەوە.',
                p3Cat: 'سیستەمی بەڕێوەبردن',
                p3Title: 'داشبۆرد و بەڕێوەبردنی پڕۆژەکان',
                p3Desc: 'ئەپڵیکەیشنی وێب بۆ چاودێریکردنی فرۆش و کارەکانی تیمەکەت لە مۆبایل یان کۆمپیوتەرەوە.',
                btnDetails: 'وردەکاری تەکنیکی',
                servicesTag: 'بوارەکانی پسپۆڕیمان',
                servicesTitle: 'چی پێشکەش بە پڕۆژەکەت دەکەین؟',
                servicesSub: 'چارەسەری ئەندازیاری کە هێزی ژیری دەستکرد و دیزاینی پڕۆفیشناڵی وێب کۆدەکاتەوە',
                s1Title: 'دروستکردنی پلاتفۆرمی ژیری دەستکرد',
                s1Desc: 'پەرەپێدانی پلاتفۆرم و ئەپڵیکەیشنی وێب بە پاڵپشتی ژیری دەستکرد (وەک VoltAI) بۆ پێشکەشکردنی خزمەتگوزاری نوێ.',
                s2Title: 'دروستکردنی ماڵپەڕ و پەڕەی فرۆشتن',
                s2Desc: 'دیزاین و پڕۆگرامسازی ماڵپەڕی خێرا و گونجاو لەگەڵ مۆبایل کە متمانەی کڕیارەکانت زیاد دەکات.',
                s3Title: 'گۆڕینی بیرۆکە بۆ پڕۆژەی ڕاستەقینە',
                s3Desc: 'لە سەرەتای پلانەوە تا بڵاوکردنەوەی تەواو لەسەر ئینتەرنێت لەگەڵت دەبین و تەواوی کۆدەکانت ڕادەست دەکەین.',
                faqTag: 'وەڵامی ڕوون',
                faqTitle: 'پرسیارە باوەکان',
                q1Title: 'دروستکردنی ماڵپەڕ یان پلاتفۆرم چەند کاتی دەوێت؟',
                q1Desc: 'ماڵپەڕی کۆمپانیا و پەڕەی فرۆشتن ٣ بۆ ٧ ڕۆژی دەوێت، و پلاتفۆرمەکانی ژیری دەستکرد ١ بۆ ٢ هەفتەیان دەوێت بەپێی تایبەتمەندییەکان.',
                q2Title: 'ئایا ماڵپەڕەکە بە باشی لەسەر هەموو مۆبایلەکان کار دەکات؟',
                q2Desc: 'بەڵێ، هەموو پڕۆژەکانمان بە تەواوی لەگەڵ شاشەی مۆبایلەکانی ئایفۆن و ئەندرۆید دەگونجێن بە خێراییەکی بەرز.',
                q3Title: 'ئایا تەواوی کۆد و خاوەندارێتی پڕۆژەکە وەردەگرم؟',
                q3Desc: 'بە دڵنیاییەوە، دوای تەواوبوونی پڕۆژەکە تەواوی کۆدەکان و فایلەکانت بە خاوەندارێتی ١٠٠٪ ڕادەست دەکرێت.',
                contactTitle: 'ڕاستەوخۆ پەیوەندیمان پێوە بکە',
                contactDesc: 'جۆری پڕۆژەکەت دیاری بکە بۆ ناردنی داواکاری خێرا لە واتسئەپ، یان ڕاستەوخۆ نامەمان بۆ بنێرە.',
                briefSelectLabel: '١. جۆری پڕۆژەکەت هەڵبژێرە:',
                typeAI: 'پلاتفۆرمی ژیری دەستکرد',
                typeWeb: 'ماڵپەڕی کۆمپانیا / کلینیک',
                typeCustom: 'سیستەمی تایبەت / پڕۆژەی تەواو',
                briefInputLabel: '٢. کورتەیەک دەربارەی بیرۆکەکەت (ئارەزوومەندانە):',
                briefPlaceholder: 'نموونە: دەمەوێت ماڵپەڕێک بۆ کلینیکەکەم دروست بکەم...',
                briefSendBtn: 'ناردنی زانیاری پڕۆژە لە واتسئەپ',
                chWhatsapp: 'واتسئەپ',
                chTelegram: 'تێلیگرام',
                chInstagram: 'ئینستاگرام',
                footerText: 'هەموو مافەکان پارێزراون &copy; 2026 <strong>BABYLON WEB</strong> — پەرەپێدانی پلاتفۆرمی ژیری دەستکرد و وێب | عێراق',
                modalClose: 'داخستن',
                modalOrder: 'داواکردنی نموونەی هاوشێوە',
                modals: {
                    p1: { title: 'سیستەمی خزمەتگوزاری کڕیاران', desc: 'سیستەمێکی تەواو بۆ دانانی یاریدەدەری زیرەک لەناو ماڵپەڕەکەتدا بۆ وەڵامدانەوەی خێرای پرسیاری کڕیاران بە درێژایی ٢٤ کاتژمێر.' },
                    p2: { title: 'ماڵپەڕی کۆمپانیا و سەنتەرە پزیشکییەکان', desc: 'دیزاینێکی خێرا و فەرمی کە تیشک دەخاتە سەر ناساندنی کۆمپانیا یان کلینیکەکەت و ئاسانکاری بۆ پەیوەندیکردنی کڕیاران.' },
                    p3: { title: 'داشبۆرد و بەڕێوەبردنی پڕۆژەکان', desc: 'دروستکردنی ڕووکاری وێب بۆ بەڕێوەبردنی داتا و کارەکانی تیمەکەت بە خێراییەکی بەرز لەسەر هەموو ئامێرەکان.' }
                }
            }
        };

        function setLanguage(lang) {
            currentLang = lang;
            const data = i18n[lang];
            document.documentElement.lang = lang;
            document.documentElement.dir = data.dir;

            document.querySelectorAll('.lang-btn').forEach(btn => btn.classList.remove('active'));
            document.getElementById('btn-' + lang).classList.add('active');

            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.getAttribute('data-i18n');
                if (data[key]) {
                    el.innerHTML = data[key];
                }
            });

            document.querySelectorAll('[data-i18n-placeholder]').forEach(el => {
                const key = el.getAttribute('data-i18n-placeholder');
                if (data[key]) {
                    el.placeholder = data[key];
                }
            });
        }

        function selectType(btn, type) {
            selectedProjectType = type;
            document.querySelectorAll('.type-pill').forEach(p => p.classList.remove('selected'));
            btn.classList.add('selected');
        }

        function sendWhatsAppBrief() {
            const typeNames = {
                ai: 'منصة ذكاء اصطناعي (AI Platform)',
                web: 'موقع تعريفي / عيادة / صفحة هبوط',
                custom: 'نظام خاص / مشروع رقمي متكامل'
            };
            const idea = document.getElementById('projectIdeaInput').value.trim();
            let text = `مرحباً فريق Babylon Web، أرغب بالاستفسار عن تنفيذ مشروع:\n- نوع المشروع: ${typeNames[selectedProjectType]}`;
            if (idea) {
                text += `\n- تفاصيل الفكرة: ${idea}`;
            }
            const url = `https://wa.me/9647850772200?text=${encodeURIComponent(text)}`;
            window.open(url, '_blank', 'noopener,noreferrer');
        }

        function openProject(key) {
            const modalData = i18n[currentLang].modals[key];
            document.getElementById('mTitle').innerText = modalData.title;
            document.getElementById('mDesc').innerText = modalData.desc;
            document.getElementById('projectModal').style.display = 'flex';
        }

        function closeProject() {
            document.getElementById('projectModal').style.display = 'none';
        }
    </script>
</body>
</html>
