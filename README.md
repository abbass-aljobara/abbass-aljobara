<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أركان الرجل للحلاقة | صالون حلاقة عالمي</title>
    
    <!-- خطوط عربية وإنجليزية عالية الجودة -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@200;400;700;900&family=Tajawal:wght@400;700&display=swap" rel="stylesheet">
    
    <!-- مكتبة الأيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- مكتبة Animations -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>

    <style>
        /* --- المتغيرات والتوهجات --- */
        :root {
            --primary-gold: #FFD700;
            --dark-bg: #0a0a0a;
            --glass: rgba(255, 255, 255, 0.05);
            --text-gradient: linear-gradient(45deg, #FFD700, #FDB931);
            --shadow-glow: 0 0 15px rgba(255, 215, 0, 0.3);
            --card-bg: rgba(20, 20, 20, 0.8);
        }

        /* --- الأساسيات --- */
        * { 
            margin: 0; 
            padding: 0; 
            box-sizing: border-box; 
            outline: none; 
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: 'Tajawal', 'Cairo', sans-serif;
            background-color: var(--dark-bg);
            color: #fff;
            overflow-x: hidden;
        }

        /* --- مؤشر الماوس المخصص --- */
        .cursor {
            width: 20px; 
            height: 20px;
            border: 2px solid var(--primary-gold);
            border-radius: 50%;
            position: fixed;
            pointer-events: none;
            z-index: 9999;
            transition: transform 0.1s, width 0.3s, height 0.3s;
            mix-blend-mode: difference;
        }

        .cursor.hover {
            width: 50px;
            height: 50px;
            background-color: rgba(255, 215, 0, 0.1);
        }

        /* --- الخلفية الديناميكية --- */
        .background-fx {
            position: fixed;
            top: 0; 
            left: 0; 
            width: 100%; 
            height: 100%;
            z-index: -1;
            background: 
                radial-gradient(circle at 15% 50%, rgba(255, 215, 0, 0.08), transparent 25%),
                radial-gradient(circle at 85% 30%, rgba(184, 134, 11, 0.08), transparent 25%),
                linear-gradient(135deg, rgba(10,10,10,1) 0%, rgba(20,20,20,1) 100%);
            animation: bgPulse 10s infinite alternate;
        }
        
        @keyframes bgPulse { 
            0% { opacity: 0.5; } 
            100% { opacity: 1; } 
        }

        /* --- الهيدر العائم --- */
        header {
            position: fixed;
            top: 20px; 
            left: 50%;
            transform: translateX(-50%);
            width: 90%;
            max-width: 1200px;
            padding: 15px 30px;
            background: rgba(10, 10, 10, 0.9);
            backdrop-filter: blur(15px);
            border-radius: 50px;
            border: 1px solid rgba(255, 215, 0, 0.2);
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            box-shadow: 0 10px 30px rgba(0,0,0,0.7);
            transition: 0.4s;
        }

        header.scrolled {
            top: 10px;
            padding: 12px 25px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.9);
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 900;
            color: #fff;
            letter-spacing: 1px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo i {
            color: var(--primary-gold);
        }
        
        .logo span { 
            color: var(--primary-gold); 
        }

        nav ul { 
            display: flex; 
            gap: 30px; 
            list-style: none; 
        }
        
        nav a {
            color: #ccc;
            text-decoration: none;
            font-weight: 700;
            font-size: 0.95rem;
            transition: 0.3s;
            position: relative;
            padding: 5px 10px;
        }
        
        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            right: 0;
            width: 0;
            height: 2px;
            background: var(--primary-gold);
            transition: width 0.3s;
        }
        
        nav a:hover::after, nav a.active::after {
            width: 100%;
        }
        
        nav a:hover, nav a.active { 
            color: var(--primary-gold); 
        }

        .mobile-menu-btn { 
            display: none; 
            color: #fff; 
            font-size: 1.5rem; 
            cursor: pointer; 
            z-index: 1001;
        }

        /* --- الهيرو (النص المتحرك) --- */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            padding: 0 20px;
            overflow: hidden;
        }

        .hero-bg-img {
            position: absolute;
            width: 100%; 
            height: 100%;
            top: 0; 
            left: 0;
            background: url('https://images.unsplash.com/photo-1585747860715-2ba37e788b70?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2074&q=80') no-repeat center/cover;
            opacity: 0.4;
            z-index: -2;
            filter: grayscale(20%) brightness(0.7);
            animation: zoomInOut 30s infinite alternate;
        }
        
        @keyframes zoomInOut {
            0% { transform: scale(1); }
            100% { transform: scale(1.1); }
        }

        .hero-content {
            max-width: 900px;
            padding: 30px;
            background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(255, 215, 0, 0.2);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
        }

        .hero-content h1 {
            font-size: 5rem;
            line-height: 1.1;
            margin-bottom: 20px;
            background: var(--text-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 10px 30px rgba(0,0,0,0.5);
            animation: goldGlow 3s infinite alternate;
        }
        
        @keyframes goldGlow {
            0% { text-shadow: 0 0 20px rgba(255, 215, 0, 0.5); }
            100% { text-shadow: 0 0 30px rgba(255, 215, 0, 0.8), 0 0 40px rgba(255, 215, 0, 0.4); }
        }

        /* تأثير الآلة الكاتبة */
        .typing-text {
            font-size: 1.8rem;
            color: #fff;
            min-height: 1.8em;
            margin-bottom: 40px;
            font-family: 'Courier New', monospace;
        }
        
        .cursor-blink {
            display: inline-block;
            width: 3px; 
            height: 1.5rem;
            background-color: var(--primary-gold);
            margin-right: 5px;
            animation: blink 0.7s infinite;
        }
        
        @keyframes blink { 
            0%, 100% { opacity: 1; } 
            50% { opacity: 0; } 
        }

        /* --- الأزرار --- */
        .btn {
            padding: 15px 35px;
            border-radius: 30px;
            font-weight: bold;
            text-decoration: none;
            margin: 10px;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 0%;
            height: 100%;
            background: rgba(255, 255, 255, 0.1);
            transition: all 0.5s;
            z-index: -1;
        }
        
        .btn:hover::before {
            width: 100%;
        }

        .btn-whatsapp {
            background: #25D366;
            color: #fff;
            box-shadow: 0 0 20px rgba(37, 211, 102, 0.4);
        }
        
        .btn-whatsapp:hover { 
            transform: translateY(-5px) scale(1.05); 
            box-shadow: 0 10px 30px rgba(37, 211, 102, 0.8); 
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary-gold);
            color: var(--primary-gold);
        }
        
        .btn-outline:hover { 
            background: var(--primary-gold); 
            color: #000; 
            transform: translateY(-5px);
        }

        /* --- الأقسام العامة --- */
        section { 
            padding: 100px 10%; 
            position: relative;
        }
        
        .section-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.05;
            z-index: -1;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 { 
            font-size: 3rem; 
            color: #fff; 
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            right: 50%;
            transform: translateX(50%);
            width: 100px;
            height: 3px;
            background: var(--primary-gold);
            border-radius: 3px;
        }
        
        .section-title span { 
            color: var(--primary-gold); 
        }

        /* --- الخدمات (Floating Cards) --- */
        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background: var(--card-bg);
            padding: 40px;
            border-radius: 20px;
            border: 1px solid rgba(255,255,255,0.05);
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
        }
        
        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(255,215,0,0.03), transparent);
            transform: translateX(-100%);
            transition: transform 0.6s;
        }
        
        .card:hover::before {
            transform: translateX(100%);
        }

        .card:hover {
            transform: translateY(-10px);
            border-color: var(--primary-gold);
            box-shadow: 0 15px 40px rgba(0,0,0,0.7), 0 0 30px rgba(255,215,0,0.1);
        }

        .card i {
            font-size: 3rem;
            color: var(--primary-gold);
            margin-bottom: 20px;
            transition: transform 0.3s;
        }
        
        .card:hover i {
            transform: scale(1.2) rotate(5deg);
        }

        /* --- معرض الصور التفاعلي --- */
        .gallery-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .gallery-item {
            position: relative;
            border-radius: 15px;
            overflow: hidden;
            height: 250px;
            cursor: pointer;
            transition: all 0.4s;
        }
        
        .gallery-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.7), 0 0 30px rgba(255,215,0,0.2);
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        .gallery-overlay {
            position: absolute;
            bottom: 0;
            right: 0;
            width: 100%;
            padding: 20px;
            background: linear-gradient(to top, rgba(0,0,0,0.9), transparent);
            color: white;
            transform: translateY(100%);
            transition: transform 0.3s;
        }
        
        .gallery-item:hover .gallery-overlay {
            transform: translateY(0);
        }
        
        /* قائمة الأسعار */
        .pricing-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 25px;
            margin-top: 50px;
        }
        
        .pricing-card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(255,215,0,0.1);
            transition: all 0.3s;
            backdrop-filter: blur(10px);
        }
        
        .pricing-card:hover {
            border-color: var(--primary-gold);
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.5);
        }
        
        .pricing-card h3 {
            color: var(--primary-gold);
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(255,215,0,0.2);
            font-size: 1.5rem;
        }
        
        .price-item {
            display: flex;
            justify-content: space-between;
            padding: 15px 0;
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }
        
        .price-item:last-child {
            border-bottom: none;
        }
        
        .price-name {
            font-weight: 600;
        }
        
        .price-value {
            color: var(--primary-gold);
            font-weight: 700;
        }
        
        .price-note {
            font-size: 0.8rem;
            color: #aaa;
            margin-top: 5px;
            display: block;
        }
        
        .special-price {
            background: linear-gradient(45deg, rgba(255,215,0,0.1), transparent);
            border: 1px solid var(--primary-gold);
            position: relative;
            overflow: hidden;
        }
        
        .special-price::before {
            content: 'مميز';
            position: absolute;
            top: 10px;
            left: 10px;
            background: var(--primary-gold);
            color: #000;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
        }

        /* --- الفوتر --- */
        footer {
            background: #000;
            padding: 70px 10% 30px;
            text-align: center;
            border-top: 1px solid rgba(255,215,0,0.1);
            position: relative;
            overflow: hidden;
        }
        
        footer::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(255,215,0,0.1), transparent 70%);
        }
        
        .socials {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .socials a {
            display: inline-flex;
            width: 50px; 
            height: 50px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            align-items: center; 
            justify-content: center;
            color: #fff;
            transition: all 0.3s;
        }
        
        .socials a:hover {
            background: var(--primary-gold);
            color: #000;
            transform: translateY(-5px) rotate(360deg);
            box-shadow: 0 10px 20px rgba(255,215,0,0.3);
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin: 30px 0;
            flex-wrap: wrap;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            color: #ccc;
        }
        
        .contact-item i {
            color: var(--primary-gold);
        }

        /* --- نموذج الحجز --- */
        .booking-form {
            max-width: 600px;
            margin: 50px auto;
            background: var(--card-bg);
            padding: 40px;
            border-radius: 20px;
            border: 1px solid rgba(255,215,0,0.1);
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 10px;
            color: #ccc;
        }
        
        .form-control {
            width: 100%;
            padding: 15px;
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 10px;
            color: #fff;
            font-family: 'Tajawal', sans-serif;
            transition: all 0.3s;
        }
        
        .form-control:focus {
            border-color: var(--primary-gold);
            box-shadow: 0 0 15px rgba(255,215,0,0.2);
        }
        
        /* --- Modal للصور --- */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.9);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .modal.active {
            display: flex;
        }
        
        .modal-content {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.8);
        }
        
        .modal-content img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .modal-close {
            position: absolute;
            top: 20px;
            left: 20px;
            background: rgba(0,0,0,0.5);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .modal-close:hover {
            background: var(--primary-gold);
            color: #000;
        }

        /* --- شريط التقدم --- */
        .progress-bar {
            position: fixed;
            top: 0;
            right: 0;
            width: 0%;
            height: 3px;
            background: var(--primary-gold);
            z-index: 1001;
            transition: width 0.3s;
        }

        /* --- Responsive --- */
        @media (max-width: 992px) {
            .hero-content h1 { font-size: 4rem; }
            .section-title h2 { font-size: 2.5rem; }
        }
        
        @media (max-width: 768px) {
            header { 
                width: 95%; 
                padding: 12px 20px; 
                top: 10px;
            }
            
            .hero-content h1 { font-size: 3rem; }
            .typing-text { font-size: 1.2rem; }
            
            nav {
                position: fixed; 
                top: 0; 
                right: -100%;
                width: 80%; 
                height: 100vh;
                background: rgba(10, 10, 10, 0.95);
                padding: 80px 30px 30px; 
                flex-direction: column;
                transition: right 0.5s;
                backdrop-filter: blur(10px);
                z-index: 1000;
            }
            
            nav.show { right: 0; }
            
            nav ul { 
                flex-direction: column; 
                gap: 20px;
            }
            
            .mobile-menu-btn { 
                display: block; 
            }
            
            section { padding: 80px 5%; }
            
            .pricing-container {
                grid-template-columns: 1fr;
            }
            
            .contact-info {
                flex-direction: column;
                gap: 20px;
            }
        }
        
        @media (max-width: 480px) {
            .hero-content h1 { font-size: 2.5rem; }
            .section-title h2 { font-size: 2rem; }
            .btn { padding: 12px 25px; }
            .gallery-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- مؤشر الماوس -->
    <div class="cursor" id="cursor"></div>
    
    <!-- شريط التقدم -->
    <div class="progress-bar" id="progressBar"></div>

    <!-- الخلفية -->
    <div class="background-fx"></div>

    <!-- القائمة -->
    <header id="mainHeader">
        <div class="logo">
            <i class="fas fa-cut"></i>
            أركان <span>الرجل</span>
        </div>
        <div class="mobile-menu-btn" onclick="toggleNav()">
            <i class="fas fa-bars" id="menuIcon"></i>
        </div>
        <nav id="navbar">
            <ul>
                <li><a href="#home" class="active" onclick="closeNav()">الرئيسية</a></li>
                <li><a href="#services" onclick="closeNav()">خدماتنا</a></li>
                <li><a href="#gallery" onclick="closeNav()">معرض الصور</a></li>
                <li><a href="#pricing" onclick="closeNav()">قائمة الأسعار</a></li>
                <li><a href="#booking" onclick="closeNav()">حجز موعد</a></li>
                <li><a href="#contact" onclick="closeNav()">اتصل بنا</a></li>
            </ul>
        </nav>
    </header>

    <!-- الواجهة الرئيسية -->
    <section class="hero" id="home">
        <div class="hero-bg-img"></div>
        <div class="hero-content animate__animated animate__fadeInUp">
            <h1>صالون أركان الرجل</h1>
            <div class="typing-text">
                المكان الذي يلتقي فيه <span id="typewriter"></span><span class="cursor-blink"></span>
            </div>
            <p class="animate__animated animate__fadeIn animate__delay-1s" style="margin-bottom: 30px; font-size: 1.2rem; color: #ccc;">
                صالون حلاقة وتجميل متكامل للرجال، نقدم خدمات عالمية بلمسة محلية
            </p>
            <div class="animate__animated animate__fadeIn animate__delay-1s">
                <a href="https://wa.me/9660596160783" class="btn btn-whatsapp">
                    <i class="fab fa-whatsapp"></i> احجز عبر واتساب
                </a>
                <a href="#gallery" class="btn btn-outline">
                    <i class="fas fa-images"></i> تصفح معرضنا
                </a>
            </div>
        </div>
    </section>

    <!-- الخدمات -->
    <section id="services">
        <div class="section-bg" style="background: url('https://images.unsplash.com/photo-1560066984-138dadb4c035?q=80&w=1974&auto=format&fit=crop') center/cover;"></div>
        <div class="section-title animate__animated animate__fadeIn">
            <h2>خدماتنا <span>المميزة</span></h2>
            <p style="color: #aaa; max-width: 700px; margin: 0 auto;">نقدم مجموعة متكاملة من خدمات التجميل والحلاقة للرجال بأعلى معايير الجودة والنظافة</p>
        </div>
        <div class="grid-container">
            <div class="card wow animate__animated animate__fadeInUp">
                <i class="fas fa-cut"></i>
                <h3>قصات الشعر الدقيقة</h3>
                <p>أحدث صيحات قصات الشعر العالمية بأيدي خبراء مدربين، باستخدام أدوات معقمة 100%.</p>
            </div>
            <div class="card wow animate__animated animate__fadeInUp animate__delay-1s">
                <i class="fas fa-hot-tub"></i>
                <h3>سبا العناية بالبشرة</h3>
                <p>تنظيف وترطيب عميق ليعيد لبشرتك حيويتها ونضارتها مع استخدام أفضل المنتجات العالمية.</p>
            </div>
            <div class="card wow animate__animated animate__fadeInUp animate__delay-2s">
                <i class="fas fa-crown"></i>
                <h3>العناية الملكية المتكاملة</h3>
                <p>خدمات متكاملة تشمل الحلاقة والشعر والمساج وتصفيف اللحى بالشكل الأمثل.</p>
            </div>
        </div>
    </section>

    <!-- معرض الصور -->
    <section id="gallery" style="background: rgba(0,0,0,0.5);">
        <div class="section-title animate__animated animate__fadeIn">
            <h2>معرض <span>الصور</span></h2>
            <p style="color: #aaa; max-width: 700px; margin: 0 auto;">تصفح أعمالنا واطلع على أحدث صيحات الحلاقة والتجميل للرجال</p>
        </div>
        
        <div class="gallery-container">
            <!-- صور الحلاقة -->
            <div class="gallery-item" onclick="openModal('https://images.unsplash.com/photo-1567894340315-735d7c361db0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80')">
                <img src="https://images.unsplash.com/photo-1567894340315-735d7c361db0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80" alt="حلاقة الشعر">
                <div class="gallery-overlay">
                    <h4>قصات شعر عصرية</h4>
                    <p>أحدث صيحات قصات الشعر للرجال</p>
                </div>
            </div>
            
            <!-- تصفيف اللحية -->
            <div class="gallery-item" onclick="openModal('https://images.unsplash.com/photo-1621605815971-fbc98d665033?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2074&q=80')">
                <img src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2074&q=80" alt="تصفيف اللحية">
                <div class="gallery-overlay">
                    <h4>تحديد وتصفيف اللحية</h4>
                    <p>تشكيل اللحية بأحدث الأساليب</p>
                </div>
            </div>
            
            <!-- العناية بالبشرة -->
            <div class="gallery-item" onclick="openModal('https://images.unsplash.com/photo-1542902097-0a53d63086bb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80')">
                <img src="https://images.unsplash.com/photo-1542902097-0a53d63086bb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="العناية بالبشرة">
                <div class="gallery-overlay">
                    <h4>العناية بالبشرة</h4>
                    <p>تنظيف وترطيب البشرة</p>
                </div>
            </div>
            
            <!-- الحلاقة التقليدية -->
            <div class="gallery-item" onclick="openModal('https://images.unsplash.com/photo-1567894340315-735d7c361db0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80')">
                <img src="https://images.unsplash.com/photo-1580618672591-eb180b1a973f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2069&q=80" alt="الحلاقة التقليدية">
                <div class="gallery-overlay">
                    <h4>الحلاقة بالشفرة</h4>
                    <p>حلاقة تقليدية بلمسة عصرية</p>
                </div>
            </div>
            
            <!-- صبغ الشعر -->
            <div class="gallery-item" onclick="openModal('https://images.unsplash.com/photo-1562169101-90343d48e463?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2069&q=80')">
                <img src="https://images.unsplash.com/photo-1562169101-90343d48e463?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2069&q=80" alt="صبغ الشعر">
                <div class="gallery-overlay">
                    <h4>صبغ الشعر وإخفاء الشيب</h4>
                    <p>ألوان طبيعية تدوم طويلاً</p>
                </div>
            </div>
            
            <!-- تجهيز العرسان -->
            <div class="gallery-item" onclick="openModal('https://images.unsplash.com/photo-1539635278303-d4002c07eae3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80')">
                <img src="https://images.unsplash.com/photo-1539635278303-d4002c07eae3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="تجهيز العرسان">
                <div class="gallery-overlay">
                    <h4>باقة العروسين</h4>
                    <p>خدمات متكاملة ليوم الزفاف</p>
                </div>
            </div>
        </div>
    </section>

    <!-- قائمة الأسعار -->
    <section id="pricing">
        <div class="section-bg" style="background: url('https://images.unsplash.com/photo-1605497788044-5a32c7078486?q=80&w=2070&auto=format&fit=crop') center/cover;"></div>
        <div class="section-title animate__animated animate__fadeIn">
            <h2>قائمة <span>الأسعار</span></h2>
            <p style="color: #aaa; max-width: 700px; margin: 0 auto;">أسعارنا تنافسية مع ضمان أعلى جودة في الخدمة</p>
        </div>
        
        <div class="pricing-container">
            <div class="pricing-card">
                <h3><i class="fas fa-cut"></i> خدمات الحلاقة</h3>
                <div class="price-item">
                    <span class="price-name">حلاقة دقن</span>
                    <span class="price-value">20 ريال</span>
                </div>
                <div class="price-item">
                    <span class="price-name">حلاقة شعر</span>
                    <span class="price-value">20 ريال</span>
                </div>
                <div class="price-item">
                    <span class="price-name">حلاقة شعر ماكينة</span>
                    <span class="price-value">15 ريال</span>
                </div>
                <div class="price-item">
                    <span class="price-name">حلاقة شعر موس</span>
                    <span class="price-value">20 ريال</span>
                </div>
                <div class="price-item">
                    <span class="price-name">استشوار</span>
                    <span class="price-value">20 ريال</span>
                </div>
            </div>
            
            <div class="pricing-card">
                <h3><i class="fas fa-spa"></i> خدمات العناية</h3>
                <div class="price-item">
                    <span class="price-name">صنفرة</span>
                    <span class="price-value">15 ريال</span>
                </div>
                <div class="price-item">
                    <span class="price-name">حمام زيت للشعر</span>
                    <span class="price-value">30 ريال</span>
                </div>
                <div class="price-item">
                    <span class="price-name">صبغ شعر</span>
                    <span class="price-value">50 ريال</span>
                </div>
                <div class="price-item">
                    <span class="price-name">صبغ دقن</span>
                    <span class="price-value">25 ريال</span>
                </div>
                <div class="price-item">
                    <span class="price-name">تنظيف بشرة</span>
                    <span class="price-value">50 - 80 - 150 ريال</span>
                    <span class="price-note">حسب نوع الخدمة</span>
                </div>
            </div>
            
            <div class="pricing-card special-price">
                <h3><i class="fas fa-gem"></i> الباقات المميزة</h3>
                <div class="price-item">
                    <span class="price-name">باقة حلاقة متكاملة</span>
                    <span class="price-value">60 ريال</span>
                    <span class="price-note">(شعر + دقن + صنفرة)</span>
                </div>
                <div class="price-item">
                    <span class="price-name">باقة العناية الكاملة</span>
                    <span class="price-value">120 ريال</span>
                    <span class="price-note">(تنظيف بشرة + حمام زيت + حلاقة)</span>
                </div>
                <div class="price-item">
                    <span class="price-name">تجهيز عرسان</span>
                    <span class="price-value">250 ريال</span>
                    <span class="price-note">(خدمات متكاملة ليوم الزفاف)</span>
                </div>
                <div class="price-item">
                    <span class="price-name">باقة شهرية</span>
                    <span class="price-value">300 ريال</span>
                    <span class="price-note">(4 زيارات + خدمة مجانية)</span>
                </div>
            </div>
        </div>
    </section>

    <!-- نموذج الحجز -->
    <section id="booking">
        <div class="section-title animate__animated animate__fadeIn">
            <h2>حجز <span>موعد</span></h2>
            <p style="color: #aaa; max-width: 700px; margin: 0 auto;">احجز موعدك الآن واستمتع بخدماتنا المميزة</p>
        </div>
        
        <div class="booking-form">
            <form id="bookingForm">
                <div class="form-group">
                    <label for="name"><i class="fas fa-user"></i> الاسم الكامل</label>
                    <input type="text" id="name" class="form-control" placeholder="أدخل اسمك الكامل" required>
                </div>
                
                <div class="form-group">
                    <label for="phone"><i class="fas fa-phone"></i> رقم الهاتف</label>
                    <input type="tel" id="phone" class="form-control" placeholder="مثال: 05xxxxxxxx" required>
                </div>
                
                <div class="form-group">
                    <label for="service"><i class="fas fa-concierge-bell"></i> نوع الخدمة</label>
                    <select id="service" class="form-control" required>
                        <option value="">اختر الخدمة</option>
                        <option value="حلاقة شعر">حلاقة شعر - 20 ريال</option>
                        <option value="حلاقة دقن">حلاقة دقن - 20 ريال</option>
                        <option value="حلاقة شعر موس">حلاقة شعر موس - 20 ريال</option>
                        <option value="باقة حلاقة متكاملة">باقة حلاقة متكاملة - 60 ريال</option>
                        <option value="تنظيف بشرة">تنظيف بشرة - 50 ريال</option>
                        <option value="تجهيز عرسان">تجهيز عرسان - 250 ريال</option>
                        <option value="خدمات أخرى">خدمات أخرى</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="date"><i class="fas fa-calendar-alt"></i> التاريخ والوقت المناسب</label>
                    <input type="datetime-local" id="date" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="notes"><i class="fas fa-sticky-note"></i> ملاحظات إضافية</label>
                    <textarea id="notes" class="form-control" rows="3" placeholder="أي ملاحظات أو طلبات خاصة"></textarea>
                </div>
                
                <button type="submit" class="btn btn-whatsapp" style="width: 100%;">
                    <i class="fab fa-whatsapp"></i> تأكيد الحجز عبر واتساب
                </button>
            </form>
        </div>
    </section>

    <!-- الفوتر -->
    <footer id="contact">
        <div class="logo" style="justify-content: center; margin-bottom: 30px;">
            <i class="fas fa-cut"></i>
            أركان <span>الرجل</span>
        </div>
        
        <div class="socials">
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="https://wa.me/9660596160783"><i class="fab fa-whatsapp"></i></a>
            <a href="#"><i class="fab fa-snapchat-ghost"></i></a>
        </div>
        
        <div class="contact-info">
            <div class="contact-item">
                <i class="fas fa-map-marker-alt"></i>
                <span>الدمام - المملكة العربية السعودية</span>
            </div>
            <div class="contact-item">
                <i class="fas fa-phone"></i>
                <span>0596160783</span>
            </div>
            <div class="contact-item">
                <i class="fas fa-clock"></i>
                <span>الأحد - الخميس: 9 صباحاً - 11 مساءً</span>
            </div>
        </div>
        
        <p style="margin-top: 40px; color: #666;">&copy; 2023 صالون أركان الرجل للحلاقة. جميع الحقوق محفوظة.</p>
        <p style="color: var(--primary-gold); margin-top: 10px; font-size: 0.9rem;">تصميم وتطوير بخبرة محترفين</p>
    </footer>

    <!-- Modal للصور -->
    <div class="modal" id="imageModal">
        <div class="modal-close" onclick="closeModal()">
            <i class="fas fa-times"></i>
        </div>
        <div class="modal-content">
            <img id="modalImage" src="" alt="صورة معرض">
        </div>
    </div>

    <script>
        // 1. تأثير الآلة الكاتبة (Typewriter Effect)
        const words = ["الأناقة", "الجودة", "التميز", "الراحة", "الفخامة"];
        let i = 0;
        let timer;
        let isDeleting = false;

        function typeWriter() {
            const heading = document.getElementById("typewriter");
            const word = words[i];
            const currentText = heading.textContent;
            
            if (!isDeleting && currentText !== word) {
                // كتابة الحروف
                heading.textContent = word.substring(0, currentText.length + 1);
                timer = setTimeout(typeWriter, 150); 
            } else if (!isDeleting && currentText === word) {
                // انتظار بعد كتابة الكلمة
                isDeleting = true;
                timer = setTimeout(typeWriter, 2000); 
            } else if (isDeleting && currentText !== "") {
                // مسح الحروف
                heading.textContent = word.substring(0, currentText.length - 1);
                timer = setTimeout(typeWriter, 100);
            } else {
                // الانتقال للكلمة التالية
                isDeleting = false;
                i = (i + 1) % words.length;
                timer = setTimeout(typeWriter, 500);
            }
        }
        
        // 2. تأثير الماوس (Cursor Follower)
        const cursor = document.getElementById('cursor');
        document.addEventListener('mousemove', (e) => {
            cursor.style.left = e.clientX + 'px';
            cursor.style.top = e.clientY + 'px';
        });
        
        // تأثير زيادة حجم المؤشر عند التمرير على عناصر تفاعلية
        const interactiveElements = document.querySelectorAll('a, button, .card, .gallery-item, .pricing-card');
        interactiveElements.forEach(el => {
            el.addEventListener('mouseenter', () => {
                cursor.classList.add('hover');
            });
            el.addEventListener('mouseleave', () => {
                cursor.classList.remove('hover');
            });
        });

        // 3. التحكم بالقائمة في الجوال
        function toggleNav() {
            const nav = document.getElementById('navbar');
            const menuIcon = document.getElementById('menuIcon');
            nav.classList.toggle('show');
            
            if (nav.classList.contains('show')) {
                menuIcon.classList.remove('fa-bars');
                menuIcon.classList.add('fa-times');
            } else {
                menuIcon.classList.remove('fa-times');
                menuIcon.classList.add('fa-bars');
            }
        }
        
        function closeNav() {
            const nav = document.getElementById('navbar');
            const menuIcon = document.getElementById('menuIcon');
            nav.classList.remove('show');
            menuIcon.classList.remove('fa-times');
            menuIcon.classList.add('fa-bars');
        }

        // 4. تأثير Header عند التمرير
        window.addEventListener('scroll', () => {
            const header = document.getElementById('mainHeader');
            const progressBar = document.getElementById('progressBar');
            
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
            
            // شريط التقدم
            const windowHeight = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrolled = (window.scrollY / windowHeight) * 100;
            progressBar.style.width = scrolled + '%';
            
            // تفعيل الرسوم المتحركة عند التمرير
            animateOnScroll();
        });

        // 5. نموذج الحجز
        document.getElementById('bookingForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const service = document.getElementById('service').value;
            const date = document.getElementById('date').value;
            const notes = document.getElementById('notes').value;
            
            // تنسيق الرسالة
            const message = `*حجز موعد - صالون أركان الرجل*
            
الاسم: ${name}
رقم الهاتف: ${phone}
الخدمة المطلوبة: ${service}
التاريخ والوقت: ${date}
${notes ? `ملاحظات: ${notes}` : ''}

شكراً لحجزك معنا، سنتواصل معك قريباً لتأكيد الموعد.`;
            
            // تشفير الرسالة لرابط واتساب
            const encodedMessage = encodeURIComponent(message);
            const whatsappURL = `https://wa.me/9660596160783?text=${encodedMessage}`;
            
            // فتح واتساب
            window.open(whatsappURL, '_blank');
            
            // إعادة تعيين النموذج
            this.reset();
            
            // رسالة تأكيد
            alert('شكراً لحجزك! سيتم فتح تطبيق واتساب لإرسال تفاصيل الحجز.');
        });

        // 6. Modal للصور
        function openModal(imageSrc) {
            const modal = document.getElementById('imageModal');
            const modalImage = document.getElementById('modalImage');
            
            modalImage.src = imageSrc;
            modal.classList.add('active');
            document.body.style.overflow = 'hidden';
        }
        
        function closeModal() {
            const modal = document.getElementById('imageModal');
            modal.classList.remove('active');
            document.body.style.overflow = 'auto';
        }
        
        // إغلاق Modal عند الضغط على ESC
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') {
                closeModal();
            }
        });
        
        // إغلاق Modal عند النقر خارج الصورة
        document.getElementById('imageModal').addEventListener('click', (e) => {
            if (e.target.id === 'imageModal') {
                closeModal();
            }
        });

        // 7. تفعيل الرسوم المتحركة عند التمرير
        function animateOnScroll() {
            const elements = document.querySelectorAll('.card, .gallery-item, .pricing-card');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.2;
                
                if (elementPosition < screenPosition) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        }
        
        // بدء التأثيرات عند التحميل
        document.addEventListener('DOMContentLoaded', () => {
            typeWriter();
            animateOnScroll();
            
            // تعيين التاريخ الحالي كأقل تاريخ في حجز المواعيد
            const now = new Date();
            const future = new Date(now.getTime() + 24 * 60 * 60 * 1000); // بعد يوم واحد
            const dateInput = document.getElementById('date');
            
            // تنسيق التاريخ للعنصر input
            const formattedDate = future.toISOString().slice(0, 16);
            dateInput.min = formattedDate;
            
            // تعيين القيمة الافتراضية لليوم التالي في نفس الوقت
            dateInput.value = formattedDate;
        });

        // 8. التنقل النشط في القائمة
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('nav a');
        
        window.addEventListener('scroll', () => {
            let current = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                
                if (pageYOffset >= (sectionTop - 200)) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>