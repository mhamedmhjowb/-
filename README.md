<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>محمد محجوب إسماعيل | طالب علوم رياضية وحاسوب</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2ecc71;
            --dark-color: #2c3e50;
            --light-color: #ecf0f1;
            --text-color: #333;
            --text-light: #7f8c8d;
            --transition: all 0.3s ease;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --border-radius: 8px;
            --header-height: 80px;
        }

        .dark-mode {
            --primary-color: #1abc9c;
            --secondary-color: #9b59b6;
            --dark-color: #ecf0f1;
            --light-color: #2c3e50;
            --text-color: #ecf0f1;
            --text-light: #bdc3c7;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.4);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--light-color);
            color: var(--text-color);
            transition: var(--transition);
            line-height: 1.6;
            background-image: linear-gradient(120deg, #fdfbfb 0%, #ebedee 100%);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        header {
            background-color: var(--dark-color);
            color: white;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
            height: var(--header-height);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            display: flex;
            align-items: center;
        }

        .logo i {
            margin-left: 10px;
            color: var(--primary-color);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin: 0 10px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            padding: 10px 15px;
            border-radius: var(--border-radius);
            transition: var(--transition);
        }

        .nav-links a:hover, 
        .nav-links a.active {
            background-color: var(--primary-color);
        }

        .theme-toggle {
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            transition: var(--transition);
            margin-right: 15px;
        }

        .theme-toggle:hover {
            transform: rotate(30deg);
        }

        .page {
            min-height: 100vh;
            padding-top: calc(var(--header-height) + 40px);
            padding-bottom: 40px;
            display: none;
        }

        .page.active {
            display: block;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary-color);
            border-radius: 2px;
        }

        #home {
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(135deg, rgba(255,255,255,0.8) 50%, rgba(0,0,0,0.03) 50%);
        }

        .hero-content {
            max-width: 800px;
        }

        .hero-content h1 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            color: var(--dark-color);
        }

        .hero-content .greeting {
            font-size: 2rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            color: var(--text-light);
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-image {
            width: 280px;
            height: 280px;
            border-radius: 50%;
            margin: 0 auto 30px;
            overflow: hidden;
            position: relative;
            box-shadow: var(--shadow);
            border: 5px solid var(--primary-color);
            background-color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .hero-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--primary-color);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: 600;
            transition: var(--transition);
            border: 2px solid var(--primary-color);
            margin: 0 10px;
        }

        .btn:hover {
            background-color: transparent;
            color: var(--primary-color);
            transform: translateY(-5px);
        }

        .btn-outline {
            background-color: transparent;
            color: var(--primary-color);
        }

        .btn-outline:hover {
            background-color: var(--primary-color);
            color: white;
        }

        .cv-container {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 30px;
        }

        .cv-sidebar {
            background-color: var(--dark-color);
            color: white;
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }

        .cv-main {
            background-color: white;
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            color: var(--text-color);
        }

        .cv-section {
            margin-bottom: 30px;
        }

        .cv-section h3 {
            color: var(--primary-color);
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--light-color);
        }

        .cv-item {
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px dashed #eee;
        }

        .cv-item:last-child {
            border-bottom: none;
        }

        .cv-item h4 {
            color: var(--dark-color);
        }

        .cv-item .date {
            color: var(--text-light);
            font-size: 0.9rem;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-tag {
            background-color: var(--primary-color);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            margin-bottom: 5px;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            background-color: white;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            display: flex;
            flex-direction: column;
            height: 100%;
        }

        .portfolio-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
        }

        .portfolio-img {
            height: 200px;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: #f8f9fa;
        }

        .portfolio-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .portfolio-item:hover .portfolio-img img {
            transform: scale(1.05);
        }

        .portfolio-content {
            padding: 20px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .portfolio-content h3 {
            margin-bottom: 10px;
            color: var(--dark-color);
        }

        .portfolio-content p {
            color: var(--text-light);
            margin-bottom: 15px;
            flex-grow: 1;
        }

        .portfolio-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .portfolio-tag {
            background-color: var(--light-color);
            color: var(--text-color);
            padding: 3px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }

        .contact-form {
            background-color: white;
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--dark-color);
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #ddd;
            border-radius: var(--border-radius);
            font-family: inherit;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-control:focus {
            border-color: var(--primary-color);
            outline: none;
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        .form-error {
            color: #e74c3c;
            font-size: 0.9rem;
            margin-top: 5px;
            display: none;
        }

        .contact-info {
            background-color: var(--dark-color);
            color: white;
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }

        .contact-info h3 {
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
        }

        .contact-item i {
            font-size: 1.2rem;
            color: var(--secondary-color);
            margin-left: 15px;
            margin-top: 5px;
            min-width: 25px;
        }

        .contact-comments {
            margin-top: 40px;
            grid-column: 1 / -1;
        }

        .comment {
            background-color: white;
            padding: 20px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            margin-bottom: 20px;
        }

        .comment-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            border-bottom: 1px solid #eee;
            padding-bottom: 10px;
        }

        .comment-name {
            font-weight: 600;
            color: var(--dark-color);
        }

        .comment-type {
            background-color: var(--primary-color);
            color: white;
            padding: 3px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        .comment-email {
            color: var(--text-light);
            font-size: 0.9rem;
            margin-bottom: 10px;
        }

        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 30px 0;
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }

        .social-links a {
            display: inline-block;
            width: 50px;
            height: 50px;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            transition: var(--transition);
        }

        .social-links a:hover {
            background-color: var(--primary-color);
            transform: translateY(-5px);
        }

        .background-options {
            position: fixed;
            bottom: 20px;
            left: 20px;
            display: flex;
            gap: 10px;
            z-index: 100;
        }

        .bg-option {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .bg-option:hover {
            transform: scale(1.1);
        }

        .cursor-effect {
            position: fixed;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background-color: rgba(52, 152, 219, 0.5);
            pointer-events: none;
            transform: translate(-50%, -50%);
            z-index: 9999;
            mix-blend-mode: difference;
        }

        .about-me {
            background-color: white;
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            margin-bottom: 30px;
            line-height: 1.8;
        }

        @media (max-width: 992px) {
            .cv-container, .contact-container {
                grid-template-columns: 1fr;
            }
            
            .hero-content h1 {
                font-size: 2.2rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
        }

        @media (max-width: 768px) {
            .portfolio-grid {
                grid-template-columns: 1fr;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .hero-image {
                width: 220px;
                height: 220px;
            }
            
            .hero-btns {
                display: flex;
                flex-direction: column;
                gap: 15px;
            }
            
            .hero-btns .btn {
                margin: 5px 0;
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="cursor-effect" id="cursor"></div>
    
    <div class="background-options">
        <div class="bg-option" style="background-color: #ecf0f1;" data-bg="color"></div>
        <div class="bg-option" style="background-color: #d5f5e3;" data-bg="color2"></div>
        <div class="bg-option" style="background: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);" data-bg="gradient"></div>
    </div>
    
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <i class="fas fa-user"></i>
                    <span>محمد محجوب إسماعيل</span>
                </div>
                <ul class="nav-links">
                    <li><a href="#" class="nav-link active" data-page="home">الرئيسية</a></li>
                    <li><a href="#" class="nav-link" data-page="cv">السيرة الذاتية</a></li>
                    <li><a href="#" class="nav-link" data-page="portfolio">أعمالي</a></li>
                    <li><a href="#" class="nav-link" data-page="contact">اتصل بنا</a></li>
                </ul>
                <button class="theme-toggle" id="themeToggle">
                    <i class="fas fa-moon"></i>
                </button>
            </nav>
        </div>
    </header>
    
    <main>
        <section id="home" class="page active">
            <div class="container">
                <div class="hero-content">
                    <div class="hero-image">
                        <img src="a.jpg" alt="صورة محمد محجوب إسماعيل">
                    </div>
                    <div class="greeting" id="greeting">مرحباً!</div>
                    <h1>أنا <span class="highlight">محمد محجوب إسماعيل</span></h1>
                    <p>طالب جامعي بكلية العلوم الرياضية والحاسوب بجامعة الجزيرة، أسعى لتطوير نفسي باستمرار وتعلم كل ما يمكن تعلمه في مجال الرياضيات والحوسبة.</p>
                    <div class="hero-btns">
                        <a href="#" class="btn" data-page="portfolio">مشاريعي</a>
                        <a href="#" class="btn btn-outline" data-page="contact">تواصل معي</a>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="cv" class="page">
            <div class="container">
                <div class="section-title">
                    <h2>السيرة الذاتية</h2>
                    <p>تعرف على مهاراتي وخبراتي</p>
                </div>
                
                <div class="cv-container">
                    <div class="cv-sidebar">
                        <div class="cv-section">
                            <h3>معلومات شخصية</h3>
                            <div class="cv-item">
                                <p><strong>الاسم:</strong> محمد محجوب إسماعيل</p>
                                <p><strong>العمر:</strong> 25 سنة</p>
                                <p><strong>البلد:</strong> السودان</p>
                                <p><strong>اللغات:</strong> العربية (متقن)، الإنجليزية (متوسط)</p>
                            </div>
                        </div>
                        
                        <div class="cv-section">
                            <h3>المهارات</h3>
                            <div class="skills">
                                <span class="skill-tag">HTML/CSS</span>
                                <span class="skill-tag">MySQL</span>
                                <span class="skill-tag">التحليل الإحصائي</span>
                                <span class="skill-tag">الرياضيات التطبيقية</span>
                                <span class="skill-tag">تحليل البيانات</span>
                                <span class="skill-tag">حل المشكلات</span>
                                <span class="skill-tag">البحث العلمي</span>
                            </div>
                        </div>
                        
                        <div class="cv-section">
                            <h3>التواصل</h3>
                            <div class="cv-item">
                                <p><i class="fas fa-envelope"></i> mhjwmhmd.com</p>
                                <p><i class="fas fa-phone"></i> 0964916347</p>
                                <p><i class="fas fa-map-marker-alt"></i> السودان</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="cv-main">
                        <div class="about-me">
                            <h3>نبذة عني</h3>
                            <p>أنا طالب جامعي في كلية العلوم الرياضية والحاسوب بجامعة الجزيرة، أسعى دائماً لتطوير نفسي ومهاراتي في مجالات الرياضيات التطبيقية وعلوم الحاسوب. أحب التعلم المستمر وأبحث دائماً عن فرص جديدة للتطور المهني والشخصي.</p>
                        </div>
                        
                        <div class="cv-section">
                            <h3>التعليم</h3>
                            <div class="cv-item">
                                <h4>بكالوريوس العلوم الرياضية والحاسوب</h4>
                                <p>جامعة الجزيرة، السودان</p>
                                <p>طالب في السنة النهائية، متخصص في الرياضيات التطبيقية وعلوم الحاسوب.</p>
                            </div>
                        </div>
                        
                        <div class="cv-section">
                            <h3>المشاريع الأكاديمية</h3>
                            <div class="cv-item">
                                <h4>نظام مراقبة المحال التجارية</h4>
                                <p>تطوير نظام متكامل لمراقبة وإدارة المحال التجارية مع واجهة مستخدم سهلة الاستخدام وقاعدة بيانات فعالة.</p>
                            </div>
                            
                            <div class="cv-item">
                                <h4>تطوير عمل بنك البركة</h4>
                                <p>مشروع يهدف إلى تحسين وتطوير العمليات المصرفية باستخدام حلول تقنية مبتكرة.</p>
                            </div>
                            
                            <div class="cv-item">
                                <h4>تحليل إحصائي للبطالة في السودان</h4>
                                <p>دراسة إحصائية شاملة لمشكلة البطالة في السودان، مع تحليل الأسباب واقتراح حلول.</p>
                            </div>
                        </div>
                        
                        <div class="cv-section">
                            <h3>الأهداف المهنية</h3>
                            <div class="cv-item">
                                <p>تطوير مهاراتي في مجال علوم البيانات والتحليل الإحصائي</p>
                                <p>اكتساب خبرة عملية في مجال تطوير البرمجيات</p>
                                <p>المساهمة في حل المشكلات المجتمعية من خلال التكنولوجيا</p>
                                <p>مواصلة التعليم العالي في مجال الرياضيات التطبيقية</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="portfolio" class="page">
            <div class="container">
                <div class="section-title">
                    <h2>أعمالي ومشاريعي</h2>
                    <p>أهم المشاريع التي قمت بتنفيذها</p>
                </div>
                
                <div class="portfolio-grid">
                    <div class="portfolio-item">
                        <div class="portfolio-img">
                            <img src="project1.jpg" alt="نظام مراقبة المحال التجارية">
                        </div>
                        <div class="portfolio-content">
                            <h3>نظام مراقبة المحال التجارية</h3>
                            <p>نظام متكامل لإدارة ومراقبة المحال التجارية يتضمن إدارة المخزون والمبيعات والموظفين.</p>
                            <div class="portfolio-tags">
                                <span class="portfolio-tag">HTML/CSS</span>
                                <span class="portfolio-tag">MySQL</span>
                                <span class="portfolio-tag">نظم الإدارة</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="portfolio-item">
                        <div class="portfolio-img">
                            <img src="project2.jpg" alt="تطوير عمل بنك البركة">
                        </div>
                        <div class="portfolio-content">
                            <h3>تطوير عمل بنك البركة</h3>
                            <p>مشروع يهدف إلى تحسين العمليات المصرفية وتطوير أنظمة العمل في بنك البركة باستخدام حلول تقنية متقدمة.</p>
                            <div class="portfolio-tags">
                                <span class="portfolio-tag">تحليل النظم</span>
                                <span class="portfolio-tag">تطوير العمليات</span>
                                <span class="portfolio-tag">حلول مصرفية</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="portfolio-item">
                        <div class="portfolio-img">
                            <img src="project3.jpg" alt="تحليل إحصائي للبطالة">
                        </div>
                        <div class="portfolio-content">
                            <h3>تحليل إحصائي للبطالة في السودان</h3>
                            <p>دراسة إحصائية شاملة لمشكلة البطالة في السودان تشمل تحليل البيانات، تحديد الأسباب، واقتراح حلول عملية.</p>
                            <div class="portfolio-tags">
                                <span class="portfolio-tag">التحليل الإحصائي</span>
                                <span class="portfolio-tag">علوم البيانات</span>
                                <span class="portfolio-tag">البحث العلمي</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="contact" class="page">
            <div class="container">
                <div class="section-title">
                    <h2>اتصل بنا</h2>
                    <p>نحن هنا للإجابة على استفساراتك</p>
                </div>
                
                <div class="contact-container">
                    <div class="contact-form">
                        <form id="contactForm">
                            <div class="form-group">
                                <label for="name">الاسم الكامل</label>
                                <input type="text" id="name" class="form-control" required>
                                <div class="form-error" id="nameError">يرجى إدخال اسم صحيح</div>
                            </div>
                            
                            <div class="form-group">
                                <label for="email">البريد الإلكتروني</label>
                                <input type="email" id="email" class="form-control" required>
                                <div class="form-error" id="emailError">يرجى إدخال بريد إلكتروني صحيح</div>
                            </div>
                            
                            <div class="form-group">
                                <label for="inquiry">نوع الاستفسار</label>
                                <select id="inquiry" class="form-control" required>
                                    <option value="" disabled selected>اختر نوع الاستفسار</option>
                                    <option value="تعليق">تعليق</option>
                                    <option value="مقترح">مقترح</option>
                                    <option value="شكوى">شكوى</option>
                                    <option value="استفسار">استفسار</option>
                                    <option value="أخرى">أخرى</option>
                                </select>
                                <div class="form-error" id="inquiryError">يرجى اختيار نوع الاستفسار</div>
                            </div>
                            
                            <div class="form-group">
                                <label for="message">رسالتك</label>
                                <textarea id="message" class="form-control" required></textarea>
                                <div class="form-error" id="messageError">يرجى كتابة رسالتك</div>
                            </div>
                            
                            <button type="submit" class="btn" style="width: 100%;">
                                <i class="fas fa-paper-plane"></i> إرسال الرسالة
                            </button>
                        </form>
                    </div>
                    
                    <div class="contact-info">
                        <h3>معلومات التواصل</h3>
                        
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <div>
                                <h4>العنوان</h4>
                                <p>جامعة الجزيرة، السودان</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <div>
                                <h4>الهاتف</h4>
                                <p>0964916347</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <div>
                                <h4>البريد الإلكتروني</h4>
                                <p>mhjwmhmd.com</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <i class="fas fa-clock"></i>
                            <div>
                                <h4>ساعات التواصل</h4>
                                <p>الأحد - الخميس: 9 صباحاً - 5 مساءاً</p>
                                <p>الجمعة والسبت: متاح في الصباح</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <i class="fas fa-graduation-cap"></i>
                            <div>
                                <h4>الدراسة</h4>
                                <p>طالب في كلية العلوم الرياضية والحاسوب</p>
                                <p>جامعة الجزيرة</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="contact-comments">
                        <h3>آخر التعليقات</h3>
                        <div id="commentsContainer">
                            <div class="comment">
                                <div class="comment-header">
                                    <span class="comment-name">أحمد حسن</span>
                                    <span class="comment-type">مقترح</span>
                                </div>
                                <div class="comment-email">ahmed@example.com</div>
                                <p>أعجبني مشروع التحليل الإحصائي للبطالة، هل يمكن مشاركة الدراسة كاملة؟</p>
                            </div>
                            <div class="comment">
                                <div class="comment-header">
                                    <span class="comment-name">سارة محمد</span>
                                    <span class="comment-type">استفسار</span>
                                </div>
                                <div class="comment-email">sara@example.com</div>
                                <p>هل تبحث عن فرص تدريب في مجال تحليل البيانات؟ لدينا فرصة قد تناسبك.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.nav-link');
            const pages = document.querySelectorAll('.page');
            
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetPage = this.getAttribute('data-page');
                    
                    navLinks.forEach(l => l.classList.remove('active'));
                    this.classList.add('active');
                    
                    pages.forEach(page => page.classList.remove('active'));
                    document.getElementById(targetPage).classList.add('active');
                });
            });
            
            const themeToggle = document.getElementById('themeToggle');
            const themeIcon = themeToggle.querySelector('i');
            
            const savedTheme = localStorage.getItem('theme');
            if (savedTheme === 'dark') {
                document.body.classList.add('dark-mode');
                themeIcon.classList.remove('fa-moon');
                themeIcon.classList.add('fa-sun');
            }
            
            themeToggle.addEventListener('click', function() {
                document.body.classList.toggle('dark-mode');
                
                if (document.body.classList.contains('dark-mode')) {
                    themeIcon.classList.remove('fa-moon');
                    themeIcon.classList.add('fa-sun');
                    localStorage.setItem('theme', 'dark');
                } else {
                    themeIcon.classList.remove('fa-sun');
                    themeIcon.classList.add('fa-moon');
                    localStorage.setItem('theme', 'light');
                }
            });
            
            const greeting = document.getElementById('greeting');
            const hour = new Date().getHours();
            
            if (hour >= 5 && hour < 12) {
                greeting.textContent = 'صباح الخير!';
            } else if (hour >= 12 && hour < 18) {
                greeting.textContent = 'مساء الخير!';
            } else {
                greeting.textContent = 'مساء الخير!';
            }
            
            const cursor = document.getElementById('cursor');
            let mouseX = 0;
            let mouseY = 0;
            
            document.addEventListener('mousemove', function(e) {
                mouseX = e.clientX;
                mouseY = e.clientY;
                
                cursor.style.left = mouseX + 'px';
                cursor.style.top = mouseY + 'px';
            });
            
            const bgOptions = document.querySelectorAll('.bg-option');
            
            bgOptions.forEach(option => {
                option.addEventListener('click', function() {
                    const bgType = this.getAttribute('data-bg');
                    
                    if (bgType === 'color') {
                        document.body.style.backgroundImage = 'none';
                        document.body.style.backgroundColor = '#ecf0f1';
                    } else if (bgType === 'color2') {
                        document.body.style.backgroundImage = 'none';
                        document.body.style.backgroundColor = '#d5f5e3';
                    } else if (bgType === 'gradient') {
                        document.body.style.backgroundImage = 'linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%)';
                    }
                    
                    localStorage.setItem('background', bgType);
                });
            });
            
            const savedBg = localStorage.getItem('background');
            if (savedBg) {
                const selectedOption = document.querySelector(`.bg-option[data-bg="${savedBg}"]`);
                if (selectedOption) {
                    selectedOption.click();
                }
            }
            
            const contactForm = document.getElementById('contactForm');
            
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                document.querySelectorAll('.form-error').forEach(error => {
                    error.style.display = 'none';
                });
                
                const name = document.getElementById('name').value;
                const email = document.getElementById('email').value;
                const inquiry = document.getElementById('inquiry').value;
                const message = document.getElementById('message').value;
                
                let isValid = true;
                
                if (name.trim() === '' || name.length < 3) {
                    document.getElementById('nameError').style.display = 'block';
                    isValid = false;
                }
                
                const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                if (!emailRegex.test(email)) {
                    document.getElementById('emailError').style.display = 'block';
                    isValid = false;
                }
                
                if (inquiry === '') {
                    document.getElementById('inquiryError').style.display = 'block';
                    isValid = false;
                }
                
                if (message.trim() === '' || message.length < 10) {
                    document.getElementById('messageError').style.display = 'block';
                    isValid = false;
                }
                
                if (isValid) {
                    const commentsContainer = document.getElementById('commentsContainer');
                    
                    const commentDiv = document.createElement('div');
                    commentDiv.className = 'comment';
                    commentDiv.innerHTML = `
                        <div class="comment-header">
                            <span class="comment-name">${name}</span>
                            <span class="comment-type">${inquiry}</span>
                        </div>
                        <div class="comment-email">${email}</div>
                        <p>${message}</p>
                    `;
                    
                    commentsContainer.insertBefore(commentDiv, commentsContainer.firstChild);
                    
                    alert('تم إرسال رسالتك بنجاح! شكراً لتواصلك معي.');
                    
                    contactForm.reset();
                }
            });
            
            document.querySelectorAll('.hero-btns .btn').forEach(btn => {
                btn.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetPage = this.getAttribute('data-page');
                    
                    navLinks.forEach(l => l.classList.remove('active'));
                    document.querySelector(`.nav-link[data-page="${targetPage}"]`).classList.add('active');
                    
                    pages.forEach(page => page.classList.remove('active'));
                    document.getElementById(targetPage).classList.add('active');
                });
            });
        });
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <!-- باقي كود head كما هو -->
</head>
<body>
    <!-- باقي كود الموقع كما هو -->

    <footer>
        <div class="container">
            <div class="logo">
                <i class="fas fa-user"></i>
                <span>محمد محجوب إسماعيل</span>
            </div>
            
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-researchgate"></i></a>
            </div>
            
            <p>طالب في كلية العلوم الرياضية والحاسوب بجامعة الجزيرة &copy; 2025</p>
        </div>
    </footer>

    <script>
        // باقي كود الجافاسكريبت كما هو
    </script>
</body>
</html>
