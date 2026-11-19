<DOCTYPE html>
<html lang="ar" dir="rtl" translate="no" data-type="service" data-kind="tech">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="google" content="notranslate">
    <meta name="theme-color" content="#06070A">
    <title>Babylon Web | هندسة منصات الذكاء الاصطناعي وتطوير المواقع</title>
    <meta name="description" content="نبني منصات الذكاء الاصطناعي والمواقع الرقمية عالية الأداء للشركات ورواد الأعمال في العراق والمنطقة بملكية كاملة للكود المصدري.">
    <meta property="og:title" content="Babylon Web | هندسة منصات الذكاء الاصطناعي وتطوير المواقع">
    <meta property="og:description" content="تطوير منصات SaaS مدعومة بالذكاء الاصطناعي ومواقع الشركات السريعة بأكواد مخصصة.">
    <meta property="og:type" content="website">
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 48 48'%3E%3Crect width='48' height='48' rx='12' fill='%230E121B'/%3E%3Cpath d='M12 34H36M15 28H33M18 22H30' stroke='%23D9B36C' stroke-width='3' stroke-linecap='round'/%3E%3Cpath d='M24 11L30 17L24 22L18 17L24 11Z' stroke='%2338BDF8' stroke-width='2.5' fill='none'/%3E%3C/svg%3E">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@400;500;600;700&family=Space+Grotesk:wght@600;700&display=swap" rel="stylesheet">
    <style>
        .markdown-body > h1:first-child,
        .markdown-body > hr:first-of-type {
            display: none !important;
        }

        :root {
            --bg-primary: #06070A;
            --bg-surface: #0D1017;
            --bg-elevated: #131823;
            --gold-primary: #D9B36C;
            --gold-light: #F0D59B;
            --gold-dark: #9E7B3B;
            --tech-cyan: #38BDF8;
            --text-primary: #F8FAFC;
            --text-secondary: #94A3B8;
            --border-subtle: rgba(217, 179, 108, 0.16);
            --border-strong: rgba(217, 179, 108, 0.42);
            --radius-sm: 8px;
            --radius-md: 12px;
            --radius-lg: 18px;
            --wrap-max: 1140px;
            --ease-out: cubic-bezier(0.22, 1, 0.36, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            font-family: 'IBM Plex Sans Arabic', sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-primary);
        }

        body {
            line-height: 1.7;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 75% 0%, rgba(217, 179, 108, 0.09) 0%, transparent 48%),
                radial-gradient(circle at 15% 25%, rgba(56, 189, 248, 0.05) 0%, transparent 42%),
                linear-gradient(rgba(255, 255, 255, 0.015) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255, 255, 255, 0.015) 1px, transparent 1px);
            background-size: 100% 100%, 100% 100%, 48px 48px, 48px 48px;
        }

        .en-font {
            font-family: 'Space Grotesk', sans-serif;
            letter-spacing: 0.4px;
        }

        /* Accessibility Focus & Skip Link */
        :focus-visible {
            outline: 2px solid var(--gold-light);
            outline-offset: 3px;
        }

        .skip-link {
            position: fixed;
            top: -100px;
            inset-inline-start: 16px;
            background: var(--gold-primary);
            color: #06070A;
            padding: 12px 20px;
            border-radius: var(--radius-sm);
            font-weight: 700;
            z-index: 1000;
            text-decoration: none;
            transition: top 0.2s var(--ease-out);
        }

        .skip-link:focus {
            top: 16px;
        }

        /* Layout Container - Equal Edges */
        .wrap {
            width: 100%;
            max-width: var(--wrap-max);
            margin: 0 auto;
            padding-inline: 24px;
        }

        /* Header - Single Line <= 80px */
        header {
            position: sticky;
            top: 0;
            z-index: 100;
            height: 76px;
            background: rgba(6, 7, 10, 0.92);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid var(--border-subtle);
            display: flex;
            align-items: center;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 16px;
        }

        .brand {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
            min-height: 44px;
        }

        .brand-title {
            display: flex;
            flex-direction: column;
            line-height: 1.2;
        }

        .brand-title .en-name {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.15rem;
            font-weight: 700;
            color: var(--text-primary);
        }

        .brand-title .en-name span {
            color: var(--gold-primary);
        }

        .brand-title .ar-sub {
            font-size: 0.75rem;
            color: var(--text-secondary);
            font-weight: 500;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 24px;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 0.92rem;
            font-weight: 500;
            min-height: 44px;
            display: inline-flex;
            align-items: center;
            transition: color 0.15s ease;
        }

        .nav-links a:hover {
            color: var(--text-primary);
        }

        .header-controls {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        /* Language Switcher - 44px Tap Target */
        .lang-switcher {
            display: inline-flex;
            align-items: center;
            background: var(--bg-surface);
            border: 1px solid var(--border-subtle);
            border-radius: var(--radius-md);
            padding: 3px;
            gap: 2px;
        }

        .lang-btn {
            background: transparent;
            border: none;
            color: var(--text-secondary);
            font-family: inherit;
            font-size: 0.82rem;
            font-weight: 600;
            min-height: 38px;
            min-width: 44px;
            padding: 0 10px;
            border-radius: var(--radius-sm);
            cursor: pointer;
            transition: background-color 0.15s ease, color 0.15s ease;
        }

        .lang-btn.active {
            background: var(--gold-primary);
            color: #06070A;
        }

        .lang-btn:hover:not(.active) {
            color: var(--text-primary);
        }

        /* Buttons - Unified Shape & Hover Step */
        .btn-primary {
            background: linear-gradient(135deg, var(--gold-light), var(--gold-primary));
            color: #06070A;
            min-height: 46px;
            padding: 0 22px;
            border-radius: var(--radius-md);
            text-decoration: none;
            font-family: inherit;
            font-weight: 700;
            font-size: 0.94rem;
            border: none;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            transition: transform 0.15s var(--ease-out), box-shadow 0.15s var(--ease-out);
        }

        .btn-primary:hover {
            transform: translateY(-1px);
            box-shadow: 0 8px 24px rgba(217, 179, 108, 0.22);
        }

        .btn-primary:active {
            transform: translateY(0);
        }

        .btn-secondary {
            background: var(--bg-surface);
            color: var(--text-primary);
            min-height: 46px;
            padding: 0 22px;
            border-radius: var(--radius-md);
            text-decoration: none;
            font-family: inherit;
            font-weight: 600;
            font-size: 0.92rem;
            border: 1px solid var(--border-subtle);
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            transition: transform 0.15s var(--ease-out), border-color 0.15s ease, background-color 0.15s ease;
        }

        .btn-secondary:hover {
            transform: translateY(-1px);
            border-color: var(--gold-primary);
            background: var(--bg-elevated);
        }

        /* Split Hero - Fits First Screen Cleanly */
        .hero {
            min-height: calc(100vh - 76px);
            display: flex;
            align-items: center;
            padding-block: 48px;
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1.15fr 0.85fr;
            gap: 48px;
            align-items: center;
        }

        .hero-meta {
            display: inline-block;
            font-size: 0.84rem;
            font-weight: 600;
            color: var(--gold-primary);
            margin-bottom: 14px;
            letter-spacing: 0.3px;
        }

        .hero h1 {
            font-size: clamp(2rem, 3.8vw, 3.1rem);
            font-weight: 700;
            line-height: 1.25;
            margin-bottom: 18px;
        }

        .hero h1 span {
            color: var(--gold-light);
        }

        .hero-desc {
            color: var(--text-secondary);
            font-size: 1.05rem;
            max-width: 560px;
            margin-bottom: 28px;
        }

        .hero-actions {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            margin-bottom: 36px;
        }

        .hero-facts {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 16px;
            padding-top: 24px;
            border-top: 1px solid var(--border-subtle);
        }

        .fact-item strong {
            display: block;
            font-size: 1.05rem;
            color: var(--text-primary);
            font-weight: 700;
            margin-bottom: 2px;
        }

        .fact-item span {
            font-size: 0.82rem;
            color: var(--text-secondary);
        }

        /* Live Product UI Frame in Hero */
        .hero-showcase {
            background: var(--bg-surface);
            border: 1px solid var(--border-strong);
            border-radius: var(--radius-lg);
            padding: 20px;
            box-shadow: 0 24px 60px rgba(0, 0, 0, 0.55);
        }

        .window-top {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding-bottom: 14px;
            margin-bottom: 16px;
            border-bottom: 1px solid var(--border-subtle);
        }

        .window-title {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 0.85rem;
            font-weight: 700;
            color: var(--text-primary);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .window-tag {
            font-size: 0.74rem;
            color: var(--tech-cyan);
            background: rgba(56, 189, 248, 0.1);
            border: 1px solid rgba(56, 189, 248, 0.25);
            padding: 2px 8px;
            border-radius: 6px;
            font-weight: 600;
        }

        .ui-chat-stack {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .ui-msg {
            background: var(--bg-elevated);
            border: 1px solid var(--border-subtle);
            border-radius: var(--radius-md);
            padding: 12px 14px;
            font-size: 0.86rem;
        }

        .ui-msg-label {
            
