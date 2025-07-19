<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تعلم الإنجليزية: الأبجدية والقواعد</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* CSS Code */
        :root {
            --primary-color: #6a0572; /* Deep Purple */
            --secondary-color: #ff6f61; /* Coral */
            --text-color: #333;
            --bg-color: #fce4ec; /* Light Pink Background */
            --card-bg: #ffffff;
            --border-color: #e0e0e0;
            --shadow-color: rgba(0, 0, 0, 0.15);
            --accent-color-1: #4CAF50; /* Green */
            --accent-color-2: #2196F3; /* Blue */
            --accent-color-3: #FFC107; /* Amber */
            --accent-color-4: #9C27B0; /* Dark Purple */
        }

        body {
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.8; /* Increased line height for readability */
            direction: rtl;
            text-align: right;
            scroll-behavior: smooth;
        }

        header {
            background-image: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 2em 0;
            text-align: center;
            box-shadow: 0 4px 10px var(--shadow-color);
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: -50px;
            left: -50px;
            width: 200px;
            height: 200px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transform: rotate(45deg);
        }

        header::after {
            content: '';
            position: absolute;
            bottom: -50px;
            right: -50px;
            width: 150px;
            height: 150px;
            background-color: rgba(255, 255, 255, 0.15);
            border-radius: 50%;
            transform: rotate(-30deg);
        }

        header h1 {
            margin: 0;
            font-size: 3em;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            letter-spacing: 1px;
        }

        main {
            padding: 30px 20px;
            max-width: 1300px; /* Increased max-width */
            margin: 30px auto; /* Increased margin */
            background-color: var(--card-bg);
            border-radius: 12px; /* More rounded corners */
            box-shadow: 0 0 20px var(--shadow-color);
        }

        section {
            margin-bottom: 50px; /* Increased margin */
            padding-bottom: 30px; /* Increased padding */
            border-bottom: 1px solid var(--border-color);
        }

        section:last-of-type {
            border-bottom: none;
        }

        h2 {
            color: var(--primary-color);
            text-align: center;
            margin-bottom: 40px; /* Increased margin */
            font-size: 2.5em; /* Larger heading */
            border-bottom: 3px solid var(--secondary-color); /* Thicker border */
            display: inline-block;
            padding-bottom: 10px;
            position: relative;
            left: 50%;
            transform: translateX(-50%);
            letter-spacing: 0.5px;
        }

        h2::after {
            content: '✨'; /* Fun emoji */
            position: absolute;
            left: -30px;
            top: 50%;
            transform: translateY(-50%);
        }

        h2::before {
            content: '✨'; /* Fun emoji */
            position: absolute;
            right: -30px;
            top: 50%;
            transform: translateY(-50%);
        }

        h3 {
            color: var(--text-color);
            font-size: 1.8em; /* Larger subheadings */
            margin-top: 30px; /* Increased margin */
            margin-bottom: 20px;
            padding-bottom: 5px;
            border-bottom: 1px dashed var(--border-color);
        }

        p.instruction {
            text-align: center;
            font-style: italic;
            color: #666;
            margin-bottom: 30px; /* Increased margin */
            font-size: 1.1em;
        }

        /* Alphabet Section */
        .alphabet-container {
            display: flex;
            flex-wrap: wrap;
            gap: 25px; /* Increased gap */
            justify-content: center;
        }

        .alphabet-card {
            background-color: var(--card-bg);
            border: 2px solid var(--border-color); /* Thicker border */
            border-radius: 10px; /* More rounded */
            box-shadow: 0 5px 15px var(--shadow-color); /* More prominent shadow */
            padding: 25px; /* Increased padding */
            width: calc(33% - 50px); /* Adjust for larger gap */
            box-sizing: border-box;
            display: flex;
            flex-direction: column;
            align-items: center;
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            cursor: default; /* Indicate not clickable as a whole */
        }

        .alphabet-card:hover {
            transform: translateY(-8px); /* More pronounced lift */
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }

        .alphabet-card h3 {
            font-size: 2.8em; /* Much larger letter */
            margin-top: 0;
            margin-bottom: 20px;
            text-align: center;
            width: 100%;
            color: var(--secondary-color); /* Default color for letter */
            transition: color 0.3s ease-in-out;
        }

        /* Dynamic colors for alphabet cards */
        .alphabet-card:nth-child(4n+1) h3 { color: var(--accent-color-1); }
        .alphabet-card:nth-child(4n+2) h3 { color: var(--accent-color-2); }
        .alphabet-card:nth-child(4n+3) h3 { color: var(--accent-color-3); }
        .alphabet-card:nth-child(4n) h3 { color: var(--accent-color-4); }


        .alphabet-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px; /* Increased margin */
        }

        .alphabet-table th, .alphabet-table td {
            border: 1px solid var(--border-color);
            padding: 12px; /* Increased padding */
            text-align: center;
            font-size: 1.05em;
        }

        .alphabet-table th {
            background-color: var(--primary-color);
            color: white;
            font-weight: bold;
        }

        .alphabet-table tr:nth-child(even) {
            background-color: #fcf4f8; /* Lighter even row */
        }

        .alphabet-table tr:hover {
            background-color: #ffe6f2; /* Light pink on hover */
        }

        .english-word {
            cursor: pointer;
            font-weight: bold;
            color: var(--primary-color);
            transition: color 0.2s ease-in-out, text-decoration 0.2s ease-in-out;
        }

        .english-word:hover {
            color: var(--secondary-color);
            text-decoration: underline;
        }

        /* Added for color display in the colors section */
        .color-box {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 1px solid #ccc;
            vertical-align: middle;
            margin-left: 8px; /* Adjusted margin for RTL */
            border-radius: 4px;
        }

        /* Grammar and Tenses Sections */
        .grammar-topic {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 30px; /* Increased padding */
            margin-bottom: 30px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1); /* Softer shadow */
            transition: box-shadow 0.3s ease-in-out;
        }

        .grammar-topic:hover {
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15);
        }

        .grammar-topic h3.speakable-heading {
            cursor: pointer;
            color: var(--primary-color);
            font-size: 2em; /* Larger heading */
            margin-top: 0;
            border-bottom: 2px dashed var(--secondary-color); /* Different dashed line */
            padding-bottom: 12px;
            transition: color 0.2s ease-in-out;
        }

        .grammar-topic h3.speakable-heading:hover {
            color: var(--secondary-color);
        }

        .grammar-text {
            margin-bottom: 20px;
            font-size: 1.1em;
        }

        .grammar-topic ul {
            list-style: none;
            padding-right: 0;
            margin-top: 15px;
        }

        .grammar-topic ul li {
            position: relative;
            padding-right: 30px; /* More space for custom bullet */
            margin-bottom: 12px; /* Increased margin */
            font-size: 1.05em;
        }

        .grammar-topic ul li::before {
            content: '🌟'; /* Star bullet */
            color: var(--secondary-color);
            font-weight: bold;
            position: absolute;
            right: 0;
            font-size: 1.2em;
        }

        .grammar-topic ul ul {
            margin-top: 8px;
            margin-bottom: 8px;
            padding-right: 20px; /* Indent sub-list */
        }

        .grammar-topic ul ul li::before {
            content: '💡'; /* Lightbulb sub-bullet */
            color: var(--accent-color-2);
        }

        .speakable-word {
            cursor: pointer;
            color: var(--primary-color);
            font-weight: bold;
            transition: color 0.2s ease-in-out;
        }

        .speakable-word:hover {
            color: var(--secondary-color);
            text-decoration: underline;
        }

        /* New Common Words Table Styles */
        .info-table-container {
            overflow-x: auto;
            margin-top: 25px; /* Increased margin */
        }

        .info-table {
            width: 100%;
            border-collapse: collapse;
            min-width: 600px; /* Ensure table doesn't get too small on mobile */
        }

        .info-table th,
        .info-table td {
            border: 1px solid var(--border-color);
            padding: 15px; /* More padding */
            text-align: center;
            font-size: 1.05em;
        }

        .info-table thead th {
            background-color: var(--primary-color);
            color: white;
            font-weight: bold;
            font-size: 1.1em;
        }

        .info-table tbody tr:nth-child(even) {
            background-color: #fcf4f8; /* Lighter even row */
        }

        .info-table tbody tr:hover {
            background-color: #ffe6f2; /* Light pink on hover */
        }
        
        footer {
            text-align: center;
            padding: 25px; /* Increased padding */
            background-image: linear-gradient(to left, var(--primary-color), var(--secondary-color));
            color: white;
            margin-top: 50px;
            border-radius: 0 0 12px 12px;
            box-shadow: 0 -4px 10px var(--shadow-color);
            font-size: 1.1em;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .alphabet-card {
                width: calc(50% - 40px); /* 2 cards per row, adjust for gap */
            }
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2.5em;
            }
            h2 {
                font-size: 2.2em;
            }
            h3 {
                font-size: 1.6em;
            }
            .alphabet-card {
                width: 100%; /* 1 card per row */
            }
            main {
                margin: 20px auto;
                padding: 20px;
            }
            .info-table th,
            .info-table td {
                padding: 10px;
                font-size: 0.9em;
            }
            .grammar-topic ul li {
                padding-right: 25px;
            }
        }

        @media (max-width: 480px) {
            header h1 {
                font-size: 2em;
            }
            h2 {
                font-size: 1.8em;
                margin-bottom: 30px;
            }
            h2::after, h2::before {
                display: none; /* Hide emojis on very small screens */
            }
            h3 {
                font-size: 1.4em;
            }
            .alphabet-table th, .alphabet-table td,
            .info-table th, .info-table td {
                padding: 8px;
                font-size: 0.85em;
            }
            .alphabet-card h3 {
                font-size: 2.5em;
            }
            .grammar-text, .grammar-topic ul li {
                font-size: 1em;
            }
            footer {
                padding: 15px;
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>تعلم الإنجليزية: الأبجدية والقواعد الأساسية</h1>
    </header>

    <main>
        <section id="alphabet-section">
            <h2>الأبجدية الإنجليزية وقائمة الكلمات</h2>
            <p class="instruction">اضغط على أي كلمة إنجليزية لسماع نطقها.</p>
            <div class="alphabet-container" id="alphabet-container">
                </div>
        </section>

        ---

        <section id="pronunciation-rules-section">
            <h2>قواعد النطق (Pronunciation Rules)</h2>
            <p class="instruction">اضغط على أي كلمة إنجليزية لسماع نطقها.</p>

            <div class="grammar-topic">
                <h3 class="speakable-heading">1. الحروف المتحركة (Vowels)</h3>
                <p class="grammar-text">الحروف المتحركة الأساسية هي <span class="speakable-word">A</span>, <span class="speakable-word">E</span>, <span class="speakable-word">I</span>, <span class="speakable-word">O</span>, <span class="speakable-word">U</span>. كل حرف متحرك يمكن أن يكون له نطق قصير أو طويل، بالإضافة إلى أصوات أخرى.</p>
                <ul>
                    <li>**حرف <span class="speakable-word">A</span>:**
                        <ul>
                            <li>**صوت قصير:** مثل كلمة <span class="speakable-word">cat</span> (a مثل فتحة).</li>
                            <li>**صوت طويل:** مثل كلمة <span class="speakable-word">name</span> (a مثل أي).</li>
                            <li>**أصوات أخرى:** مثل كلمة <span class="speakable-word">car</span> (a مثل آ) أو <span class="speakable-word">ball</span> (a مثل أو).</li>
                        </ul>
                    </li>
                    <li>**حرف <span class="speakable-word">E</span>:**
                        <ul>
                            <li>**صوت قصير:** مثل كلمة <span class="speakable-word">bed</span> (e مثل كسرة خفيفة).</li>
                            <li>**صوت طويل:** مثل كلمة <span class="speakable-word">tree</span> (e مثل ياء طويلة).</li>
                        </ul>
                    </li>
                    <li>**حرف <span class="speakable-word">I</span>:**
                        <ul>
                            <li>**صوت قصير:** مثل كلمة <span class="speakable-word">pig</span> (i مثل كسرة).</li>
                            <li>**صوت طويل:** مثل كلمة <span class="speakable-word">bike</span> (i مثل آي).</li>
                        </ul>
                    </li>
                    <li>**حرف <span class="speakable-word">O</span>:**
                        <ul>
                            <li>**صوت قصير:** مثل كلمة <span class="speakable-word">dog</span> (o مثل ضمة خفيفة).</li>
                            <li>**صوت طويل:** مثل كلمة <span class="speakable-word">boat</span> (o مثل او).</li>
                        </ul>
                    </li>
                    <li>**حرف <span class="speakable-word">U</span>:**
                        <ul>
                            <li>**صوت قصير:** مثل كلمة <span class="speakable-word">sun</span> (u مثل فتحة قوية).</li>
                            <li>**صوت طويل:** مثل كلمة <span class="speakable-word">blue</span> (u مثل يو) أو <span class="speakable-word">flute</span> (u مثل أو).</li>
                        </ul>
                    </li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">2. الحروف الساكنة (Consonants)</h3>
                <p class="grammar-text">معظم الحروف الساكنة لها نطق واحد أو بضعة نطقات شائعة. إليك بعض الأمثلة على الحروف الساكنة التي قد تسبب التباساً في النطق:</p>
                <ul>
                    <li>**حرف <span class="speakable-word">C</span>:**
                        <ul>
                            <li>**ينطق كـ <span class="speakable-word">S</span>:** عندما يتبعه <span class="speakable-word">E</span>, <span class="speakable-word">I</span>, <span class="speakable-word">Y</span>. أمثلة: <span class="speakable-word">city</span>, <span class="speakable-word">face</span>.</li>
                            <li>**ينطق كـ <span class="speakable-word">K</span>:** في معظم الحالات الأخرى. أمثلة: <span class="speakable-word">cat</span>, <span class="speakable-word">car</span>.</li>
                        </ul>
                    </li>
                    <li>**حرف <span class="speakable-word">G</span>:**
                        <ul>
                            <li>**ينطق كـ <span class="speakable-word">J</span>:** عندما يتبعه <span class="speakable-word">E</span>, <span class="speakable-word">I</span>, <span class="speakable-word">Y</span> (ولكن هناك استثناءات!). أمثلة: <span class="speakable-word">giant</span>, <span class="speakable-word">gym</span>.</li>
                            <li>**ينطق كـ <span class="speakable-word">غ</span>:** في معظم الحالات الأخرى. أمثلة: <span class="speakable-word">go</span>, <span class="speakable-word">game</span>.</li>
                        </ul>
                    </li>
                    <li>**حرف <span class="speakable-word">S</span>:**
                        <ul>
                            <li>**ينطق كـ <span class="speakable-word">س</span>:** أمثلة: <span class="speakable-word">sun</span>, <span class="speakable-word">sit</span>.</li>
                            <li>**ينطق كـ <span class="speakable-word">ز</span>:** أحياناً في نهاية الكلمات أو بين حرفين متحركين. أمثلة: <span class="speakable-word">is</span>, <span class="speakable-word">bags</span>.</li>
                        </ul>
                    </li>
                    <li>**حرف <span class="speakable-word">K</span> و <span class="speakable-word">N</span>:** عندما يأتي <span class="speakable-word">K</span> قبل <span class="speakable-word">N</span> في بداية الكلمة، يكون حرف <span class="speakable-word">K</span> صامتاً. أمثلة: <span class="speakable-word">know</span>, <span class="speakable-word">knife</span>.</li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">3. الحروف المركبة (Diphthongs and Consonant Digraphs)</h3>
                <p class="grammar-text">الحروف المركبة هي مجموعات من حرفين أو أكثر تنتج صوتاً واحداً. قد تكون حروفاً متحركة مركبة (diphthongs) أو حروفاً ساكنة مركبة (consonant digraphs).</p>
                <ul>
                    <li>**الحروف المتحركة المركبة (Diphthongs):**
                        <ul>
                            <li>**<span class="speakable-word">OU</span> / <span class="speakable-word">OW</span>:** مثل كلمة <span class="speakable-word">house</span>, <span class="speakable-word">cow</span> (صوت "او" عميق).</li>
                            <li>**<span class="speakable-word">OI</span> / <span class="speakable-word">OY</span>:** مثل كلمة <span class="speakable-word">coin</span>, <span class="speakable-word">boy</span> (صوت "أوي").</li>
                            <li>**<span class="speakable-word">EA</span>:** يمكن أن يكون له عدة أصوات. أمثلة: <span class="speakable-word">read</span> (يقرأ - ياء طويلة), <span class="speakable-word">bread</span> (خبز - كسرة خفيفة), <span class="speakable-word">great</span> (عظيم - إي).</li>
                        </ul>
                    </li>
                    <li>**الحروف الساكنة المركبة (Consonant Digraphs):**
                        <ul>
                            <li>**<span class="speakable-word">CH</span>:** مثل كلمة <span class="speakable-word">chair</span> (صوت "تش").</li>
                            <li>**<span class="speakable-word">SH</span>:** مثل كلمة <span class="speakable-word">shoe</span> (صوت "ش").</li>
                            <li>**<span class="speakable-word">TH</span>:** يمكن أن يكون له صوتان:
                                <ul>
                                    <li>**صوت مسموع (voiced):** مثل كلمة <span class="speakable-word">this</span>, <span class="speakable-word">that</span> (مثل الذال).</li>
                                    <li>**صوت غير مسموع (unvoiced):** مثل كلمة <span class="speakable-word">think</span>, <span class="speakable-word">three</span> (مثل الثاء).</li>
                                </ul>
                            </li>
                            <li>**<span class="speakable-word">PH</span>:** ينطق مثل <span class="speakable-word">F</span>. أمثلة: <span class="speakable-word">phone</span>, <span class="speakable-word">elephant</span>.</li>
                            <li>**<span class="speakable-word">WH</span>:** في معظم الكلمات، ينطق مثل <span class="speakable-word">W</span>. أمثلة: <span class="speakable-word">what</span>, <span class="speakable-word">when</span>. (في بعض اللهجات، قد ينطق صوت "هو" خفيف).</li>
                        </ul>
                    </li>
                </ul>
            </div>
        </section>

        ---

        <section id="cardinal-numbers-section">
            <h2>الأعداد الأساسية (Cardinal Numbers)</h2>
            <p class="instruction">اضغط على أي كلمة إنجليزية لسماع نطقها.</p>
            <div class="info-table-container">
                <table class="info-table">
                    <thead>
                        <tr>
                            <th>العدد</th>
                            <th>الإنجليزية</th>
                            <th>العدد</th>
                            <th>الإنجليزية</th>
                            <th>العدد</th>
                            <th>الإنجليزية</th>
                            <th>العدد</th>
                            <th>الإنجليزية</th>
                            <th>العدد</th>
                            <th>الإنجليزية</th>
                        </tr>
                    </thead>
                    <tbody id="cardinal-numbers-tbody">
                        </tbody>
                </table>
            </div>
        </section>

        ---

        <section id="ordinal-numbers-section">
            <h2>الأعداد الترتيبية (Ordinal Numbers)</h2>
            <p class="instruction">اضغط على أي كلمة إنجليزية لسماع نطقها.</p>
            <div class="info-table-container">
                <table class="info-table">
                    <thead>
                        <tr>
                            <th>الترتيب</th>
                            <th>الإنجليزية</th>
                            <th>الترتيب</th>
                            <th>الإنجليزية</th>
                            <th>الترتيب</th>
                            <th>الإنجليزية</th>
                            <th>الترتيب</th>
                            <th>الإنجليزية</th>
                            <th>الترتيب</th>
                            <th>الإنجليزية</th>
                        </tr>
                    </thead>
                    <tbody id="ordinal-numbers-tbody">
                        </tbody>
                </table>
            </div>
        </section>

        ---

        <section id="colors-section">
            <h2>الألوان في اللغة الإنجليزية</h2>
            <p class="instruction">اضغط على أي كلمة إنجليزية لسماع نطقها.</p>
            <div class="info-table-container">
                <table class="info-table">
                    <thead>
                        <tr>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                            <th>اللون</th>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                            <th>اللون</th>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                            <th>اللون</th>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                            <th>اللون</th>
                        </tr>
                    </thead>
                    <tbody id="colors-tbody">
                        </tbody>
                </table>
            </div>
        </section>

        ---

        <section id="grammar-section">
            <h2>شرح القواعد الأساسية في اللغة الإنجليزية</h2>

            <div class="grammar-topic">
                <h3 class="speakable-heading">1. الأفعال المساعدة (Auxiliary Verbs / Helping Verbs)</h3>
                <p class="grammar-text">الأفعال المساعدة هي أفعال تُستخدم مع الأفعال الرئيسية لتكوين الأزمنة المختلفة، السؤال، النفي، والتعبير عن الإمكانية، الوجوب، أو القدرة. أهم الأفعال المساعدة هي: <span class="speakable-word">be</span>، <span class="speakable-word">do</span>، و <span class="speakable-word">have</span>.</p>
                <ul>
                    <li>**Be (يكون):** يُستخدم لتكوين الأزمنة المستمرة والمبني للمجهول. أشكاله: <span class="speakable-word">am</span>, <span class="speakable-word">is</span>, <span class="speakable-word">are</span>, <span class="speakable-word">was</span>, <span class="speakable-word">were</span>, <span class="speakable-word">been</span>, <span class="speakable-word">being</span>.
                        <ul>
                            <li>**أمثلة:** He <span class="speakable-word">is</span> reading a book. (هو يقرأ كتاباً.) The car <span class="speakable-word">was</span> repaired. (تم إصلاح السيارة.)</li>
                        </ul>
                    </li>
                    <li>**Do (يفعل):** يُستخدم في صياغة النفي والسؤال في الأزمنة البسيطة وللتأكيد. أشكاله: <span class="speakable-word">do</span>, <span class="speakable-word">does</span>, <span class="speakable-word">did</span>.
                        <ul>
                            <li>**أمثلة:** <span class="speakable-word">Do</span> you like coffee? (هل تحب القهوة؟) She <span class="speakable-word">doesn't</span> speak French. (هي لا تتحدث الفرنسية.)</li>
                        </ul>
                    </li>
                    <li>**Have (يملك):** يُستخدم لتكوين الأزمنة التامة. أشكاله: <span class="speakable-word">have</span>, <span class="speakable-word">has</span>, <span class="speakable-word">had</span>.
                        <ul>
                            <li>**أمثلة:** I <span class="speakable-word">have</span> finished my work. (لقد أنهيت عملي.) She <span class="speakable-word">has</span> visited Paris. (لقد زارت باريس.)</li>
                        </ul>
                    </li>
                    <li>**الأفعال المساعدة المشروطة (Modal Auxiliary Verbs):** تعبر عن القدرة، الإمكانية، الوجوب، النصيحة، إلخ. أمثلة: <span class="speakable-word">can</span>, <span class="speakable-word">could</span>, <span class="speakable-word">may</span>, <span class="speakable-word">might</span>, <span class="speakable-word">must</span>, <span class="speakable-word">shall</span>, <span class="speakable-word">should</span>, <span class="speakable-word">will</span>, <span class="speakable-word">would</span>.
                        <ul>
                            <li>**أمثلة:** I <span class="speakable-word">can</span> swim. (أستطيع السباحة.) You <span class="speakable-word">should</span> study hard. (يجب أن تدرس بجد.)</li>
                        </ul>
                    </li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">2. الأفعال الأساسية (Main Verbs)</h3>
                <p class="grammar-text">الأفعال الأساسية هي الأفعال التي تحمل المعنى الرئيسي للجملة وتصف الحدث أو الحالة. يمكن أن تكون الأفعال الأساسية <span class="speakable-word">أفعال حركة (action verbs)</span> أو <span class="speakable-word">أفعال حالة (state verbs)</span>.</p>
                <ul>
                    <li>**أمثلة على أفعال الحركة:** <span class="speakable-word">run</span> (يجري), <span class="speakable-word">eat</span> (يأكل), <span class="speakable-word">sleep</span> (ينام), <span class="speakable-word">write</span> (يكتب), <span class="speakable-word">walk</span> (يمشي).
                        <ul>
                            <li>**أمثلة:** She <span class="speakable-word">eats</span> an apple. (هي تأكل تفاحة.) He <span class="speakable-word">runs</span> fast. (هو يجري بسرعة.)</li>
                        </ul>
                    </li>
                    <li>**أمثلة على أفعال الحالة:** <span class="speakable-word">be</span> (يكون), <span class="speakable-word">seem</span> (يبدو), <span class="speakable-word">feel</span> (يشعر), <span class="speakable-word">know</span> (يعرف), <span class="speakable-word">believe</span> (يؤمن).
                        <ul>
                            <li>**أمثلة:** She <span class="speakable-word">is</span> happy. (هي سعيدة.) He <span class="speakable-word">knows</span> the answer. (هو يعرف الإجابة.)</li>
                        </ul>
                    </li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">3. الضمائر (Pronouns)</h3>
                <p class="grammar-text">الضمائر هي كلمات تحل محل الأسماء لتجنب تكرارها. تُقسم إلى عدة أنواع:</p>
                <ul>
                    <li>** ضمائر الفاعل (Subject Pronouns):** تحل محل الاسم الذي يقوم بالفعل.
                        <ul>
                            <li><span class="speakable-word">I</span> (أنا), <span class="speakable-word">you</span> (أنت/أنتم), <span class="speakable-word">he</span> (هو), <span class="speakable-word">she</span> (هي), <span class="speakable-word">it</span> (هو/هي لغير العاقل), <span class="speakable-word">we</span> (نحن), <span class="speakable-word">they</span> (هم/هن).</li>
                            <li>**أمثلة:** <span class="speakable-word">She</span> is my sister. (هي أختي.) <span class="speakable-word">They</span> live in Cairo. (هم يعيشون في القاهرة.)</li>
                        </ul>
                    </li>
                    <li>** ضمائر المفعول به (Object Pronouns):** تحل محل الاسم الذي يقع عليه الفعل.
                        <ul>
                            <li><span class="speakable-word">me</span> (لي/إياي), <span class="speakable-word">you</span> (لك/إياك), <span class="speakable-word">him</span> (له/إياه), <span class="speakable-word">her</span> (لها/إياها), <span class="speakable-word">it</span> (له/إياه لغير العاقل), <span class="speakable-word">us</span> (لنا/إيانا), <span class="speakable-word">them</span> (لهم/إياهم).</li>
                            <li>**أمثلة:** He gave the book to <span class="speakable-word">me</span>. (أعطاني الكتاب.) I saw <span class="speakable-word">him</span> yesterday. (رأيته أمس.)</li>
                        </ul>
                    </li>
                    <li>** صفات الملكية (Possessive Adjectives):** تأتي قبل الاسم لتوضح ملكيته.
                        <ul>
                            <li><span class="speakable-word">my</span> (ملكي), <span class="speakable-word">your</span> (ملكك/ملككم), <span class="speakable-word">his</span> (ملكه), <span class="speakable-word">her</span> (ملكها), <span class="speakable-word">its</span> (ملكه/ملكها لغير العاقل), <span class="speakable-word">our</span> (ملكنا), <span class="speakable-word">their</span> (ملكهم/ملكهن).</li>
                            <li>**أمثلة:** This is <span class="speakable-word">my</span> car. (هذه سيارتي.) <span class="speakable-word">Their</span> house is big. (منزلهم كبير.)</li>
                        </ul>
                    </li>
                    <li>** ضمائر الملكية (Possessive Pronouns):** تحل محل الاسم وصفة الملكية معاً.
                        <ul>
                            <li><span class="speakable-word">mine</span> (ملكي), <span class="speakable-word">yours</span> (ملكك/ملككم), <span class="speakable-word">himself</span> (نفسه), <span class="speakable-word">hers</span> (ملكها), <span class="speakable-word">its</span> (ملكه/ملكها لغير العاقل), <span class="speakable-word">ours</span> (ملكنا), <span class="speakable-word">theirs</span> (ملكهم/ملكهن).</li>
                            <li>**أمثلة:** This book is <span class="speakable-word">mine</span>. (هذا الكتاب ملكي.) The red car is <span class="speakable-word">theirs</span>. (السيارة الحمراء ملكهم.)</li>
                        </ul>
                    </li>
                    <li>**الضمائر الانعكاسية (Reflexive Pronouns):** تشير إلى الفاعل نفسه.
                        <ul>
                            <li><span class="speakable-word">myself</span> (نفسي), <span class="speakable-word">yourself</span> (نفسك), <span class="speakable-word">himself</span> (نفسه), <span class="speakable-word">herself</span> (نفسها), <span class="speakable-word">itself</span> (نفسها/نفسه لغير العاقل), <span class="speakable-word">ourselves</span> (أنفسنا), <span class="speakable-word">yourselves</span> (أنفسكم), <span class="speakable-word">themselves</span> (أنفسهم/أنفسهن).</li>
                            <li>**أمثلة:** She taught <span class="speakable-word">herself</span> to play guitar. (علمت نفسها العزف على الغيتار.) They built the house <span class="speakable-word">themselves</span>. (بنوا المنزل بأنفسهم.)</li>
                        </ul>
                    </li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">4. الصفات (Adjectives)</h3>
                <p class="grammar-text">الصفات هي كلمات تصف أو تعدل الأسماء والضمائر، وتضيف معلومات عنها مثل اللون، الحجم، الشكل، الحالة، إلخ.</p>
                <ul>
                    <li>عادةً ما تأتي الصفة قبل الاسم الذي تصفه.
                        <ul>
                            <li>**أمثلة:** a <span class="speakable-word">beautiful</span> flower (زهرة جميلة) a <span class="speakable-word">tall</span> building (مبنى طويل) a <span class="speakable-word">red</span> car (سيارة حمراء)</li>
                        </ul>
                    </li>
                    <li>يمكن أن تأتي الصفة بعد أفعال الربط (linking verbs) مثل <span class="speakable-word">be</span>, <span class="speakable-word">seem</span>, <span class="speakable-word">feel</span>, <span class="speakable-word">look</span>, <span class="speakable-word">sound</span>, <span class="speakable-word">smell</span>, <span class="speakable-word">taste</span>, <span class="speakable-word">become</span>, <span class="speakable-word">get</span>.
                        <ul>
                            <li>**أمثلة:** She <span class="speakable-word">is beautiful</span>. (هي جميلة.) The food <span class="speakable-word">tastes delicious</span>. (الطعام مذاقه لذيذ.)</li>
                        </ul>
                    </li>
                </ul>
            </div>
        </section>

        <section id="tenses-section">
            <h2>الأزمنة في اللغة الإنجليزية (Tenses) والكلمات الدالة عليها</h2>
            <p class="instruction">اضغط على أي عنوان زمن أو كلمة إنجليزية لسماع نطقها.</p>

            <div class="grammar-topic">
                <h3 class="speakable-heading">1. زمن المضارع البسيط (Present Simple)</h3>
                <p class="grammar-text">يُستخدم للتعبير عن الحقائق العامة، العادات، والجداول الزمنية.</p>
                <ul>
                    <li>**الاستخدامات:**
                        <ul>
                            <li>الحقائق العامة: The sun <span class="speakable-word">rises</span> in the east. (الشمس تشرق من الشرق.)</li>
                            <li>العادات والروتين: I <span class="speakable-word">drink</span> coffee every morning. (أشرب القهوة كل صباح.)</li>
                        </ul>
                    </li>
                    <li>**الكلمات الدالة:** <span class="speakable-word">always</span>, <span class="speakable-word">usually</span>, <span class="speakable-word">often</span>, <span class="speakable-word">sometimes</span>, <span class="speakable-word">rarely</span>, <span class="speakable-word">never</span>, <span class="speakable-word">every day</span>/<span class="speakable-word">week</span>/<span class="speakable-word">month</span>/<span class="speakable-word">year</span>, <span class="speakable-word">on Mondays</span>, <span class="speakable-word">at weekends</span>.</li>
                    <li>**أمثلة:** She <span class="speakable-word">works</span> in a hospital. (هي تعمل في مستشفى.) We <span class="speakable-word">don't eat</span> meat. (نحن لا نأكل اللحم.) <span class="speakable-word">Does</span> he <span class="speakable-word">play</span> tennis? (هل يلعب التنس؟)</li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">2. زمن المضارع المستمر (Present Continuous)</h3>
                <p class="grammar-text">يُستخدم للتعبير عن أفعال تحدث الآن أو في فترة زمنية مؤقتة حول الوقت الحاضر.</p>
                <ul>
                    <li>**الاستخدامات:**
                        <ul>
                            <li>أفعال تحدث الآن: I <span class="speakable-word">am studying</span> English right now. (أنا أدرس الإنجليزية الآن.)</li>
                            <li>أفعال مؤقتة: He <span class="speakable-word">is working</span> on a new project this month. (هو يعمل على مشروع جديد هذا الشهر.)</li>
                        </ul>
                    </li>
                    <li>**الكلمات الدالة:** <span class="speakable-word">now</span>, <span class="speakable-word">right now</span>, <span class="speakable-word">at the moment</span>, <span class="speakable-word">currently</span>, <span class="speakable-word">today</span>, <span class="speakable-word">this week</span>/<span class="speakable-word">month</span>/<span class="speakable-word">year</span>, <span class="speakable-word">listen!</span>, <span class="speakable-word">look!</span></li>
                    <li>**أمثلة:** They <span class="speakable-word">are watching</span> TV. (هم يشاهدون التلفاز.) She <span class="speakable-word">isn't sleeping</span>. (هي لا تنام.) <span class="speakable-word">Are</span> you <span class="speakable-word">listening</span> to me? (هل تستمع إلي؟)</li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">3. زمن المضارع التام (Present Perfect)</h3>
                <p class="grammar-text">يُستخدم للتعبير عن أفعال بدأت في الماضي ولها تأثير على الحاضر، أو أفعال حدثت في وقت غير محدد في الماضي.</p>
                <ul>
                    <li>**الاستخدامات:**
                        <ul>
                            <li>تجارب سابقة: I <span class="speakable-word">have visited</span> London three times. (لقد زرت لندن ثلاث مرات.)</li>
                            <li>أفعال بدأت في الماضي وما زالت مستمرة: She <span class="speakable-word">has lived</span> here for five years. (لقد عاشت هنا لمدة خمس سنوات.)</li>
                        </ul>
                    </li>
                    <li>**الكلمات الدالة:** <span class="speakable-word">already</span>, <span class="speakable-word">yet</span>, <span class="speakable-word">just</span>, <span class="speakable-word">ever</span>, <span class="speakable-word">never</span>, <span class="speakable-word">since</span>, <span class="speakable-word">for</span>, <span class="speakable-word">so far</span>, <span class="speakable-word">recently</span>, <span class="speakable-word">lately</span>.</li>
                    <li>**أمثلة:** They <span class="speakable-word">have bought</span> a new car. (لقد اشتروا سيارة جديدة.) I <span class="speakable-word">haven't seen</span> him since last week. (لم أره منذ الأسبوع الماضي.) <span class="speakable-word">Have</span> you <span class="speakable-word">ever been</span> to New York? (هل سبق لك أن زرت نيويورك؟)</li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">4. زمن الماضي البسيط (Past Simple)</h3>
                <p class="grammar-text">يُستخدم للتعبير عن أفعال أو أحداث انتهت في وقت محدد في الماضي.</p>
                <ul>
                    <li>**الاستخدامات:**
                        <ul>
                            <li>أحداث منتهية في الماضي: I <span class="speakable-word">went</span> to the cinema yesterday. (ذهبت إلى السينما أمس.)</li>
                            <li>سلسلة من الأحداث في الماضي: She <span class="speakable-word">woke up</span>, <span class="speakable-word">ate</span> breakfast, and <span class="speakable-word">left</span> for work. (استيقظت، أكلت الفطور، وغادرت للعمل.)</li>
                        </ul>
                    </li>
                    <li>**الكلمات الدالة:** <span class="speakable-word">yesterday</span>, <span class="speakable-word">last night</span>/<span class="speakable-word">week</span>/<span class="speakable-word">month</span>/<span class="speakable-word">year</span>, <span class="speakable-word">ago</span>, <span class="speakable-word">in 2005</span>, <span class="speakable-word">when I was young</span>.</li>
                    <li>**أمثلة:** He <span class="speakable-word">played</span> football an hour ago. (لعب كرة القدم قبل ساعة.) We <span class="speakable-word">didn't go</span> to the party. (لم نذهب إلى الحفلة.) <span class="speakable-word">Did</span> you <span class="speakable-word">see</span> her? (هل رأيتها؟)</li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">5. زمن الماضي المستمر (Past Continuous)</h3>
                <p class="grammar-text">يُستخدم للتعبير عن أفعال كانت مستمرة في وقت معين في الماضي، أو لحدث كان مستمراً عندما قطعه حدث آخر.</p>
                <ul>
                    <li>**الاستخدامات:**
                        <ul>
                            <li>حدث كان مستمراً في وقت محدد: At 8 PM yesterday, I <span class="speakable-word">was eating</span> dinner. (في الساعة 8 مساءً أمس، كنت أتناول العشاء.)</li>
                            <li>حدث طويل قطعه حدث قصير: While I <span class="speakable-word">was reading</span>, the phone <span class="speakable-word">rang</span>. (بينما كنت أقرأ، رن الهاتف.)</li>
                        </ul>
                    </li>
                    <li>**الكلمات الدالة:** <span class="speakable-word">while</span>, <span class="speakable-word">when</span>, <span class="speakable-word">as</span>, <span class="speakable-word">all day</span>/<span class="speakable-word">night yesterday</span>, <span class="speakable-word">at that moment</span>.</li>
                    <li>**أمثلة:** They <span class="speakable-word">were waiting</span> for the bus. (كانوا ينتظرون الحافلة.) She <span class="speakable-word">wasn't sleeping</span> when I called. (لم تكن نائمة عندما اتصلت.) What <span class="speakable-word">were</span> you <span class="speakable-word">doing</span> at 10 AM? (ماذا كنت تفعل في الساعة 10 صباحاً؟)</li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">6. زمن الماضي التام (Past Perfect)</h3>
                <p class="grammar-text">يُستخدم للتعبير عن حدث وقع قبل حدث آخر في الماضي.</p>
                <ul>
                    <li>**الاستخدامات:**
                        <ul>
                            <li>حدث سابق لحدث آخر في الماضي: I <span class="speakable-word">had finished</span> my homework before I went out. (كنت قد أنهيت واجبي قبل أن أخرج.)</li>
                            <li>التقرير عن الكلام غير المباشر: He said he <span class="speakable-word">had seen</span> the movie. (قال إنه شاهد الفيلم.)</li>
                        </ul>
                    </li>
                    <li>**الكلمات الدالة:** <span class="speakable-word">before</span>, <span class="speakable-word">after</span>, <span class="speakable-word">by the time</span>, <span class="speakable-word">already</span>, <span class="speakable-word">yet</span>, <span class="speakable-word">when</span>.</li>
                    <li>**أمثلة:** By the time we arrived, they <span class="speakable-word">had left</span>. (بحلول الوقت الذي وصلنا فيه، كانوا قد غادروا.) She <span class="speakable-word">had never seen</span> a snow before she went to Canada. (لم تر الثلج من قبل أن ذهبت إلى كندا.)</li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">7. زمن المستقبل البسيط (Future Simple)</h3>
                <p class="grammar-text">يُستخدم للتعبير عن قرارات سريعة، تنبؤات، وعروض.</p>
                <ul>
                    <li>**الاستخدامات:**
                        <ul>
                            <li>قرارات لحظية: I <span class="speakable-word">will help</span> you. (سأساعدك.)</li>
                            <li>تنبؤات (معتقد شخصي): I think it <span class="speakable-word">will rain</span> tomorrow. (أعتقد أنها ستمطر غداً.)</li>
                        </ul>
                    </li>
                    <li>**الكلمات الدالة:** <span class="speakable-word">tomorrow</span>, <span class="speakable-word">next week</span>/<span class="speakable-word">month</span>/<span class="speakable-word">year</span>, <span class="speakable-word">in the future</span>, <span class="speakable-word">soon</span>, <span class="speakable-word">probably</span>, <span class="speakable-word">I think</span>, <span class="speakable-word">I believe</span>.</li>
                    </ul>
                    <li>**أمثلة:** They <span class="speakable-word">will travel</span> to Spain next year. (سيسافرون إلى إسبانيا العام القادم.) She <span class="speakable-word">won't forget</span> you. (هي لن تنساك.) <span class="speakable-word">Will</span> you <span class="speakable-word">come</span> to the party? (هل ستأتي إلى الحفلة؟)</li>
                </ul>
            </div>

            <div class="grammar-topic">
                <h3 class="speakable-heading">8. المستقبل باستخدام (Be going to)</h3>
                <p class="grammar-text">يُستخدم للتعبير عن خطط ونوايا مستقبلية، أو للتنبؤات المبنية على أدلة واضحة.</p>
                <ul>
                    <li>**الاستخدامات:**
                        <ul>
                            <li>خطط ونوايا: I <span class="speakable-word">am going to buy</span> a new car. (أنا ذاهب لشراء سيارة جديدة.)</li>
                            <li>تنبؤات بناءً على دليل: Look at those clouds! It <span class="speakable-word">is going to rain</span>. (انظر إلى تلك الغيوم! إنها ستمطر.)</li>
                        </ul>
                    </li>
                    <li>**الكلمات الدالة:** <span class="speakable-word">tomorrow</span>, <span class="speakable-word">next week</span>, <span class="speakable-word">soon</span>, <span class="speakable-word">in the near future</span>, <span class="speakable-word">I've decided</span>.</li>
                    <li>**أمثلة:** We <span class="speakable-word">are going to visit</span> our grandparents. (سنزور أجدادنا.) He <span class="speakable-word">isn't going to study</span> for the exam. (هو لن يدرس للامتحان.) <span class="speakable-word">Are</span> you <span class="speakable-word">going to watch</span> the movie? (هل ستشاهد الفيلم؟)</li>
                </ul>
            </div>
        </section>

        ---

        <section id="common-words-section">
            <h2>كلمات إنجليزية شائعة ومعانيها</h2>
            <p class="instruction">اضغط على أي كلمة إنجليزية لسماع نطقها.</p>
            <div class="info-table-container">
                <table class="info-table">
                    <thead>
                        <tr>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                        </tr>
                    </thead>
                    <tbody id="common-words-tbody">
                        </tbody>
                </table>
            </div>
        </section>

    </main>


    <script>
        // JavaScript Code
        document.addEventListener('DOMContentLoaded', () => {
            const alphabetData = {
                'A': [
                    { en: 'Apple', ar: 'تفاحة' }, { en: 'Ant', ar: 'نملة' }, { en: 'All', ar: 'كل' },
                    { en: 'Ask', ar: 'يسأل' }, { en: 'Art', ar: 'فن' }, { en: 'Arm', ar: 'ذراع' },
                    { en: 'Age', ar: 'عمر' }, { en: 'Air', ar: 'هواء' }, { en: 'Able', ar: 'قادر' },
                    { en: 'Act', ar: 'فعل' }, { en: 'Ace', ar: 'ممتاز' }, { en: 'Aid', ar: 'مساعدة' },
                    { en: 'Aim', ar: 'هدف' }, { en: 'Ale', ar: 'جعة' }, { en: 'Ape', ar: 'قرد' },
                    { en: 'Arc', ar: 'قوس' }, { en: 'Are', ar: 'يكون (للمتعدد)' }, { en: 'Ash', ar: 'رماد' },
                    { en: 'Awe', ar: 'رهبة' }, { en: 'Axis', ar: 'محور' }, { en: 'Award', ar: 'جائزة' },
                    { en: 'Aware', ar: 'مدرك' }, { en: 'Away', ar: 'بعيد' }, { en: 'Awake', ar: 'مستيقظ' },
                    { en: 'Adapt', ar: 'يتكيف' }
                ],
                'B': [
                    { en: 'Ball', ar: 'كرة' }, { en: 'Book', ar: 'كتاب' }, { en: 'Big', ar: 'كبير' },
                    { en: 'Blue', ar: 'أزرق' }, { en: 'Boy', ar: 'ولد' }, { en: 'Bird', ar: 'طائر' },
                    { en: 'Bake', ar: 'يخبز' }, { en: 'Bank', ar: 'بنك' }, { en: 'Bear', ar: 'دب' },
                    { en: 'Bed', ar: 'سرير' }, { en: 'Bee', ar: 'نحلة' }, { en: 'Bell', ar: 'جرس' },
                    { en: 'Belt', ar: 'حزام' }, { en: 'Bench', ar: 'مقعد' }, { en: 'Bend', ar: 'ينحني' },
                    { en: 'Best', ar: 'الأفضل' }, { en: 'Bet', ar: 'رهان' }, { en: 'Bike', ar: 'دراجة' },
                    { en: 'Bill', ar: 'فاتورة' }, { en: 'Bind', ar: 'يربط' }, { en: 'Bite', ar: 'يعض' },
                    { en: 'Black', ar: 'أسود' }, { en: 'Blend', ar: 'يمزج' }, { en: 'Block', ar: 'كتلة' },
                    { en: 'Blood', ar: 'دم' }
                ],
                'C': [
                    { en: 'Cat', ar: 'قطة' }, { en: 'Car', ar: 'سيارة' }, { en: 'Cup', ar: 'كوب' },
                    { en: 'Cold', ar: 'بارد' }, { en: 'City', ar: 'مدينة' }, { en: 'Cake', ar: 'كعكة' },
                    { en: 'Call', ar: 'ينادي' }, { en: 'Calm', ar: 'هادئ' }, { en: 'Camp', ar: 'مخيم' },
                    { en: 'Can', ar: 'يستطيع / علبة' }, { en: 'Cap', ar: 'قبعة' }, { en: 'Card', ar: 'بطاقة' },
                    { en: 'Care', ar: 'رعاية' }, { en: 'Case', ar: 'حقيبة / حالة' }, { en: 'Cast', ar: 'يرمي / طاقم' },
                    { en: 'Catch', ar: 'يمسك' }, { en: 'Cave', ar: 'كهف' }, { en: 'Cell', ar: 'خلية' },
                    { en: 'Cent', ar: 'سنت' }, { en: 'Chain', ar: 'سلسلة' }, { en: 'Chair', ar: 'كرسي' },
                    { en: 'Chalk', ar: 'طباشير' }, { en: 'Charm', ar: 'سحر' }, { en: 'Chart', ar: 'رسم بياني' },
                    { en: 'Chase', ar: 'يطارد' }
                ],
                'D': [
                    { en: 'Dog', ar: 'كلب' }, { en: 'Door', ar: 'باب' }, { en: 'Day', ar: 'يوم' },
                    { en: 'Dark', ar: 'مظلم' }, { en: 'Dream', ar: 'حلم' }, { en: 'Dance', ar: 'يرقص' },
                    { en: 'Dare', ar: 'يتجرأ' }, { en: 'Dash', ar: 'يندفع' }, { en: 'Date', ar: 'تاريخ / تمر' },
                    { en: 'Dawn', ar: 'فجر' }, { en: 'Deal', ar: 'صفقة' }, { en: 'Dear', ar: 'عزيز' },
                    { en: 'Debt', ar: 'دين' }, { en: 'Deck', ar: 'سطح' }, { en: 'Deep', ar: 'عميق' },
                    { en: 'Deer', ar: 'غزال' }, { en: 'Defy', ar: 'يتحدى' }, { en: 'Delay', ar: 'تأخير' },
                    { en: 'Dent', ar: 'انبعاج' }, { en: 'Desk', ar: 'مكتب' }, { en: 'Dew', ar: 'ندى' },
                    { en: 'Dial', ar: 'يطلب (رقم)' }, { en: 'Dice', ar: 'نرد' }, { en: 'Diet', ar: 'حمية' },
                    { en: 'Dig', ar: 'يحفر' }
                ],
                'E': [
                    { en: 'Elephant', ar: 'فيل' }, { en: 'Egg', ar: 'بيضة' }, { en: 'Eye', ar: 'عين' },
                    { en: 'Eat', ar: 'يأكل' }, { en: 'Earth', ar: 'أرض' }, { en: 'Ear', ar: 'أذن' },
                    { en: 'Early', ar: 'مبكر' }, { en: 'Ease', ar: 'سهولة' }, { en: 'East', ar: 'شرق' },
                    { en: 'Echo', ar: 'صدى' }, { en: 'Edge', ar: 'حافة' }, { en: 'Edit', ar: 'يحرر' },
                    { en: 'Eel', ar: 'ثعبان البحر' }, { en: 'Eject', ar: 'يقذف' }, { en: 'Elder', ar: 'أكبر سناً' },
                    { en: 'Elect', ar: 'ينتخب' }, { en: 'Empty', ar: 'فارغ' }, { en: 'End', ar: 'نهاية' },
                    { en: 'Enjoy', ar: 'يستمتع' }, { en: 'Enter', ar: 'يدخل' }, { en: 'Equal', ar: 'متساوٍ' },
                    { en: 'Even', ar: 'حتى / مسطح' }, { en: 'Ever', ar: 'دائماً' }, { en: 'Every', ar: 'كل' },
                    { en: 'Exact', ar: 'دقيق' }
                ],
                'F': [
                    { en: 'Fish', ar: 'سمكة' }, { en: 'Flower', ar: 'زهرة' }, { en: 'Fast', ar: 'سريع' },
                    { en: 'Fun', ar: 'ممتع' }, { en: 'Friend', ar: 'صديق' }, { en: 'Face', ar: 'وجه' },
                    { en: 'Fact', ar: 'حقيقة' }, { en: 'Fade', ar: 'يتلاشى' }, { en: 'Fail', ar: 'يفشل' },
                    { en: 'Fair', ar: 'عادل / معرض' }, { en: 'Fall', ar: 'يسقط / خريف' }, { en: 'False', ar: 'خطأ' },
                    { en: 'Fame', ar: 'شهرة' }, { en: 'Fan', ar: 'مروحة / معجب' }, { en: 'Farm', ar: 'مزرعة' },
                    { en: 'Far', ar: 'بعيد' }, { en: 'Fat', ar: 'سمين' }, { en: 'Fault', ar: 'خطأ / عيب' },
                    { en: 'Fear', ar: 'خوف' }, { en: 'Feast', ar: 'وليمة' }, { en: 'Feel', ar: 'يشعر' },
                    { en: 'Feet', ar: 'أقدام' }, { en: 'Fell', ar: 'سقط (ماضي)' }, { en: 'Felt', ar: 'شعر (ماضي)' },
                    { en: 'Fence', ar: 'سياج' }
                ],
                'G': [
                    { en: 'Girl', ar: 'فتاة' }, { en: 'Green', ar: 'أخضر' }, { en: 'Game', ar: 'لعبة' },
                    { en: 'Good', ar: 'جيد' }, { en: 'Go', ar: 'يذهب' }, { en: 'Gate', ar: 'بوابة' },
                    { en: 'Gather', ar: 'يجمع' }, { en: 'Gay', ar: 'مرح' }, { en: 'Gaze', ar: 'يحدق' },
                    { en: 'Gear', ar: 'ترس / معدات' }, { en: 'Gem', ar: 'جوهرة' }, { en: 'Gene', ar: 'جين' },
                    { en: 'Get', ar: 'يحصل على' }, { en: 'Ghost', ar: 'شبح' }, { en: 'Giant', ar: 'عملاق' },
                    { en: 'Gift', ar: 'هدية' }, { en: 'Gird', ar: 'يحزم' }, { en: 'Give', ar: 'يعطي' },
                    { en: 'Glad', ar: 'سعيد' }, { en: 'Glass', ar: 'زجاج / كوب' }, { en: 'Glim', ar: 'وميض' },
                    { en: 'Glide', ar: 'ينزلق' }, { en: 'Globe', ar: 'كرة أرضية' }, { en: 'Gloom', ar: 'كآبة' },
                    { en: 'Glory', ar: 'مجد' }
                ],
                'H': [
                    { en: 'House', ar: 'منزل' }, { en: 'Hand', ar: 'يد' }, { en: 'Happy', ar: 'سعيد' },
                    { en: 'Hot', ar: 'حار' }, { en: 'Hear', ar: 'يسمع' }, { en: 'Hair', ar: 'شعر' },
                    { en: 'Halt', ar: 'يتوقف' }, { en: 'Ham', ar: 'لحم خنزير' }, { en: 'Hang', ar: 'يعلق' },
                    { en: 'Hard', ar: 'صعب' }, { en: 'Harm', ar: 'ضرر' }, { en: 'Hat', ar: 'قبعة' },
                    { en: 'Hate', ar: 'يكره' }, { en: 'Have', ar: 'يملك' }, { en: 'Hay', ar: 'تبن' },
                    { en: 'Head', ar: 'رأس' }, { en: 'Heal', ar: 'يشفى' }, { en: 'Heap', ar: 'كومة' },
                    { en: 'Heart', ar: 'قلب' }, { en: 'Heat', ar: 'حرارة' }, { en: 'Heavy', ar: 'ثقيل' },
                    { en: 'Heck', ar: 'جحيم (للتعبير)' }, { en: 'Heel', ar: 'كعب' }, { en: 'Heir', ar: 'وريث' },
                    { en: 'Help', ar: 'مساعدة' }
                ],
                'I': [
                    { en: 'Ice', ar: 'ثلج' }, { en: 'Idea', ar: 'فكرة' }, { en: 'Inside', ar: 'داخل' },
                    { en: 'Iron', ar: 'حديد / يكوي' }, { en: 'Island', ar: 'جزيرة' }, { en: 'I', ar: 'أنا' },
                    { en: 'If', ar: 'إذا' }, { en: 'Ill', ar: 'مريض' }, { en: 'Impry', ar: 'يشير ضمنًا' },
                    { en: 'In', ar: 'في' }, { en: 'Inch', ar: 'بوصة' }, { en: 'Info', ar: 'معلومات' },
                    { en: 'Ink', ar: 'حبر' }, { en: 'Inn', ar: 'نزل' }, { en: 'Input', ar: 'إدخال' },
                    { en: 'Inst', ar: 'فوري' }, { en: 'Into', ar: 'إلى' }, { en: 'Invent', ar: 'يخترع' },
                    { en: 'Invite', ar: 'يدعو' }, { en: 'Iris', ar: 'قزحية' }, { en: 'Irony', ar: 'سخرية' },
                    { en: 'Is', ar: 'يكون (للمفرد)' }, { en: 'Issue', ar: 'قضية' }, { en: 'Item', ar: 'عنصر' },
                    { en: 'Itself', ar: 'نفسها / نفسه' }
                ],
                'J': [
                    { en: 'Jump', ar: 'يقفز' }, { en: 'Joy', ar: 'فرح' }, { en: 'Jelly', ar: 'جيلي' },
                    { en: 'Job', ar: 'وظيفة' }, { en: 'Jet', ar: 'نفاثة' }, { en: 'Jack', ar: 'رافعة / جاك' },
                    { en: 'Jam', ar: 'مربى / زحام' }, { en: 'Jaw', ar: 'فك' }, { en: 'Jazz', ar: 'جاز' },
                    { en: 'Jeer', ar: 'يهزأ' }, { en: 'Jest', ar: 'مزحة' }, { en: 'Jewel', ar: 'جوهرة' },
                    { en: 'Jinx', ar: 'نحس' }, { en: 'Jive', ar: 'يرقص' }, { en: 'Jog', ar: 'يهرول' },
                    { en: 'Join', ar: 'ينضم' }, { en: 'Joint', ar: 'مفصل' }, { en: 'Joke', ar: 'نكتة' },
                    { en: 'Jolt', ar: 'صدمة' }, { en: 'Judge', ar: 'قاضي / يحكم' }, { en: 'Juice', ar: 'عصير' },
                    { en: 'July', ar: 'يوليو' }, { en: 'June', ar: 'يونيو' }, { en: 'Jury', ar: 'هيئة محلفين' },
                    { en: 'Just', ar: 'فقط / عادل' }
                ],
                'K': [
                    { en: 'King', ar: 'ملك' }, { en: 'Key', ar: 'مفتاح' }, { en: 'Kite', ar: 'طائرة ورقية' },
                    { en: 'Kiss', ar: 'يقبل' }, { en: 'Knife', ar: 'سكين' }, { en: 'Keep', ar: 'يحتفظ' },
                    { en: 'Keen', ar: 'حاد / متحمس' }, { en: 'Ken', ar: 'معرفة' }, { en: 'Kepi', ar: 'قبعة عسكرية' },
                    { en: 'Kernel', ar: 'نواة' }, { en: 'Ketchup', ar: 'كاتشب' }, { en: 'Kettle', ar: 'غلاية' },
                    { en: 'Kick', ar: 'يركل' }, { en: 'Kid', ar: 'طفل' }, { en: 'Kill', ar: 'يقتل' },
                    { en: 'Kind', ar: 'نوع / طيب' }, { en: 'Kin', ar: 'أقارب' }, { en: 'Kiss', ar: 'قبلة' },
                    { en: 'Kit', ar: 'طقم' }, { en: 'Knee', ar: 'ركبة' }, { en: 'Kneel', ar: 'يركع' },
                    { en: 'Knew', ar: 'عرف (ماضي)' }, { en: 'Knit', ar: 'يحبك' }, { en: 'Knock', ar: 'يطرق' },
                    { en: 'Knot', ar: 'عقدة' }
                ],
                'L': [
                    { en: 'Lion', ar: 'أسد' }, { en: 'Light', ar: 'ضوء / خفيف' }, { en: 'Love', ar: 'حب' },
                    { en: 'Live', ar: 'يعيش' }, { en: 'Long', ar: 'طويل' }, { en: 'Lady', ar: 'سيدة' },
                    { en: 'Lake', ar: 'بحيرة' }, { en: 'Lamp', ar: 'مصباح' }, { en: 'Land', ar: 'أرض / يهبط' },
                    { en: 'Lap', ar: 'حضن / دورة' }, { en: 'Large', ar: 'كبير' }, { en: 'Last', ar: 'أخير / يدوم' },
                    { en: 'Late', ar: 'متأخر' }, { en: 'Laugh', ar: 'يضحك' }, { en: 'Lay', ar: 'يضع' },
                    { en: 'Lead', ar: 'يقود / رصاص' }, { en: 'Leaf', ar: 'ورقة شجر' }, { en: 'Lean', ar: 'يتكئ / نحيل' },
                    { en: 'Leap', ar: 'يقفز' }, { en: 'Learn', ar: 'يتعلم' }, { en: 'Least', ar: 'الأقل' },
                    { en: 'Leave', ar: 'يغادر / يترك' }, { en: 'Led', ar: 'قاد (ماضي)' }, { en: 'Left', ar: 'يسار / غادر (ماضي)' },
                    { en: 'Leg', ar: 'ساق' }
                ],
                'M': [
                    { en: 'Monkey', ar: 'قرد' }, { en: 'Moon', ar: 'قمر' }, { en: 'Man', ar: 'رجل' },
                    { en: 'More', ar: 'أكثر' }, { en: 'Make', ar: 'يصنع' }, { en: 'Mad', ar: 'غاضب / مجنون' },
                    { en: 'Made', ar: 'صنع (ماضي)' }, { en: 'Mail', ar: 'بريد' }, { en: 'Main', ar: 'رئيسي' },
                    { en: 'Male', ar: 'ذكر' }, { en: 'Malt', ar: 'شعير' }, { en: 'Mama', ar: 'ماما' },
                    { en: 'Map', ar: 'خريطة' }, { en: 'Mark', ar: 'علامة' }, { en: 'Mash', ar: 'يهرس' },
                    { en: 'Mask', ar: 'قناع' }, { en: 'Mass', ar: 'كتلة / قداس' }, { en: 'Mast', ar: 'سارية' },
                    { en: 'Mat', ar: 'حصيرة' }, { en: 'Match', ar: 'مباراة / يطابق' }, { en: 'Mate', ar: 'رفيق / يتزاوج' },
                    { en: 'Max', ar: 'أقصى' }, { en: 'May', ar: 'قد / مايو' }, { en: 'Maze', ar: 'متاهة' },
                    { en: 'Mead', ar: 'شراب العسل' }
                ],
                'N': [
                    { en: 'Nose', ar: 'أنف' }, { en: 'Night', ar: 'ليل' }, { en: 'New', ar: 'جديد' },
                    { en: 'Name', ar: 'اسم' }, { en: 'Next', ar: 'التالي' }, { en: 'Nail', ar: 'مسمار / ظفر' },
                    { en: 'Naked', ar: 'عارٍ' }, { en: 'Nap', ar: 'قيلولة' }, { en: 'Nasty', ar: 'سيء / قذر' },
                    { en: 'Naught', ar: 'لا شيء' }, { en: 'Near', ar: 'قريب' }, { en: 'Neat', ar: 'أنيق / مرتب' },
                    { en: 'Neck', ar: 'رقبة' }, { en: 'Need', ar: 'يحتاج' }, { en: 'Needle', ar: 'إبرة' },
                    { en: 'Nerve', ar: 'عصب' }, { en: 'Nest', ar: 'عش' }, { en: 'Net', ar: 'شبكة' },
                    { en: 'Never', ar: 'أبداً' }, { en: 'Newt', ar: 'سمندل' }, { en: 'Nice', ar: 'لطيف' },
                    { en: 'Nick', ar: 'شق / يخدش' }, { en: 'Nifty', ar: 'أنيق' }, { en: 'Night', ar: 'ليل' }
                ],
                'O': [
                    { en: 'Orange', ar: 'برتقال' }, { en: 'Owl', ar: 'بومة' }, { en: 'Old', ar: 'قديم' },
                    { en: 'Open', ar: 'يفتح / مفتوح' }, { en: 'One', ar: 'واحد' }, { en: 'Oak', ar: 'بلوط' },
                    { en: 'Oath', ar: 'قسم' }, { en: 'Obey', ar: 'يطيع' }, { en: 'Object', ar: 'غرض / يعترض' },
                    { en: 'Odd', ar: 'غريب / فردي' }, { en: 'Off', ar: 'خارج / إيقاف' }, { en: 'Offer', ar: 'يعرض / عرض' },
                    { en: 'Often', ar: 'غالباً' }, { en: 'Oil', ar: 'زيت' }, { en: 'Okay', ar: 'حسناً' },
                    { en: 'Olden', ar: 'قديم' }, { en: 'Olive', ar: 'زيتون' }, { en: 'On', ar: 'على' },
                    { en: 'Once', ar: 'مرة واحدة' }, { en: 'Only', ar: 'فقط' }, { en: 'Onto', ar: 'إلى' },
                    { en: 'Opal', ar: 'أوبال' }, { en: 'Opt', ar: 'يختار' }, { en: 'Oral', ar: 'شفوي' },
                    { en: 'Order', ar: 'ترتيب / يطلب' }
                ],
                'P': [
                    { en: 'Pen', ar: 'قلم' }, { en: 'Pig', ar: 'خنزير' }, { en: 'Pink', ar: 'وردي' },
                    { en: 'Play', ar: 'يلعب' }, { en: 'People', ar: 'ناس' }, { en: 'Pack', ar: 'حزمة / يحزم' },
                    { en: 'Page', ar: 'صفحة' }, { en: 'Paid', ar: 'دفع (ماضي)' }, { en: 'Pain', ar: 'ألم' },
                    { en: 'Paint', ar: 'يرسم / دهان' }, { en: 'Pair', ar: 'زوج' }, { en: 'Pale', ar: 'شاحب' },
                    { en: 'Palm', ar: 'كف / نخيل' }, { en: 'Pan', ar: 'مقلاة' }, { en: 'Pane', ar: 'لوح زجاج' },
                    { en: 'Pant', ar: 'يلهث' }, { en: 'Papa', ar: 'بابا' }, { en: 'Para', ar: 'جزء' },
                    { en: 'Park', ar: 'حديقة / يركن' }, { en: 'Part', ar: 'جزء' }, { en: 'Pass', ar: 'يمر / يجتاز' },
                    { en: 'Past', ar: 'ماضي' }, { en: 'Path', ar: 'مسار' }, { en: 'Pause', ar: 'وقفة / يتوقف' },
                    { en: 'Paw', ar: 'مخلب' }
                ],
                'Q': [
                    { en: 'Queen', ar: 'ملكة' }, { en: 'Quick', ar: 'سريع' }, { en: 'Quiet', ar: 'هادئ' },
                    { en: 'Quiz', ar: 'اختبار قصير' }, { en: 'Quote', ar: 'يقتبس / اقتباس' }, { en: 'Quack', ar: 'صوت البطة' },
                    { en: 'Quail', ar: 'سمان' }, { en: 'Quake', ar: 'يهتز / زلزال' }, { en: 'Qualm', ar: 'شك / قلق' },
                    { en: 'Quant', ar: 'كمية' }, { en: 'Quash', ar: 'يبطل' }, { en: 'Quay', ar: 'رصيف ميناء' },
                    { en: 'Queer', ar: 'غريب' }, { en: 'Quell', ar: 'يخمد' }, { en: 'Quest', ar: 'بحث' },
                    { en: 'Queue', ar: 'طابور' }, { en: 'Quill', ar: 'ريشة كتابة' }, { en: 'Quilt', ar: 'لحاف' },
                    { en: 'Quint', ar: 'خماسي' }, { en: 'Quit', ar: 'يترك / يتوقف' }, { en: 'Quite', ar: 'تماماً' },
                    { en: 'Quiver', ar: 'يرتجف / جعبة سهام' }, { en: 'Quoin', ar: 'حجر الزاوية' }
                ],
                'R': [
                    { en: 'Rabbit', ar: 'أرنب' }, { en: 'Red', ar: 'أحمر' }, { en: 'Run', ar: 'يجري' },
                    { en: 'Read', ar: 'يقرأ' }, { en: 'Right', ar: 'صحيح / يمين' }, { en: 'Race', ar: 'سباق / يتسابق' },
                    { en: 'Rack', ar: 'رف' }, { en: 'Rage', ar: 'غضب' }, { en: 'Raid', ar: 'غارة' },
                    { en: 'Rail', ar: 'سكة حديد' }, { en: 'Rain', ar: 'مطر' }, { en: 'Raise', ar: 'يرفع' },
                    { en: 'Rake', ar: 'يجمع' }, { en: 'Ram', ar: 'كبش / يدفع بقوة' }, { en: 'Random', ar: 'عشوائي' },
                    { en: 'Range', ar: 'مدى / يتراوح' }, { en: 'Rank', ar: 'رتبة' }, { en: 'Rapid', ar: 'سريع' },
                    { en: 'Rare', ar: 'نادر' }, { en: 'Rat', ar: 'فأر' }, { en: 'Rate', ar: 'سعر / معدل' },
                    { en: 'Rave', ar: 'يهذو' }, { en: 'Raw', ar: 'خام' }, { en: 'Ray', ar: 'شعاع' },
                    { en: 'Reach', ar: 'يصل' }
                ],
                'S': [
                    { en: 'Sun', ar: 'شمس' }, { en: 'Star', ar: 'نجمة' }, { en: 'Sit', ar: 'يجلس' },
                    { en: 'Small', ar: 'صغير' }, { en: 'Sleep', ar: 'ينام' }, { en: 'Sad', ar: 'حزين' },
                    { en: 'Safe', ar: 'آمن / خزنة' }, { en: 'Said', ar: 'قال (ماضي)' }, { en: 'Sail', ar: 'يبحر / شراع' },
                    { en: 'Saint', ar: 'قديس' }, { en: 'Sale', ar: 'بيع' }, { en: 'Salt', ar: 'ملح' },
                    { en: 'Same', ar: 'نفس الـ' }, { en: 'Sand', ar: 'رمل' }, { en: 'Save', ar: 'ينقذ / يوفر' },
                    { en: 'Saw', ar: 'رأى (ماضي) / منشار' }, { en: 'Say', ar: 'يقول' }, { en: 'Scan', ar: 'يمسح' },
                    { en: 'Scar', ar: 'ندبة' }, { en: 'Scare', ar: 'يخيف' }, { en: 'Scarf', ar: 'وشاح' },
                    { en: 'Scene', ar: 'مشهد' }, { en: 'Scent', ar: 'رائحة' }, { en: 'School', ar: 'مدرسة' }
                ],
                'T': [
                    { en: 'Tree', ar: 'شجرة' }, { en: 'Table', ar: 'طاولة' }, { en: 'Talk', ar: 'يتحدث' },
                    { en: 'Time', ar: 'وقت' }, { en: 'Take', ar: 'يأخذ' }, { en: 'Tail', ar: 'ذيل' },
                    { en: 'Tale', ar: 'حكاية' }, { en: 'Tall', ar: 'طويل' }, { en: 'Tame', ar: 'يروض / أليف' },
                    { en: 'Tank', ar: 'خزان / دبابة' }, { en: 'Tap', ar: 'حنفية / ينقر' }, { en: 'Tape', ar: 'شريط / يسجل' },
                    { en: 'Tar', ar: 'قطران' }, { en: 'Target', ar: 'هدف' }, { en: 'Task', ar: 'مهمة' },
                    { en: 'Taste', ar: 'يتذوق / طعم' }, { en: 'Tax', ar: 'ضريبة' }, { en: 'Teach', ar: 'يعلم' },
                    { en: 'Team', ar: 'فريق' }, { en: 'Tear', ar: 'يمزق / دمعة' }, { en: 'Tech', ar: 'تكنولوجيا' },
                    { en: 'Teen', ar: 'مراهق' }, { en: 'Tell', ar: 'يخبر' }
                ],
                'U': [
                    { en: 'Umbrella', ar: 'مظلة' }, { en: 'Up', ar: 'فوق' }, { en: 'Under', ar: 'تحت' },
                    { en: 'Use', ar: 'يستخدم' }, { en: 'Ugly', ar: 'قبيح' }, { en: 'Uncle', ar: 'عم / خال' },
                    { en: 'Uncut', ar: 'غير مقطوع' }, { en: 'Undue', ar: 'غير مبرر' }, { en: 'Undo', ar: 'يتراجع' },
                    { en: 'Unfit', ar: 'غير لائق' }, { en: 'Unfold', ar: 'يكشف' }, { en: 'Unison', ar: 'انسجام' },
                    { en: 'Unit', ar: 'وحدة' }, { en: 'Unite', ar: 'يتحد' }, { en: 'Untie', ar: 'يفك' },
                    { en: 'Until', ar: 'حتى' }, { en: 'Unused', ar: 'غير مستخدم' }, { en: 'Unwise', ar: 'غير حكيم' },
                    { en: 'Upset', ar: 'منزعج / يقلب' }, { en: 'Urban', ar: 'حضري' }, { en: 'Urge', ar: 'يحث / إلحاح' },
                    { en: 'Urgent', ar: 'عاجل' }, { en: 'Urn', ar: 'جرة / رماد' }, { en: 'Us', ar: 'نحن (مفعول به)' },
                    { en: 'Usual', ar: 'معتاد' }
                ],
                'V': [
                    { en: 'Van', ar: 'شاحنة صغيرة' }, { en: 'Vase', ar: 'مزهرية' }, { en: 'Voice', ar: 'صوت' },
                    { en: 'Very', ar: 'جداً' }, { en: 'Visit', ar: 'يزور / زيارة' }, { en: 'Vain', ar: 'عبثي / مغرور' },
                    { en: 'Vale', ar: 'وادي' }, { en: 'Valet', ar: 'خادم' }, { en: 'Valid', ar: 'صالح' },
                    { en: 'Valley', ar: 'وادي' }, { en: 'Value', ar: 'قيمة' }, { en: 'Vane', ar: 'ريشة دوارة' },
                    { en: 'Vary', ar: 'يختلف' }, { en: 'Vast', ar: 'واسع' }, { en: 'Vault', ar: 'قبو' },
                    { en: 'Veal', ar: 'لحم عجل' }, { en: 'Veer', ar: 'ينحرف' }, { en: 'Veil', ar: 'حجاب' },
                    { en: 'Vein', ar: 'وريد' }, { en: 'Veld', ar: 'سهول' }, { en: 'Venom', ar: 'سم' },
                    { en: 'Vent', ar: 'فتحة تهوية' }, { en: 'Verb', ar: 'فعل' }, { en: 'Verse', ar: 'آية / بيت شعر' },
                    { en: 'Vest', ar: 'سترة' }
                ],
                'W': [
                    { en: 'Water', ar: 'ماء' }, { en: 'Write', ar: 'يكتب' }, { en: 'Walk', ar: 'يمشي' },
                    { en: 'Warm', ar: 'دافئ' }, { en: 'Work', ar: 'يعمل / عمل' }, { en: 'Wage', ar: 'أجر' },
                    { en: 'Wait', ar: 'ينتظر' }, { en: 'Wake', ar: 'يستيقظ' }, { en: 'Wall', ar: 'جدار' },
                    { en: 'Want', ar: 'يريد' }, { en: 'War', ar: 'حرب' }, { en: 'Ward', ar: 'جناح' },
                    { en: 'Ware', ar: 'بضاعة' }, { en: 'Warn', ar: 'يحذر' }, { en: 'Wash', ar: 'يغسل' },
                    { en: 'Waste', ar: 'يهدر / نفايات' }, { en: 'Watch', ar: 'يشاهد / ساعة' }, { en: 'Wave', ar: 'موجة / يلوح' },
                    { en: 'Wax', ar: 'شمع' }, { en: 'Way', ar: 'طريق' }, { en: 'We', ar: 'نحن' },
                    { en: 'Weak', ar: 'ضعيف' }
                ],
                'X': [
                    { en: 'X-ray', ar: 'أشعة سينية' }, { en: 'Xylophone', ar: 'إكسيليفون' }, { en: 'Xenon', ar: 'زينون' },
                    { en: 'Xeric', ar: 'جاف' }, { en: 'Xylograph', ar: 'نقش خشبي' }, { en: 'Xylitol', ar: 'إكسيليتول' },
                    { en: 'Xylan', ar: 'زيلان' }, { en: 'Xylene', ar: 'زيلين' }, { en: 'Xanthic', ar: 'أصفر' },
                    { en: 'Xanthin', ar: 'زانثين' }, { en: 'Xanthoma', ar: 'ورم أصفر' }, { en: 'Xebec', ar: 'سفينة شراعية' },
                    { en: 'Xenia', ar: 'ضيافة' }, { en: 'Xenical', ar: 'زينيكال' }, { en: 'Xenograft', ar: 'طعم أجنبي' },
                    { en: 'Xeriscape', ar: 'تنسيق طبيعي جاف' }, { en: 'Xeroderma', ar: 'جفاف الجلد' }, { en: 'Xerox', ar: 'ينسخ / آلة تصوير' },
                    { en: 'Xerophyte', ar: 'نبات جفافي' }, { en: 'Xiphoid', ar: 'خنجري الشكل' }, { en: 'Xylose', ar: 'سكر الخشب' },
                    { en: 'Xyst', ar: 'رواق' }, { en: 'Xystus', ar: 'ممر مغطى' }
                ],
                'Y': [
                    { en: 'Yellow', ar: 'أصفر' }, { en: 'Yes', ar: 'نعم' }, { en: 'You', ar: 'أنت / أنتم' },
                    { en: 'Year', ar: 'سنة' }, { en: 'Young', ar: 'شاب' }, { en: 'Yacht', ar: 'يخت' },
                    { en: 'Yak', ar: 'حيوان الياك' }, { en: 'Yam', ar: 'بطاطا' }, { en: 'Yank', ar: 'يسحب بقوة' },
                    { en: 'Yap', ar: 'ينبح' }, { en: 'Yard', ar: 'ساحة / ياردة' }, { en: 'Yarn', ar: 'خيط / قصة' },
                    { en: 'Yelp', ar: 'يصرخ' }, { en: 'Yet', ar: 'بعد / حتى الآن' }, { en: 'Yield', ar: 'ينتج / يستسلم' },
                    { en: 'Yoga', ar: 'يوغا' }, { en: 'Yogurt', ar: 'زبادي' }, { en: 'Yoke', ar: 'نير' },
                    { en: 'Your', ar: 'لك / لكم' }, { en: 'Yours', ar: 'ملكك / ملككم' }, { en: 'Youth', ar: 'شباب' },
                    { en: 'Yawn', ar: 'يتثاءب' }, { en: 'Zeal', ar: 'حماس' }
                ],
                'Z': [
                    { en: 'Zebra', ar: 'حمار وحشي' }, { en: 'Zoo', ar: 'حديقة حيوان' }, { en: 'Zip', ar: 'سحاب / يغلق بسحاب' },
                    { en: 'Zone', ar: 'منطقة' }, { en: 'Zero', ar: 'صفر' }, { en: 'Zany', ar: 'غريب الأطوار' },
                    { en: 'Zap', ar: 'يقضي على' }, { en: 'Zenith', ar: 'ذروة' }, { en: 'Zephyr', ar: 'نسيم عليل' },
                    { en: 'Zepto', ar: 'زبتو (بادئة)' }, { en: 'Zest', ar: 'حماس / قشرة الحمضيات' }, { en: 'Zigzag', ar: 'متعرج' },
                    { en: 'Zinc', ar: 'زنك' }, { en: 'Zing', ar: 'حيوية' }, { en: 'Zinnia', ar: 'زينية (زهرة)' },
                    { en: 'Zion', ar: 'صهيون' }, { en: 'Zipper', ar: 'سحاب' }, { en: 'Zircon', ar: 'زركون' },
                    { en: 'Zodiac', ar: 'برج فلكي' }, { en: 'Zombie', ar: 'زومبي' }, { en: 'Zoom', ar: 'يكبر / يسرع' }
                ]
            };

            const commonWordsData = [
                { en: 'the', ar: 'الـ' }, { en: 'be', ar: 'يكون' }, { en: 'to', ar: 'إلى' }, { en: 'of', ar: 'من' }, { en: 'and', ar: 'و' },
                { en: 'a', ar: 'أ' }, { en: 'in', ar: 'في' }, { en: 'that', ar: 'ذلك' }, { en: 'have', ar: 'يملك' }, { en: 'I', ar: 'أنا' },
                { en: 'it', ar: 'هو/هي (لغير العاقل)' }, { en: 'for', ar: 'لأجل' }, { en: 'not', ar: 'لا' }, { en: 'on', ar: 'على' }, { en: 'with', ar: 'مع' },
                { en: 'he', ar: 'هو' }, { en: 'as', ar: 'كـ' }, { en: 'you', ar: 'أنت/أنتم' }, { en: 'do', ar: 'يفعل' }, { en: 'at', ar: 'في' },
                { en: 'this', ar: 'هذا' }, { en: 'but', ar: 'لكن' }, { en: 'his', ar: 'ملكه' }, { en: 'by', ar: 'بواسطة' }, { en: 'from', ar: 'من' },
                { en: 'they', ar: 'هم/هن' }, { en: 'we', ar: 'نحن' }, { en: 'say', ar: 'يقول' }, { en: 'her', ar: 'لها' }, { en: 'she', ar: 'هي' },
                { en: 'or', ar: 'أو' }, { en: 'an', ar: 'أ (للمفرد)' }, { en: 'will', ar: 'سوف' }, { en: 'my', ar: 'ملكي' }, { en: 'one', ar: 'واحد' },
                { en: 'all', ar: 'كل' }, { en: 'would', ar: 'كان سـ' }, { en: 'there', ar: 'هناك' }, { en: 'their', ar: 'ملكهم/ملكهن' }, { en: 'what', ar: 'ماذا' },
                { en: 'so', ar: 'لذا' }, { en: 'up', ar: 'فوق' }, { en: 'out', ar: 'خارج' }, { en: 'if', ar: 'إذا' }, { en: 'get', ar: 'يحصل على' },
                { en: 'which', ar: 'أي' }, { en: 'go', ar: 'يذهب' }, { en: 'me', ar: 'لي/إياي' }, { en: 'when', ar: 'متى' }, { en: 'make', ar: 'يصنع' },
                { en: 'can', ar: 'يستطيع' }, { en: 'like', ar: 'يحب/مثل' }, { en: 'time', ar: 'وقت' }, { en: 'no', ar: 'لا' }, { en: 'just', ar: 'فقط' },
                { en: 'him', ar: 'له/إياه' }, { en: 'know', ar: 'يعرف' }, { en: 'take', ar: 'يأخذ' }, { en: 'person', ar: 'شخص' }, { en: 'into', ar: 'إلى' },
                { en: 'year', ar: 'سنة' }, { en: 'your', ar: 'لك/لكم' }, { en: 'good', ar: 'جيد' }, { en: 'some', ar: 'بعض' }, { en: 'could', ar: 'كان يستطيع' },
                { en: 'them', ar: 'لهم/إياهم' }, { en: 'see', ar: 'يرى' }, { en: 'other', ar: 'آخر' }, { en: 'than', ar: 'من' }, { en: 'then', ar: 'ثم' },
                { en: 'now', ar: 'الآن' }, { en: 'look', ar: 'ينظر' }, { en: 'only', ar: 'فقط' }, { en: 'come', ar: 'يأتي' }, { en: 'its', ar: 'ملكها/ملكه (لغير العاقل)' },
                { en: 'over', ar: 'فوق/انتهى' }, { en: 'think', ar: 'يعتقد' }, { en: 'also', ar: 'أيضاً' }, { en: 'back', ar: 'خلف' }, { en: 'after', ar: 'بعد' },
                { en: 'use', ar: 'يستخدم' }, { en: 'two', ar: 'اثنين' }, { en: 'how', ar: 'كيف' }, { en: 'our', ar: 'ملكنا' }, { en: 'work', ar: 'يعمل/عمل' },
                { en: 'first', ar: 'أول' }, { en: 'well', ar: 'جيداً' }, { en: 'way', ar: 'طريق' }, { en: 'even', ar: 'حتى' }, { en: 'new', ar: 'جديد' },
                { en: 'want', ar: 'يريد' }, { en: 'because', ar: 'لأن' }, { en: 'any', ar: 'أي' }, { en: 'these', ar: 'هؤلاء' }, { en: 'give', ar: 'يعطي' },
                { en: 'day', ar: 'يوم' }, { en: 'most', ar: 'معظم' }, { en: 'us', ar: 'نحن (مفعول به)' }, { en: 'man', ar: 'رجل' }, { en: 'find', ar: 'يجد' }
            ];

            const colorsData = [
                { en: 'Red', ar: 'أحمر', hex: '#FF0000' },
                { en: 'Blue', ar: 'أزرق', hex: '#0000FF' },
                { en: 'Green', ar: 'أخضر', hex: '#008000' },
                { en: 'Yellow', ar: 'أصفر', hex: '#FFFF00' },
                { en: 'Orange', ar: 'برتقالي', hex: '#FFA500' },
                { en: 'Purple', ar: 'أرجواني', hex: '#800080' },
                { en: 'Pink', ar: 'وردي', hex: '#FFC0CB' },
                { en: 'Black', ar: 'أسود', hex: '#000000' },
                { en: 'White', ar: 'أبيض', hex: '#FFFFFF' },
                { en: 'Brown', ar: 'بني', hex: '#A52A2A' },
                { en: 'Gray', ar: 'رمادي', hex: '#808080' },
                { en: 'Silver', ar: 'فضي', hex: '#C0C0C0' },
                { en: 'Gold', ar: 'ذهبي', hex: '#FFD700' },
                { en: 'Cyan', ar: 'سماوي', hex: '#00FFFF' },
                { en: 'Magenta', ar: 'أرجواني فاتح', hex: '#FF00FF' },
                { en: 'Teal', ar: 'أزرق مخضر', hex: '#008080' },
                { en: 'Olive', ar: 'زيتوني', hex: '#808000' },
                { en: 'Maroon', ar: 'كستنائي', hex: '#800000' },
                { en: 'Navy', ar: 'كحلي', hex: '#000080' },
                { en: 'Lime', ar: 'ليموني', hex: '#00FF00' }
            ];

            const cardinalNumbersData = [
                { num: 1, en: 'One', ar: 'واحد' },
                { num: 2, en: 'Two', ar: 'اثنان' },
                { num: 3, en: 'Three', ar: 'ثلاثة' },
                { num: 4, en: 'Four', ar: 'أربعة' },
                { num: 5, en: 'Five', ar: 'خمسة' },
                { num: 6, en: 'Six', ar: 'ستة' },
                { num: 7, en: 'Seven', ar: 'سبعة' },
                { num: 8, en: 'Eight', ar: 'ثمانية' },
                { num: 9, en: 'Nine', ar: 'تسعة' },
                { num: 10, en: 'Ten', ar: 'عشرة' },
                { num: 11, en: 'Eleven', ar: 'أحد عشر' },
                { num: 12, en: 'Twelve', ar: 'اثنا عشر' },
                { num: 13, en: 'Thirteen', ar: 'ثلاثة عشر' },
                { num: 14, en: 'Fourteen', ar: 'أربعة عشر' },
                { num: 15, en: 'Fifteen', ar: 'خمسة عشر' },
                { num: 16, en: 'Sixteen', ar: 'ستة عشر' },
                { num: 17, en: 'Seventeen', ar: 'سبعة عشر' },
                { num: 18, en: 'Eighteen', ar: 'ثمانية عشر' },
                { num: 19, en: 'Nineteen', ar: 'تسعة عشر' },
                { num: 20, en: 'Twenty', ar: 'عشرون' },
                { num: 21, en: 'Twenty-one', ar: 'واحد وعشرون' },
                { num: 30, en: 'Thirty', ar: 'ثلاثون' },
                { num: 40, en: 'Forty', ar: 'أربعون' },
                { num: 50, en: 'Fifty', ar: 'خمسون' },
                { num: 60, en: 'Sixty', ar: 'ستون' },
                { num: 70, en: 'Seventy', ar: 'سبعون' },
                { num: 80, en: 'Eighty', ar: 'ثمانون' },
                { num: 90, en: 'Ninety', ar: 'تسعون' },
                { num: 100, en: 'One hundred', ar: 'مائة' },
                { num: 1000, en: 'One thousand', ar: 'ألف' },
                { num: 1000000, en: 'One million', ar: 'مليون' }
            ];

            const ordinalNumbersData = [
                { num: 1, en: 'First', ar: 'الأول' },
                { num: 2, en: 'Second', ar: 'الثاني' },
                { num: 3, en: 'Third', ar: 'الثالث' },
                { num: 4, en: 'Fourth', ar: 'الرابع' },
                { num: 5, en: 'Fifth', ar: 'الخامس' },
                { num: 6, en: 'Sixth', ar: 'السادس' },
                { num: 7, en: 'Seventh', ar: 'السابع' },
                { num: 8, en: 'Eighth', ar: 'الثامن' },
                { num: 9, en: 'Ninth', ar: 'التاسع' },
                { num: 10, en: 'Tenth', ar: 'العاشر' },
                { num: 11, en: 'Eleventh', ar: 'الحادي عشر' },
                { num: 12, en: 'Twelfth', ar: 'الثاني عشر' },
                { num: 13, en: 'Thirteenth', ar: 'الثالث عشر' },
                { num: 14, en: 'Fourteenth', ar: 'الرابع عشر' },
                { num: 15, en: 'Fifteenth', ar: 'الخامس عشر' },
                { num: 16, en: 'Sixteenth', ar: 'السادس عشر' },
                { num: 17, en: 'Seventeenth', ar: 'السابع عشر' },
                { num: 18, en: 'Eighteenth', ar: 'الثامن عشر' },
                { num: 19, en: 'Nineteenth', ar: 'التاسع عشر' },
                { num: 20, en: 'Twentieth', ar: 'العشرون' },
                { num: 21, en: 'Twenty-first', ar: 'الحادي والعشرون' },
                { num: 22, en: 'Twenty-second', ar: 'الثاني والعشرون' },
                { num: 30, en: 'Thirtieth', ar: 'الثلاثون' },
                { num: 40, en: 'Fortieth', ar: 'الأربعون' },
                { num: 50, en: 'Fiftieth', ar: 'الخمسون' },
                { num: 100, en: 'Hundredth', ar: 'المائة' },
                { num: 1000, en: 'Thousandth', ar: 'الألف' }
            ];


            const alphabetContainer = document.getElementById('alphabet-container');
            const commonWordsTbody = document.getElementById('common-words-tbody');
            const colorsTbody = document.getElementById('colors-tbody');
            const cardinalNumbersTbody = document.getElementById('cardinal-numbers-tbody');
            const ordinalNumbersTbody = document.getElementById('ordinal-numbers-tbody');


            // Function to speak text
            function speakText(text, lang = 'en-US') {
                const synth = window.speechSynthesis;
                if (synth.speaking) {
                    synth.cancel(); // Stop current speech if any
                }
                const utterance = new SpeechSynthesisUtterance(text);
                utterance.lang = lang; // Set language for pronunciation
                synth.speak(utterance);
            }

            // Generic function to populate tables
            function populateTable(tbodyElement, data, colsPerRow, type = 'word') {
                tbodyElement.innerHTML = ''; // Clear existing content
                
                // For the 'color' type, we actually have 3 columns per data item (en, ar, hex)
                // So, if colsPerRow is 4, total table columns will be 4 * 3 = 12
                const actualColsPerDataItem = (type === 'color') ? 3 : 2; 
                const totalTableColumns = colsPerRow * actualColsPerDataItem;

                // Calculate the number of rows needed
                const rowsNeeded = Math.ceil(data.length / colsPerRow);

                for (let i = 0; i < rowsNeeded; i++) {
                    const row = document.createElement('tr');
                    for (let j = 0; j < colsPerRow; j++) {
                        const dataIndex = i + (j * rowsNeeded); // Populate column by column

                        if (dataIndex < data.length) {
                            const item = data[dataIndex];
                            if (type === 'color') {
                                const cell1 = document.createElement('td'); // English word
                                const cell2 = document.createElement('td'); // Arabic translation
                                const cell3 = document.createElement('td'); // Color box

                                const enSpan = document.createElement('span');
                                enSpan.classList.add('english-word');
                                enSpan.textContent = item.en;
                                enSpan.addEventListener('click', () => speakText(item.en, 'en-US'));
                                cell1.appendChild(enSpan);
                                cell2.textContent = item.ar;

                                const colorBox = document.createElement('span');
                                colorBox.classList.add('color-box');
                                colorBox.style.backgroundColor = item.hex;
                                cell3.appendChild(colorBox);

                                row.appendChild(cell1);
                                row.appendChild(cell2);
                                row.appendChild(cell3);
                            } else { // type === 'word' or 'number'
                                const cell1 = document.createElement('td');
                                const cell2 = document.createElement('td');

                                if (type === 'number') {
                                    cell1.textContent = item.num; // Display number
                                    const enSpan = document.createElement('span');
                                    enSpan.classList.add('english-word');
                                    enSpan.textContent = item.en;
                                    enSpan.addEventListener('click', () => speakText(item.en, 'en-US'));
                                    cell2.appendChild(enSpan);
                                } else { // type === 'word'
                                    const enSpan = document.createElement('span');
                                    enSpan.classList.add('english-word');
                                    enSpan.textContent = item.en;
                                    enSpan.addEventListener('click', () => speakText(item.en, 'en-US'));
                                    cell1.appendChild(enSpan);
                                    cell2.textContent = item.ar;
                                }
                                row.appendChild(cell1);
                                row.appendChild(cell2);
                            }
                        } else {
                            // Fill empty cells if data doesn't perfectly fit
                            if (type === 'color') {
                                row.appendChild(document.createElement('td'));
                                row.appendChild(document.createElement('td'));
                                row.appendChild(document.createElement('td'));
                            } else {
                                row.appendChild(document.createElement('td'));
                                row.appendChild(document.createElement('td'));
                            }
                        }
                    }
                    tbodyElement.appendChild(row);
                }
            }


            // Generate alphabet cards dynamically
            for (const letter in alphabetData) {
                const words = alphabetData[letter];

                const cardDiv = document.createElement('div');
                cardDiv.classList.add('alphabet-card');

                const cardHeader = document.createElement('h3');
                cardHeader.textContent = letter;
                cardDiv.appendChild(cardHeader);

                const table = document.createElement('table');
                table.classList.add('alphabet-table');
                table.innerHTML = `
                    <thead>
                        <tr>
                            <th>الإنجليزية</th>
                            <th>العربية</th>
                        </tr>
                    </thead>
                    <tbody>
                    </tbody>
                `;
                const tbody = table.querySelector('tbody');

                words.forEach(word => {
                    const row = document.createElement('tr');
                    const enCell = document.createElement('td');
                    const arCell = document.createElement('td');

                    const enSpan = document.createElement('span');
                    enSpan.classList.add('english-word');
                    enSpan.textContent = word.en;
                    enSpan.addEventListener('click', () => speakText(word.en, 'en-US')); // Speak English word

                    enCell.appendChild(enSpan);
                    arCell.textContent = word.ar;

                    row.appendChild(enCell);
                    row.appendChild(arCell);
                    tbody.appendChild(row);
                });

                cardDiv.appendChild(table);
                alphabetContainer.appendChild(cardDiv);
            }

            // Populate common words table (5 columns)
            populateTable(commonWordsTbody, commonWordsData, 5, 'word');

            // Populate colors table in 4 columns
            populateTable(colorsTbody, colorsData, 4, 'color');


            // Populate cardinal numbers table (5 columns)
            populateTable(cardinalNumbersTbody, cardinalNumbersData, 5, 'number');

            // Populate ordinal numbers table (5 columns)
            populateTable(ordinalNumbersTbody, ordinalNumbersData, 5, 'number');


            // Add click event listeners for grammar headings and speakable words
            document.querySelectorAll('.speakable-heading, .speakable-word').forEach(element => {
                element.addEventListener('click', function() {
                    const textToSpeak = this.textContent;
                    if (this.classList.contains('speakable-heading')) {
                        const match = textToSpeak.match(/\((.*?)\)/);
                        if (match && match[1]) {
                            speakText(match[1], 'en-US'); // Speak English part of heading
                        } else {
                            speakText(textToSpeak, 'ar-SA'); // Default to Arabic if English part not found
                        }
                    } else if (this.classList.contains('speakable-word')) {
                        speakText(textToSpeak, 'en-US'); // Always speak .speakable-word in English
                    }
                });
            });

            // Speak entire grammar topic content when clicking on a grammar-topic div (excluding nested speakable elements)
            document.querySelectorAll('.grammar-topic').forEach(topicDiv => {
                topicDiv.addEventListener('click', function(event) {
                    // Prevent speaking the whole topic if a specific speakable element inside was clicked
                    if (event.target.classList.contains('speakable-heading') || event.target.classList.contains('speakable-word')) {
                        return;
                    }

                    const paragraphs = this.querySelectorAll('p:not(.grammar-topic p .english-word), li:not(.grammar-topic li .english-word)');
                    let fullText = '';
                    paragraphs.forEach(p => {
                        // Extract only Arabic text for speaking the full section, by removing English words in spans
                        let text = p.textContent;
                        // Regex to remove content within span.speakable-word tags
                        text = text.replace(/<span class="speakable-word"[^>]*>.*?<\/span>/g, '');
                        // Remove English words in parentheses that are not wrapped in speakable-word spans (for headings logic)
                        text = text.replace(/\((.*?)\)/g, '').trim();

                        if (text) {
                            fullText += text + ' ';
                        }
                    });
                    if (fullText.trim()) {
                        speakText(fullText.trim(), 'ar-SA'); // Speak the whole Arabic text
                    }
                });
            });
        });
    </script>
   
   <html lang="ar" dir="rtl">
   <head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>الأزمنة في اللغة الإنجليزية والأسئلة التدريبية</title>
   <style>
   :root {
   --primary-color: #6a0572;
   --secondary-color: #ff6f61;
   --text-color: #333;
   --bg-color: #fce4ec;
   --card-bg: #ffffff;
   --border-color: #e0e0e0;
   --shadow-color: rgba(0, 0, 0, 0.15);
   --accent-color-1: #4CAF50;
   --accent-color-2: #2196F3;
   --accent-color-3: #FFC107;
   --accent-color-4: #9C27B0;
   }
   
   body {
   font-family: 'Cairo', sans-serif;
   margin: 0;
   padding: 0;
   background-color: var(--bg-color);
   color: var(--text-color);
   line-height: 1.8;
   direction: rtl;
   text-align: right;
   scroll-behavior: smooth;
   }
   
   header {
   background-image: linear-gradient(to right, var(--primary-color), var(--secondary-color));
   color: white;
   padding: 2em 0;
   text-align: center;
   box-shadow: 0 4px 10px var(--shadow-color);
   }
   
   main {
   padding: 30px 20px;
   max-width: 1300px;
   margin: 30px auto;
   background-color: var(--card-bg);
   border-radius: 12px;
   box-shadow: 0 0 20px var(--shadow-color);
   }
   
   section {
   margin-bottom: 50px;
   padding-bottom: 30px;
   border-bottom: 1px solid var(--border-color);
   }
   
   h2 {
   color: var(--primary-color);
   text-align: center;
   margin-bottom: 40px;
   font-size: 2.5em;
   border-bottom: 3px solid var(--secondary-color);
   display: inline-block;
   padding-bottom: 10px;
   position: relative;
   left: 50%;
   transform: translateX(-50%);
   }
   
   h3 {
   color: var(--text-color);
   font-size: 1.8em;
   margin-top: 30px;
   margin-bottom: 20px;
   padding-bottom: 5px;
   border-bottom: 1px dashed var(--border-color);
   }
   
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
   
   .grammar-topic h3.speakable-heading {
   cursor: pointer;
   color: var(--primary-color);
   font-size: 2em;
   margin-top: 0;
   border-bottom: 2px dashed var(--secondary-color);
   padding-bottom: 12px;
   transition: color 0.2s ease-in-out;
   }
   
   .grammar-topic h3.speakable-heading:hover {
   color: var(--secondary-color);
   }
   
   .grammar-text {
   margin-bottom: 20px;
   font-size: 1.1em;
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
   font-size: 1.05em;
   }
   
   .grammar-topic ul li::before {
   content: '🌟';
   color: var(--secondary-color);
   font-weight: bold;
   position: absolute;
   right: 0;
   font-size: 1.2em;
   }
   
   .speakable-word {
   cursor: pointer;
   color: var(--primary-color);
   font-weight: bold;
   transition: color 0.2s ease-in-out;
   }
   
   .speakable-word:hover {
   color: var(--secondary-color);
   text-decoration: underline;
   }
   
   .exercises-section {
   margin-top: 40px;
   padding-top: 20px;
   border-top: 2px dashed #ccc;
   }
   
   .question-group {
   background-color: #f9f9f9;
   padding: 20px;
   border-radius: 8px;
   margin-bottom: 30px;
   border: 1px solid #ddd;
   }
   
   .question-group ol {
   list-style-type: decimal;
   padding-right: 20px;
   }
   
   .question-group li {
   margin-bottom: 15px;
   padding: 5px 0;
   }
   
   .question-group label {
   display: block;
   margin-bottom: 5px;
   font-weight: bold;
   }
   
   .question-group .options span {
   margin-left: 15px;
   display: inline-block;
   }
   
   .correct-answer {
   color: #4CAF50;
   font-weight: bold;
   margin-top: 5px;
   display: block;
   }
   
   footer {
   text-align: center;
   padding: 25px;
   background-image: linear-gradient(to left, var(--primary-color), var(--secondary-color));
   color: white;
   margin-top: 50px;
   border-radius: 0 0 12px 12px;
   box-shadow: 0 -4px 10px var(--shadow-color);
   font-size: 1.1em;
   }
   
   @media (max-width: 768px) {
   h2 {
   font-size: 2.2em;
   }
   h3 {
   font-size: 1.6em;
   }
   }
   </style>
   </head>
   <body>
   <header>
   <h1>الأزمنة في اللغة الإنجليزية والأسئلة التدريبية</h1>
   </header>
   
   <main>
   <section id="tenses-section">
   <h2>الأزمنة في اللغة الإنجليزية (Tenses) والكلمات الدالة عليها</h2>
   <p class="instruction">اضغط على أي عنوان زمن أو كلمة إنجليزية لسماع نطقها.</p>
   
   <!-- Present Simple -->
   <div class="grammar-topic">
   <h3 class="speakable-heading">1. زمن المضارع البسيط (Present Simple)</h3>
   <p class="grammar-text">يُستخدم للتعبير عن الحقائق العامة، العادات، والجداول الزمنية.</p>
   <ul>
   <li>**الاستخدامات:**
   <ul>
   <li>الحقائق العامة: The sun <span class="speakable-word">rises</span> in the east. (الشمس تشرق من الشرق.)</li>
   <li>العادات والروتين: I <span class="speakable-word">drink</span> coffee every morning. (أشرب القهوة كل صباح.)</li>
   </ul>
   </li>
   <li>**الكلمات الدالة:** <span class="speakable-word">always</span>, <span class="speakable-word">usually</span>, <span class="speakable-word">often</span>, <span class="speakable-word">sometimes</span>, <span class="speakable-word">rarely</span>, <span class="speakable-word">never</span>, <span class="speakable-word">every day</span>/<span class="speakable-word">week</span>/<span class="speakable-word">month</span>/<span class="speakable-word">year</span>, <span class="speakable-word">on Mondays</span>, <span class="speakable-word">at weekends</span>.</li>
   <li>**أمثلة وجمل (10 أمثلة):**
   <ul>
   <li>She <span class="speakable-word">works</span> in a hospital. (هي تعمل في مستشفى.)</li>
   <li>We <span class="speakable-word">don't eat</span> meat. (نحن لا نأكل اللحم.)</li>
   <li><span class="speakable-word">Does</span> he <span class="speakable-word">play</span> tennis? (هل يلعب التنس؟)</li>
   <li>They <span class="speakable-word">live</span> in New York. (هم يعيشون في نيويورك.)</li>
   <li>The train <span class="speakable-word">leaves</span> at 7 AM. (القطار يغادر في الساعة 7 صباحًا.)</li>
   </ul>
   </li>
   </ul>
   
   <div class="exercises-section">
   <h4>أسئلة تدريبية على المضارع البسيط (Present Simple)</h4>
   <p>اختر الإجابة الصحيحة:</p>
   <div class="question-group">
   <ol>
   <li>
   <label>He usually _____ (go) to work by bus.</label>
   <div class="options">
   <span><input type="radio" name="q1_ps" value="a"> a) go</span>
   <span><input type="radio" name="q1_ps" value="b"> b) goes</span>
   <span><input type="radio" name="q1_ps" value="c"> c) going</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) goes</span>
   </li>
   <li>
   <label>Do they _____ (live) in Cairo?</label>
   <div class="options">
   <span><input type="radio" name="q2_ps" value="a"> a) live</span>
   <span><input type="radio" name="q2_ps" value="b"> b) lives</span>
   <span><input type="radio" name="q2_ps" value="c"> c) living</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: a) live</span>
   </li>
   <li>
   <label>She _____ (not / like) coffee.</label>
   <div class="options">
   <span><input type="radio" name="q3_ps" value="a"> a) don't like</span>
   <span><input type="radio" name="q3_ps" value="b"> b) doesn't like</span>
   <span><input type="radio" name="q3_ps" value="c"> c) isn't liking</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) doesn't like</span>
   </li>
   <li>
   <label>The sun _____ (rise) in the east.</label>
   <div class="options">
   <span><input type="radio" name="q4_ps" value="a"> a) rise</span>
   <span><input type="radio" name="q4_ps" value="b"> b) rises</span>
   <span><input type="radio" name="q4_ps" value="c"> c) rising</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) rises</span>
   </li>
   <li>
   <label>What time _____ the train _____ (leave)?</label>
   <div class="options">
   <span><input type="radio" name="q5_ps" value="a"> a) do / leave</span>
   <span><input type="radio" name="q5_ps" value="b"> b) does / leave</span>
   <span><input type="radio" name="q5_ps" value="c"> c) is / leaving</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) does / leave</span>
   </li>
   </ol>
   </div>
   </div>
   </div>
   
   <!-- Present Continuous -->
   <div class="grammar-topic">
   <h3 class="speakable-heading">2. زمن المضارع المستمر (Present Continuous)</h3>
   <p class="grammar-text">يُستخدم للتعبير عن أفعال تحدث الآن أو في فترة زمنية مؤقتة حول الوقت الحاضر.</p>
   <ul>
   <li>**الاستخدامات:**
   <ul>
   <li>أفعال تحدث الآن: I <span class="speakable-word">am studying</span> English right now. (أنا أدرس الإنجليزية الآن.)</li>
   <li>أفعال مؤقتة: He <span class="speakable-word">is working</span> on a new project this month. (هو يعمل على مشروع جديد هذا الشهر.)</li>
   </ul>
   </li>
   <li>**الكلمات الدالة:** <span class="speakable-word">now</span>, <span class="speakable-word">right now</span>, <span class="speakable-word">at the moment</span>, <span class="speakable-word">currently</span>, <span class="speakable-word">today</span>, <span class="speakable-word">this week</span>/<span class="speakable-word">month</span>/<span class="speakable-word">year</span>, <span class="speakable-word">listen!</span>, <span class="speakable-word">look!</span></li>
   <li>**أمثلة وجمل (10 أمثلة):**
   <ul>
   <li>They <span class="speakable-word">are watching</span> TV. (هم يشاهدون التلفاز.)</li>
   <li>She <span class="speakable-word">isn't sleeping</span>. (هي لا تنام.)</li>
   <li><span class="speakable-word">Are</span> you <span class="speakable-word">listening</span> to me? (هل تستمع إلي؟)</li>
   <li>I <span class="speakable-word">am writing</span> an email. (أنا أكتب بريدًا إلكترونيًا.)</li>
   <li>The children <span class="speakable-word">are playing</span> outside. (الأطفال يلعبون في الخارج.)</li>
   </ul>
   </li>
   </ul>
   
   <div class="exercises-section">
   <h4>أسئلة تدريبية على المضارع المستمر (Present Continuous)</h4>
   <p>اختر الإجابة الصحيحة:</p>
   <div class="question-group">
   <ol>
   <li>
   <label>She _____ (study) English right now.</label>
   <div class="options">
   <span><input type="radio" name="q1_pc" value="a"> a) study</span>
   <span><input type="radio" name="q1_pc" value="b"> b) studies</span>
   <span><input type="radio" name="q1_pc" value="c"> c) is studying</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: c) is studying</span>
   </li>
   <li>
   <label>They _____ (not / watch) TV at the moment.</label>
   <div class="options">
   <span><input type="radio" name="q2_pc" value="a"> a) don't watch</span>
   <span><input type="radio" name="q2_pc" value="b"> b) aren't watching</span>
   <span><input type="radio" name="q2_pc" value="c"> c) isn't watching</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) aren't watching</span>
   </li>
   <li>
   <label>_____ you _____ (listen) to music?</label>
   <div class="options">
   <span><input type="radio" name="q3_pc" value="a"> a) Do / listen</span>
   <span><input type="radio" name="q3_pc" value="b"> b) Are / listening</span>
   <span><input type="radio" name="q3_pc" value="c"> c) Is / listening</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) Are / listening</span>
   </li>
   <li>
   <label>Look! The baby _____ (sleep).</label>
   <div class="options">
   <span><input type="radio" name="q4_pc" value="a"> a) sleep</span>
   <span><input type="radio" name="q4_pc" value="b"> b) sleeps</span>
   <span><input type="radio" name="q4_pc" value="c"> c) is sleeping</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: c) is sleeping</span>
   </li>
   <li>
   <label>What _____ he _____ (do) now?</label>
   <div class="options">
   <span><input type="radio" name="q5_pc" value="a"> a) do / do</span>
   <span><input type="radio" name="q5_pc" value="b"> b) does / do</span>
   <span><input type="radio" name="q5_pc" value="c"> c) is / doing</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: c) is / doing</span>
   </li>
   </ol>
   </div>
   </div>
   </div>
   
   <!-- Present Perfect -->
   <div class="grammar-topic">
   <h3 class="speakable-heading">3. زمن المضارع التام (Present Perfect)</h3>
   <p class="grammar-text">يُستخدم للتعبير عن أفعال بدأت في الماضي ولها تأثير على الحاضر، أو أفعال حدثت في وقت غير محدد في الماضي.</p>
   <ul>
   <li>**الاستخدامات:**
   <ul>
   <li>تجارب سابقة: I <span class="speakable-word">have visited</span> London three times. (لقد زرت لندن ثلاث مرات.)</li>
   <li>أفعال بدأت في الماضي وما زالت مستمرة: She <span class="speakable-word">has lived</span> here for five years. (لقد عاشت هنا لمدة خمس سنوات.)</li>
   </ul>
   </li>
   <li>**الكلمات الدالة:** <span class="speakable-word">already</span>, <span class="speakable-word">yet</span>, <span class="speakable-word">just</span>, <span class="speakable-word">ever</span>, <span class="speakable-word">never</span>, <span class="speakable-word">since</span>, <span class="speakable-word">for</span>, <span class="speakable-word">so far</span>, <span class="speakable-word">recently</span>, <span class="speakable-word">lately</span>.</li>
   <li>**أمثلة وجمل (10 أمثلة):**
   <ul>
   <li>They <span class="speakable-word">have bought</span> a new car. (لقد اشتروا سيارة جديدة.)</li>
   <li>I <span class="speakable-word">haven't seen</span> him since last week. (لم أره منذ الأسبوع الماضي.)</li>
   <li><span class="speakable-word">Have</span> you <span class="speakable-word">ever been</span> to New York? (هل سبق لك أن زرت نيويورك؟)</li>
   <li>She <span class="speakable-word">has just finished</span> her homework. (لقد أنهت واجباتها للتو.)</li>
   <li>We <span class="speakable-word">have lived</span> in this city for ten years. (لقد عشنا في هذه المدينة لمدة عشر سنوات.)</li>
   </ul>
   </li>
   </ul>
   
   <div class="exercises-section">
   <h4>أسئلة تدريبية على المضارع التام (Present Perfect)</h4>
   <p>اختر الإجابة الصحيحة:</p>
   <div class="question-group">
   <ol>
   <li>
   <label>I _____ (visit) London three times.</label>
   <div class="options">
   <span><input type="radio" name="q1_pp" value="a"> a) visit</span>
   <span><input type="radio" name="q1_pp" value="b"> b) visited</span>
   <span><input type="radio" name="q1_pp" value="c"> c) have visited</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: c) have visited</span>
   </li>
   <li>
   <label>She _____ (not / finish) her homework yet.</label>
   <div class="options">
   <span><input type="radio" name="q2_pp" value="a"> a) hasn't finished</span>
   <span><input type="radio" name="q2_pp" value="b"> b) haven't finished</span>
   <span><input type="radio" name="q2_pp" value="c"> c) didn't finish</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: a) hasn't finished</span>
   </li>
   <li>
   <label>_____ you ever _____ (be) to New York?</label>
   <div class="options">
   <span><input type="radio" name="q3_pp" value="a"> a) Did / be</span>
   <span><input type="radio" name="q3_pp" value="b"> b) Have / been</span>
   <span><input type="radio" name="q3_pp" value="c"> c) Are / being</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) Have / been</span>
   </li>
   <li>
   <label>He _____ just _____ (eat) dinner.</label>
   <div class="options">
   <span><input type="radio" name="q4_pp" value="a"> a) has / eaten</span>
   <span><input type="radio" name="q4_pp" value="b"> b) have / eaten</span>
   <span><input type="radio" name="q4_pp" value="c"> c) had / eaten</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: a) has / eaten</span>
   </li>
   <li>
   <label>They _____ (live) here since 2010.</label>
   <div class="options">
   <span><input type="radio" name="q5_pp" value="a"> a) live</span>
   <span><input type="radio" name="q5_pp" value="b"> b) lived</span>
   <span><input type="radio" name="q5_pp" value="c"> c) have lived</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: c) have lived</span>
   </li>
   </ol>
   </div>
   </div>
   </div>
   
   <!-- Past Simple -->
   <div class="grammar-topic">
   <h3 class="speakable-heading">4. زمن الماضي البسيط (Past Simple)</h3>
   <p class="grammar-text">يُستخدم للتعبير عن أفعال أو أحداث انتهت في وقت محدد في الماضي.</p>
   <ul>
   <li>**الاستخدامات:**
   <ul>
   <li>أحداث منتهية في الماضي: I <span class="speakable-word">went</span> to the cinema yesterday. (ذهبت إلى السينما أمس.)</li>
   <li>سلسلة من الأحداث في الماضي: She <span class="speakable-word">woke up</span>, <span class="speakable-word">ate</span> breakfast, and <span class="speakable-word">left</span> for work. (استيقظت، أكلت الفطور، وغادرت للعمل.)</li>
   </ul>
   </li>
   <li>**الكلمات الدالة:** <span class="speakable-word">yesterday</span>, <span class="speakable-word">last night</span>/<span class="speakable-word">week</span>/<span class="speakable-word">month</span>/<span class="speakable-word">year</span>, <span class="speakable-word">ago</span>, <span class="speakable-word">in 2005</span>, <span class="speakable-word">when I was young</span>.</li>
   <li>**أمثلة وجمل (10 أمثلة):**
   <ul>
   <li>He <span class="speakable-word">played</span> football an hour ago. (لعب كرة القدم قبل ساعة.)</li>
   <li>We <span class="speakable-word">didn't go</span> to the party. (لم نذهب إلى الحفلة.)</li>
   <li><span class="speakable-word">Did</span> you <span class="speakable-word">see</span> her? (هل رأيتها؟)</li>
   <li>She <span class="speakable-word">visited</span> her grandparents last weekend. (زارت أجدادها نهاية الأسبوع الماضي.)</li>
   <li>They <span class="speakable-word">moved</span> to London in 2010. (انتقلوا إلى لندن في 2010.)</li>
   </ul>
   </li>
   </ul>
   
   <div class="exercises-section">
   <h4>أسئلة تدريبية على الماضي البسيط (Past Simple)</h4>
   <p>اختر الإجابة الصحيحة:</p>
   <div class="question-group">
   <ol>
   <li>
   <label>He _____ (go) to school yesterday.</label>
   <div class="options">
   <span><input type="radio" name="q1_past" value="a"> a) go</span>
   <span><input type="radio" name="q1_past" value="b"> b) goes</span>
   <span><input type="radio" name="q1_past" value="c"> c) went</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: c) went</span>
   </li>
   <li>
   <label>She _____ (not / eat) breakfast this morning.</label>
   <div class="options">
   <span><input type="radio" name="q2_past" value="a"> a) didn't eat</span>
   <span><input type="radio" name="q2_past" value="b"> b) doesn't eat</span>
   <span><input type="radio" name="q2_past" value="c"> c) hasn't eaten</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: a) didn't eat</span>
   </li>
   <li>
   <label>_____ you _____ (see) the movie last night?</label>
   <div class="options">
   <span><input type="radio" name="q3_past" value="a"> a) Did / see</span>
   <span><input type="radio" name="q3_past" value="b"> b) Do / see</span>
   <span><input type="radio" name="q3_past" value="c"> c) Are / seeing</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: a) Did / see</span>
   </li>
   <li>
   <label>They _____ (play) football last Saturday.</label>
   <div class="options">
   <span><input type="radio" name="q4_past" value="a"> a) play</span>
   <span><input type="radio" name="q4_past" value="b"> b) played</span>
   <span><input type="radio" name="q4_past" value="c"> c) plays</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) played</span>
   </li>
   <li>
   <label>I _____ (be) in London last year.</label>
   <div class="options">
   <span><input type="radio" name="q5_past" value="a"> a) am</span>
   <span><input type="radio" name="q5_past" value="b"> b) was</span>
   <span><input type="radio" name="q5_past" value="c"> c) were</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) was</span>
   </li>
   </ol>
   </div>
   </div>
   </div>
   
   <!-- Future Simple -->
   <div class="grammar-topic">
   <h3 class="speakable-heading">5. زمن المستقبل البسيط (Future Simple)</h3>
   <p class="grammar-text">يُستخدم للتعبير عن قرارات سريعة، تنبؤات، وعروض.</p>
   <ul>
   <li>**الاستخدامات:**
   <ul>
   <li>قرارات لحظية: I <span class="speakable-word">will help</span> you. (سأساعدك.)</li>
   <li>تنبؤات (معتقد شخصي): I think it <span class="speakable-word">will rain</span> tomorrow. (أعتقد أنها ستمطر غداً.)</li>
   </ul>
   </li>
   <li>**الكلمات الدالة:** <span class="speakable-word">tomorrow</span>, <span class="speakable-word">next week</span>/<span class="speakable-word">month</span>/<span class="speakable-word">year</span>, <span class="speakable-word">in the future</span>, <span class="speakable-word">soon</span>, <span class="speakable-word">probably</span>, <span class="speakable-word">I think</span>, <span class="speakable-word">I believe</span>.</li>
   <li>**أمثلة وجمل (10 أمثلة):**
   <ul>
   <li>They <span class="speakable-word">will travel</span> to Spain next year. (سيسافرون إلى إسبانيا العام القادم.)</li>
   <li>She <span class="speakable-word">won't forget</span> you. (هي لن تنساك.)</li>
   <li><span class="speakable-word">Will</span> you <span class="speakable-word">come</span> to the party? (هل ستأتي إلى الحفلة؟)</li>
   <li>I <span class="speakable-word">will call</span> you later. (سأتصل بك لاحقاً.)</li>
   <li>He <span class="speakable-word">will not pass</span> the exam. (هو لن يجتاز الامتحان.)</li>
   </ul>
   </li>
   </ul>
   
   <div class="exercises-section">
   <h4>أسئلة تدريبية على المستقبل البسيط (Future Simple)</h4>
   <p>اختر الإجابة الصحيحة:</p>
   <div class="question-group">
   <ol>
   <li>
   <label>She _____ (visit) her parents tomorrow.</label>
   <div class="options">
   <span><input type="radio" name="q1_future" value="a"> a) visit</span>
   <span><input type="radio" name="q1_future" value="b"> b) visits</span>
   <span><input type="radio" name="q1_future" value="c"> c) will visit</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: c) will visit</span>
   </li>
   <li>
   <label>They _____ (not / come) to the meeting.</label>
   <div class="options">
   <span><input type="radio" name="q2_future" value="a"> a) won't come</span>
   <span><input type="radio" name="q2_future" value="b"> b) don't come</span>
   <span><input type="radio" name="q2_future" value="c"> c) aren't coming</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: a) won't come</span>
   </li>
   <li>
   <label>_____ you _____ (help) me with this?</label>
   <div class="options">
   <span><input type="radio" name="q3_future" value="a"> a) Do / help</span>
   <span><input type="radio" name="q3_future" value="b"> b) Are / helping</span>
   <span><input type="radio" name="q3_future" value="c"> c) Will / help</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: c) Will / help</span>
   </li>
   <li>
   <label>I think it _____ (rain) later.</label>
   <div class="options">
   <span><input type="radio" name="q4_future" value="a"> a) rain</span>
   <span><input type="radio" name="q4_future" value="b"> b) rains</span>
   <span><input type="radio" name="q4_future" value="c"> c) will rain</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: c) will rain</span>
   </li>
   <li>
   <label>We _____ (be) there at 8 PM.</label>
   <div class="options">
   <span><input type="radio" name="q5_future" value="a"> a) are</span>
   <span><input type="radio" name="q5_future" value="b"> b) will be</span>
   <span><input type="radio" name="q5_future" value="c"> c) be</span>
   </div>
   <span class="correct-answer">الإجابة الصحيحة: b) will be</span>
   </li>
   </ol>
   </div>
   </div>
   </div>
   </section>
   </main>
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ألعاب تعلم الإنجليزية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
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
</head>
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
</body>
</html>

   
   <footer>
   <p>مصمم بـ ❤️ لأحباب اللغة الإنجليزية</p>
   <p>&copy; 2024 تعلم الإنجليزية. جميع الحقوق محفوظة.</p>
   </footer>
   
   <script>
   document.addEventListener('DOMContentLoaded', () => {
   // Function to speak text
   function speakText(text, lang = 'en-US') {
   const synth = window.speechSynthesis;
   if (synth.speaking) {
   synth.cancel();
   }
   const utterance = new SpeechSynthesisUtterance(text);
   utterance.lang = lang;
   synth.speak(utterance);
   }
   
   // Add click event listeners
   document.querySelectorAll('.speakable-heading, .speakable-word').forEach(element => {
   element.addEventListener('click', function() {
   const textToSpeak = this.textContent;
   if (this.classList.contains('speakable-heading')) {
   const match = textToSpeak.match(/\((.*?)\)/);
   if (match && match[1]) {
   speakText(match[1], 'en-US');
   } else {
   speakText(textToSpeak, 'ar-SA');
   }
   } else if (this.classList.contains('speakable-word')) {
   speakText(textToSpeak, 'en-US');
   }
   });
   });
   
   // Highlight correct answers on click
   document.querySelectorAll('input[type="radio"]').forEach(radio => {
   radio.addEventListener('click', function() {
   const correctAnswer = this.closest('li').querySelector('.correct-answer');
   correctAnswer.style.display = 'block';
   });
   });
   });
   </script>
   </body>
   </html>
