<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ورشة الفارس للنحت وزخرفة الحديد</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* جميع الأنماط السابقة تبقى كما هي */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            background: linear-gradient(rgba(0, 0, 0, 0.0), rgba(0, 0, 0, 0.0)), 
                        url('https://i.postimg.cc/d3c9GFtQ/IMG-20250504-WA0021.jpg');
            background-size: cover;
            background-attachment: fixed;
            color: #fff;
            line-height: 1.6;
        }

        .welcome-page {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(0, 0, 0, 0.0), rgba(0, 0, 0, 0.0)), 
                        url('https://i.postimg.cc/8zSqT8hx/FB-IMG-1649978073623.jpg');
            background-size: cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            transition: opacity 1s ease;
        }

        .welcome-logo {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            overflow: hidden;
            margin-bottom: 20px;
            border: 3px solid gold;
        }

        .welcome-logo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .welcome-text {
            text-align: center;
            margin-bottom: 30px;
        }

        .welcome-text h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            color: #f11ff1;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
            letter-spacing: 5px;
            transform: scaleX(1.3);
            display: inline-block;
        }

        .welcome-text h2 {
            font-size: 1.6rem;
            margin-bottom: 20px;
            color: #11ffc9;
        }

        .enter-btn {
            padding: 15px 40px;
            background: linear-gradient(45deg, gold, silver);
            border: none;
            border-radius: 50px;
            color: #000;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(255, 215, 0, 0.4);
        }

        .enter-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(255, 215, 0, 0.6);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            display: none;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            border-bottom: 2px solid rgba(255, 215, 0, 0.5);
            margin-bottom: 30px;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            margin-left: 15px;
            border: 2px solid gold;
        }

        .logo-text {
            text-align: right;
        }

        .workshop-name {
            font-size: 3.5rem;
            font-weight: bold;
            background: linear-gradient(to right, gold, silver, #ff6b6b, #4ecdc4, #bbbbbd, #ddddde, #ff54cc, #c12fff, #ff316d, #b534cc, #a65dcd, #deebda);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: colorChange 2s infinite alternate;
            background-size: 300% 300%;
            letter-spacing: 5px;
            transform: scaleX(1.3);
            display: inline-block;
            position: relative;
        }

        .workshop-name::after {
            content: "";
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background: linear-gradient(90deg, transparent 0%, rgba(255, 215, 0, 0.4) 50%, transparent 100%);
            opacity: 0;
            animation: glowEffect 0s infinite;
        }

        @keyframes glowEffect {
            0%, 100% { opacity: 0; }
            50% { opacity: 1; }
        }

        .laser-text {
            font-size: 0.9rem;
            margin-top: 5px;
            color: #11ffc9;
            text-shadow: 0 0 5px rgba(25, 215, 54, 18.7);
            font-weight: bold;
            font-family: 'Times New Roman', serif;
            letter-spacing: 5px;
            position: relative;
            display: inline-block;
        }

        .laser-text::after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(to right, transparent, gold, transparent);
        }

        @keyframes colorChange {
            0% { background-position: 0% 50%; }
            100% { background-position: 100% 50%; }
        }

        .knight-name {
            font-size: 1.4rem;
            color: silver;
            margin-top: 5px;
        }

        .section {
            background: rgba(0, 0, 0, 0.7);
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 30px;
            border: 1px solid rgba(255, 215, 0, 0.3);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(10px);
        }

        .section-title {
            text-align: center;
            font-size: 1rem;
            margin-bottom: 20px;
            background: linear-gradient(to right, gold, silver,  #ff78fc);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            padding: 10px;
            border-bottom: 2px solid gold;
        }

        .image-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .image-gallery img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 10px;
            transition: transform 0.3s ease;
            border: 2px solid rgba(255, 215, 0, 0.3);
        }

        .image-gallery img:hover {
            transform: scale(1.05);
            border-color: gold;
        }

        .price-btn {
            display: block;
            margin: 30px auto;
            padding: 15px 40px;
            background: linear-gradient(45deg, gold, silver);
            border: none;
            border-radius: 50px;
            color: #000;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(255, 215, 0, 0.4);
        }

        .price-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(255, 215, 0, 0.6);
        }

        .price-table {
            display: none;
            margin-top: 20px;
            width: 100%;
            border-collapse: collapse;
            background: rgba(0, 0, 0, 0.8);
            border-radius: 10px;
            overflow: hidden;
        }

        .price-table th, .price-table td {
            padding: 15px;
            text-align: center;
            border-bottom: 1px solid rgba(255, 215, 0, 0.3);
        }

        .price-table th {
            background: linear-gradient(45deg, gold, silver);
            color: #000;
            font-weight: bold;
        }

        .price-table tr:last-child td {
            border-bottom: none;
        }

        .owner-name {
            text-align: center;
            padding: 25px;
            border: 2px solid gold;
            border-radius: 10px;
            margin: 20px 0;
            overflow: hidden;
            white-space: nowrap;
            position: relative;
            background: rgba(0, 0, 0, 0.7);
            animation: colorCycle 10s infinite;
        }

        .owner-name::before {
            content: "🔮 لصاحبها ☜ وديع عبدالواحد الذماري 🔮";
            position: absolute;
            right: 100%;
            animation: marquee 10s linear infinite;
        }

        @keyframes marquee {
            10% { right: 100%; }
            100% { right: -100%; }
        }

        @keyframes colorCycle {
            0% { color: gold; }
            25% { color: silver; }
            30% { color: #facedb; }
            40% { color: #86cdff; }
            50% { color: #ff6b6b; }
            60% { color: #dbbeef; }
            75% { color: #4ecdc4; }
            85% { color: #ff87df; }
            90% { color: #f33ccd; }
            100% { color: gold; }
        }

        .address {
            text-align: center;
           font-size: 0.9rem;
           
            color: #11ffc9;
            padding: 15px;
            border: 2px solid silver;
            border-radius: 10px;
            margin: 20px 0;
            background: rgba(0, 0, 0, 0.5);
        }

        .contact-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .phones {
            display: flex;
            gap: 2px;
        }

        .phone {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 1.0rem;
            color: #11ffc9;
        
        }

        .social-icons {
            display: flex;
            gap: 15px;
        }

        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            color: #fff;
            font-size: 1.6rem;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .social-icons a:nth-child(1) { /* واتساب */
            background: rgba(37, 211, 102, 0.8);
        }
        
        .social-icons a:nth-child(2) { /* تليجرام */
            background: rgba(0, 136, 204, 0.8);
        }
        
        .social-icons a:nth-child(3) { /* فيسبوك */
            background: rgba(59, 89, 152, 0.8);
        }
        
        .social-icons a:nth-child(4) { /* واتساب للأعمال */
            background: rgba(37, 211, 102, 0.8);
        }

        .social-icons a:hover {
            transform: scale(1.1);
            background: rgba(255, 215, 0, 0.7);
            color: #000;
        }

        .designer {
            text-align: center;
            margin-top: 30px;
            padding: 2px;
            border-top: 8px solid rgba(25, 25, 25, 5.2);
            font-size: 1.0rem;
            color: #111111;
        }

        /* إطارات الصور المتحركة */
        .animated-frame {
            position: relative;
            border-radius: 15px;
            overflow: hidden;
            margin-bottom: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
            animation: frameAnimation 6s infinite alternate;
            border: 2px solid transparent;
            background: linear-gradient(45deg, rgba(255,215,0,0.2), rgba(192,192,192,0.2));
            padding: 10px;
        }

        @keyframes frameAnimation {
            0% {
                border-color: gold;
                box-shadow: 0 0 20px rgba(255,215,0,0.5);
                transform: scale(1);
            }
            25% {
                border-color: silver;
                box-shadow: 0 0 20px rgba(192,192,192,0.5);
                transform: scale(1.01);
            }
            50% {
                border-color: #ff6b6b;
                box-shadow: 0 0 20px rgba(255,107,107,0.5);
                transform: scale(1);
            }
            75% {
                border-color: #4ecdc4;
                box-shadow: 0 0 20px rgba(78,205,196,0.5);
                transform: scale(1.01);
            }
            100% {
                border-color: gold;
                box-shadow: 0 0 20px rgba(255,215,0,0.5);
                transform: scale(1);
            }
        }

        .animated-frame .image-container {
            display: flex;
            overflow: hidden;
            border-radius: 10px;
            height: 250px;
            position: relative;
        }

        .animated-frame .image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            top: 0;
            left: 0;
            opacity: 0;
            transition: opacity 1s ease-in-out;
        }

        .animated-frame .image-container img.active {
            opacity: 1;
        }

        .frame-title {
            text-align: center;
            padding: 10px;
            background: linear-gradient(45deg, rgba(255,215,0,0.3), rgba(192,192,192,0.3));
            border-radius: 8px;
            margin-top: 10px;
            font-weight: bold;
            font-size: 1.2rem;
            color: #fff;
            text-shadow: 0 0 5px rgba(0,0,0,0.7);
        }

        @media (max-width: 768px) {
            header {
                flex-direction: column;
                text-align: center;
            }
            
            .logo {
                margin-bottom: 15px;
            }
            
            .workshop-name {
                font-size: 2.5rem;
                transform: scaleX(1.1);
            }
            
            .welcome-text h1 {
                font-size: 2.5rem;
                transform: scaleX(1.1);
            }
            
            .contact-info {
                flex-direction: column;
                gap: 20px;
            }
            
            .phones {
                flex-direction: column;
                gap: 10px;
            }
            
            .image-gallery {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
            
            .animated-frame .image-container {
                height: 200px;
            }
        }
    </style>
</head>
<body>
    <!-- صفحة الترحيب -->
    <div class="welcome-page" id="welcomePage">
        <div class="welcome-logo">
            <img src="https://i.postimg.cc/LXNt7Pm0/Screenshot-2.jpg" alt="شعار الورشة">
        </div>
        <div class="welcome-text">
            <h1>الفارس</h1>
          <h2>للنحت وزخرفة الحديد بالليزار</h2>
            <h2>ترحب بكم</h2>
        </div>
        <button class="enter-btn" id="enterBtn">الدخول إلى المعرض</button>
    </div>

    <!-- الصفحة الرئيسية -->
    <div class="container" id="mainPage">
        <header>
            <div class="logo">
                <img src="https://i.postimg.cc/LXNt7Pm0/Screenshot-2.jpg" alt="شعار الورشة">
                <div class="logo-text">
                    <div class="workshop-name">الفارس</div>
                    <div class="laser-text">للنحت وزخرفة الحديد بالليزار </div>
                
                </div>
            </div>
        </header>

        <!-- قسم النحت وزخرفة الحديد بالليزر -->
        <section class="section">
            <h2 class="section-title">نحت وزخرفة بوابات أحواش</h2>
            <div class="animated-frame">
                <div class="image-container" id="laserContainer"></div>
                <div class="frame-title">أعمال النحت بالليزر</div>
            </div>
        </section>

        <!-- قسم النحت وزخرفة بوابات أحواش -->
        <section class="section">
            <h2 class="section-title">نحت وزخرفة أبواب رسمية</h2>
            <div class="animated-frame">
                <div class="image-container" id="gatesContainer"></div>
                <div class="frame-title">نحت وزخرفة بالليزار</div>
            </div>
        </section>

        <!-- قسم النحت وزخرفة حماية النوافذ -->
        <section class="section">
            <h2 class="section-title">نحت وزخرفة حماية النوافذ</h2>
            <div class="animated-frame">
                <div class="image-container" id="windowsContainer"></div>
                <div class="frame-title">حماية النوافذ المزخرفة</div>
            </div>
        </section>

        <!-- قسم النحت وزخرفة درابزينات -->
        <section class="section">
            <h2 class="section-title">نحت وزخرفة درابزينات</h2>
            <div class="animated-frame">
                <div class="image-container" id="railingsContainer"></div>
                <div class="frame-title">درابزينات فنية</div>
            </div>
        </section>

        <!-- قسم النحت وزخرفة حماية البلكونات -->
        <section class="section">
            <h2 class="section-title">نحت وزخرفة حماية البلكونات</h2>
            <div class="animated-frame">
                <div class="image-container" id="balconiesContainer"></div>
                <div class="frame-title">حماية البلكونات المزخرفة</div>
            </div>
        </section>

        <!-- قسم النحت وزخرفة ديكورات -->
        <section class="section">
            <h2 class="section-title">نحت وزخرفة ديكورات</h2>
            <div class="animated-frame">
                <div class="image-container" id="decorationsContainer"></div>
                <div class="frame-title">ديكورات حديدية فنية</div>
            </div>
        </section>

        <!-- قسم النحت وزخرفة طاولات ومقاعد وكراسي -->
        <section class="section">
            <h2 class="section-title">نحت وزخرفة طاولات ومقاعد</h2>
            <div class="animated-frame">
                <div class="image-container" id="furnitureContainer"></div>
                <div class="frame-title">أثاث حديدي مزخرف</div>
            </div>
        </section>

        <!-- قسم فريق التصميم -->
        <section class="section">
            <h2 class="section-title">إطلب نقشتك تجدها المصمم</h2>
            <div class="animated-frame">
                <div class="image-container" id="designTeamContainer"></div>
                <div class="frame-title">محمد الصوفي وديع الذماري</div>
            </div>
        </section>

        <!-- قسم جديد: قطع غيار مكائن الليزر -->
        <section class="section">
            <h2 class="section-title">يوجد لدينا قطاع</h2>
            <div class="animated-frame">
                <div class="image-container" id="sparePartsContainer"></div>
                <div class="frame-title">مكائن الليزار وفرمات البلوك</div>
            </div>
        </section>

        <!-- قسم الأسعار -->
        <section class="section">
            <h2 class="section-title">أسعارنا</h2>
            <button class="price-btn" id="priceBtn">عرض الأسعار</button>
            <table class="price-table" id="priceTable">
                <thead>
                    <tr>
                        <th>نوع العمل</th>
                        <th>السعر (ريال سعودي)</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>نحت الحديد المتر المربع أبو 4ملي</td>
                        <td>155 ريال سعودي</td>
                    </tr>
                    <tr>
                        <td>نحت الحديد المتر المربع أبو 3ملي</td>
                        <td>125 ريال سعودي</td>
                    </tr>
                    <tr>
                        <td>نحت الحديد المتر المربع أبو 2ملي</td>
                        <td>100 ريال سعودي</td>
                    </tr>
                    <tr>
                        <td>نحت الحديد المتر المربع أبو 1ملي</td>
                        <td>80 ريال سعودي</td>
                 </tr>
            
                <tr>
                        <td>فرمات أبو 15</td>
                        <td>500 ريال سعودي</td>
                 </tr>
                
                <tr>
                        <td>فرمات أبو 20</td>
                        <td>600 ريال سعودي</td>
                 </tr>
                
                </tbody>
            </table>
        </section>

        <!-- اسم المالك -->
        <div class="owner-name"></div>

        <!-- العنوان -->
        <div class="address">
            <h3>العنوان: النشمة خط الاحد العين جوار مصنع الذماري للبلوك والنيسة</h3>
        </div>

        <!-- معلومات الاتصال -->
        <div class="contact-info">
            <div class="phones">
                <div class="phone">
                    <i class="fas fa-phone"></i>
                    <span>738406789📱774854854</span>
                </div>

            </div>
            <div class="social-icons">
                <a href="https://wa.me/738406789" target="_blank">
                    <i class="fab fa-whatsapp"></i>
                </a>
                <a href="https://t.me/738406789" target="_blank">
                    <i class="fab fa-telegram"></i>
                </a>
                <a href="#" target="_blank">
                    <i class="fab fa-facebook"></i>
                </a>
                <a href="https://wa.me/774854854" target="_blank">
                    <i class="fab fa-whatsapp"></i>
                </a>
            </div>
        </div>

        <!-- معلومات المصمم -->
        <div class="designer">
            <p>إعداد وتطوير 🖋️فياد رضوان الصوفي</p>
            <p>تلفون: 730441554 📱 784773426</p>
        </div>
    </div>

    <script>
        // بيانات الصور
        const imageData = {
            laser: [
                "https://i.postimg.cc/y62RYqBm/trashed-1761994231-6966ceac981ce1bf9909ea5fb792d18c.jpg",
                "https://i.postimg.cc/3wwNF97j/trashed-1761994240-7fa737e85c87e416e944e54cdcbbaf10.jpg",
                "https://i.postimg.cc/JhymhFR8/trashed-1761994263-512c89a4a853150e6c8597215e42ff34.jpg",
                "https://i.postimg.cc/fyC1C7Mr/trashed-1761994287-1787196996f91bb9d783677479b42662-2.jpg",
                "https://i.postimg.cc/J7xF9qWb/trashed-1761994336-87baa2ac188af1e0fe785cbb78996b35.jpg"
            ],
            gates: [
                "https://i.postimg.cc/FHrCGk6G/trashed-1761994632-f28807a9-6a60-49bd-852c-04f263ab042e.jpg",
                "https://i.postimg.cc/MT7QV7cQ/38732303.jpg",
                "https://i.postimg.cc/hjBdbTyM/trashed-1761994686-f7a08efdff01148f229d4a6c0998e58a.jpg",
                "https://i.postimg.cc/ZR4WyZn2/trashed-1761994704-eaa5c90781fecad0ba3bd8e3553d3fac.jpg",
                "https://i.postimg.cc/4xp4vMrP/trashed-1761994722-089f40b36c537fe32ccbdf0baa58b24e.jpg"
            ],
            windows: [
                "https://i.postimg.cc/4NDVND6P/trashed-1761994863-6b949ffc38f7f3a36efd9820b0e31f10.jpg",
                "https://i.postimg.cc/bJV2XWY5/trashed-1761994898-a6d786554e6dbfdae52594e9ce8879fc.jpg",
                "https://i.postimg.cc/HLpJrdVX/trashed-1761994921-compressed-15-1024x1536.webp",
                "https://i.postimg.cc/hGy9gfpP/trashed-1761994937-compressed-9-1024x1536-1.webp",
                "https://i.postimg.cc/FHGSgYtB/trashed-1761994967-ec90f2b5ba15b50b7cfb51299064c94c.jpg"
            ],
            railings: [
                "https://i.postimg.cc/kgPsh6pX/f3351278871a101b826cf5a05378d769-2.jpg",
                "https://i.postimg.cc/mr2581PS/a0027aa264befbe60ca7fc1942934d03.jpg",
                "https://i.postimg.cc/CK1cjy27/6d84a18595800d06783938f6ac737527.jpg",
                "https://i.postimg.cc/8cBR2w3k/6c1e8d17df7adf8a02baee9a03886b70.jpg",
                "https://i.postimg.cc/wxcDTfWC/53f396549298d36b07e70282b692b868-2.jpg"
            ],
            balconies: [
                "https://i.postimg.cc/BZkfbpXd/7852c4dc1850332752b71878d8061787.jpg",
                "https://i.postimg.cc/sXxbDGzq/6d588b267649253191d054fabd4204c8.jpg",
                "https://i.postimg.cc/sgcVMSFd/61c75fb52291c2839c939cc9a36de49b.jpg",
                "https://i.postimg.cc/DfXnqRVC/420967f44b69943ef6f498babc64cf9e.jpg"
            ],
            decorations: [
                "https://i.postimg.cc/vTLK0rtf/11fd86ff1cf0845cdef7c095a07bd00f-2.jpg",
                "https://i.postimg.cc/DzJY9kcW/1a3bf4ff011e91c338d1f33b9612e733.jpg",
                "https://i.postimg.cc/0Q1Zh6Qj/2eccd32b19422bd24b6517b5c5a3fc42.jpg",
                "https://i.postimg.cc/dtVnMcq5/321272555c4424c55ca83a1d9b0c34f1-2.jpg",
                "https://i.postimg.cc/XJWcQTHP/5efcc1df2daf4fa467632ef5159ca7ec.jpg"
            ],
            furniture: [
                "https://i.postimg.cc/c1ntrDFy/06ae59655b3ee6aa0d632459edb001ef.jpg",
                "https://i.postimg.cc/jj1CjNNL/112277af73c7038921595bf5d51a00fb.jpg",
                "https://i.postimg.cc/qvbvmn1b/15dfaf6531626b5d34c22f1eb7c94ee8.jpg",
                "https://i.postimg.cc/C5sFbfZC/3ebd27ee8a44d112c1257cbb60b25687.jpg",
                "https://i.postimg.cc/JnbmWBQC/433f485d52054fe6d325db6d338a9245.jpg"
            ],
            designTeam: [
                "https://i.postimg.cc/4ycTZV2M/IMG-2.jpg",
                "https://i.postimg.cc/8Cn86t2V/2.jpg",
                "https://i.postimg.cc/vH7pzQJg/IMG-20201117-WA0007.jpg",
 
                "https://i.postimg.cc/J4Hk0Vy7/img-1761064295284.jpg",                  
            
"https://i.postimg.cc/Hn4F4PnS/img-1761065083309.png",      
            
            ],
            spareParts: [
                "https://i.postimg.cc/sx8fV3Jm/images-2.jpg",
                "https://i.postimg.cc/MTpzVnPy/images-4.jpg",
                "https://i.postimg.cc/HLBgYpY5/images-3.jpg",
                "https://i.postimg.cc/Bt9WYbp6/images-1.jpg",
                "https://i.postimg.cc/KvB4ZgdW/trashed-1763484260-images.jpg"
            ]
        };

        // تحميل الصور في الإطارات المتحركة
        function loadImages() {
            for (const category in imageData) {
                const container = document.getElementById(`${category}Container`);
                if (container) {
                    imageData[category].forEach((imgUrl, index) => {
                        const img = document.createElement('img');
                        img.src = imgUrl;
                        img.alt = `صورة ${category}`;
                        if (index === 0) {
                            img.classList.add('active');
                        }
                        container.appendChild(img);
                    });
                }
            }
            
            // بدء تحريك الصور
            startImageSlideshow();
        }

        // تحريك الصور في الإطارات
        function startImageSlideshow() {
            for (const category in imageData) {
                const container = document.getElementById(`${category}Container`);
                if (container) {
                    const images = container.getElementsByTagName('img');
                    let currentIndex = 0;
                    
                    setInterval(() => {
                        // إخفاء جميع الصور
                        for (let img of images) {
                            img.classList.remove('active');
                        }
                        
                        // إظهار الصورة التالية
                        currentIndex = (currentIndex + 1) % images.length;
                        images[currentIndex].classList.add('active');
                    }, 3000); // تغيير الصورة كل 3 ثواني
                }
            }
        }

        // التحكم في صفحة الترحيب
        document.getElementById('enterBtn').addEventListener('click', function() {
            document.getElementById('welcomePage').style.opacity = '0';
            setTimeout(() => {
                document.getElementById('welcomePage').style.display = 'none';
                document.getElementById('mainPage').style.display = 'block';
            }, 1000);
        });

        // التحكم في جدول الأسعار
        document.getElementById('priceBtn').addEventListener('click', function() {
            const table = document.getElementById('priceTable');
            if (table.style.display === 'none' || table.style.display === '') {
                table.style.display = 'table';
                this.textContent = 'إخفاء الأسعار';
            } else {
                table.style.display = 'none';
                this.textContent = 'عرض الأسعار';
            }
        });

        // تحميل الصور عند فتح الصفحة
        window.addEventListener('load', loadImages);
    </script>
</body>
</html>
