<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فروشگاه موسیقی زینب: دنیای نغمه‌های نئونی</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts for Vazirmatn and a more decorative one if available -->
    <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        /* CSS Variables for a dark, neon theme */
        :root {
            --primary-bg: #1a0f30; /* Deep dark purple/blue */
            --secondary-bg: #2b1d40; /* Slightly lighter dark */
            --neon-blue: #00f0ff;
            --neon-pink: #bd00ff;
            --text-light: #e0e0e0;
            --text-dark: #a0a0a0;
            --white: #ffffff;
            --shadow-neon: 0 0 15px rgba(0, 240, 255, 0.6), 0 0 25px rgba(189, 0, 255, 0.4);
            --shadow-soft: 0 4px 15px rgba(0, 0, 0, 0.3);
            --border-gradient: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
        }

        /* Base Styles */
        body {
            font-family: 'Vazirmatn', sans-serif;
            line-height: 1.7;
            color: var(--text-light);
            background-color: var(--primary-bg);
            margin: 0;
            padding: 0;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        .container {
            max-width: 1100px; /* Wider container for a more spacious feel */
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navbar */
        header {
            background-color: rgba(26, 15, 48, 0.8); /* Semi-transparent dark header */
            backdrop-filter: blur(10px); /* Frosted glass effect */
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 2.2rem; /* Larger logo */
            font-weight: 900;
            text-decoration: none;
            position: relative;
            z-index: 1;
        }

        .logo .helia-text {
            /* Styling for "Helia" */
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 8px rgba(0, 240, 255, 0.5); /* Subtle neon glow */
            font-size: 1.2em; /* Emphasize Helia */
        }

        .nav-links {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        .nav-links li {
            margin-right: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-light);
            font-weight: 400;
            transition: color 0.3s ease, text-shadow 0.3s ease;
            position: relative;
            padding-bottom: 5px;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--border-gradient);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--neon-blue);
            text-shadow: 0 0 5px var(--neon-blue);
        }

        .nav-links a:hover::after {
            width: 100%;
        }
        /* Hero Section */
        .hero {
            background: var(--primary-bg);
            padding: 8rem 0 4rem; /* More padding */
            text-align: center;
            min-height: 100vh; /* Full viewport height */
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            border-bottom: 2px solid;
            border-image: var(--border-gradient) 1;
        }

        /* Background Particle/Shape Animation */
        .hero::before, .hero::after {
            content: '';
            position: absolute;
            border-radius: 50%;
            background: rgba(0, 240, 255, 0.1);
            animation: backgroundFloat 15s infinite ease-in-out alternate;
        }
        .hero::before {
            width: 300px; height: 300px; top: 10%; left: -10%;
            animation-delay: 0s;
        }
        .hero::after {
            width: 400px; height: 400px; bottom: 5%; right: -15%;
            background: rgba(189, 0, 255, 0.1);
            animation-delay: 5s;
        }

        @keyframes backgroundFloat {
            0% { transform: translate(0, 0) scale(1); opacity: 0.7; }
            50% { transform: translate(50px, 100px) scale(1.1); opacity: 0.9; }
            100% { transform: translate(0, 0) scale(1); opacity: 0.7; }
        }

        .hero-content {
            max-width: 900px;
            z-index: 2;
            position: relative;
        }

        .hero h1 {
            font-size: 4.5rem; /* Larger, bolder headline */
            margin-bottom: 1.5rem;
            font-weight: 900;
            line-height: 1.1;
            color: var(--white); /* Default for other parts */
            text-shadow: 0 0 20px rgba(0, 240, 255, 0.7); /* Stronger glow */
        }

        .hero h1 .helia-text {
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: var(--shadow-neon);
            display: block; /* Make Helia stand out on its own line or strong visual */
            margin-bottom: 10px;
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 3rem;
            opacity: 0.8;
            color: var(--text-light);
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-button {
            display: inline-block;
            background: var(--border-gradient);
            color: var(--primary-bg); /* Dark text on bright button */
            padding: 1.2rem 3rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.3rem;
            transition: all 0.3s ease;
            box-shadow: var(--shadow-neon);
            border: none;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .cta-button::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 300%;
            height: 300%;
            background: rgba(255, 255, 255, 0.15);
            transition: all 0.5s ease-out;
            border-radius: 50%;
            transform: translate(-50%, -50%) scale(0);
            z-index: -1;
        }

        .cta-button:hover::before {
            transform: translate(-50%, -50%) scale(1);
        }

        .cta-button:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 0 25px rgba(0, 240, 255, 0.8), 0 0 35px rgba(189, 0, 255, 0.6);
            color: var(--white); /* Lighten text on hover */
        }

        .hero-visual {
            margin-top: 4rem;
            width: 500px;
            height: 300px;
            background: url('https://via.placeholder.com/500x300/1a0f30/00f0ff?text=Helia+Soundscape') no-repeat center center/cover;
            border-radius: 20px;
            box-shadow: var(--shadow-neon);
            animation: visualPulse 3s ease-in-out infinite alternate;
            border: 2px solid transparent;
            border-image: var(--border-gradient) 1;
        }

        @keyframes visualPulse {
            0% { transform: scale(1); box-shadow: var(--shadow-neon); }
            100% { transform: scale(1.02); box-shadow: 0 0 20px var(--neon-blue), 0 0 30px var(--neon-pink); }
        }

        /* Section Styling */
        section {
            padding: 6rem 0;
            position: relative;
            overflow: hidden;
        }
        section:nth-of-type(even) {
            background-color: var(--secondary-bg);
        }

        .section-title {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            font-weight: 900;
            color: var(--white);
            text-align: center;
            text-shadow: 0 0 10px rgba(0, 240, 255, 0.3);
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .section-subtitle {
            font-size: 1.3rem;
            color: var(--text-dark);
            margin-bottom: 4rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            text-align: center;
        }

        /* Features Section */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 3rem;
        }

        .feature-item {
            background-color: var(--secondary-bg);
            padding: 35px;
            border-radius: 15px;
            text-align: center;
            box-shadow: var(--shadow-soft);
            transition: transform 0.4s ease, box-shadow 0.4s ease, border-color 0.4s ease;
            border: 1px solid rgba(0, 240, 255, 0.2);
            position: relative;
            overflow: hidden;
        }

        .feature-item::before {
            content: '';
            position: absolute;
            top: -20px;
            right: -20px;
            width: 60px;
            height: 60px;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            border-radius: 50%;
            filter: blur(15px);
            opacity: 0.3;
            transition: all 0.5s ease;
        }

        .feature-item:hover {
            transform: translateY(-15px) scale(1.02);
            box-shadow: var(--shadow-neon);
            border-color: var(--neon-pink);
        }
        .feature-item:hover::before {
            transform: scale(1.5);
            opacity: 0.6;
            top: -30px;
            right: -30px;
        }

        .feature-item i {
            font-size: 4rem;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1.5rem;
            text-shadow: 0 0 10px rgba(0, 240, 255, 0.4);
        }

        .feature-item h3 {
            font-size: 1.8rem;
            color: var(--white);
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .feature-item p {
            font-size: 1.1rem;
            color: var(--text-dark);
        }

        /* Join Us Section */
        .join-us {
            background: var(--primary-bg);
            padding: 8rem 0;
            text-align: center;
            position: relative;
            border-top: 2px solid;
            border-image: var(--border-gradient) 1;
        }
        .join-us-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 3rem;
            max-width: 800px;
            margin: 0 auto;
        }

        .join-us-buttons {
            display: flex;
            gap: 25px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .join-us-buttons a {
            display: inline-flex;
            align-items: center;
            background-color: var(--secondary-bg);
            color: var(--neon-blue);
            padding: 1rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 0 10px rgba(0, 240, 255, 0.3);
            border: 1px solid var(--neon-blue);
        }

        .join-us-buttons a i {
            margin-left: 12px;
            font-size: 1.6rem;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 5px rgba(0, 240, 255, 0.5);
        }

        .join-us-buttons a:hover {
            background: var(--border-gradient);
            color: var(--white);
            transform: translateY(-5px) scale(1.05);
            box-shadow: var(--shadow-neon);
            border-color: transparent;
        }
        .join-us-buttons a:hover i {
            -webkit-text-fill-color: var(--white);
            text-shadow: none;
        }


        .newsletter-form {
            background-color: var(--secondary-bg);
            padding: 40px;
            border-radius: 20px;
            box-shadow: var(--shadow-soft);
            width: 100%;
            max-width: 500px;
            border: 1px solid rgba(189, 0, 255, 0.2);
        }

        .newsletter-form p {
            margin-bottom: 2rem;
            color: var(--text-light);
            font-size: 1.2rem;
            font-weight: 400;
        }

        .newsletter-form label {
            display: block;
            text-align: right;
            margin-bottom: 10px;
            font-weight: 700;
            color: var(--neon-pink);
            font-size: 1.1rem;
        }

        .newsletter-form input[type="email"] {
            width: calc(100% - 24px); /* Account for padding */
            padding: 14px;
            margin-bottom: 20px;
            border: 2px solid var(--neon-blue);
            border-radius: 10px;
            background-color: var(--primary-bg);
            color: var(--white);
            font-family: 'Vazirmatn', sans-serif;
            font-size: 1.1rem;
            text-align: right;
            box-shadow: inset 0 0 5px rgba(0, 240, 255, 0.2);
            transition: border-color 0.3s ease, box-shadow 0.3s ease;
        }

        .newsletter-form input[type="email"]:focus {
            outline: none;
            border-color: var(--neon-pink);
            box-shadow: inset 0 0 10px rgba(189, 0, 255, 0.4), 0 0 15px rgba(189, 0, 255, 0.3);
        }

        .newsletter-form button {
            background: var(--border-gradient);
            color: var(--primary-bg);
            border: none;
            padding: 14px 30px;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.2rem;
            font-weight: 700;
            transition: all 0.3s ease;
            width: 100%;
            box-shadow: var(--shadow-neon);
        }

        .newsletter-form button:hover {
            opacity: 0.9;
            transform: translateY(-3px);
            box-shadow: 0 0 20px var(--neon-blue), 0 0 30px var(--neon-pink);
            color: var(--white);
        }

        /* Footer */
        footer {
            background-color: var(--primary-bg);
            color: var(--text-dark);
            text-align: center;
            padding: 2.5rem 0;
            font-size: 0.95rem;
            border-top: 1px solid rgba(0, 240, 255, 0.1);
        }
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 3.5rem;
            }
            .hero p {
                font-size: 1.2rem;
            }
            .section-title {
                font-size: 2.8rem;
            }
        }

        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                gap: 1rem;
            }
            .nav-links {
                margin-top: 1rem;
                justify-content: center;
            }
            .nav-links li {
                margin: 0 15px;
            }
            .logo {
                font-size: 1.8rem;
            }
            .hero {
                padding: 6rem 0 3rem;
                min-height: 80vh;
            }
            .hero h1 {
                font-size: 2.8rem;
            }
            .hero h1 .helia-text {
                font-size: 1.1em;
            }
            .hero p {
                font-size: 1.1rem;
                margin-bottom: 2rem;
            }
            .cta-button {
                padding: 1rem 2rem;
                font-size: 1.1rem;
            }
            .hero-visual {
                width: 90%;
                height: 250px;
                margin-top: 3rem;
            }
            .section-title {
                font-size: 2.2rem;
            }
            .section-subtitle {
                font-size: 1rem;
                margin-bottom: 3rem;
            }
            .features-grid {
                grid-template-columns: 1fr;
            }
            .join-us-buttons {
                flex-direction: column;
                gap: 15px;
            }
            .join-us-buttons a {
                width: 80%; /* Make buttons wider on small screens */
                justify-content: center;
            }
            .newsletter-form {
                padding: 30px;
                max-width: 90%;
            }
        }

        @media (max-width: 480px) {
            .nav-links li {
                margin: 0 8px;
            }
            .hero h1 {
                font-size: 2.2rem;
            }
            .hero p {
                font-size: 0.95rem;
            }
            .section-title {
                font-size: 1.8rem;
            }
            .feature-item h3 {
                font-size: 1.4rem;
            }
            .feature-item p {
                font-size: 0.9rem;
            }
            .newsletter-form button, .newsletter-form input[type="email"] {
                font-size: 1rem;
                padding: 10px;
            }
        }
    </style>


    <style>
    /* Responsive Design */
    @media (max-width: 992px) {
        .hero h1 {
            font-size: 3.5rem;
        }
        .hero p {
            font-size: 1.2rem;
        }
        .section-title {
            font-size: 2.8rem;
        }
    }

    @media (max-width: 768px) {
        .navbar {
            flex-direction: column;
            gap: 1rem;
        }
        .nav-links {
            margin-top: 1rem;
            justify-content: center;
        }
        .nav-links li {
            margin: 0 15px;
        }
        .logo {
            font-size: 1.8rem;
        }
        .hero {
            padding: 6rem 0 3rem;
            min-height: 80vh;
        }
        .hero h1 {
            font-size: 2.8rem;
        }
        .hero h1 .helia-text {
            font-size: 1.1em;
        }
        .hero p {
            font-size: 1.1rem;
            margin-bottom: 2rem;
        }
        .cta-button {
            padding: 1rem 2rem;
            font-size: 1.1rem;
        }
        .hero-visual {
            width: 90%;
            height: 250px;
            margin-top: 3rem;
        }
        .section-title {
            font-size: 2.2rem;
        }
        .section-subtitle {
            font-size: 1rem;
            margin-bottom: 3rem;
        }
        .features-grid {
            grid-template-columns: 1fr;
        }
        .join-us-buttons {
            flex-direction: column;
            gap: 15px;
        }
        .join-us-buttons a {
            width: 80%; /* Make buttons wider on small screens */
            justify-content: center;
        }
        .newsletter-form {
            padding: 30px;
            max-width: 90%;
        }
    }

    @media (max-width: 480px) {
        .nav-links li {
            margin: 0 8px;
        }
        .hero h1 {
            font-size: 2.2rem;
        }
        .hero p {
            font-size: 0.95rem;
        }
        .section-title {
            font-size: 1.8rem;
        }
        .feature-item h3 {
            font-size: 1.4rem;
        }
        .feature-item p {
            font-size: 0.9rem;
        }
        .newsletter-form button, .newsletter-form input[type="email"] {
            font-size: 1rem;
            padding: 10px;
        }
    }
</style>
</head>
<body>
<header>
    <div class="container navbar">
        <a href="#" class="logo">
            <span class="helia-text">زینب</span> موزیک
        </a>
        <nav>
            <ul class="nav-links">
                <li><a href="#hero">خانه</a></li>
                <li><a href="#features">دنیای زینب</a></li>
                <li><a href="#join-us">همین حالا بپیوندید</a></li>
                <li><a href="#">تماس با ما</a></li>
            </ul>
        </nav>
    </div>
</header>

<main>
    <section id="hero" class="hero">
        <div class="container hero-content">
            <h1 data-aos="fade-up" data-aos-duration="1200">
                <span class="helia-text">زینب</span>
                دنیایی از نغمه‌های بی‌پایان
            </h1>
            <p data-aos="fade-up" data-aos-delay="200" data-aos-duration="1200">
                در فروشگاه موسیقی <span class="helia-text">زینب</span>، هر نت داستانی دارد. خود را در دریایی از ملودی‌های تازه و هیجان‌انگیز غرق کنید و جهان موسیقی را دوباره کشف کنید.
            </p>
            <a href="#join-us" class="cta-button" data-aos="zoom-in" data-aos-delay="400" data-aos-duration="1200">
سفر موسیقایی خود را آغاز کنید
            </a>
            <div class="hero-visual" data-aos="fade-up" data-aos-delay="600" data-aos-duration="1500">
                <!-- Placeholder for a more abstract/visualizer image -->
            </div>
        </div>
    </section>

    <section id="features" class="features">
        <div class="container">
            <h2 class="section-title" data-aos="fade-down" data-aos-duration="1000">چرا <span class="helia-text">فروشگاه زینب</span> انتخاب اول شماست؟</h2>
            <p class="section-subtitle" data-aos="fade-down" data-aos-delay="100" data-aos-duration="1000">
                ما فراتر از یک فروشگاه، یک تجربه جامع موسیقی را برای شما به ارمغان می‌آوریم.
            </p>
            <div class="features-grid">
                <div class="feature-item" data-aos="fade-up" data-aos-delay="200">
                    <i class="fas fa-compact-disc"></i>
                    <h3>کالکشن بی‌نظیر</h3>
                    <p>دسترسی به آرشیوی عظیم از هزاران هنرمند و میلیون‌ها قطعه از هر سبک و ژانری که فکرش را بکنید.</p>
                </div>
                <div class="feature-item" data-aos="fade-up" data-aos-delay="300">
                    <i class="fas fa-waveform"></i> <!-- A more modern icon for sound -->
                    <h3>کیفیت فوق‌العاده</h3>
                    <p>موسیقی را با کیفیت Hi-Fi و Lossless تجربه کنید. هر نت را با وضوح و جزئیات کامل بشنوید.</p>
                </div>
                <div class="feature-item" data-aos="fade-up" data-aos-delay="400">
                    <i class="fas fa-sparkles"></i> <!-- A new icon for magic/discovery -->
                    <h3>کشف‌های هوشمند</h3>
                    <p>الگوریتم‌های پیشرفته <span class="helia-text">زینب</span>، موسیقی جدید را بر اساس سلیقه شما پیشنهاد می‌دهند.</p>
                </div>
                <div class="feature-item" data-aos="fade-up" data-aos-delay="500">
                    <i class="fas fa-rocket"></i>
                    <h3>سرعت و سادگی</h3>
                    <p>رابط کاربری روان و بهینه، دسترسی شما را به موسیقی مورد علاقه در کمترین زمان ممکن می‌کند.</p>
                </div>
                <div class="feature-item" data-aos="fade-up" data-aos-delay="600">
                    <i class="fas fa-heart"></i>
                    <h3>حمایت از هنرمند</h3>
                    <p>با هر خرید، مستقیم از هنرمندان مستقل و محبوب خود حمایت کنید و به رشد صنعت موسیقی کمک کنید.</p>
                </div>
                <div class="feature-item" data-aos="fade-up" data-aos-delay="700">
                    <i class="fas fa-calendar-star"></i> <!-- Calendar with a star for new releases -->
                    <h3>اولین شنونده باشید</h3>
                    <p>قبل از هرکس دیگر به جدیدترین آلبوم‌ها و تک‌آهنگ‌ها از هنرمندان برتر دسترسی پیدا کنید.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="join-us" class="join-us">
        <div class="container join-us-content">
            <h2 class="section-title" data-aos="fade-up" data-aos-duration="1000">
                به دنیای <span class="helia-text">زینب</span> قدم بگذارید!
            </h2>
            <p class="section-subtitle" data-aos="fade-up" data-aos-delay="100" data-aos-duration="1000">
                آماده‌اید تا تجربه موسیقی خود را متحول کنید؟ همین امروز به جمع بزرگ دوستداران موسیقی در <span class="helia-text">زینب</span> بپیوندید.
            </p>
            
            <div class="join-us-buttons" data-aos="fade-up" data-aos-delay="200" data-aos-duration="1200">
                <a href="#" target="_blank">
<i class="fas fa-headphones-alt"></i>
                    کشف پلی‌لیست‌ها
                </a>
                <a href="#" target="_blank">
                    <i class="fas fa-guitar"></i>
                    هنرمندان محبوب
                </a>
            </div>

            <div class="newsletter-form" data-aos="fade-up" data-aos-delay="300" data-aos-duration="1200">
                <p>برای دریافت جدیدترین اخبار، پیشنهادهای ویژه و کشف‌های موسیقی، ایمیل خود را وارد کنید:</p>
                <form action="#" method="post">
                    <label for="email">آدرس ایمیل شما:</label>
                    <input type="email" id="email" name="email" placeholder="example@email.com" required>
                    <button type="submit">عضویت در خبرنامه <span class="helia-text">زینب</span></button>
                </form>
            </div>
        </div>
    </section>
</main>

<footer>
    <div class="container">
        <p>&copy; 2023 فروشگاه موسیقی زینب. تمامی حقوق محفوظ است. این وب‌سایت با عشق توسط **سهیل** طراحی و توسعه داده شده است.</p>

        <br>

        <p></p>
    </div>
</footer>

<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
<script>
    AOS.init({
        duration: 1000,
        easing: 'ease-in-out',
        once: true,
        mirror: false,
    });

    // Smooth scrolling for navigation links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();

            const targetId = this.getAttribute('href');
            const targetElement = document.querySelector(targetId);

            if (targetElement) {
                window.scrollTo({
                    top: targetElement.offsetTop - (document.querySelector('header').offsetHeight + 20), // Adjust for sticky header + a little buffer
                    behavior: 'smooth'
                });
            }
        });
    });
</script>
</body>
</html>
