<DOCTYPE html>
<html lang="ar" dir="rtl" translate="no">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="google" content="notranslate">
    <title>Babylon Web | هندسة منصات الذكاء الاصطناعي وتطوير المواقع</title>
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 48 48'%3E%3Crect width='48' height='48' rx='12' fill='%23421d24'/%3E%3Cpath d='M13 33H35M16 26H32M19 19H29' stroke='%23f2f0eb' stroke-width='3' stroke-linecap='round'/%3E%3C/svg%3E">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@400;500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* إخفاء أي عنوان تلقائي يضيفه GitHub Pages */
        .markdown-body > h1:first-child,
        .markdown-body > hr:first-of-type {
            display: none !important;
        }

        :root {
            /* Superhuman Editorial Palette */
            --color-midnight-wine: #421d24;
            --color-royal-violet: #714cb6;
            --color-lilac-mist: #d4c7ff;
            --color-deep-lagoon: #0c4243;
            --color-warm-parchment: #f2f0eb;
            --color-soft-mist: #e3e3e2;
            --color-ink-charcoal: #292827;
            --color-stone-gray: #666666;
            --color-paper-white: #ffffff;

            /* Radii */
            --radius-sm: 8px;
            --radius-md: 12px;
            --radius-lg: 16px;
            --radius-pill: 999px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--color-warm-parchment);
            color: var(--color-ink-charcoal);
            font-family: 'IBM Plex Sans Arabic', 'Inter', sans-serif;
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            overflow-x: hidden;
        }

        .en-font {
            font-family: 'Inter', sans-serif;
            font-feature-settings: "ss01" on, "tnum" on;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* Top Announcement Banner (Midnight Wine) */
        .top-banner {
            background-color: var(--color-midnight-wine);
            color: var(--color-paper-white);
            font-size: 0.85rem;
            padding: 10px 16px;
            text-align: center;
        }

        .top-banner-inner {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
        }

        .top-banner a {
            color: var(--color-paper-white);
            text-decoration: none;
            border: 1px solid rgba(255, 255, 255, 0.35);
            padding: 3px 12px;
            border-radius: var(--radius-pill);
            font-size: 0.78rem;
            transition: background 0.2s;
        }

        .top-banner a:hover {
            background: rgba(255, 255, 255, 0.12);
        }

        /* Sticky Header with Backdrop Blur */
        header {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(242, 240, 235, 0.82);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--color-soft-mist);
            height: 68px;
            display: flex;
            align-items: center;
        }

        .nav-inner {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            gap: 16px;
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            color: var(--color-ink-charcoal);
        }

        .brand-mark {
            width: 34px;
            height: 34px;
            background: var(--color-midnight-wine);
            border-radius: 9px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--color-warm-parchment);
        }

        .brand-name {
            font-family: 'Inter', sans-serif;
            font-size: 1.15rem;
            font-weight: 600;
            letter-spacing: -0.02em;
            color: var(--color-ink-charcoal);
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 28px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--color-ink-charcoal);
            font-size: 0.95rem;
            font-weight: 500;
            transition: color 0.2s;
        }

        .nav-links a:hover {
            color: var(--color-royal-violet);
        }

        .header-controls {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .lang-switcher {
            display: inline-flex;
            background: var(--color-paper-white);
            border: 1px solid var(--color-soft-mist);
            border-radius: var(--radius-sm);
            padding: 3px;
            gap: 2px;
        }

        .lang-btn {
            background: transparent;
            border: none;
            color: var(--color-stone-gray);
            font-family: inherit;
            font-size: 0.78rem;
            font-weight: 600;
            padding: 5px 9px;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.15s, color 0.15s;
        }

        .lang-btn.active {
            background: var(--color-lilac-mist);
            color: var(--color-ink-charcoal);
        }

        /* Superhuman Buttons */
        .btn-wine {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            min-height: 46px;
            padding: 0 22px;
            background-color: var(--color-midnight-wine);
            color: var(--color-paper-white);
            border: none;
            border-radius: var(--radius-lg);
            font-family: inherit;
            font-size: 0.95rem;
            font-weight: 500;
            text-decoration: none;
            cursor: pointer;
            transition: opacity 0.2s, transform 0.1s;
        }

        .btn-wine:hover {
            opacity: 0.92;
        }

        .btn-wine:active {
            transform: translateY(1px);
        }

        .btn-lilac {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            min-height: 40px;
            padding: 6px 16px;
            background-color: var(--color-lilac-mist);
            color: var(--color-ink-charcoal);
            border: 1px solid var(--color-ink-charcoal);
            border-radius: var(--radius-sm);
            font-family: inherit;
            font-size: 0.88rem;
            font-weight: 500;
            text-decoration: none;
            cursor: pointer;
            transition: background 0.2s, transform 0.1s;
        }

        .btn-lilac:hover {
            background-color: #c5b3ff;
        }

        .btn-ghost-white {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            min-height: 44px;
            padding: 8px 20px;
            background: transparent;
            color: var(--color-paper-white);
            border: 1px solid var(--color-paper-white);
            border-radius: var(--radius-sm);
            font-family: inherit;
            font-size: 0.92rem;
            font-weight: 500;
            text-decoration: none;
            cursor: pointer;
            transition: background 0.2s;
        }

        .btn-ghost-white:hover {
            background: rgba(255, 255, 255, 0.12);
        }

        .violet-link {
            color: var(--color-royal-violet);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            background: none;
            border: none;
            cursor: pointer;
            font-family: inherit;
        }

        .violet-link:hover {
            text-decoration: underline;
        }

        /* Editorial Hero with Warm Golden-Hour Atmosphere & Floating Glass UI */
        .hero-wrapper {
            padding: 20px 24px 0;
            max-width: 1248px;
            margin: 0 auto;
        }

        .hero-canvas {
            position: relative;
            border-radius: 24px;
            overflow: hidden;
            padding: 80px 40px;
            background: 
                radial-gradient(circle at 80% 25%, rgba(212, 199, 255, 0.55) 0%, transparent 50%),
                radial-gradient(circle at 18% 75%, rgba(229, 195, 166, 0.55) 0%, transparent 55%),
                linear-gradient(160deg, #ebe6dc 0%, #dfd7c8 50%, #d6cbb9 100%);
            border: 1px solid var(--color-soft-mist);
        }

        .hero-grid {
            max-width: 1120px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1.15fr 0.85fr;
            gap: 48px;
            align-items: center;
        }

        .hero-eyebrow {
            display: inline-block;
            font-size: 0.82rem;
            font-weight: 600;
            color: var(--color-midnight-wine);
            background: rgba(255, 255, 255, 0.7);
            border: 1px solid rgba(66, 29, 36, 0.15);
            padding: 5px 14px;
            border-radius: var(--radius-pill);
            margin-bottom: 20px;
        }

        .hero-canvas h1 {
            font-size: clamp(2.1rem, 4.5vw, 3.6rem);
            font-weight: 500;
            line-height: 1.12;
            letter-spacing: -0.025em;
            color: var(--color-ink-charcoal);
            margin-bottom: 20px;
        }

        .hero-desc {
            font-size: 1.08rem;
            color: var(--color-ink-charcoal);
            opacity: 0.85;
            max-width: 520px;
            margin-bottom: 32px;
            line-height: 1.65;
        }

        .hero-actions {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 14px;
        }

        /* Floating Translucent UI Cards (Signature Superhuman Move) */
        .floating-stack {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .floating-ui-card {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.6);
            border-radius: var(--radius-lg);
            padding: 18px 20px;
        }

        .floating-ui-head {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 8px;
            font-size: 0.82rem;
        }

        .ui-badge-lilac {
            background: var(--color-lilac-mist);
            color: var(--color-ink-charcoal);
            padding: 2px 10px;
            border-radius: var(--radius-pill);
            font-weight: 600;
            font-size: 0.75rem;
        }

        .floating-ui-card h3 {
            font-size: 1.02rem;
            font-weight: 600;
            color: var(--color-ink-charcoal);
            margin-bottom: 4px;
        }

        .floating-ui-card p {
            font-size: 0.88rem;
            color: var(--color-stone-gray);
        }

        /* Trust Strip Row (Square Monochrome Cells) */
        .trust-band {
            max-width: 1200px;
            margin: 40px auto 0;
            padding: 0 24px;
        }

        .trust-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            background: var(--color-paper-white);
            border: 1px solid var(--color-soft-mist);
        }

        .trust-cell {
            padding: 22px 16px;
            text-align: center;
            border-inline-end: 1px solid var(--color-soft-mist);
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .trust-cell:last-child {
            border-inline-end: none;
        }

        .trust-cell strong {
            font-size: 0.95rem;
            font-weight: 600;
            color: var(--color-ink-charcoal);
        }

        .trust-cell span {
            font-size: 0.8rem;
            color: var(--color-stone-gray);
            margin-top: 2px;
        }

        /* Editorial Sections */
        .section {
            padding: 80px 0;
        }

        .section-head {
            margin-bottom: 40px;
            max-width: 640px;
        }

        .section-head h2 {
            font-size: clamp(1.85rem, 3.5vw, 2.8rem);
            font-weight: 500;
            line-height: 1.12;
            letter-spacing: -0.02em;
            color: var(--color-ink-charcoal);
            margin-bottom: 12px;
        }

        .section-head p {
            color: var(--color-stone-gray);
            font-size: 1.02rem;
        }

        /* Suite Tab Strip + Product Cards */
        .suite-tabs {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            background: var(--color-paper-white);
            border: 1px solid var(--color-soft-mist);
            border-radius: var(--radius-sm);
            overflow: hidden;
            margin-bottom: 24px;
        }

        .suite-tab {
            padding: 16px;
            text-align: center;
            font-weight: 600;
            font-size: 0.95rem;
            color: var(--color-ink-charcoal);
            background: var(--color-paper-white);
            border: none;
            border-inline-end: 1px solid var(--color-soft-mist);
            cursor: pointer;
            font-family: inherit;
            transition: background 0.2s;
        }

        .suite-tab:last-child {
            border-inline-end: none;
        }

        .suite-tab.active {
            background: var(--color-lilac-mist);
        }

        .cards-grid-3 {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .suite-card {
            background: var(--color-paper-white);
            border: 1px solid var(--color-soft-mist);
            border-radius: var(--radius-lg);
            padding: 24px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: border-color 0.2s;
        }

        .suite-card:hover {
            border-color: var(--color-ink-charcoal);
        }

        .card-icon {
            width: 36px;
            height: 36px;
            border-radius: 8px;
            background: var(--color-warm-parchment);
            border: 1px solid var(--color-soft-mist);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--color-midnight-wine);
            margin-bottom: 16px;
        }

        .suite-card h3 {
            font-size: 1.18rem;
            font-weight: 600;
            color: var(--color-ink-charcoal);
            margin-bottom: 8px;
        }

        .suite-card p {
            font-size: 0.94rem;
            color: var(--color-stone-gray);
            margin-bottom: 20px;
            line-height: 1.6;
        }

        /* Dark Feature Band (Deep Lagoon #0c4243) — Flagship VoltAI Showcase */
        .dark-band {
            background-color: var(--color-deep-lagoon);
            color: var(--color-paper-white);
            padding: 88px 0;
            margin: 20px 0;
        }

        .dark-band-grid {
            display: grid;
            grid-template-columns: 0.95fr 1.05fr;
            gap: 56px;
            align-items: center;
        }

        /* Layered Geometric Collage Art (Left side of Dark Band) */
        .lagoon-collage {
            position: relative;
            background: rgba(255, 255, 255, 0.06);
            border: 1px solid rgba(255, 255, 255, 0.16);
            border-radius: 20px;
            padding: 28px;
            overflow: hidden;
        }

        .collage-layer-1 {
            background: rgba(212, 199, 255, 0.16);
            border: 1px solid rgba(212, 199, 255, 0.3);
            border-radius: 14px;
            padding: 20px;
            margin-bottom: 16px;
        }

        .collage-layer-2 {
            background: rgba(255, 255, 255, 0.92);
            color: var(--color-ink-charcoal);
            border-radius: 14px;
            padding: 20px;
        }

        .collage-row {
            display: flex;
            justify-content: space-between;
            padding: 8px 0;
            border-bottom: 1px solid var(--color-soft-mist);
            font-size: 0.86rem;
        }

        .collage-row:last-child {
            border-bottom: none;
        }

        .dark-band-content .tag-pill {
            display: inline-block;
            background: rgba(212, 199, 255, 0.18);
            color: var(--color-lilac-mist);
            padding: 5px 14px;
            border-radius: var(--radius-pill);
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 18px;
        }

        .dark-band-content h2 {
            font-size: clamp(2rem, 4vw, 3.2rem);
            font-weight: 500;
            line-height: 1.1;
            letter-spacing: -0.02em;
            margin-bottom: 18px;
            color: var(--color-paper-white);
        }

        .dark-band-content p {
            color: rgba(255, 255, 255, 0.82);
            font-size: 1.02rem;
            margin-bottom: 28px;
            line-height: 1.7;
        }

        .dark-band-actions {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        /* Atmospheric Gradient Banner (Superhuman Style) */
        .gradient-banner-wrap {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        .gradient-banner {
            border-radius: 24px;
            padding: 56px 44px;
            border: 1px solid var(--color-soft-mist);
            background:
                radial-gradient(circle at 68% 50%, rgba(113, 76, 182, 0.18) 0%, transparent 45%),
                radial-gradient(circle at 93% 50%, rgba(56, 189, 248, 0.16) 0%, transparent 40%),
                radial-gradient(circle at 30% 80%, rgba(212, 199, 255, 0.45) 0%, transparent 50%),
                var(--color-paper-white);
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 24px;
        }

        .gradient-banner h2 {
            font-size: clamp(1.6rem, 3.2vw, 2.5rem);
            font-weight: 500;
            color: var(--color-ink-charcoal);
            max-width: 620px;
            line-height: 1.2;
        }

        /* FAQ Accordion Cards */
        .faq-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .faq-card {
            background: var(--color-paper-white);
            border: 1px solid var(--color-soft-mist);
            border-radius: var(--radius-lg);
            padding: 24px;
        }

        .faq-card h4 {
            font-size: 1.05rem;
            font-weight: 600;
            color: var(--color-ink-charcoal);
            margin-bottom: 10px;
        }

        .faq-card p {
            font-size: 0.92rem;
            color: var(--color-stone-gray);
            line-height: 1.65;
        }

        /* Contact & WhatsApp Brief Section */
        .contact-grid {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 28px;
            align-items: start;
        }

        .brief-card {
            background: var(--color-paper-white);
            border: 1px solid var(--color-soft-mist);
            border-radius: var(--radius-lg);
            padding: 28px;
        }

        .brief-label {
            display: block;
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--color-ink-charcoal);
            margin-bottom: 10px;
        }

        .type-pills {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .type-pill {
            background: var(--color-warm-parchment);
            border: 1px solid var(--color-soft-mist);
            color: var(--color-ink-charcoal);
            padding: 8px 14px;
            border-radius: var(--radius-sm);
            font-family: inherit;
            font-size: 0.86rem;
            font-weight: 500;
            cursor: pointer;
            min-height: 42px;
            transition: all 0.15s;
        }

        .type-pill.selected {
            background: var(--color-lilac-mist);
            border-color: var(--color-ink-charcoal);
            font-weight: 600;
        }

        .brief-input {
            width: 100%;
            background: var(--color-warm-parchment);
            border: 1px solid var(--color-soft-mist);
            border-radius: var(--radius-sm);
            padding: 12px 14px;
            color: var(--color-ink-charcoal);
            font-family: inherit;
            font-size: 0.94rem;
            margin-bottom: 18px;
        }

        .brief-input:focus {
            outline: none;
            border-color: var(--color-royal-violet);
            background: var(--color-paper-white);
        }

        .channels-list {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .channel-item {
            background: var(--color-paper-white);
            border: 1px solid var(--color-soft-mist);
            border-radius: var(--radius-lg);
            padding: 18px 20px;
            text-decoration: none;
            color: var(--color-ink-charcoal);
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: border-color 0.2s;
        }

        .channel-item:hover {
            border-color: var(--color-ink-charcoal);
        }

        .channel-item strong {
            display: block;
            font-size: 0.96rem;
        }

        .channel-item span {
            font-size: 0.86rem;
            color: var(--color-royal-violet);
            font-family: 'Inter', sans-serif;
            direction: ltr;
            display: inline-block;
        }

        /* Midnight Wine Multi-Column Footer */
        footer {
            background-color: var(--color-midnight-wine);
            color: var(--color-paper-white);
            padding: 64px 0 48px;
            margin-top: 40px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 1.5fr 1fr 1fr;
            gap: 40px;
            padding-bottom: 40px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.14);
        }

        .footer-col h4 {
            font-size: 0.9rem;
            font-weight: 700;
            margin-bottom: 14px;
            color: var(--color-paper-white);
        }

        .footer-col p,
        .footer-col a {
            display: block;
            font-size: 0.88rem;
            color: rgba(255, 255, 255, 0.72);
            text-decoration: none;
            margin-bottom: 10px;
            line-height: 1.6;
        }

        .footer-col a:hover {
            color: var(--color-paper-white);
            text-decoration: underline;
        }

        .footer-bottom {
            padding-top: 24px;
            font-size: 0.84rem;
            color: rgba(255, 255, 255, 0.7);
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 12px;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(41, 40, 39, 0.65);
            backdrop-filter: blur(4px);
            z-index: 999;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal-card {
            background: var(--color-paper-white);
            border: 1px solid var(--color-soft-mist);
            border-radius: var(--radius-lg);
            max-width: 480px;
            width: 100%;
            padding: 28px;
        }

        .modal-card h3 {
            color: var(--color-ink-charcoal);
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 10px;
        }

        .modal-card p {
            color: var(--color-stone-gray);
            font-size: 0.95rem;
            margin-bottom: 22px;
            line-height: 1.65;
        }

        .modal-actions {
            display: flex;
            gap: 10px;
            justify-content: flex-end;
        }

        /* Responsive */
        @media (max-width: 920px) {
            .nav-links {
                display: none;
            }
            .hero-grid,
            .dark-band-grid,
            .cards-grid-3,
            .faq-grid,
            .contact-grid,
            .footer-grid {
                grid-template-columns: 1fr;
            }
            .trust-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .trust-cell:nth-child(2) {
                border-inline-end: none;
            }
            .trust-cell:nth-child(1),
            .trust-cell:nth-child(2) {
                border-bottom: 1px solid var(--color-soft-mist);
            }
        }

        @media (max-width: 600px) {
            .hero-wrapper {
                padding: 12px 16px 0;
            }
            .hero-canvas {
                padding: 44px 22px;
            }
            .header-cta {
                display: none;
            }
            .hero-actions .btn-wine,
            .hero-actions .btn-lilac {
                width: 100%;
            }
            .gradient-banner {
                padding: 36px 24px;
            }
        }
    </style>
</head>
<body>

    <!-- Top Wine Announcement Strip -->
    <div class="top-banner">
        <div class="top-banner-inner">
            <span data-i18n="bannerText">إطلاق منصة VoltAI — أحدث أنظمة الذكاء الاصطناعي من تطوير Babylon Web</span>
            <a href="https://volt-ai.std24341059.workers.dev/" target="_blank" rel="noopener noreferrer" data-i18n="bannerLink">تجربة المنصة</a>
        </div>
    </div>

    <!-- Sticky Frosted Parchment Header -->
    <header>
        <div class="container nav-inner">
            <a href="#" class="brand">
                <div class="brand-mark">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M4 18h16M6 13h12M8 8h8"/></svg>
                </div>
                <span class="brand-name">Babylon Web</span>
            </a>

            <nav class="nav-links" aria-label="Main Navigation">
                <a href="#suite" data-i18n="navServices">الحلول والخدمات</a>
                <a href="#voltai" data-i18n="navVolt">منصة VoltAI</a>
                <a href="#faq" data-i18n="navFaq">الأسئلة الشائعة</a>
            </nav>

            <div class="header-controls">
                <div class="lang-switcher" role="group" aria-label="Language Switcher">
                    <button type="button" class="lang-btn active" onclick="setLanguage('ar')" id="btn-ar">العربية</button>
                    <button type="button" class="lang-btn" onclick="setLanguage('en')" id="btn-en">EN</button>
                    <button type="button" class="lang-btn" onclick="setLanguage('ku')" id="btn-ku">کوردی</button>
                </div>
                <a href="#contact" class="btn-lilac header-cta" data-i18n="navCta">ابدأ مشروعك</a>
            </div>
        </div>
    </header>

    <main>
        <!-- Editorial Golden-Hour Hero with Floating Glass Product Cards -->
        <div class="hero-wrapper">
            <section class="hero-canvas">
                <div class="hero-grid">
                    <div>
                        <span class="hero-eyebrow" data-i18n="heroEyebrow">هندسة الذكاء الاصطناعي وتطوير الويب</span>
                        <h1 data-i18n="heroTitle">نصمم منصات الذكاء الاصطناعي والمواقع الرقمية بسرعة ودقة</h1>
                        <p class="hero-desc" data-i18n="heroDesc">
                            في Babylon Web نحول أفكارك إلى مواقع شركات عالية الأداء ومنصات ذكاء اصطناعي متكاملة تمنح عملك حضوراً موثوقاً وتجربة استخدام استثنائية.
                        </p>
                        <div class="hero-actions">
                            <a href="#contact" class="btn-wine">
                                <span data-i18n="heroBtnPrimary">اطلب بناء مشروعك</span>
                                <span aria-hidden="true">&larr;</span>
                            </a>
                            <a href="#voltai" class="btn-lilac" data-i18n="heroBtnSecondary">استكشف منصة VoltAI</a>
                        </div>
                    </div>

                    <!-- Floating Translucent Product UI Stack -->
                    <div class="floating-stack">
                        <div class="floating-ui-card">
                            <div class="floating-ui-head">
                                <span class="ui-badge-lilac en-font">VoltAI Live</span>
                                <span class="en-font" style="color: var(--color-stone-gray);">Production</span>
                            </div>
                            <h3 data-i18n="float1Title">منصة ذكاء اصطناعي متكاملة</h3>
                            <p data-i18n="float1Desc">أتمتة المهام وتوليد المحتوى عبر واجهة سريعة الاستجابة ومهيأة للهواتف.</p>
                        </div>

                        <div class="floating-ui-card">
                            <div class="floating-ui-head">
                                <span class="ui-badge-lilac" data-i18n="float2Tag">تسليم سريع</span>
                                <span class="en-font" style="color: var(--color-stone-gray);">3 - 7 Days</span>
                            </div>
                            <h3 data-i18n="float2Title">ملكية كاملة للكود المصدري</h3>
                            <p data-i18n="float2Desc">تطوير مخصص بدون قوالب مكررة مع ربط الاستضافة والدومين باسمك 100%.</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <!-- Monochrome Square Trust Strip -->
        <div class="trust-band">
            <div class="trust-grid">
                <div class="trust-cell">
                    <strong data-i18n="trust1Title">برمجة مخصصة</strong>
                    <span data-i18n="trust1Sub">أكواد نظيفة وسريعة</span>
                </div>
                <div class="trust-cell">
                    <strong data-i18n="trust2Title">تكامل الذكاء الاصطناعي</strong>
                    <span data-i18n="trust2Sub">ربط الأنظمة الذكية</span>
                </div>
                <div class="trust-cell">
                    <strong data-i18n="trust3Title">توافق تام للهواتف</strong>
                    <span class="en-font">iOS & Android First</span>
                </div>
                <div class="trust-cell">
                    <strong data-i18n="trust4Title">ملكية 100% للعميل</strong>
                    <span data-i18n="trust4Sub">تسليم كامل الملفات</span>
                </div>
            </div>
        </div>

        <!-- Suite Cards Section on Warm Parchment -->
        <section id="suite" class="section">
            <div class="container">
                <div class="section-head">
                    <h2 data-i18n="suiteTitle">منظومة حلول Babylon Web</h2>
                    <p data-i18n="suiteSub">نطور الأنظمة الرقمية والمواقع الاحترافية المصممة خصيصاً لتنمية أعمالك وزيادة ثقة عملائك.</p>
                </div>

                <div class="suite-tabs" role="tablist">
                    <button type="button" class="suite-tab active" onclick="filterSuite('all', this)" data-i18n="tabAll">جميع الحلول الهندسية</button>
                    <button type="button" class="suite-tab" onclick="filterSuite('ai', this)" data-i18n="tabAI">منصات الذكاء الاصطناعي</button>
                    <button type="button" class="suite-tab" onclick="filterSuite('web', this)" data-i18n="tabWeb">مواقع الشركات والأنظمة</button>
                </div>

                <div class="cards-grid-3">
                    <div class="suite-card" data-cat="ai">
                        <div>
                            <div class="card-icon">
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
                            </div>
                            <h3 data-i18n="s1Title">بناء منصات الذكاء الاصطناعي</h3>
                            <p data-i18n="s1Desc">تطوير تطبيقات ومنصات ويب مدعومة بنماذج الذكاء الاصطناعي لأتمتة الأعمال وتقديم خدمات رقمية حديثة.</p>
                        </div>
                        <button type="button" class="violet-link" onclick="openProject('p1')" data-i18n="learnMore">تفاصيل البنية البرمجية &larr;</button>
                    </div>

                    <div class="suite-card" data-cat="web">
                        <div>
                            <div class="card-icon">
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>
                            </div>
                            <h3 data-i18n="s2Title">مواقع الشركات والمراكز الطبية</h3>
                            <p data-i18n="s2Desc">واجهات تعريفية عالية الثقة تعرض خدماتك ومشاريعك مع ربط مباشر بقنوات التواصل ونظام حجز المواعيد.</p>
                        </div>
                        <button type="button" class="violet-link" onclick="openProject('p2')" data-i18n="learnMore">تفاصيل البنية البرمجية &larr;</button>
                    </div>

                    <div class="suite-card" data-cat="ai web">
                        <div>
                            <div class="card-icon">
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg>
                            </div>
                            <h3 data-i18n="s3Title">مساعد خدمة العملاء الذكي</h3>
                            <p data-i18n="s3Desc">ربط موقعك بمساعد ذكي مدرب على بيانات نشاطك التجاري للرد على استفسارات الزبائن على مدار الساعة.</p>
                        </div>
                        <button type="button" class="violet-link" onclick="openProject('p3')" data-i18n="learnMore">تفاصيل البنية البرمجية &larr;</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Deep Lagoon Dark Feature Band (#0c4243) — VoltAI Flagship Showcase -->
        <section id="voltai" class="dark-band">
            <div class="container dark-band-grid">
                <div class="lagoon-collage">
                    <div class="collage-layer-1">
                        <span class="en-font" style="font-size: 0.78rem; color: var(--color-lilac-mist); display: block; margin-bottom: 6px;">ARCHITECTURE OVERVIEW</span>
                        <strong style="font-size: 1.05rem; display: block;" data-i18n="voltBoxTitle">هندسة متكاملة من الصفر إلى الإطلاق</strong>
                    </div>
                    <div class="collage-layer-2">
                        <div class="collage-row">
                            <span style="color: var(--color-stone-gray);" data-i18n="voltSpec1Label">الفئة المستهدفة</span>
                            <strong data-i18n="voltSpec1Short">رواد الأعمال والفرق التقنية</strong>
                        </div>
                        <div class="collage-row">
                            <span style="color: var(--color-stone-gray);" data-i18n="voltSpec2Label">الأداء والتجاوب</span>
                            <strong class="en-font">Mobile-First UI</strong>
                        </div>
                        <div class="collage-row">
                            <span style="color: var(--color-stone-gray);" data-i18n="voltSpec3Label">دور Babylon Web</span>
                            <strong data-i18n="voltSpec3Short">الهوية + الواجهة + ربط AI</strong>
                        </div>
                    </div>
                </div>

                <div class="dark-band-content">
                    <span class="tag-pill" data-i18n="voltBadge">مشروع حقيقي مُطلق | Live Platform</span>
                    <h2 class="en-font">VoltAI Platform</h2>
                    <p data-i18n="voltDesc">
                        منصة VoltAI هي أحد مشاريعنا الهندسية المتكاملة في مجال الذكاء الاصطناعي؛ تم تطويرها لتوفير أدوات ذكية سريعة الاستجابة تساعد المستخدمين وأصحاب الأعمال على إنجاز المهام المعقدة، توليد المحتوى، وتحليل البيانات عبر واجهة عصرية فائقة السرعة.
                    </p>
                    <div class="dark-band-actions">
                        <a href="https://volt-ai.std24341059.workers.dev/" target="_blank" rel="noopener noreferrer" class="btn-ghost-white" data-i18n="voltBtnVisit">زيارة منصة VoltAI مباشرة</a>
                        <a href="#contact" class="btn-lilac" style="border-color: transparent;" data-i18n="voltBtnOrder">اطلب بناء منصة مماثلة</a>
                    </div>
                </div>
            </div>
        </section>

        <!-- FAQ Section -->
        <section id="faq" class="section">
            <div class="container">
                <div class="section-head">
                    <h2 data-i18n="faqTitle">إجابات واضحة قبل بدء العمل</h2>
                    <p data-i18n="faqSub">كل ما تحتاج معرفته حول مدة التنفيذ، التوافق مع الهواتف، وملكية الكود.</p>
                </div>

                <div class="faq-grid">
                    <div class="faq-card">
                        <h4 data-i18n="q1Title">كم يستغرق بناء الموقع أو المنصة؟</h4>
                        <p data-i18n="q1Desc">من 3 إلى 7 أيام للمواقع التعريفية وصفحات الهبوط، ومن أسبوع إلى أسبوعين لمنصات الذكاء الاصطناعي والأنظمة المخصصة.</p>
                    </div>
                    <div class="faq-card">
                        <h4 data-i18n="q2Title">هل يعمل بسلاسة على هواتف الآيفون والأندرويد؟</h4>
                        <p data-i18n="q2Desc">نعم، جميع مشاريعنا تُبنى بمنهجية التوافق الكامل مع شاشات الهواتف الذكية أولاً، مع سرعة تحميل عالية وتجربة تصفح مريحة.</p>
                    </div>
                    <div class="faq-card">
                        <h4 data-i18n="q3Title">هل أستلم ملكية الكود والمشروع بالكامل؟</h4>
                        <p data-i18n="q3Desc">بالتأكيد، عند الانتهاء يتم تسليمك كافة الأكواد المصدرية وربط الموقع بالاستضافة والدومين الخاص بك بملكية كاملة 100%.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Atmospheric Gradient Banner -->
        <div class="gradient-banner-wrap">
            <div class="gradient-banner">
                <h2 data-i18n="bannerCtaTitle">حوّل فكرتك الرقمية إلى منصة حقيقية جاهزة للعمل</h2>
                <a href="#contact" class="btn-wine" data-i18n="navCta">ابدأ مشروعك</a>
            </div>
        </div>

        <!-- Contact & WhatsApp Brief Builder -->
        <section id="contact" class="section">
            <div class="container">
                <div class="section-head">
                    <h2 data-i18n="contactTitle">تواصل معنا مباشرة لبدء مشروعك</h2>
                    <p data-i18n="contactDesc">حدد نوع مشروعك لإرسال طلب سريع عبر واتساب، أو تواصل معنا مباشرة عبر حساباتنا الرسمية.</p>
                </div>

                <div class="contact-grid">
                    <div class="brief-card">
                        <span class="brief-label" data-i18n="briefSelectLabel">1. اختر نوع المشروع المطلوب:</span>
                        <div class="type-pills">
                            <button type="button" class="type-pill selected" onclick="selectType(this, 'ai')" data-i18n="typeAI">منصة ذكاء اصطناعي</button>
                            <button type="button" class="type-pill" onclick="selectType(this, 'web')" data-i18n="typeWeb">موقع شركة / عيادة / صفحة هبوط</button>
                            <button type="button" class="type-pill" onclick="selectType(this, 'custom')" data-i18n="typeCustom">نظام خاص / مشروع متكامل</button>
                        </div>

                        <label for="projectIdeaInput" class="brief-label" data-i18n="briefInputLabel">2. نبذة قصيرة عن فكرتك (اختياري):</label>
                        <input type="text" id="projectIdeaInput" class="brief-input" placeholder="مثال: أرغب ببناء موقع تعريفي لعيادتي مع نظام حجز..." data-i18n-placeholder="briefPlaceholder">

                        <button type="button" onclick="sendWhatsAppBrief()" class="btn-wine" style="width: 100%;" data-i18n="briefSendBtn">إرسال تفاصيل المشروع عبر واتساب</button>
                    </div>

                    <div class="channels-list">
                        <a href="https://wa.me/9647850772200" target="_blank" rel="noopener noreferrer" class="channel-item">
                            <div>
                                <strong data-i18n="chWhatsapp">واتساب مباشر</strong>
                                <span>+964 785 077 2200</span>
                            </div>
                            <span aria-hidden="true">&nearr;</span>
                        </a>

                        <a href="https://t.me/mzr_eng" target="_blank" rel="noopener noreferrer" class="channel-item">
                            <div>
                                <strong data-i18n="chTelegram">تليجرام</strong>
                                <span>@mzr_eng</span>
                            </div>
                            <span aria-hidden="true">&nearr;</span>
                        </a>

                        <a href="https://instagram.com/0dst" target="_blank" rel="noopener noreferrer" class="channel-item">
                            <div>
                                <strong data-i18n="chInstagram">إنستغرام</strong>
                                <span>@0dst</span>
                            </div>
                            <span aria-hidden="true">&nearr;</span>
                        </a>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Midnight Wine Multi-Column Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <h4 class="en-font">Babylon Web</h4>
                    <p data-i18n="footerAbout">هندسة منصات الذكاء الاصطناعي وتطوير المواقع الرقمية عالية الأداء للشركات ورواد الأعمال في العراق والمنطقة.</p>
                </div>
                <div class="footer-col">
                    <h4 data-i18n="footerColLinks">الأقسام</h4>
                    <a href="#suite" data-i18n="navServices">الحلول والخدمات</a>
                    <a href="#voltai" data-i18n="navVolt">منصة VoltAI</a>
                    <a href="#faq" data-i18n="navFaq">الأسئلة الشائعة</a>
                </div>
                <div class="footer-col">
                    <h4 data-i18n="footerColDirect">تواصل مباشر</h4>
                    <a href="https://wa.me/9647850772200" target="_blank" rel="noopener noreferrer">WhatsApp: +964 785 077 2200</a>
                    <a href="https://t.me/mzr_eng" target="_blank" rel="noopener noreferrer">Telegram: @mzr_eng</a>
                    <a href="https://instagram.com/0dst" target="_blank" rel="noopener noreferrer">Instagram: @0dst</a>
                </div>
            </div>
            <div class="footer-bottom">
                <span data-i18n="footerRights">جميع الحقوق محفوظة &copy; 2026 BABYLON WEB - العراق</span>
                <span class="en-font">AI Platforms & Web Engineering</span>
            </div>
        </div>
    </footer>

    <!-- Details Modal -->
    <div id="projectModal" class="modal" onclick="closeProject()">
        <div class="modal-card" onclick="event.stopPropagation()">
            <h3 id="mTitle"></h3>
            <p id="mDesc"></p>
            <div class="modal-actions">
                <button type="button" class="btn-lilac" onclick="closeProject()" data-i18n="modalClose">إغلاق</button>
                <a href="#contact" class="btn-wine" onclick="closeProject()" data-i18n="modalOrder">اطلب نموذجاً مشابهاً</a>
            </div>
        </div>
    </div>

    <script>
        let currentLang = 'ar';
        let selectedProjectType = 'ai';

        const i18n = {
            ar: {
                dir: 'rtl',
                bannerText: 'إطلاق منصة VoltAI — أحدث أنظمة الذكاء الاصطناعي من تطوير Babylon Web',
                bannerLink: 'تجربة المنصة',
                navServices: 'الحلول والخدمات',
                navVolt: 'منصة VoltAI',
                navFaq: 'الأسئلة الشائعة',
                navCta: 'ابدأ مشروعك',
                heroEyebrow: 'هندسة الذكاء الاصطناعي وتطوير الويب',
                heroTitle: 'نصمم منصات الذكاء الاصطناعي والمواقع الرقمية بسرعة ودقة',
                heroDesc: 'في Babylon Web نحول أفكارك إلى مواقع شركات عالية الأداء ومنصات ذكاء اصطناعي متكاملة تمنح عملك حضوراً موثوقاً وتجربة استخدام استثنائية.',
                heroBtnPrimary: 'اطلب بناء مشروعك',
                heroBtnSecondary: 'استكشف منصة VoltAI',
                float1Title: 'منصة ذكاء اصطناعي متكاملة',
                float1Desc: 'أتمتة المهام وتوليد المحتوى عبر واجهة سريعة الاستجابة ومهيأة للهواتف.',
                float2Tag: 'تسليم سريع',
                float2Title: 'ملكية كاملة للكود المصدري',
                float2Desc: 'تطوير مخصص بدون قوالب مكررة مع ربط الاستضافة والدومين باسمك 100%.',
                trust1Title: 'برمجة مخصصة',
                trust1Sub: 'أكواد نظيفة وسريعة',
                trust2Title: 'تكامل الذكاء الاصطناعي',
                trust2Sub: 'ربط الأنظمة الذكية',
                trust3Title: 'توافق تام للهواتف',
                trust4Title: 'ملكية 100% للعميل',
                trust4Sub: 'تسليم كامل الملفات',
                suiteTitle: 'منظومة حلول Babylon Web',
                suiteSub: 'نطور الأنظمة الرقمية والمواقع الاحترافية المصممة خصيصاً لتنمية أعمالك وزيادة ثقة عملائك.',
                tabAll: 'جميع الحلول الهندسية',
                tabAI: 'منصات الذكاء الاصطناعي',
                tabWeb: 'مواقع الشركات والأنظمة',
                s1Title: 'بناء منصات الذكاء الاصطناعي',
                s1Desc: 'تطوير تطبيقات ومنصات ويب مدعومة بنماذج الذكاء الاصطناعي لأتمتة الأعمال وتقديم خدمات رقمية حديثة.',
                s2Title: 'مواقع الشركات والمراكز الطبية',
                s2Desc: 'واجهات تعريفية عالية الثقة تعرض خدماتك ومشاريعك مع ربط مباشر بقنوات التواصل ونظام حجز المواعيد.',
                s3Title: 'مساعد خدمة العملاء الذكي',
                s3Desc: 'ربط موقعك بمساعد ذكي مدرب على بيانات نشاطك التجاري للرد على استفسارات الزبائن على مدار الساعة.',
                learnMore: 'تفاصيل البنية البرمجية ←',
                voltBoxTitle: 'هندسة متكاملة من الصفر إلى الإطلاق',
                voltSpec1Label: 'الفئة المستهدفة',
                voltSpec1Short: 'رواد الأعمال والفرق التقنية',
                voltSpec2Label: 'الأداء والتجاوب',
                voltSpec3Label: 'دور Babylon Web',
                voltSpec3Short: 'الهوية + الواجهة + ربط AI',
                voltBadge: 'مشروع حقيقي مُطلق | Live Platform',
                voltDesc: 'منصة VoltAI هي أحد مشاريعنا الهندسية المتكاملة في مجال الذكاء الاصطناعي؛ تم تطويرها لتوفير أدوات ذكية سريعة الاستجابة تساعد المستخدمين وأصحاب الأعمال على إنجاز المهام المعقدة، توليد المحتوى، وتحليل البيانات عبر واجهة عصرية فائقة السرعة.',
                voltBtnVisit: 'زيارة منصة VoltAI مباشرة',
                voltBtnOrder: 'اطلب بناء منصة مماثلة',
                faqTitle: 'إجابات واضحة قبل بدء العمل',
                faqSub: 'كل ما تحتاج معرفته حول مدة التنفيذ، التوافق مع الهواتف، وملكية الكود.',
                q1Title: 'كم يستغرق بناء الموقع أو المنصة؟',
                q1Desc: 'من 3 إلى 7 أيام للمواقع التعريفية وصفحات الهبوط، ومن أسبوع إلى أسبوعين لمنصات الذكاء الاصطناعي والأنظمة المخصصة.',
                q2Title: 'هل يعمل بسلاسة على هواتف الآيفون والأندرويد؟',
                q2Desc: 'نعم، جميع مشاريعنا تُبنى بمنهجية التوافق الكامل مع شاشات الهواتف الذكية أولاً، مع سرعة تحميل عالية وتجربة تصفح مريحة.',
                q3Title: 'هل أستلم ملكية الكود والمشروع بالكامل؟',
                q3Desc: 'بالتأكيد، عند الانتهاء يتم تسليمك كافة الأكواد المصدرية وربط الموقع بالاستضافة والدومين الخاص بك بملكية كاملة 100%.',
                bannerCtaTitle: 'حوّل فكرتك الرقمية إلى منصة حقيقية جاهزة للعمل',
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
                footerAbout: 'هندسة منصات الذكاء الاصطناعي وتطوير المواقع الرقمية عالية الأداء للشركات ورواد الأعمال في العراق والمنطقة.',
                footerColLinks: 'الأقسام',
                footerColDirect: 'تواصل مباشر',
                footerRights: 'جميع الحقوق محفوظة © 2026 BABYLON WEB - العراق',
                modalClose: 'إغلاق',
                modalOrder: 'اطلب نموذجاً مشابهاً',
                modals: {
                    p1: { title: 'بناء منصات الذكاء الاصطناعي', desc: 'تطوير واجهات تفاعلية سريعة وربطها بنماذج الذكاء الاصطناعي لمعالجة النصوص والبيانات مع تجربة مستخدم سلسة على جميع الأجهزة.' },
                    p2: { title: 'مواقع الشركات والمراكز الطبية', desc: 'تصميم هندسي سريع التحميل يركز على إبراز هوية المؤسسة، عرض الخدمات والأطباء أو المشاريع، وتسهيل التواصل الفوري.' },
                    p3: { title: 'مساعد خدمة العملاء الذكي', desc: 'بنية برمجية تتيح تضمين مساعد ذكي داخل موقعك الإلكتروني للإجابة الفورية على أسئلة العملاء وحجز المواعيد تلقائياً.' }
                }
            },
            en: {
                dir: 'ltr',
                bannerText: 'VoltAI Launch — Next-gen AI productivity platform engineered by Babylon Web',
                bannerLink: 'Explore Live',
                navServices: 'Solutions',
                navVolt: 'VoltAI Platform',
                navFaq: 'FAQ',
                navCta: 'Start Project',
                heroEyebrow: 'AI Platforms & Web Engineering',
                heroTitle: 'We architect AI platforms and websites built for speed and trust',
                heroDesc: 'At Babylon Web, we transform ideas into high-performance company websites and integrated AI platforms engineered to scale your business.',
                heroBtnPrimary: 'Build Your Project',
                heroBtnSecondary: 'Explore VoltAI',
                float1Title: 'Integrated AI Platform',
                float1Desc: 'Task automation and content generation through a fast, mobile-ready interface.',
                float2Tag: 'Fast Delivery',
                float2Title: '100% Source Code Ownership',
                float2Desc: 'Custom engineering without templates, delivered with full domain and hosting setup.',
                trust1Title: 'Custom Engineering',
                trust1Sub: 'Clean, fast codebases',
                trust2Title: 'AI Integration',
                trust2Sub: 'Smart automation workflows',
                trust3Title: 'Mobile Optimized',
                trust4Title: '100% Ownership',
                trust4Sub: 'Full source code handover',
                suiteTitle: 'The Babylon Web Suite',
                suiteSub: 'Digital systems and professional websites tailored to grow your business and earn client trust.',
                tabAll: 'All Engineering Solutions',
                tabAI: 'AI Platforms',
                tabWeb: 'Corporate & Web Systems',
                s1Title: 'AI Platform Development',
                s1Desc: 'Building AI-powered web applications and SaaS tools to automate workflows and launch modern digital products.',
                s2Title: 'Corporate & Clinic Websites',
                s2Desc: 'High-trust websites showcasing your services and portfolio with direct mobile communication and booking.',
                s3Title: 'Smart Customer Assistant',
                s3Desc: 'Embedding custom AI assistants trained on your business data to answer client inquiries 24/7.',
                learnMore: 'Architecture details →',
                voltBoxTitle: 'End-to-End Engineering from Zero to Launch',
                voltSpec1Label: 'Target Audience',
                voltSpec1Short: 'Founders & Tech Teams',
                voltSpec2Label: 'Performance',
                voltSpec3Label: 'Babylon Web Scope',
                voltSpec3Short: 'Identity + UI/UX + AI',
                voltBadge: 'Live Production Project',
                voltDesc: 'VoltAI is one of our flagship AI engineering projects, built to deliver ultra-responsive intelligent tools that help entrepreneurs and teams automate workflows, generate content, and analyze data seamlessly.',
                voltBtnVisit: 'Visit VoltAI Live',
                voltBtnOrder: 'Request Similar Platform',
                faqTitle: 'Clear answers before we begin',
                faqSub: 'Everything you need to know about timelines, mobile optimization, and code ownership.',
                q1Title: 'How long does it take to build a website or platform?',
                q1Desc: '3 to 7 days for corporate websites and landing pages, and 1 to 2 weeks for custom AI platforms and web systems.',
                q2Title: 'Are all sites optimized for iOS and Android?',
                q2Desc: 'Yes, every project is engineered mobile-first for fast load speeds and clean responsive layouts across all phones.',
                q3Title: 'Do I receive 100% source code ownership?',
                q3Desc: 'Yes, upon completion we hand over all source files and connect everything to your own domain and hosting.',
                bannerCtaTitle: 'Turn your digital idea into a production-ready platform',
                contactTitle: 'Connect directly to start your project',
                contactDesc: 'Select your project type to send a quick brief via WhatsApp, or reach out through our official channels.',
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
                footerAbout: 'Engineering AI platforms and high-performance websites for businesses and founders in Iraq and the region.',
                footerColLinks: 'Navigation',
                footerColDirect: 'Direct Contact',
                footerRights: 'All Rights Reserved © 2026 BABYLON WEB - Iraq',
                modalClose: 'Close',
                modalOrder: 'Request Similar Build',
                modals: {
                    p1: { title: 'AI Platform Development', desc: 'Building fast interactive front-ends integrated with AI models for text and data processing across all devices.' },
                    p2: { title: 'Corporate & Clinic Websites', desc: 'Fast-loading corporate and medical websites focused on authority, clear service presentation, and instant conversion.' },
                    p3: { title: 'Smart Customer Assistant', desc: 'Custom web architecture embedding an AI assistant trained on your business knowledge base for 24/7 support.' }
                }
            },
            ku: {
                dir: 'rtl',
                bannerText: 'بڵاوکردنەوەی پلاتفۆرمی VoltAI — نوێترین سیستەمی ژیری دەستکرد لەلایەن Babylon Web',
                bannerLink: 'تاقیکردنەوە',
                navServices: 'خزمەتگوزارییەکان',
                navVolt: 'پلاتفۆرمی VoltAI',
                navFaq: 'پرسیارە باوەکان',
                navCta: 'پڕۆژەکەت دەستپێبکە',
                heroEyebrow: 'ئەندازیاری ژیری دەستکرد و وێب',
                heroTitle: 'پلاتفۆرمی ژیری دەستکرد و ماڵپەڕی پێشکەوتوو بە خێرایی و وردی دروست دەکەین',
                heroDesc: 'لە Babylon Web بیرۆکەکانت دەگۆڕین بۆ ماڵپەڕی کۆمپانیا و پلاتفۆرمی ژیری دەستکرد کە متمانە لای کڕیارەکانت دروست دەکات.',
                heroBtnPrimary: 'داواکردنی پڕۆژە',
                heroBtnSecondary: 'بینینی پلاتفۆرمی VoltAI',
                float1Title: 'پلاتفۆرمی ژیری دەستکرد',
                float1Desc: 'ئاسانکردنی کارەکان و دروستکردنی ناوەڕۆک لە ڕێگەی ڕووکارێکی خێرا و گونجاو بۆ مۆبایل.',
                float2Tag: 'جێبەجێکردنی خێرا',
                float2Title: 'خاوەندارێتی تەواوی کۆدەکان',
                float2Desc: 'پڕۆگرامسازی تایبەت بەبێ قاڵبی دووبارە لەگەڵ بەستنەوەی دۆمەین و هۆستینگ بە ناوی خۆت.',
                trust1Title: 'پڕۆگرامسازی تایبەت',
                trust1Sub: 'کۆدی خاوێن و خێرا',
                trust2Title: 'ژیری دەستکرد (AI)',
                trust2Sub: 'بەستنەوەی سیستەمی زیرەک',
                trust3Title: 'گونجان لەگەڵ مۆبایل',
                trust4Title: 'خاوەندارێتی ١٠٠٪',
                trust4Sub: 'ڕادەستکردنی تەواوی فایلەکان',
                suiteTitle: 'چارەسەرەکانی Babylon Web',
                suiteSub: 'سیستەمی دیجیتاڵی و ماڵپەڕی پڕۆفیشناڵ دروست دەکەین بۆ گەشەپێدانی کارەکانت.',
                tabAll: 'هەموو چارەسەرەکان',
                tabAI: 'پلاتفۆرمی ژیری دەستکرد',
                tabWeb: 'ماڵپەڕی کۆمپانیا و سیستەم',
                s1Title: 'دروستکردنی پلاتفۆرمی ژیری دەستکرد',
                s1Desc: 'پەرەپێدانی پلاتفۆرم و ئەپڵیکەیشنی وێب بە پاڵپشتی ژیری دەستکرد بۆ خێراکردنی کارەکان.',
                s2Title: 'ماڵپەڕی کۆمپانیا و کلینیکەکان',
                s2Desc: 'ڕووکاری فەرمی و متمانەپێکراو بۆ نمایشکردنی خزمەتگوزارییەکان و پەیوەندیکردنی خێرا.',
                s3Title: 'یاریدەدەری زیرەکی کڕیاران',
                s3Desc: 'بەستنەوەی ماڵپەڕەکەت بە یاریدەدەرێکی زیرەک بۆ وەڵامدانەوەی کڕیاران بە درێژایی ٢٤ کاتژمێر.',
                learnMore: 'وردەکاری تەکنیکی ←',
                voltBoxTitle: 'ئەندازیاری تەواو لە سەرەتاوە تا بڵاوکردنەوە',
                voltSpec1Label: 'بۆ کێ گونجاوە',
                voltSpec1Short: 'خاوەنکاران و تیمە تەکنیکییەکان',
                voltSpec2Label: 'خێرایی و گونجان',
                voltSpec3Label: 'ڕۆڵی Babylon Web',
                voltSpec3Short: 'ناسنامە + ڕووکار + AI',
                voltBadge: 'پڕۆژەی ڕاستەقینە | Live Platform',
                voltDesc: 'پلاتفۆرمی VoltAI یەکێکە لە پڕۆژە ئەندازیارییە تەواوەکانمان لە بواری ژیری دەستکرد؛ دروستکراوە بۆ دابینکردنی ئامرازی زیرەک و خێرا کە یارمەتی خاوەنکاران دەدات بۆ جێبەجێکردنی کارەکان.',
                voltBtnVisit: 'سەردانی پلاتفۆرمی VoltAI',
                voltBtnOrder: 'داواکردنی پلاتفۆرمی هاوشێوە',
                faqTitle: 'وەڵامی ڕوون پێش دەستپێکردن',
                faqSub: 'هەموو زانیارییەک دەربارەی کاتی جێبەجێکردن، گونجان لەگەڵ مۆبایل، و خاوەندارێتی کۆد.',
                q1Title: 'دروستکردنی ماڵپەڕ یان پلاتفۆرم چەند کاتی دەوێت؟',
                q1Desc: '٣ بۆ ٧ ڕۆژ بۆ ماڵپەڕی کۆمپانیا و پەڕەی فرۆشتن، و ١ بۆ ٢ هەفتە بۆ پلاتفۆرمەکانی ژیری دەستکرد.',
                q2Title: 'ئایا بە باشی لەسەر هەموو مۆبایلەکان کار دەکات؟',
                q2Desc: 'بەڵێ، هەموو پڕۆژەکانمان بە تەواوی لەگەڵ شاشەی مۆبایلەکانی ئایفۆن و ئەندرۆید دەگونجێن.',
                q3Title: 'ئایا تەواوی کۆد و خاوەندارێتی پڕۆژەکە وەردەگرم؟',
                q3Desc: 'بە دڵنیاییەوە، دوای تەواوبوونی پڕۆژەکە تەواوی کۆدەکان و فایلەکانت بە خاوەندارێتی ١٠٠٪ ڕادەست دەکرێت.',
                bannerCtaTitle: 'بیرۆکەکەت بگۆڕە بۆ پلاتفۆرمێکی ڕاستەقینە و ئامادە بۆ کار',
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
                footerAbout: 'ئەندازیاری پلاتفۆرمی ژیری دەستکرد و پەرەپێدانی ماڵپەڕی خێرا بۆ کۆمپانیا و خاوەنکاران لە عێراق.',
                footerColLinks: 'بەشەکان',
                footerColDirect: 'پەیوەندی ڕاستەوخۆ',
                footerRights: 'هەموو مافەکان پارێزراون © 2026 BABYLON WEB - عێراق',
                modalClose: 'داخستن',
                modalOrder: 'داواکردنی نموونەی هاوشێوە',
                modals: {
                    p1: { title: 'دروستکردنی پلاتفۆرمی ژیری دەستکرد', desc: 'پەرەپێدانی ڕووکاری خێرا و بەستنەوەی بە مۆدێلەکانی ژیری دەستکرد بۆ چارەسەرکردنی داتا لەسەر هەموو ئامێرەکان.' },
                    p2: { title: 'ماڵپەڕی کۆمپانیا و کلینیکەکان', desc: 'دیزاینێکی خێرا و فەرمی کە تیشک دەخاتە سەر ناساندنی کۆمپانیا یان کلینیکەکەت و ئاسانکاری بۆ پەیوەندیکردن.' },
                    p3: { title: 'یاریدەدەری زیرەکی کڕیاران', desc: 'سیستەمێکی تەواو بۆ دانانی یاریدەدەری زیرەک لەناو ماڵپەڕەکەتدا بۆ وەڵامدانەوەی خێرای پرسیاری کڕیاران.' }
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

        function filterSuite(category, btnEl) {
            document.querySelectorAll('.suite-tab').forEach(t => t.classList.remove('active'));
            btnEl.classList.add('active');

            document.querySelectorAll('.suite-card').forEach(card => {
                const cats = card.getAttribute('data-cat');
                if (category === 'all' || cats.includes(category)) {
                    card.style.display = 'flex';
                } else {
                    card.style.display = 'none';
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
