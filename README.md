<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>يوم جمعة سعيد - قواعد الإنجليزية</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* الأساسيات والخلفية */
        body {
            font-family: 'Cairo', sans-serif;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #FFD700, #FF6347);
            color: #FFFFFF;
            overflow-x: hidden;
            position: relative;
            padding-bottom: 80px;
        }

        /* الحاوية الرئيسية للصفحة */
        .container {
            text-align: center;
            background-color: rgba(0, 0, 0, 0.6);
            padding: 30px 40px;
            border-radius: 20px;
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.4);
            transform: scale(0.95);
            animation: appearScale 1.5s ease-out forwards;
            margin-top: 50px;
            margin-bottom: 25px;
            max-width: 900px;
            width: 90%;
            box-sizing: border-box;
            backdrop-filter: blur(5px);
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        @keyframes appearScale {
            from { transform: scale(0); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }

        h1 {
            font-size: 3.2em;
            margin-bottom: 25px;
            color: #FFFF00;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.6);
            animation: bounceIn 1s ease-out;
            letter-spacing: 2px;
        }

        @keyframes bounceIn {
            0%, 20%, 40%, 60%, 80%, 100% { transition-timing-function: cubic-bezier(0.215, .61, .355, 1); }
            0% { opacity: 0; transform: scale3d(.3, .3, .3); }
            20% { transform: scale3d(1.1, 1.1, 1.1); }
            40% { transform: scale3d(.9, .9, .9); }
            60% { opacity: 1; transform: scale3d(1.03, 1.03, 1.03); }
            80% { transform: scale3d(.97, .97, .97); }
            100% { opacity: 1; transform: scale3d(1, 1, 1); }
        }

        /* تنسيق الجداول */
        .content-table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0 10px;
            margin-top: 20px;
            direction: rtl;
            animation: fadeIn 1s ease-out;
            text-align: right; /* محاذاة النص داخل الجدول لليمين */
        }

        .content-table th {
            background-color: rgba(255, 255, 255, 0.15);
            color: #FFFF00;
            padding: 12px 15px;
            font-size: 1.1em;
            text-align: center;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        
        .content-table th:first-child { border-top-right-radius: 8px; border-bottom-right-radius: 8px; }
        .content-table th:last-child { border-top-left-radius: 8px; border-bottom-left-radius: 8px; }

        .content-table td {
            background-color: rgba(255, 255, 255, 0.08);
            padding: 10px 15px;
            font-size: 1.05em;
            vertical-align: middle;
            border-radius: 8px;
            transition: background-color 0.3s ease, transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .content-table tr:hover td {
            background-color: rgba(255, 255, 255, 0.15);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
        }

        .content-table td:hover {
            transform: scale(1.01); /* تكبير أقل لتناسب النصوص الطويلة */
        }

        .english-text {
            color: #98FB98;
            font-weight: bold;
            text-align: left; /* النص الإنجليزي من اليسار لليمين */
            direction: ltr;
        }

        .arabic-text {
            color: #ADD8E6;
            text-align: right; /* النص العربي من اليمين لليسار */
            direction: rtl;
        }

        .read-button {
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 8px;
            padding: 8px 15px;
            cursor: pointer;
            font-size: 0.9em;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .read-button:hover {
            background-color: #0056b3;
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
        }
        .read-button:active {
            transform: translateY(0);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        /* تنسيق الأقسام الجديدة (القواعد والأزمنة) */
        .section-title {
            font-size: 2.2em;
            color: #FFFF00;
            margin-top: 50px;
            margin-bottom: 25px;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
            border-bottom: 3px solid #FFFF00;
            padding-bottom: 10px;
            width: 80%;
        }

        .section-content {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 30px;
            text-align: right;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            width: 100%;
            box-sizing: border-box;
        }

        .section-content p {
            font-size: 1.15em;
            line-height: 1.7;
            margin-bottom: 15px;
            color: #F0F8FF;
            text-align: justify; /* لمحاذاة النص */
        }

        .section-content ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .section-content li {
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            padding: 12px;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            font-size: 1.1em;
            text-align: right; /* للغة العربية */
            direction: rtl;
        }

        .section-content li .english-example {
            color: #98FB98;
            font-weight: bold;
            flex-grow: 1;
            text-align: left;
            direction: ltr;
        }
        .section-content li .arabic-example {
            color: #ADD8E6;
            margin-right: 15px; /* مسافة بين الإنجليزي والعربي */
        }

        .example-type {
            font-weight: bold;
            color: #FFEB3B;
            margin-bottom: 10px;
            display: block;
            text-align: right;
            font-size: 1.1em;
        }

        .exercise-item {
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 15px;
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.2);
            text-align: right;
        }

        .exercise-question {
            font-size: 1.1em;
            color: #F0F8FF;
            margin-bottom: 10px;
            text-align: right;
            direction: rtl;
        }
        .exercise-answer {
            color: #FFEB3B;
            font-weight: bold;
            font-size: 1.05em;
            margin-top: 5px;
            display: none; /* إخفاء الإجابات في البداية */
            text-align: left; /* لجعل الإجابة الإنجليزية تبدأ من اليسار */
            direction: ltr;
            background-color: rgba(0,0,0,0.3);
            padding: 8px;
            border-radius: 5px;
        }
        .show-answer-button {
            background-color: #28a745; /* لون أخضر */
            color: white;
            border: none;
            border-radius: 5px;
            padding: 8px 15px;
            cursor: pointer;
            font-size: 0.9em;
            margin-top: 10px;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }
        .show-answer-button:hover {
            background-color: #218838;
            transform: translateY(-2px);
        }

        /* أزرار التنقل بين الصفحات */
        .pagination-controls {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            gap: 20px;
            width: 100%;
        }

        .pagination-button {
            background-color: #FF5722;
            color: white;
            border: none;
            border-radius: 10px;
            padding: 12px 25px;
            font-size: 1.2em;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
        }

        .pagination-button:hover {
            background-color: #E64A19;
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
        }
        .pagination-button:active {
            transform: translateY(0);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .pagination-button:disabled {
            background-color: #ccc;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
            opacity: 0.7;
        }

        .page-info {
            font-size: 1.2em;
            color: #FFEB3B;
            align-self: center;
            margin: 0 10px;
        }

        /* الملاحظة وزر التحكم في الموسيقى */
        .note {
            margin-top: 30px;
            font-size: 1.3em;
            color: #ADD8E6;
            opacity: 0;
            animation: fadeIn 1s forwards;
            animation-delay: var(--note-delay);
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* تأثير الفقاعات */
        .bubble {
            position: fixed;
            bottom: -100px;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            animation: bubbleUp 15s infinite ease-in;
            z-index: -1;
        }

        .bubble:nth-child(1) { left: 10%; animation-duration: 12s; width: 60px; height: 60px; opacity: 0.7;}
        .bubble:nth-child(2) { left: 20%; animation-duration: 10s; animation-delay: 2s;}
        .bubble:nth-child(3) { left: 30%; animation-duration: 14s; width: 50px; height: 50px; opacity: 0.6;}
        .bubble:nth-child(4) { left: 40%; animation-duration: 11s; animation-delay: 1s;}
        .bubble:nth-child(5) { left: 50%; animation-duration: 13s; width: 45px; height: 45px; opacity: 0.5;}
        .bubble:nth-child(6) { left: 60%; animation-duration: 9s; animation-delay: 3s;}
        .bubble:nth-child(7) { left: 70%; animation-duration: 16s; width: 70px; height: 70px; opacity: 0.8;}
        .bubble:nth-child(8) { left: 80%; animation-duration: 10s; animation-delay: 4s;}

        @keyframes bubbleUp {
            0% { transform: translateY(0) scale(0.5); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateY(-100vh) scale(1.2); opacity: 0; }
        }

        #audioControl {
            margin-top: 25px;
            padding: 12px 25px;
            font-size: 1.3em;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
            opacity: 0;
            animation: fadeIn 1s forwards;
            animation-delay: var(--button-delay);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
            margin-bottom: 50px;
        }

        #audioControl:hover {
            background-color: #45a049;
            transform: translateY(-3px) scale(1.03);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4);
        }
        #audioControl:active {
            transform: translateY(0);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }

        /* تنسيق السكرولبار */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.1);
        }

        ::-webkit-scrollbar-thumb {
            background: #FFFF00;
            border-radius: 5px;
        }
        
    </style>
</head>
<body>
    <div class="container">
        <h1>يوم جمعة سعيد!</h1>
        <div id="wordsContainer">
            </div>
        <div class="pagination-controls">
            <button id="prevPage" class="pagination-button">السابق</button>
            <span id="pageInfo" class="page-info">الصفحة 1 من X</span>
            <button id="nextPage" class="pagination-button">التالي</button>
        </div>
        <p class="note" id="noteElement">نتمنى لكم عطلة نهاية أسبوع هادئة ومبهجة ومليئة بهذه اللحظات الرائعة!</p>
    </div>

    <button id="audioControl">تشغيل/إيقاف الموسيقى</button>

    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>

    <audio id="backgroundAudio" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <script>
        // دالة لخلط (shuffle) مصفوفة بطريقة عشوائية (Fisher-Yates shuffle)
        function shuffleArray(array) {
            for (let i = array.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [array[i], array[j]] = [array[j], array[i]];
            }
            return array;
        }

        const synth = window.speechSynthesis;

        function speakText(text) {
            if (synth.speaking) {
                synth.cancel();
            }
            const utterance = new SpeechSynthesisUtterance(text);
            utterance.lang = 'en-US';
            utterance.rate = 0.95;
            utterance.pitch = 1;

            const voices = synth.getVoices();
            utterance.voice = voices.find(voice => voice.lang.startsWith('en') && (voice.name.includes('Google') || voice.name.includes('Samantha') || voice.name.includes('Karen') || voice.name.includes('Zira')) || voice.lang.startsWith('en'));
            
            synth.speak(utterance);
        }

        const wordsContainer = document.getElementById('wordsContainer');
        const prevPageBtn = document.getElementById('prevPage');
        const nextPageBtn = document.getElementById('nextPage');
        const pageInfoSpan = document.getElementById('pageInfo');
        const noteElement = document.getElementById('noteElement');
        const audio = document.getElementById('backgroundAudio');
        const audioControl = document.getElementById('audioControl');
        let isPlaying = false;
        let startDelay = 1.6;

        let currentPage = 1;
        let totalPages = 0;
        const itemsPerPage = 1; // كل صفحة هتعرض جزء تعليمي واحد فقط

        const contentSections = [
            { id: 'vowels-consonants', title: 'الحروف الساكنة والمتحركة (Vowels & Consonants)', type: 'alphabet', content: null },
            { id: 'verb-to-be', title: 'قاعدة الفعل "To Be"', type: 'grammar', content: null },
            { id: 'he-is-it-is', title: '"He Is" و "It Is"', type: 'grammar', content: null },
            { id: 'verb-to-do', title: 'قاعدة الفعل "To Do"', type: 'grammar', content: null },
            { id: 'verb-to-have', title: 'قاعدة الفعل "To Have"', type: 'grammar', content: null },
            { id: 'present-simple', title: 'زمن المضارع البسيط (Present Simple)', type: 'grammar', content: null },
            { id: 'past-simple', title: 'زمن الماضي البسيط (Past Simple)', type: 'grammar', content: null },
            { id: 'present-continuous', title: 'زمن المضارع المستمر (Present Continuous)', type: 'grammar', content: null },
            { id: 'past-perfect', title: 'زمن الماضي التام (Past Perfect)', type: 'grammar', content: null },
        ];


        // بيانات الحروف الساكنة والمتحركة والتمارين
        const alphabetData = {
            vowels: ['A', 'E', 'I', 'O', 'U'],
            consonants: ['B', 'C', 'D', 'F', 'G', 'H', 'J', 'K', 'L', 'M', 'N', 'P', 'Q', 'R', 'S', 'T', 'V', 'W', 'X', 'Y', 'Z'],
            vowel_examples: [
                {en: "Apple", ar: "تفاحة"}, {en: "Elephant", ar: "فيل"}, {en: "Igloo", ar: "كوخ جليدي"}, {en: "Orange", ar: "برتقالة"}, {en: "Umbrella", ar: "مظلة"},
                {en: "Ant", ar: "نملة"}, {en: "Egg", ar: "بيضة"}, {en: "Island", ar: "جزيرة"}, {en: "Ostrich", ar: "نعامة"}, {en: "Up", ar: "أعلى"}
            ],
            consonant_examples: [
                {en: "Ball", ar: "كرة"}, {en: "Cat", ar: "قطة"}, {en: "Dog", ar: "كلب"}, {en: "Fish", ar: "سمكة"}, {en: "Goat", ar: "معزة"},
                {en: "House", ar: "منزل"}, {en: "Jug", ar: "إبريق"}, {en: "Kite", ar: "طائرة ورقية"}, {en: "Lamp", ar: "مصباح"}, {en: "Moon", ar: "قمر"}
            ],
            exercises: [
                {q: "Identify the vowels: B, A, C, E, D", a: "A, E"},
                {q: "Identify the consonants: I, F, O, G, U", a: "F, G"},
                {q: "Which word starts with a vowel? Cat / Apple", a: "Apple"},
                {q: "Which word starts with a consonant? Elephant / Dog", a: "Dog"},
                {q: "Is 'Y' a vowel or consonant in 'sky'?", a: "Vowel"},
                {q: "Is 'Y' a vowel or consonant in 'yellow'?", a: "Consonant"},
                {q: "Add a vowel to complete the word: B_x", a: "Box"},
                {q: "Add a consonant to complete the word: _at", a: "Cat"},
                {q: "Circle the vowels: book", a: "o, o"},
                {q: "Circle the consonants: table", a: "t, b, l"},
                {q: "How many vowels in 'beautiful'?", a: "5 (e, a, u, i, u)"},
                {q: "How many consonants in 'computer'?", a: "5 (c, m, p, t, r)"},
                {q: "Fill in the blank with a vowel: R_d", a: "Red"},
                {q: "Fill in the blank with a consonant: _en", a: "Pen"},
                {q: "What type of letter is 'P'?", a: "Consonant"},
                {q: "What type of letter is 'O'?", a: "Vowel"},
                {q: "Find the odd one out: A, E, I, B, O", a: "B (It's a consonant)"},
                {q: "Find the odd one out: F, G, H, U, J", a: "U (It's a vowel)"},
                {q: "Complete the word with a vowel: Tr_ _", a: "Tree"},
                {q: "Complete the word with a consonant: _lower", a: "Flower"}
            ]
        };

        // دالة لبناء قسم الحروف الساكنة والمتحركة والتمارين
        function buildVowelsConsonantsSection() {
            let html = `
                <div class="section-content">
                    <p>في اللغة الإنجليزية، الحروف تنقسم إلى نوعين أساسيين: **الحروف المتحركة (Vowels)** و **الحروف الساكنة (Consonants)**.</p>
                    
                    <p><span class="example-type">الحروف المتحركة (Vowels):</span></p>
                    <ul>
                        <li><span class="english-example">${alphabetData.vowels.join(', ').toUpperCase()}</span></li>
                    </ul>
                    <p>الحروف المتحركة هي أصوات تُنتج بدون أي عائق في مجرى الهواء من الفم. هي أساس النطق في كل كلمة.</p>

                    <p><span class="example-type">أمثلة على كلمات تبدأ بحروف متحركة:</span></p>
                    <ul>
            `;
            alphabetData.vowel_examples.forEach(item => {
                html += `<li><span class="english-example">${item.en}</span><span class="arabic-example">${item.ar}</span><button class="read-button" onclick="speakText('${item.en}')">استمع</button></li>`;
            });
            html += `
                    </ul>

                    <p><span class="example-type">الحروف الساكنة (Consonants):</span></p>
                    <ul>
                        <li><span class="english-example">${alphabetData.consonants.join(', ').toUpperCase()}</span></li>
                    </ul>
                    <p>الحروف الساكنة هي أصوات تُنتج عن طريق إعاقة جزئية أو كلية لمجرى الهواء في الفم أو الحلق.</p>

                    <p><span class="example-type">أمثلة على كلمات تبدأ بحروف ساكنة:</span></p>
                    <ul>
            `;
            alphabetData.consonant_examples.forEach(item => {
                html += `<li><span class="english-example">${item.en}</span><span class="arabic-example">${item.ar}</span><button class="read-button" onclick="speakText('${item.en}')">استمع</button></li>`;
            });
            html += `
                    </ul>
                    
                    <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">تمارين على الحروف الساكنة والمتحركة</h3>
            `;
            alphabetData.exercises.forEach((ex, index) => {
                html += `
                    <div class="exercise-item">
                        <p class="exercise-question">${ex.q}</p>
                        <button class="show-answer-button" onclick="toggleAnswer(this, 'answer${index}')">أظهر الإجابة</button>
                        <p id="answer${index}" class="exercise-answer">${ex.a}</p>
                    </div>
                `;
            });
            html += `</div>`;
            return html;
        }

        // بيانات Verb To Be
        const verbToBeData = {
            explanation: `
                <p>الفعل <b>"To Be"</b> هو أحد أهم الأفعال في اللغة الإنجليزية، ويعني "يكون". يتغير شكله حسب الفاعل والزمن.</p>
                <p><span class="example-type">المضارع البسيط (Present Simple):</span></p>
                <ul>
                    <li><span class="english-example">I am</span> <span class="arabic-example">أنا أكون</span></li>
                    <li><span class="english-example">You are</span> <span class="arabic-example">أنت/أنتم تكونون</span></li>
                    <li><span class="english-example">He is</span> <span class="arabic-example">هو يكون</span></li>
                    <li><span class="english-example">She is</span> <span class="arabic-example">هي تكون</span></li>
                    <li><span class="english-example">It is</span> <span class="arabic-example">هو/هي يكون (لغير العاقل)</span></li>
                    <li><span class="english-example">We are</span> <span class="arabic-example">نحن نكون</span></li>
                    <li><span class="english-example">They are</span> <span class="arabic-example">هم/هن يكونون</span></li>
                </ul>
                <p><span class="example-type">الماضي البسيط (Past Simple):</span></p>
                <ul>
                    <li><span class="english-example">I was</span> <span class="arabic-example">أنا كنت</span></li>
                    <li><span class="english-example">You were</span> <span class="arabic-example">أنت/أنتم كنتم</span></li>
                    <li><span class="english-example">He was</span> <span class="arabic-example">هو كان</span></li>
                    <li><span class="english-example">She was</span> <span class="arabic-example">هي كانت</span></li>
                    <li><span class="english-example">It was</span> <span class="arabic-example">هو/هي كان (لغير العاقل)</span></li>
                    <li><span class="english-example">We were</span> <span class="arabic-example">نحن كنا</span></li>
                    <li><span class="english-example">They were</span> <span class="arabic-example">هم/هن كانوا</span></li>
                </ul>
                <p><span class="example-type">أمثلة:</span></p>
                <ul>
                    <li><span class="english-example">She is happy.</span> <span class="arabic-example">هي سعيدة.</span><button class="read-button" onclick="speakText('She is happy.')">استمع</button></li>
                    <li><span class="english-example">They are students.</span> <span class="arabic-example">هم طلاب.</span><button class="read-button" onclick="speakText('They are students.')">استمع</button></li>
                    <li><span class="english-example">I was tired yesterday.</span> <span class="arabic-example">كنت متعباً أمس.</span><button class="read-button" onclick="speakText('I was tired yesterday.')">استمع</button></li>
                    <li><span class="english-example">We were at the park.</span> <span class="arabic-example">كنا في المنتزه.</span><button class="read-button" onclick="speakText('We were at the park.')">استمع</button></li>
                </ul>
                <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">تمارين على Verb "To Be"</h3>
            `,
            exercises: [
                {q: "She ___ a doctor. (is/are)", a: "is"},
                {q: "We ___ friends. (am/are)", a: "are"},
                {q: "I ___ happy. (am/is)", a: "am"},
                {q: "They ___ playing. (was/were)", a: "were"},
                {q: "He ___ at home. (was/were)", a: "was"},
                {q: "It ___ a sunny day. (is/are)", a: "is"},
                {q: "You ___ a good student. (am/are)", a: "are"},
                {q: "My cat ___ sleeping. (is/am)", a: "is"},
                {q: "The children ___ in the garden. (was/were)", a: "were"},
                {q: "I ___ sick last week. (was/were)", a: "was"},
                {q: "He ___ 10 years old. (is/are)", a: "is"},
                {q: "We ___ going to the cinema tomorrow. (are/is)", a: "are"},
                {q: "She ___ studying now. (is/am)", a: "is"},
                {q: "They ___ busy. (are/is)", a: "are"},
                {q: "It ___ cold outside. (is/am)", a: "is"},
                {q: "You ___ very kind. (are/am)", a: "are"},
                {q: "He ___ tall. (is/are)", a: "is"},
                {q: "I ___ a student. (am/is)", a: "am"},
                {q: "They ___ laughing. (are/is)", a: "are"},
                {q: "We ___ happy to see you. (are/am)", a: "are"},
                {q: "The book ___ on the table. (is/are)", a: "is"},
                {q: "My parents ___ coming tonight. (are/is)", a: "are"}
            ]
        };

        // بيانات He Is و It Is
        const heItIsData = {
            explanation: `
                <p>تُستخدم <b>"He Is"</b> و <b>"It Is"</b> للإشارة إلى أشخاص أو أشياء محددة.</p>
                <p><span class="example-type">He Is (هو يكون):</span></p>
                <p>تُستخدم للإشارة إلى <b>ذكر مفرد عاقل</b> (شخص أو حيوان ذكر محدد له اسم).</p>
                <ul>
                    <li><span class="english-example">He is a boy.</span> <span class="arabic-example">هو ولد.</span><button class="read-button" onclick="speakText('He is a boy.')">استمع</button></li>
                    <li><span class="english-example">He is my brother.</span> <span class="arabic-example">هو أخي.</span><button class="read-button" onclick="speakText('He is my brother.')">استمع</button></li>
                    <li><span class="english-example">He is reading.</span> <span class="arabic-example">هو يقرأ.</span><button class="read-button" onclick="speakText('He is reading.')">استمع</button></li>
                </ul>
                <p><span class="example-type">It Is (هو/هي يكون):</span></p>
                <p>تُستخدم للإشارة إلى <b>مفرد غير عاقل</b> (جماد، حيوان غير محدد جنسه أو اسمه، فكرة، طقس، وقت).</p>
                <ul>
                    <li><span class="english-example">It is a chair.</span> <span class="arabic-example">إنه كرسي.</span><button class="read-button" onclick="speakText('It is a chair.')">استمع</button></li>
                    <li><span class="english-example">It is raining.</span> <span class="arabic-example">إنها تمطر.</span><button class="read-button" onclick="speakText('It is raining.')">استمع</button></li>
                    <li><span class="english-example">It is 3 o'clock.</span> <span class="arabic-example">إنها الساعة الثالثة.</span><button class="read-button" onclick="speakText('It is 3 o\'clock.')">استمع</button></li>
                    <li><span class="english-example">It is a cat.</span> <span class="arabic-example">إنها قطة.</span><button class="read-button" onclick="speakText('It is a cat.')">استمع</button></li>
                </ul>
                <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">تمارين على "He Is" و "It Is"</h3>
            `,
            exercises: [
                {q: "___ a beautiful day. (He is / It is)", a: "It is"},
                {q: "___ my father. (He is / It is)", a: "He is"},
                {q: "___ a new car. (He is / It is)", a: "It is"},
                {q: "___ playing football. (He is / It is)", a: "He is"},
                {q: "___ a big house. (He is / It is)", a: "It is"},
                {q: "___ my teacher. (He is / It is)", a: "He is"},
                {q: "___ cold outside. (He is / It is)", a: "It is"},
                {q: "___ a dog. (He is / It is)", a: "It is"},
                {q: "___ very smart. (He is / It is)", a: "He is"},
                {q: "___ 7 PM. (He is / It is)", a: "It is"},
                {q: "___ a challenging task. (He is / It is)", a: "It is"},
                {q: "___ my best friend. (He is / It is)", a: "He is"},
                {q: "___ easy to learn. (He is / It is)", a: "It is"},
                {q: "___ reading a book. (He is / It is)", a: "He is"},
                {q: "___ a historical place. (He is / It is)", a: "It is"},
                {q: "___ my manager. (He is / It is)", a: "He is"},
                {q: "___ getting late. (He is / It is)", a: "It is"},
                {q: "___ a new project. (He is / It is)", a: "It is"},
                {q: "___ very kind. (He is / It is)", a: "He is"},
                {q: "___ fun to play. (He is / It is)", a: "It is"}
            ]
        };

        // بيانات Verb To Do
        const verbToDoData = {
            explanation: `
                <p>الفعل <b>"To Do"</b> يعني "يفعل" أو "يعمل". يُستخدم كفعل رئيسي أو فعل مساعد (Auxiliary Verb) في الأسئلة والنفي.</p>
                <p><span class="example-type">كفعل رئيسي:</span></p>
                <ul>
                    <li><span class="english-example">I do my homework.</span> <span class="arabic-example">أنا أعمل واجبي.</span><button class="read-button" onclick="speakText('I do my homework.')">استمع</button></li>
                    <li><span class="english-example">She does a great job.</span> <span class="arabic-example">هي تقوم بعمل رائع.</span><button class="read-button" onclick="speakText('She does a great job.')">استمع</button></li>
                </ul>
                <p><span class="example-type">كفعل مساعد (في المضارع البسيط):</span></p>
                <ul>
                    <li><span class="english-example">Do you like coffee?</span> <span class="arabic-example">هل تحب القهوة؟</span><button class="read-button" onclick="speakText('Do you like coffee?')">استمع</button></li>
                    <li><span class="english-example">She does not sing.</span> <span class="arabic-example">هي لا تغني.</span><button class="read-button" onclick="speakText('She does not sing.')">استمع</button></li>
                    <li><span class="english-example">They don't know.</span> <span class="arabic-example">هم لا يعرفون.</span><button class="read-button" onclick="speakText('They don\'t know.')">استمع</button></li>
                </ul>
                 <p><span class="example-type">الماضي البسيط (Did):</span></p>
                <ul>
                    <li><span class="english-example">I did my best.</span> <span class="arabic-example">لقد بذلت قصارى جهدي.</span><button class="read-button" onclick="speakText('I did my best.')">استمع</button></li>
                    <li><span class="english-example">Did you go?</span> <span class="arabic-example">هل ذهبت؟</span><button class="read-button" onclick="speakText('Did you go?')">استمع</button></li>
                    <li><span class="english-example">He didn't come.</span> <span class="arabic-example">هو لم يأتِ.</span><button class="read-button" onclick="speakText('He didn\'t come.')">استمع</button></li>
                </ul>
                <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">تمارين على Verb "To Do"</h3>
            `,
            exercises: [
                {q: "I ___ my homework every day. (do/does)", a: "do"},
                {q: "She ___ not like pizza. (do/does)", a: "does"},
                {q: "___ you play sports? (Do/Does)", a: "Do"},
                {q: "He ___ his job well. (do/does)", a: "does"},
                {q: "They ___ not understand. (do/does)", a: "do"},
                {q: "We ___ exercise in the morning. (do/does)", a: "do"},
                {q: "___ she speak French? (Do/Does)", a: "Does"},
                {q: "It ___ not matter. (do/does)", a: "does"},
                {q: "You ___ a lot of work. (do/does)", a: "do"},
                {q: "My brother ___ not watch TV. (do/does)", a: "does"},
                {q: "I ___ not know the answer. (do/does)", a: "do"},
                {q: "What ___ you do?", a: "do"},
                {q: "When ___ he arrive?", a: "did"},
                {q: "They ___ not call me. (did/do)", a: "did"},
                {q: "She ___ not eat meat. (did/does)", a: "does"},
                {q: "___ you finish the report yesterday? (Did/Do)", a: "Did"},
                {q: "We ___ our best. (did/do)", a: "did"},
                {q: "He ___ not go to school today. (did/does)", a: "did"},
                {q: "How ___ you feel now? (do/did)", a: "do"},
                {q: "I ___ not agree with you. (do/does)", a: "do"}
            ]
        };

        // بيانات Verb To Have
        const verbToHaveData = {
            explanation: `
                <p>الفعل <b>"To Have"</b> يعني "يملك" أو "لديه"، ويُستخدم أيضاً كفعل مساعد في الأزمنة التامة.</p>
                <p><span class="example-type">كفعل رئيسي (للتملك):</span></p>
                <ul>
                    <li><span class="english-example">I have a car.</span> <span class="arabic-example">أنا أملك سيارة.</span><button class="read-button" onclick="speakText('I have a car.')">استمع</button></li>
                    <li><span class="english-example">She has a brother.</span> <span class="arabic-example">هي لديها أخ.</span><button class="read-button" onclick="speakText('She has a brother.')">استمع</button></li>
                </ul>
                <p><span class="example-type">للتعبير عن الخبرات أو الأفعال:</span></p>
                <ul>
                    <li><span class="english-example">We have breakfast at 7 AM.</span> <span class="arabic-example">نتناول الفطور الساعة 7 صباحًا.</span><button class="read-button" onclick="speakText('We have breakfast at 7 AM.')">استمع</button></li>
                    <li><span class="english-example">He has a cold.</span> <span class="arabic-example">هو مصاب بالزكام.</span><button class="read-button" onclick="speakText('He has a cold.')">استمع</button></li>
                </ul>
                <p><span class="example-type">كفعل مساعد (في المضارع التام):</span></p>
                <ul>
                    <li><span class="english-example">I have finished my work.</span> <span class="arabic-example">لقد أنهيت عملي.</span><button class="read-button" onclick="speakText('I have finished my work.')">استمع</button></li>
                    <li><span class="english-example">She has seen that movie.</span> <span class="arabic-example">هي شاهدت ذلك الفيلم.</span><button class="read-button" onclick="speakText('She has seen that movie.')">استمع</button></li>
                </ul>
                <p><span class="example-type">الماضي (Had):</span></p>
                <ul>
                    <li><span class="english-example">I had a good time.</span> <span class="arabic-example">قضيت وقتا ممتعا.</span><button class="read-button" onclick="speakText('I had a good time.')">استمع</button></li>
                    <li><span class="english-example">They had already left.</span> <span class="arabic-example">كانوا قد غادروا بالفعل.</span><button class="read-button" onclick="speakText('They had already left.')">استمع</button></li>
                </ul>
                <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">تمارين على Verb "To Have"</h3>
            `,
            exercises: [
                {q: "I ___ a new phone. (have/has)", a: "have"},
                {q: "He ___ two sisters. (have/has)", a: "has"},
                {q: "We ___ lunch at noon. (have/has)", a: "have"},
                {q: "She ___ a great idea. (have/has)", a: "has"},
                {q: "They ___ a big house. (have/has)", a: "have"},
                {q: "It ___ beautiful colors. (have/has)", a: "has"},
                {q: "You ___ to study. (have/has)", a: "have"},
                {q: "My dog ___ a long tail. (have/has)", a: "has"},
                {q: "I ___ already eaten. (have/has)", a: "have"},
                {q: "He ___ finished his work. (have/has)", a: "has"},
                {q: "We ___ a meeting tomorrow. (have/has)", a: "have"},
                {q: "She ___ a fever. (have/has)", a: "has"},
                {q: "They ___ traveled around the world. (have/has)", a: "have"},
                {q: "He ___ a headache yesterday. (had/has)", a: "had"},
                {q: "I ___ my breakfast already. (had/have)", a: "have"},
                {q: "We ___ a wonderful time last night. (had/have)", a: "had"},
                {q: "She ___ never seen a lion. (has/had)", a: "has"},
                {q: "By the time I arrived, they ___ left. (had/have)", a: "had"},
                {q: "You ___ a lot of patience. (have/has)", a: "have"},
                {q: "The cat ___ black fur. (has/have)", a: "has"}
            ]
        };

        // بيانات المضارع البسيط
        const presentSimpleData = {
            explanation: `
                <p><b>زمن المضارع البسيط (Present Simple)</b> يُستخدم للتعبير عن:</p>
                <ul>
                    <li>حقائق عامة أو علمية.</li>
                    <li>عادات أو روتين يومي.</li>
                    <li>جداول زمنية ثابتة (مثل مواعيد القطارات).</li>
                </ul>
                <p><span class="example-type">صيغة الفعل:</span></p>
                <ul>
                    <li><span class="english-example">I / You / We / They + الفعل الأساسي (بدون S)</span></li>
                    <li><span class="english-example">He / She / It + الفعل الأساسي + s / es</span></li>
                </ul>
                <p><span class="example-type">الكلمات الدالة (Keywords):</span></p>
                <ul>
                    <li><span class="english-example">Always</span> (دائماً)</li>
                    <li><span class="english-example">Usually</span> (عادةً)</li>
                    <li><span class="english-example">Often</span> (غالباً)</li>
                    <li><span class="english-example">Sometimes</span> (أحياناً)</li>
                    <li><span class="english-example">Never</span> (أبداً)</li>
                    <li><span class="english-example">Every day / week / month / year</span> (كل يوم / أسبوع / شهر / سنة)</li>
                    <li><span class="english-example">On Mondays / Tuesdays...</span> (في أيام الاثنين / الثلاثاء...)</li>
                </ul>
                <p><span class="example-type">أمثلة:</span></p>
                <ul>
                    <li><span class="english-example">I usually drink coffee in the morning.</span> <span class="arabic-example">أنا عادةً أشرب القهوة في الصباح.</span><button class="read-button" onclick="speakText('I usually drink coffee in the morning.')">استمع</button></li>
                    <li><span class="english-example">The sun rises in the east.</span> <span class="arabic-example">الشمس تشرق من الشرق.</span><button class="read-button" onclick="speakText('The sun rises in the east.')">استمع</button></li>
                    <li><span class="english-example">She plays tennis every Sunday.</span> <span class="arabic-example">هي تلعب التنس كل يوم أحد.</span><button class="read-button" onclick="speakText('She plays tennis every Sunday.')">استمع</button></li>
                </ul>
                <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">تمارين على المضارع البسيط</h3>
            `,
            exercises: [
                {q: "She often ___ to the gym. (go/goes)", a: "goes"},
                {q: "Birds ___ in the sky. (fly/flies)", a: "fly"},
                {q: "He never ___ meat. (eat/eats)", a: "eats"},
                {q: "We ___ our grandparents every month. (visit/visits)", a: "visit"},
                {q: "The train ___ at 8 AM. (leave/leaves)", a: "leaves"},
                {q: "I always ___ my teeth. (brush/brushes)", a: "brush"},
                {q: "Water ___ at 100 degrees Celsius. (boil/boils)", a: "boils"},
                {q: "They ___ English at school. (study/studies)", a: "study"},
                {q: "My sister ___ TV in the evening. (watch/watches)", a: "watches"},
                {q: "You usually ___ up early. (get/gets)", a: "get"},
                {q: "He ___ a lot. (read/reads)", a: "reads"},
                {q: "We ___ on vacation every summer. (go/goes)", a: "go"},
                {q: "She ___ tea in the morning. (drink/drinks)", a: "drinks"},
                {q: "I ___ in an office. (work/works)", a: "work"},
                {q: "The Earth ___ around the sun. (revolve/revolves)", a: "revolves"},
                {q: "They always ___ their homework. (do/does)", a: "do"},
                {q: "He ___ his car once a week. (wash/washes)", a: "washes"},
                {q: "We never ___ late for class. (are/is)", a: "are"},
                {q: "It often ___ in winter. (snow/snows)", a: "snows"},
                {q: "I ___ a student. (am/is)", a: "am"}
            ]
        };

        // بيانات الماضي البسيط
        const pastSimpleData = {
            explanation: `
                <p><b>زمن الماضي البسيط (Past Simple)</b> يُستخدم للتعبير عن أفعال أو أحداث بدأت وانتهت في وقت محدد في الماضي.</p>
                <p><span class="example-type">صيغة الفعل:</span></p>
                <ul>
                    <li>الأفعال المنتظمة: <span class="english-example">الفعل الأساسي + ed</span> (مثل: played, walked)</li>
                    <li>الأفعال الشاذة: تتغير كلياً (مثل: go -> went, eat -> ate)</li>
                </ul>
                <p><span class="example-type">الكلمات الدالة (Keywords):</span></p>
                <ul>
                    <li><span class="english-example">Yesterday</span> (أمس)</li>
                    <li><span class="english-example">Last night / week / month / year</span> (الليلة الماضية / الأسبوع الماضي / الشهر الماضي / السنة الماضية)</li>
                    <li><span class="english-example">Ago</span> (منذ - مثلاً: two days ago)</li>
                    <li><span class="english-example">In 2010 (أي سنة ماضية)</span></li>
                    <li><span class="english-example">When I was young</span> (عندما كنت صغيراً)</li>
                </ul>
                <p><span class="example-type">أمثلة:</span></p>
                <ul>
                    <li><span class="english-example">I visited my grandparents yesterday.</span> <span class="arabic-example">زرت أجدادي أمس.</span><button class="read-button" onclick="speakText('I visited my grandparents yesterday.')">استمع</button></li>
                    <li><span class="english-example">She went to Paris last summer.</span> <span class="arabic-example">هي ذهبت إلى باريس الصيف الماضي.</span><button class="read-button" onclick="speakText('She went to Paris last summer.')">استمع</button></li>
                    <li><span class="english-example">They ate dinner at 7 PM.</span> <span class="arabic-example">هم تناولوا العشاء الساعة 7 مساءً.</span><button class="read-button" onclick="speakText('They ate dinner at 7 PM.')">استمع</button></li>
                </ul>
                <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">تمارين على الماضي البسيط</h3>
            `,
            exercises: [
                {q: "She ___ to the cinema last night. (go/went)", a: "went"},
                {q: "I ___ my homework two hours ago. (finish/finished)", a: "finished"},
                {q: "They ___ football yesterday. (play/played)", a: "played"},
                {q: "He ___ a new car in 2020. (buy/bought)", a: "bought"},
                {q: "We ___ happy to see him. (were/was)", a: "were"},
                {q: "She ___ coffee for breakfast. (drink/drank)", a: "drank"},
                {q: "He ___ me a letter last week. (write/wrote)", a: "wrote"},
                {q: "I ___ up late this morning. (get/got)", a: "got"},
                {q: "They ___ a lot of noise. (make/made)", a: "made"},
                {q: "We ___ at home all day yesterday. (stay/stayed)", a: "stayed"},
                {q: "He ___ the news on TV. (watch/watched)", a: "watched"},
                {q: "I ___ my keys. (lose/lost)", a: "lost"},
                {q: "She ___ sad. (was/were)", a: "was"},
                {q: "They ___ to the party. (come/came)", a: "came"},
                {q: "We ___ a good time. (have/had)", a: "had"},
                {q: "He ___ a book. (read/read - same spelling for past)", a: "read"},
                {q: "I ___ in Cairo last year. (live/lived)", a: "lived"},
                {q: "She ___ him an email. (send/sent)", a: "sent"},
                {q: "They ___ the game. (win/won)", a: "won"},
                {q: "We ___ early. (leave/left)", a: "left"}
            ]
        };

        // بيانات المضارع المستمر
        const presentContinuousData = {
            explanation: `
                <p><b>زمن المضارع المستمر (Present Continuous)</b> يُستخدم للتعبير عن:</p>
                <ul>
                    <li>أحداث تحدث الآن في لحظة الكلام.</li>
                    <li>أفعال مؤقتة أو خطط مستقبلية مؤكدة (غالباً مع التعبير عن الزمان).</li>
                </ul>
                <p><span class="example-type">صيغة الفعل:</span></p>
                <ul>
                    <li><span class="english-example">Subject + am / is / are + الفعل الأساسي + ing</span></li>
                </ul>
                <p><span class="example-type">الكلمات الدالة (Keywords):</span></p>
                <ul>
                    <li><span class="english-example">Now</span> (الآن)</li>
                    <li><span class="english-example">Right now</span> (في هذه اللحظة بالذات)</li>
                    <li><span class="english-example">At the moment</span> (في الوقت الحالي)</li>
                    <li><span class="english-example">Look! / Listen!</span> (انظر! / استمع! - للدلالة على حدث يحدث الآن)</li>
                    <li><span class="english-example">Today / This week / This month</span> (اليوم / هذا الأسبوع / هذا الشهر)</li>
                </ul>
                <p><span class="example-type">أمثلة:</span></p>
                <ul>
                    <li><span class="english-example">I am studying English now.</span> <span class="arabic-example">أنا أدرس الإنجليزية الآن.</span><button class="read-button" onclick="speakText('I am studying English now.')">استمع</button></li>
                    <li><span class="english-example">She is watching TV at the moment.</span> <span class="arabic-example">هي تشاهد التلفاز في الوقت الحالي.</span><button class="read-button" onclick="speakText('She is watching TV at the moment.')">استمع</button></li>
                    <li><span class="english-example">They are playing football.</span> <span class="arabic-example">هم يلعبون كرة القدم.</span><button class="read-button" onclick="speakText('They are playing football.')">استمع</button></li>
                </ul>
                <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">تمارين على المضارع المستمر</h3>
            `,
            exercises: [
                {q: "He ___ a book now. (read/is reading)", a: "is reading"},
                {q: "They ___ football at the moment. (play/are playing)", a: "are playing"},
                {q: "I ___ to music. (listen/am listening)", a: "am listening"},
                {q: "She ___ dinner right now. (cook/is cooking)", a: "is cooking"},
                {q: "We ___ for the bus. (wait/are waiting)", a: "are waiting"},
                {q: "Look! It ___ outside. (rain/is raining)", a: "is raining"},
                {q: "What ___ you ___? (do/are doing)", a: "are doing"},
                {q: "The birds ___ . (sing/are singing)", a: "are singing"},
                {q: "My sister ___ her homework. (do/is doing)", a: "is doing"},
                {q: "They ___ to London next week. (travel/are traveling)", a: "are traveling"},
                {q: "He ___ a new project this month. (work/is working)", a: "is working"},
                {q: "We ___ at a restaurant tonight. (eat/are eating)", a: "are eating"},
                {q: "She ___ about her future. (think/is thinking)", a: "is thinking"},
                {q: "I ___ coffee. (drink/am drinking)", a: "am drinking"},
                {q: "The children ___ in the garden. (play/are playing)", a: "are playing"},
                {q: "Listen! Someone ___ at the door. (knock/is knocking)", a: "is knocking"},
                {q: "They ___ their new house. (build/are building)", a: "are building"},
                {q: "I ___ a letter to my friend. (write/am writing)", a: "am writing"},
                {q: "He ___ on the phone. (talk/is talking)", a: "is talking"},
                {q: "The sun ___ . (shine/is shining)", a: "is shining"}
            ]
        };

        // بيانات الماضي التام
        const pastPerfectData = {
            explanation: `
                <p><b>زمن الماضي التام (Past Perfect)</b> يُستخدم للتعبير عن حدث وقع وانتهى في الماضي **قبل** حدث آخر وقع في الماضي أيضاً. إنه يوضح تسلسل الأحداث في الماضي.</p>
                <p><span class="example-type">صيغة الفعل:</span></p>
                <ul>
                    <li><span class="english-example">Subject + had + التصريف الثالث للفعل (Past Participle)</span></li>
                </ul>
                <p><span class="example-type">الكلمات الدالة (Keywords):</span></p>
                <ul>
                    <li><span class="english-example">By the time</span> (بحلول الوقت)</li>
                    <li><span class="english-example">Before</span> (قبل)</li>
                    <li><span class="english-example">After</span> (بعد)</li>
                    <li><span class="english-example">Already</span> (بالفعل)</li>
                    <li><span class="english-example">Never</span> (أبداً)</li>
                    <li><span class="english-example">Once</span> (مرة واحدة)</li>
                </ul>
                <p><span class="example-type">أمثلة:</span></p>
                <ul>
                    <li><span class="english-example">By the time I arrived, she had already left.</span> <span class="arabic-example">بحلول الوقت الذي وصلت فيه، كانت قد غادرت بالفعل.</span><button class="read-button" onclick="speakText('By the time I arrived, she had already left.')">استمع</button></li>
                    <li><span class="english-example">He had finished his work before he went home.</span> <span class="arabic-example">كان قد أنهى عمله قبل أن يذهب إلى المنزل.</span><button class="read-button" onclick="speakText('He had finished his work before he went home.')">استمع</button></li>
                    <li><span class="english-example">I had never seen such a beautiful place until I visited Egypt.</span> <span class="arabic-example">لم أرَ مكانًا بهذا الجمال من قبل حتى زرت مصر.</span><button class="read-button" onclick="speakText('I had never seen such a beautiful place until I visited Egypt.')">استمع</button></li>
                </ul>
                <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">تمارين على الماضي التام</h3>
            `,
            exercises: [
                {q: "By the time I arrived, the train ___ (leave).", a: "had left"},
                {q: "She ___ (finish) her homework before she watched TV.", a: "had finished"},
                {q: "He ___ (never see) a lion before his trip to Africa.", a: "had never seen"},
                {q: "They ___ (eat) all the food before we got there.", a: "had eaten"},
                {q: "After he ___ (pass) his exam, he celebrated.", a: "had passed"},
                {q: "I ___ (already buy) the tickets when she suggested going.", a: "had already bought"},
                {q: "She couldn't enter because she ___ (forget) her key.", a: "had forgotten"},
                {q: "By 2010, he ___ (work) in the company for 10 years.", a: "had worked"},
                {q: "We ___ (not meet) before that day.", a: "had not met"},
                {q: "He realized he ___ (make) a mistake.", a: "had made"},
                {q: "They ___ (live) in Cairo for five years before they moved to Dubai.", a: "had lived"},
                {q: "She explained that she ___ (not understand) the lesson.", a: "had not understood"},
                {q: "The movie ___ (already start) when we arrived.", a: "had already started"},
                {q: "He asked if I ___ (see) his phone.", a: "had seen"},
                {q: "I ___ (lose) my wallet before I noticed.", a: "had lost"},
                {q: "By the time he came, I ___ (finish) cooking.", a: "had finished"},
                {q: "She was tired because she ___ (study) all night.", a: "had studied"},
                {q: "They ___ (never visit) that museum before.", a: "had never visited"},
                {q: "He told me he ___ (clean) the house.", a: "had cleaned"},
                {q: "When I called her, she ___ (already sleep).", a: "had already slept"}
            ]
        };


        // ربط المحتوى بالأقسام
        contentSections[0].content = buildVowelsConsonantsSection();
        contentSections[1].content = `<div class="section-content">${verbToBeData.explanation} ${generateExercisesHtml(verbToBeData.exercises)}</div>`;
        contentSections[2].content = `<div class="section-content">${heItIsData.explanation} ${generateExercisesHtml(heItIsData.exercises)}</div>`;
        contentSections[3].content = `<div class="section-content">${verbToDoData.explanation} ${generateExercisesHtml(verbToDoData.exercises)}</div>`;
        contentSections[4].content = `<div class="section-content">${verbToHaveData.explanation} ${generateExercisesHtml(verbToHaveData.exercises)}</div>`;
        contentSections[5].content = `<div class="section-content">${presentSimpleData.explanation} ${generateExercisesHtml(presentSimpleData.exercises)}</div>`;
        contentSections[6].content = `<div class="section-content">${pastSimpleData.explanation} ${generateExercisesHtml(pastSimpleData.exercises)}</div>`;
        contentSections[7].content = `<div class="section-content">${presentContinuousData.explanation} ${generateExercisesHtml(presentContinuousData.exercises)}</div>`;
        contentSections[8].content = `<div class="section-content">${pastPerfectData.explanation} ${generateExercisesHtml(pastPerfectData.exercises)}</div>`;


        // دالة لتوليد HTML للتمارين
        function generateExercisesHtml(exercises) {
            let html = ``;
            exercises.forEach((ex, index) => {
                html += `
                    <div class="exercise-item">
                        <p class="exercise-question">${ex.q}</p>
                        <button class="show-answer-button" onclick="toggleAnswer(this, 'answer${ex.q.replace(/[^a-zA-Z0-9]/g, '')}${index}')">أظهر الإجابة</button>
                        <p id="answer${ex.q.replace(/[^a-zA-Z0-9]/g, '')}${index}" class="exercise-answer">${ex.a}</p>
                    </div>
                `;
            });
            return html;
        }

        // دالة لإظهار/إخفاء الإجابة
        window.toggleAnswer = function(button, answerId) {
            const answerElement = document.getElementById(answerId);
            if (answerElement.style.display === 'none' || answerElement.style.display === '') {
                answerElement.style.display = 'block';
                button.textContent = 'إخفاء الإجابة';
                button.style.backgroundColor = '#dc3545'; // لون أحمر للإخفاء
            } else {
                answerElement.style.display = 'none';
                button.textContent = 'أظهر الإجابة';
                button.style.backgroundColor = '#28a745'; // لون أخضر للإظهار
            }
        };

        // دالة لعرض المحتوى للصفحة الحالية
        function displayContentForPage(pageNumber) {
            wordsContainer.innerHTML = ''; // تفريغ المحتوى الحالي

            if (pageNumber > 0 && pageNumber <= contentSections.length) {
                const section = contentSections[pageNumber - 1];
                const sectionDiv = document.createElement('div');
                sectionDiv.className = 'section-block';
                
                const titleElement = document.createElement('h2');
                titleElement.className = 'section-title';
                titleElement.textContent = section.title;
                sectionDiv.appendChild(titleElement);

                sectionDiv.innerHTML += section.content;
                wordsContainer.appendChild(sectionDiv);
            } else {
                wordsContainer.innerHTML = "<p style='font-size: 1.5em; color: #ADD8E6;'>لا توجد المزيد من الدروس هنا.</p>";
            }

            updatePaginationControls();
        }

        // تحديث أزرار التنقل ومعلومات الصفحة
        function updatePaginationControls() {
            pageInfoSpan.textContent = `الصفحة ${currentPage} من ${totalPages}`;
            prevPageBtn.disabled = (currentPage === 1);
            nextPageBtn.disabled = (currentPage === totalPages);
        }

        // وظيفة التحضير الأولية
        function initializePage() {
            totalPages = contentSections.length; // كل قسم هو صفحة
            displayContentForPage(currentPage);
            
            noteElement.style.setProperty('--note-delay', `${startDelay + 0.5}s`);
            audioControl.style.setProperty('--button-delay', `${startDelay + 0.9}s`);
        }

        // إضافة مستمعي الأحداث لأزرار التنقل
        prevPageBtn.addEventListener('click', () => {
            if (currentPage > 1) {
                currentPage--;
                displayContentForPage(currentPage);
                window.scrollTo(0, 0);
            }
        });

        nextPageBtn.addEventListener('click', () => {
            if (currentPage < totalPages) {
                currentPage++;
                displayContentForPage(currentPage);
                window.scrollTo(0, 0);
            }
        });

        // تشغيل/إيقاف الصوت الخلفي
        audioControl.addEventListener('click', () => {
            if (isPlaying) {
                audio.pause();
                audioControl.textContent = 'تشغيل الموسيقى';
            } else {
                audio.play().catch(e => {
                    console.error("Audio play failed:", e);
                    audioControl.textContent = 'خطأ في تشغيل الموسيقى';
                });
                audioControl.textContent = 'إيقاف الموسيقى';
            }
            isPlaying = !isPlaying;
        });

        // تشغيل الإعدادات الأولية والموسيقى عند تحميل الصفحة
        window.addEventListener('load', () => {
             initializePage();
             audio.play().then(() => {
                isPlaying = true;
                audioControl.textContent = 'إيقاف الموسيقى';
            }).catch(e => {
                console.log("Audio autoplay prevented. Please use the button.");
                audioControl.textContent = 'تشغيل الموسيقى';
            });

            if (synth.onvoiceschanged !== undefined) {
                synth.onvoiceschanged = () => {};
            }
        });
    </script>
</body>
</html>
