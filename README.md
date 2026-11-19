<!DOCTYPE html>
<html lang="ar" dir="rtl" translate="no">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="google" content="notranslate">
    <title>Babylon Web | منصات الذكاء الاصطناعي والويب</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@400;500;600&family=Space+Grotesk:wght@500;600&display=swap" rel="stylesheet">
    <style>
        /* CSS Reset & System Variables */
        :root {
            --bg-base: #000000;
            --bg-surface: #0A0A0A;
            --bg-panel: #111111;
            --text-main: #FFFFFF;
            --text-muted: #A1A1AA;
            --accent: #E2DFD2;
            --border-dim: #1F1F1F;
            --border-focus: #333333;
            --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: var(--bg-base);
            color: var(--text-main);
            font-family: 'IBM Plex Sans Arabic', sans-serif;
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            overflow-x: hidden;
        }

        .en-font {
            font-family: 'Space Grotesk', sans-serif;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* Calm Motion & Accessibility */
        @media (prefers-reduced-motion: no-preference) {
            html { scroll-behavior: smooth; }
            .hero-content > * {
                animation: fadeUp 0.8s var(--ease-out) forwards;
                opacity: 0;
                transform: translateY(12px);
            }
            .hero-content > *:nth-child(1) { animation-delay: 0.1s; }
            .hero-content > *:nth-child(2) { animation-delay: 0.2s; }
            .hero-content > *:nth-child(3) { animation-delay: 0.3s; }
        }

        @keyframes fadeUp {
            to { opacity: 1; transform: translateY(0); }
        }

        :focus-visible {
            outline: 2px solid var(--accent);
            outline-offset: 2px;
        }

        /* Strict Navigation (<= 80px) */
        header {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-dim);
            height: 72px;
            display: flex;
            align-items: center;
        }

        .nav-inner {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
        }

        .brand-logo {
            font-size: 1.125rem;
            font-weight: 600;
            letter-spacing: -0.02em;
            text-decoration: none;
            color: var(--text-main);
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .controls-group {
            display: flex;
            align-items: center;
            gap: 16px;
        }

        /* Precision Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            height: 44px; /* Strict Touch Target */
            padding: 0 20px;
            font-size: 0.875rem;
            font-weight: 500;
            border-radius: 6px;
            text-decoration: none;
            cursor: pointer;
            transition: background 0.2s var(--ease-out), transform 0.1s;
            border: 1px solid transparent;
        }

        .btn:active {
            transform: translateY(1px);
        }

        .btn-primary {
            background: var(--text-main);
            color: var(--bg-base);
        }

        .btn-primary:hover {
            background: #E4E4E7;
        }

        .btn-secondary {
            background: transparent;
            color: var(--text-main);
            border-color: var(--border-dim);
        }

        .btn-secondary:hover {
            background: var(--bg-panel);
            border-color: var(--border-focus);
        }

        /* Split Hero (One Section per Screen) */
        .hero-section {
            min-height: calc(100vh - 72px);
            display: flex;
            align-items: center;
            padding: 60px 0;
            border-bottom: 1px solid var(--border-dim);
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 64px;
            align-items: center;
        }

        .hero-label {
            display: inline-block;
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            color: var(--text-muted);
            border: 1px solid var(--border-dim);
            padding: 4px 12px;
            border-radius: 4px;
            margin-bottom: 24px;
        }

        .hero-title {
            font-size: clamp(2rem, 4vw, 3.5rem);
            line-height: 1.15;
            font-weight: 600;
            letter-spacing: -0.02em;
            margin-bottom: 20px;
        }

        .hero-desc {
            font-size: 1.125rem;
            color: var(--text-muted);
            max-width: 480px;
            margin-bottom: 40px;
            line-height: 1.5;
        }

        .hero-actions {
            display: flex;
            gap: 12px;
        }

        /* Real UI Fragment Mock (No abstract wireframes) */
        .ui-fragment {
            background: var(--bg-surface);
            border: 1px solid var(--border-dim);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 24px 48px rgba(0,0,0,0.4);
            display: flex;
            flex-direction: column;
        }

        .ui-header {
            height: 40px;
            border-bottom: 1px solid var(--border-dim);
            display: flex;
            align-items: center;
            padding: 0 16px;
            gap: 8px;
            background: var(--bg-panel);
        }

        .ui-dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: var(--border-focus);
        }

        .ui-body {
            padding: 24px;
            font-family: 'Space Grotesk', monospace;
            font-size: 0.85rem;
            color: var(--text-muted);
            min-height: 320px;
            display: flex;
            flex-direction: column;
            gap: 16px;
        }

        .ui-line {
            display: flex;
            justify-content: space-between;
            border-bottom: 1px solid var(--border-dim);
            padding-bottom: 12px;
        }

        .ui-value { color: var(--text-main); }

        /* Structural Sections */
        .section-block {
            padding: 100px 0;
            border-bottom: 1px solid var(--border-dim);
        }

        .section-header {
            margin-bottom: 64px;
            max-width: 600px;
        }

        .section-header h2 {
            font-size: 2rem;
            font-weight: 600;
            margin-bottom: 16px;
        }

        .section-header p {
            color: var(--text-muted);
            font-size: 1.05rem;
        }

        /* Project Cards - Rigid Grid */
        .grid-2 {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 24px;
        }

        .project-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-dim);
            border-radius: 8px;
            padding: 32px;
            transition: border-color 0.2s;
        }

        .project-card:hover {
            border-color: var(--border-focus);
        }

        .project-card h3 {
            font-size: 1.25rem;
            font-weight: 500;
            margin-bottom: 12px;
        }

        .project-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 24px;
        }

        /* Footer */
        footer {
            padding: 40px 0;
            text-align: center;
            color: var(--text-muted);
            font-size: 0.85rem;
        }

        @media (max-width: 900px) {
            .hero-grid { grid-template-columns: 1fr; gap: 40px; }
            .grid-2 { grid-template-columns: 1fr; }
            .hero-section { min-height: auto; padding: 40px 0; }
        }
    </style>
</head>
<body>

    <header>
        <div class="container nav-inner">
            <a href="#" class="brand-logo en-font">
                BABYLON WEB
            </a>
            <div class="controls-group">
                <a href="#contact" class="btn btn-primary" data-i18n="navCta">بدء مشروع</a>
            </div>
        </div>
    </header>

    <main>
        <section class="hero-section">
            <div class="container hero-grid">
                <div class="hero-content">
                    <span class="hero-label" data-i18n="heroLabel">أعمال هندسية وتقنية</span>
                    <h1 class="hero-title" data-i18n="heroTitle">منصات ذكاء اصطناعي ومواقع مصممة للنمو</h1>
                    <p class="hero-desc" data-i18n="heroDesc">
                        نصمم مواقع إلكترونية ومنصات ذكاء اصطناعي تمنح عملك حضوراً موثوقاً وتجربة استخدام استثنائية، بأكواد نظيفة وأداء فائق.
                    </p>
                    <div class="hero-actions">
                        <a href="#contact" class="btn btn-primary" data-i18n="heroBtnPrimary">طلب استشارة معمارية</a>
                        <a href="#projects" class="btn btn-secondary" data-i18n="heroBtnSecondary">المشاريع الحية</a>
                    </div>
                </div>
                
                <!-- Real UI Fragment Representation (Anti-Slop) -->
                <div class="ui-fragment" aria-hidden="true">
                    <div class="ui-header">
                        <div class="ui-dot"></div><div class="ui-dot"></div><div class="ui-dot"></div>
                    </div>
                    <div class="ui-body">
                        <div class="ui-line">
                            <span>System.Architecture</span>
                            <span class="ui-value">VoltAI_v2</span>
                        </div>
                        <div class="ui-line">
                            <span>Latency.Average</span>
                            <span class="ui-value">42ms</span>
                        </div>
                        <div class="ui-line">
                            <span>LLM.Integration</span>
                            <span class="ui-value">Active</span>
                        </div>
                        <div style="margin-top: auto; padding: 12px; background: rgba(255,255,255,0.03); border-radius: 4px;">
                            > Deployment successful. All systems operational.
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="projects" class="section-block">
            <div class="container">
                <div class="section-header">
                    <h2 data-i18n="projectsTitle">بنية تحتية موثوقة</h2>
                    <p data-i18n="projectsSub">حلول برمجية جاهزة للتخصيص الكامل حسب متطلبات نشاطك التجاري.</p>
                </div>

                <div class="grid-2">
                    <div class="project-card">
                        <h3 data-i18n="p1Title">منصة VoltAI</h3>
                        <p data-i18n="voltDesc">منصة ذكاء اصطناعي متكاملة للأتمتة، توفر أدوات استجابة فورية لمعالجة الأوامر وتوليد المحتوى وتحليل البيانات.</p>
                        <a href="https://volt-ai.std24341059.workers.dev/" target="_blank" class="btn btn-secondary">عرض المنصة</a>
                    </div>
                    
                    <div class="project-card">
                        <h3 data-i18n="p2Title">بوابات الشركات والخدمات الطبية</h3>
                        <p data-i18n="p2Desc">مواقع رسمية سريعة التحميل تعرض الخدمات والمشاريع مع ربط مباشر بقنوات الحجز الآلي وأنظمة الدعم.</p>
                        <a href="#contact" class="btn btn-secondary">تفاصيل البنية</a>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p data-i18n="footerText">جميع الحقوق محفوظة &copy; 2026 BABYLON WEB - تطوير المنصات الرقمية | العراق</p>
        </div>
    </footer>

</body>
</html>
