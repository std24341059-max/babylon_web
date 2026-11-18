<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Babylon Web | بابل ويب لتطوير المواقع</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-dark: #070B14;
            --bg-card: #0F172A;
            --gold: #D4AF37;
            --gold-light: #F3D06B;
            --lapis: #1E3A8A;
            --text-main: #F8FAFC;
            --text-muted: #94A3B8;
            --border-color: rgba(212, 175, 55, 0.2);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.7;
            overflow-x: hidden;
        }

        /* Navbar */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(7, 11, 20, 0.9);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
        }

        .logo-icon {
            width: 38px;
            height: 38px;
            background: linear-gradient(135deg, var(--gold), #9A7B1C);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 900;
            color: var(--bg-dark);
            font-size: 1.1rem;
        }

        .logo-text {
            font-size: 1.3rem;
            font-weight: 900;
            color: var(--text-main);
            letter-spacing: 0.5px;
        }

        .logo-text span {
            color: var(--gold);
        }

        nav {
            display: flex;
            gap: 25px;
        }

        nav a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 600;
            transition: 0.3s;
            font-size: 0.95rem;
        }

        nav a:hover {
            color: var(--gold);
        }

        .btn-gold {
            background: linear-gradient(135deg, var(--gold), #B89225);
            color: var(--bg-dark);
            padding: 10px 22px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 700;
            transition: 0.3s;
            border: none;
            cursor: pointer;
            display: inline-block;
        }

        .btn-gold:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(212, 175, 55, 0.3);
        }

        .btn-outline {
            border: 1.5px solid var(--gold);
            color: var(--gold);
            padding: 10px 22px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 700;
            transition: 0.3s;
            display: inline-block;
        }

        .btn-outline:hover {
            background: rgba(212, 175, 55, 0.1);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            padding: 130px 5% 80px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: radial-gradient(circle at top center, rgba(30, 58, 138, 0.35), transparent 60%);
        }

        .badge {
            background: rgba(212, 175, 55, 0.12);
            border: 1px solid var(--border-color);
            color: var(--gold-light);
            padding: 6px 18px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 20px;
        }

        .hero h1 {
            font-size: clamp(2rem, 5vw, 3.6rem);
            font-weight: 900;
            max-width: 850px;
            line-height: 1.3;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: var(--gold);
        }

        .hero p {
            color: var(--text-muted);
            font-size: 1.1rem;
            max-width: 650px;
            margin-bottom: 35px;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            justify-content: center;
        }

        /* Sections General */
        section {
            padding: 80px 5%;
        }

        .section-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-header h2 {
            font-size: 2.1rem;
            font-weight: 900;
            margin-bottom: 10px;
        }

        .section-header h2 span {
            color: var(--gold);
        }

        .section-header p {
            color: var(--text-muted);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Grid Layout */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
            gap: 25px;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Cards */
        .card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 30px;
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-6px);
            border-color: var(--gold);
        }

        .card-icon {
            font-size: 2.2rem;
            margin-bottom: 15px;
        }

        .card h3 {
            font-size: 1.3rem;
            margin-bottom: 12px;
            color: var(--text-main);
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Portfolio Cards */
        .portfolio-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            overflow: hidden;
            transition: 0.3s;
            display: flex;
            flex-direction: column;
        }

        .portfolio-card:hover {
            transform: translateY(-6px);
            border-color: var(--gold);
        }

        .portfolio-thumb {
            height: 180px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            font-weight: 900;
            position: relative;
        }

        .thumb-1 { background: linear-gradient(135deg, #0F766E, #115E59); }
        .thumb-2 { background: linear-gradient(135deg, #9A3412, #7C2D12); }
        .thumb-3 { background: linear-gradient(135deg, #1D4ED8, #1E3A8A); }

        .portfolio-tag {
            position: absolute;
            top: 12px;
            right: 12px;
            background: rgba(0, 0, 0, 0.6);
            color: var(--gold-light);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        .portfolio-body {
            padding: 25px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .portfolio-body h3 {
            font-size: 1.25rem;
            margin-bottom: 10px;
        }

        .portfolio-body p {
            color: var(--text-muted);
            font-size: 0.92rem;
            margin-bottom: 20px;
        }

        /* Contact Box */
        .contact-box {
            max-width: 750px;
            margin: 0 auto;
            background: linear-gradient(145deg, var(--bg-card), #0B1221);
            border: 1px solid var(--gold);
            border-radius: 20px;
            padding: 40px 25px;
            text-align: center;
        }

        .contact-box h2 {
            font-size: 1.9rem;
            margin-bottom: 15px;
        }

        .contact-box p {
            color: var(--text-muted);
            margin-bottom: 25px;
        }

        /* Footer */
        footer {
            border-top: 1px solid var(--border-color);
            padding: 30px 5%;
            text-align: center;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        footer span {
            color: var(--gold);
            font-weight: 700;
        }

        /* Modal for Demo Preview */
        .modal {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.85);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal-content {
            background: var(--bg-card);
            border: 1px solid var(--gold);
            border-radius: 16px;
            max-width: 500px;
            width: 100%;
            padding: 30px;
            text-align: center;
        }

        @media (max-width: 768px) {
            nav { display: none; }
            .hero { padding-top: 110px; }
        }
    </style>
</head>
<body>

    <!-- الشريط العلوي -->
    <header>
        <a href="#" class="logo">
            <div class="logo-icon">&lt;/&gt;</div>
            <div class="logo-text">Babylon <span>Web</span></div>
        </a>
        <nav>
            <a href="#home">الرئيسية</a>
            <a href="#services">خدماتنا</a>
            <a href="#portfolio">أعمالنا</a>
            <a href="#contact">تواصل معنا</a>
        </nav>
        <a href="#contact" class="btn-gold">اطلب موقعك</a>
    </header>

    <!-- القسم الرئيسي -->
    <section id="home" class="hero">
        <div class="badge">🇮🇶 استوديو تطوير مواقع رقمي من قلب العراق</div>
        <h1>نبني واجهتك الرقمية بمعايير عالمية و<span>هوية عريقة</span></h1>
        <p>في <strong>Babylon Web (بابل ويب)</strong>، نصمم ونبرمج مواقع إلكترونية سريعة، عصرية، ومتجاوبة مع جميع الهواتف لتعزز ثقة عملائك وتضاعف مبيعات مشروعك.</p>
        <div class="hero-buttons">
            <a href="#portfolio" class="btn-gold">شاهد نماذج أعمالنا</a>
            <a href="#services" class="btn-outline">استكشف خدماتنا</a>
        </div>
    </section>

    <!-- قسم الخدمات -->
    <section id="services">
        <div class="section-header">
            <h2>خدماتنا <span>البرمجية</span></h2>
            <p>حلول ويب متكاملة مصممة خصيصاً لأصحاب الأعمال، العيادات، المطاعم، والشركات الناشئة</p>
        </div>
        <div class="grid-3">
            <div class="card">
                <div class="card-icon">🏢</div>
                <h3>مواقع الشركات والعيادات</h3>
                <p>تصميم مواقع تعريفية رسمية تعرض خدماتك، فريق عملك، وموقعك الجغرافي مع أزرار حجز وتواصل مباشر عبر واتساب.</p>
            </div>
            <div class="card">
                <div class="card-icon">🚀</div>
                <h3>صفحات الهبوط (Landing Pages)</h3>
                <p>صفحات تسويقية مركزة وسريعة التحميل مصممة لتحويل زوار إعلاناتك إلى عملاء فعليين وزيادة مبيعاتك.</p>
            </div>
            <div class="card">
                <div class="card-icon">📱</div>
                <h3>تصميم متجاوب 100%</h3>
                <p>نضمن عمل موقعك بأعلى كفاءة وسلاسة على شاشات الهواتف الذكية والأجهزة اللوحية والحواسيب دون أي أخطاء.</p>
            </div>
        </div>
    </section>

    <!-- قسم الأعمال -->
    <section id="portfolio">
        <div class="section-header">
            <h2>نماذج من <span>أعمالنا</span></h2>
            <p>اطلع على أمثلة حية للمواقع التي نصممها لعملائنا في مختلف المجالات</p>
        </div>
        <div class="grid-3">
            <!-- مشروع 1 -->
            <div class="portfolio-card">
                <div class="portfolio-thumb thumb-1">
                    <span class="portfolio-tag">قطاع طبي</span>
                    🦷
                </div>
                <div class="portfolio-body">
                    <div>
                        <h3>عيادة دجلة لطب الأسنان</h3>
                        <p>موقع تعريفي متكامل لعيادة طبية يشمل عرض التخصصات، أوقات الدوام، ونظام حجز مواعيد سريع.</p>
                    </div>
                    <button class="btn-outline" onclick="openPreview('عيادة دجلة لطب الأسنان', 'نموذج موقع طبي احترافي جاهز للتخصيص بألوان عيادتك وأرقام التواصل الخاصة بك.')">معاينة التفاصيل</button>
                </div>
            </div>

            <!-- مشروع 2 -->
            <div class="portfolio-card">
                <div class="portfolio-thumb thumb-2">
                    <span class="portfolio-tag">مطاعم وكافيهات</span>
                    🍽️
                </div>
                <div class="portfolio-body">
                    <div>
                        <h3>مطعم شناشيل بغداد</h3>
                        <p>قائمة طعام رقمية (Digital Menu) تفاعلية تتيح للزبائن تصفح الوجبات والطلب مباشرة عبر الهاتف.</p>
                    </div>
                    <button class="btn-outline" onclick="openPreview('مطعم شناشيل بغداد', 'نموذج قائمة طعام رقمية وموقع تعريفي للمطاعم مع إمكانية مسح الكود QR.')">معاينة التفاصيل</button>
                </div>
            </div>

            <!-- مشروع 3 -->
            <div class="portfolio-card">
                <div class="portfolio-thumb thumb-3">
                    <span class="portfolio-tag">شركات وأعمال</span>
                    💼
                </div>
                <div class="portfolio-body">
                    <div>
                        <h3>شركة الرافدين للخدمات</h3>
                        <p>واجهة رقمية رسمية للشركات التجارية تعرض المشاريع المنجزة وتبني الثقة مع العملاء والشركاء.</p>
                    </div>
                    <button class="btn-outline" onclick="openPreview('شركة الرافدين للخدمات', 'تصميم رسمي موجه للشركات والمكاتب الهندسية والتجارية لعرض سابقة الأعمال.')">معاينة التفاصيل</button>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم التواصل -->
    <section id="contact">
        <div class="contact-box">
            <h2>جاهز لإطلاق موقعك الإلكتروني؟</h2>
            <p>تواصل مع فريق <strong>Babylon Web</strong> الآن لمناقشة فكرة مشروعك والحصول على تصميم احترافي خلال وقت قياسي.</p>
            <!-- يمكنك استبدال الرابط أدناه برابط حسابك في خمسات أو رقم الواتساب -->
            <a href="https://wa.me/9647700000000" target="_blank" class="btn-gold">تواصل معنا عبر واتساب 💬</a>
        </div>
    </section>

    <!-- التذييل -->
    <footer>
        <p>جميع الحقوق محفوظة &copy; 2026 <span>Babylon Web (بابل ويب)</span> | صُنع بشغف في العراق 🇮🇶</p>
    </footer>

    <!-- نافذة معاينة سريعة -->
    <div id="previewModal" class="modal" onclick="closePreview()">
        <div class="modal-content" onclick="event.stopPropagation()">
            <h3 id="modalTitle" style="color: var(--gold); margin-bottom: 12px; font-size: 1.4rem;"></h3>
            <p id="modalDesc" style="color: var(--text-muted); margin-bottom: 25px;"></p>
            <button class="btn-gold" onclick="closePreview()">إغلاق</button>
        </div>
    </div>

    <script>
        function openPreview(title, desc) {
            document.getElementById('modalTitle').innerText = title;
            document.getElementById('modalDesc').innerText = desc;
            document.getElementById('previewModal').style.display = 'flex';
        }
        function closePreview() {
            document.getElementById('previewModal').style.display = 'none';
        }
    </script>
</body>
</html>
