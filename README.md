<DOCTYPE html>
<html lang="ar" dir="rtl" translate="no">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="google" content="notranslate">
    <title>Babylon Web | هندسة منصات الذكاء الاصطناعي وتطوير المواقع</title>
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 48 48'%3E%3Crect width='48' height='48' rx='12' fill='%230A0A0A'/%3E%3Cpath d='M12 34H36M15 28H33M18 22H30' stroke='%23E2C07D' stroke-width='3' stroke-linecap='round'/%3E%3C/svg%3E">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&display=swap" rel="stylesheet">
    <style>
        /* إخفاء أي عنوان تلقائي يضيفه GitHub Pages */
        .markdown-body > h1:first-child,
        .markdown-body > hr:first-of-type {
            display: none !important;
        }

        :root {
            --bg-base: #060709;
            --bg-surface: #0D0F14;
            --bg-panel: #14171F;
            --text-main: #FAFAFA;
            --text-muted: #A1A1AA;
            --accent: #E2C07D;
            --accent-hover: #EDD39E;
            --border-dim: #20242E;
            --border-strong: #343A4A;
            --radius: 8px;
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
            background-color: var(--bg-base);
            color: var(--text-main);
            font-family: 'IBM Plex Sans Arabic', sans-serif;
            line-height: 1.65;
            -webkit-font-smoothing: antialiased;
            overflow-x: hidden;
        }

        .en-font {
            font-family: 'Space Grotesk', sans-serif;
        }

        .container {
            max-width: 1160px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* Header */
        header {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(6, 7, 9, 0.92);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
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
            gap: 12px;
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
            color: var(--text-main);
        }

        .brand-text {
            display: flex;
            flex-direction: column;
            line-height: 1.2;
        }

        .brand-name {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.1rem;
            font-weight: 700;
            letter-spacing: 0.4px;
        }

        .brand-name span {
            color: var(--accent);
        }

        .brand-sub {
            font-size: 0.72rem;
            color: var(--text-muted);
        }

        .header-controls {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .lang-switcher {
            display: inline-flex;
            background: var(--bg-surface);
            border: 1px solid var(--border-dim);
            border-radius: var(--radius);
            padding: 3px;
            gap: 2px;
        }

        .lang-btn {
            background: transparent;
            border: none;
            color: var(--text-muted);
            font-family: inherit;
            font-size: 0.78rem;
            font-weight: 600;
            padding: 6px 10px;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.15s, color 0.15s;
        }

        .lang-btn.active {
            background: var(--accent);
            color: #060709;
        }

        .lang-btn:hover:not(.active) {
            color: var(--text-main);
        }

        /* Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            min-height: 44px;
            padding: 0 22px;
            font-family: inherit;
            font-size: 0.9rem;
            font-weight: 600;
            border-radius: var(--radius);
            text-decoration: none;
            cursor: pointer;
            border: 1px solid transparent;
            transition: background 0.15s, border-color 0.15s, transform 0.1s;
        }

        .btn:active {
            transform: translateY(1px);
        }

        .btn-primary {
            background: var(--accent);
            color: #060709;
        }

        .btn-primary:hover {
            background: var(--accent-hover);
        }

        .btn-secondary {
            background: var(--bg-surface);
            color: var(--text-main);
            border-color: var(--border-dim);
        }

        .btn-secondary:hover {
            background: var(--bg-panel);
            border-color: var(--border-strong);
        }

        /* Hero Section (Visible Immediately - Zero Opacity Trap) */
        .hero {
            padding: 72px 0 84px;
            border-bottom: 1px solid var(--border-dim);
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1.15fr 0.85fr;
            gap: 48px;
            align-items: center;
        }

        .hero-badge {
            display: inline-block;
            font-size: 0.8rem;
            font-weight: 500;
            color: var(--accent);
            background: rgba(226, 192, 125, 0.08);
            border: 1px solid rgba(226, 192, 125, 0.25);
            padding: 6px 14px;
            border-radius: 6px;
            margin-bottom: 22px;
        }

        .hero h1 {
            font-size: clamp(2rem, 4.2vw, 3.1rem);
            font-weight: 700;
            line-height: 1.25;
            margin-bottom: 18px;
        }

        .hero h1 span {
            color: var(--accent);
        }

        .hero-desc {
            font-size: 1.05rem;
            color: var(--text-muted);
            max-width: 540px;
            margin-bottom: 32px;
        }

        .hero-actions {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 40px;
        }

        .hero-facts {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 16px;
            padding-top: 24px;
            border-top: 1px solid var(--border-dim);
        }

        .fact-item strong {
            display: block;
            font-size: 0.95rem;
            color: var(--text-main);
            margin-bottom: 2px;
        }

        .fact-item span {
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        /* Live Architecture Card */
        .system-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-dim);
            border-radius: 12px;
            overflow: hidden;
        }

        .system-card-top {
            background: var(--bg-panel);
            padding: 12px 18px;
            border-bottom: 1px solid var(--border-dim);
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        .system-card-body {
            padding: 24px;
            display: flex;
            flex-direction: column;
            gap: 16px;
        }

        .sys-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-bottom: 12px;
            border-bottom: 1px solid var(--border-dim);
            font-size: 0.88rem;
        }

        .sys-row:last-of-type {
            border-bottom: none;
            padding-bottom: 0;
        }

        .sys-key {
            color: var(--text-muted);
        }

        .sys-val {
            color: var(--text-main);
            font-weight: 600;
        }

        .sys-val.gold {
            color: var(--accent);
        }

        /* Sections */
        .section {
            padding: 80px 0;
            border-bottom: 1px solid var(--border-dim);
        }

        .section-head {
            margin-bottom: 44px;
            max-width: 620px;
        }

        .section-tag {
            display: block;
            font-size: 0.8rem;
            font-weight: 600;
            color: var(--accent);
            margin-bottom: 8px;
        }

        .section-head h2 {
            font-size: clamp(1.6rem, 3vw, 2.2rem);
            font-weight: 700;
            margin-bottom: 10px;
        }

        .section-head p {
            color: var(--text-muted);
            font-size: 0.98rem;
        }

        /* Flagship Card */
        .flagship {
            background: var(--bg-surface);
            border: 1px solid var(--border-strong);
            border-radius: 12px;
            padding: 32px;
            margin-bottom: 28px;
        }

        .flagship-top {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            flex-wrap: wrap;
            gap: 16px;
            margin-bottom: 18px;
        }

        .flagship h3 {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 4px;
        }

        .flagship-sub {
            color: var(--accent);
            font-size: 0.9rem;
            font-weight: 500;
        }

        .flagship-desc {
            color: var(--text-muted);
            max-width: 780px;
            margin-bottom: 24px;
            font-size: 0.98rem;
        }

        .specs-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 16px;
            margin-bottom: 26px;
        }

        .spec-box {
            background: var(--bg-panel);
            border: 1px solid var(--border-dim);
            border-radius: var(--radius);
            padding: 16px;
        }

        .spec-box span {
            display: block;
            font-size: 0.78rem;
            color: var(--accent);
            font-weight: 600;
            margin-bottom: 6px;
        }

        .spec-box p {
            font-size: 0.88rem;
            color: var(--text-main);
        }

        .flagship-actions {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        /* Grid 3 */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .card {
            background: var(--bg-surface);
            border: 1px solid var(--border-dim);
            border-radius: 10px;
            padding: 26px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: border-color 0.2s, transform 0.2s;
        }

        .card:hover {
            border-color: var(--border-strong);
            transform: translateY(-2px);
        }

        .card-cat {
            font-size: 0.76rem;
            color: var(--accent);
            font-weight: 600;
            margin-bottom: 10px;
            display: block;
        }

        .card h3 {
            font-size: 1.15rem;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.92rem;
            margin-bottom: 22px;
        }

        /* FAQ */
        .faq-grid {
            display: grid;
            gap: 14px;
            max-width: 820px;
        }

        .faq-item {
            background: var(--bg-surface);
            border: 1px solid var(--border-dim);
            border-radius: var(--radius);
            padding: 20px 24px;
        }

        .faq-item h4 {
            font-size: 1.02rem;
            color: var(--text-main);
            margin-bottom: 6px;
        }

        .faq-item p {
            font-size: 0.92rem;
            color: var(--text-muted);
        }

        /* Contact & Brief Builder */
        .contact-grid {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 32px;
            align-items: start;
        }

        .brief-box {
            background: var(--bg-surface);
            border: 1px solid var(--border-dim);
            border-radius: 12px;
            padding: 28px;
        }

        .brief-label {
            display: block;
            font-size: 0.88rem;
            font-weight: 600;
            color: var(--text-main);
            margin-bottom: 10px;
        }

        .type-pills {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .type-pill {
            background: var(--bg-panel);
            border: 1px solid var(--border-dim);
            color: var(--text-muted);
            padding: 8px 14px;
            border-radius: 6px;
            font-family: inherit;
            font-size: 0.84rem;
            font-weight: 600;
            cursor: pointer;
            min-height: 40px;
            transition: all 0.15s;
        }

        .type-pill.selected {
            background: rgba(226, 192, 125, 0.15);
            border-color: var(--accent);
            color: var(--accent);
        }

        .brief-input {
            width: 100%;
            background: var(--bg-base);
            border: 1px solid var(--border-dim);
            border-radius: var(--radius);
            padding: 12px 14px;
            color: var(--text-main);
            font-family: inherit;
            font-size: 0.92rem;
            margin-bottom: 18px;
        }

        .brief-input:focus {
            outline: none;
            border-color: var(--accent);
        }

        .channels-stack {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .channel-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-dim);
            border-radius: 10px;
            padding: 18px 20px;
            text-decoration: none;
            color: var(--text-main);
            display: flex;
            justify-content: space-between;
            align-items: center;
            min-height: 68px;
            transition: border-color 0.2s, transform 0.2s;
        }

        .channel-card:hover {
            border-color: var(--accent);
            transform: translateY(-2px);
        }

        .channel-card strong {
            display: block;
            font-size: 0.95rem;
        }

        .channel-card span {
            font-size: 0.85rem;
            color: var(--accent);
            font-family: 'Space Grotesk', sans-serif;
            direction: ltr;
            display: inline-block;
        }

        /* Footer */
        footer {
            padding: 36px 0;
            text-align: center;
            color: var(--text-muted);
            font-size: 0.85rem;
        }

        footer strong {
            color: var(--accent);
            font-family: 'Space Grotesk', sans-serif;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.85);
            z-index: 999;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-strong);
            border-radius: 12px;
            max-width: 480px;
            width: 100%;
            padding: 28px;
        }

        .modal-card h3 {
            color: var(--accent);
            font-size: 1.25rem;
            margin-bottom: 10px;
        }

        .modal-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 22px;
        }

        .modal-actions {
            display: flex;
            gap: 10px;
            justify-content: flex-end;
        }

        /* Responsive */
        @media (max-width: 900px) {
            .hero-grid,
            .specs-grid,
            .grid-3,
            .contact-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 600px) {
            .brand-sub,
            .header-cta {
                display: none;
            }
            .hero {
                padding: 44px 0 56px;
            }
            .hero-facts {
                grid-template-columns: 1fr;
            }
            .hero-actions .btn {
                width: 100%;
            }
            .flagship {
                padding: 22px;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container nav-inner">
            <a href="#" class="brand">
                <svg width="34" height="34" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect x="2" y="2" width="44" height="44" rx="10" fill="#14171F" stroke="#E2C07D" stroke-width="2"/>
                    <path d="M13 33H35M16 26H32M19 19H29" stroke="#E2C07D" stroke-width="2.5" stroke-linecap="round"/>
                </svg>
                <div class="brand-text">
                    <span class="brand-name">BABYLON <span>WEB</span></span>
                    <span class="brand-sub" data-i18n="brandSub">هندسة الذكاء الاصطناعي والويب</span>
                </div>
            </a>

            <div class="header-controls">
                <div class="lang-switcher" role="group" aria-label="Language Switcher">
                    <button type="button" class="lang-btn active" onclick="setLanguage('ar')" id="btn-ar">العربية</button>
                    <button type="button" class="lang-btn" onclick="setLanguage('en')" id="btn-en">EN</button>
                    <button type="button" class="lang-btn" onclick="setLanguage('ku')" id="btn-ku">کوردی</button>
                </div>
                <a href="#contact" class="btn btn-primary header-cta" data-i18n="navCta">ابدأ مشروعك</a>
            </div>
        </div>
    </header>

    <main>
        <section class="hero">
            <div class="container hero-grid">
                <div>
                    <span class="hero-badge" data-i18n="statusPill">متاحون لاستقبال مشاريع المواقع ومنصات الذكاء الاصطناعي</span>
                    <h1 data-i18n="heroTitle">نحول أفكارك إلى <span>منصات ذكاء اصطناعي</span> ومواقع رقمية متكاملة</h1>
                    <p class="hero-desc" data-i18n="heroDesc">
                        في Babylon Web نصمم ونطور مواقع إلكترونية عالية الأداء، منصات مدعومة بالذكاء الاصطناعي، ومشاريع رقمية مخصصة تمنح عملك حضوراً موثوقاً وتجربة استخدام سلسة.
                    </p>
                    <div class="hero-actions">
                        <a href="#contact" class="btn btn-primary" data-i18n="heroBtnPrimary">اطلب بناء مشروعك</a>
                        <a href="#projects" class="btn btn-secondary" data-i18n="heroBtnSecondary">شاهد أعمالنا الحقيقية</a>
                    </div>
                    <div class="hero-facts">
                        <div class="fact-item">
                            <strong data-i18n="trust1Title">برمجة مخصصة</strong>
                            <span data-i18n="trust1Desc">أكواد نظيفة وسريعة بدون قوالب</span>
                        </div>
                        <div class="fact-item">
                            <strong data-i18n="trust2Title">تكامل الذكاء الاصطناعي</strong>
                            <span data-i18n="trust2Desc">ربط الأنظمة الذكية والأتمتة</span>
                        </div>
                        <div class="fact-item">
                            <strong data-i18n="trust3Title">ملكية كاملة للعميل</strong>
                            <span data-i18n="trust3Desc">تسليم الكود المصدري 100%</span>
                        </div>
                    </div>
                </div>

                <div class="system-card" aria-label="Production Architecture Overview">
                    <div class="system-card-top">
                        <span class="en-font">PRODUCTION STACK</span>
                        <span class="en-font">BABYLON-CORE</span>
                    </div>
                    <div class="system-card-body">
                        <div class="sys-row">
                            <span class="sys-key" data-i18n="cardRow1K">المنصة المنجزة</span>
                            <span class="sys-val gold en-font">VoltAI Platform</span>
                        </div>
                        <div class="sys-row">
                            <span class="sys-key" data-i18n="cardRow2K">زمن التنفيذ للمواقع</span>
                            <span class="sys-val" data-i18n="cardRow2V">3 - 7 أيام عمل</span>
                        </div>
                        <div class="sys-row">
                            <span class="sys-key" data-i18n="cardRow3K">التوافق مع الهواتف</span>
                            <span class="sys-val en-font">iOS / Android Ready</span>
                        </div>
                        <div class="sys-row">
                            <span class="sys-key" data-i18n="cardRow4K">تسليم الملكية</span>
                            <span class="sys-val" data-i18n="cardRow4V">كود مصدري + استضافة ودومين</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="projects" class="section">
            <div class="container">
                <div class="section-head">
                    <span class="section-tag" data-i18n="projectsTag">معرض الإنجازات</span>
                    <h2 data-i18n="projectsTitle">مشاريع ومنصات من تطويرنا</h2>
                    <p data-i18n="projectsSub">اطلع على مشاريعنا الفعلية والحلول البرمجية الجاهزة للتخصيص حسب نشاطك التجاري</p>
                </div>

                <div class="flagship">
                    <div class="flagship-top">
                        <div>
                            <h3 class="en-font">VoltAI Platform</h3>
                            <span class="flagship-sub" data-i18n="voltSubtitle">منصة ذكاء اصطناعي متكاملة للأتمتة والإنتاجية</span>
                        </div>
                        <span class="hero-badge" style="margin-bottom: 0;" data-i18n="voltBadge">مشروع حقيقي مُطلق | Live</span>
                    </div>

                    <p class="flagship-desc" data-i18n="voltDesc">
                        منصة VoltAI هي أحد مشاريعنا الهندسية المتكاملة في مجال الذكاء الاصطناعي؛ تم تطويرها لتوفير أدوات ذكية سريعة الاستجابة تساعد المستخدمين وأصحاب الأعمال على إنجاز المهام المعقدة، توليد المحتوى، وتحليل البيانات عبر واجهة عصرية فائقة السرعة.
                    </p>

                    <div class="specs-grid">
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
                        <a href="https://volt-ai.std24341059.workers.dev/" target="_blank" rel="noopener noreferrer" class="btn btn-primary" data-i18n="voltBtnVisit">زيارة منصة VoltAI مباشرة</a>
                        <a href="#contact" class="btn btn-secondary" data-i18n="voltBtnOrder">اطلب بناء منصة مماثلة</a>
                    </div>
                </div>

                <div class="grid-3">
                    <div class="card">
                        <div>
                            <span class="card-cat" data-i18n="p1Cat">مساعد ذكي للشركات</span>
                            <h3 data-i18n="p1Title">نظام خدمة العملاء الذكي</h3>
                            <p data-i18n="p1Desc">ربط موقعك بمساعد ذكاء اصطناعي مدرب على بيانات شركتك للرد على استفسارات الزبائن وحجز المواعيد تلقائياً.</p>
                        </div>
                        <button type="button" class="btn btn-secondary" onclick="openProject('p1')" data-i18n="btnDetails">تفاصيل البنية البرمجية</button>
                    </div>

                    <div class="card">
                        <div>
                            <span class="card-cat" data-i18n="p2Cat">منصات تجارية وعقارية</span>
                            <h3 data-i18n="p2Title">مواقع الشركات والمراكز الطبية</h3>
                            <p data-i18n="p2Desc">واجهات تعريفية رسمية عالية الثقة تعرض الخدمات والمشاريع مع ربط مباشر بقنوات التواصل والحجز.</p>
                        </div>
                        <button type="button" class="btn btn-secondary" onclick="openProject('p2')" data-i18n="btnDetails">تفاصيل البنية البرمجية</button>
                    </div>

                    <div class="card">
                        <div>
                            <span class="card-cat" data-i18n="p3Cat">أنظمة إدارة سحابية</span>
                            <h3 data-i18n="p3Title">لوحات التحكم وإدارة المشاريع</h3>
                            <p data-i18n="p3Desc">تطبيقات ويب مخصصة لمتابعة المبيعات، المهام، وتقارير الأداء من الهاتف أو الحاسوب بواجهة سهلة.</p>
                        </div>
                        <button type="button" class="btn btn-secondary" onclick="openProject('p3')" data-i18n="btnDetails">تفاصيل البنية البرمجية</button>
                    </div>
                </div>
            </div>
        </section>

        <section id="services" class="section">
            <div class="container">
                <div class="section-head">
                    <span class="section-tag" data-i18n="servicesTag">مجالات التخصص</span>
                    <h2 data-i18n="servicesTitle">ماذا نقدم لمشروعك؟</h2>
                    <p data-i18n="servicesSub">حلول هندسية تجمع بين قوة الذكاء الاصطناعي وتصميم الويب الاحترافي</p>
                </div>

                <div class="grid-3">
                    <div class="card">
                        <div>
                            <h3 data-i18n="s1Title">بناء منصات الذكاء الاصطناعي</h3>
                            <p style="margin-bottom: 0;" data-i18n="s1Desc">تطوير تطبيقات ومنصات ويب مدعومة بالذكاء الاصطناعي (مثل منصة VoltAI) لأتمتة الأعمال وتقديم خدمات رقمية مبتكرة.</p>
                        </div>
                    </div>

                    <div class="card">
                        <div>
                            <h3 data-i18n="s2Title">تطوير المواقع وصفحات الهبوط</h3>
                            <p style="margin-bottom: 0;" data-i18n="s2Desc">تصميم وبرمجة مواقع سريعة ومتجاوبة بالكامل مع الهواتف تعكس قوة علامتك التجارية وتزيد من ثقة عملائك.</p>
                        </div>
                    </div>

                    <div class="card">
                        <div>
                            <h3 data-i18n="s3Title">تحويل الأفكار إلى مشاريع رقمية</h3>
                            <p style="margin-bottom: 0;" data-i18n="s3Desc">نرافقك من التخطيط الأولي إلى إطلاق النسخة الكاملة على الإنترنت مع تسليم كافة الأكواد والملفات البرمجية.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="faq" class="section">
            <div class="container">
                <div class="section-head">
                    <span class="section-tag" data-i18n="faqTag">إجابات واضحة</span>
                    <h2 data-i18n="faqTitle">الأسئلة الشائعة</h2>
                </div>

                <div class="faq-grid">
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
            </div>
        </section>

        <section id="contact" class="section">
            <div class="container">
                <div class="section-head">
                    <span class="section-tag" data-i18n="contactTag">ابدأ التنفيذ</span>
                    <h2 data-i18n="contactTitle">تواصل معنا مباشرة لبدء مشروعك</h2>
                    <p data-i18n="contactDesc">حدد نوع مشروعك لإرسال طلب سريع عبر واتساب، أو تواصل معنا مباشرة عبر حساباتنا الرسمية.</p>
                </div>

                <div class="contact-grid">
                    <div class="brief-box">
                        <span class="brief-label" data-i18n="briefSelectLabel">1. اختر نوع المشروع المطلوب:</span>
                        <div class="type-pills">
                            <button type="button" class="type-pill selected" onclick="selectType(this, 'ai')" data-i18n="typeAI">منصة ذكاء اصطناعي</button>
                            <button type="button" class="type-pill" onclick="selectType(this, 'web')" data-i18n="typeWeb">موقع شركة / عيادة / صفحة هبوط</button>
                            <button type="button" class="type-pill" onclick="selectType(this, 'custom')" data-i18n="typeCustom">نظام خاص / مشروع متكامل</button>
                        </div>

                        <label for="projectIdeaInput" class="brief-label" data-i18n="briefInputLabel">2. نبذة قصيرة عن فكرتك (اختياري):</label>
                        <input type="text" id="projectIdeaInput" class="brief-input" placeholder="مثال: أرغب ببناء موقع تعريفي لعيادتي مع نظام حجز..." data-i18n-placeholder="briefPlaceholder">

                        <button type="button" onclick="sendWhatsAppBrief()" class="btn btn-primary" style="width: 100%;" data-i18n="briefSendBtn">إرسال تفاصيل المشروع عبر واتساب</button>
                    </div>

                    <div class="channels-stack">
                        <a href="https://wa.me/9647850772200" target="_blank" rel="noopener noreferrer" class="channel-card">
                            <div>
                                <strong data-i18n="chWhatsapp">واتساب مباشر</strong>
                                <span>+964 785 077 2200</span>
                            </div>
                            <span aria-hidden="true">&nearr;</span>
                        </a>

                        <a href="https://t.me/mzr_eng" target="_blank" rel="noopener noreferrer" class="channel-card">
                            <div>
                                <strong data-i18n="chTelegram">تليجرام</strong>
                                <span>@mzr_eng</span>
                            </div>
                            <span aria-hidden="true">&nearr;</span>
                        </a>

                        <a href="https://instagram.com/0dst" target="_blank" rel="noopener noreferrer" class="channel-card">
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

    <footer>
        <div class="container">
            <p data-i18n="footerText">جميع الحقوق محفوظة &copy; 2026 <strong>BABYLON WEB</strong> - تطوير منصات الذكاء الاصطناعي والحلول الرقمية | العراق</p>
        </div>
    </footer>

    <div id="projectModal" class="modal" onclick="closeProject()">
        <div class="modal-card" onclick="event.stopPropagation()">
            <h3 id="mTitle"></h3>
            <p id="mDesc"></p>
            <div class="modal-actions">
                <button type="button" class="btn btn-secondary" onclick="closeProject()" data-i18n="modalClose">إغلاق</button>
                <a href="#contact" class="btn btn-primary" onclick="closeProject()" data-i18n="modalOrder">اطلب نموذجاً مشابهاً</a>
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
                heroDesc: 'في Babylon Web نصمم ونطور مواقع إلكترونية عالية الأداء، منصات مدعومة بالذكاء الاصطناعي، ومشاريع رقمية مخصصة تمنح عملك حضوراً موثوقاً وتجربة استخدام سلسة.',
                heroBtnPrimary: 'اطلب بناء مشروعك',
                heroBtnSecondary: 'شاهد أعمالنا الحقيقية',
                trust1Title: 'برمجة مخصصة',
                trust1Desc: 'أكواد نظيفة وسريعة بدون قوالب',
                trust2Title: 'تكامل الذكاء الاصطناعي',
                trust2Desc: 'ربط الأنظمة الذكية والأتمتة',
                trust3Title: 'ملكية كاملة للعميل',
                trust3Desc: 'تسليم الكود المصدري 100%',
                cardRow1K: 'المنصة المنجزة',
                cardRow2K: 'زمن التنفيذ للمواقع',
                cardRow2V: '3 - 7 أيام عمل',
                cardRow3K: 'التوافق مع الهواتف',
                cardRow4K: 'تسليم الملكية',
                cardRow4V: 'كود مصدري + استضافة ودومين',
                projectsTag: 'معرض الإنجازات',
                projectsTitle: 'مشاريع ومنصات من تطويرنا',
                projectsSub: 'اطلع على مشاريعنا الفعلية والحلول البرمجية الجاهزة للتخصيص حسب نشاطك التجاري',
                voltBadge: 'مشروع حقيقي مُطلق | Live',
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
                contactTag: 'ابدأ التنفيذ',
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
                footerText: 'جميع الحقوق محفوظة &copy; 2026 <strong>BABYLON WEB</strong> - تطوير منصات الذكاء الاصطناعي والحلول الرقمية | العراق',
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
                trust1Desc: 'Clean, fast codebases without templates',
                trust2Title: 'AI Integration',
                trust2Desc: 'Smart automation & LLM integration',
                trust3Title: '100% Ownership',
                trust3Desc: 'Full source code handover',
                cardRow1K: 'Live Production',
                cardRow2K: 'Website Delivery',
                cardRow2V: '3 - 7 Business Days',
                cardRow3K: 'Mobile Optimization',
                cardRow4K: 'Handover',
                cardRow4V: 'Source Code + Domain Setup',
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
                contactTag: 'Get Started',
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
                footerText: 'All Rights Reserved &copy; 2026 <strong>BABYLON WEB</strong> - AI Platforms & Web Engineering | Iraq',
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
                cardRow1K: 'پلاتفۆرمی چالاک',
                cardRow2K: 'ماوەی جێبەجێکردن',
                cardRow2V: '٣ - ٧ ڕۆژی کارکردن',
                cardRow3K: 'گونجان لەگەڵ مۆبایل',
                cardRow4K: 'ڕادەستکردنی خاوەندارێتی',
                cardRow4V: 'کۆدی سەرچاوە + دۆمەین و هۆستینگ',
                projectsTag: 'پێشانگای کارەکانمان',
                projectsTitle: 'پڕۆژە و پلاتفۆرمە دروستکراوەکانمان',
                projectsSub: 'سەیری پڕۆژە ڕاستەقینەکانمان و نموونە ئامادەکانمان بکە کە بەپێی کارەکەت دەگونجێنرێن',
                voltBadge: 'پڕۆژەی ڕاستەقینە | Live',
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
                contactTag: 'دەستپێبکە',
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
                footerText: 'هەموو مافەکان پارێزراون &copy; 2026 <strong>BABYLON WEB</strong> - پەرەپێدانی پلاتفۆرمی ژیری دەستکرد و وێب | عێراق',
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
