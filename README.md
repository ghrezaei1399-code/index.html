<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دکتر غلامرضا رضائی | خرد + فناوری</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/vazirmatn@33.003/font.css">
    <style>
        :root {
            --navy-blue: #0A2463;
            --deep-teal: #1A5276;
            --accent-gold: #D4AF37;
            --soft-blue: #3498DB;
            --literary-purple: #6A4C93;
            --light-bg: #F8F9FA;
            --card-shadow: rgba(10, 36, 99, 0.1);
        }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        /* رفع مشکل عرض صفحه */
        html, body { 
            width: 100% !important; 
            max-width: 100% !important; 
            overflow-x: hidden !important; 
        }
        
        body { 
            font-family: 'Vazirmatn', 'Segoe UI', sans-serif; 
            background: var(--light-bg); 
            color: #333; 
        }
        
        /* دکمه زبان در هدر */
        .lang-switcher {
            position: absolute;
            top: 25px;
            left: 25px;
            z-index: 1000;
        }
        .lang-btn {
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            color: white;
            border: 1px solid rgba(255, 255, 255, 0.3);
            padding: 8px 16px;
            border-radius: 20px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }
        .lang-btn:hover {
            background: var(--accent-gold);
            color: var(--navy-blue);
            transform: scale(1.05);
        }
        
        /* هدر اصلی */
        .main-header {
            background: linear-gradient(135deg, var(--navy-blue), var(--deep-teal));
            min-height: 50vh;
            padding: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            width: 100%;
        }
        .header-container {
            max-width: 100%;
            width: 100%;
            display: grid;
            grid-template-columns: 1fr 280px;
            gap: 30px;
            align-items: start;
            padding: 0 20px;
        }
        .profile-section {
            background: rgba(255, 255, 255, 0.12);
            backdrop-filter: blur(12px);
            border-radius: 20px;
            padding: 30px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            border: 1px solid rgba(255, 255, 255, 0.18);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        .profile-img-container {
            display: flex;
            align-items: center;
            gap: 25px;
            margin-bottom: 20px;
            width: 100%;
        }
        .profile-img {
            width: 140px;
            height: 140px;
            border-radius: 15px;
            border: 4px solid var(--accent-gold);
            overflow: hidden;
            flex-shrink: 0;
        }
        .profile-img img { width: 100%; height: 100%; object-fit: cover; }
        .profile-titles {
            flex: 1;
        }
        .profile-titles h1 {
            color: white;
            font-size: 2.2rem;
            margin-bottom: 8px;
        }
        .profile-titles .tagline {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1.1rem;
            line-height: 1.5;
        }
        .motto-box {
            color: white;
            background: rgba(0, 0, 0, 0.15);
            padding: 15px 20px;
            border-radius: 15px;
            border-right: 4px solid var(--accent-gold);
            font-size: 1rem;
            line-height: 1.6;
            width: 100%;
        }
        .motto {
            color: var(--accent-gold);
            font-weight: 600;
        }
        
        /* نوار ابزار عمودی */
        .vertical-nav {
            background: rgba(255, 255, 255, 0.98);
            border-radius: 20px;
            padding: 25px 20px;
            box-shadow: 0 12px 25px var(--card-shadow);
            display: flex;
            flex-direction: column;
            gap: 12px;
            height: fit-content;
        }
        .nav-item {
            background: linear-gradient(to left, var(--soft-blue), var(--deep-teal));
            color: white;
            padding: 14px 20px;
            border-radius: 12px;
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(52, 152, 219, 0.2);
            font-size: 0.95rem;
        }
        .nav-item:hover {
            transform: translateX(-5px);
            box-shadow: 0 8px 18px rgba(52, 152, 219, 0.4);
        }
        .nav-icon { font-size: 1.1rem; }
        
        /* بخش فراخوان جهانی */
        .global-call-section {
            padding: 80px 30px;
            background: linear-gradient(135deg, #f0f7ff, #e3f2fd);
            width: 100%;
        }
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--navy-blue);
            margin-bottom: 50px;
        }
        .call-to-action-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 100%;
            margin: 0 auto;
            padding: 0 20px;
        }
        .call-card {
            background: white;
            border-radius: 20px;
            padding: 35px;
            box-shadow: 0 15px 35px rgba(10, 36, 99, 0.1);
            border: 2px solid transparent;
            transition: all 0.4s;
            text-align: center;
            display: flex;
            flex-direction: column;
        }
        .call-card:hover {
            transform: translateY(-10px);
            border-color: var(--accent-gold);
            box-shadow: 0 25px 50px rgba(10, 36, 99, 0.15);
        }
        .call-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }
        .call-card h3 {
            color: var(--navy-blue);
            font-size: 1.6rem;
            margin-bottom: 15px;
        }
        .call-card p {
            color: #555;
            line-height: 1.7;
            flex: 1;
            margin-bottom: 20px;
        }
        .call-highlight {
            background: rgba(212, 175, 55, 0.1);
            border-right: 4px solid var(--accent-gold);
            padding: 15px;
            border-radius: 10px;
            margin-top: 15px;
            font-size: 0.95rem;
            color: #333;
            text-align: right;
        }
        
        /* باکس شمارنده */
        .stats-section {
            padding: 50px 30px;
            background: white;
            width: 100%;
        }
        .stats-container {
            max-width: 100%;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            padding: 0 20px;
        }
        .stat-box {
            background: linear-gradient(135deg, #ffffff, #f0f7ff);
            border-radius: 18px;
            padding: 25px;
            text-align: center;
            border: 2px solid #e2e8f0;
            transition: all 0.4s;
            box-shadow: 0 8px 20px rgba(10, 36, 99, 0.05);
        }
        .stat-box:hover {
            transform: translateY(-8px);
            border-color: var(--soft-blue);
            box-shadow: 0 15px 30px var(--card-shadow);
        }
        .stat-number {
            font-size: 2.8rem;
            font-weight: 800;
            color: var(--navy-blue);
            display: block;
            line-height: 1;
            margin-bottom: 10px;
        }
        .stat-label {
            color: #555;
            font-size: 0.95rem;
            line-height: 1.5;
            min-height: 45px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        /* بخش مقالات */
        .research-section {
            padding: 80px 30px;
            background: white;
            width: 100%;
        }
        .research-tabs {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 40px;
            justify-content: center;
        }
        .tab-btn {
            padding: 15px 30px;
            background: #f0f7ff;
            border: none;
            border-radius: 15px;
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--navy-blue);
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .tab-btn:hover {
            background: var(--soft-blue);
            color: white;
        }
        .tab-btn.active {
            background: linear-gradient(135deg, var(--navy-blue), var(--deep-teal));
            color: white;
            box-shadow: 0 8px 20px rgba(10, 36, 99, 0.2);
        }
        .tab-icon { font-size: 1.3rem; }
        .tab-content {
            display: none;
            animation: fadeIn 0.5s ease;
        }
        .tab-content.active {
            display: block;
        }
        .research-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
            padding: 0 20px;
        }
        .research-card {
            background: #f8fafc;
            border-radius: 20px;
            padding: 30px;
            border: 1px solid #e2e8f0;
            transition: all 0.4s;
            height: 100%;
            display: flex;
            flex-direction: column;
        }
        .research-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(10, 36, 99, 0.1);
            border-color: var(--soft-blue);
        }
        .research-card-header {
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #e2e8f0;
        }
        .research-card-title {
            font-size: 1.4rem;
            color: var(--navy-blue);
            margin-bottom: 10px;
            line-height: 1.4;
        }
        .research-card-meta {
            display: flex;
            justify-content: space-between;
            font-size: 0.9rem;
            color: #666;
        }
        .research-card-date { font-weight: 600; }
        .research-card-keywords {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin: 15px 0;
        }
        .keyword {
            background: rgba(52, 152, 219, 0.1);
            color: var(--deep-teal);
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }
        .research-card-body {
            flex: 1;
            color: #555;
            line-height: 1.7;
            margin-bottom: 20px;
        }
        .research-card-footer {
            margin-top: auto;
            padding-top: 15px;
            border-top: 1px dashed #ddd;
            text-align: left;
            font-style: italic;
            color: #777;
            font-size: 0.9rem;
        }
        .request-ppt-btn {
            background: linear-gradient(135deg, var(--literary-purple), #8A63B5);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 10px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 15px;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }
        .request-ppt-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(106, 76, 147, 0.3);
        }
        
        /* یادداشت‌های روزانه */
        .notes-section {
            padding: 80px 30px;
            background: #f8fafc;
            width: 100%;
        }
        .timeline {
            max-width: 100%;
            margin: 50px auto;
            position: relative;
            padding: 0 20px;
        }
        .timeline::before {
            content: '';
            position: absolute;
            right: 50%;
            top: 0;
            bottom: 0;
            width: 4px;
            background: linear-gradient(to bottom, var(--soft-blue), var(--literary-purple));
            border-radius: 2px;
        }
        .timeline-item {
            margin-bottom: 40px;
            position: relative;
            width: 45%;
        }
        .timeline-item:nth-child(odd) {
            margin-right: 55%;
        }
        .timeline-item:nth-child(even) {
            margin-right: 0;
            margin-left: 55%;
        }
        .timeline-date {
            background: var(--navy-blue);
            color: white;
            padding: 8px 20px;
            border-radius: 20px;
            font-weight: 600;
            display: inline-block;
            margin-bottom: 10px;
        }
        .timeline-content {
            background: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
        }
        .timeline-content h3 {
            color: var(--deep-teal);
            margin-bottom: 10px;
        }
        
        /* اسلایدشو مقالات */
        .slideshow-section {
            padding: 70px 30px;
            background: white;
            width: 100%;
        }
        .slideshow-container {
            max-width: 100%;
            margin: 40px auto;
            border-radius: 22px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.18);
            position: relative;
            padding: 0 20px;
        }
        .slides-wrapper {
            display: flex;
            transition: transform 0.4s ease;
            direction: ltr;
        }
        .slide-item {
            min-width: 100%;
            height: 400px;
            background: #1e293b;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .slide-item img {
            max-width: 85%;
            max-height: 85%;
            object-fit: contain;
            border-radius: 8px;
        }
        .slide-controls {
            position: absolute;
            bottom: 20px;
            right: 50%;
            transform: translateX(50%);
            display: flex;
            gap: 10px;
        }
        .slide-dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.5);
            cursor: pointer;
            transition: all 0.3s;
        }
        .slide-dot.active {
            background: white;
            transform: scale(1.3);
        }
        
        /* اسلایدشو کتاب‌ها */
        .books-slideshow {
            padding: 70px 30px;
            background: linear-gradient(135deg, #f9f5ff, #f0ebfa);
            width: 100%;
        }
        .books-slider {
            max-width: 100%;
            margin: 40px auto;
            overflow: hidden;
            border-radius: 22px;
            box-shadow: 0 20px 40px rgba(106, 76, 147, 0.18);
            padding: 0 20px;
        }
        .books-track {
            display: flex;
            transition: transform 0.5s ease;
            direction: ltr;
        }
        .book-slide {
            min-width: 25%;
            padding: 15px;
        }
        .book-item {
            background: white;
            border-radius: 18px;
            overflow: hidden;
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.1);
            height: 320px;
            display: flex;
            flex-direction: column;
        }
        .book-cover {
            height: 180px;
            background: var(--literary-purple);
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        .book-cover img {
            max-width: 75%;
            max-height: 75%;
            object-fit: contain;
            border-radius: 5px;
        }
        .book-info {
            padding: 20px;
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        .book-title {
            color: var(--literary-purple);
            font-size: 1.2rem;
            font-weight: 700;
            margin-bottom: 8px;
        }
        .book-desc {
            color: #555;
            font-size: 0.9rem;
            line-height: 1.5;
        }
        .book-status {
            color: #666;
            font-size: 0.85rem;
            font-style: italic;
            margin-top: 10px;
            text-align: left;
        }
        
        /* بخش سرمایه‌گذاری */
        .investment-section {
            padding: 70px 30px;
            background: linear-gradient(135deg, var(--navy-blue), var(--deep-teal));
            color: white;
            text-align: center;
            width: 100%;
        }
        .investment-content {
            max-width: 100%;
            margin: 0 auto;
            padding: 0 20px;
        }
        .investment-content h2 {
            font-size: 2.3rem;
            margin-bottom: 20px;
        }
        .investment-text {
            font-size: 1.2rem;
            line-height: 1.7;
            margin-bottom: 25px;
            opacity: 0.95;
        }
        .highlight-box {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 20px;
            border-right: 4px solid var(--accent-gold);
            margin-top: 20px;
            font-size: 1.1rem;
        }
        
        /* مودال پاورپوینت */
        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.7);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }
        .modal.active { display: flex; }
        .modal-content {
            background: white;
            border-radius: 20px;
            padding: 40px;
            max-width: 500px;
            width: 90%;
            text-align: center;
            box-shadow: 0 25px 50px rgba(0,0,0,0.3);
        }
        .modal-icon { font-size: 4rem; color: var(--accent-gold); margin-bottom: 20px; }
        .modal h3 { color: var(--navy-blue); margin-bottom: 15px; }
        .modal p { color: #555; line-height: 1.7; margin-bottom: 25px; }
        .modal-close {
            background: var(--navy-blue);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
        }
        .modal-contact {
            background: var(--accent-gold);
            color: var(--navy-blue);
            margin-right: 10px;
        }
        
        /* پنل مدیریت (مخفی) */
        .admin-panel-section {
            padding: 50px 30px;
            background: #f0f7ff;
            display: none;
            width: 100%;
        }
        .admin-panel {
            max-width: 100%;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 40px rgba(10, 36, 99, 0.1);
        }
        .admin-form input, .admin-form textarea, .admin-form select {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 2px solid #e2e8f0;
            border-radius: 10px;
            font-family: inherit;
            font-size: 1rem;
        }
        .admin-form textarea { min-height: 150px; resize: vertical; }
        .admin-submit {
            background: linear-gradient(135deg, var(--navy-blue), var(--deep-teal));
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 10px;
            font-weight: 600;
            cursor: pointer;
            font-size: 1.1rem;
        }
        
        /* نوار پایینی */
        .final-bar {
            background: linear-gradient(90deg, var(--navy-blue), var(--literary-purple));
            padding: 18px 0;
            overflow: hidden;
            margin-top: 50px;
            width: 100%;
        }
        .bar-content {
            display: flex;
            animation: scrollLeft 35s linear infinite;
            white-space: nowrap;
        }
        .bar-text {
            font-size: 1.3rem;
            color: white;
            font-weight: 600;
            padding: 0 40px;
            display: inline-block;
        }
        @keyframes scrollLeft {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }
        
        /* فوتر */
        footer {
            background: var(--navy-blue);
            color: white;
            padding: 50px 30px;
            text-align: center;
            width: 100%;
        }
        .footer-content {
            max-width: 100%;
            margin: 0 auto;
            padding: 0 20px;
        }
        .footer-content h3 {
            font-size: 1.8rem;
            margin-bottom: 35px;
        }
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }
        .footer-col div:first-child {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 12px;
        }
        .copyright {
            color: rgba(255,255,255,0.7);
            font-size: 0.9rem;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        /* انیمیشن‌ها */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* ریسپانسیو */
        @media (max-width: 1100px) {
            .header-container { grid-template-columns: 1fr; }
            .vertical-nav { order: -1; margin-bottom: 30px; }
            .stats-container { grid-template-columns: repeat(2, 1fr); }
            .book-slide { min-width: 33.333%; }
            .research-grid { grid-template-columns: repeat(2, 1fr); }
            .call-to-action-grid { grid-template-columns: repeat(2, 1fr); }
        }
        @media (max-width: 768px) {
            .main-header, .global-call-section, .research-section, .notes-section { padding: 30px 20px; }
            .profile-section { padding: 25px; }
            .profile-img-container { flex-direction: column; text-align: center; gap: 20px; }
            .profile-img { width: 160px; height: 160px; }
            .stats-container { grid-template-columns: 1fr; }
            .book-slide { min-width: 50%; }
            .slide-item { height: 320px; }
            .section-title { font-size: 2rem; }
            .research-grid { grid-template-columns: 1fr; }
            .tab-btn { padding: 12px 20px; font-size: 1rem; }
            .call-to-action-grid { grid-template-columns: 1fr; }
            .timeline::before { right: 30px; }
            .timeline-item { width: 100%; margin-right: 0 !important; margin-left: 0 !important; }
        }
        @media (max-width: 480px) {
            .book-slide { min-width: 100%; }
            .nav-item { padding: 12px 16px; font-size: 0.9rem; }
            .stat-number { font-size: 2.3rem; }
            .section-title { font-size: 1.8rem; }
            .lang-switcher { top: 15px; left: 15px; }
            .lang-btn { padding: 6px 12px; font-size: 0.9rem; }
        }
    </style>
</head>
<body>
    <!-- دکمه زبان -->
        <div class="lang-switcher">
    <a href="https://ghrezaei1399.github.io/سایت-انگلیسی-ghrezaei/" class="lang-btn" target="_blank">English</a>
</div>
    <!-- هدر اصلی -->
    <header class="main-header">
        <div class="header-container">
            <div class="profile-section">
                <div class="profile-img-container">
                    <div class="profile-img">
                        <img src="https://i.postimg.cc/02YrBwDP/%CA%BEks-khwdm2.jpg" alt="دکتر رضائی">
                    </div>
                    <div class="profile-titles">
                        <h1>دکتر غلامرضا رضائی</h1>
                        <div class="tagline">
                            معمار تحول سازمانی | نظریه‌پرداز هوش مصنوعی | شاعر و نویسنده
                        </div>
                    </div>
                </div>
                <div class="motto-box">
                    <span class="motto">شعار: </span>ترکیب خرد انسانی با فناوری‌های پیشرفته برای فردایی امن و شکوفا
                </div>
            </div>
            
            <nav class="vertical-nav">
                <a href="#global-call" class="nav-item"><span class="nav-icon">🌍</span> فراخوان جهانی</a>
                <a href="#stats" class="nav-item"><span class="nav-icon">📊</span> آمار و دستاوردها</a>
                <a href="#research" class="nav-item"><span class="nav-icon">📄</span> مقالات و پژوهش‌ها</a>
                <a href="#notes" class="nav-item"><span class="nav-icon">📝</span> یادداشت‌های روزانه</a>
                <a href="#books" class="nav-item"><span class="nav-icon">📚</span> آثار ادبی</a>
                <a href="#investment" class="nav-item"><span class="nav-icon">🔒</span> همکاری و سرمایه‌گذاری</a>
                <a href="#contact" class="nav-item"><span class="nav-icon">📞</span> تماس و ارتباط</a>
            </nav>
        </div>
    </header>
    
    <!-- بخش فراخوان جهانی -->
    <section id="global-call" class="global-call-section">
        <h2 class="section-title">فراخوان همکاری جهانی</h2>
        <div class="call-to-action-grid">
            <div class="call-card">
                <div class="call-icon">🏛️</div>
                <h3>کشورها و دولت‌ها</h3>
                <p>اجرای طرح‌های ملی تحول دیجیتال و هوش مصنوعی انسان‌محور. بیش از ۱۰ طرح آماده اجرا با الحاقیات کامل.</p>
                <div class="call-highlight">مشارکت در پروژه‌های کلان ملی</div>
            </div>
            <div class="call-card">
                <div class="call-icon">🏢</div>
                <h3>شرکت‌های فناوری</h3>
                <p>خرید یا مشارکت در اجرای چارچوب‌های تحولی مانند سازمان کیفی سیار (IMQO) و نکسوس کارآفرین جهانی (GENF).</p>
                <div class="call-highlight">طرح‌های عملیاتی آماده پیاده‌سازی</div>
            </div>
            <div class="call-card">
                <div class="call-icon">🤝</div>
                <h3>سرمایه‌گذاران اثرگذار</h3>
                <p>سرمایه‌گذاری در مدل‌های کسب‌وکار مبتنی بر هوش مصنوعی اخلاق‌محور و مهندسی فرهنگی. بازگشت سرمایه تضمین‌شده.</p>
                <div class="call-highlight">۱۶ طرح با تحلیل مالی کامل</div>
            </div>
            <div class="call-card">
                <div class="call-icon">🌐</div>
                <h3>مجامع بین‌المللی</h3>
                <p>همکاری با نهادهایی مانند یونسکو، WEF و IEEE برای گسترش چارچوب‌های نظری و استانداردهای جهانی.</p>
                <div class="call-highlight">همکاری در تدوین استانداردها</div>
            </div>
            <div class="call-card">
                <div class="call-icon">👥</div>
                <h3>نمایندگان اجرایی</h3>
                <p>اعطای نمایندگی برای اجرای منطقه‌ای طرح‌ها در کشورهای عربی، آسیایی و اروپایی.</p>
                <div class="call-highlight">آموزش، پشتیبانی و مربی‌گری کامل</div>
            </div>
        </div>
    </section>
    
    <!-- باکس شمارنده -->
    <section id="stats" class="stats-section">
        <div class="stats-container">
            <div class="stat-box">
                <span class="stat-number">18</span>
                <div class="stat-label">مقاله علمی-نظری با ثبت بین‌المللی (DOI)</div>
            </div>
            <div class="stat-box">
                <span class="stat-number">2</span>
                <div class="stat-label">مقاله سیاسی-اجتماعی تحلیلی</div>
            </div>
            <div class="stat-box">
                <span class="stat-number">33+</span>
                <div class="stat-label">نظریه جدید در هوش مصنوعی و تحول سازمانی</div>
            </div>
            <div class="stat-box">
                <span class="stat-number">4</span>
                <div class="stat-label">کتاب شعر منتشر شده</div>
            </div>
            <div class="stat-box">
                <span class="stat-number">1</span>
                <div class="stat-label">کتاب داستان منتشر شده</div>
            </div>
            <div class="stat-box">
                <span class="stat-number">13</span>
                <div class="stat-label">کتاب داستان در حال اخذ مجوز</div>
            </div>
            <div class="stat-box">
                <span class="stat-number">1</span>
                <div class="stat-label">کتاب هوشمندنگاری</div>
            </div>
            <div class="stat-box">
                <span class="stat-number">1</span>
                <div class="stat-label">کتاب در حال نگارش (فساد سازمانی)</div>
            </div>
        </div>
    </section>
    
    <!-- بخش مقالات و پژوهش‌ها -->
    <section id="research" class="research-section">
        <h2 class="section-title">مقاله‌ها و پژوهش‌های علمی-نظری</h2>
        
        <div class="research-tabs">
            <button class="tab-btn active" data-tab="tab1">
                <span class="tab-icon">🤖</span> هوش مصنوعی انسان‌محور
            </button>
            <button class="tab-btn" data-tab="tab2">
                <span class="tab-icon">🏢</span> تحول سازمانی هوشمند
            </button>
            <button class="tab-btn" data-tab="tab3">
                <span class="tab-icon">🌍</span> مهندسی فرهنگی دیجیتال
            </button>
            <button class="tab-btn" data-tab="tab4">
                <span class="tab-icon">🧠</span> نظریه‌های شناختی-اجتماعی
            </button>
        </div>
        
        <!-- تب 1: هوش مصنوعی انسان‌محور -->
        <div id="tab1" class="tab-content active">
            <div class="research-grid">
                <div class="research-card">
                    <div class="research-card-header">
                        <h3 class="research-card-title">طرح درهم‌تنیدگی انسان و هوش مصنوعی</h3>
                        <div class="research-card-meta">
                            <span class="research-card-date">دسامبر ۲۰۲۵</span>
                            <span>مقاله ۱۱</span>
                        </div>
                    </div>
                    <div class="research-card-keywords">
                        <span class="keyword">هوش مصنوعی شخصی</span>
                        <span class="keyword">حفاظت فرهنگی</span>
                    </div>
                    <div class="research-card-body">
                        ارائه چارچوبی برای ایجاد همکار دیجیتالی وفادار تحت استیلای کامل کاربر مصلح فرهنگی.
                    </div>
                    <button class="request-ppt-btn">📥 درخواست فایل ارائه (PPT)</button>
                    <div class="research-card-footer">چارچوب عملیاتی برای مهندسان فرهنگ</div>
                </div>
                
                <div class="research-card">
                    <div class="research-card-header">
                        <h3 class="research-card-title">پارادایم تکوین همگام</h3>
                        <div class="research-card-meta">
                            <span class="research-card-date">دسامبر ۲۰۲۵</span>
                            <span>مقاله ۸</span>
                        </div>
                    </div>
                    <div class="research-card-keywords">
                        <span class="keyword">تکوین همگام</span>
                        <span class="keyword">ایمنی ذاتی</span>
                    </div>
                    <div class="research-card-body">
                        معرفی معماری بدیل بنیادین با سه اصل یکپارچه برای توسعه امن هوش مصنوعی.
                    </div>
                    <button class="request-ppt-btn">📥 درخواست فایل ارائه (PPT)</button>
                    <div class="research-card-footer">پارادایم جدید برای توسعه امن</div>
                </div>
            </div>
        </div>
        
        <!-- تب 2: تحول سازمانی هوشمند -->
        <div id="tab2" class="tab-content">
            <div class="research-grid">
                <div class="research-card">
                    <div class="research-card-header">
                        <h3 class="research-card-title">سازمان تحول‌گرای هوشمند</h3>
                        <div class="research-card-meta">
                            <span class="research-card-date">دسامبر ۲۰۲۵</span>
                            <span>مقاله ۳</span>
                        </div>
                    </div>
                    <div class="research-card-keywords">
                        <span class="keyword">تحول سازمانی</span>
                        <span class="keyword">هوشمندی پویا</span>
                    </div>
                    <div class="research-card-body">
                        ارائه نقشه‌راهی برای تبدیل هوشمندسازی به یک «سفر تحول فرهنگی» در خدمت شکوفایی جمعی.
                    </div>
                    <button class="request-ppt-btn">📥 درخواست فایل ارائه (PPT)</button>
                    <div class="research-card-footer">پاسخ به نرخ شکست ۷۰٪ پروژه‌ها</div>
                </div>
            </div>
        </div>
        
        <!-- تب 3: مهندسی فرهنگی دیجیتال -->
        <div id="tab3" class="tab-content">
            <div class="research-grid">
                <div class="research-card">
                    <div class="research-card-header">
                        <h3 class="research-card-title">طرح ملی «هوشمندسازی همراهان روشنایی»</h3>
                        <div class="research-card-meta">
                            <span class="research-card-date">دسامبر ۲۰۲۵</span>
                            <span>مقاله ۱</span>
                        </div>
                    </div>
                    <div class="research-card-keywords">
                        <span class="keyword">مهندسی فرهنگی</span>
                        <span class="keyword">همراهان روشنایی</span>
                    </div>
                    <div class="research-card-body">
                        معرفی چارچوب عملیاتی طرح ملی با ارائه «نظریه هوشمندسازی همراهان روشنایی».
                    </div>
                    <button class="request-ppt-btn">📥 درخواست فایل ارائه (PPT)</button>
                    <div class="research-card-footer">پاسخ بومی به بحران حکمرانی فرهنگی</div>
                </div>
            </div>
        </div>
        
        <!-- تب 4: نظریه‌های شناختی-اجتماعی -->
        <div id="tab4" class="tab-content">
            <div class="research-grid">
                <div class="research-card">
                    <div class="research-card-header">
                        <h3 class="research-card-title">چارچوب نظری گسست دیجیتال-کنشگری</h3>
                        <div class="research-card-meta">
                            <span class="research-card-date">دسامبر ۲۰۲۵</span>
                            <span>مقاله ۶</span>
                        </div>
                    </div>
                    <div class="research-card-keywords">
                        <span class="keyword">گسست دیجیتال</span>
                        <span class="keyword">کنشگری اجتماعی</span>
                    </div>
                    <div class="research-card-body">
                        تحلیل پارادوکس کاهش اثرگذاری کنش جمعی علی‌رغم دسترسی بی‌سابقه به فناوری.
                    </div>
                    <button class="request-ppt-btn">📥 درخواست فایل ارائه (PPT)</button>
                    <div class="research-card-footer">چارچوب یکپارچه تحلیل بحران کنشگری</div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- یادداشت‌های روزانه -->
    <section id="notes" class="notes-section">
        <h2 class="section-title">یادداشت‌های روزانه دکتر رضائی</h2>
        <div class="timeline">
            <div class="timeline-item">
                <div class="timeline-date">۳۰ دسامبر ۲۰۲۵</div>
                <div class="timeline-content">
                    <h3>یادداشت روز تعویض، تطمیع، تهدید، دیگر اثر ندارد</h3>
                    <p>تحلیلی بر تحول گفتمان قدرت و مقاومت در عصر دیجیتال...</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-date">۲۹ دسامبر ۲۰۲۵</div>
                <div class="timeline-content">
                    <h3>یادداشت روز اتحاد در کف خیابان</h3>
                    <p>ضرورت بازتعریف کنش جمعی در فضای عمومی...</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- اسلایدشو مقالات (تصاویر) -->
    <section class="slideshow-section">
        <h2 class="section-title">اسلایدهای مقالات علمی</h2>
        <div class="slideshow-container">
            <div class="slides-wrapper" id="articlesSlides"></div>
            <div class="slide-controls" id="articlesDots"></div>
        </div>
    </section>
    
    <!-- اسلایدشو کتاب‌ها -->
    <section id="books" class="books-slideshow">
        <h2 class="section-title">آثار ادبی و شعری منتشر شده</h2>
        <div class="books-slider">
            <div class="books-track" id="booksTrack"></div>
        </div>
        <p style="text-align: center; color: #666; margin-top: 30px; font-size: 1rem; max-width: 800px; margin-left: auto; margin-right: auto;">
            <strong>توضیح:</strong> این‌ها بخشی از آثار چاپ‌شده از «سپهر ۲۰۰۰۰ بیت شعر سروده شده» است. بقیه آثار ادبی در حال تدوین نهایی و اخذ مجوز هستند.
        </p>
    </section>
    
    <!-- بخش سرمایه‌گذاری -->
    <section id="investment" class="investment-section">
        <div class="investment-content">
            <h2>همکاری و سرمایه‌گذاری</h2>
            <p class="investment-text">
                <strong>۱۶ طرح کامل با الحاقیات، اصول فنی، معماری و مدل‌های درآمدی آماده ارائه است.</strong><br>
                تحلیل‌های مالی دقیق، مستندات ROI و طرح‌های اجرایی برای همکاری‌های استراتژیک.
            </p>
            <div class="highlight-box">
                <strong>توجه:</strong> تمامی مستندات و تحلیل‌ها فقط پس از عقد قرارداد محرمانگی (NDA) و تأیید شخصی ارائه می‌شوند.
            </div>
        </div>
    </section>
    
    <!-- پنل مدیریت (مخفی) -->
    <section id="admin-panel" class="admin-panel-section">
        <div class="admin-panel">
            <h2>پنل مدیریت محتوا</h2>
            <form class="admin-form" id="adminForm">
                <input type="text" id="itemTitle" placeholder="عنوان (فارسی)" required>
                <textarea id="itemContent" placeholder="محتوا (فارسی)" required></textarea>
                <select id="itemType">
                    <option value="article">مقاله</option>
                    <option value="book">کتاب</option>
                    <option value="note">یادداشت روزانه</option>
                    <option value="stat">آمار</option>
                </select>
                <input type="text" id="itemDate" placeholder="تاریخ (مثال: ۲۰۲۵-۱۲-۳۰)">
                <input type="text" id="itemKeywords" placeholder="کلیدواژه‌ها (با کاما جدا کنید)">
                <button type="submit" class="admin-submit">ذخیره و انتشار</button>
            </form>
        </div>
    </section>
    
    <!-- مودال درخواست پاورپوینت -->
    <div class="modal" id="pptModal">
        <div class="modal-content">
            <div class="modal-icon">🔒</div>
            <h3>درخواست فایل ارائه</h3>
            <p>فایل کامل ارائه (پاورپوینت) این پژوهش، پس از ثبت درخواست رسمی و موافقت شخصی دکتر رضائی، ارائه می‌گردد.</p>
            <p>لطفاً از طریق بخش تماس، درخواست خود را ارسال نمایید.</p>
            <div style="margin-top: 30px;">
                <button class="modal-close modal-contact" onclick="location.href='#contact'">📧 ارسال درخواست</button>
                <button class="modal-close" onclick="closeModal()">بستن</button>
            </div>
        </div>
    </div>
    
    <!-- نوار پایینی -->
    <div class="final-bar">
        <div class="bar-content">
            <span class="bar-text">ساخت چارچوب‌هایی که نه ترس را دامن می‌زنند و نه ساده‌لوحی را • ترکیب خرد با فناوری برای فردایی امن و شکوفا • از شعر کهن تا هوش مصنوعی پیشرفته • تحول سازمانی با حفظ اصالت فرهنگی • نگاه به آینده، ریشه در گذشته • هر پایان، آغازی برای تکامل است • ۱۶ طرح آماده اجرا • سپهری از ۲۰۰۰۰ بیت شعر • پژوهش‌های بین‌المللی ثبت‌شده • ۱۸ مقاله علمی-نظری • پارادایم‌های نوین سازمان ارتعاشی • فراخوان جهانی همکاری</span>
            <span class="bar-text">ساخت چارچوب‌هایی که نه ترس را دامن می‌زنند و نه ساده‌لوحی را • ترکیب خرد با فناوری برای فردایی امن و شکوفا • از شعر کهن تا هوش مصنوعی پیشرفته • تحول سازمانی با حفظ اصالت فرهنگی • نگاه به آینده، ریشه در گذشته • هر پایان، آغازی برای تکامل است • ۱۶ طرح آماده اجرا • سپهری از ۲۰۰۰۰ بیت شعر • پژوهش‌های بین‌المللی ثبت‌شده • ۱۸ مقاله علمی-نظری • پارادایم‌های نوین سازمان ارتعاشی • فراخوان جهانی همکاری</span>
        </div>
    </div>
    
    <!-- فوتر -->
    <footer id="contact">
        <div class="footer-content">
            <h3>ارتباط و همکاری</h3>
            <div class="footer-grid">
                <div class="footer-col">
                    <div>ایمیل‌های رسمی</div>
                    <div>ghrezaei1399@gmail.com</div>
                    <div>Gh_rezaei2003@yahoo.com</div>
                </div>
                <div class="footer-col">
                    <div>نمایه پژوهشی</div>
                    <div>ORCID: 0009-0007-5840-8833</div>
                    <div>LinkedIn: linkedin.com/in/reaei-researcher</div>
                </div>
                <div class="footer-col">
                    <div>دسترسی به مقالات</div>
                    <div>۱۸ مقاله ثبت‌شده در Zenodo</div>
                    <div>با تأیید و درخواست رسمی</div>
                </div>
            </div>
            <div class="copyright">
                © کلیه حقوق محفوظ است - دکتر غلامرضا رضائی - طراحی بر پایه ترکیب خرد انسانی و فناوری پیشرفته
            </div>
        </div>
    </footer>
    
    <script>
    // داده‌های مقالات (اسلایدشو - ۱۱ عکس)
    const articleSlides = [
        'https://i.postimg.cc/g2d9gwHj/dh-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/521csHS6/dw-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/DwFVxWPS/sh-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/GmjWVcXh/shsh-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/ht0k6S2G/nh-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/RZTkyMgN/hsht-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/x1Pwh06C/hft-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/qv0f1txH/pnj-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/vZMR01tD/chhar-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/0yCTF8V6/yazdh-az-syzdh-aslayd.jpg',
        'https://i.postimg.cc/3xZsVKtG/yk-az-syzdh-aslayd.jpg'
    ];
    
    // داده‌های کتاب‌ها (۱۸ عکس)
    const booksData = [
        { img: 'https://i.postimg.cc/nr7K5hYW/20240301-203438-(3).jpg', title: 'آوای دل', desc: 'اشعار عاشقانه ۱۳۹۷' },
        { img: 'https://i.postimg.cc/PJZbc5Qd/20240301-203516-(2).jpg', title: 'ترنم دل', desc: 'غزلیات و مثنویات ۱۳۹۷' },
        { img: 'https://i.postimg.cc/6qRVSpf9/20240301-203539-(2).jpg', title: 'دیوان اشعار', desc: 'گزیده اشعار کلاسیک' },
        { img: 'https://i.postimg.cc/7h71cZnL/20240301-203802-(2).jpg', title: 'مجموعه شعر نو', desc: 'آفرینش‌های معاصر' },
        { img: 'https://i.postimg.cc/d3dRXVjD/20240301-204004-(2).jpg', title: 'در انتظار محور', desc: 'داستان نوآورانه' },
        { img: 'https://i.postimg.cc/pVnBysb0/20240301-204056-(2).jpg', title: 'هوشمندنگاری', desc: 'کتاب آموزشی' },
        { img: 'https://i.postimg.cc/zDRk3xZ0/20240301-204119-(2).jpg', title: 'زمزمه دل', desc: 'اشعار عارفانه' },
        { img: 'https://i.postimg.cc/L4ZVhxKb/20240301-204156-(2).jpg', title: 'نغمه دل', desc: 'اشعار اجتماعی' },
        { img: 'https://i.postimg.cc/MK2mB1zG/20240301-204217.jpg', title: 'آوای دل ۲', desc: 'اشعار منتخب' },
        { img: 'https://i.postimg.cc/jdHQ4Cjy/20240301-204444.jpg', title: 'ترنم دل ۲', desc: 'غزلیات جدید' },
        { img: 'https://i.postimg.cc/7Y3MnbLM/20240301-205811.jpg', title: 'مجموعه شعر کهن', desc: 'بازسرایی اشعار کلاسیک' },
        { img: 'https://i.postimg.cc/BQTcBtvC/20240301-205901.jpg', title: 'داستان‌های کوتاه', desc: 'آثار داستانی' },
        { img: 'https://i.postimg.cc/65rLfTQ0/20240301-210721-(2).jpg', title: 'هوشمندنگاری پیشرفته', desc: 'جلد دوم' },
        { img: 'https://i.postimg.cc/kg7N19VF/20240301-211151-(2).jpg', title: 'در انتظار محور ۲', desc: 'ادامه داستان' },
        { img: 'https://i.postimg.cc/CxwCPYZm/20240301-211220-(2).jpg', title: 'اشعار اجتماعی ۲', desc: 'نقد جامعه' },
        { img: 'https://i.postimg.cc/YCtNnk4V/20240301-211256-(2).jpg', title: 'عرفان و هوش مصنوعی', desc: 'تلفیق فلسفی' },
        { img: 'https://i.postimg.cc/pLPQGx94/20240301-211527-(2).jpg', title: 'تحول سازمانی در شعر', desc: 'نگاهی نو' },
        { img: 'https://i.postimg.cc/pLPQGx93/20240301-211628-(2).jpg', title: 'هزار بیت از سپهر', desc: 'گزیده‌ای از ۲۰۰۰۰ بیت' }
    ];
    
    // 1. اسلایدشو مقالات
    let currentArticleSlide = 0;
    let articleInterval;

    function initArticleSlideshow() {
        const slidesContainer = document.getElementById('articlesSlides');
        const dotsContainer = document.getElementById('articlesDots');
        
        // پاک کردن محتوای قبلی
        slidesContainer.innerHTML = '';
        dotsContainer.innerHTML = '';
        
        articleSlides.forEach((slide, index) => {
            const slideDiv = document.createElement('div');
            slideDiv.className = 'slide-item';
            slideDiv.innerHTML = `<img src="${slide}" alt="مقاله ${index + 1}" style="width: auto; height: auto; max-width: 90%; max-height: 90%;">`;
            slidesContainer.appendChild(slideDiv);
            
            const dot = document.createElement('div');
            dot.className = `slide-dot ${index === 0 ? 'active' : ''}`;
            dot.addEventListener('click', () => {
                currentArticleSlide = index;
                updateArticleSlideshow();
                resetArticleInterval();
            });
            dotsContainer.appendChild(dot);
        });
        
        function updateArticleSlideshow() {
            slidesContainer.style.transform = `translateX(-${currentArticleSlide * 100}%)`;
            document.querySelectorAll('#articlesDots .slide-dot').forEach((dot, i) => {
                dot.classList.toggle('active', i === currentArticleSlide);
            });
        }
        
        function resetArticleInterval() {
            clearInterval(articleInterval);
            articleInterval = setInterval(() => {
                currentArticleSlide = (currentArticleSlide + 1) % articleSlides.length;
                updateArticleSlideshow();
            }, 3000);
        }
        
        updateArticleSlideshow();
        resetArticleInterval();
    }

    // 2. اسلایدشو کتاب‌ها
    let currentBookSlide = 0;
    let bookInterval;

    function initBooksSlideshow() {
        const track = document.getElementById('booksTrack');
        
        // پاک کردن محتوای قبلی
        track.innerHTML = '';
        
        // فقط یک بار اضافه کن
        booksData.forEach((book, index) => {
            const slide = document.createElement('div');
            slide.className = 'book-slide';
            slide.innerHTML = `
                <div class="book-item">
                    <div class="book-cover">
                        <img src="${book.img}" alt="${book.title}">
                    </div>
                    <div class="book-info">
                        <div class="book-title">${book.title}</div>
                        <div class="book-desc">${book.desc}</div>
                        <div class="book-status">منتشر شده</div>
                    </div>
                </div>
            `;
            track.appendChild(slide);
        });
        
        // ریست اینتروال قبلی
        clearInterval(bookInterval);
        
        bookInterval = setInterval(() => {
            currentBookSlide++;
            const totalSlides = booksData.length;
            const slideWidth = 100 / 4; // 4 کتاب در هر صفحه
            
            track.style.transform = `translateX(-${currentBookSlide * slideWidth}%)`;
            
            // اگر به انتها رسید، برگرد به اول
            if (currentBookSlide >= totalSlides - 3) {
                setTimeout(() => {
                    track.style.transition = 'none';
                    currentBookSlide = 0;
                    track.style.transform = 'translateX(0)';
                    setTimeout(() => {
                        track.style.transition = 'transform 0.5s ease';
                    }, 50);
                }, 500);
            }
        }, 2500);
    }
    
    // 3. شمارنده آمار
    function animateStats() {
        const stats = document.querySelectorAll('.stat-number');
        stats.forEach(stat => {
            const target = parseInt(stat.textContent);
            let current = 0;
            const increment = target / 50;
            
            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    current = target;
                    clearInterval(timer);
                }
                stat.textContent = Math.floor(current);
            }, 25);
        });
    }
    
    // 4. سیستم تب‌ها
    function initResearchTabs() {
        const tabBtns = document.querySelectorAll('.tab-btn');
        const tabContents = document.querySelectorAll('.tab-content');
        
        tabBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                const tabId = btn.getAttribute('data-tab');
                tabBtns.forEach(b => b.classList.remove('active'));
                tabContents.forEach(c => c.classList.remove('active'));
                btn.classList.add('active');
                document.getElementById(tabId).classList.add('active');
            });
        });
    }
    
    // 5. مودال پاورپوینت
    function initPPTButtons() {
        const buttons = document.querySelectorAll('.request-ppt-btn');
        const modal = document.getElementById('pptModal');
        
        buttons.forEach(btn => {
            btn.addEventListener('click', () => {
                modal.classList.add('active');
            });
        });
        
        window.closeModal = function() {
            modal.classList.remove('active');
        }
        
        modal.addEventListener('click', function(e) {
            if (e.target === modal) closeModal();
        });
    }
    
    // 6. اسکرول نرم
    function initSmoothScroll() {
        document.querySelectorAll('.nav-item').forEach(item => {
            item.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({ 
                        behavior: 'smooth', 
                        block: 'start' 
                    });
                }
            });
        });
    }
    
    // 7. دکمه زبان
    document.querySelector('.lang-btn').addEventListener('click', function(e) {
        // لینک مستقیم است، نیاز به alert نیست
    });
    
    // 8. پنل مدیریت (نمایشی)
    document.getElementById('adminForm').addEventListener('submit', function(e) {
        e.preventDefault();
        alert('پنل مدیریت در حال تکمیل است. این فرم در نسخه نهایی، محتوا را ذخیره و نمایش می‌دهد.');
    });
    
    // اجرای همه
    window.addEventListener('DOMContentLoaded', () => {
        // اول اسلایدشوها
        initArticleSlideshow();
        initBooksSlideshow();
        
        // بقیه
        initResearchTabs();
        initPPTButtons();
        initSmoothScroll();
        setTimeout(animateStats, 400);
    });
</script>
</body>
</html>
