<!DOCTYPE html>
<html lang="ar" dir="rtl" translate="no">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="google" content="notranslate">
    <title>Babylon Web | هندسة منصات الذكاء الاصطناعي وتطوير المواقع</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@300;400;500;600;700&family=Space+Grotesk:wght@600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-primary: #06070A;
            --bg-surface: rgba(14, 17, 24, 0.82);
            --bg-card-hover: rgba(22, 27, 38, 0.95);
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
                radial-gradient(circle at 50% 0%, rgba(217, 179, 108, 0.11) 0%, transparent 55%),
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
            background: rgba(6, 7, 10, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid var(--border-subtle);
            padding: 14px 5%;
        }

        .nav-container {
            max-width: 1120px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
        }

        .brand-title {
            display: flex;
            flex-direction: column;
            line-height: 1.1;
        }

        .brand-title .en-name {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--text-primary);
            letter-spacing: 0.8px;
        }

        .brand-title .en-name span {
            color: var(--gold-primary);
        }

        .brand-title .ar-sub {
            font-size: 0.72rem;
            color: var(--text-secondary);
            font-weight: 500;
        }

        .nav-links {
            display: flex;
            gap: 28px;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 0.92rem;
            font-weight: 500;
            transition: color 0.25s;
        }

        .nav-links a:hover {
            color: var(--gold-primary);
        }

        /* Buttons */
        .btn-primary {
            background: linear-gradient(135deg, var(--gold-light), var(--gold-primary), var(--gold-dark));
            color: #06070A;
            padding: 11px 24px;
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
            padding: 11px 24px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.92rem;
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
            background: rgba(217, 179, 108, 0.07);
        }

        /* Bio-Focused Executive Hero */
        .hero {
            max-width: 1120px;
            margin: 0 auto;
            padding: 65px 5% 70px;
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
            margin-bottom: 26px;
        }

        .status-dot {
            width: 7px;
            height: 7px;
            background-color: #10B981;
            border-radius: 50%;
            box-shadow: 0 0 10px #10B981;
        }

        .hero-logo-emblem {
            margin-bottom: 22px;
            filter: drop-shadow(0 12px 30px rgba(217, 179, 108, 0.2));
        }

        .hero h1 {
            font-size: clamp(1.9rem, 4.8vw, 3.3rem);
            font-weight: 700;
            line-height: 1.3;
            max-width: 820px;
            margin-bottom: 18px;
            letter-spacing: -0.3px;
        }

        .hero h1 span {
            background: linear-gradient(135deg, var(--gold-light), var(--gold-primary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-bio-desc {
            color: var(--text-secondary);
            font-size: 1.05rem;
            max-width: 640px;
            margin-bottom: 32px;
            font-weight: 400;
        }

        .hero-actions {
            display: flex;
            gap: 14px;
            flex-wrap: wrap;
            justify-content: center;
            width: 100%;
            max-width: 480px;
            margin-bottom: 48px;
        }

        .hero-actions a, .hero-actions button {
            flex: 1;
            min-width: 190px;
        }

        /* Trust Metrics Bar */
        .trust-strip {
            width: 100%;
            max-width: 860px;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            background: var(--bg-surface);
            border: 1px solid var(--border-subtle);
            border-radius: 16px;
            padding: 20px 15px;
            backdrop-filter: blur(12px);
        }

        .trust-item {
            padding: 0 12px;
            border-left: 1px solid var(--border-subtle);
        }

        .trust-item:last-child {
            border-left: none;
        }

        .trust-item strong {
            display: block;
            font-size: 1.15rem;
            color: var(--gold-light);
            font-weight: 700;
            margin-bottom: 2px;
        }

        .trust-item span {
            font-size: 0.82rem;
            color: var(--text-secondary);
        }

        /* Sections */
        section {
            max-width: 1120px;
            margin: 0 auto;
            padding: 70px 5%;
        }

        .section-head {
            margin-bottom: 42px;
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

        /* Grid */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
            gap: 22px;
        }

        /* Service Cards */
        .service-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-subtle);
            border-radius: 18px;
            padding: 30px 26px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: "";
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--gold-primary), transparent);
            opacity: 0;
            transition: opacity 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
            border-color: var(--border-strong);
            background: var(--bg-card-hover);
        }

        .service-card:hover::before {
            opacity: 1;
        }

        .icon-box {
            width: 48px;
            height: 48px;
            border-radius: 12px;
            background: rgba(217, 179, 108, 0.1);
            border: 1px solid rgba(217, 179, 108, 0.25);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gold-primary);
            margin-bottom: 20px;
        }

        .service-card h3 {
            font-size: 1.2rem;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .service-card p {
            color: var(--text-secondary);
            font-size: 0.92rem;
            line-height: 1.7;
        }

        /* Portfolio Cards */
        .project-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-subtle);
            border-radius: 18px;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            border-color: var(--border-strong);
        }

        .project-visual {
            height: 175px;
            background: linear-gradient(145deg, #0D121D, #151C2C);
            border-bottom: 1px solid var(--border-subtle);
            padding: 18px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            position: relative;
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
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.2);
        }

        .project-category {
            font-size: 0.75rem;
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
            gap: 8px;
            margin-top: auto;
        }

        .wire-line {
            height: 8px;
            border-radius: 4px;
            background: rgba(255, 255, 255, 0.08);
        }

        .wire-accent {
            height: 28px;
            border-radius: 8px;
            background: linear-gradient(90deg, rgba(217, 179, 108, 0.22), rgba(56, 189, 248, 0.12));
            border: 1px solid rgba(217, 179, 108, 0.2);
        }

        .project-info {
            padding: 24px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .project-info h3 {
            font-size: 1.18rem;
            margin-bottom: 8px;
        }

        .project-info p {
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-bottom: 20px;
        }

        /* Workflow Steps */
        .process-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 18px;
        }

        .step-box {
            background: var(--bg-surface);
            border: 1px solid var(--border-subtle);
            border-radius: 14px;
            padding: 22px;
        }

        .step-num {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 0.85rem;
            font-weight: 700;
            color: var(--gold-primary);
            margin-bottom: 8px;
            display: block;
        }

        .step-box h4 {
            font-size: 1.05rem;
            margin-bottom: 6px;
        }

        .step-box p {
            font-size: 0.88rem;
            color: var(--text-secondary);
        }

        /* CTA Box */
        .cta-panel {
            background: linear-gradient(145deg, rgba(18, 22, 33, 0.95), rgba(9, 11, 16, 0.98));
            border: 1px solid var(--border-strong);
            border-radius: 22px;
            padding: 46px 28px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .cta-panel h2 {
            font-size: clamp(1.5rem, 3.5vw, 2.1rem);
            margin-bottom: 12px;
        }

        .cta-panel p {
            color: var(--text-secondary);
            max-width: 560px;
            margin: 0 auto 28px;
            font-size: 0.98rem;
        }

        /* Footer */
        footer {
            border-top: 1px solid var(--border-subtle);
            padding: 32px 5%;
            text-align: center;
            color: var(--text-secondary);
            font-size: 0.86rem;
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
            max-width: 480px;
            width: 100%;
            padding: 30px 24px;
            text-align: right;
        }

        .modal-card h3 {
            color: var(--gold-light);
            font-size: 1.3rem;
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

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .trust-strip {
                grid-template-columns: 1fr;
                gap: 16px;
            }
            .trust-item {
                border-left: none;
                border-bottom: 1px solid var(--border-subtle);
                padding-bottom: 14px;
            }
            .trust-item:last-child {
                border-bottom: none;
                padding-bottom: 0;
            }
        }
    </style>
</head>
<body>

    <!-- الشريط العلوي -->
    <header>
        <div class="nav-container">
            <a href="#" class="brand">
                <!-- شعار Babylon Web الهندسي المخصص -->
                <svg width="38" height="38" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
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
                    <span class="ar-sub">هندسة الذكاء الاصطناعي والويب</span>
                </div>
            </a>

            <nav class="nav-links">
                <a href="#services">الخدمات</a>
                <a href="#projects">نماذج المنصات</a>
                <a href="#workflow">آلية العمل</a>
                <a href="#contact">بدء مشروع</a>
            </nav>

            <a href="#contact" class="btn-primary">تواصل معنا</a>
        </div>
    </header>

    <!-- الواجهة الرئيسية (مصممة لتكون مثالية لرابط البايو) -->
    <section class="hero">
        <div class="status-pill">
            <span class="status-dot"></span>
            <span>نستقبل مشاريع تطوير المواقع ومنصات الذكاء الاصطناعي</span>
        </div>

        <!-- الشعار المركزي الكبير -->
        <div class="hero-logo-emblem">
            <svg width="74" height="74" viewBox="0 0 74 74" fill="none" xmlns="http://www.w3.org/2000/svg">
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

        <h1>نحول أفكارك إلى <span>منصات ذكاء اصطناعي</span> ومواقع رقمية متكاملة</h1>
        <p class="hero-bio-desc">
            في <strong class="en-font" style="color: var(--gold-light);">Babylon Web</strong> نصمم ونبني مواقع إلكترونية عالية الأداء، أنظمة مدعومة بالذكاء الاصطناعي، ومشاريع رقمية مخصصة تمنح علامتك التجارية حضوراً موثوقاً وتجربة استخدام استثنائية.
        </p>

        <div class="hero-actions">
            <a href="#contact" class="btn-primary">
                <span>اطلب بناء مشروعك</span>
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><line x1="19" y1="12" x2="5" y2="12"/><polyline points="12 19 5 12 12 5"/></svg>
            </a>
            <a href="#projects" class="btn-secondary">
                <span>استعراض النماذج</span>
            </a>
        </div>

        <!-- شريط الثقة -->
        <div class="trust-strip">
            <div class="trust-item">
                <strong>برمجة مخصصة</strong>
                <span>أكواد نظيفة وسريعة بدون قوالب مكررة</span>
            </div>
            <div class="trust-item">
                <strong>تكامل الذكاء الاصطناعي</strong>
                <span>ربط الأنظمة الذكية والأتمتة بمشروعك</span>
            </div>
            <div class="trust-item">
                <strong>ملكية كاملة للعميل</strong>
                <span>تسليم المشروع مع الكود المصدري بالكامل</span>
            </div>
        </div>
    </section>

    <!-- قسم الخدمات -->
    <section id="services">
        <div class="section-head">
            <span class="section-tag">مجالات التخصص</span>
            <h2>حلول تقنية مصممة للنمو</h2>
            <p>نجمع بين دقة الهندسة البرمجية وتقنيات الذكاء الاصطناعي الحديثة لبناء أصول رقمية حقيقية لمشروعك</p>
        </div>

        <div class="grid-3">
            <!-- خدمة 1 -->
            <div class="service-card">
                <div class="icon-box">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2a4 4 0 0 1 4 4v2a4 4 0 0 1-8 0V6a4 4 0 0 1 4-4z"/><path d="M16 14H8a4 4 0 0 0-4 4v2h16v-2a4 4 0 0 0-4-4z"/><circle cx="12" cy="6" r="1"/></svg>
                </div>
                <h3>تطوير منصات الذكاء الاصطناعي</h3>
                <p>بناء مساعدين أذكياء مخصصين لخدمة العملاء، أتمتة العمليات التجارية، وربط نماذج الذكاء الاصطناعي بواجهات استخدام سهلة ومباشرة.</p>
            </div>

            <!-- خدمة 2 -->
            <div class="service-card">
                <div class="icon-box">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>
                </div>
                <h3>تصميم وبرمجة المواقع الاحترافية</h3>
                <p>مواقع تعريفية للشركات، صفحات هبوط تسويقية عالية التحويل، ومنصات عرض خدمات بتصميم فائق السرعة ومتجاوب مع جميع الشاشات.</p>
            </div>

            <!-- خدمة 3 -->
            <div class="service-card">
                <div class="icon-box">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><polygon points="12 2 2 7 12 12 22 7 12 2"/><polyline points="2 17 12 22 22 17"/><polyline points="2 12 12 17 22 12"/></svg>
                </div>
                <h3>بناء المشاريع الرقمية المتكاملة</h3>
                <p>نأخذ فكرتك من مرحلة التخطيط إلى الإطلاق الفعلي عبر بناء النسخة الأولية (MVP) ولوحات الإدارة السحابية القابلة للتوسع مستقبلاً.</p>
            </div>
        </div>
    </section>

    <!-- قسم نماذج الأعمال -->
    <section id="projects">
        <div class="section-head">
            <span class="section-tag">معرض الهندسة الرقمية</span>
            <h2>نماذج من الأنظمة والمواقع</h2>
            <p>بنية برمجية حديثة قابلة للتخصيص الكامل لتناسب هوية مشروعك وأهدافك التجارية</p>
        </div>

        <div class="grid-3">
            <!-- مشروع 1 -->
            <div class="project-card">
                <div class="project-visual">
                    <div class="mockup-bar">
                        <div class="mockup-dots"><span></span><span></span><span></span></div>
                        <span class="project-category">منصة ذكاء اصطناعي</span>
                    </div>
                    <div class="mockup-wireframe">
                        <div class="wire-line" style="width: 65%;"></div>
                        <div class="wire-line" style="width: 45%;"></div>
                        <div class="wire-accent"></div>
                    </div>
                </div>
                <div class="project-info">
                    <div>
                        <h3>منصة أفق للمساعد الذكي</h3>
                        <p>واجهة ويب تفاعلية لربط الشركات بمساعد ذكاء اصطناعي يجيب على استفسارات العملاء ويحلل البيانات تلقائياً.</p>
                    </div>
                    <button class="btn-secondary" onclick="openProject('منصة أفق للمساعد الذكي', 'نظام متكامل يتيح لأصحاب الأعمال تدريب مساعد ذكي على بيانات شركتهم وتضمينه داخل موقعهم الإلكتروني للرد الفوري على الزبائن على مدار الساعة.')">تفاصيل البنية البرمجية</button>
                </div>
            </div>

            <!-- مشروع 2 -->
            <div class="project-card">
                <div class="project-visual">
                    <div class="mockup-bar">
                        <div class="mockup-dots"><span></span><span></span><span></span></div>
                        <span class="project-category">منصة أعمال ومبيعات</span>
                    </div>
                    <div class="mockup-wireframe">
                        <div class="wire-line" style="width: 75%;"></div>
                        <div class="wire-line" style="width: 50%;"></div>
                        <div class="wire-accent"></div>
                    </div>
                </div>
                <div class="project-info">
                    <div>
                        <h3>بوابة الرافدين للاستثمار والعقار</h3>
                        <p>منصة رقمية متطورة لعرض المشاريع التجارية والعقارية مع نظام تصفية ذكي وحجز معاينات مباشرة.</p>
                    </div>
                    <button class="btn-secondary" onclick="openProject('بوابة الرافدين للاستثمار والعقار', 'موقع مؤسسي سريع التحميل مصمم لبناء الثقة مع المستثمرين، يتضمن عرضاً تفصيلياً للمشاريع مع ربط مباشر بقنوات المبيعات.')">تفاصيل البنية البرمجية</button>
                </div>
            </div>

            <!-- مشروع 3 -->
            <div class="project-card">
                <div class="project-visual">
                    <div class="mockup-bar">
                        <div class="mockup-dots"><span></span><span></span><span></span></div>
                        <span class="project-category">نظام إدارة سحابي</span>
                    </div>
                    <div class="mockup-wireframe">
                        <div class="wire-line" style="width: 55%;"></div>
                        <div class="wire-line" style="width: 70%;"></div>
                        <div class="wire-accent"></div>
                    </div>
                </div>
                <div class="project-info">
                    <div>
                        <h3>نظام سومر لإدارة المشاريع</h3>
                        <p>لوحة تحكم حديثة لمتابعة المهام، تقارير الأداء، وإدارة فرق العمل من أي جهاز بواجهة عربية واضحة.</p>
                    </div>
                    <button class="btn-secondary" onclick="openProject('نظام سومر لإدارة المشاريع', 'تطبيق ويب متجاوب مصمم للشركات الناشئة لتنظيم سير العمل ومتابعة إنجاز المشاريع بدقة وسهولة من الهاتف أو الحاسوب.')">تفاصيل البنية البرمجية</button>
                </div>
            </div>
        </div>
    </section>

    <!-- خطوات العمل -->
    <section id="workflow">
        <div class="section-head">
            <span class="section-tag">منهجية التنفيذ</span>
            <h2>كيف نبني مشروعك؟</h2>
        </div>

        <div class="process-grid">
            <div class="step-box">
                <span class="step-num">01 / التحليل والتخطيط</span>
                <h4>فهم الفكرة والأهداف</h4>
                <p>نحدد معك متطلبات المشروع، الجمهور المستهدف، والميزات الأساسية بدقة قبل كتابة أي سطر برمجي.</p>
            </div>
            <div class="step-box">
                <span class="step-num">02 / الهوية والواجهة</span>
                <h4>تصميم تجربة المستخدم</h4>
                <p>نصمم واجهة عصرية تعكس قوة علامتك التجارية وتضمن سهولة التصفح على الهواتف والحواسيب.</p>
            </div>
            <div class="step-box">
                <span class="step-num">03 / التطوير والربط</span>
                <h4>البرمجة والذكاء الاصطناعي</h4>
                <p>نطور المنصة بأحدث التقنيات مع دمج أدوات الذكاء الاصطناعي والنماذج التفاعلية المطلوبة.</p>
            </div>
            <div class="step-box">
                <span class="step-num">04 / الإطلاق والتسليم</span>
                <h4>الاختبار والنشر الرسمي</h4>
                <p>نختبر سرعة وأمان الموقع بالكامل ثم نطلقه على الإنترنت ونسلمك كافة الملفات والصلاحيات.</p>
            </div>
        </div>
    </section>

    <!-- قسم التواصل -->
    <section id="contact">
        <div class="cta-panel">
            <h2>هل لديك فكرة مشروع أو منصة رقمية؟</h2>
            <p>تواصل مباشرة مع فريق <strong class="en-font" style="color: var(--gold-light);">Babylon Web</strong> لمناقشة تفاصيل مشروعك والحصول على تصور واضح وخطة تنفيذ احترافية.</p>
            <!-- استبدل الرقم أدناه برقم الواتساب الخاص بك بصيغة دولية بدون أصفار في البداية -->
            <a href="https://wa.me/9647700000000" target="_blank" class="btn-primary">
                <span>ابدأ محادثة مباشرة عبر واتساب</span>
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"/><polyline points="7 7 17 7 17 17"/></svg>
            </a>
        </div>
    </section>

    <!-- التذييل -->
    <footer>
        <p>جميع الحقوق محفوظة &copy; 2026 <strong>BABYLON WEB</strong> — تطوير منصات الذكاء الاصطناعي والحلول الرقمية | العراق</p>
    </footer>

    <!-- نافذة تفاصيل المشاريع -->
    <div id="projectModal" class="modal" onclick="closeProject()">
        <div class="modal-card" onclick="event.stopPropagation()">
            <h3 id="mTitle"></h3>
            <p id="mDesc"></p>
            <div class="modal-actions">
                <button class="btn-secondary" onclick="closeProject()">إغلاق</button>
                <a href="#contact" class="btn-primary" onclick="closeProject()">اطلب نموذجاً مشابهاً</a>
            </div>
        </div>
    </div>

    <script>
        function openProject(title, desc) {
            document.getElementById('mTitle').innerText = title;
            document.getElementById('mDesc').innerText = desc;
            document.getElementById('projectModal').style.display = 'flex';
        }
        function closeProject() {
            document.getElementById('projectModal').style.display = 'none';
        }
    </script>
</body>
</html>
