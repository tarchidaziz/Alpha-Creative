<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alpha Creative | فيلميكر & مصمم جرافيك & مصور</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-green: #006233;
            --secondary-green: #005529;
            --accent-red: #d21034;
            --star-red: #d21034;
            --black: #0a0a0a;
            --dark-gray: #1a1a1a;
            --white: #ffffff;
            --light-gray: #f5f5f5;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--black);
            color: var(--white);
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Algerian Flag Badge */
        .algeria-badge {
            position: fixed;
            top: 100px;
            left: 20px;
            z-index: 999;
            background: linear-gradient(135deg, var(--primary-green) 0%, var(--secondary-green) 100%);
            padding: 10px 15px;
            border-radius: 10px;
            border: 2px solid var(--white);
            box-shadow: 0 5px 20px rgba(0, 98, 51, 0.4);
            display: flex;
            align-items: center;
            gap: 10px;
            animation: slideInLeft 1s ease;
        }

        .algeria-badge img {
            width: 30px;
            height: 20px;
            border-radius: 3px;
        }

        .algeria-badge span {
            font-size: 12px;
            font-weight: 700;
            color: var(--white);
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-100px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 20px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(0, 98, 51, 0.3);
            transition: all 0.3s ease;
        }

        .logo {
            font-size: 28px;
            font-weight: 900;
            background: linear-gradient(135deg, var(--white) 0%, var(--primary-green) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 2px;
        }

        .logo span {
            color: var(--primary-green);
            -webkit-text-fill-color: var(--primary-green);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 40px;
        }

        .nav-links a {
            color: var(--white);
            text-decoration: none;
            font-weight: 600;
            position: relative;
            transition: color 0.3s ease;
            font-size: 16px;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            right: 0;
            width: 0;
            height: 2px;
            background: var(--primary-green);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--primary-green);
        }

        .mobile-menu {
            display: none;
            font-size: 24px;
            cursor: pointer;
            color: var(--white);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(135deg, var(--black) 0%, #001a0d 50%, var(--black) 100%);
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 50%, rgba(0, 98, 51, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(210, 16, 52, 0.1) 0%, transparent 50%);
            pointer-events: none;
        }

        .hero-content {
            text-align: center;
            z-index: 2;
            padding: 0 20px;
            max-width: 900px;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 10px 25px;
            background: rgba(0, 98, 51, 0.2);
            border: 1px solid var(--primary-green);
            border-radius: 50px;
            color: var(--primary-green);
            font-weight: 600;
            margin-bottom: 30px;
            font-size: 14px;
            letter-spacing: 2px;
            animation: fadeInDown 1s ease;
        }

        .hero-badge i {
            color: var(--accent-red);
        }

        .hero h1 {
            font-size: 72px;
            font-weight: 900;
            margin-bottom: 20px;
            line-height: 1.2;
            animation: fadeInUp 1s ease 0.2s both;
            text-shadow: 0 0 40px rgba(0, 98, 51, 0.3);
        }

        .hero h1 .highlight {
            background: linear-gradient(135deg, var(--primary-green) 0%, #00cc66 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-subtitle {
            font-size: 24px;
            color: #aaa;
            margin-bottom: 40px;
            font-weight: 300;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            animation: fadeInUp 1s ease 0.6s both;
        }

        .btn {
            padding: 15px 40px;
            border: none;
            border-radius: 50px;
            font-size: 16px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            font-family: 'Cairo', sans-serif;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--primary-green) 0%, #00cc66 100%);
            color: var(--white);
            box-shadow: 0 10px 30px rgba(0, 98, 51, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(0, 98, 51, 0.6);
        }

        .btn-secondary {
            background: transparent;
            color: var(--white);
            border: 2px solid var(--white);
        }

        .btn-secondary:hover {
            background: var(--white);
            color: var(--black);
            transform: translateY(-3px);
        }

        .scroll-indicator {
            position: absolute;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            animation: bounce 2s infinite;
            color: var(--primary-green);
            font-size: 24px;
        }

        /* Services Section */
        .services {
            padding: 100px 50px;
            background: var(--dark-gray);
            position: relative;
        }

        .section-header {
            text-align: center;
            margin-bottom: 80px;
        }

        .section-tag {
            color: var(--primary-green);
            font-weight: 700;
            letter-spacing: 3px;
            font-size: 14px;
            margin-bottom: 15px;
            display: block;
        }

        .section-title {
            font-size: 48px;
            font-weight: 900;
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-green), var(--accent-red));
            border-radius: 2px;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .service-card {
            background: linear-gradient(145deg, #1e1e1e 0%, #151515 100%);
            padding: 50px 40px;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            text-align: center;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-green), var(--accent-red));
            transform: scaleX(0);
            transition: transform 0.4s ease;
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-card:hover {
            transform: translateY(-10px);
            border-color: rgba(0, 98, 51, 0.3);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
        }

        .service-icon {
            font-size: 50px;
            color: var(--primary-green);
            margin-bottom: 25px;
            display: block;
        }

        .service-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: var(--white);
        }

        .service-card p {
            color: #888;
            line-height: 1.8;
            font-size: 15px;
        }

        /* Portfolio Section */
        .portfolio {
            padding: 100px 50px;
            background: var(--black);
        }

        .portfolio-filter {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 50px;
            flex-wrap: wrap;
        }

        .filter-btn {
            padding: 10px 25px;
            background: transparent;
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: var(--white);
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-family: 'Cairo', sans-serif;
            font-weight: 600;
        }

        .filter-btn.active,
        .filter-btn:hover {
            background: var(--primary-green);
            border-color: var(--primary-green);
            color: var(--white);
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 25px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .portfolio-item {
            position: relative;
            border-radius: 15px;
            overflow: hidden;
            aspect-ratio: 16/10;
            cursor: pointer;
            background: linear-gradient(145deg, #1e1e1e 0%, #151515 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px dashed rgba(0, 98, 51, 0.3);
        }

        .portfolio-placeholder {
            text-align: center;
            padding: 40px;
            color: #666;
        }

        .portfolio-placeholder i {
            font-size: 60px;
            color: var(--primary-green);
            margin-bottom: 20px;
            opacity: 0.5;
        }

        .portfolio-placeholder h3 {
            font-size: 20px;
            margin-bottom: 10px;
            color: #888;
        }

        .portfolio-placeholder p {
            font-size: 14px;
        }

        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to top, rgba(0, 38, 20, 0.95) 0%, transparent 100%);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 30px;
            opacity: 0;
            transition: all 0.4s ease;
        }

        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }

        .portfolio-item.real-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s ease;
        }

        .portfolio-item.real-item:hover img {
            transform: scale(1.1);
        }

        .portfolio-category {
            color: var(--primary-green);
            font-size: 14px;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .portfolio-title {
            font-size: 24px;
            font-weight: 700;
            color: var(--white);
        }

        .play-btn {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0);
            width: 80px;
            height: 80px;
            background: rgba(0, 98, 51, 0.9);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 24px;
            transition: all 0.4s ease;
            backdrop-filter: blur(10px);
        }

        .portfolio-item:hover .play-btn {
            transform: translate(-50%, -50%) scale(1);
        }

        /* About Section */
        .about {
            padding: 100px 50px;
            background: linear-gradient(135deg, #001a0d 0%, var(--black) 100%);
            position: relative;
            overflow: hidden;
        }

        .about::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(0, 98, 51, 0.1) 0%, transparent 70%);
            pointer-events: none;
        }

        .about-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 80px;
            align-items: center;
        }

        .about-image {
            position: relative;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.5);
            background: linear-gradient(145deg, #1e1e1e 0%, #151515 100%);
            min-height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px dashed rgba(0, 98, 51, 0.3);
        }

        .about-image-placeholder {
            text-align: center;
            padding: 40px;
            color: #666;
        }

        .about-image-placeholder i {
            font-size: 80px;
            color: var(--primary-green);
            margin-bottom: 20px;
            opacity: 0.5;
        }

        .about-image-placeholder p {
            font-size: 18px;
        }

        .experience-badge {
            position: absolute;
            bottom: -20px;
            left: -20px;
            background: linear-gradient(135deg, var(--primary-green) 0%, var(--secondary-green) 100%);
            color: var(--white);
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0, 98, 51, 0.4);
        }

        .experience-badge .number {
            font-size: 48px;
            font-weight: 900;
            display: block;
            line-height: 1;
        }

        .experience-badge .text {
            font-size: 14px;
            font-weight: 600;
        }

        .about-content h2 {
            font-size: 42px;
            margin-bottom: 30px;
            line-height: 1.3;
        }

        .about-content p {
            color: #aaa;
            margin-bottom: 20px;
            font-size: 16px;
            line-height: 1.8;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            margin-top: 40px;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 36px;
            font-weight: 900;
            color: var(--primary-green);
            display: block;
        }

        .stat-label {
            color: #888;
            font-size: 14px;
            margin-top: 5px;
        }

        /* Contact Section */
        .contact {
            padding: 100px 50px;
            background: var(--dark-gray);
        }

        .contact-container {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
        }

        .contact-info h3 {
            font-size: 32px;
            margin-bottom: 20px;
        }

        .contact-info p {
            color: #aaa;
            margin-bottom: 40px;
            line-height: 1.8;
        }

        .contact-details {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .contact-icon {
            width: 60px;
            height: 60px;
            background: rgba(0, 98, 51, 0.1);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-green);
            font-size: 24px;
            border: 1px solid rgba(0, 98, 51, 0.2);
        }

        .contact-text h4 {
            font-size: 18px;
            margin-bottom: 5px;
        }

        .contact-text p {
            color: #888;
            margin: 0;
            font-size: 14px;
            direction: ltr;
            text-align: right;
        }

        .contact-form {
            background: #1e1e1e;
            padding: 50px;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 10px;
            color: var(--white);
            font-weight: 600;
            font-size: 14px;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 15px 20px;
            background: #151515;
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            color: var(--white);
            font-family: 'Cairo', sans-serif;
            font-size: 15px;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: var(--primary-green);
            box-shadow: 0 0 0 3px rgba(0, 98, 51, 0.1);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .submit-btn {
            width: 100%;
            padding: 18px;
            background: linear-gradient(135deg, var(--primary-green) 0%, var(--secondary-green) 100%);
            color: var(--white);
            border: none;
            border-radius: 10px;
            font-size: 16px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            font-family: 'Cairo', sans-serif;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(0, 98, 51, 0.4);
        }

        /* Social Media Section */
        .social-section {
            padding: 80px 50px;
            background: var(--black);
            text-align: center;
        }

        .social-grid {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 50px;
            flex-wrap: wrap;
        }

        .social-card {
            width: 150px;
            height: 150px;
            background: linear-gradient(145deg, #1e1e1e 0%, #151515 100%);
            border-radius: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 15px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: all 0.4s ease;
            cursor: pointer;
            text-decoration: none;
            color: var(--white);
        }

        .social-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary-green);
            box-shadow: 0 20px 40px rgba(0, 98, 51, 0.3);
        }

        .social-card i {
            font-size: 40px;
            color: var(--primary-green);
            transition: all 0.3s ease;
        }

        .social-card:hover i {
            color: var(--accent-red);
            transform: scale(1.2);
        }

        .social-card span {
            font-size: 14px;
            font-weight: 600;
        }

        /* Footer */
        footer {
            background: var(--black);
            padding: 60px 50px 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 30px;
        }

        .footer-logo {
            font-size: 24px;
            font-weight: 900;
            color: var(--white);
        }

        .footer-logo span {
            color: var(--primary-green);
        }

        .footer-info {
            text-align: center;
            color: #666;
            font-size: 14px;
        }

        .footer-info i {
            color: var(--accent-red);
            margin: 0 5px;
        }

        .copyright {
            width: 100%;
            text-align: center;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            color: #666;
            font-size: 14px;
        }

        .algeria-flag-footer {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            margin-top: 10px;
            padding: 8px 15px;
            background: rgba(0, 98, 51, 0.1);
            border-radius: 20px;
            border: 1px solid rgba(0, 98, 51, 0.3);
        }

        .algeria-flag-footer img {
            width: 24px;
            height: 16px;
            border-radius: 3px;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateX(-50%) translateY(0);
            }
            40% {
                transform: translateX(-50%) translateY(-10px);
            }
            60% {
                transform: translateX(-50%) translateY(-5px);
            }
        }

        /* Responsive */
        @media (max-width: 968px) {
            .nav-links {
                display: none;
            }

            .mobile-menu {
                display: block;
            }

            .hero h1 {
                font-size: 42px;
            }

            .hero-subtitle {
                font-size: 18px;
            }

            .about-container,
            .contact-container {
                grid-template-columns: 1fr;
            }

            .portfolio-grid {
                grid-template-columns: 1fr;
            }

            .services-grid {
                grid-template-columns: 1fr;
            }

            .stats {
                grid-template-columns: 1fr;
                gap: 20px;
            }

            .experience-badge {
                position: relative;
                bottom: auto;
                left: auto;
                margin-top: 20px;
            }

            .algeria-badge {
                top: 80px;
                left: 10px;
                padding: 8px 12px;
            }

            .social-grid {
                gap: 20px;
            }

            .social-card {
                width: 120px;
                height: 120px;
            }
        }

        /* Scroll Animation Classes */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>

    <!-- Algeria Badge -->
    <div class="algeria-badge">
        <img src="https://flagcdn.com/w40/dz.png" alt="Algeria Flag">
        <span>صنع في الجزائر 🇩🇿</span>
    </div>

    <!-- Navigation -->
    <nav id="navbar">
        <div class="logo">ALPHA <span>CREATIVE</span></div>
        <ul class="nav-links">
            <li><a href="#home">الرئيسية</a></li>
            <li><a href="#services">الخدمات</a></li>
            <li><a href="#portfolio">أعمالي</a></li>
            <li><a href="#about">من أنا</a></li>
            <li><a href="#social">تواصل اجتماعي</a></li>
            <li><a href="#contact">تواصل</a></li>
        </ul>
        <div class="mobile-menu" onclick="toggleMenu()">
            <i class="fas fa-bars"></i>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <div class="hero-badge">
                <i class="fas fa-star"></i>
                فيلميكر | مصمم جرافيك | مصور
            </div>
            <h1>نحوّل <span class="highlight">رؤيتك</span><br>إلى واقع بصري</h1>
            <p class="hero-subtitle">نصنع محتوى بصرياً استثنائياً ي captivate الجمهور ويترك أثراً لا يُنسى</p>
            <div class="hero-buttons">
                <a href="#portfolio" class="btn btn-primary">شاهد أعمالي</a>
                <a href="#contact" class="btn btn-secondary">تواصل معي</a>
            </div>
        </div>
        <div class="scroll-indicator">
            <i class="fas fa-chevron-down"></i>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="section-header reveal">
            <span class="section-tag">الخدمات</span>
            <h2 class="section-title">ماذا أقدم لك؟</h2>
        </div>
        <div class="services-grid">
            <div class="service-card reveal">
                <i class="fas fa-video service-icon"></i>
                <h3>إنتاج الفيديو والأفلام</h3>
                <p>إنتاج سينمائي احترافي يجمع بين الإبداع والتقنية العالية، من الفكرة حتى الشاشة</p>
            </div>
            <div class="service-card reveal">
                <i class="fas fa-paint-brush service-icon"></i>
                <h3>التصميم الجرافيكي</h3>
                <p>تصاميم بصرية مبتكرة لهويتك التجارية، من الشعارات إلى الهوية الكاملة</p>
            </div>
            <div class="service-card reveal">
                <i class="fas fa-camera service-icon"></i>
                <h3>تصوير المناسبات</h3>
                <p>تغطية شاملة لجميع المناسبات بأعلى معايير الجودة والإحترافية</p>
            </div>
            <div class="service-card reveal">
                <i class="fas fa-bullhorn service-icon"></i>
                <h3>التسويق بالمحتوى البصري</h3>
                <p>استراتيجيات محتوى مرئي تزيد من تواجدك الرقمي وتفاعل جمهورك</p>
            </div>
            <div class="service-card reveal">
                <i class="fas fa-film service-icon"></i>
                <h3>المونتاج والبوست برودكشن</h3>
                <p>مونتاج احترافي وتلوين سينمائي يضفي طابعاً فنياً على مشاريعك</p>
            </div>
            <div class="service-card reveal">
                <i class="fas fa-drone service-icon"></i>
                <h3>التصوير الجوي</h3>
                <p>لقطات جوية مذهلة بالدرونز لإضافة منظور فريد لأعمالك</p>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section class="portfolio" id="portfolio">
        <div class="section-header reveal">
            <span class="section-tag">المعرض</span>
            <h2 class="section-title">أحدث الأعمال</h2>
        </div>
        
        <div class="portfolio-filter reveal">
            <button class="filter-btn active" onclick="filterPortfolio('all')">الكل</button>
            <button class="filter-btn" onclick="filterPortfolio('video')">فيديو</button>
            <button class="filter-btn" onclick="filterPortfolio('photo')">تصوير</button>
            <button class="filter-btn" onclick="filterPortfolio('design')">تصميم</button>
        </div>

        <div class="portfolio-grid">
            <!-- Placeholder for your work - Replace with your actual images -->
            <div class="portfolio-item reveal" data-category="video">
                <div class="portfolio-placeholder">
                    <i class="fas fa-plus-circle"></i>
                    <h3>أضف عملك هنا</h3>
                    <p>فيديو قصير</p>
                </div>
                <div class="portfolio-overlay">
                    <span class="portfolio-category">إنتاج فيديو</span>
                    <h3 class="portfolio-title">عنوان العمل</h3>
                </div>
            </div>
            
            <div class="portfolio-item reveal" data-category="photo">
                <div class="portfolio-placeholder">
                    <i class="fas fa-plus-circle"></i>
                    <h3>أضف عملك هنا</h3>
                    <p>تصوير فوتوغرافي</p>
                </div>
                <div class="portfolio-overlay">
                    <span class="portfolio-category">تصوير فوتوغرافي</span>
                    <h3 class="portfolio-title">عنوان العمل</h3>
                </div>
            </div>

            <div class="portfolio-item reveal" data-category="design">
                <div class="portfolio-placeholder">
                    <i class="fas fa-plus-circle"></i>
                    <h3>أضف عملك هنا</h3>
                    <p>تصميم جرافيك</p>
                </div>
                <div class="portfolio-overlay">
                    <span class="portfolio-category">تصميم جرافيك</span>
                    <h3 class="portfolio-title">عنوان العمل</h3>
                </div>
            </div>

            <div class="portfolio-item reveal" data-category="video">
                <div class="portfolio-placeholder">
                    <i class="fas fa-plus-circle"></i>
                    <h3>أضف عملك هنا</h3>
                    <p>إعلان تجاري</p>
                </div>
                <div class="portfolio-overlay">
                    <span class="portfolio-category">إعلان تجاري</span>
                    <h3 class="portfolio-title">عنوان العمل</h3>
                </div>
            </div>

            <div class="portfolio-item reveal" data-category="photo">
                <div class="portfolio-placeholder">
                    <i class="fas fa-plus-circle"></i>
                    <h3>أضف عملك هنا</h3>
                    <p>تغطية فعالية</p>
                </div>
                <div class="portfolio-overlay">
                    <span class="portfolio-category">تغطية فعاليات</span>
                    <h3 class="portfolio-title">عنوان العمل</h3>
                </div>
            </div>

            <div class="portfolio-item reveal" data-category="design">
                <div class="portfolio-placeholder">
                    <i class="fas fa-plus-circle"></i>
                    <h3>أضف عملك هنا</h3>
                    <p>سوشيال ميديا</p>
                </div>
                <div class="portfolio-overlay">
                    <span class="portfolio-category">سوشيال ميديا</span>
                    <h3 class="portfolio-title">عنوان العمل</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="about-container">
            <div class="about-image reveal">
                <div class="about-image-placeholder">
                    <i class="fas fa-user-circle"></i>
                    <p>أضف صورتك الشخصية هنا</p>
                </div>
                <div class="experience-badge">
                    <span class="number">+5</span>
                    <span class="text">سنوات خبرة</span>
                </div>
            </div>
            <div class="about-content reveal">
                <span class="section-tag">من أنا</span>
                <h2>شغفي هو تحويل الأفكار إلى تجارب بصرية لا تُنسى</h2>
                <p>أنا <strong>محمد طرشيد</strong>، فيلميكر ومصمم جرافيك ومصور محترف من الجزائر، أؤمن بقوة البصر في نقل الرسائل والعواطف. على مدى أكثر من 5 سنوات، ساعدت العلامات التجارية والأفراد على تحويل رؤاهم إلى محتوى بصري استثنائي.</p>
                <p>أجمع بين الخبرة التقنية العالية والنظرة الإبداعية الفريدة لأقدم لك منتجاً يتجاوز التوقعات. سواء كان فيلماً قصيراً، أو حفل زفاف، أو هوية بصرية كاملة، أضمن لك الجودة والإبداع في كل تفصيل.</p>
                
                <div class="stats">
                    <div class="stat-item">
                        <span class="stat-number">+150</span>
                        <span class="stat-label">مشروع منجز</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">+80</span>
                        <span class="stat-label">عميل سعيد</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">+12</span>
                        <span class="stat-label">جائزة محلية</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Social Media Section -->
    <section class="social-section" id="social">
        <div class="section-header reveal">
            <span class="section-tag">تابعني</span>
            <h2 class="section-title">مواقع التواصل الاجتماعي</h2>
        </div>
        
        <div class="social-grid reveal">
            <!-- Instagram -->
            <a href="#" class="social-card" onclick="showSocialMessage('Instagram')">
                <i class="fab fa-instagram"></i>
                <span>إنستغرام</span>
            </a>
            
            <!-- Facebook -->
            <a href="#" class="social-card" onclick="showSocialMessage('Facebook')">
                <i class="fab fa-facebook-f"></i>
                <span>فيسبوك</span>
            </a>
            
            <!-- YouTube -->
            <a href="#" class="social-card" onclick="showSocialMessage('YouTube')">
                <i class="fab fa-youtube"></i>
                <span>يوتيوب</span>
            </a>
            
            <!-- TikTok -->
            <a href="#" class="social-card" onclick="showSocialMessage('TikTok')">
                <i class="fab fa-tiktok"></i>
                <span>تيك توك</span>
            </a>
            
            <!-- Behance -->
            <a href="#" class="social-card" onclick="showSocialMessage('Behance')">
                <i class="fab fa-behance"></i>
                <span>بيهانس</span>
            </a>
            
            <!-- WhatsApp -->
            <a href="https://wa.me/213666412618" target="_blank" class="social-card">
                <i class="fab fa-whatsapp"></i>
                <span>واتساب</span>
            </a>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="section-header reveal">
            <span class="section-tag">تواصل معي</span>
            <h2 class="section-title">لنبدأ مشروعك القادم</h2>
        </div>
        
        <div class="contact-container">
            <div class="contact-info reveal">
                <h3>جاهز لتحويل فكرتك إلى واقع؟</h3>
                <p>سواء كان لديك مشروع واضح أو مجرد فكرة ترغب في تطويرها، أنا هنا لمساعدتك. تواصل معي الآن للحصول على استشارة مجانية وعرض سعر مخصص لاحتياجاتك.</p>
                
                <div class="contact-details">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-text">
                            <h4>الهاتف / واتساب</h4>
                            <p>0666 41 26 18</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">
                            <h4>البريد الإلكتروني</h4>
                            <p>tarchidmohamed439@gmail.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h4>الموقع</h4>
                            <p>الأغواط، الجزائر</p>
                        </div>
                    </div>
                </div>
            </div>

            <div class="contact-form reveal">
                <form onsubmit="handleSubmit(event)">
                    <div class="form-group">
                        <label>الاسم الكامل</label>
                        <input type="text" placeholder="أدخل اسمك" required>
                    </div>
                    
                    <div class="form-group">
                        <label>البريد الإلكتروني</label>
                        <input type="email" placeholder="your@email.com" required>
                    </div>
                    
                    <div class="form-group">
                        <label>نوع الخدمة</label>
                        <select required>
                            <option value="">اختر الخدمة المطلوبة</option>
                            <option value="video">إنتاج فيديو وأفلام</option>
                            <option value="photo">تصوير فوتوغرافي</option>
                            <option value="design">تصميم جرافيك</option>
                            <option value="event">تغطية فعالية</option>
                            <option value="other">أخرى</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label>تفاصيل المشروع</label>
                        <textarea placeholder="أخبرني أكثر عن مشروعك..." required></textarea>
                    </div>
                    
                    <button type="submit" class="submit-btn">إرسال الطلب</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-logo">ALPHA <span>CREATIVE</span></div>
            
            <div class="footer-info">
                <p>صنع بـ <i class="fas fa-heart"></i> في الجزائر</p>
                <div class="algeria-flag-footer">
                    <img src="https://flagcdn.com/w40/dz.png" alt="Algeria Flag">
                    <span>الأغواط، الجزائر</span>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2024 Alpha Creative - Mohamed Tarchid. جميع الحقوق محفوظة.</p>
            </div>
        </div>
    </footer>

    <script>
        // Navbar scroll effect
        window.addEventListener('scroll', function() {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.style.padding = '15px 50px';
                navbar.style.background = 'rgba(10, 10, 10, 0.98)';
            } else {
                navbar.style.padding = '20px 50px';
                navbar.style.background = 'rgba(10, 10, 10, 0.95)';
            }
        });

        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Portfolio filter
        function filterPortfolio(category) {
            const items = document.querySelectorAll('.portfolio-item');
            const buttons = document.querySelectorAll('.filter-btn');
            
            buttons.forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
            
            items.forEach(item => {
                if (category === 'all' || item.dataset.category === category) {
                    item.style.display = 'block';
                    setTimeout(() => {
                        item.style.opacity = '1';
                        item.style.transform = 'scale(1)';
                    }, 10);
                } else {
                    item.style.opacity = '0';
                    item.style.transform = 'scale(0.8)';
                    setTimeout(() => {
                        item.style.display = 'none';
                    }, 300);
                }
            });
        }

        // Scroll reveal animation
        const revealElements = document.querySelectorAll('.reveal');
        
        const revealOnScroll = () => {
            const windowHeight = window.innerHeight;
            const elementVisible = 150;
            
            revealElements.forEach((reveal) => {
                const elementTop = reveal.getBoundingClientRect().top;
                if (elementTop < windowHeight - elementVisible) {
                    reveal.classList.add('active');
                }
            });
        };

        window.addEventListener('scroll', revealOnScroll);
        revealOnScroll(); // Trigger once on load

        // Form submission
        function handleSubmit(e) {
            e.preventDefault();
            alert('شكراً لتواصلك! سأرد عليك في أقرب وقت ممكن.');
            e.target.reset();
        }

        // Mobile menu toggle
        function toggleMenu() {
            const navLinks = document.querySelector('.nav-links');
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        }

        // Social media message
        function showSocialMessage(platform) {
            alert(`سيتم إضافة رابط ${platform} الخاص بك هنا. يمكنك تعديل الكود وإضافة روابطك الحقيقية.`);
        }
    </script>
</body>
</html>
# Alpha-Creative
