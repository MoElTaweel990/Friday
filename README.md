<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تعلم الإنجليزية: الأبجدية والقواعد الأساسية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #6a0572;
            --secondary-color: #ff6f61;
            --accent-color: #4CAF50;
            --light-color: #fce4ec;
            --dark-color: #4a4a68;
            --card-bg: #ffffff;
            --border-color: #e0e0e0;
            --shadow-color: rgba(0, 0, 0, 0.15);
            --nav-height: 70px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--light-color);
            color: var(--dark-color);
            line-height: 1.8;
            direction: rtl;
            text-align: right;
            scroll-behavior: smooth;
            padding-top: var(--nav-height);
        }

        /* Navigation Bar */
        .nav-container {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            background: linear-gradient(135deg, #6a0572, #4a0360);
            padding: 10px 0;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
            height: var(--nav-height);
        }
        
        .nav-scroll-container {
            display: flex;
            justify-content: center;
            overflow-x: auto;
            padding: 0 15px;
            scrollbar-width: none;
        }
        
        .nav-scroll-container::-webkit-scrollbar {
            display: none;
        }
        
        .nav-buttons {
            display: flex;
            gap: 8px;
            padding: 5px 0;
        }
        
        .nav-btn {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-width: 110px;
            padding: 10px 15px;
            background: rgba(255, 255, 255, 0.1);
            border: 2px solid rgba(255, 255, 255, 0.15);
            border-radius: 20px;
            color: white;
            font-weight: bold;
            font-size: 0.9rem;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(5px);
        }
        
        .nav-btn:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.25);
        }
        
        .nav-btn.active {
            background: var(--secondary-color);
            border-color: rgba(255, 255, 255, 0.3);
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(255, 111, 97, 0.4);
        }
        
        .nav-btn i {
            font-size: 1.4rem;
            margin-bottom: 5px;
            transition: transform 0.3s ease;
        }
        
        .nav-btn:hover i {
            transform: scale(1.2);
        }
        
        /* Header */
        header {
            background-image: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 2em 0;
            text-align: center;
            position: relative;
            overflow: hidden;
            margin-top: 0;
        }

        header::before, header::after {
            content: '';
            position: absolute;
            width: 200px;
            height: 200px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }

        header::before {
            top: -50px;
            left: -50px;
            transform: rotate(45deg);
        }

        header::after {
            bottom: -50px;
            right: -50px;
            transform: rotate(-30deg);
        }

        header h1 {
            margin: 0;
            font-size: 2.8rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            letter-spacing: 1px;
            position: relative;
            z-index: 1;
        }

        /* Main content */
        main {
            padding: 30px 20px;
            max-width: 1300px;
            margin: 30px auto;
        }

        section {
            background-color: var(--card-bg);
            border-radius: 12px;
            box-shadow: 0 0 20px var(--shadow-color);
            margin-bottom: 40px;
            padding: 30px;
            scroll-margin-top: calc(var(--nav-height) + 20px);
        }
        
        .section-intro {
            text-align: center;
            font-size: 1.15rem;
            margin-bottom: 30px;
            color: #555;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        h2 {
            color: var(--primary-color);
            text-align: center; /* Ensures text is centered */
            margin: 0 auto 20px auto; /* Centers the block itself */
            font-size: 2.2rem;
            border-bottom: 3px solid var(--secondary-color);
            display: block; /* Ensure it's a block for margin: auto to work */
            padding-bottom: 10px;
            position: relative; /* Keep for pseudo-elements */
            width: fit-content; /* Make the width fit content for centering with margin: auto */
        }

        h2::after, h2::before {
            content: '✨';
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
        }

        h2::after {
            left: -30px;
        }

        h2::before {
            right: -30px;
        }

        h3 {
            color: var(--dark-color);
            font-size: 1.8rem;
            margin: 30px 0 20px;
            padding-bottom: 5px;
            border-bottom: 1px dashed var(--border-color);
            text-align: center; /* Center h3 elements */
        }

        .instruction {
            text-align: center;
            font-style: italic;
            color: #666;
            margin-bottom: 30px;
            font-size: 1.1rem;
        }

        /* Alphabet Section */
        #alphabet-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
            gap: 15px;
            justify-content: center;
            margin-bottom: 30px;
        }

        .alphabet-letter-button {
            background-color: var(--primary-color);
            color: white;
            font-size: 2.5rem;
            font-weight: bold;
            padding: 15px 0;
            border-radius: 10px;
            cursor: pointer;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            border: 2px solid var(--primary-color);
        }

        .alphabet-letter-button:hover {
            background-color: var(--secondary-color);
            transform: translateY(-5px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
            border-color: var(--secondary-color);
        }

        .alphabet-letter-button.active-letter {
            background-color: var(--accent-color);
            border-color: var(--accent-color);
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }

        #words-display-area {
            margin-top: 40px;
            padding: 30px;
            background-color: var(--light-color);
            border-radius: 12px;
            box-shadow: inset 0 0 15px rgba(0, 0, 0, 0.1);
            min-height: 200px;
            display: none; /* Hidden by default, JS will show it */
            flex-direction: column;
            gap: 15px;
            border: 2px dashed var(--secondary-color);
        }

        .word-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 15px;
            background-color: var(--card-bg);
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .word-item:hover {
            transform: translateX(-5px);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }

        .english-word {
            cursor: pointer;
            font-weight: bold;
            color: var(--primary-color);
            font-size: 1.2rem;
            transition: color 0.2s ease-in-out;
            direction: ltr; /* Ensure English words are LTR */
            text-align: left;
        }

        .english-word:hover {
            color: var(--secondary-color);
            text-decoration: underline;
        }

        .arabic-translation {
            color: var(--dark-color);
            font-size: 1.1rem;
        }
        
        /* Colors Section specific */
        .color-box {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 1px solid #ccc;
            vertical-align: middle;
            margin-left: 8px;
            border-radius: 4px;
        }

        /* Grammar and Tenses Sections */
        .grammar-topic {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: box-shadow 0.3s ease-in-out;
        }

        .grammar-topic:hover {
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15);
        }
        
        .grammar-topic h3 {
            cursor: pointer;
            color: var(--primary-color);
            font-size: 2rem;
            margin-top: 0;
            border-bottom: 2px dashed var(--secondary-color);
            padding-bottom: 12px;
            transition: color 0.2s ease-in-out;
        }

        .grammar-topic h3:hover {
            color: var(--secondary-color);
        }

        .grammar-text {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .grammar-topic ul {
            list-style: none;
            padding-right: 0;
            margin-top: 15px;
        }

        .grammar-topic ul li {
            position: relative;
            padding-right: 30px;
            margin-bottom: 12px;
            font-size: 1.05rem;
        }

        .grammar-topic ul li::before {
            content: '🌟';
            color: var(--secondary-color);
            font-weight: bold;
            position: absolute;
            right: 0;
            font-size: 1.2rem;
        }

        .grammar-topic ul ul {
            margin-top: 8px;
            margin-bottom: 8px;
            padding-right: 20px;
        }

        .grammar-topic ul ul li::before {
            content: '💡';
            color: var(--accent-color);
        }

        /* Tables */
        .info-table-container {
            overflow-x: auto;
            margin-top: 25px;
        }

        .info-table {
            width: 100%;
            border-collapse: collapse;
            min-width: 600px;
        }

        .info-table th,
        .info-table td {
            border: 1px solid var(--border-color);
            padding: 15px;
            text-align: center;
            font-size: 1.05rem;
        }

        .info-table thead th {
            background-color: var(--primary-color);
            color: white;
            font-weight: bold;
            font-size: 1.1rem;
        }

        .info-table tbody tr:nth-child(even) {
            background-color: #fcf4f8;
        }

        .info-table tbody tr:hover {
            background-color: #ffe6f2;
        }
        
        /* Interactive Games Section */
        .game-card {
            background-color: var(--card-bg);
            border: 2px solid var(--border-color);
            border-radius: 10px;
            box-shadow: 0 5px 15px var(--shadow-color);
            padding: 25px;
            margin-bottom: 25px;
            text-align: center;
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
        }

        .game-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }

        .game-card h3 {
            font-size: 2rem;
            color: var(--primary-color);
            margin-bottom: 20px;
            border-bottom: 2px dashed var(--secondary-color);
            padding-bottom: 10px;
        }

        .game-card p {
            font-size: 1.1rem;
            color: var(--dark-color);
            margin-bottom: 20px;
        }

        .game-card .play-button {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 12px 25px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }

        .game-card .play-button:hover {
            background-color: #3e8e41;
            transform: translateY(-2px);
        }

        footer {
            text-align: center;
            padding: 25px;
            background-image: linear-gradient(to left, var(--primary-color), var(--secondary-color));
            color: white;
            margin-top: 50px;
            border-radius: 12px;
            box-shadow: 0 -4px 10px var(--shadow-color);
            font-size: 1.1rem;
        }

        /* Scroll to top button */
        .scroll-top-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--secondary-color);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            z-index: 100;
            opacity: 0;
            transform: translateY(20px);
        }
        
        .scroll-top-btn.show {
            opacity: 1;
            transform: translateY(0);
        }
        
        .scroll-top-btn:hover {
            background: #e55e50;
            transform: translateY(-5px);
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .nav-btn {
                min-width: 100px;
                padding: 8px 12px;
                font-size: 0.85rem;
            }
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2.2rem;
            }
            h2 {
                font-size: 1.8rem;
            }
            h3 {
                font-size: 1.6rem;
            }
            main {
                margin: 20px auto;
                padding: 20px;
            }
            .info-table th,
            .info-table td {
                padding: 10px;
                font-size: 0.9rem;
            }
            
            .nav-btn {
                min-width: 85px;
                padding: 6px 8px;
                font-size: 0.8rem;
            }
            
            .nav-btn i {
                font-size: 1.2rem;
            }

            #alphabet-grid {
                grid-template-columns: repeat(auto-fit, minmax(50px, 1fr));
                gap: 10px;
            }

            .alphabet-letter-button {
                font-size: 2rem;
                padding: 10px 0;
            }

            .word-item {
                flex-direction: column;
                align-items: flex-start;
                gap: 5px;
            }

            .english-word {
                font-size: 1.1rem;
            }
            .arabic-translation {
                font-size: 1rem;
            }
        }

        @media (max-width: 480px) {
            header h1 {
                font-size: 1.8rem;
            }
            h2 {
                font-size: 1.6rem;
                margin-bottom: 30px;
            }
            h2::after, h2::before {
                display: none;
            }
            h3 {
                font-size: 1.4rem;
            }
            .grammar-text, .grammar-topic ul li {
                font-size: 1rem;
            }
            footer {
                padding: 15px;
                font-size: 1rem;
            }
            
            .nav-buttons {
                gap: 5px;
            }
            
            .nav-btn {
                min-width: 75px;
                padding: 5px 6px;
                font-size: 0.75rem;
            }
            
            .nav-btn i {
                font-size: 1rem;
            }

            #alphabet-grid {
                grid-template-columns: repeat(auto-fit, minmax(40px, 1fr));
                gap: 8px;
            }

            .alphabet-letter-button {
                font-size: 1.8rem;
                padding: 8px 0;
            }
        }
    </style>
</head>
<body>
    <div class="nav-container">
        <div class="nav-scroll-container">
            <div class="nav-buttons">
                <div class="nav-btn active" data-section="alphabet-section">
                    <i class="fas fa-font"></i>
                    <span>الأبجدية</span>
                </div>
                <div class="nav-btn" data-section="pronunciation-section">
                    <i class="fas fa-microphone-alt"></i>
                    <span>النطق</span>
                </div>
                <div class="nav-btn" data-section="numbers-section">
                    <i class="fas fa-sort-numeric-up"></i>
                    <span>الأعداد</span>
                </div>
                <div class="nav-btn" data-section="colors-section">
                    <i class="fas fa-palette"></i>
                    <span>الألوان</span>
                </div>
                <div class="nav-btn" data-section="grammar-section">
                    <i class="fas fa-book"></i>
                    <span>القواعد</span>
                </div>
                <div class="nav-btn" data-section="tenses-section">
                    <i class="fas fa-clock"></i>
                    <span>الأزمنة</span>
                </div>
                <div class="nav-btn" data-section="common-words-section">
                    <i class="fas fa-list"></i>
                    <span>كلمات شائعة</span>
                </div>
                <div class="nav-btn" data-section="games-section">
                    <i class="fas fa-gamepad"></i>
                    <span>ألعاب تفاعلية</span>
                </div>
            </div>
        </div>
    </div>

    <div class="scroll-top-btn">
        <i class="fas fa-arrow-up"></i>
    </div>

    <header>
        <h1>تعلم الإنجليزية: الأبجدية والقواعد الأساسية</h1>
    </header>

    <main>
        <section id="alphabet-section">
            <h2>الأبجدية الإنجليزية وقائمة الكلمات</h2>
            <p class="section-intro">
                هنا تبدأ رحلتك مع حروف اللغة الإنجليزية. استكشف الحروف الأبجدية، واضغط على أي حرف لترى قائمة من الكلمات التي تبدأ به مع ترجمتها. هذه هي خطوتك الأولى لبناء مفرداتك.
            </p>
            <p class="instruction">اضغط على أي حرف لعرض 10 كلمات تبدأ به. اضغط على الكلمة لسماع نطقها.</p>
            <div class="alphabet-container" id="alphabet-container">
                <div id="alphabet-grid">
                    </div>
                <div id="words-display-area">
                    <p style="text-align: center; color: #777;">اختر حرفًا من الأعلى لعرض الكلمات.</p>
                </div>
            </div>
        </section>

        <section id="pronunciation-section">
            <h2>قواعد النطق (Pronunciation Rules)</h2>
            <p class="section-intro">
                النطق الصحيح هو مفتاح الثقة في التحدث. في هذا القسم، سنستعرض أهم قواعد نطق الحروف المتحركة، الساكنة، والمركبة بطريقة مبسطة. سيساعدك هذا على فهم كيف تتغير أصوات الحروف في الكلمات المختلفة.
            </p>
            <p class="instruction">اضغط على أي كلمة إنجليزية لسماع نطقها الصحيح وممارسة استماعك.</p>
            
            <div class="grammar-topic">
                <h3>1. الحروف المتحركة (Vowels)</h3>
                <div class="grammar-text">
                    <p>الحروف المتحركة الأساسية في اللغة الإنجليزية هي 
                        <span class="english-word">A</span>, 
                        <span class="english-word">E</span>, 
                        <span class="english-word">I</span>, 
                        <span class="english-word">O</span>, 
                        <span class="english-word">U</span>. هذه الحروف هي العمود الفقري للنطق في الإنجليزية، حيث يمكن لكل حرف متحرك أن ينتج أصواتًا متعددة، وأكثرها شيوعًا هي الأصوات القصيرة والطويلة.
                    </p>
                    <ul>
                        <li><strong>حرف A:</strong>
                            <ul>
                                <li>الصوت القصير (مثل الفتحة في العربية): يُنطق كـ "آ" خفيف مثل كلمة 
                                    <span class="english-word">cat</span> (قطة), 
                                    <span class="english-word">apple</span> (تفاحة), 
                                    <span class="english-word">back</span> (خلف).
                                </li>
                                <li>الصوت الطويل (مثل الألف الممدودة في العربية): يُنطق كـ "إيْ" في كلمة 
                                    <span class="english-word">name</span> (اسم), 
                                    <span class="english-word">cake</span> (كعكة), 
                                    <span class="english-word">game</span> (لعبة).
                                </li>
                            </ul>
                        </li>
                        <li>
                            <strong>حرف E:</strong>
                            <ul>
                                <li>الصوت القصير (مثل الكسرة الخفيفة): يُنطق كـ "إي" قصير مثل كلمة 
                                    <span class="english-word">bed</span> (سرير), 
                                    <span class="english-word">red</span> (أحمر), 
                                    <span class="english-word">pen</span> (قلم).
                                </li>
                                <li>الصوت الطويل (مثل الياء الممدودة في العربية): يُنطق كـ "إيي" طويل مثل كلمة 
                                    <span class="english-word">tree</span> (شجرة), 
                                    <span class="english-word">meet</span> (يقابل), 
                                    <span class="english-word">see</span> (يرى).
                                </li>
                            </ul>
                        </li>
                        <li>
                            <strong>حرف I:</strong>
                            <ul>
                                <li>الصوت القصير (مثل الكسرة الشديدة): يُنطق كـ "إِ" قصير مثل كلمة 
                                    <span class="english-word">pig</span> (خنزير), 
                                    <span class="english-word">sit</span> (يجلس), 
                                    <span class="english-word">fish</span> (سمكة).
                                </li>
                                <li>الصوت الطويل (مثل "آي" في العربية): يُنطق كـ "آي" مثل كلمة 
                                    <span class="english-word">bike</span> (دراجة), 
                                    <span class="english-word">light</span> (ضوء), 
                                    <span class="english-word">time</span> (وقت).
                                </li>
                            </ul>
                        </li>
                        <li>
                            <strong>حرف O:</strong>
                            <ul>
                                <li>الصوت القصير (مثل الضمة الخفيفة): يُنطق كـ "أو" قصير مثل كلمة 
                                    <span class="english-word">dog</span> (كلب), 
                                    <span class="english-word">hot</span> (حار), 
                                    <span class="english-word">box</span> (صندوق).
                                </li>
                                <li>الصوت الطويل (مثل الواو الممدودة في العربية): يُنطق كـ "أو" طويل مثل كلمة 
                                    <span class="english-word">boat</span> (قارب), 
                                    <span class="english-word">go</span> (يذهب), 
                                    <span class="english-word">home</span> (منزل).
                                </li>
                            </ul>
                        </li>
                        <li>
                            <strong>حرف U:</strong>
                            <ul>
                                <li>الصوت القصير (مثل الضمة الخفيفة): يُنطق كـ "أَ" مثل كلمة 
                                    <span class="english-word">sun</span> (شمس), 
                                    <span class="english-word">cup</span> (كوب), 
                                    <span class="english-word">run</span> (يركض).
                                </li>
                                <li>الصوت الطويل (مثل "يو" في العربية): يُنطق كـ "يو" مثل كلمة 
                                    <span class="english-word">blue</span> (أزرق),
                                    <span class="english-word">cute</span> (لطيف), 
                                    <span class="english-word">music</span> (موسيقى).
                                </li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="grammar-topic">
                <h3>2. الحروف الساكنة (Consonants)</h3>
                <div class="grammar-text">
                    <p>الحروف الساكنة في اللغة الإنجليزية لها أصوات محددة، ولكن بعضها قد يتغير نطقه بناءً على الحروف التي تليه أو موقعه في الكلمة. فهم هذه الاختلافات يساعد كثيرًا في تحسين النطق.</p>
                    <ul>
                        <li><strong>حرف C:</strong>
                            <ul>
                                <li>يُنطق كـ **"S"** عندما يتبعه أحد الحروف المتحركة 
                                    <span class="english-word">E</span>, 
                                    <span class="english-word">I</span>, 
                                    <span class="english-word">Y</span>: مثل 
                                    <span class="english-word">city</span> (مدينة), 
                                    <span class="english-word">face</span> (وجه), 
                                    <span class="english-word">cycle</span> (دورة).
                                </li>
                                <li>يُنطق كـ **"K"** في معظم الحالات الأخرى: مثل 
                                    <span class="english-word">cat</span> (قطة), 
                                    <span class="english-word">car</span> (سيارة), 
                                    <span class="english-word">cold</span> (بارد).
                                </li>
                            </ul>
                        </li>
                        <li>
                            <strong>حرف G:</strong>
                            <ul>
                                <li>يُنطق كـ **"J"** (مثل الجيم المصرية) عندما يتبعه أحد الحروف المتحركة 
                                    <span class="english-word">E</span>, 
                                    <span class="english-word">I</span>, 
                                    <span class="english-word">Y</span>: مثل 
                                    <span class="english-word">giant</span> (عملاق), 
                                    <span class="english-word">gem</span> (جوهرة),
                                    <span class="english-word">gym</span> (صالة ألعاب رياضية).
                                </li>
                                <li>يُنطق كـ "غ" (مثل الغين في العربية) في معظم الحالات الأخرى: مثل 
                                    <span class="english-word">go</span> (يذهب), 
                                    <span class="english-word">game</span> (لعبة), 
                                    <span class="english-word">green</span> (أخضر).
                                </li>
                            </ul>
                        </li>
                        <li>
                            <strong>حرف S:</strong>
                            <ul>
                                <li>يُنطق كـ **"س"** في بداية الكلمات أو عندما يكون الحرف الذي يليه ساكناً: مثل 
                                    <span class="english-word">sun</span> (شمس), 
                                    <span class="english-word">start</span> (يبدأ), 
                                    <span class="english-word">street</span> (شارع).
                                </li>
                                <li>يُنطق كـ **"ز"** أحياناً، خاصة بين حرفين متحركين أو في نهاية بعض الكلمات: مثل 
                                    <span class="english-word">is</span> (يكون), 
                                    <span class="english-word">rose</span> (وردة), 
                                    <span class="english-word">easy</span> (سهل).
                                </li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="grammar-topic">
                <h3>3. الحروف المركبة (Digraphs)</h3>
                <div class="grammar-text">
                    <p>الحروف المركبة هي زوج من الحروف التي تنتج صوتًا واحدًا. وهي شائعة جدًا في اللغة الإنجليزية.</p>
                    <ul>
                        <li><strong>CH:</strong> يُنطق كـ "تش" مثل 
                            <span class="english-word">chair</span> (كرسي), 
                            <span class="english-word">teacher</span> (معلم), 
                            <span class="english-word">watch</span> (ساعة يد/يشاهد).
                        </li>
                        <li><strong>SH:</strong> يُنطق كـ "ش" مثل 
                            <span class="english-word">ship</span> (سفينة), 
                            <span class="english-word">shop</span> (متجر), 
                            <span class="english-word">fish</span> (سمكة).
                        </li>
                        <li><strong>TH:</strong> له صوتان:
                            <ul>
                                <li>صوت مهموس (بدون اهتزاز الأحبال الصوتية) كـ "ث" مثل 
                                    <span class="english-word">three</span> (ثلاثة), 
                                    <span class="english-word">think</span> (يفكر), 
                                    <span class="english-word">bath</span> (حمام).
                                </li>
                                <li>صوت مجهور (مع اهتزاز الأحبال الصوتية) كـ "ذ" مثل 
                                    <span class="english-word">this</span> (هذا), 
                                    <span class="english-word">that</span> (ذلك), 
                                    <span class="english-word">mother</span> (أم).
                                </li>
                            </ul>
                        </li>
                        <li><strong>PH:</strong> يُنطق كـ "ف" مثل 
                            <span class="english-word">phone</span> (هاتف), 
                            <span class="english-word">photo</span> (صورة), 
                            <span class="english-word">elephant</span> (فيل).
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="numbers-section">
            <h2>الأعداد الأساسية (Numbers)</h2>
            <p class="section-intro">الأرقام جزء لا يتجزأ من المحادثات اليومية، من تحديد الوقت إلى التسوق. هذا الجدول يوضح لكم الأعداد الأساسية وكيفية كتابتها ونطقها باللغة الإنجليزية.</p>
            <div class="info-table-container">
                <table class="info-table">
                    <thead>
                        <tr>
                            <th>الرقم</th>
                            <th>الكلمة الإنجليزية</th>
                            <th>الترجمة العربية</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr><td>1</td><td class="english-word">One</td><td>واحد</td></tr>
                        <tr><td>2</td><td class="english-word">Two</td><td>اثنان</td></tr>
                        <tr><td>3</td><td class="english-word">Three</td><td>ثلاثة</td></tr>
                        <tr><td>4</td><td class="english-word">Four</td><td>أربعة</td></tr>
                        <tr><td>5</td><td class="english-word">Five</td><td>خمسة</td></tr>
                        <tr><td>6</td><td class="english-word">Six</td><td>ستة</td></tr>
                        <tr><td>7</td><td class="english-word">Seven</td><td>سبعة</td></tr>
                        <tr><td>8</td><td class="english-word">Eight</td><td>ثمانية</td></tr>
                        <tr><td>9</td><td class="english-word">Nine</td><td>تسعة</td></tr>
                        <tr><td>10</td><td class="english-word">Ten</td><td>عشرة</td></tr>
                        <tr><td>11</td><td class="english-word">Eleven</td><td>أحد عشر</td></tr>
                        <tr><td>12</td><td class="english-word">Twelve</td><td>اثنا عشر</td></tr>
                        <tr><td>13</td><td class="english-word">Thirteen</td><td>ثلاثة عشر</td></tr>
                        <tr><td>20</td><td class="english-word">Twenty</td><td>عشرون</td></tr>
                        <tr><td>30</td><td class="english-word">Thirty</td><td>ثلاثون</td></tr>
                        <tr><td>100</td><td class="english-word">One Hundred</td><td>مائة</td></tr>
                        <tr><td>1000</td><td class="english-word">One Thousand</td><td>ألف</td></tr>
                    </tbody>
                </table>
            </div>
            <div class="info-table-container" style="margin-top: 40px;">
                <h3>الأعداد الترتيبية (Ordinal Numbers)</h3>
                <table class="info-table">
                    <thead>
                        <tr>
                            <th>الترتيب</th>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                            <th>الترتيب</th>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>الأول</td>
                            <td><span class="english-word">First</span></td>
                            <td>أول</td>
                            <td>الحادي عشر</td>
                            <td><span class="english-word">Eleventh</span></td>
                            <td>حادي عشر</td>
                        </tr>
                        <tr>
                            <td>الثاني</td>
                            <td><span class="english-word">Second</span></td>
                            <td>ثاني</td>
                            <td>الثاني عشر</td>
                            <td><span class="english-word">Twelfth</span></td>
                            <td>ثاني عشر</td>
                        </tr>
                        <tr>
                            <td>الثالث</td>
                            <td><span class="english-word">Third</span></td>
                            <td>ثالث</td>
                            <td>العشرون</td>
                            <td><span class="english-word">Twentieth</span></td>
                            <td>عشرون</td>
                        </tr>
                        <tr>
                            <td>الرابع</td>
                            <td><span class="english-word">Fourth</span></td>
                            <td>رابع</td>
                            <td>المائة</td>
                            <td><span class="english-word">Hundredth</span></td>
                            <td>مائة</td>
                        </tr>
                        <tr>
                            <td>الخامس</td>
                            <td><span class="english-word">Fifth</span></td>
                            <td>خامس</td>
                            <td>الألف</td>
                            <td><span class="english-word">Thousandth</span></td>
                            <td>ألف</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <section id="colors-section">
            <h2>الألوان (Colors)</h2>
            <p class="section-intro">تستخدم الألوان لوصف كل شيء حولنا. تعلم أسماء الألوان الشائعة باللغة الإنجليزية سيساعدك على التعبير عن نفسك بشكل أفضل وأكثر دقة.</p>
            <div class="info-table-container">
                <table class="info-table">
                    <thead>
                        <tr>
                            <th>اللون</th>
                            <th>الكلمة الإنجليزية</th>
                            <th>الترجمة العربية</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr><td><span class="color-box" style="background-color: red;"></span></td><td class="english-word">Red</td><td>أحمر</td></tr>
                        <tr><td><span class="color-box" style="background-color: blue;"></span></td><td class="english-word">Blue</td><td>أزرق</td></tr>
                        <tr><td><span class="color-box" style="background-color: green;"></span></td><td class="english-word">Green</td><td>أخضر</td></tr>
                        <tr><td><span class="color-box" style="background-color: yellow;"></span></td><td class="english-word">Yellow</td><td>أصفر</td></tr>
                        <tr><td><span class="color-box" style="background-color: black;"></span></td><td class="english-word">Black</td><td>أسود</td></tr>
                        <tr><td><span class="color-box" style="background-color: white;"></span></td><td class="english-word">White</td><td>أبيض</td></tr>
                        <tr><td><span class="color-box" style="background-color: orange;"></span></td><td class="english-word">Orange</td><td>برتقالي</td></tr>
                        <tr><td><span class="color-box" style="background-color: purple;"></span></td><td class="english-word">Purple</td><td>بنفسجي</td></tr>
                        <tr><td><span class="color-box" style="background-color: brown;"></span></td><td class="english-word">Brown</td><td>بني</td></tr>
                        <tr><td><span class="color-box" style="background-color: pink;"></span></td><td class="english-word">Pink</td><td>وردي</td></tr>
                        <tr><td><span class="color-box" style="background-color: grey;"></span></td><td class="english-word">Gray</td><td>رمادي</td></tr>
                    </tbody>
                </table>
            </div>
        </section>

        <section id="grammar-section">
          
                                                                        <h2>شرح القواعد الأساسية في اللغة الإنجليزية</h2>
            
            <div class="grammar-topic">
                <h3>1. الأفعال (Verbs)</h3>
                <div class="grammar-text">
                    <p>الفعل هو كلمة تُعبر عن حدث أو حالة أو وجود، وهو العنصر الأساسي في أي جملة إنجليزية. تنقسم الأفعال إلى نوعين رئيسيين: الأفعال الأساسية (Main Verbs) والأفعال المساعدة (Auxiliary Verbs).</p>
                    
                    <h4>أ. الأفعال الأساسية (Main Verbs)</h4>
                    <p>هي الأفعال التي تحمل المعنى الرئيسي للجملة وتصف الحدث أو الحالة. يمكن أن تكون هذه الأفعال منتظمة (Regular) أو غير منتظمة (Irregular).</p>
                    <ul>
                        <li><strong>أمثلة:</strong>
                            <ul>
                                <li>He <span class="english-word">eats</span> an apple every day. (يأكل تفاحة كل يوم.)</li>
                                <li>She <span class="english-word">works</span> in a big office. (هي تعمل في مكتب كبير.)</li>
                                <li>They <span class="english-word">play</span> football on weekends. (هم يلعبون كرة القدم في عطلات نهاية الأسبوع.)</li>
                                <li>I <span class="english-word">read</span> a book last night. (قرأت كتابًا الليلة الماضية.)</li>
                                <li>We <span class="english-word">travel</span> to new countries. (نسافر إلى بلدان جديدة.)</li>
                            </ul>
                        </li>
                    </ul>

                    <h4>ب. الأفعال المساعدة (Auxiliary Verbs)</h4>
                    <p>هي أفعال تُستخدم مع الأفعال الرئيسية لتكوين الأزمنة المختلفة، السؤال، النفي، والتعبير عن الإمكانية، الوجوب، أو القدرة. لا تحمل معنى رئيسيًا بمفردها.</p>
                    <ul>
                        <li><strong>Be (يكون):</strong> يُستخدم لتكوين الأزمنة المستمرة والمبني للمجهول.
                            <ul>
                                <li>أشكاله: <span class="english-word">am</span>, <span class="english-word">is</span>, <span class="english-word">are</span> (في المضارع), <span class="english-word">was</span>, <span class="english-word">were</span> (في الماضي).</li>
                                <li><strong>أمثلة:</strong>
                                    <ul>
                                        <li>I <span class="english-word">am</span> learning English. (أنا أتعلم الإنجليزية.)</li>
                                        <li>She <span class="english-word">is</span> singing a beautiful song. (هي تغني أغنية جميلة.)</li>
                                        <li>They <span class="english-word">are</span> playing in the park. (هم يلعبون في الحديقة.)</li>
                                        <li>He <span class="english-word">was</span> studying all night. (كان يدرس طوال الليل.)</li>
                                        <li>We <span class="english-word">were</span> watching a movie. (كنا نشاهد فيلمًا.)</li>
                                    </ul>
                                </li>
                            </ul>
                        </li>
                        <li><strong>Do (يفعل):</strong> يُستخدم في صياغة النفي والسؤال في الأزمنة البسيطة وللتأكيد.
                            <ul>
                                <li>أشكاله: <span class="english-word">do</span>, <span class="english-word">does</span> (في المضارع), <span class="english-word">did</span> (في الماضي).</li>
                                <li><strong>أمثلة:</strong>
                                    <ul>
                                        <li><span class="english-word">Do</span> you like coffee? (هل تحب القهوة؟)</li>
                                        <li>She <span class="english-word">does</span> not speak French. (هي لا تتحدث الفرنسية.)</li>
                                        <li>They <span class="english-word">did</span> not go to the party. (هم لم يذهبوا إلى الحفلة.)</li>
                                        <li>I <span class="english-word">do</span> believe in you. (أنا أؤمن بك حقًا.)</li>
                                        <li>What <span class="english-word">did</span> he say? (ماذا قال؟)</li>
                                    </ul>
                                </li>
                            </ul>
                        </li>
                        <li><strong>Have (يملك):</strong> يُستخدم لتكوين الأزمنة التامة.
                            <ul>
                                <li>أشكاله: <span class="english-word">have</span>, <span class="english-word">has</span> (في المضارع), <span class="english-word">had</span> (في الماضي).</li>
                                <li><strong>أمثلة:</strong>
                                    <ul>
                                        <li>I <span class="english-word">have</span> finished my homework. (لقد أنهيت واجبي.)</li>
                                        <li>He <span class="english-word">has</span> lived here for five years. (لقد عاش هنا لخمس سنوات.)</li>
                                        <li>They <span class="english-word">had</span> already left when I arrived. (كانوا قد غادروا بالفعل عندما وصلت.)</li>
                                        <li>We <span class="english-word">have</span> seen that movie before. (لقد رأينا هذا الفيلم من قبل.)</li>
                                        <li>She <span class="english-word">has</span> visited many countries. (لقد زارت العديد من البلدان.)</li>
                                    </ul>
                                </li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="grammar-topic">
                <h3>2. الضمائر (Pronouns)</h3>
                <div class="grammar-text">
                    <p>الضمائر هي كلمات تحل محل الأسماء لتجنب تكرارها وجعل الجمل أكثر سلاسة. تُقسم إلى عدة أنواع:</p>
                    
                    <h4>أ. ضمائر الفاعل (Subject Pronouns)</h4>
                    <p>تُستخدم كفاعل للفعل في الجملة، أي من يقوم بالفعل.</p>
                    <ul>
                        <li><span class="english-word">I</span> (أنا)</li>
                        <li><span class="english-word">You</span> (أنت / أنتم)</li>
                        <li><span class="english-word">He</span> (هو - للمذكر العاقل)</li>
                        <li><span class="english-word">She</span> (هي - للمؤنث العاقل)</li>
                        <li><span class="english-word">It</span> (هو / هي - لغير العاقل والمفرد)</li>
                        <li><span class="english-word">We</span> (نحن)</li>
                        <li><span class="english-word">They</span> (هم / هن - للجمع عاقل وغير عاقل)</li>
                    </ul>
                    <ul>
                        <li><strong>أمثلة:</strong>
                            <ul>
                                <li><span class="english-word">I</span> am a student. (أنا طالب.)</li>
                                <li><span class="english-word">She</span> loves to read books. (هي تحب قراءة الكتب.)</li>
                                <li><span class="english-word">They</span> went to the cinema yesterday. (هم ذهبوا إلى السينما أمس.)</li>
                                <li><span class="english-word">It</span> is raining outside. (إنها تمطر في الخارج.)</li>
                                <li><span class="english-word">We</span> are going to the beach. (نحن ذاهبون إلى الشاطئ.)</li>
                            </ul>
                        </li>
                    </ul>

                    <h4>ب. ضمائر المفعول به (Object Pronouns)</h4>
                    <p>تُستخدم كـمفعول به للفعل أو بعد حروف الجر، أي من يقع عليه الفعل.</p>
                    <ul>
                        <li><span class="english-word">Me</span> (لي / إياي)</li>
                        <li><span class="english-word">You</span> (لك / إياك)</li>
                        <li><span class="english-word">Him</span> (له / إياه)</li>
                        <li><span class="english-word">Her</span> (لها / إياها)</li>
                        <li><span class="english-word">It</span> (له / لها - لغير العاقل)</li>
                        <li><span class="english-word">Us</span> (لنا / إيانا)</li>
                        <li><span class="english-word">Them</span> (لهم / إياهم)</li>
                    </ul>
                    <ul>
                        <li><strong>أمثلة:</strong>
                            <ul>
                                <li>He saw <span class="english-word">me</span> at the store. (رآني في المتجر.)</li>
                                <li>I will call <span class="english-word">you</span> later. (سأتصل بك لاحقًا.)</li>
                                <li>She gave the book to <span class="english-word">him</span>. (هي أعطت الكتاب له.)</li>
                                <li>Please help <span class="english-word">her</span> with the bags. (من فضلك ساعدها في الحقائب.)</li>
                                <li>The dog chased <span class="english-word">it</span>. (الكلب طاردها.)</li>
                            </ul>
                        </li>
                    </ul>

                    <h4>ج. صفات الملكية (Possessive Adjectives)</h4>
                    <p>تُستخدم لوصف اسم وتُشير إلى الملكية. تأتي دائمًا قبل الاسم الذي تصفه.</p>
                    <ul>
                        <li><span class="english-word">My</span> (لي / خاصتي)</li>
                        <li><span class="english-word">Your</span> (لك / خاصتك)</li>
                        <li><span class="english-word">His</span> (له / خاصته)</li>
                        <li><span class="english-word">Her</span> (لها / خاصتها)</li>
                        <li><span class="english-word">Its</span> (له / لها - لغير العاقل)</li>
                        <li><span class="english-word">Our</span> (لنا / خاصتنا)</li>
                        <li><span class="english-word">Their</span> (لهم / خاصتهم)</li>
                    </ul>
                    <ul>
                        <li><strong>أمثلة:</strong>
                            <ul>
                                <li>This is <span class="english-word">my</span> car. (هذه سيارتي.)</li>
                                <li>Is that <span class="english-word">your</span> phone? (هل هذا هاتفك؟)</li>
                                <li>He lost <span class="english-word">his</span> keys. (لقد فقد مفاتيحه.)</li>
                                <li>She loves <span class="english-word">her</span> new dress. (هي تحب فستانها الجديد.)</li>
                                <li>The cat is playing with <span class="english-word">its</span> toy. (القط يلعب بلعبته.)</li>
                            </ul>
                        </li>
                    </ul>

                    <h4>د. ضمائر الملكية (Possessive Pronouns)</h4>
                    <p>تحل محل صفة الملكية والاسم الذي تصفه لتجنب التكرار. لا تأتي قبل اسم.</p>
                    <ul>
                        <li><span class="english-word">Mine</span> (ملكي)</li>
                        <li><span class="english-word">Yours</span> (ملكك / ملككم)</li>
                        <li><span class="english-word">His</span> (ملكه)</li>
                        <li><span class="english-word">Hers</span> (ملكها)</li>
                        <li><span class="english-word">Its</span> (ملكه / ملكها - لغير العاقل)</li>
                        <li><span class="english-word">Ours</span> (ملكنا)</li>
                        <li><span class="english-word">Theirs</span> (ملكهم)</li>
                    </ul>
                    <ul>
                        <li><strong>أمثلة:</strong>
                            <ul>
                                <li>This book is <span class="english-word">mine</span>. (هذا الكتاب ملكي.)</li>
                                <li>That car is <span class="english-word">yours</span>. (تلك السيارة ملكك.)</li>
                                <li>The blue umbrella is <span class="english-word">his</span>. (المظلة الزرقاء ملكه.)</li>
                                <li>The idea was <span class="english-word">hers</span>. (الفكرة كانت ملكها.)</li>
                                <li>The responsibility is <span class="english-word">ours</span>. (المسؤولية ملكنا.)</li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="grammar-topic">
                <h3>3. الصفات (Adjectives)</h3>
                <div class="grammar-text">
                    <p>الصفات هي كلمات تصف الأسماء أو الضمائر، وتُعطي معلومات إضافية عنها مثل الحجم، اللون، الشكل، الكمية، أو الجودة. تأتي الصفات عادةً قبل الاسم الذي تصفه أو بعد أفعال الربط (مثل <span class="english-word">be</span>, <span class="english-word">feel</span>, <span class="english-word">seem</span>).</p>
                    <ul>
                        <li><strong>أمثلة:</strong>
                            <ul>
                                <li>She has a <span class="english-word">beautiful</span> dress. (لديها فستان جميل.)</li>
                                <li>He is a <span class="english-word">tall</span> man. (هو رجل طويل.)</li>
                                <li>The weather is <span class="english-word">cold</span> today. (الطقس بارد اليوم.)</li>
                                <li>I saw a <span class="english-word">red</span> car. (رأيت سيارة حمراء.)</li>
                                <li>This is an <span class="english-word">interesting</span> story. (هذه قصة مثيرة للاهتمام.)</li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
        </section>
       <section id="tenses-section">
    <h2>الأزمنة في اللغة الإنجليزية (Tenses)</h2>
    <p class="instruction">اضغط على أي عنوان زمن أو كلمة إنجليزية لسماع نطقها.</p>

    <div class="grammar-topic">
        <h3>1. زمن المضارع البسيط (Present Simple)</h3>
        <div class="grammar-text">
            <p>يُستخدم زمن المضارع البسيط للتعبير عن الحقائق العامة، العادات والروتين اليومي، والجداول الزمنية الثابتة. يُعد من أبسط الأزمنة وأكثرها شيوعًا.</p>
            
            <h4>أ. الاستخدامات:</h4>
            <ul>
                <li><strong>الحقائق العامة والحقائق العلمية:</strong> أشياء صحيحة دائمًا.
                    <ul>
                        <li>The sun <span class="english-word">rises</span> in the east. (الشمس تشرق من الشرق.)</li>
                        <li>Water <span class="english-word">boils</span> at 100 degrees Celsius. (الماء يغلي عند 100 درجة مئوية.)</li>
                    </ul>
                </li>
                <li><strong>العادات والروتين اليومي:</strong> أفعال تتكرر بانتظام.
                    <ul>
                        <li>I <span class="english-word">drink</span> coffee every morning. (أنا أشرب القهوة كل صباح.)</li>
                        <li>She <span class="english-word">goes</span> to school by bus. (هي تذهب إلى المدرسة بالحافلة.)</li>
                    </ul>
                </li>
                <li><strong>الجداول الزمنية الثابتة:</strong> مثل مواعيد القطارات أو الحصص.
                    <ul>
                        <li>The train <span class="english-word">leaves</span> at 7 PM. (القطار يغادر في الساعة 7 مساءً.)</li>
                        <li>The movie <span class="english-word">starts</span> at 9 o'clock. (الفيلم يبدأ في الساعة 9.)</li>
                    </ul>
                </li>
                <li><strong>وصف حالة ثابتة أو مشاعر دائمة:</strong>
                    <ul>
                        <li>He <span class="english-word">lives</span> in Cairo. (هو يعيش في القاهرة.)</li>
                        <li>She <span class="english-word">loves</span> chocolate. (هي تحب الشوكولاتة.)</li>
                    </ul>
                </li>
            </ul>

            <h4>ب. الكلمات الدالة (Keywords):</h4>
            <ul>
                <li><span class="english-word">Always</span> (دائماً)</li>
                <li><span class="english-word">Usually</span> (عادةً)</li>
                <li><span class="english-word">Often</span> (غالباً)</li>
                <li><span class="english-word">Sometimes</span> (أحياناً)</li>
                <li><span class="english-word">Seldom</span> (نادراً)</li>
                <li><span class="english-word">Never</span> (أبداً)</li>
                <li><span class="english-word">Every day/week/year</span> (كل يوم/أسبوع/سنة)</li>
                <li><span class="english-word">On Mondays/weekends</span> (في أيام الاثنين/عطلات نهاية الأسبوع)</li>
            </ul>

            <h4>ج. التكوين (Formation):</h4>
            <ul>
                <li><strong>الفاعل (I, You, We, They) + الفعل في صورته الأساسية (Base Form):</strong>
                    <ul>
                        <li>I <span class="english-word">play</span> football.</li>
                        <li>We <span class="english-word">study</span> English.</li>
                    </ul>
                </li>
                <li><strong>الفاعل (He, She, It) + الفعل + s/es/ies:</strong>
                    <ul>
                        <li>He <span class="english-word">plays</span> football.</li>
                        <li>She <span class="english-word">studies</span> English.</li>
                    </ul>
                </li>
            </ul>

            <h4>د. أمثلة (10 Examples):</h4>
            <ol>
                <li>I <span class="english-word">wake up</span> at 7 AM every day. (أستيقظ في السابعة صباحاً كل يوم.)</li>
                <li>She <span class="english-word">reads</span> a book before bed. (هي تقرأ كتاباً قبل النوم.)</li>
                <li>They <span class="english-word">work</span> in a big company. (هم يعملون في شركة كبيرة.)</li>
                <li>He <span class="english-word">drinks</span> tea in the morning. (هو يشرب الشاي في الصباح.)</li>
                <li>We <span class="english-word">go</span> to the gym twice a week. (نحن نذهب إلى النادي مرتين في الأسبوع.)</li>
                <li>The store <span class="english-word">opens</span> at 9 AM. (المتجر يفتح في التاسعة صباحاً.)</li>
                <li>Cats <span class="english-word">love</span> milk. (القطط تحب الحليب.)</li>
                <li>It <span class="english-word">rains</span> a lot in winter. (تمطر كثيراً في الشتاء.)</li>
                <li>You always <span class="english-word">help</span> me. (أنت دائماً تساعدني.)</li>
                <li>My parents <span class="english-word">live</span> in a small town. (والداي يعيشان في بلدة صغيرة.)</li>
            </ol>

            <h4>هـ. السؤال والنفي (Questions and Negation):</h4>
            <ul>
                <li><strong>للسؤال:</strong> نستخدم <span class="english-word">Do</span> أو <span class="english-word">Does</span> في بداية الجملة.
                    <ul>
                        <li><span class="english-word">Do</span> I/you/we/they + الفعل في صورته الأساسية ...?
                            <ul>
                                <li><span class="english-word">Do</span> you like pizza? (هل تحب البيتزا؟)</li>
                                <li><span class="english-word">Do</span> they play tennis? (هل يلعبون التنس؟)</li>
                            </ul>
                        </li>
                        <li><span class="english-word">Does</span> he/she/it + الفعل في صورته الأساسية ...?
                            <ul>
                                <li><span class="english-word">Does</span> she speak Spanish? (هل تتحدث الإسبانية؟)</li>
                                <li><span class="english-word">Does</span> it work? (هل يعمل؟)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للنفي:</strong> نستخدم <span class="english-word">don't</span> (<span class="english-word">do not</span>) أو <span class="english-word">doesn't</span> (<span class="english-word">does not</span>) قبل الفعل.
                    <ul>
                        <li>I/You/We/They <span class="english-word">don't</span> + الفعل في صورته الأساسية.
                            <ul>
                                <li>I <span class="english-word">don't</span> understand. (أنا لا أفهم.)</li>
                                <li>They <span class="english-word">don't</span> live here. (هم لا يعيشون هنا.)</li>
                            </ul>
                        </li>
                        <li>He/She/It <span class="english-word">doesn't</span> + الفعل في صورته الأساسية.
                            <ul>
                                <li>She <span class="english-word">doesn't</span> like coffee. (هي لا تحب القهوة.)</li>
                                <li>He <span class="english-word">doesn't</span> watch TV. (هو لا يشاهد التلفاز.)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>

    <div class="grammar-topic">
        <h3>2. زمن المضارع المستمر (Present Continuous)</h3>
        <div class="grammar-text">
            <p>يُستخدم زمن المضارع المستمر للتعبير عن أفعال تحدث الآن في لحظة الكلام، أو في فترة زمنية مؤقتة حول الوقت الحاضر، أو لترتيبات مستقبلية مؤكدة.</p>
            
            <h4>أ. الاستخدامات:</h4>
            <ul>
                <li><strong>أفعال تحدث الآن:</strong> النشاطات التي تجري في هذه اللحظة.
                    <ul>
                        <li>I <span class="english-word">am writing</span> an email right now. (أنا أكتب بريداً إلكترونياً الآن.)</li>
                        <li>She <span class="english-word">is cooking</span> dinner. (هي تطهو العشاء.)</li>
                    </ul>
                </li>
                <li><strong>أفعال مؤقتة:</strong> نشاطات تحدث في فترة مؤقتة وليست دائمة.
                    <ul>
                        <li>He <span class="english-word">is studying</span> for his exams this week. (هو يدرس لامتحاناته هذا الأسبوع.)</li>
                        <li>They <span class="english-word">are living</span> in a rented apartment. (هم يعيشون في شقة مستأجرة.)</li>
                    </ul>
                </li>
                <li><strong>ترتيبات مستقبلية مؤكدة:</strong> أحداث مخططة ومؤكدة في المستقبل القريب.
                    <ul>
                        <li>We <span class="english-word">are meeting</span> Sarah tomorrow. (سنقابل سارة غداً.)</li>
                        <li>The bus <span class="english-word">is arriving</span> in ten minutes. (الحافلة ستصل خلال عشر دقائق.)</li>
                    </ul>
                </li>
                <li><strong>التعبير عن الانزعاج من عادة متكررة (مع Always):</strong>
                    <ul>
                        <li>He <span class="english-word">is always complaining</span>. (هو دائم الشكوى.)</li>
                    </ul>
                </li>
            </ul>

            <h4>ب. الكلمات الدالة (Keywords):</h4>
            <ul>
                <li><span class="english-word">Now</span> (الآن)</li>
                <li><span class="english-word">Right now</span> (في هذه اللحظة بالضبط)</li>
                <li><span class="english-word">At the moment</span> (في هذه اللحظة)</li>
                <li><span class="english-word">Look!</span> (انظر!)</li>
                <li><span class="english-word">Listen!</span> (استمع!)</li>
                <li><span class="english-word">Currently</span> (حالياً)</li>
                <li><span class="english-word">Today</span> (اليوم)</li>
                <li><span class="english-word">This week/month/year</span> (هذا الأسبوع/الشهر/العام)</li>
            </ul>

            <h4>ج. التكوين (Formation):</h4>
            <ul>
                <li><strong>الفاعل + فعل <span class="english-word">be</span> (am/is/are) + الفعل + ing (Present Participle):</strong>
                    <ul>
                        <li>I <span class="english-word">am working</span>.</li>
                        <li>She <span class="english-word">is singing</span>.</li>
                        <li>They <span class="english-word">are playing</span>.</li>
                    </ul>
                </li>
            </ul>

            <h4>د. أمثلة (10 Examples):</h4>
            <ol>
                <li>I <span class="english-word">am watching</span> a movie now. (أنا أشاهد فيلماً الآن.)</li>
                <li>She <span class="english-word">is studying</span> English at the university. (هي تدرس الإنجليزية في الجامعة.)</li>
                <li>They <span class="english-word">are playing</span> football in the park. (هم يلعبون كرة القدم في الحديقة.)</li>
                <li>He <span class="english-word">is having</span> dinner with his family. (هو يتناول العشاء مع عائلته.)</li>
                <li>We <span class="english-word">are listening</span> to music. (نحن نستمع إلى الموسيقى.)</li>
                <li>The birds <span class="english-word">are singing</span> outside. (الطيور تغرد في الخارج.)</li>
                <li>Look! It <span class="english-word">is snowing</span>. (انظر! إنها تمطر ثلجاً.)</li>
                <li>My brother <span class="english-word">is learning</span> to drive. (أخي يتعلم القيادة.)</li>
                <li>You <span class="english-word">are wearing</span> a beautiful dress. (أنت ترتدين فستاناً جميلاً.)</li>
                <li>They <span class="english-word">are building</span> a new house. (هم يبنون منزلاً جديداً.)</li>
            </ol>

            <h4>هـ. السؤال والنفي (Questions and Negation):</h4>
            <ul>
                <li><strong>للسؤال:</strong> نضع فعل <span class="english-word">be</span> (am/is/are) قبل الفاعل.
                    <ul>
                        <li><span class="english-word">Am</span> I + الفعل + ing ...?</li>
                        <li><span class="english-word">Is</span> he/she/it + الفعل + ing ...?
                            <ul>
                                <li><span class="english-word">Is</span> she working? (هل هي تعمل؟)</li>
                            </ul>
                        </li>
                        <li><span class="english-word">Are</span> you/we/they + الفعل + ing ...?
                            <ul>
                                <li><span class="english-word">Are</span> you listening? (هل أنت تستمع؟)</li>
                                <li><span class="english-word">Are</span> they coming? (هل هم قادمون؟)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للنفي:</strong> نضع <span class="english-word">not</span> بعد فعل <span class="english-word">be</span> (am/is/are).
                    <ul>
                        <li>I <span class="english-word">am not</span> + الفعل + ing.
                            <ul>
                                <li>I <span class="english-word">am not</span> sleeping. (أنا لا أنام.)</li>
                            </ul>
                        </li>
                        <li>He/She/It <span class="english-word">is not</span> (isn't) + الفعل + ing.
                            <ul>
                                <li>She <span class="english-word">isn't</span> studying. (هي لا تدرس.)</li>
                            </ul>
                        </li>
                        <li>You/We/They <span class="english-word">are not</span> (aren't) + الفعل + ing.
                            <ul>
                                <li>We <span class="english-word">aren't</span> playing. (نحن لا نلعب.)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>

    <div class="grammar-topic">
        <h3>3. زمن الماضي البسيط (Past Simple)</h3>
        <div class="grammar-text">
            <p>يُستخدم زمن الماضي البسيط للتعبير عن أفعال أو أحداث اكتملت في وقت محدد في الماضي. من المهم معرفة الأفعال المنتظمة (Regular Verbs) والأفعال غير المنتظمة (Irregular Verbs) في هذا الزمن.</p>
            
            <h4>أ. الاستخدامات:</h4>
            <ul>
                <li><strong>أحداث مكتملة في الماضي:</strong>
                    <ul>
                        <li>I <span class="english-word">visited</span> Paris last year. (زرت باريس العام الماضي.)</li>
                        <li>She <span class="english-word">finished</span> her homework an hour ago. (هي أنهت واجبها قبل ساعة.)</li>
                    </ul>
                </li>
                <li><strong>سلسلة من الأحداث في الماضي:</strong>
                    <ul>
                        <li>He <span class="english-word">woke up</span>, <span class="english-word">ate</span> breakfast, and <span class="english-word">went</span> to work. (استيقظ، تناول الفطور، وذهب إلى العمل.)</li>
                    </ul>
                </li>
                <li><strong>عادات في الماضي (لم تعد تحدث الآن):</strong>
                    <ul>
                        <li>When I was a child, I often <span class="english-word">played</span> in the park. (عندما كنت طفلاً، كنت ألعب غالباً في الحديقة.)</li>
                    </ul>
                </li>
            </ul>

            <h4>ب. الكلمات الدالة (Keywords):</h4>
            <ul>
                <li><span class="english-word">Yesterday</span> (أمس)</li>
                <li><span class="english-word">Last night/week/month/year</span> (الليلة/الأسبوع/الشهر/السنة الماضية)</li>
                <li><span class="english-word">Ago</span> (منذ) - (e.g., two days <span class="english-word">ago</span>)</li>
                <li><span class="english-word">In 2010</span> (في عام 2010) - أي تاريخ محدد في الماضي</li>
                <li><span class="english-word">When I was young</span> (عندما كنت صغيراً)</li>
            </ul>

            <h4>ج. التكوين (Formation):</h4>
            <ul>
                <li><strong>للأفعال المنتظمة (Regular Verbs):</strong> نضيف <span class="english-word">-ed</span> إلى نهاية الفعل.
                    <ul>
                        <li><span class="english-word">Play</span> &rarr; <span class="english-word">Played</span></li>
                        <li><span class="english-word">Work</span> &rarr; <span class="english-word">Worked</span></li>
                        <li><span class="english-word">Visit</span> &rarr; <span class="english-word">Visited</span></li>
                    </ul>
                </li>
                <li><strong>للأفعال غير المنتظمة (Irregular Verbs):</strong> تتغير صيغة الفعل بالكامل (يجب حفظها).
                    <ul>
                        <li><span class="english-word">Go</span> &rarr; <span class="english-word">Went</span></li>
                        <li><span class="english-word">Eat</span> &rarr; <span class="english-word">Ate</span></li>
                        <li><span class="english-word">See</span> &rarr; <span class="english-word">Saw</span></li>
                    </ul>
                </li>
            </ul>

            <h4>د. أمثلة (10 Examples):</h4>
            <ol>
                <li>I <span class="english-word">watched</span> a great movie yesterday. (شاهدت فيلماً رائعاً أمس.)</li>
                <li>She <span class="english-word">went</span> to London last summer. (هي ذهبت إلى لندن الصيف الماضي.)</li>
                <li>They <span class="english-word">ate</span> pizza for dinner. (هم أكلوا بيتزا للعشاء.)</li>
                <li>He <span class="english-word">played</span> football when he was a child. (هو لعب كرة القدم عندما كان طفلاً.)</li>
                <li>We <span class="english-word">visited</span> our grandparents last weekend. (زرنا أجدادنا عطلة نهاية الأسبوع الماضية.)</li>
                <li>The class <span class="english-word">started</span> at 8 AM. (بدأت الحصة في الساعة 8 صباحاً.)</li>
                <li>She <span class="english-word">bought</span> a new car. (هي اشترت سيارة جديدة.)</li>
                <li>I <span class="english-word">saw</span> him at the supermarket. (رأيته في السوبر ماركت.)</li>
                <li>They <span class="english-word">finished</span> the project on time. (هم أنهوا المشروع في الوقت المحدد.)</li>
                <li>The birds <span class="english-word">flew</span> south for the winter. (الطيور طارت جنوباً للشتاء.)</li>
            </ol>

            <h4>هـ. السؤال والنفي (Questions and Negation):</h4>
            <ul>
                <li><strong>للسؤال:</strong> نستخدم <span class="english-word">Did</span> في بداية الجملة لجميع الفاعلين، ونعيد الفعل إلى صورته الأساسية.
                    <ul>
                        <li><span class="english-word">Did</span> + الفاعل + الفعل في صورته الأساسية ...?
                            <ul>
                                <li><span class="english-word">Did</span> you go to the party? (هل ذهبت إلى الحفلة؟)</li>
                                <li><span class="english-word">Did</span> she call you? (هل اتصلت بك؟)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للنفي:</strong> نستخدم <span class="english-word">didn't</span> (<span class="english-word">did not</span>) قبل الفعل، ونعيد الفعل إلى صورته الأساسية.
                    <ul>
                        <li>الفاعل + <span class="english-word">didn't</span> + الفعل في صورته الأساسية.
                            <ul>
                                <li>I <span class="english-word">didn't</span> like the movie. (لم أحب الفيلم.)</li>
                                <li>They <span class="english-word">didn't</span> come to school yesterday. (هم لم يأتوا إلى المدرسة أمس.)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>

    <div class="grammar-topic">
        <h3>4. زمن الماضي المستمر (Past Continuous)</h3>
        <div class="grammar-text">
            <p>يُستخدم زمن الماضي المستمر للتعبير عن فعل كان مستمراً في نقطة معينة في الماضي، أو فعلين كانا يحدثان في نفس الوقت في الماضي، أو فعل كان مستمراً وقطعه فعل آخر.</p>
            
            <h4>أ. الاستخدامات:</h4>
            <ul>
                <li><strong>فعل كان مستمراً في نقطة معينة في الماضي:</strong>
                    <ul>
                        <li>At 8 AM, I <span class="english-word">was having</span> breakfast. (في الساعة الثامنة صباحاً، كنت أتناول الفطور.)</li>
                        <li>What <span class="english-word">were you doing</span> yesterday evening? (ماذا كنت تفعل مساء أمس؟)</li>
                    </ul>
                </li>
                <li><strong>فعلان مستمران في نفس الوقت في الماضي:</strong>
                    <ul>
                        <li>While I <span class="english-word">was reading</span>, my sister <span class="english-word">was watching</span> TV. (بينما كنت أقرأ، كانت أختي تشاهد التلفاز.)</li>
                    </ul>
                </li>
                <li><strong>فعل مستمر في الماضي قطعه فعل آخر (عادة ماضي بسيط):</strong>
                    <ul>
                        <li>I <span class="english-word">was sleeping</span> when the phone <span class="english-word">rang</span>. (كنت نائماً عندما رن الهاتف.)</li>
                        <li>She <span class="english-word">was walking</span> home when she <span class="english-word">saw</span> an accident. (كانت تمشي إلى المنزل عندما رأت حادثاً.)</li>
                    </ul>
                </li>
            </ul>

            <h4>ب. الكلمات الدالة (Keywords):</h4>
            <ul>
                <li><span class="english-word">While</span> (بينما)</li>
                <li><span class="english-word">When</span> (عندما)</li>
                <li><span class="english-word">As</span> (بينما/حينما)</li>
                <li><span class="english-word">At that time</span> (في ذلك الوقت)</li>
                <li><span class="english-word">All day yesterday</span> (طوال يوم أمس)</li>
            </ul>

            <h4>ج. التكوين (Formation):</h4>
            <ul>
                <li><strong>الفاعل + فعل <span class="english-word">be</span> في الماضي (was/were) + الفعل + ing (Present Participle):</strong>
                    <ul>
                        <li>I/He/She/It <span class="english-word">was working</span>.</li>
                        <li>You/We/They <span class="english-word">were playing</span>.</li>
                    </ul>
                </li>
            </ul>

            <h4>د. أمثلة (10 Examples):</h4>
            <ol>
                <li>I <span class="english-word">was studying</span> when you called me. (كنت أدرس عندما اتصلت بي.)</li>
                <li>She <span class="english-word">was cooking</span> dinner while he <span class="english-word">was watching</span> TV. (كانت تطهو العشاء بينما هو يشاهد التلفاز.)</li>
                <li>They <span class="english-word">were playing</span> outside when it started to rain. (كانوا يلعبون في الخارج عندما بدأت تمطر.)</li>
                <li>At 6 PM yesterday, I <span class="english-word">was driving</span> home. (في الساعة 6 مساءً أمس، كنت أقود السيارة إلى المنزل.)</li>
                <li>He <span class="english-word">was reading</span> a book all morning. (هو كان يقرأ كتاباً طوال الصباح.)</li>
                <li>We <span class="english-word">were talking</span> about our plans. (كنا نتحدث عن خططنا.)</li>
                <li>The students <span class="english-word">were listening</span> to the teacher. (الطلاب كانوا يستمعون إلى المعلم.)</li>
                <li>What <span class="english-word">were you doing</span> at midnight? (ماذا كنت تفعل في منتصف الليل؟)</li>
                <li>She <span class="english-word">was waiting</span> for the bus. (كانت تنتظر الحافلة.)</li>
                <li>The children <span class="english-word">were laughing</span> loudly. (الأطفال كانوا يضحكون بصوت عالٍ.)</li>
            </ol>

            <h4>هـ. السؤال والنفي (Questions and Negation):</h4>
            <ul>
                <li><strong>للسؤال:</strong> نضع فعل <span class="english-word">be</span> في الماضي (was/were) قبل الفاعل.
                    <ul>
                        <li><span class="english-word">Was</span> I/he/she/it + الفعل + ing ...?
                            <ul>
                                <li><span class="english-word">Was</span> she crying? (هل كانت تبكي؟)</li>
                            </ul>
                        </li>
                        <li><span class="english-word">Were</span> you/we/they + الفعل + ing ...?
                            <ul>
                                <li><span class="english-word">Were</span> you sleeping? (هل كنت نائماً؟)</li>
                                <li><span class="english-word">Were</span> they working? (هل كانوا يعملون؟)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للنفي:</strong> نضع <span class="english-word">not</span> بعد فعل <span class="english-word">be</span> في الماضي (was/were).
                    <ul>
                        <li>I/He/She/It <span class="english-word">was not</span> (wasn't) + الفعل + ing.
                            <ul>
                                <li>He <span class="english-word">wasn't</span> listening. (هو لم يكن يستمع.)</li>
                            </ul>
                        </li>
                        <li>You/We/They <span class="english-word">were not</span> (weren't) + الفعل + ing.
                            <ul>
                                <li>We <span class="english-word">weren't</span> expecting you. (لم نكن نتوقع قدومك.)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>

    <div class="grammar-topic">
        <h3>5. زمن المستقبل البسيط (Future Simple)</h3>
        <div class="grammar-text">
            <p>يُستخدم زمن المستقبل البسيط للتعبير عن تنبؤات، قرارات سريعة، وعروض أو وعود للمستقبل. يمكن تكوينه باستخدام <span class="english-word">will</span> أو <span class="english-word">be going to</span>، مع اختلافات طفيفة في الاستخدام.</p>
            
            <h4>أ. الاستخدامات:</h4>
            <ul>
                <li><strong>تنبؤات (Predictions):</strong> غالبًا ما تكون غير مؤكدة ومبنية على رأي شخصي.
                    <ul>
                        <li>I think it <span class="english-word">will rain</span> tomorrow. (أعتقد أنها ستمطر غداً.)</li>
                        <li>He <span class="english-word">will probably win</span> the game. (من المحتمل أن يفوز بالمباراة.)</li>
                    </ul>
                </li>
                <li><strong>قرارات سريعة (Spontaneous Decisions):</strong> قرارات يتم اتخاذها في لحظة الكلام.
                    <ul>
                        <li>"I'm thirsty." "I <span class="english-word">will get</span> you some water." ("أنا عطشان." "سأحضر لك بعض الماء.")</li>
                        <li>"The phone is ringing." "I <span class="english-word">will answer</span> it." ("الهاتف يرن." "سأجيب عليه.")</li>
                    </ul>
                </li>
                <li><strong>عروض، وعود، تهديدات (Offers, Promises, Threats):</strong>
                    <ul>
                        <li>I <span class="english-word">will help</span> you with your homework. (سأساعدك في واجباتك.)</li>
                        <li>I <span class="english-word">will call</span> you later. (سأتصل بك لاحقاً.)</li>
                    </ul>
                </li>
                <li><strong>باستخدام <span class="english-word">be going to</span> (خطط ونوايا مؤكدة):</strong> للتعبير عن خطط ونوايا مستقبلية تم اتخاذ قرار بشأنها مسبقاً، أو تنبؤات مبنية على دليل حالي.
                    <ul>
                        <li>We <span class="english-word">are going to visit</span> our friends next week. (سنزور أصدقاءنا الأسبوع المقبل.)</li>
                        <li>Look at those dark clouds. It <span class="english-word">is going to rain</span>. (انظر إلى تلك الغيوم الداكنة. ستمطر.)</li>
                    </ul>
                </li>
            </ul>

            <h4>ب. الكلمات الدالة (Keywords):</h4>
            <ul>
                <li><span class="english-word">Tomorrow</span> (غداً)</li>
                <li><span class="english-word">Next week/month/year</span> (الأسبوع/الشهر/السنة القادمة)</li>
                <li><span class="english-word">Soon</span> (قريباً)</li>
                <li><span class="english-word">Later</span> (لاحقاً)</li>
                <li><span class="english-word">In the future</span> (في المستقبل)</li>
                <li><span class="english-word">I think</span>, <span class="english-word">I believe</span>, <span class="english-word">Probably</span> (للتنبؤات بـ <span class="english-word">will</span>)</li>
            </ul>

            <h4>ج. التكوين (Formation):</h4>
            <ul>
                <li><strong>باستخدام <span class="english-word">Will</span>: الفاعل + <span class="english-word">will</span> + الفعل في صورته الأساسية.</strong>
                    <ul>
                        <li>I <span class="english-word">will travel</span>.</li>
                        <li>They <span class="english-word">will study</span>.</li>
                    </ul>
                </li>
                <li><strong>باستخدام <span class="english-word">Be going to</span>: الفاعل + فعل <span class="english-word">be</span> (am/is/are) + <span class="english-word">going to</span> + الفعل في صورته الأساسية.</strong>
                    <ul>
                        <li>I <span class="english-word">am going to travel</span>.</li>
                        <li>They <span class="english-word">are going to study</span>.</li>
                    </ul>
                </li>
            </ul>

            <h4>د. أمثلة (10 Examples):</h4>
            <ol>
                <li>I <span class="english-word">will help</span> you with your bags. (سأساعدك في حقائبك.)</li>
                <li>She <span class="english-word">is going to start</span> a new job next month. (هي ستبدأ عملاً جديداً الشهر المقبل.)</li>
                <li>They <span class="english-word">will probably win</span> the match. (من المحتمل أن يفوزوا بالمباراة.)</li>
                <li>We <span class="english-word">are going to buy</span> a new car. (سنشتري سيارة جديدة.)</li>
                <li>He <span class="english-word">will call</span> you back in five minutes. (سيتصل بك بعد خمس دقائق.)</li>
                <li>It <span class="english-word">will be</span> sunny tomorrow. (سيكون الجو مشمساً غداً.)</li>
                <li>I think I <span class="english-word">will have</span> some tea. (أعتقد أنني سأتناول بعض الشاي.)</li>
                <li>They <span class="english-word">are going to build</span> a hospital in this area. (هم سيبنون مستشفى في هذه المنطقة.)</li>
                <li>You <span class="english-word">will enjoy</span> the party. (ستستمتع بالحفلة.)</li>
                <li>She <span class="english-word">is going to learn</span> French. (هي ستتعلم الفرنسية.)</li>
            </ol>

            <h4>هـ. السؤال والنفي (Questions and Negation):</h4>
            <ul>
                <li><strong>للسؤال بـ <span class="english-word">Will</span>:</strong> نضع <span class="english-word">Will</span> قبل الفاعل.
                    <ul>
                        <li><span class="english-word">Will</span> + الفاعل + الفعل في صورته الأساسية ...?
                            <ul>
                                <li><span class="english-word">Will</span> you come to the party? (هل ستأتي إلى الحفلة؟)</li>
                                <li><span class="english-word">Will</span> she help us? (هل ستساعدنا؟)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للنفي بـ <span class="english-word">Will</span>:</strong> نستخدم <span class="english-word">won't</span> (<span class="english-word">will not</span>) قبل الفعل.
                    <ul>
                        <li>الفاعل + <span class="english-word">won't</span> + الفعل في صورته الأساسية.
                            <ul>
                                <li>I <span class="english-word">won't</span> be late. (لن أتأخر.)</li>
                                <li>They <span class="english-word">won't</span> agree. (لن يوافقوا.)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للسؤال بـ <span class="english-word">Be going to</span>:</strong> نضع فعل <span class="english-word">be</span> (am/is/are) قبل الفاعل.
                    <ul>
                        <li><span class="english-word">Am</span> I / <span class="english-word">Is</span> he/she/it / <span class="english-word">Are</span> you/we/they + <span class="english-word">going to</span> + الفعل في صورته الأساسية ...?
                            <ul>
                                <li><span class="english-word">Are</span> you <span class="english-word">going to</span> study tonight? (هل ستدرس الليلة؟)</li>
                                <li><span class="english-word">Is</span> she <span class="english-word">going to</span> travel? (هل ستسافر؟)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للنفي بـ <span class="english-word">Be going to</span>:</strong> نضع <span class="english-word">not</span> بعد فعل <span class="english-word">be</span> (am/is/are).
                    <ul>
                        <li>الفاعل + <span class="english-word">am/is/are not</span> + <span class="english-word">going to</span> + الفعل في صورته الأساسية.
                            <ul>
                                <li>I <span class="english-word">am not going to</span> eat that. (لن آكل ذلك.)</li>
                                <li>They <span class="english-word">aren't going to</span> finish on time. (لن ينهوا في الوقت المحدد.)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>

    <div class="grammar-topic">
        <h3>6. زمن المضارع التام (Present Perfect)</h3>
        <div class="grammar-text">
            <p>يربط زمن المضارع التام الماضي بالحاضر. يُستخدم للتعبير عن أفعال بدأت في الماضي ولها تأثير أو علاقة بالحاضر، أو أفعال حدثت في وقت غير محدد في الماضي.</p>
            
            <h4>أ. الاستخدامات:</h4>
            <ul>
                <li><strong>أفعال بدأت في الماضي وما زالت مستمرة حتى الآن:</strong>
                    <ul>
                        <li>I <span class="english-word">have lived</span> in this city for 10 years. (عشت في هذه المدينة لمدة 10 سنوات - وما زلت أعيش.)</li>
                        <li>She <span class="english-word">has worked</span> here since 2015. (هي تعمل هنا منذ عام 2015 - وما زالت تعمل.)</li>
                    </ul>
                </li>
                <li><strong>تجارب أو أحداث حدثت في وقت غير محدد في الماضي (التركيز على النتيجة في الحاضر):</strong>
                    <ul>
                        <li>I <span class="english-word">have visited</span> New York. (لقد زرت نيويورك - التجربة مهمة، وليس متى حدثت.)</li>
                        <li>He <span class="english-word">has lost</span> his keys. (لقد فقد مفاتيحه - والآن لا يملكها.)</li>
                    </ul>
                </li>
                <li><strong>أحداث حديثة جدًا (غالبًا مع <span class="english-word">just</span>):</strong>
                    <ul>
                        <li>She <span class="english-word">has just finished</span> her homework. (هي أنهت واجبها للتو.)</li>
                    </ul>
                </li>
            </ul>

            <h4>ب. الكلمات الدالة (Keywords):</h4>
            <ul>
                <li><span class="english-word">For</span> (لمدة) - يتبعه مدة زمنية (e.g., <span class="english-word">for five years</span>)</li>
                <li><span class="english-word">Since</span> (منذ) - يتبعه نقطة زمنية محددة (e.g., <span class="english-word">since 2020</span>)</li>
                <li><span class="english-word">Already</span> (بالفعل)</li>
                <li><span class="english-word">Yet</span> (بعد) - تستخدم في النفي والسؤال</li>
                <li><span class="english-word">Just</span> (للتو/فقط)</li>
                <li><span class="english-word">Ever</span> (من قبل) - في السؤال</li>
                <li><span class="english-word">Never</span> (أبداً)</li>
                <li><span class="english-word">Recently</span> (مؤخراً)</li>
                <li><span class="english-word">Lately</span> (مؤخراً)</li>
            </ul>

            <h4>ج. التكوين (Formation):</h4>
            <ul>
                <li><strong>الفاعل + <span class="english-word">have</span> أو <span class="english-word">has</span> + الفعل في التصريف الثالث (Past Participle):</strong>
                    <ul>
                        <li>I/You/We/They <span class="english-word">have seen</span>.</li>
                        <li>He/She/It <span class="english-word">has gone</span>.</li>
                    </ul>
                </li>
                <li><strong>التصريف الثالث (Past Participle):</strong>
                    <ul>
                        <li>للأفعال المنتظمة: هو نفسه صيغة الماضي البسيط (الفعل + <span class="english-word">-ed</span>).
                            <ul>
                                <li><span class="english-word">Work</span> &rarr; <span class="english-word">Worked</span></li>
                            </ul>
                        </li>
                        <li>للأفعال غير المنتظمة: صيغة مختلفة (يجب حفظها).
                            <ul>
                                <li><span class="english-word">See</span> &rarr; <span class="english-word">Seen</span></li>
                                <li><span class="english-word">Go</span> &rarr; <span class="english-word">Gone</span></li>
                                <li><span class="english-word">Eat</span> &rarr; <span class="english-word">Eaten</span></li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>

            <h4>د. أمثلة (10 Examples):</h4>
            <ol>
                <li>I <span class="english-word">have visited</span> many countries. (لقد زرت العديد من البلدان.)</li>
                <li>She <span class="english-word">has lived</span> in New York since 2010. (هي عاشت في نيويورك منذ عام 2010.)</li>
                <li>They <span class="english-word">have just arrived</span>. (هم وصلوا للتو.)</li>
                <li>He <span class="english-word">has never eaten</span> sushi. (هو لم يأكل السوشي أبداً.)</li>
                <li>We <span class="english-word">have finished</span> our project. (لقد أنهينا مشروعنا.)</li>
                <li>The company <span class="english-word">has grown</span> a lot recently. (الشركة نمت كثيراً مؤخراً.)</li>
                <li>Have you <span class="english-word">ever seen</span> a ghost? (هل رأيت شبحاً من قبل؟)</li>
                <li>She <span class="english-word">has bought</span> a new phone. (هي اشترت هاتفاً جديداً.)</li>
                <li>I <span class="english-word">haven't seen</span> him lately. (لم أره مؤخراً.)</li>
                <li>They <span class="english-word">have known</span> each other for years. (هم يعرفون بعضهم البعض لسنوات.)</li>
            </ol>

            <h4>هـ. السؤال والنفي (Questions and Negation):</h4>
            <ul>
                <li><strong>للسؤال:</strong> نضع <span class="english-word">Have</span> أو <span class="english-word">Has</span> قبل الفاعل.
                    <ul>
                        <li><span class="english-word">Have</span> I/you/we/they + الفعل في التصريف الثالث ...?
                            <ul>
                                <li><span class="english-word">Have</span> you finished? (هل انتهيت؟)</li>
                                <li><span class="english-word">Have</span> they left yet? (هل غادروا بعد؟)</li>
                            </ul>
                        </li>
                        <li><span class="english-word">Has</span> he/she/it + الفعل في التصريف الثالث ...?
                            <ul>
                                <li><span class="english-word">Has</span> she arrived? (هل وصلت؟)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للنفي:</strong> نضع <span class="english-word">not</span> بعد <span class="english-word">have</span> أو <span class="english-word">has</span>.
                    <ul>
                        <li>I/You/We/They <span class="english-word">have not</span> (<span class="english-word">haven't</span>) + الفعل في التصريف الثالث.
                            <ul>
                                <li>I <span class="english-word">haven't</span> seen that movie. (لم أشاهد ذلك الفيلم.)</li>
                            </ul>
                        </li>
                        <li>He/She/It <span class="english-word">has not</span> (<span class="english-word">hasn't</span>) + الفعل في التصريف الثالث.
                            <ul>
                                <li>He <span class="english-word">hasn't</span> called me back. (لم يتصل بي بعد.)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>

    <div class="grammar-topic">
        <h3>7. زمن المضارع التام المستمر (Present Perfect Continuous)</h3>
        <div class="grammar-text">
            <p>يُستخدم زمن المضارع التام المستمر للتعبير عن أفعال بدأت في الماضي واستمرت حتى الآن أو توقفت للتو، مع التركيز على مدة النشاط.</p>
            
            <h4>أ. الاستخدامات:</h4>
            <ul>
                <li><strong>أفعال بدأت في الماضي وما زالت مستمرة (التركيز على المدة):</strong>
                    <ul>
                        <li>I <span class="english-word">have been studying</span> English for two hours. (أنا أدرس الإنجليزية لمدة ساعتين - وما زلت أدرس.)</li>
                        <li>She <span class="english-word">has been working</span> all day. (هي تعمل طوال اليوم - وما زالت تعمل.)</li>
                    </ul>
                </li>
                <li><strong>أفعال انتهت للتو ولها نتيجة واضحة في الحاضر:</strong>
                    <ul>
                        <li>Her eyes are red because she <span class="english-word">has been crying</span>. (عيناها حمراوان لأنها كانت تبكي.)</li>
                        <li>The ground is wet. It <span class="english-word">has been raining</span>. (الأرض مبللة. لقد كانت تمطر.)</li>
                    </ul>
                </li>
            </ul>

            <h4>ب. الكلمات الدالة (Keywords):</h4>
            <ul>
                <li><span class="english-word">For</span> (لمدة)</li>
                <li><span class="english-word">Since</span> (منذ)</li>
                <li><span class="english-word">How long</span> (كم المدة) - في السؤال</li>
                <li><span class="english-word">All day/morning/week</span> (طوال اليوم/الصباح/الأسبوع)</li>
                <li><span class="english-word">Recently</span> (مؤخراً)</li>
                <li><span class="english-word">Lately</span> (مؤخراً)</li>
            </ul>

            <h4>ج. التكوين (Formation):</h4>
            <ul>
                <li><strong>الفاعل + <span class="english-word">have been</span> أو <span class="english-word">has been</span> + الفعل + ing (Present Participle):</strong>
                    <ul>
                        <li>I/You/We/They <span class="english-word">have been waiting</span>.</li>
                        <li>He/She/It <span class="english-word">has been sleeping</span>.</li>
                    </ul>
                </li>
            </ul>

            <h4>د. أمثلة (10 Examples):</h4>
            <ol>
                <li>I <span class="english-word">have been learning</span> Arabic for three years. (أنا أتعلم العربية لمدة ثلاث سنوات.)</li>
                <li>She <span class="english-word">has been cooking</span> since morning. (هي تطهو منذ الصباح.)</li>
                <li>They <span class="english-word">have been living</span> in this house for five months. (هم يعيشون في هذا المنزل لمدة خمسة أشهر.)</li>
                <li>He <span class="english-word">has been working</span> on this project all week. (هو يعمل على هذا المشروع طوال الأسبوع.)</li>
                <li>We <span class="english-word">have been waiting</span> for you for an hour. (كنا ننتظرك لمدة ساعة.)</li>
                <li>It <span class="english-word">has been raining</span> heavily. (كانت تمطر بغزارة.)</li>
                <li>The children <span class="english-word">have been playing</span> outside. (الأطفال كانوا يلعبون في الخارج.)</li>
                <li>How long <span class="english-word">have you been studying</span>? (كم المدة التي كنت تدرس فيها؟)</li>
                <li>She <span class="english-word">has been feeling</span> tired lately. (هي تشعر بالتعب مؤخراً.)</li>
                <li>They <span class="english-word">have been planning</span> their trip. (هم يخططون لرحلتهم.)</li>
            </ol>

            <h4>هـ. السؤال والنفي (Questions and Negation):</h4>
            <ul>
                <li><strong>للسؤال:</strong> نضع <span class="english-word">Have</span> أو <span class="english-word">Has</span> قبل الفاعل.
                    <ul>
                        <li><span class="english-word">Have</span> I/you/we/they <span class="english-word">been</span> + الفعل + ing ...?
                            <ul>
                                <li><span class="english-word">Have</span> you <span class="english-word">been waiting</span> long? (هل كنت تنتظر طويلاً؟)</li>
                            </ul>
                        </li>
                        <li><span class="english-word">Has</span> he/she/it <span class="english-word">been</span> + الفعل + ing ...?
                            <ul>
                                <li><span class="english-word">Has</span> she <span class="english-word">been sleeping</span>? (هل كانت نائمة؟)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للنفي:</strong> نضع <span class="english-word">not</span> بعد <span class="english-word">have</span> أو <span class="english-word">has</span>.
                    <ul>
                        <li>I/You/We/They <span class="english-word">have not been</span> (<span class="english-word">haven't been</span>) + الفعل + ing.
                            <ul>
                                <li>I <span class="english-word">haven't been</span> feeling well. (لم أكن أشعر بخير.)</li>
                            </ul>
                        </li>
                        <li>He/She/It <span class="english-word">has not been</span> (<span class="english-word">hasn't been</span>) + الفعل + ing.
                            <ul>
                                <li>He <span class="english-word">hasn't been</span> studying. (هو لم يكن يدرس.)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>

    <div class="grammar-topic">
        <h3>8. زمن الماضي التام (Past Perfect)</h3>
        <div class="grammar-text">
            <p>يُستخدم زمن الماضي التام للتعبير عن حدث وقع واكتمل قبل حدث آخر في الماضي. يُظهر الترتيب الزمني للأحداث الماضية.</p>
            
            <h4>أ. الاستخدامات:</h4>
            <ul>
                <li><strong>حدث اكتمل قبل حدث آخر في الماضي:</strong> غالباً ما يستخدم مع الماضي البسيط.
                    <ul>
                        <li>When I arrived, the train <span class="english-word">had already left</span>. (عندما وصلت، كان القطار قد غادر بالفعل.)</li>
                        <li>She <span class="english-word">had finished</span> her work before she went home. (هي أنهت عملها قبل أن تذهب إلى المنزل.)</li>
                    </ul>
                </li>
                <li><strong>السبب والنتيجة في الماضي:</strong>
                    <ul>
                        <li>He was tired because he <span class="english-word">had worked</span> all night. (كان متعباً لأنه عمل طوال الليل.)</li>
                    </ul>
                </li>
            </ul>

            <h4>ب. الكلمات الدالة (Keywords):</h4>
            <ul>
                <li><span class="english-word">Before</span> (قبل)</li>
                <li><span class="english-word">After</span> (بعد)</li>
                <li><span class="english-word">By the time</span> (بحلول الوقت)</li>
                <li><span class="english-word">Already</span> (بالفعل)</li>
                <li><span class="english-word">When</span> (عندما)</li>
                <li><span class="english-word">Until then</span> (حتى ذلك الحين)</li>
            </ul>

            <h4>ج. التكوين (Formation):</h4>
            <ul>
                <li><strong>الفاعل + <span class="english-word">had</span> + الفعل في التصريف الثالث (Past Participle):</strong>
                    <ul>
                        <li>I/You/He/She/It/We/They <span class="english-word">had eaten</span>.</li>
                    </ul>
                </li>
            </ul>

            <h4>د. أمثلة (10 Examples):</h4>
            <ol>
                <li>I <span class="english-word">had never seen</span> such a beautiful place before I visited Egypt. (لم أر مكاناً جميلاً كهذا قبل أن أزور مصر.)</li>
                <li>She <span class="english-word">had already left</span> when he arrived. (كانت قد غادرت بالفعل عندما وصل.)</li>
                <li>By the time we got to the cinema, the movie <span class="english-word">had started</span>. (بحلول الوقت الذي وصلنا فيه إلى السينما، كان الفيلم قد بدأ.)</li>
                <li>He <span class="english-word">had eaten</span> all the cake before I got home. (هو كان قد أكل كل الكعكة قبل أن أصل إلى المنزل.)</li>
                <li>They <span class="english-word">had finished</span> their homework before they went to play. (هم كانوا قد أنهوا واجباتهم قبل أن يذهبوا للعب.)</li>
                <li>The patient <span class="english-word">had died</span> before the doctor arrived. (المريض كان قد توفي قبل وصول الطبيب.)</li>
                <li>We <span class="english-word">had planned</span> the trip long before. (كنا قد خططنا للرحلة قبل فترة طويلة.)</li>
                <li>He <span class="english-word">had heard</span> the news from his friend. (هو كان قد سمع الأخبار من صديقه.)</li>
                <li>I <span class="english-word">had lived</span> in London for five years before I moved to Paris. (كنت قد عشت في لندن لمدة خمس سنوات قبل أن أنتقل إلى باريس.)</li>
                <li>She realized she <span class="english-word">had forgotten</span> her wallet. (أدركت أنها قد نسيت محفظتها.)</li>
            </ol>

            <h4>هـ. السؤال والنفي (Questions and Negation):</h4>
            <ul>
                <li><strong>للسؤال:</strong> نضع <span class="english-word">Had</span> قبل الفاعل.
                    <ul>
                        <li><span class="english-word">Had</span> + الفاعل + الفعل في التصريف الثالث ...?
                            <ul>
                                <li><span class="english-word">Had</span> you eaten before you came? (هل كنت قد أكلت قبل أن تأتي؟)</li>
                                <li><span class="english-word">Had</span> she finished her work? (هل كانت قد أنهت عملها؟)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li><strong>للنفي:</strong> نضع <span class="english-word">not</span> بعد <span class="english-word">had</span>.
                    <ul>
                        <li>الفاعل + <span class="english-word">had not</span> (<span class="english-word">hadn't</span>) + الفعل في التصريف الثالث.
                            <ul>
                                <li>I <span class="english-word">hadn't</span> seen him before that day. (لم أره قبل ذلك اليوم.)</li>
                                <li>They <span class="english-word">hadn't</span> prepared for the meeting. (هم لم يكونوا قد استعدوا للاجتماع.)</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
 </section>

        <section id="common-words-section">
            <h2>كلمات شائعة (Common Words)</h2>
            <p class="section-intro">
               بناء حصيلة لغوية قوية يبدأ من الكلمات الأساسية. نستعرض هنا مجموعات من المفردات الشائعة والمصنفة حسب الموضوع (مثل أيام الأسبوع وأفراد العائلة) لتسهيل عملية الحفظ والربط.
            </p>
            <p class="instruction">اضغط على أي كلمة إنجليزية لسماع نطقها وتثبيت المعلومة.</p>
            
            <h3>أيام الأسبوع (Days of the Week)</h3>
            <div class="info-table-container">
                <table class="info-table">
                     <tbody>
                        <tr><td class="english-word">Saturday</td><td>السبت</td></tr>
                        <tr><td class="english-word">Sunday</td><td>الأحد</td></tr>
                        <tr><td class="english-word">Monday</td><td>الإثنين</td></tr>
                        <tr><td class="english-word">Tuesday</td><td>الثلاثاء</td></tr>
                        <tr><td class="english-word">Wednesday</td><td>الأربعاء</td></tr>
                        <tr><td class="english-word">Thursday</td><td>الخميس</td></tr>
                        <tr><td class="english-word">Friday</td><td>الجمعة</td></tr>
                    </tbody>
                </table>
            </div>

            <h3>أفراد العائلة (Family Members)</h3>
            <div class="info-table-container">
                <table class="info-table">
                    <tbody>
                        <tr><td class="english-word">Father</td><td>أب</td></tr>
                        <tr><td class="english-word">Mother</td><td>أم</td></tr>
                        <tr><td class="english-word">Brother</td><td>أخ</td></tr>
                        <tr><td class="english-word">Sister</td><td>أخت</td></tr>
                        <tr><td class="english-word">Son</td><td>ابن</td></tr>
                        <tr><td class="english-word">Daughter</td><td>ابنة</td></tr>
                    </tbody>
                </table>
            </div>
<section id="common-words-section">
    <h2>كلمات شائعة (Common Words)</h2>
    <p class="section-intro">
        ابدأ في بناء مفرداتك اليومية مع هذه القائمة من الكلمات والجمل الأكثر استخدامًا في اللغة الإنجليزية. اضغط على أي كلمة إنجليزية لسماع نطقها الصحيح وممارسة استماعك.
    </p>
    <p class="instruction">اضغط على الكلمة الإنجليزية لسماع نطقها.</p>

    <div class="info-table-container">
        <table class="info-table">
            <thead>
                <tr>
                    <th>الإنجليزية</th>
                    <th>العربية</th>
                    <th>الإنجليزية</th>
                    <th>العربية</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><span class="english-word">Hello</span></td>
                    <td>مرحبًا</td>
                    <td><span class="english-word">Goodbye</span></td>
                    <td>وداعًا</td>
                </tr>
                <tr>
                    <td><span class="english-word">Please</span></td>
                    <td>من فضلك</td>
                    <td><span class="english-word">Thank you</span></td>
                    <td>شكرًا</td>
                </tr>
                <tr>
                    <td><span class="english-word">Sorry</span></td>
                    <td>آسف</td>
                    <td><span class="english-word">Yes</span></td>
                    <td>نعم</td>
                </tr>
                <tr>
                    <td><span class="english-word">No</span></td>
                    <td>لا</td>
                    <td><span class="english-word">What</span></td>
                    <td>ماذا</td>
                </tr>
                <tr>
                    <td><span class="english-word">Where</span></td>
                    <td>أين</td>
                    <td><span class="english-word">When</span></td>
                    <td>متى</td>
                </tr>
                <tr>
                    <td><span class="english-word">Why</span></td>
                    <td>لماذا</td>
                    <td><span class="english-word">How</span></td>
                    <td>كيف</td>
                </tr>
                <tr>
                    <td><span class="english-word">Man</span></td>
                    <td>رجل</td>
                    <td><span class="english-word">Woman</span></td>
                    <td>امرأة</td>
                </tr>
                <tr>
                    <td><span class="english-word">Child</span></td>
                    <td>طفل</td>
                    <td><span class="english-word">Family</span></td>
                    <td>عائلة</td>
                </tr>
                <tr>
                    <td><span class="english-word">Friend</span></td>
                    <td>صديق</td>
                    <td><span class="english-word">House</span></td>
                    <td>منزل</td>
                </tr>
                <tr>
                    <td><span class="english-word">Food</span></td>
                    <td>طعام</td>
                    <td><span class="english-word">Water</span></td>
                    <td>ماء</td>
                </tr>
                <tr>
                    <td><span class="english-word">Time</span></td>
                    <td>وقت</td>
                    <td><span class="english-word">Day</span></td>
                    <td>يوم</td>
                </tr>
                <tr>
                    <td><span class="english-word">Night</span></td>
                    <td>ليل</td>
                    <td><span class="english-word">Week</span></td>
                    <td>أسبوع</td>
                </tr>
            </tbody>
        </table>
    </div>
</section>
            <section class="interactive-games" id="interactive-games">
                <section id="games-section">
            <h2>ألعاب تفاعلية لتعزيز تعلمك</h2>
            <p class="instruction">استمتع بتعلم الإنجليزية بطريقة ممتعة وتفاعلية! اختر اللعبة التي تفضلها.</p>

          
    <style>
        /* CSS Styles for the games */
        :root {
            --primary: #FF6F61;
            --secondary: #6A0572;
            --accent: #FFD166;
            --light: #FCE4EC;
            --dark: #4A4A68;
            --success: #06D6A0;
            --blue: #118AB2;
            --green: #1DB954;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
            direction: rtl; /* لضمان دعم اللغة العربية */
            text-align: right; /* لمحاذاة النص لليمين */
        }

        /* Common Section Title Style */
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 15px;
        }

        .section-title p {
            font-size: 1.2rem;
            color: var(--dark);
            max-width: 700px;
            margin: 0 auto;
        }

        /* Button Styles (common for all games) */
        .btn {
            padding: 14px 32px;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            border: none;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
            box-shadow: 0 6px 15px rgba(255, 111, 97, 0.4);
        }

        .btn-primary:hover {
            background: #ff5343;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 111, 97, 0.6);
        }

        .btn-secondary {
            background: white;
            color: var(--secondary);
            border: 2px solid var(--secondary);
        }

        .btn-secondary:hover {
            background: var(--light);
            transform: translateY(-3px);
        }

        /* Interactive Games Section */
        .interactive-games {
            padding: 60px 20px;
            background: linear-gradient(135deg, #e8f4f8 0%, #d6edff 100%);
            border-radius: 20px;
            max-width: 1000px;
            margin: 40px auto;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08);
        }

        .tabs {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .tab-btn {
            padding: 12px 25px;
            border-radius: 30px;
            background: white;
            border: 2px solid var(--secondary);
            color: var(--secondary);
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            min-width: 150px;
            text-align: center;
        }

        .tab-btn:hover, .tab-btn.active {
            background: var(--secondary);
            color: white;
        }

        .game-content {
            display: none;
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .game-content.active {
            display: block;
        }

        .game-title {
            text-align: center;
            color: var(--secondary);
            margin-bottom: 20px;
            font-size: 2rem;
        }

        /* Matching Game */
        .matching-game {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
        }

        .card {
            height: 100px;
            background: var(--light);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem; /* Adjusted for icons/emojis */
            cursor: pointer;
            transition: transform 0.3s, background-color 0.3s;
            position: relative;
            transform-style: preserve-3d;
        }

        .card.flipped .card-inner {
            transform: rotateY(180deg);
        }

        .card .card-inner {
            width: 100%;
            height: 100%;
            position: absolute;
            transform-style: preserve-3d;
            transition: transform 0.6s;
        }

        .card .card-front,
        .card .card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 10px;
            font-size: 2rem; /* Adjusted for icons/emojis */
            padding: 5px; 
            text-align: center;
        }

        .card .card-front {
            background: var(--light);
            color: var(--dark);
        }

        .card .card-back {
            background: var(--accent);
            color: white;
            transform: rotateY(180deg);
            /* No image specific styles needed here anymore */
        }
        
        .card.matched .card-back {
            background: var(--success);
        }

        /* Pronunciation Game */
        .pronunciation-game {
            text-align: center;
        }

        .word-display {
            font-size: 3rem;
            margin: 20px 0;
            color: var(--secondary);
            font-weight: bold;
        }

        .pronunciation-btn {
            padding: 15px 30px;
            background: var(--blue);
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            cursor: pointer;
            display: inline-flex; 
            align-items: center;
            gap: 10px;
            margin: 0 5px; 
            transition: all 0.3s ease;
        }

        .pronunciation-btn:disabled {
            opacity: 0.7;
            cursor: not-allowed;
        }

        .pronunciation-btn:hover:not(:disabled) {
            opacity: 0.9;
            transform: translateY(-2px);
        }

        .feedback {
            margin-top: 20px;
            font-size: 1.2rem;
            min-height: 30px;
            font-weight: bold;
        }
        .pronunciation-controls {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px; 
            margin-top: 20px;
        }

        /* Word Scramble Game */
        .scramble-game {
            text-align: center;
        }

        .scramble-word {
            font-size: 2.5rem;
            letter-spacing: 8px;
            margin: 20px 0;
            color: var(--secondary);
            font-weight: bold;
            text-transform: uppercase;
            word-break: break-all; 
        }

        .scramble-input {
            padding: 10px 15px;
            border: 2px solid var(--secondary);
            border-radius: 10px;
            font-size: 1.2rem;
            width: 300px;
            max-width: 80%;
            text-align: center;
        }

        .scramble-result {
            font-size: 1.2rem;
            margin-top: 20px;
            min-height: 30px;
            font-weight: bold;
        }
        .scramble-controls .btn-primary {
            min-width: 100px;
            justify-content: center;
        }

        /* Responsive Design */
        @media (max-width: 900px) {
            .matching-game {
                grid-template-columns: repeat(3, 1fr);
            }
        }

        @media (max-width: 768px) {
            .matching-game {
                grid-template-columns: repeat(2, 1fr);
            }
            .tabs {
                flex-direction: column;
                align-items: center;
            }
            .tab-btn {
                width: 80%; 
                max-width: 300px;
            }
            .pronunciation-controls {
                flex-direction: column;
            }
            .pronunciation-btn {
                margin: 5px auto; 
            }
        }

        @media (max-width: 480px) {
            .section-title h2 {
                font-size: 2rem;
            }
            .btn {
                padding: 12px 25px;
                font-size: 1rem;
            }
            .matching-game {
                grid-template-columns: 1fr;
            }
            .scramble-input {
                width: 100%;
                max-width: unset;
            }
            .scramble-controls {
                flex-direction: column;
                align-items: center;
            }
            .card {
                height: 80px; 
            }
            .card .card-front, .card .card-back {
                font-size: 1.5rem; 
            }
        </style>

<body>

    <section class="interactive-games" id="interactive-games">
        <div class="section-title">
            <h2>الألعاب التفاعلية</h2>
            <p>العب وتعلم الإنجليزية في نفس الوقت!</p>
        </div>

        <div class="tabs">
            <button class="tab-btn active" onclick="devGames.openGame('matching')">مطابقة الصور</button>
            <button class="tab-btn" onclick="devGames.openGame('pronunciation')">اختبار النطق</button>
            <button class="tab-btn" onclick="devGames.openGame('scramble')">ترتيب الكلمة</button>
        </div>

        <div id="matching" class="game-content active">
            <h3 class="game-title">لعبة مطابقة الصور مع الكلمات</h3>
            <p style="text-align: center; margin-bottom: 20px; color: var(--dark);">انقر على البطاقات لقلبها وابحث عن الرموز التعبيرية (الإيموجي) التي تطابق الكلمات</p>
            <div class="matching-game" id="matchingGame"></div>
            <div style="text-align: center; margin-top: 20px;">
                <button class="btn btn-primary" onclick="devGames.resetMatchingGame()">
                    <i class="fas fa-redo"></i> اعادة اللعبة
                </button>
            </div>
        </div>

        <div id="pronunciation" class="game-content">
            <h3 class="game-title">لعبة اختبار النطق</h3>
            <div class="pronunciation-game">
                <div class="word-display" id="wordDisplay"></div>
                <div class="pronunciation-controls">
                    <button class="pronunciation-btn" id="listenPronunciationBtn" onclick="devGames.speakWord()">
                        <i class="fas fa-volume-up"></i> استمع للنطق الصحيح
                    </button>
                    </div>
                <button class="btn btn-primary" style="margin-top: 20px;" id="nextPronunciationWordBtn" onclick="devGames.nextPronunciationWord()">
                    <i class="fas fa-arrow-right"></i> كلمة جديدة
                </button>
                <div class="feedback" id="feedback"></div>
            </div>
        </div>

        <div id="scramble" class="game-content">
            <h3 class="game-title">لعبة ترتيب الحروف</h3>
            <div class="scramble-game">
                <p style="color: var(--dark);">رتب الحروف لتكوين الكلمة الصحيحة</p>
                <div class="scramble-word" id="scrambleWord"></div>
                <div class="scramble-controls">
                    <input type="text" class="scramble-input" id="scrambleInput" placeholder="اكتب الكلمة هنا">
                    <button class="btn btn-primary" onclick="devGames.checkScramble()">
                        <i class="fas fa-check"></i> تحقق
                    </button>
                </div>
                <button class="btn btn-secondary" onclick="devGames.newScramble()">
                    <i class="fas fa-redo"></i> كلمة جديدة
                </button>
                <div class="scramble-result" id="scrambleResult"></div>
            </div>
        </div>
    </section>

    <script>
        const devGames = (function() {
            function speakLetter(textToSpeak) {
                if ('speechSynthesis' in window) {
                    const utterance = new SpeechSynthesisUtterance(textToSpeak);
                    utterance.lang = 'en-US';
                    utterance.rate = 0.8;
                    speechSynthesis.speak(utterance);
                } else {
                    console.warn("Your browser does not support speech synthesis.");
                }
            }

            // 1. Matching Game Logic
            const allMatchingPairs = [
                { word: 'Apple', arabic: 'تفاحة', icon: '🍎' }, 
                { word: 'Banana', arabic: 'موزة', icon: '🍌' },
                { word: 'Orange', arabic: 'برتقالة', icon: '🍊' },
                { word: 'Strawberry', arabic: 'فراولة', icon: '🍓' },
                { word: 'Grapes', arabic: 'عنب', icon: '🍇' },
                { word: 'Watermelon', arabic: 'بطيخ', icon: '🍉' },
                { word: 'Lemon', arabic: 'ليمون', icon: '🍋' },
                { word: 'Peach', arabic: 'خوخ', icon: '🍑' },
                { word: 'Cat', arabic: 'قطة', icon: '🐈' },
                { word: 'Dog', arabic: 'كلب', icon: '🐕' },
                { word: 'House', arabic: 'منزل', icon: '🏠' },
                { word: 'Tree', arabic: 'شجرة', icon: '🌳' },
                { word: 'Car', arabic: 'سيارة', icon: '🚗' },
                { word: 'Book', arabic: 'كتاب', icon: '📚' },
                { word: 'Ball', arabic: 'كرة', icon: '⚽' },
                { word: 'Sun', arabic: 'شمس', icon: '☀️' },
                { word: 'Moon', arabic: 'قمر', icon: '🌙' },
                { word: 'Star', arabic: 'نجمة', icon: '⭐' },
                { word: 'Flower', arabic: 'زهرة', icon: '🌸' },
                // أضف هنا باقي الـ 200 كلمة وأيقونة (إيموجي)
            ];
            
            let flippedCards = [];
            let matchedPairsCount = 0;
            let canFlip = true;
            const numberOfPairsToPlay = 10; 

            function createMatchingGame() {
                const gameContainer = document.getElementById('matchingGame');
                gameContainer.innerHTML = '';
                flippedCards = [];
                matchedPairsCount = 0;
                canFlip = true;
                
                const shuffledAllPairs = [...allMatchingPairs].sort(() => Math.random() - 0.5);
                const selectedPairs = shuffledAllPairs.slice(0, numberOfPairsToPlay);

                const cardsData = [];
                selectedPairs.forEach(pair => {
                    cardsData.push({ type: 'word', value: pair.word, matchId: pair.word });
                    cardsData.push({ type: 'icon', value: pair.icon, matchId: pair.word }); 
                });
                
                cardsData.sort(() => Math.random() - 0.5);
                
                cardsData.forEach((data, index) => {
                    const card = document.createElement('div');
                    card.classList.add('card');
                    card.dataset.matchId = data.matchId;
                    card.dataset.type = data.type;
                    
                    let backContent = data.value; 

                    card.innerHTML = `
                        <div class="card-inner">
                            <div class="card-front"></div>
                            <div class="card-back">${backContent}</div>
                        </div>
                    `;
                    card.addEventListener('click', function() {
                        if (canFlip && !this.classList.contains('flipped') && !this.classList.contains('matched')) {
                            this.classList.add('flipped');
                            flippedCards.push(this);
                            
                            if (data.type === 'word') {
                                speakLetter(data.value); 
                            }

                            if (flippedCards.length === 2) {
                                canFlip = false; 
                                setTimeout(checkMatch, 1000);
                            }
                        }
                    });
                    gameContainer.appendChild(card);
                });
            }
            
            function checkMatch() {
                const [card1, card2] = flippedCards;
                
                if (card1.dataset.matchId === card2.dataset.matchId) {
                    card1.classList.add('matched');
                    card2.classList.add('matched');
                    matchedPairsCount++;
                    speakLetter("Good job!"); 

                    if (matchedPairsCount === numberOfPairsToPlay) { 
                        setTimeout(() => {
                            alert('تهانينا! لقد طابقت جميع الكلمات!');
                            speakLetter("Congratulations! You matched all the words!");
                        }, 500);
                    }
                } else {
                    speakLetter("Try again."); 
                    setTimeout(() => {
                        card1.classList.remove('flipped');
                        card2.classList.remove('flipped');
                    }, 800);
                }
                
                flippedCards = []; 
                canFlip = true; 
            }
            
            function resetMatchingGame() {
                createMatchingGame();
            }

            // 2. Pronunciation Game Logic
            const pronunciationWords = [
                { word: 'Apple', arabic: 'تفاحة' }, { word: 'Banana', arabic: 'موزة' },
                { word: 'Cat', arabic: 'قطة' }, { word: 'Dog', arabic: 'كلب' },
                { word: 'Elephant', arabic: 'فيل' }, { word: 'Fish', arabic: 'سمكة' },
                { word: 'Grape', arabic: 'عنب' }, { word: 'House', arabic: 'منزل' },
                { word: 'Book', arabic: 'كتاب' }, { word: 'Table', arabic: 'طاولة' },
                { word: 'Chair', arabic: 'كرسي' }, { word: 'Sun', arabic: 'شمس' },
                { word: 'Moon', arabic: 'قمر' }, { word: 'Star', arabic: 'نجمة' },
                { word: 'Water', arabic: 'ماء' }, { word: 'Milk', arabic: 'حليب' },
                { word: 'Bread', arabic: 'خبز' }, { word: 'Car', arabic: 'سيارة' },
                { word: 'Bike', arabic: 'دراجة' }, { word: 'Tree', arabic: 'شجرة' },
                { word: 'Flower', arabic: 'زهرة' }, { word: 'Bird', arabic: 'طائر' },
                { word: 'Frog', arabic: 'ضفدع' }, { word: 'Lion', arabic: 'أسد' },
                { word: 'Tiger', arabic: 'نمر' }, { word: 'Zebra', arabic: 'حمار وحشي' },
                { word: 'Bear', arabic: 'دب' }, { word: 'Fox', arabic: 'ثعلب' },
                { word: 'School', arabic: 'مدرسة' }, { word: 'Teacher', arabic: 'معلم' },
                { word: 'Student', arabic: 'طالب' }, { word: 'Friend', arabic: 'صديق' },
                { word: 'Family', arabic: 'عائلة' }, { word: 'Home', arabic: 'منزل' },
                { word: 'Park', arabic: 'حديقة' }, { word: 'Store', arabic: 'متجر' },
                { word: 'Hospital', arabic: 'مستشفى' }, { word: 'Office', arabic: 'مكتب' },
                { word: 'Doctor', arabic: 'طبيب' }, { word: 'Nurse', arabic: 'ممرضة' },
                { word: 'Police', arabic: 'شرطة' }, { word: 'Fireman', arabic: 'رجل إطفاء' },
                { word: 'Chef', arabic: 'طباخ' }, { word: 'Farmer', arabic: 'مزارع' },
                { word: 'Singer', arabic: 'مغنّي' }, { word: 'Dancer', arabic: 'راقص' },
                { word: 'Artist', arabic: 'فنان' }, { word: 'Writer', arabic: 'كاتب' },
                { word: 'Happy', arabic: 'سعيد' }, { word: 'Sad', arabic: 'حزين' },
                { word: 'Big', arabic: 'كبير' }, { word: 'Small', arabic: 'صغير' },
                { word: 'Hot', arabic: 'حار' }, { word: 'Cold', arabic: 'بارد' },
                { word: 'Fast', arabic: 'سريع' }, { word: 'Slow', arabic: 'بطيء' },
                { word: 'New', arabic: 'جديد' }, { word: 'Old', arabic: 'قديم' },
                { word: 'Clean', arabic: 'نظيف' }, { word: 'Dirty', arabic: 'متسخ' },
                { word: 'Tall', arabic: 'طويل' }, { word: 'Short', arabic: 'قصير' },
                { word: 'Good', arabic: 'جيد' }, { word: 'Bad', arabic: 'سيئ' },
                { word: 'Red', arabic: 'أحمر' }, { word: 'Blue', arabic: 'أزرق' },
                { word: 'Green', arabic: 'أخضر' }, { word: 'Yellow', arabic: 'أصفر' },
                { word: 'Black', arabic: 'أسود' }, { word: 'White', arabic: 'أبيض' },
                { word: 'Brown', arabic: 'بني' }, { word: 'Purple', arabic: 'أرجواني' },
                { word: 'Pink', arabic: 'وردي' }, { word: 'Orange', arabic: 'برتقالي' },
                { word: 'One', arabic: 'واحد' }, { word: 'Two', arabic: 'اثنان' },
                { word: 'Three', arabic: 'ثلاثة' }, { word: 'Four', arabic: 'أربعة' },
                { word: 'Five', arabic: 'خمسة' }, { word: 'Six', arabic: 'ستة' },
                { word: 'Seven', arabic: 'سبعة' }, { word: 'Eight', arabic: 'ثمانية' },
                { word: 'Nine', arabic: 'تسعة' }, { word: 'Ten', arabic: 'عشرة' },
                { word: 'Eleven', arabic: 'أحد عشر' }, { word: 'Twelve', arabic: 'اثنا عشر' },
                { word: 'Thirteen', arabic: 'ثلاثة عشر' }, { word: 'Fourteen', arabic: 'أربعة عشر' },
                { word: 'Fifteen', arabic: 'خمسة عشر' }, { word: 'Sixteen', arabic: 'ستة عشر' },
                { word: 'Seventeen', arabic: 'سبعة عشر' }, { word: 'Eighteen', arabic: 'ثمانية عشر' },
                { word: 'Nineteen', arabic: 'تسعة عشر' }, { word: 'Twenty', arabic: 'عشرون' },
                { word: 'Thirty', arabic: 'ثلاثون' }, { word: 'Forty', arabic: 'أربعون' },
                { word: 'Fifty', arabic: 'خمسون' }, { word: 'Sixty', arabic: 'ستون' },
                { word: 'Seventy', arabic: 'سبعون' }, { word: 'Eighty', arabic: 'ثمانون' },
                { word: 'Ninety', arabic: 'تسعون' }, { word: 'Hundred', arabic: 'مئة' },
                { word: 'Day', arabic: 'يوم' }, { word: 'Night', arabic: 'ليل' },
                { word: 'Morning', arabic: 'صباح' }, { word: 'Evening', arabic: 'مساء' },
                { word: 'Yesterday', arabic: 'أمس' }, { word: 'Today', arabic: 'اليوم' },
                { word: 'Tomorrow', arabic: 'غداً' }, { word: 'Week', arabic: 'أسبوع' },
                { word: 'Month', arabic: 'شهر' }, { word: 'Year', arabic: 'سنة' },
                { word: 'January', arabic: 'يناير' }, { word: 'February', arabic: 'فبراير' },
                { word: 'March', arabic: 'مارس' }, { word: 'April', arabic: 'أبريل' },
                { word: 'May', arabic: 'مايو' }, { word: 'June', arabic: 'يونيو' },
                { word: 'July', arabic: 'يوليو' }, { word: 'August', arabic: 'أغسطس' },
                { word: 'September', arabic: 'سبتمبر' }, { word: 'October', arabic: 'أكتوبر' },
                { word: 'November', arabic: 'نوفمبر' }, { word: 'December', arabic: 'ديسمبر' },
                { word: 'Spring', arabic: 'ربيع' }, { word: 'Summer', arabic: 'صيف' },
                { word: 'Autumn', arabic: 'خريف' }, { word: 'Winter', arabic: 'شتاء' },
                { word: 'North', arabic: 'شمال' }, { word: 'South', arabic: 'جنوب' },
                { word: 'East', arabic: 'شرق' }, { word: 'West', arabic: 'غرب' },
                { word: 'Up', arabic: 'فوق' }, { word: 'Down', arabic: 'تحت' },
                { word: 'In', arabic: 'في' }, { word: 'Out', arabic: 'خارج' },
                { word: 'On', arabic: 'على' }, { word: 'Off', arabic: 'إيقاف' },
                { word: 'Near', arabic: 'قريب' }, { word: 'Far', arabic: 'بعيد' },
                { word: 'Left', arabic: 'يسار' }, { word: 'Right', arabic: 'يمين' },
                { word: 'Yes', arabic: 'نعم' }, { word: 'No', arabic: 'لا' },
                { word: 'Hello', arabic: 'مرحباً' }, { word: 'Goodbye', arabic: 'وداعاً' },
                { word: 'Please', arabic: 'رجاءً' }, { word: 'Thank you', arabic: 'شكراً لك' },
                { word: 'Sorry', arabic: 'آسف' }, { word: 'Excuse me', arabic: 'عفواً' },
                { word: 'Brother', arabic: 'أخ' }, { word: 'Sister', arabic: 'أخت' },
                { word: 'Mother', arabic: 'أم' }, { word: 'Father', arabic: 'أب' },
                { word: 'Son', arabic: 'ابن' }, { word: 'Daughter', arabic: 'ابنة' },
                { word: 'Grandfather', arabic: 'جد' }, { word: 'Grandmother', arabic: 'جدة' }
            ];
            let currentPronunciationWordIndex = 0;
            // تم حذف المتغيرات المتعلقة بـ SpeechRecognition و MediaRecorder
            
            const listenBtn = document.getElementById('listenPronunciationBtn');
            const nextWordBtn = document.getElementById('nextPronunciationWordBtn');
            const feedbackElement = document.getElementById('feedback');

            // لم يعد هناك حاجة للتحقق من APIs التعرف على الكلام هنا
            // لأن زر "تحدث وقارن" قد تم حذفه.

            function displayPronunciationWord() {
                const wordData = pronunciationWords[currentPronunciationWordIndex];
                document.getElementById('wordDisplay').textContent = wordData.word;
                let instructions = `
                    <p>الكلمة: <strong>${wordData.word}</strong> (${wordData.arabic})</p>
                    <p style="color: var(--blue); margin-top: 10px;">استمع جيداً للنطق الصحيح ثم حاول تقليده!</p>
                `;
                feedbackElement.innerHTML = instructions;
            }
            
            function speakWord() {
                const word = pronunciationWords[currentPronunciationWordIndex].word;
                speakLetter(word);
            }

            function nextPronunciationWord() {
                currentPronunciationWordIndex = (currentPronunciationWordIndex + 1) % pronunciationWords.length;
                displayPronunciationWord();
            }
            
            // 3. Word Scramble Game Logic (Remains the same as previous version)
            const scrambleWords = [
                'APPLE', 'BANANA', 'ORANGE', 'CAT', 'DOG', 'SUN', 'MOON', 'STAR', 'BOOK', 'BALL',
                'TREE', 'FLOWER', 'BIRD', 'FISH', 'FROG', 'LION', 'TIGER', 'ZEBRA', 'BEAR', 'FOX',
                'HOUSE', 'CAR', 'BIKE', 'SPOON', 'FORK', 'KNIFE', 'PLATE', 'CUP', 'GLASS', 'JUICE',
                'WATER', 'MILK', 'BREAD', 'CHEESE', 'EGG', 'RICE', 'PASTA', 'PIZZA', 'CAKE', 'COOKIE',
                'TABLE', 'CHAIR', 'BED', 'SOFA', 'LAMP', 'DOOR', 'WINDOW', 'WALL', 'ROOF', 'FLOOR',
                'PENCIL', 'PEN', 'PAPER', 'ERASER', 'RULER', 'BAG', 'SHOE', 'HAT', 'SHIRT', 'PANTS',
                'DRESS', 'COAT', 'SOCKS', 'GLOVES', 'SCARF', 'CLOUD', 'RAIN', 'SNOW', 'WIND', 'STORM',
                'SKY', 'OCEAN', 'RIVER', 'LAKE', 'MOUNTAIN', 'HILL', 'VALLEY', 'DESERT', 'FOREST', 'FIELD',
                'ROAD', 'BRIDGE', 'TRAIN', 'BUS', 'PLANE', 'BOAT', 'SHIP', 'TRUCK', 'TAXI', 'JEEP',
                'SCHOOL', 'TEACHER', 'STUDENT', 'FRIEND', 'FAMILY', 'HOME', 'PARK', 'STORE', 'HOSPITAL', 'OFFICE',
                'DOCTOR', 'NURSE', 'POLICE', 'FIREMAN', 'CHEF', 'FARMER', 'SINGER', 'DANCER', 'ARTIST', 'WRITER'
            ];
            let currentScrambleWord = '';
            
            function setupScrambleGame() {
                currentScrambleWord = scrambleWords[Math.floor(Math.random() * scrambleWords.length)];
                const scrambled = shuffleWord(currentScrambleWord);
                document.getElementById('scrambleWord').textContent = scrambled;
                document.getElementById('scrambleInput').value = '';
                document.getElementById('scrambleResult').innerHTML = '';
            }
            
            function shuffleWord(word) {
                const letters = word.split('');
                for (let i = letters.length - 1; i > 0; i--) {
                    const j = Math.floor(Math.random() * (i + 1));
                    [letters[i], letters[j]] = [letters[j], letters[i]];
                }
                return letters.join('');
            }
            
            function checkScramble() {
                const userInput = document.getElementById('scrambleInput').value.toUpperCase();
                const resultElement = document.getElementById('scrambleResult');
                
                if (userInput === currentScrambleWord) {
                    resultElement.innerHTML = '<p style="color: var(--success);">✓ أحسنت! الإجابة صحيحة!</p>';
                    speakLetter("Excellent!");
                    setTimeout(newScramble, 1500); 
                } else {
                    resultElement.innerHTML = '<p style="color: var(--primary);">✗ حاول مرة أخرى!</p>';
                    speakLetter("Try again!");
                }
            }
            
            function newScramble() {
                setupScrambleGame();
            }
            
            // Tab Switching Functions
            function openGame(gameId) {
                document.querySelectorAll('.game-content').forEach(game => {
                    game.classList.remove('active');
                });
                
                document.querySelectorAll('.tab-btn').forEach(btn => {
                    btn.classList.remove('active');
                });
                
                document.getElementById(gameId).classList.add('active');
                document.querySelector(`.tab-btn[onclick="devGames.openGame('${gameId}')"]`).classList.add('active');
                
                // Initialize the selected game
                if (gameId === 'matching') {
                    createMatchingGame();
                } else if (gameId === 'pronunciation') {
                    currentPronunciationWordIndex = Math.floor(Math.random() * pronunciationWords.length); 
                    displayPronunciationWord();
                    // تأكد من أن زر الاستماع متاح
                    if (listenBtn) listenBtn.disabled = false;
                    if (nextWordBtn) nextWordBtn.disabled = false;

                } else if (gameId === 'scramble') {
                    setupScrambleGame();
                }
            }

            // Public interface of the devGames module
            return {
                openGame: openGame,
                resetMatchingGame: resetMatchingGame,
                speakWord: speakWord,
                nextPronunciationWord: nextPronunciationWord,
                checkScramble: checkScramble,
                newScramble: newScramble
            };
        })(); 

        // Initialize the first game when the DOM is loaded
        document.addEventListener('DOMContentLoaded', function() {
            devGames.openGame('matching');
        });
    </script>

    <footer>
        <p>تم التصميم والتطوير لرحلتك في تعلم اللغة الإنجليزية. &copy; 2025</p>
    </footer>

    <script>
    document.addEventListener('DOMContentLoaded', function() {
        const navButtons = document.querySelectorAll('.nav-btn');
        const sections = document.querySelectorAll('main section');
        const scrollTopBtn = document.querySelector('.scroll-top-btn');
        const alphabetGrid = document.getElementById('alphabet-grid');
        const wordsDisplayArea = document.getElementById('words-display-area');

        // --- Navigation Logic ---
        navButtons.forEach(button => {
            button.addEventListener('click', () => {
                const sectionId = button.getAttribute('data-section');
                const section = document.getElementById(sectionId);
                
                if (section) {
                    window.scrollTo({
                        top: section.offsetTop - (window.innerHeight * 0.15),
                        behavior: 'smooth'
                    });
                }
            });
        });

        // --- Active Nav on Scroll ---
        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                if (pageYOffset >= sectionTop - (window.innerHeight * 0.2)) {
                    current = section.getAttribute('id');
                }
            });

            navButtons.forEach(button => {
                button.classList.remove('active');
                if (button.getAttribute('data-section') === current) {
                    button.classList.add('active');
                }
            });

            // --- Scroll to Top Button Visibility ---
            if (window.scrollY > 300) {
                scrollTopBtn.classList.add('show');
            } else {
                scrollTopBtn.classList.remove('show');
            }
        });
        
        // --- Scroll to Top Click ---
        scrollTopBtn.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });


        // --- Alphabet & Words Logic ---
        const alphabet = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('');
        const wordData = {
            A: [{en: 'Apple', ar: 'تفاحة'}, {en: 'Ant', ar: 'نملة'}, {en: 'Arm', ar: 'ذراع'}, {en: 'Art', ar: 'فن'}, {en: 'Ask', ar: 'يسأل'}, {en: 'Air', ar: 'هواء'}, {en: 'And', ar: 'و'}, {en: 'Animal', ar: 'حيوان'}, {en: 'All', ar: 'كل'}, {en: 'Angry', ar: 'غاضب'}],
            B: [{en: 'Ball', ar: 'كرة'}, {en: 'Book', ar: 'كتاب'}, {en: 'Boy', ar: 'ولد'}, {en: 'Blue', ar: 'أزرق'}, {en: 'Bed', ar: 'سرير'}, {en: 'Big', ar: 'كبير'}, {en: 'Banana', ar: 'موز'}, {en: 'Bird', ar: 'طائر'}, {en: 'Box', ar: 'صندوق'}, {en: 'Bread', ar: 'خبز'}],
            C: [{en: 'Cat', ar: 'قطة'}, {en: 'Car', ar: 'سيارة'}, {en: 'Cup', ar: 'كوب'}, {en: 'Cold', ar: 'بارد'}, {en: 'City', ar: 'مدينة'}, {en: 'Cake', ar: 'كعكة'}, {en: 'Cloud', ar: 'سحابة'}, {en: 'Chair', ar: 'كرسي'}, {en: 'Clean', ar: 'نظيف'}, {en: 'Cook', ar: 'يطبخ'}],
            D: [{en: 'Dog', ar: 'كلب'}, {en: 'Door', ar: 'باب'}, {en: 'Day', ar: 'يوم'}, {en: 'Duck', ar: 'بطة'}, {en: 'Desk', ar: 'مكتب'}, {en: 'Dark', ar: 'مظلم'}, {en: 'Down', ar: 'أسفل'}, {en: 'Drink', ar: 'يشرب'}, {en: 'Date', ar: 'تمر'}, {en: 'Dream', ar: 'حلم'}],
            E: [{en: 'Egg', ar: 'بيضة'}, {en: 'Elephant', ar: 'فيل'}, {en: 'Eye', ar: 'عين'}, {en: 'Earth', ar: 'أرض'}, {en: 'Easy', ar: 'سهل'}, {en: 'Eat', ar: 'يأكل'}, {en: 'End', ar: 'نهاية'}, {en: 'Eight', ar: 'ثمانية'}, {en: 'Empty', ar: 'فارغ'}, {en: 'Early', ar: 'مبكر'}],
            F: [{en: 'Fish', ar: 'سمكة'}, {en: 'Fan', ar: 'مروحة'}, {en: 'Face', ar: 'وجه'}, {en: 'Five', ar: 'خمسة'}, {en: 'Flower', ar: 'زهرة'}, {en: 'Friend', ar: 'صديق'}, {en: 'Fast', ar: 'سريع'}, {en: 'Fat', ar: 'سمين'}, {en: 'Fire', ar: 'نار'}, {en: 'Food', ar: 'طعام'}],
            G: [{en: 'Goat', ar: 'ماعز'}, {en: 'Green', ar: 'أخضر'}, {en: 'Game', ar: 'لعبة'}, {en: 'Glass', ar: 'كأس'}, {en: 'Go', ar: 'يذهب'}, {en: 'Good', ar: 'جيد'}, {en: 'Girl', ar: 'فتاة'}, {en: 'Gift', ar: 'هدية'}, {en: 'Garden', ar: 'حديقة'}, {en: 'Gold', ar: 'ذهب'}],
            H: [{en: 'Hand', ar: 'يد'}, {en: 'Hat', ar: 'قبعة'}, {en: 'House', ar: 'منزل'}, {en: 'Hot', ar: 'حار'}, {en: 'Happy', ar: 'سعيد'}, {en: 'Horse', ar: 'حصان'}, {en: 'Heart', ar: 'قلب'}, {en: 'Help', ar: 'يساعد'}, {en: 'Honey', ar: 'عسل'}, {en: 'Heavy', ar: 'ثقيل'}],
            I: [{en: 'Ice', ar: 'ثلج'}, {en: 'Iron', ar: 'حديد'}, {en: 'Island', ar: 'جزيرة'}, {en: 'Idea', ar: 'فكرة'}, {en: 'Ink', ar: 'حبر'}, {en: 'In', ar: 'في'}, {en: 'Important', ar: 'مهم'}, {en: 'Inside', ar: 'داخل'}, {en: 'Insect', ar: 'حشرة'}, {en: 'Image', ar: 'صورة'}],
            J: [{en: 'Jam', ar: 'مربى'}, {en: 'Juice', ar: 'عصير'}, {en: 'Jacket', ar: 'سترة'}, {en: 'Job', ar: 'وظيفة'}, {en: 'Jump', ar: 'يقفز'}, {en: 'Jar', ar: 'جرة'}, {en: 'Joy', ar: 'فرح'}, {en: 'Jungle', ar: 'غابة'}, {en: 'Jewel', ar: 'جوهرة'}, {en: 'Join', ar: 'ينضم'}],
            K: [{en: 'Key', ar: 'مفتاح'}, {en: 'King', ar: 'ملك'}, {en: 'Kitchen', ar: 'مطبخ'}, {en: 'Kite', ar: 'طائرة ورقية'}, {en: 'Knee', ar: 'ركبة'}, {en: 'Knife', ar: 'سكين'}, {en: 'Know', ar: 'يعرف'}, {en: 'Kind', ar: 'لطيف'}, {en: 'Kick', ar: 'يركل'}, {en: 'Kid', ar: 'طفل'}],
            L: [{en: 'Lion', ar: 'أسد'}, {en: 'Lamp', ar: 'مصباح'}, {en: 'Lemon', ar: 'ليمون'}, {en: 'Light', ar: 'ضوء'}, {en: 'Long', ar: 'طويل'}, {en: 'Love', ar: 'حب'}, {en: 'Lake', ar: 'بحيرة'}, {en: 'Learn', ar: 'يتعلم'}, {en: 'Left', ar: 'يسار'}, {en: 'Listen', ar: 'يستمع'}],
            M: [{en: 'Man', ar: 'رجل'}, {en: 'Moon', ar: 'قمر'}, {en: 'Milk', ar: 'حليب'}, {en: 'Money', ar: 'مال'}, {en: 'Mother', ar: 'أم'}, {en: 'Map', ar: 'خريطة'}, {en: 'Mouse', ar: 'فأر'}, {en: 'Mountain', ar: 'جبل'}, {en: 'Music', ar: 'موسيقى'}, {en: 'Morning', ar: 'صباح'}],
            N: [{en: 'Nose', ar: 'أنف'}, {en: 'Night', ar: 'ليل'}, {en: 'Nine', ar: 'تسعة'}, {en: 'Name', ar: 'اسم'}, {en: 'New', ar: 'جديد'}, {en: 'No', ar: 'لا'}, {en: 'Neck', ar: 'رقبة'}, {en: 'Nest', ar: 'عش'}, {en: 'Number', ar: 'رقم'}, {en: 'North', ar: 'شمال'}],
            O: [{en: 'Orange', ar: 'برتقال'}, {en: 'Old', ar: 'قديم'}, {en: 'One', ar: 'واحد'}, {en: 'Open', ar: 'يفتح'}, {en: 'Oil', ar: 'زيت'}, {en: 'Ocean', ar: 'محيط'}, {en: 'Office', ar: 'مكتب'}, {en: 'Onion', ar: 'بصل'}, {en: 'Out', ar: 'خارج'}, {en: 'Oven', ar: 'فرن'}],
            P: [{en: 'Pen', ar: 'قلم'}, {en: 'Pig', ar: 'خنزير'}, {en: 'Pink', ar: 'وردي'}, {en: 'Pizza', ar: 'بيتزا'}, {en: 'Park', ar: 'حديقة'}, {en: 'Photo', ar: 'صورة'}, {en: 'Paper', ar: 'ورق'}, {en: 'Play', ar: 'يلعب'}, {en: 'Put', ar: 'يضع'}, {en: 'Paint', ar: 'يرسم'}],
            Q: [{en: 'Queen', ar: 'ملكة'}, {en: 'Quiet', ar: 'هادئ'}, {en: 'Question', ar: 'سؤال'}, {en: 'Quick', ar: 'سريع'}, {en: 'Quilt', ar: 'لحاف'}, {en: 'Quarter', ar: 'ربع'}, {en: 'Queue', ar: 'طابور'}, {en: 'Quiz', ar: 'اختبار'}, {en: 'Quote', ar: 'اقتباس'}, {en: 'Quit', ar: 'يترك'}],
            R: [{en: 'Red', ar: 'أحمر'}, {en: 'Run', ar: 'يجري'}, {en: 'Rabbit', ar: 'أرنب'}, {en: 'Rain', ar: 'مطر'}, {en: 'Road', ar: 'طريق'}, {en: 'Room', ar: 'غرفة'}, {en: 'Read', ar: 'يقرأ'}, {en: 'Rich', ar: 'غني'}, {en: 'Right', ar: 'يمين/صحيح'}, {en: 'River', ar: 'نهر'}],
            S: [{en: 'Sun', ar: 'شمس'}, {en: 'Star', ar: 'نجمة'}, {en: 'Sad', ar: 'حزين'}, {en: 'Sit', ar: 'يجلس'}, {en: 'School', ar: 'مدرسة'}, {en: 'Sea', ar: 'بحر'}, {en: 'Small', ar: 'صغير'}, {en: 'Sleep', ar: 'ينام'}, {en: 'Snake', ar: 'ثعبان'}, {en: 'Sugar', ar: 'سكر'}],
            T: [{en: 'Table', ar: 'طاولة'}, {en: 'Tree', ar: 'شجرة'}, {en: 'Ten', ar: 'عشرة'}, {en: 'Tea', ar: 'شاي'}, {en: 'Tall', ar: 'طويل'}, {en: 'Time', ar: 'وقت'}, {en: 'Teacher', ar: 'معلم'}, {en: 'Train', ar: 'قطار'}, {en: 'Talk', ar: 'يتحدث'}, {en: 'Thank you', ar: 'شكراً'}],
            U: [{en: 'Umbrella', ar: 'مظلة'}, {en: 'Under', ar: 'تحت'}, {en: 'Up', ar: 'فوق'}, {en: 'Uncle', ar: 'عم/خال'}, {en: 'Use', ar: 'يستخدم'}, {en: 'Ugly', ar: 'قبيح'}, {en: 'Unit', ar: 'وحدة'}, {en: 'Understand', ar: 'يفهم'}, {en: 'Uniform', ar: 'زي موحد'}, {en: 'University', ar: 'جامعة'}],
            V: [{en: 'Van', ar: 'شاحنة صغيرة'}, {en: 'Vase', ar: 'مزهرية'}, {en: 'Vegetable', ar: 'خضروات'}, {en: 'Village', ar: 'قرية'}, {en: 'Visit', ar: 'يزور'}, {en: 'Voice', ar: 'صوت'}, {en: 'Volcano', ar: 'بركان'}, {en: 'Very', ar: 'جداً'}, {en: 'View', ar: 'منظر'}, {en: 'Video', ar: 'فيديو'}],
            W: [{en: 'Water', ar: 'ماء'}, {en: 'Window', ar: 'نافذة'}, {en: 'White', ar: 'أبيض'}, {en: 'Watch', ar: 'ساعة يد'}, {en: 'Walk', ar: 'يمشي'}, {en: 'Wall', ar: 'جدار'}, {en: 'Warm', ar: 'دافئ'}, {en: 'Wind', ar: 'رياح'}, {en: 'Woman', ar: 'امرأة'}, {en: 'Write', ar: 'يكتب'}],
            X: [{en: 'X-ray', ar: 'أشعة سينية'}, {en: 'Xylophone', ar: 'إكسيليفون'}, {en: 'Box', ar: 'صندوق'}, {en: 'Fox', ar: 'ثعلب'}, {en: 'Six', ar: 'ستة'}, {en: 'Mix', ar: 'يخلط'}, {en: 'Fix', ar: 'يصلح'}, {en: 'Wax', ar: 'شمع'}, {en: 'Next', ar: 'التالي'}, {en: 'Exit', ar: 'خروج'}],
            Y: [{en: 'Yellow', ar: 'أصفر'}, {en: 'Yes', ar: 'نعم'}, {en: 'You', ar: 'أنت'}, {en: 'Year', ar: 'سنة'}, {en: 'Yogurt', ar: 'زبادي'}, {en: 'Yard', ar: 'فناء'}, {en: 'Young', ar: 'شاب'}, {en: 'Yell', ar: 'يصرخ'}, {en: 'Yesterday', ar: 'أمس'}, {en: 'Yummy', ar: 'لذيذ'}],
            Z: [{en: 'Zebra', ar: 'حمار وحشي'}, {en: 'Zoo', ar: 'حديقة حيوان'}, {en: 'Zero', ar: 'صفر'}, {en: 'Zip', ar: 'سحاب'}, {en: 'Zone', ar: 'منطقة'}, {en: 'Zigzag', ar: 'متعرج'}, {en: 'Lazy', ar: 'كسول'}, {en: 'Size', ar: 'حجم'}, {en: 'Quiz', ar: 'اختبار'}, {en: 'Pizza', ar: 'بيتزا'}]
        };

        // Populate alphabet grid
        alphabet.forEach(letter => {
            const letterButton = document.createElement('div');
            letterButton.className = 'alphabet-letter-button';
            letterButton.textContent = letter;
            letterButton.dataset.letter = letter;
            alphabetGrid.appendChild(letterButton);

            letterButton.addEventListener('click', () => {
                displayWordsForLetter(letter);
                // Highlight active letter
                document.querySelectorAll('.alphabet-letter-button').forEach(btn => btn.classList.remove('active-letter'));
                letterButton.classList.add('active-letter');
            });
        });

        function displayWordsForLetter(letter) {
            const words = wordData[letter];
            wordsDisplayArea.innerHTML = ''; // Clear previous content
            wordsDisplayArea.style.display = 'flex'; // Show the area

            if (words && words.length > 0) {
                words.forEach(word => {
                    const wordItem = document.createElement('div');
                    wordItem.className = 'word-item';
                    
                    const englishWordSpan = document.createElement('span');
                    englishWordSpan.className = 'english-word';
                    englishWordSpan.textContent = word.en;
                    
                    const arabicTranslationSpan = document.createElement('span');
                    arabicTranslationSpan.className = 'arabic-translation';
                    arabicTranslationSpan.textContent = word.ar;
                    
                    wordItem.appendChild(englishWordSpan);
                    wordItem.appendChild(arabicTranslationSpan);
                    wordsDisplayArea.appendChild(wordItem);
                });
            } else {
                wordsDisplayArea.innerHTML = `<p style="text-align: center; color: #777;">لا توجد كلمات متاحة لهذا الحرف حاليًا.</p>`;
            }
        }
        
        // --- Text-to-Speech Logic ---
        function speak(text) {
            // Cancel any previous speech
            window.speechSynthesis.cancel();
            if ('speechSynthesis' in window) {
                const utterance = new SpeechSynthesisUtterance(text);
                utterance.lang = 'en-US'; // Set language to English
                window.speechSynthesis.speak(utterance);
            } else {
                alert('عذرًا، متصفحك لا يدعم خاصية النطق.');
            }
        }
        
        // Add event listener to the whole document for any .english-word click
        document.addEventListener('click', function(event) {
            if (event.target.classList.contains('english-word')) {
                speak(event.target.textContent);
            }
        });

    });
    </script>
</body>
