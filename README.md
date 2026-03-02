# Zen-Botanica-
leading pages: Zen Botanica



<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zen Botanica · Природная гармония</title>
    <!-- Font Awesome 6 (бесплатный) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts: мягкий Poppins & элегантный Playfair Display -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* ========== СБРОС И ПЕРЕМЕННЫЕ ========== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --deep-forest: #1B4D3E;       /* глубокий зелёный, премиум */
            --soft-mint: #D1F0E2;          /* нежная мята */
            --warm-sand: #FAF3E0;           /* песочный, уют */
            --golden-nectar: #F4B942;       /* тёплый акцент (мёд/куркума) */
            --slate: #2E3B3B;                /* тёмный для текста */
            --cloud: #F9FBFD;                /* почти белый */
            --shadow-sm: 0 15px 30px -12px rgba(0, 20, 10, 0.15);
            --shadow-hover: 0 30px 40px -15px rgba(27, 77, 62, 0.25);
            --border-radius-card: 2rem 1rem 2rem 1rem;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: var(--slate);
            background-color: var(--cloud);
            line-height: 1.5;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 600;
            letter-spacing: -0.02em;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* ========== ДЕКОРАТИВНЫЕ ЭЛЕМЕНТЫ ========== */
        .leaf-bg {
            position: relative;
            overflow: hidden;
        }
        .leaf-bg::before {
            content: "";
            position: absolute;
            inset: 0;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" opacity="0.03"><path fill="%231B4D3E" d="M61.7,29.5c-2.8-3.5-6.9-5.8-11.6-5.8c-8.2,0-14.9,6.7-14.9,14.9c0,2.5,0.6,4.8,1.7,6.9c-2.9,2.5-4.7,6.1-4.7,10.1c0,7.5,6.1,13.6,13.6,13.6c7.5,0,13.6-6.1,13.6-13.6c0-2.2-0.5-4.3-1.5-6.1c2.6-2.1,4.3-5.3,4.3-8.9C65.8,36,64.2,32.1,61.7,29.5z M50.1,53.2c-2.7,0-5-2.2-5-5c0-2.7,2.2-5,5-5c2.7,0,5,2.2,5,5C55.1,51,52.9,53.2,50.1,53.2z"/></svg>') repeat;
            pointer-events: none;
        }

        /* ========== HEADER ========== */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 2rem;
            background-color: rgba(255, 255, 255, 0.75);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid rgba(27, 77, 62, 0.1);
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.9rem;
            font-weight: 700;
            color: var(--deep-forest);
            line-height: 1;
        }
        .logo span {
            font-size: 1rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 300;
            display: block;
            letter-spacing: 2px;
            color: var(--golden-nectar);
            margin-top: -5px;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            font-weight: 500;
        }
        .nav-links a {
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
            background: var(--golden-nectar);
            transition: width 0.3s ease;
        }
        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-cta {
            background-color: var(--deep-forest);
            color: white;
            padding: 0.7rem 1.8rem;
            border-radius: 40px;
            font-weight: 500;
            transition: all 0.2s;
            border: 1px solid transparent;
        }
        .nav-cta:hover {
            background-color: transparent;
            color: var(--deep-forest);
            border-color: var(--deep-forest);
        }

        /* ========== HERO ========== */
        .hero {
            display: grid;
            grid-template-columns: 1fr 1fr;
            align-items: center;
            gap: 3rem;
            padding: 3rem 2rem 5rem;
            max-width: 1400px;
            margin: 0 auto;
            position: relative;
        }

        .hero-content h1 {
            font-size: clamp(2.8rem, 6vw, 4.5rem);
            line-height: 1.1;
            color: var(--deep-forest);
            margin-bottom: 1.2rem;
        }
        .hero-content h1 i {
            font-style: italic;
            color: var(--golden-nectar);
            font-weight: 500;
        }

        .hero-content p {
            font-size: 1.2rem;
            color: #3f5a55;
            margin-bottom: 2rem;
            max-width: 500px;
            border-left: 4px solid var(--golden-nectar);
            padding-left: 1.5rem;
        }

        .hero-btns {
            display: flex;
            gap: 1.5rem;
            flex-wrap: wrap;
        }
        .btn-primary {
            background-color: var(--deep-forest);
            color: white;
            padding: 1rem 2.8rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            box-shadow: var(--shadow-sm);
            transition: all 0.2s;
            border: 1px solid var(--deep-forest);
        }
        .btn-primary:hover {
            background-color: transparent;
            color: var(--deep-forest);
            transform: translateY(-3px);
            box-shadow: var(--shadow-hover);
        }
        .btn-outline {
            border: 1px solid var(--deep-forest);
            background: transparent;
            color: var(--deep-forest);
            padding: 1rem 2.5rem;
            border-radius: 50px;
            font-weight: 600;
            transition: 0.2s;
        }
        .btn-outline:hover {
            background-color: var(--deep-forest);
            color: white;
            transform: translateY(-3px);
        }

        .hero-visual {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .floating-card {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(8px);
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            width: 380px;
            height: 380px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: var(--shadow-hover);
            border: 2px solid white;
            animation: float 6s ease-in-out infinite;
        }
        .floating-card i {
            font-size: 8rem;
            color: var(--golden-nectar);
            filter: drop-shadow(0 8px 12px rgba(0,0,0,0.1));
        }
        .floating-card .product-badge {
            background: var(--deep-forest);
            color: white;
            padding: 0.5rem 1.5rem;
            border-radius: 50px;
            margin-top: 1rem;
            font-weight: 600;
            letter-spacing: 1px;
        }
        @keyframes float {
            0% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(2deg); }
            100% { transform: translateY(0px) rotate(0deg); }
        }

        /* ========== БРЕНД-СТАТИСТИКА ========== */
        .stats {
            display: flex;
            justify-content: space-around;
            background: var(--soft-mint);
            padding: 2.5rem 1rem;
            border-radius: 100px 20px 100px 20px;
            margin: 2rem auto 4rem;
            max-width: 1000px;
            box-shadow: var(--shadow-sm);
        }
        .stat-item {
            text-align: center;
        }
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--deep-forest);
            font-family: 'Playfair Display', serif;
        }
        .stat-label {
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 0.9rem;
        }

        /* ========== ПРЕИМУЩЕСТВА (НЕОБЫЧНАЯ СЕТКА) ========== */
        .benefits {
            padding: 5rem 2rem;
            background-color: white;
            position: relative;
        }
        .benefits h2 {
            text-align: center;
            font-size: 2.8rem;
            color: var(--deep-forest);
            margin-bottom: 3rem;
        }
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        .benefit-card {
            background: var(--warm-sand);
            padding: 2.5rem 1.5rem;
            border-radius: 3rem 1rem 3rem 1rem;
            text-align: center;
            transition: 0.3s;
            border: 1px solid transparent;
        }
        .benefit-card:hover {
            transform: scale(1.02) translateY(-8px);
            border-color: var(--golden-nectar);
            box-shadow: var(--shadow-hover);
        }
        .benefit-icon {
            font-size: 3.5rem;
            color: var(--deep-forest);
            margin-bottom: 1.5rem;
        }
        .benefit-card h3 {
            font-size: 1.6rem;
            margin-bottom: 0.8rem;
        }

        /* ========== ПРОДУКТЫ ========== */
        .products {
            padding: 5rem 2rem;
            background: linear-gradient(145deg, var(--cloud) 30%, var(--soft-mint) 100%);
        }
        .products h2 {
            font-size: 2.8rem;
            text-align: center;
            color: var(--deep-forest);
        }
        .products-sub {
            text-align: center;
            max-width: 600px;
            margin: 0.5rem auto 3rem;
            opacity: 0.8;
        }
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 2.5rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        .product-card {
            background: white;
            border-radius: var(--border-radius-card);
            padding: 2rem 1.5rem 1.5rem;
            box-shadow: var(--shadow-sm);
            transition: 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            position: relative;
            border: 1px solid rgba(27, 77, 62, 0.1);
            display: flex;
            flex-direction: column;
        }
        .product-card:hover {
            transform: rotate(1deg) scale(1.02);
            box-shadow: var(--shadow-hover);
            border-color: var(--golden-nectar);
        }
        .product-badge {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background: var(--golden-nectar);
            color: var(--deep-forest);
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-weight: 600;
            font-size: 0.8rem;
        }
        .product-img {
            font-size: 5rem;
            color: var(--deep-forest);
            margin-bottom: 1.2rem;
            text-align: center;
            background: var(--soft-mint);
            width: fit-content;
            padding: 1rem 1.8rem;
            border-radius: 40% 60% 40% 60%;
            margin-left: auto;
            margin-right: auto;
        }
        .product-card h3 {
            font-size: 1.8rem;
            color: var(--deep-forest);
        }
        .product-desc {
            margin: 0.5rem 0 1rem;
            font-size: 0.95rem;
        }
        .product-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: auto;
        }
        .price {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--golden-nectar);
        }
        .btn-add {
            background: var(--deep-forest);
            color: white;
            border: none;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            font-size: 1.5rem;
            cursor: pointer;
            transition: 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .btn-add:hover {
            background: var(--golden-nectar);
            color: var(--deep-forest);
            transform: rotate(90deg);
        }

        /* ========== НАУЧНЫЙ ПОДХОД ========== */
        .science {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
            align-items: center;
        }
        .science-text h2 {
            font-size: 2.8rem;
            color: var(--deep-forest);
        }
        .science-text p {
            font-size: 1.2rem;
            margin: 1.5rem 0;
        }
        .science-highlight {
            background: var(--soft-mint);
            padding: 2rem;
            border-radius: 2rem 0 2rem 0;
            font-weight: 500;
        }
        .science-visual {
            background: var(--deep-forest);
            border-radius: 3rem 1rem 3rem 1rem;
            padding: 3rem 2rem;
            color: white;
            box-shadow: 20px 20px 0 var(--golden-nectar);
            transition: 0.3s;
        }
        .science-visual:hover {
            transform: translate(-5px, -5px);
            box-shadow: 25px 25px 0 var(--golden-nectar);
        }
        .science-visual i {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        /* ========== ОТЗЫВЫ ========== */
        .testimonials {
            background: var(--deep-forest);
            color: white;
            padding: 5rem 2rem;
            clip-path: polygon(0 5%, 100% 0%, 100% 95%, 0% 100%);
        }
        .testimonials h2 {
            text-align: center;
            font-size: 2.8rem;
            color: var(--soft-mint);
        }
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 1100px;
            margin: 3rem auto 0;
        }
        .testimonial-card {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(4px);
            padding: 2rem;
            border-radius: 3rem 0.5rem 3rem 0.5rem;
            border: 1px solid rgba(255,255,255,0.2);
        }
        .testimonial-card i {
            color: var(--golden-nectar);
            font-size: 2rem;
            margin-bottom: 1rem;
        }
        .client {
            margin-top: 1.5rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }
        .client span {
            background: var(--golden-nectar);
            color: var(--deep-forest);
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* ========== ПРИЗЫВ (CTA) ========== */
        .cta-banner {
            background: linear-gradient(120deg, var(--soft-mint), var(--warm-sand));
            margin: 4rem auto;
            padding: 4rem 2rem;
            border-radius: 5rem 1rem 5rem 1rem;
            max-width: 1100px;
            text-align: center;
            box-shadow: var(--shadow-hover);
        }
        .cta-banner h2 {
            font-size: 3rem;
            color: var(--deep-forest);
        }
        .cta-banner .btn-primary {
            margin-top: 2rem;
            display: inline-block;
            font-size: 1.3rem;
            padding: 1.2rem 3.5rem;
        }

        /* ========== FOOTER ========== */
        footer {
            background: var(--slate);
            color: var(--cloud);
            padding: 3rem 2rem 1.5rem;
        }
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        .footer-logo {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            color: var(--soft-mint);
        }
        .footer-links a {
            display: block;
            margin: 0.8rem 0;
            opacity: 0.8;
            transition: 0.2s;
        }
        .footer-links a:hover {
            opacity: 1;
            color: var(--golden-nectar);
            transform: translateX(5px);
        }
        .socials {
            display: flex;
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        .socials a {
            background: var(--deep-forest);
            color: white;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: 0.2s;
        }
        .socials a:hover {
            background: var(--golden-nectar);
            color: var(--deep-forest);
            transform: scale(1.1) rotate(5deg);
        }
        .copyright {
            text-align: center;
            margin-top: 3rem;
            opacity: 0.6;
            font-size: 0.9rem;
        }

        /* ========== АДАПТАЦИЯ ========== */
        @media (max-width: 800px) {
            .hero, .science {
                grid-template-columns: 1fr;
                text-align: center;
            }
            .hero-content p {
                margin-left: auto;
                margin-right: auto;
            }
            .navbar {
                flex-direction: column;
                gap: 1rem;
            }
            .nav-links {
                flex-wrap: wrap;
                justify-content: center;
                gap: 1.2rem;
            }
            .stats {
                flex-direction: column;
                gap: 1.5rem;
                border-radius: 3rem;
            }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <div class="logo">Zen Botanica<span>nature·science·balance</span></div>
        <div class="nav-links">
            <a href="#home">Acasă</a>
            <a href="#products">Produse</a>
            <a href="#science">Științe</a>
            <a href="#reviews">Comandă</a>
        </div>
        <a href="#" class="nav-cta"><i class="fas fa-leaf" style="margin-right: 8px;"></i>Заказать</a>
    </nav>

    <main>
        <!-- HERO -->
        <section class="hero leaf-bg" id="home">
            <div class="hero-content">
                <h1>Respiră liber <br>cu <i>ZEN</i> Botanica</h1>
                <p> Suplimente create la granița dintre cunoștințele străvechi și cercetările clinice moderne.</p>
                <div class="hero-btns">
                    <a href="#" class="btn-primary"> Alege un produs</a>
                    <a href="#" class="btn-outline"> Consultanță</a>
                </div>
            </div>
            <div class="hero-visual">
                <div class="floating-card">
                    <i class="fas fa-seedling"></i>
                    <div class="product-badge">NEW</div>
                    <div style="font-size: 1.8rem; font-weight: 600; color: var(--deep-forest);">Immuno Zen</div>
                    <div style="font-size: 0.9rem;">c ашвагандой</div>
                </div>
            </div>
        </section>

        <!-- СТАТИСТИКА ДОВЕРИЯ -->
        <div class="stats container">
            <div class="stat-item">
                <div class="stat-number">15+</div>
                <div class="stat-label">лет исследований</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">50k+</div>
                <div class="stat-label">довольных клиентов</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">100%</div>
                <div class="stat-label">натуральный состав</div>
            </div>
        </div>

        <!-- ПРЕИМУЩЕСТВА (НЕОБЫЧНЫЕ КАРТОЧКИ) -->
        <section class="benefits">
            <h2>De ce Zen Botanica?</h2>
            <div class="benefits-grid">
                <div class="benefit-card">
                    <div class="benefit-icon"><i class="fas fa-flask"></i></div>
                    <h3> Dovedit clinic </h3>
                    <p>6 Studiile placebo dublu-orb confirmă eficacitatea</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon"><i class="fas fa-recycle"></i></div>
                    <h3> Eco‑prietenos</h3>
                    <p>Ambalaje biodegradabile și recoltare etică a plantelor medicinale</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon"><i class="fas fa-brain"></i></div>
                    <h3>Adaptogeni</h3>
                   
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon"><i class="fas fa-heartbeat"></i></div>
                    <h3>Fără efecte secundare</h3>
                    <p>Acțiune blândă, fără dependență sau somnolență</p>
                </div>
            </div>
        </section>

        <!-- ПРОДУКТЫ -->
        <section class="products" id="products">
           <div class="product-grid">
    <div class="product-card">
        <span class="product-badge">Nou</span>
        <div class="product-img"><i class="fas fa-capsules"></i></div>
        <h3>Immuno Zen</h3>
        <p class="product-desc">Echinaceea, soc, zinc – protecție triplă pentru imunitate.</p>
        <div class="product-footer">
           
            <button class="btn-add" aria-label="Adaugă"><i class="fas fa-plus"></i></button>
        </div>
    </div>
</div> 

        </section>

        <!-- НАУЧНЫЙ ПОДХОД -->
        <section class="science" id="science">
            <div class="science-text">
                <h2>Научный подход к природе</h2>
                <p>Каждая партия Zen Botanica проходит тройной контроль: фитохимический, микробиологический и клинический.</p>
                <div class="science-highlight">
                    <i class="fas fa-dna" style="color: var(--deep-forest); margin-right: 10px;"></i>
                    Запатентованная технология экстракции сохраняет в 3 раза больше активных веществ.
                </div>
            </div>
            <div class="science-visual">
                <i class="fas fa-microscope"></i>
                <h3 style="color: var(--golden-nectar);">Лаборатория ZB</h3>
                <p>Мы не просто смешиваем травы — мы исследуем синергию. Более 2000 комбинаций протестировано.</p>
            </div>
        </section>

        <!-- ОТЗЫВЫ -->
        <section class="testimonials" id="reviews">
            <h2>Голоса доверия</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <i class="fas fa-quote-right"></i>
                    <p>После курса Immuno Zen забыла про сезонные простуды. Состав чистый, без химии. Рекомендую!</p>
                    <div class="client"><span>ЕК</span> Елена, 42 года</div>
                </div>
                <div class="testimonial-card">
                    <i class="fas fa-quote-right"></i>
                    <p>Calm Zen — спасение при бессоннице. Засыпаю за 15 минут и просыпаюсь отдохнувшей.</p>
                    <div class="client"><span>МР</span> Мария, 37 лет</div>
                </div>
                <div class="testimonial-card">
                    <i class="fas fa-quote-right"></i>
                    <p>Digest Zen помог наладить пищеварение после антибиотиков. Вкусный, мятный.</p>
                    <div class="client"><span>АК</span> Алексей, 29 лет</div>
                </div>
            </div>
        </section>

        <!-- БАННЕР ПРИЗЫВА -->
        <div class="cta-banner">
            <h2>Начни свой путь к балансу</h2>
            <p style="font-size: 1.2rem;">Первый заказ — скидка 15% + бесплатная доставка</p>
            <a href="#" class="btn-primary"><i class="fas fa-arrow-right"></i> Выбрать набор</a>
        </div>
    </main>

    <!-- FOOTER -->
    <footer>
        <div class="footer-grid">
            <div>
                <div class="footer-logo">Zen Botanica</div>
                <p style="margin-top: 1rem; opacity: 0.7;">Фитотерапия, прошедшая испытание временем и наукой.</p>
                <div class="socials">
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-telegram"></i></a>
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                </div>
            </div>
            <div class="footer-links">
                <h4>Каталог</h4>
                <a href="#">Иммунитет</a>
                <a href="#">Сон и стресс</a>
                <a href="#">Пищеварение</a>
                <a href="#">Энергия</a>
            </div>
            <div class="footer-links">
                <h4>Покупателям</h4>
                <a href="#">Доставка и оплата</a>
                <a href="#">Сертификаты</a>
                <a href="#">Блог</a>
                <a href="#">Контакты</a>
            </div>
            <div class="footer-links">
                <h4>Связаться</h4>
                <a href="mailto:info@zenbotanica.com">info@zenbotanica.com</a>
                <a href="tel:+18005551234">+1 (800) 555-1234</a>
                <p style="margin-top: 1rem;">📍 Ботаническая лаборатория, Вермонт</p>
            </div>
        </div>
        <div class="copyright">
            © 2025 Zen Botanica. Природа внутри тебя.
        </div>
    </footer>
</body>
</html>

