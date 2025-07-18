<!DOCTYPE html>
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
            --primary-color: #3498db;
            --secondary-color: #2ecc71;
            --text-color: #333;
            --bg-color: #f4f7f6;
            --card-bg: #ffffff;
            --border-color: #ddd;
            --shadow-color: rgba(0, 0, 0, 0.1);
        }

        body {
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            direction: rtl; /* Set text direction to Right-to-Left */
            text-align: right; /* Align text to the right */
        }

        header {
            background-color: var(--primary-color);
            color: white;
            padding: 1.5em 0;
            text-align: center;
            box-shadow: 0 2px 5px var(--shadow-color);
        }

        header h1 {
            margin: 0;
            font-size: 2.5em;
        }

        main {
            padding: 20px;
            max-width: 1200px;
            margin: 20px auto;
            background-color: var(--card-bg);
            border-radius: 8px;
            box-shadow: 0 0 15px var(--shadow-color);
        }

        section {
            margin-bottom: 40px;
            padding-bottom: 20px;
            border-bottom: 1px solid var(--border-color);
        }

        section:last-of-type {
            border-bottom: none;
        }

        h2 {
            color: var(--primary-color);
            text-align: center;
            margin-bottom: 30px;
            font-size: 2em;
            border-bottom: 2px solid var(--secondary-color);
            display: inline-block;
            padding-bottom: 5px;
        }

        h3 {
            color: var(--text-color);
            font-size: 1.5em;
            margin-top: 25px;
            margin-bottom: 15px;
        }

        p.instruction {
            text-align: center;
            font-style: italic;
            color: #666;
            margin-bottom: 20px;
        }

        /* Alphabet Section */
        .alphabet-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .alphabet-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            box-shadow: 0 2px 8px var(--shadow-color);
            padding: 20px;
            width: calc(33% - 40px); /* 3 cards per row, accounting for gap */
            box-sizing: border-box;
            display: flex;
            flex-direction: column;
            align-items: center;
            transition: transform 0.2s ease-in-out;
        }

        .alphabet-card:hover {
            transform: translateY(-5px);
        }

        .alphabet-card h3 {
            color: var(--secondary-color);
            font-size: 2.2em;
            margin-top: 0;
            margin-bottom: 15px;
            text-align: center;
            width: 100%; /* Ensure heading takes full width for center alignment */
        }

        .alphabet-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }

        .alphabet-table th, .alphabet-table td {
            border: 1px solid var(--border-color);
            padding: 10px;
            text-align: center;
        }

        .alphabet-table th {
            background-color: var(--primary-color);
            color: white;
            font-weight: bold;
        }

        .alphabet-table tr:nth-child(even) {
            background-color: #f9f9f9;
        }

        .alphabet-table tr:hover {
            background-color: #f1f1f1;
        }

        .english-word {
            cursor: pointer;
            font-weight: bold;
            color: var(--primary-color);
            transition: color 0.2s ease-in-out;
        }

        .english-word:hover {
            color: var(--secondary-color);
            text-decoration: underline;
        }

        /* Grammar and Tenses Sections */
        .grammar-topic {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: 0 2px 8px var(--shadow-color);
        }

        .grammar-topic h3 {
            cursor: pointer; /* Make headings speakable */
            color: var(--primary-color);
            font-size: 1.8em;
            margin-top: 0;
            border-bottom: 1px dashed var(--border-color);
            padding-bottom: 10px;
            transition: color 0.2s ease-in-out;
        }

        .grammar-topic h3:hover {
            color: var(--secondary-color);
        }

        .grammar-text {
            margin-bottom: 15px;
        }

        .grammar-topic ul {
            list-style: none; /* Remove default bullet */
            padding-right: 0; /* Remove default padding */
        }

        .grammar-topic ul li {
            position: relative;
            padding-right: 25px; /* Space for custom bullet */
            margin-bottom: 10px;
        }

        .grammar-topic ul li::before {
            content: '•'; /* Custom bullet */
            color: var(--secondary-color);
            font-weight: bold;
            position: absolute;
            right: 0;
        }

        .grammar-topic ul ul {
            margin-top: 5px;
            margin-bottom: 5px;
        }

        .grammar-topic ul ul li::before {
            content: '–'; /* Sub-bullet */
            color: var(--primary-color);
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
        .common-words-table-container {
            overflow-x: auto; /* Enable horizontal scrolling if table is too wide */
        }

        .common-words-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }

        .common-words-table th,
        .common-words-table td {
            border: 1px solid var(--border-color);
            padding: 12px;
            text-align: center;
            font-size: 0.95em;
        }

        .common-words-table thead th {
            background-color: var(--primary-color);
            color: white;
            font-weight: bold;
        }

        .common-words-table tbody tr:nth-child(even) {
            background-color: #f9f9f9;
        }

        .common-words-table tbody tr:hover {
            background-color: #f1f1f1;
        }

        .common-words-table .english-word {
            cursor: pointer;
            font-weight: bold;
            color: var(--primary-color);
            transition: color 0.2s ease-in-out;
        }

        .common-words-table .english-word:hover {
            color: var(--secondary-color);
            text-decoration: underline;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            background-color: var(--primary-color);
            color: white;
            margin-top: 40px;
            border-radius: 0 0 8px 8px;
            box-shadow: 0 -2px 5px var(--shadow-color);
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .alphabet-card {
                width: calc(50% - 30px); /* 2 cards per row */
            }
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2em;
            }
            h2 {
                font-size: 1.8em;
            }
            h3 {
                font-size: 1.3em;
            }
            .alphabet-card {
                width: 100%; /* 1 card per row */
            }
            main {
                margin: 10px auto;
                padding: 15px;
            }
            .common-words-table th,
            .common-words-table td {
                padding: 8px;
                font-size: 0.85em;
            }
        }

        @media (max-width: 480px) {
            header h1 {
                font-size: 1.8em;
            }
            h2 {
                font-size: 1.6em;
            }
            h3 {
                font-size: 1.2em;
            }
            .alphabet-table th, .alphabet-table td {
                padding: 8px;
                font-size: 0.9em;
            }
            .common-words-table th,
            .common-words-table td {
                padding: 6px;
                font-size: 0.8em;
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
            <div class="alphabet-container">
                </div>
        </section>

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
                    <li>**ضمائر الفاعل (Subject Pronouns):** تحل محل الاسم الذي يقوم بالفعل.
                        <ul>
                            <li><span class="speakable-word">I</span> (أنا), <span class="speakable-word">you</span> (أنت/أنتم), <span class="speakable-word">he</span> (هو), <span class="speakable-word">she</span> (هي), <span class="speakable-word">it</span> (هو/هي لغير العاقل), <span class="speakable-word">we</span> (نحن), <span class="speakable-word">they</span> (هم/هن).</li>
                            <li>**أمثلة:** <span class="speakable-word">She</span> is my sister. (هي أختي.) <span class="speakable-word">They</span> live in Cairo. (هم يعيشون في القاهرة.)</li>
                        </ul>
                    </li>
                    <li>**ضمائر المفعول به (Object Pronouns):** تحل محل الاسم الذي يقع عليه الفعل.
                        <ul>
                            <li><span class="speakable-word">me</span> (لي/إياي), <span class="speakable-word">you</span> (لك/إياك), <span class="speakable-word">him</span> (له/إياه), <span class="speakable-word">her</span> (لها/إياها), <span class="speakable-word">it</span> (له/إياه لغير العاقل), <span class="speakable-word">us</span> (لنا/إيانا), <span class="speakable-word">them</span> (لهم/إياهم).</li>
                            <li>**أمثلة:** He gave the book to <span class="speakable-word">me</span>. (أعطاني الكتاب.) I saw <span class="speakable-word">him</span> yesterday. (رأيته أمس.)</li>
                        </ul>
                    </li>
                    <li>**صفات الملكية (Possessive Adjectives):** تأتي قبل الاسم لتوضح ملكيته.
                        <ul>
                            <li><span class="speakable-word">my</span> (ملكي), <span class="speakable-word">your</span> (ملكك/ملككم), <span class="speakable-word">his</span> (ملكه), <span class="speakable-word">her</span> (ملكها), <span class="speakable-word">its</span> (ملكه/ملكها لغير العاقل), <span class="speakable-word">our</span> (ملكنا), <span class="speakable-word">their</span> (ملكهم/ملكهن).</li>
                            <li>**أمثلة:** This is <span class="speakable-word">my</span> car. (هذه سيارتي.) <span class="speakable-word">Their</span> house is big. (منزلهم كبير.)</li>
                        </ul>
                    </li>
                    <li>**ضمائر الملكية (Possessive Pronouns):** تحل محل الاسم وصفة الملكية معاً.
                        <ul>
                            <li><span class="speakable-word">mine</span> (ملكي), <span class="speakable-word">yours</span> (ملكك/ملككم), <span class="speakable-word">his</span> (ملكه), <span class="speakable-word">hers</span> (ملكها), <span class="speakable-word">its</span> (ملكه/ملكها لغير العاقل), <span class="speakable-word">ours</span> (ملكنا), <span class="speakable-word">theirs</span> (ملكهم/ملكهن).</li>
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
            <div class="common-words-table-container">
                <table class="common-words-table">
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
                    <tbody>
                        </tbody>
                </table>
            </div>
        </section>

    </main>

    <footer>
        <p>&copy; 2024 تعلم الإنجليزية. جميع الحقوق محفوظة.</p>
    </footer>

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


            const alphabetContainer = document.querySelector('.alphabet-container');
            const commonWordsTbody = document.querySelector('.common-words-table tbody');

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

            // Generate common words table dynamically
            const wordsPerColumn = 10; // 50 rows / 5 columns = 10 words per column
            const totalRows = 50;
            const numColumns = 5;

            for (let i = 0; i < totalRows; i++) {
                const row = document.createElement('tr');
                for (let j = 0; j < numColumns; j++) {
                    const wordIndex = (j * wordsPerColumn) + i; // Calculate index for word in commonWordsData

                    const enCell = document.createElement('td');
                    const arCell = document.createElement('td');

                    if (wordIndex < commonWordsData.length) {
                        const word = commonWordsData[wordIndex];
                        const enSpan = document.createElement('span');
                        enSpan.classList.add('english-word');
                        enSpan.textContent = word.en;
                        enSpan.addEventListener('click', () => speakText(word.en, 'en-US'));

                        enCell.appendChild(enSpan);
                        arCell.textContent = word.ar;
                    } else {
                        // Fill empty cells if not enough words
                        enCell.textContent = '';
                        arCell.textContent = '';
                    }
                    row.appendChild(enCell);
                    row.appendChild(arCell);
                }
                commonWordsTbody.appendChild(row);
            }


            // Add click event listeners for grammar headings and speakable words
            document.querySelectorAll('.speakable-heading, .speakable-word').forEach(element => {
                element.addEventListener('click', function() {
                    const textToSpeak = this.textContent;
                    if (this.classList.contains('speakable-heading')) {
                        const match = textToSpeak.match(/\((.*?)\)/);
                        if (match && match[1]) {
                            speakText(match[1], 'en-US');
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

                    const paragraphs = this.querySelectorAll('p, li');
                    let fullText = '';
                    paragraphs.forEach(p => {
                        // Extract only Arabic text for speaking the full section
                        let arabicText = p.textContent.replace(/\(.*?\)/g, '').trim(); // Remove text in parentheses
                        arabicText = arabicText.replace(/[a-zA-Z]/g, '').trim(); // Remove all English letters
                        if (arabicText) {
                            fullText += arabicText + ' ';
                        }
                    });
                    if (fullText.trim()) {
                        speakText(fullText.trim(), 'ar-SA'); // Speak the whole paragraph/list item in Arabic
                    }
                });
            });
        });
    </script>
</body>
</html>
