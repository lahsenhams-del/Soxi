# Soxi
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sakura Sushi - أفضل مطعم سوشي ياباني</title>
    <meta name="description" content="تجربة سوشي يابانية أصيلة في قلب المدينة">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700;800&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        :root {
            --primary: hsl(348, 83%, 47%);
            --primary-light: hsl(348, 83%, 60%);
            --gold: hsl(45, 93%, 47%);
            --dark: hsl(220, 20%, 10%);
            --dark-light: hsl(220, 15%, 15%);
            --cream: hsl(40, 30%, 96%);
        }
        body { font-family: 'Inter', sans-serif; background: var(--dark); color: var(--cream); }
        h1, h2, h3 { font-family: 'Playfair Display', serif; }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(to bottom, rgba(0,0,0,0.6), rgba(0,0,0,0.8)), 
                        url('https://images.unsplash.com/photo-1579871494447-9811cf80d66c?w=1920') center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
        }
        .hero-content { z-index: 10; padding: 2rem; }
        .hero h1 { font-size: 4rem; color: var(--cream); margin-bottom: 1rem; }
        .hero p { font-size: 1.5rem; color: var(--gold); margin-bottom: 2rem; }
        .btn { 
            padding: 1rem 2.5rem; 
            background: var(--primary); 
            color: white; 
            border: none; 
            font-size: 1.1rem; 
            cursor: pointer; 
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }
        .btn:hover { background: var(--primary-light); transform: scale(1.05); }
        .btn-outline { background: transparent; border: 2px solid var(--gold); color: var(--gold); margin-right: 1rem; }
        
        /* Section Styles */
        section { padding: 6rem 2rem; max-width: 1200px; margin: 0 auto; }
        .section-title { font-size: 3rem; text-align: center; margin-bottom: 1rem; }
        .section-subtitle { text-align: center; color: var(--gold); margin-bottom: 3rem; }
        
        /* About */
        .about { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center; }
        .about img { width: 100%; border-radius: 8px; }
        .about-text p { margin-bottom: 1.5rem; line-height: 1.8; opacity: 0.9; }
        
        /* Menu Grid */
        .menu-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 2rem; }
        .menu-card {
            background: var(--dark-light);
            border-radius: 12px;
            overflow: hidden;
            transition: transform 0.3s;
        }
        .menu-card:hover { transform: translateY(-10px); }
        .menu-card img { width: 100%; height: 200px; object-fit: cover; }
        .menu-card-content { padding: 1.5rem; }
        .menu-card h3 { color: var(--cream); margin-bottom: 0.5rem; }
        .menu-card p { opacity: 0.7; font-size: 0.9rem; margin-bottom: 1rem; }
        .price { color: var(--gold); font-size: 1.25rem; font-weight: bold; }
        
        /* Testimonials */
        .testimonials-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; }
        .testimonial {
            background: var(--dark-light);
            padding: 2rem;
            border-radius: 12px;
            border-right: 4px solid var(--primary);
        }
        .testimonial p { font-style: italic; margin-bottom: 1rem; line-height: 1.7; }
        .testimonial-author { color: var(--gold); }
        .stars { color: var(--gold); margin-bottom: 1rem; }
        
        /* Contact */
        .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; }
        .contact-info div { margin-bottom: 2rem; }
        .contact-info h3 { color: var(--gold); margin-bottom: 0.5rem; }
        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 1rem;
            margin-bottom: 1rem;
            background: var(--dark-light);
            border: 1px solid rgba(255,255,255,0.1);
            color: var(--cream);
            border-radius: 8px;
        }
        .contact-form textarea { height: 150px; resize: none; }
        
        /* Footer */
        footer {
            background: var(--dark-light);
            padding: 3rem 2rem;
            text-align: center;
        }
        .footer-links { margin: 2rem 0; }
        .footer-links a { color: var(--cream); margin: 0 1rem; text-decoration: none; opacity: 0.7; }
        .footer-links a:hover { opacity: 1; color: var(--gold); }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .about, .contact-grid { grid-template-columns: 1fr; }
            section { padding: 4rem 1rem; }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <p>مرحباً بكم في</p>
            <h1>ساكورا سوشي</h1>
            <p>تجربة يابانية أصيلة تأخذك في رحلة من النكهات الفريدة</p>
            <a href="#menu" class="btn btn-outline">استكشف القائمة</a>
            <a href="#contact" class="btn">احجز طاولتك</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2 class="section-title">قصتنا</h2>
        <p class="section-subtitle">تراث ياباني عريق منذ 1998</p>
        <div class="about">
            <img src="https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?w=600" alt="داخل المطعم">
            <div class="about-text">
                <h3 style="font-size: 2rem; margin-bottom: 1rem;">فن الطهي الياباني</h3>
                <p>نقدم لكم تجربة طعام استثنائية تجمع بين الأصالة اليابانية والإبداع العصري. يستخدم طهاتنا المتميزون أجود المكونات الطازجة المستوردة يومياً.</p>
                <p>كل طبق يُحضر بعناية فائقة وشغف حقيقي، ليقدم لكم لوحة فنية من النكهات المتناغمة التي تسعد الحواس.</p>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu">
        <h2 class="section-title">قائمتنا المميزة</h2>
        <p class="section-subtitle">أطباق مختارة بعناية</p>
        <div class="menu-grid">
            <div class="menu-card">
                <img src="https://images.unsplash.com/photo-1579584425555-c3ce17fd4351?w=400" alt="نيغيري">
                <div class="menu-card-content">
                    <h3>تشكيلة نيغيري</h3>
                    <p>8 قطع من أفخر أنواع السمك الطازج</p>
                    <span class="price">85 ر.س</span>
                </div>
            </div>
            <div class="menu-card">
                <img src="https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?w=400" alt="دراغون رول">
                <div class="menu-card-content">
                    <h3>دراغون رول</h3>
                    <p>روبيان تمبورا مع أفوكادو وصوص حار</p>
                    <span class="price">72 ر.س</span>
                </div>
            </div>
            <div class="menu-card">
                <img src="https://images.unsplash.com/photo-1553621042-f6e147245754?w=400" alt="كاليفورنيا رول">
                <div class="menu-card-content">
                    <h3>كاليفورنيا رول</h3>
                    <p>سلطعون وأفوكادو وخيار</p>
                    <span class="price">45 ر.س</span>
                </div>
            </div>
            <div class="menu-card">
                <img src="https://images.unsplash.com/photo-1611143669185-af224c5e3252?w=400" alt="ساشيمي">
                <div class="menu-card-content">
                    <h3>طبق ساشيمي</h3>
                    <p>تشكيلة فاخرة من السمك النيء</p>
                    <span class="price">120 ر.س</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials">
        <h2 class="section-title">آراء عملائنا</h2>
        <p class="section-subtitle">ماذا يقولون عنا</p>
        <div class="testimonials-grid">
            <div class="testimonial">
                <div class="stars">★★★★★</div>
                <p>"أفضل سوشي تذوقته على الإطلاق! الجودة والطعم لا يُضاهى. سأعود بالتأكيد."</p>
                <span class="testimonial-author">-
                
