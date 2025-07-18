<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>يوم جمعة سعيد ودروس إنجليزية</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* CSS الألوان والتأثيرات */
        body {
            font-family: 'Cairo', sans-serif; /* استخدام خط عربي مميز وواضح */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #FFD700, #FF6347); /* تدرج لوني دافئ */
            color: #FFFFFF;
            overflow: hidden;
            position: relative; /* لتحديد موقع الفقاعات */
        }

        .container {
            text-align: center;
            background-color: rgba(0, 0, 0, 0.6); /* خلفية شبه شفافة أغمق قليلاً */
            padding: 30px 40px; /* زيادة البادينج الأفقي */
            border-radius: 20px; /* حواف أكثر استدارة */
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.4); /* ظل أوضح */
            transform: scale(0.9);
            animation: appearScale 1.5s ease-out forwards;
            margin-bottom: 25px; /* مسافة أكبر */
            max-width: 95%; /* أقصى عرض للحاوية */
            max-height: 85vh;
            overflow-y: auto; /* سكرول إذا كانت الكلمات كثيرة */
            scrollbar-width: thin;
            scrollbar-color: #FFFF00 rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(5px); /* تأثير ضبابي على الخلفية */
        }

        /* تخصيص السكرولبار */
        .container::-webkit-scrollbar { width: 8px; }
        .container::-webkit-scrollbar-track { background: rgba(255, 255, 255, 0.15); border-radius: 10px; }
        .container::-webkit-scrollbar-thumb { background: #FFFF00; border-radius: 10px; }

        @keyframes appearScale {
            from { transform: scale(0); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }

        h1 {
            font-size: 3.2em; /* حجم أكبر للعنوان */
            margin-bottom: 25px;
            color: #FFFF00;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.6); /* ظل أوضح */
            animation: bounceIn 1s ease-out;
            letter-spacing: 2px; /* مسافة بين الحروف */
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

        .word-item {
            margin: 15px 0; /* مسافة أكبر بين العناصر */
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInSlideUp 0.8s forwards;
            break-inside: avoid-column;
            display: flex;
            flex-direction: column; /* جعل الكلمة والمعنى في سطرين */
            align-items: center;
            padding: 10px;
            border-radius: 10px;
            transition: background-color 0.3s ease, transform 0.3s ease; /* تأثير الانتقال */
            cursor: pointer; /* لإظهار أن العنصر قابل للتفاعل */
        }

        .word-item:hover {
            background-color: rgba(255, 255, 255, 0.1); /* خلفية عند التمرير */
            transform: translateY(-5px) scale(1.02); /* تأثير رفع بسيط */
        }

        .english-word {
            font-size: 1.6em; /* حجم خط الكلمة الإنجليزية */
            color: #98FB98;
            font-weight: bold;
            margin-bottom: 5px; /* مسافة تحت الكلمة الإنجليزية */
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
        }

        .arabic-meaning {
            font-size: 1.1em; /* حجم خط المعنى العربي */
            color: #ADD8E6;
            margin-bottom: 10px; /* مسافة تحت المعنى العربي */
        }

        .read-buttons-group {
            display: flex;
            gap: 10px; /* مسافة بين الأزرار (لو احتجنا أكتر من زر مستقبلا) */
        }

        .read-button {
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 8px; /* حواف أكثر استدارة */
            padding: 8px 15px; /* بادينج أكبر للزر */
            cursor: pointer;
            font-size: 0.9em;
            transition: background-color 0.3s ease, transform 0.2s ease; /* تأثير الانتقال */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* ظل للزر */
        }

        .read-button:hover {
            background-color: #0056b3;
            transform: translateY(-2px); /* رفع بسيط للزر عند التمرير */
        }
        .read-button:active {
            transform: translateY(0); /* تأثير ضغط للزر */
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        /* تأخير أنيميشن ظهور الكلمات - سيتم توليد تأخيرات ديناميكياً باستخدام JS */
        @keyframes fadeInSlideUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .note {
            margin-top: 30px;
            font-size: 1.3em; /* حجم أكبر للملاحظة */
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

        /* تأثير فقاعات خفيفة في الخلفية */
        .bubble {
            position: absolute;
            bottom: -100px;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            animation: bubbleUp 15s infinite ease-in;
            z-index: -1; /* لجعل الفقاعات خلف المحتوى الرئيسي */
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

        /* Styles for the new navigation buttons */
        .nav-buttons {
            margin-bottom: 20px;
            display: flex;
            flex-wrap: wrap; /* Allow buttons to wrap */
            gap: 15px; /* Space between buttons */
            justify-content: center;
        }

        .nav-button {
            background-color: #6A5ACD; /* MediumSlateBlue */
            color: white;
            border: none;
            border-radius: 12px; /* More rounded corners */
            padding: 12px 25px;
            cursor: pointer;
            font-size: 1.1em;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
            font-family: 'Cairo', sans-serif;
            font-weight: bold;
        }

        .nav-button:hover {
            background-color: #483D8B; /* DarkSlateBlue */
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.4);
        }

        .nav-button:active {
            transform: translateY(0);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        #audioControl {
            margin-top: 25px; /* مسافة أكبر */
            padding: 12px 25px; /* بادينج أكبر للزر */
            font-size: 1.3em; /* حجم أكبر للخط */
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 10px; /* حواف أكثر استدارة */
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
            opacity: 0;
            animation: fadeIn 1s forwards;
            animation-delay: var(--button-delay);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3); /* ظل أوضح */
            font-family: 'Cairo', sans-serif;
        }

        #audioControl:hover {
            background-color: #45a049;
            transform: translateY(-3px) scale(1.03); /* رفع وتكبير بسيط */
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4);
        }
        #audioControl:active {
            transform: translateY(0);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }

        /* استخدام خاصية الأعمدة للكلمات والمعاني معًا */
        .word-list-container {
            columns: 2; /* تقسيم الكلمات والمعاني لعمودين */
            column-gap: 40px; /* مسافة أكبر بين الأعمدة */
        }

        /* New styles for tense explanations */
        .tense-explanation, .pronunciation-rules {
            text-align: right; /* Right-align text for Arabic */
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            margin-top: 20px;
            opacity: 0;
            animation: fadeIn 1s forwards;
            animation-delay: 0.2s; /* Slight delay for the whole block */
        }

        .tense-explanation h2, .pronunciation-rules h2 {
            color: #FFFF00;
            font-size: 2em;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.4);
        }

        .tense-explanation h3, .pronunciation-rules h3 {
            color: #98FB98; /* PaleGreen */
            font-size: 1.5em;
            margin-top: 20px;
            margin-bottom: 10px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
            border-bottom: 1px solid rgba(255, 255, 255, 0.3);
            padding-bottom: 5px;
        }

        .tense-explanation p,
        .tense-explanation ul,
        .pronunciation-rules p,
        .pronunciation-rules ul {
            color: #E0FFFF; /* Light Cyan */
            font-size: 1.1em;
            line-height: 1.6;
            margin-bottom: 10px;
            text-align: right; /* Ensure text alignment for all blocks */
        }

        .tense-explanation ul, .pronunciation-rules ul {
            list-style-type: disc; /* Use discs for general lists */
            padding-right: 25px; /* Indent for list items */
            margin-right: 0; /* Reset default margin */
            text-align: right; /* Align list content */
            direction: rtl; /* Ensure RTL for list item numbers/bullets */
        }
        
        .tense-explanation ul li, .pronunciation-rules ul li {
            margin-bottom: 8px;
        }

        .tense-explanation strong, .pronunciation-rules strong {
            color: #FFD700; /* Gold for strong emphasis */
            font-weight: bold;
        }
        
        /* Specific styling for example lists */
        .tense-explanation .examples-list li, .pronunciation-rules .examples-list li {
            background-color: rgba(0, 0, 0, 0.2);
            padding: 8px 15px;
            border-radius: 8px;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: space-between; /* To push button to the left */
            flex-wrap: wrap; /* Allow wrapping on small screens */
            gap: 10px;
            border-right: 5px solid #98FB98; /* Highlight examples */
        }

        .tense-explanation .examples-list li .english-sentence,
        .pronunciation-rules .examples-list li .english-sentence {
            flex-grow: 1; /* Allow sentence to take available space */
            text-align: right;
        }

        .tense-explanation .read-button.example-button,
        .pronunciation-rules .read-button.example-button {
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 6px;
            padding: 6px 12px;
            cursor: pointer;
            font-size: 0.85em;
            transition: background-color 0.3s ease, transform 0.2s ease;
            white-space: nowrap; /* Prevent button text from wrapping */
        }

        .tense-explanation .read-button.example-button:hover,
        .pronunciation-rules .read-button.example-button:hover {
            background-color: #0056b3;
            transform: translateY(-1px);
        }

        /* Styles for the tense list buttons */
        .tense-list, .pronunciation-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-top: 20px;
            align-items: center;
        }

        .tense-list .tense-selection-button,
        .pronunciation-list .pronunciation-selection-button {
            background-color: #ADD8E6; /* Light Blue */
            color: #2F4F4F; /* Dark Slate Grey */
            border: none;
            border-radius: 10px;
            padding: 15px 30px;
            cursor: pointer;
            font-size: 1.4em;
            font-weight: bold;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            min-width: 250px;
        }

        .tense-list .tense-selection-button:hover,
        .pronunciation-list .pronunciation-selection-button:hover {
            background-color: #87CEEB; /* Sky Blue */
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }

        .tense-list .tense-selection-button:active,
        .pronunciation-list .pronunciation-selection-button:active {
            transform: translateY(0);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
        }


        /* تنسيق للاسكرولبار على المتصفحات التي تدعمها */
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
        <h1 id="mainTitle">مرحباً في عالم الكلمات الإنجليزية!</h1>

        <div class="nav-buttons">
            <button class="nav-button" onclick="displayCategory('friday')">كلمات الجمعة</button>
            <button class="nav-button" onclick="displayCategory('nouns')">الأسماء</button>
            <button class="nav-button" onclick="displayCategory('adjectives')">الصفات</button>
            <button class="nav-button" onclick="displayCategory('verbs')">الأفعال الأساسية</button>
            <button class="nav-button" onclick="displayCategory('pronouns')">الضمائر</button>
            <button class="nav-button" onclick="displayCategory('colors')">الألوان</button>
            <button class="nav-button" onclick="showTenseList()">الأزمنة</button>
            <button class="nav-button" onclick="showPronunciationRules()">قواعد النطق</button>
        </div>

        <div class="word-list-container" id="wordListContainer">
            </div>
        <p class="note" id="noteElement">ابدأ بتصفح الكلمات ومعانيها، واستمع للنطق الصحيح!</p>
    </div>

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

    <button id="audioControl">تشغيل/إيقاف الموسيقى</button>

    <script>
        // --- Data for different word categories and tenses ---

        const wordCategories = {
            friday: [
                { en: "Relax", ar: "استرخاء" },
                { en: "Recharge", ar: "إعادة شحن الطاقة" },
                { en: "Unwind", ar: "استرخِ/تخلّص من التوتر" },
                { en: "Breathe", ar: "تنفس" },
                { en: "Chill", ar: "هدوء/استجمام" },
                { en: "Explore", ar: "استكشف" },
                { en: "Connect", ar: "تواصل" },
                { en: "Reflect", ar: "تأمل" },
                { en: "Weekend Vibes", ar: "أجواء عطلة نهاية الأسبوع" },
                { en: "Enjoy Your Time", ar: "استمتع بوقتك" },
                { en: "Serenity", ar: "سكينة/صفاء" },
                { en: "Peace", ar: "سلام" },
                { en: "Tranquility", ar: "طمأنينة/هدوء" },
                { en: "Freedom", ar: "حرية" },
                { en: "Joy", ar: "فرحة/بهجة" },
                { en: "Bliss", ar: "نعيم/سعادة غامرة" },
                { en: "Gratitude", ar: "امتنان" },
                { en: "Leisure", ar: "وقت فراغ/ترويح" },
                { en: "Adventure", ar: "مغامرة" },
                { en: "Rest", ar: "راحة" },
                { en: "Delight", ar: "متعة/بهجة" },
                { en: "Calm", ar: "هدوء/سكون" },
                { en: "Harmony", ar: "انسجام" },
                { en: "Happiness", ar: "سعادة" },
                { en: "Gather", ar: "اجتمع" },
                { en: "Create", ar: "ابتكر" },
                { en: "Dream", ar: "احلم" },
                { en: "Inspire", ar: "إلهام" },
                { en: "Smile", ar: "ابتسم" },
                { en: "Savor", ar: "تذوق/استمتع بالكامل" },
                { en: "Cherish", ar: "اعتز بـ" },
                { en: "Unplug", ar: "افصل عن التكنولوجيا" },
                { en: "Discover", ar: "اكتشف" },
                { en: "Renew", ar: "جدّد" },
                { en: "Embrace", ar: "احتضن/تقبّل" },
                { en: "Prosperity", ar: "رخاء/ازدهار" },
                { en: "Balance", ar: "توازن" },
                { en: "Positivity", ar: "إيجابية" },
                { en: "Goodness", ar: "خير/صلاح" },
                { en: "Hope", ar: "أمل" },
                { en: "Love", ar: "حب" },
                { en: "Kindness", ar: "لطف" },
                { en: "Patience", ar: "صبر" },
                { en: "Growth", ar: "نمو" },
                { en: "Success", ar: "نجاح" },
                { en: "Achieve", "ar": "حقق" },
                { en: "Thrive", ar: "ازدهر" },
                { en: "Shine", ar: "تألّق" },
                { en: "Sparkle", ar: "تألق/بريق" },
                { en: "Flourish", ar: "ازدهر/تنمو" },
                { en: "Radiate", ar: "أشرق/اشعّ" },
                { en: "Connect with nature", ar: "تواصل مع الطبيعة" },
                { en: "Family time", ar: "وقت العائلة" },
                { en: "Self-care", ar: "العناية بالذات" },
                { en: "Mindfulness", ar: "الوعي التام" },
                { en: "Gratitude practice", ar: "ممارسة الامتنان" },
                { en: "Good food", ar: "طعام جيد" },
                { en: "Comfort", ar: "راحة" },
                { en: "Happiness is here", ar: "السعادة هنا" }
            ],
            nouns: [
                { en: "House", ar: "منزل" },
                { en: "Cat", ar: "قطة" },
                { en: "Tree", ar: "شجرة" },
                { en: "Book", ar: "كتاب" },
                { en: "City", ar: "مدينة" },
                { en: "Friend", ar: "صديق" },
                { en: "Table", ar: "طاولة" },
                { en: "Car", ar: "سيارة" },
                { en: "Phone", ar: "هاتف" },
                { en: "Flower", ar: "زهرة" },
                { en: "Water", ar: "ماء" },
                { en: "Sun", ar: "شمس" },
                { en: "Moon", ar: "قمر" },
                { en: "Star", ar: "نجمة" },
                { en: "Sky", ar: "سماء" },
                { en: "Food", ar: "طعام" },
                { en: "Drink", ar: "شراب" },
                { en: "Chair", ar: "كرسي" },
                { en: "Door", ar: "باب" },
                { en: "Window", ar: "نافذة" },
                { en: "Child", ar: "طفل" },
                { en: "Man", ar: "رجل" },
                { en: "Woman", ar: "امرأة" },
                { en: "Dog", ar: "كلب" },
                { en: "Bird", ar: "طائر" },
                { en: "School", ar: "مدرسة" },
                { en: "Teacher", ar: "معلم" },
                { en: "Student", ar: "طالب" },
                { en: "Money", ar: "مال" },
                { en: "Time", ar: "وقت" }
            ],
            adjectives: [
                { en: "Happy", ar: "سعيد" },
                { en: "Sad", ar: "حزين" },
                { en: "Big", ar: "كبير" },
                { en: "Small", ar: "صغير" },
                { en: "Good", ar: "جيد" },
                { en: "Bad", ar: "سيء" },
                { en: "Red", ar: "أحمر" },
                { en: "Blue", ar: "أزرق" },
                { en: "Green", ar: "أخضر" },
                { en: "Yellow", ar: "أصفر" },
                { en: "Fast", ar: "سريع" },
                { en: "Slow", ar: "بطيء" },
                { en: "Hot", ar: "حار" },
                { en: "Cold", ar: "بارد" },
                { en: "New", ar: "جديد" },
                { en: "Old", ar: "قديم" },
                { en: "Young", ar: "شاب" },
                { en: "Beautiful", ar: "جميل" },
                { en: "Ugly", ar: "قبيح" },
                { en: "Clean", ar: "نظيف" },
                { en: "Dirty", ar: "متسخ" },
                { en: "Easy", ar: "سهل" },
                { en: "Difficult", ar: "صعب" },
                { en: "Strong", ar: "قوي" },
                { en: "Weak", ar: "ضعيف" }
            ],
            verbs: [
                { en: "To Be", ar: "يكون" },
                { en: "To Have", ar: "يملك" },
                { en: "To Do", ar: "يفعل" },
                { en: "To Say", ar: "يقول" },
                { en: "To Go", ar: "يذهب" },
                { en: "To Get", ar: "يحصل على" },
                { en: "To Make", ar: "يصنع" },
                { en: "To Know", ar: "يعرف" },
                { en: "To Think", ar: "يعتقد" },
                { en: "To Take", ar: "يأخذ" },
                { en: "To See", ar: "يرى" },
                { en: "To Come", ar: "يأتي" },
                { en: "To Want", ar: "يريد" },
                { en: "To Look", ar: "ينظر" },
                { en: "To Give", ar: "يعطي" },
                { en: "To Use", ar: "يستخدم" },
                { en: "To Find", ar: "يجد" },
                { en: "To Tell", ar: "يخبر" },
                { en: "To Ask", ar: "يسأل" },
                { en: "To Work", ar: "يعمل" },
                { en: "To Seem", ar: "يبدو" },
                { en: "To Feel", ar: "يشعر" },
                { en: "To Try", ar: "يحاول" },
                { en: "To Leave", ar: "يغادر" },
                { en: "To Call", ar: "يتصل" }
            ],
            pronouns: [
                { en: "I", ar: "أنا" },
                { en: "You", ar: "أنت/أنتم" },
                { en: "He", ar: "هو" },
                { en: "She", ar: "هي" },
                { en: "It", ar: "هو/هي (لغير العاقل)" },
                { en: "We", ar: "نحن" },
                { en: "They", ar: "هم/هن" },
                { en: "Me", ar: "لي/إياي" },
                { en: "Him", ar: "له/إياه" },
                { en: "Her", ar: "لها/إياها" },
                { en: "Us", ar: "لنا/إيانا" },
                { en: "Them", ar: "لهم/إياهم" },
                { en: "My", ar: "خاصتي" },
                { en: "Your", ar: "خاصتك" },
                { en: "His", ar: "خاصته" },
                { en: "Her", ar: "خاصتها" },
                { en: "Its", ar: "خاصته/خاصتها (لغير العاقل)" },
                { en: "Our", ar: "خاصتنا" },
                { en: "Their", ar: "خاصتهم" },
                { en: "Mine", ar: "ملكي" },
                { en: "Yours", ar: "ملكك" },
                { en: "His", ar: "ملكه" },
                { en: "Hers", ar: "ملكها" },
                { en: "Ours", ar: "ملكنا" },
                { en: "Theirs", ar: "ملكهم" }
            ],
            colors: [
                { en: "Red", ar: "أحمر" },
                { en: "Blue", ar: "أزرق" },
                { en: "Green", ar: "أخضر" },
                { en: "Yellow", ar: "أصفر" },
                { en: "Black", ar: "أسود" },
                { en: "White", ar: "أبيض" },
                { en: "Orange", ar: "برتقالي" },
                { en: "Purple", ar: "بنفسجي" },
                { en: "Pink", ar: "وردي" },
                { en: "Brown", ar: "بني" },
                { en: "Gray", ar: "رمادي" },
                { en: "Gold", ar: "ذهبي" },
                { en: "Silver", ar: "فضي" },
                { en: "Turquoise", ar: "فيروزي" },
                { en: "Navy Blue", ar: "أزرق داكن" },
                { en: "Light Green", ar: "أخضر فاتح" },
                { en: "Dark Red", ar: "أحمر داكن" },
                { en: "Beige", ar: "بيج" },
                { en: "Cream", ar: "كريمي" },
                { en: "Magenta", ar: "أرجواني" }
            ],
            tenses: {
                presentSimple: {
                    title: "زمن المضارع البسيط",
                    arabicTitle: "The Present Simple Tense",
                    explanation: "يستخدم المضارع البسيط للتعبير عن العادات، الحقائق العامة، الجداول الزمنية، والأحداث المتكررة. يتميز هذا الزمن ببساطته في التكوين.",
                    form: {
                        positive: "الفاعل + الفعل (أو الفعل + s/es مع He/She/It)",
                        negative: "الفاعل + do/does not + الفعل",
                        question: "Do/Does + الفاعل + الفعل؟"
                    },
                    keywords: [
                        "Always (دائماً)",
                        "Usually (عادةً)",
                        "Often (غالباً)",
                        "Sometimes (أحياناً)",
                        "Never (أبداً)",
                        "Every day/week/year (كل يوم/أسبوع/سنة)",
                        "On Mondays/Tuesdays (أيام الاثنين/الثلاثاء)"
                    ],
                    examples: [
                        "I **drink** coffee every morning. (أنا أشرب القهوة كل صباح.)",
                        "She **works** in a hospital. (هي تعمل في مستشفى.)",
                        "The sun **rises** in the east. (الشمس تشرق من الشرق.)",
                        "Do you **play** football? (هل تلعب كرة القدم؟)",
                        "He **does not like** fast food. (هو لا يحب الطعام السريع.)",
                        "They **go** to school by bus. (هم يذهبون إلى المدرسة بالحافلة.)",
                        "My sister **studies** English. (أختي تدرس الإنجليزية.)",
                        "We **live** in a big city. (نحن نعيش في مدينة كبيرة.)",
                        "Does he **speak** French? (هل هو يتحدث الفرنسية؟)",
                        "Birds **fly**. (الطيور تطير.)"
                    ]
                },
                pastSimple: {
                    title: "زمن الماضي البسيط",
                    arabicTitle: "The Past Simple Tense",
                    explanation: "يستخدم الماضي البسيط للتعبير عن أحداث وقعت وانتهت في وقت محدد في الماضي. يمكن أن تكون المدة قصيرة أو طويلة، المهم أنها مكتملة.",
                    form: {
                        positive: "الفاعل + الفعل في التصريف الثاني (ed-verb أو شكل غير منتظم)",
                        negative: "الفاعل + did not + الفعل (مصدر)",
                        question: "Did + الفاعل + الفعل (مصدر)؟"
                    },
                    keywords: [
                        "Yesterday (أمس)",
                        "Last night/week/month/year (الليلة/الأسبوع/الشهر/السنة الماضية)",
                        "Ago (منذ)",
                        "In 2005 (في عام 2005 - أي تاريخ ماضٍ)",
                        "When I was a child (عندما كنت طفلاً)"
                    ],
                    examples: [
                        "I **visited** Paris last year. (زرت باريس العام الماضي.)",
                        "They **ate** dinner at 7 PM. (تناولوا العشاء في الساعة 7 مساءً.)",
                        "She **didn't go** to the party. (هي لم تذهب إلى الحفلة.)",
                        "Did you **see** him yesterday? (هل رأيته أمس؟)",
                        "He **was** a student in that school. (كان طالباً في تلك المدرسة.)",
                        "We **watched** a great movie. (شاهدنا فيلماً رائعاً.)",
                        "My parents **bought** a new car. (والداي اشتريا سيارة جديدة.)",
                        "The meeting **started** late. (بدأ الاجتماع متأخراً.)",
                        "She **wrote** a letter to her friend. (كتبت رسالة لصديقتها.)",
                        "I **slept** well last night. (نمت جيداً الليلة الماضية.)"
                    ]
                },
                presentContinuous: {
                    title: "زمن المضارع المستمر",
                    arabicTitle: "The Present Continuous Tense",
                    explanation: "يستخدم المضارع المستمر للتعبير عن أحداث تحدث الآن في لحظة الكلام، أو أحداث مؤقتة، أو خطط مستقبلية مؤكدة.",
                    form: {
                        positive: "الفاعل + am/is/are + الفعل + ing",
                        negative: "الفاعل + am/is/are not + الفعل + ing",
                        question: "Am/Is/Are + الفاعل + الفعل + ing؟"
                    },
                    keywords: [
                        "Now (الآن)",
                        "Right now (في هذه اللحظة)",
                        "At the moment (في هذه اللحظة)",
                        "Currently (حالياً)",
                        "Today (اليوم)",
                        "This week/month (هذا الأسبوع/الشهر)",
                        "Listen! (استمع!)",
                        "Look! (انظر!)"
                    ],
                    examples: [
                        "I **am reading** a book now. (أنا أقرأ كتاباً الآن.)",
                        "She **is watching** TV. (هي تشاهد التلفاز.)",
                        "They **are not playing** football. (هم لا يلعبون كرة القدم.)",
                        "Are you **listening** to me? (هل تستمع إلي؟)",
                        "We **are having** dinner tomorrow. (سنتناول العشاء غداً - خطة مستقبلية مؤكدة.)",
                        "He **is working** on a new project. (هو يعمل على مشروع جديد.)",
                        "The kids **are playing** outside. (الأطفال يلعبون بالخارج.)",
                        "It **is raining** heavily. (إنها تمطر بغزارة.)",
                        "What **are you doing**? (ماذا تفعل؟)",
                        "My phone **is charging**. (هاتفي يشحن.)"
                    ]
                }
            },
            pronunciation: {
                vowels: {
                    title: "الحروف المتحركة (Vowels)",
                    arabicTitle: "Vowels and Their Sounds",
                    explanation: "الحروف المتحركة في اللغة الإنجليزية هي: <strong>A, E, I, O, U</strong>. هذه الحروف يمكن أن يكون لها أصوات مختلفة (قصيرة أو طويلة) حسب موقعها في الكلمة والحروف التي تحيط بها.",
                    rules: [
                        {
                            rule: "الصوت القصير للحرف المتحرك (Short Vowel Sound):",
                            description: "يحدث عندما يكون الحرف المتحرك متبوعًا بحرف ساكن واحد في مقطع قصير. يكون الصوت قصيرًا وحادًا.",
                            examples: [
                                { en: "Cat", ar: "قطة (صوت A قصير)" },
                                { en: "Bed", ar: "سرير (صوت E قصير)" },
                                { en: "Pig", ar: "خنزير (صوت I قصير)" },
                                { en: "Dog", ar: "كلب (صوت O قصير)" },
                                { en: "Sun", ar: "شمس (صوت U قصير)" }
                            ]
                        },
                        {
                            rule: "الصوت الطويل للحرف المتحرك (Long Vowel Sound):",
                            description: "يحدث عندما ينطق الحرف المتحرك باسمه (مثل A في 'cake'). غالبًا ما يحدث هذا عندما يكون هناك حرف 'e' صامت في نهاية الكلمة (Magic E) أو عندما يكون هناك حرفان متحركان متتاليان.",
                            examples: [
                                { en: "Cake", ar: "كعكة (صوت A طويل)" },
                                { en: "Tree", ar: "شجرة (صوت E طويل)" },
                                { en: "Bike", ar: "دراجة (صوت I طويل)" },
                                { en: "Boat", ar: "قارب (صوت O طويل)" },
                                { en: "Flute", ar: "ناي (صوت U طويل)" }
                            ]
                        }
                    ]
                },
                consonants: {
                    title: "الحروف الساكنة (Consonants)",
                    arabicTitle: "Consonants and Their Sounds",
                    explanation: "الحروف الساكنة هي جميع الحروف الأبجدية الإنجليزية باستثناء الحروف المتحركة (A, E, I, O, U). غالبًا ما يكون لكل حرف ساكن صوت واحد رئيسي، ولكن بعضها يمكن أن يكون له أصوات مختلفة حسب الحروف المحيطة به.",
                    rules: [
                        {
                            rule: "أمثلة على أصوات الحروف الساكنة الشائعة:",
                            description: "هذه بعض الأمثلة على أصوات الحروف الساكنة الأساسية.",
                            examples: [
                                { en: "Ball", ar: "كرة (صوت B)" },
                                { en: "Cat", ar: "قطة (صوت C مثل K)" },
                                { en: "Dog", ar: "كلب (صوت D)" },
                                { en: "Fan", ar: "مروحة (صوت F)" },
                                { en: "Goat", ar: "ماعز (صوت G)" },
                                { en: "Hat", ar: "قبعة (صوت H)" },
                                { en: "Jump", ar: "يقفز (صوت J)" },
                                { en: "King", ar: "ملك (صوت K)" }
                            ]
                        },
                        {
                            rule: "أصوات مركبة (Digraphs):",
                            description: "عندما يجتمع حرفان ساكنان لإنتاج صوت واحد مختلف.",
                            examples: [
                                { en: "Ship", ar: "سفينة (صوت SH)" },
                                { en: "Chair", ar: "كرسي (صوت CH)" },
                                { en: "Think", ar: "يفكر (صوت TH)" },
                                { en: "Whale", ar: "حوت (صوت WH)" }
                            ]
                        }
                    ]
                }
            }
        };

        const wordListContainer = document.getElementById('wordListContainer');
        const noteElement = document.getElementById('noteElement');
        const mainTitle = document.getElementById('mainTitle'); // Get main title element
        const audio = document.getElementById('backgroundAudio');
        const audioControl = document.getElementById('audioControl');
        let isPlaying = false;
        let startDelay = 0.1;


        // SpeechSynthesis API
        const synth = window.speechSynthesis;

        // Function to speak text (English only)
        function speakText(text) {
            if (synth.speaking) {
                synth.cancel();
            }
            const utterance = new SpeechSynthesisUtterance(text);
            utterance.lang = 'en-US'; // Set to English only
            utterance.rate = 0.95;
            utterance.pitch = 1;

            const voices = synth.getVoices();
            // Prioritize specific English voices for better quality
            utterance.voice = voices.find(voice => 
                voice.lang.startsWith('en') && 
                (voice.name.includes('Google') || voice.name.includes('Samantha') || voice.name.includes('Karen') || voice.name.includes('Zira'))
            ) || voices.find(voice => voice.lang.startsWith('en')); // Fallback to any English voice
            
            synth.speak(utterance);
        }

        // Function to display words for a given category (nouns, adjectives, etc.)
        function displayCategory(categoryName) {
            mainTitle.textContent = getCategoryArabicName(categoryName) === 'كلمات الجمعة' ? 'يوم جمعة سعيد!' : `فئة ${getCategoryArabicName(categoryName)}`;
            const wordsToDisplay = wordCategories[categoryName];
            wordListContainer.innerHTML = ''; // Clear previous content

            if (!wordsToDisplay || !Array.isArray(wordsToDisplay)) { 
                console.error("Category not found or not an array:", categoryName);
                wordListContainer.innerHTML = `<p style="color:red;">عذراً، لم يتم العثور على كلمات لهذه الفئة.</p>`;
                return;
            }

            // Restore columns for word lists
            wordListContainer.style.columns = '2';
            wordListContainer.style.columnGap = '40px';

            wordsToDisplay.forEach((item, index) => {
                const wordItemDiv = document.createElement('div');
                wordItemDiv.className = 'word-item';
                wordItemDiv.style.animationDelay = `${startDelay + (index * 0.05)}s`; 

                const englishWord = document.createElement('span');
                englishWord.className = 'english-word';
                englishWord.textContent = item.en;

                const arabicMeaning = document.createElement('span');
                arabicMeaning.className = 'arabic-meaning';
                arabicMeaning.textContent = item.ar;

                const buttonsGroup = document.createElement('div');
                buttonsGroup.className = 'read-buttons-group';

                const readEnButton = document.createElement('button');
                readEnButton.className = 'read-button';
                readEnButton.textContent = 'استمع'; 
                readEnButton.onclick = (event) => {
                    event.stopPropagation();
                    speakText(item.en); 
                };

                buttonsGroup.appendChild(readEnButton);

                wordItemDiv.appendChild(englishWord);
                wordItemDiv.appendChild(arabicMeaning);
                wordItemDiv.appendChild(buttonsGroup);
                wordListContainer.appendChild(wordItemDiv);
            });

            // Update note text based on category
            let noteText = "";
            if (categoryName === 'friday') {
                noteText = "نتمنى لكم عطلة نهاية أسبوع هادئة ومبهجة ومليئة بهذه اللحظات الرائعة!";
            } else {
                noteText = `تصفح ${wordsToDisplay.length} كلمة في فئة ${getCategoryArabicName(categoryName)}.`;
            }
            noteElement.textContent = noteText;

            // Reset animation delays for note and audio control
            const currentContentDelay = startDelay + (wordsToDisplay.length * 0.05);
            noteElement.style.setProperty('--note-delay', `${currentContentDelay + 0.5}s`);
            audioControl.style.setProperty('--button-delay', `${currentContentDelay + 0.9}s`);
        }

        // NEW FUNCTION: Show list of tenses to choose from
        function showTenseList() {
            mainTitle.textContent = 'اختر الزمن لتعلم قواعده';
            wordListContainer.innerHTML = ''; // Clear previous content
            wordListContainer.style.columns = '1'; // Single column for tense list
            wordListContainer.style.columnGap = '0'; // No gap

            const tenseListDiv = document.createElement('div');
            tenseListDiv.className = 'tense-list';

            // Loop through tenses data and create buttons for each
            for (const key in wordCategories.tenses) {
                if (wordCategories.tenses.hasOwnProperty(key)) {
                    const tense = wordCategories.tenses[key];
                    const button = document.createElement('button');
                    button.className = 'tense-selection-button';
                    button.textContent = tense.title;
                    button.onclick = () => displayTenseDetails(key);
                    tenseListDiv.appendChild(button);
                }
            }
            wordListContainer.appendChild(tenseListDiv);
            noteElement.textContent = "اختر أحد الأزمنة لترى الشرح والأمثلة.";
        }


        // NEW FUNCTION: Display details for a specific tense
        function displayTenseDetails(tenseName) {
            const tenseData = wordCategories.tenses[tenseName];
            wordListContainer.innerHTML = ''; // Clear previous content
            mainTitle.textContent = tenseData.title + " (" + tenseData.arabicTitle + ")"; // Update main title

            // Remove columns for tense explanations
            wordListContainer.style.columns = '1';
            wordListContainer.style.columnGap = '0';

            if (!tenseData) {
                console.error("Tense data not found:", tenseName);
                wordListContainer.innerHTML = `<p style="color:red;">عذراً، لم يتم العثور على تفاصيل لهذا الزمن.</p>`;
                return;
            }

            const tenseDiv = document.createElement('div');
            tenseDiv.className = 'tense-explanation';

            // Explanation
            const explanationTitle = document.createElement('h3');
            explanationTitle.textContent = 'الشرح:';
            tenseDiv.appendChild(explanationTitle);
            const explanation = document.createElement('p');
            explanation.textContent = tenseData.explanation;
            tenseDiv.appendChild(explanation);

            // Form
            const formTitle = document.createElement('h3');
            formTitle.textContent = 'صيغة الزمن:';
            tenseDiv.appendChild(formTitle);
            const formList = document.createElement('ul');
            for (const formType in tenseData.form) {
                if (tenseData.form.hasOwnProperty(formType)) {
                    const listItem = document.createElement('li');
                    let typeText = '';
                    if (formType === 'positive') typeText = 'الإثبات: ';
                    else if (formType === 'negative') typeText = 'النفي: ';
                    else if (formType === 'question') typeText = 'السؤال: ';
                    listItem.innerHTML = `<strong>${typeText}</strong> ${tenseData.form[formType]}`;
                    formList.appendChild(listItem);
                }
            }
            tenseDiv.appendChild(formList);


            // Keywords
            const keywordsTitle = document.createElement('h3');
            keywordsTitle.textContent = 'الكلمات الدالة:';
            tenseDiv.appendChild(keywordsTitle);
            const keywordsList = document.createElement('ul');
            tenseData.keywords.forEach(keyword => {
                const listItem = document.createElement('li');
                listItem.textContent = keyword;
                keywordsList.appendChild(listItem);
            });
            tenseDiv.appendChild(keywordsList);

            // Examples
            const examplesTitle = document.createElement('h3');
            examplesTitle.textContent = 'أمثلة:';
            tenseDiv.appendChild(examplesTitle);
            const examplesList = document.createElement('ul');
            examplesList.className = 'examples-list'; // Add class for specific styling
            tenseData.examples.forEach(example => {
                const listItem = document.createElement('li');
                const exampleText = document.createElement('span');
                exampleText.className = 'english-sentence';
                exampleText.textContent = example;
                listItem.appendChild(exampleText);
                
                const readExampleButton = document.createElement('button');
                readExampleButton.className = 'read-button example-button';
                readExampleButton.textContent = 'استمع';
                readExampleButton.onclick = (event) => {
                    event.stopPropagation();
                    const englishPart = example.split('(')[0].trim();
                    speakText(englishPart); 
                };
                listItem.appendChild(readExampleButton);
                examplesList.appendChild(listItem);
            });
            tenseDiv.appendChild(examplesList);

            wordListContainer.appendChild(tenseDiv); // Add the entire tense block

            // Update note text for tense section
            noteElement.textContent = "استمع للأمثلة وتمرّن على النطق.";

            // Reset animation delays (simplified for single tense display)
            noteElement.style.setProperty('--note-delay', `0.7s`);
            audioControl.style.setProperty('--button-delay', `1.0s`);
        }

        // NEW FUNCTION: Show pronunciation rules
        function showPronunciationRules() {
            mainTitle.textContent = 'قواعد النطق في اللغة الإنجليزية';
            wordListContainer.innerHTML = ''; // Clear previous content
            wordListContainer.style.columns = '1'; // Single column for pronunciation rules
            wordListContainer.style.columnGap = '0'; // No gap

            const pronunciationListDiv = document.createElement('div');
            pronunciationListDiv.className = 'pronunciation-list';

            // Button for Vowels
            const vowelsButton = document.createElement('button');
            vowelsButton.className = 'pronunciation-selection-button';
            vowelsButton.textContent = wordCategories.pronunciation.vowels.title;
            vowelsButton.onclick = () => displayPronunciationDetails('vowels');
            pronunciationListDiv.appendChild(vowelsButton);

            // Button for Consonants
            const consonantsButton = document.createElement('button');
            consonantsButton.className = 'pronunciation-selection-button';
            consonantsButton.textContent = wordCategories.pronunciation.consonants.title;
            consonantsButton.onclick = () => displayPronunciationDetails('consonants');
            pronunciationListDiv.appendChild(consonantsButton);

            wordListContainer.appendChild(pronunciationListDiv);
            noteElement.textContent = "اختر نوع الحروف لتعلم قواعد نطقها.";
        }

        // NEW FUNCTION: Display details for pronunciation rules
        function displayPronunciationDetails(ruleType) {
            const ruleData = wordCategories.pronunciation[ruleType];
            wordListContainer.innerHTML = ''; // Clear previous content
            mainTitle.textContent = ruleData.title + " (" + ruleData.arabicTitle + ")"; // Update main title

            wordListContainer.style.columns = '1';
            wordListContainer.style.columnGap = '0';

            if (!ruleData) {
                console.error("Pronunciation rule data not found:", ruleType);
                wordListContainer.innerHTML = `<p style="color:red;">عذراً، لم يتم العثور على تفاصيل لهذه القاعدة.</p>`;
                return;
            }

            const ruleDiv = document.createElement('div');
            ruleDiv.className = 'pronunciation-rules';

            // Explanation
            const explanationTitle = document.createElement('h3');
            explanationTitle.textContent = 'الشرح:';
            ruleDiv.appendChild(explanationTitle);
            const explanation = document.createElement('p');
            explanation.textContent = ruleData.explanation;
            ruleDiv.appendChild(explanation);

            // Rules and Examples
            ruleData.rules.forEach(ruleItem => {
                const ruleHeading = document.createElement('h3');
                ruleHeading.textContent = ruleItem.rule;
                ruleDiv.appendChild(ruleHeading);

                const ruleDescription = document.createElement('p');
                ruleDescription.textContent = ruleItem.description;
                ruleDiv.appendChild(ruleDescription);

                const examplesList = document.createElement('ul');
                examplesList.className = 'examples-list';
                ruleItem.examples.forEach(example => {
                    const listItem = document.createElement('li');
                    const exampleText = document.createElement('span');
                    exampleText.className = 'english-sentence';
                    exampleText.textContent = example.en + " " + example.ar; // Display English and Arabic
                    listItem.appendChild(exampleText);

                    const readExampleButton = document.createElement('button');
                    readExampleButton.className = 'read-button example-button';
                    readExampleButton.textContent = 'استمع';
                    readExampleButton.onclick = (event) => {
                        event.stopPropagation();
                        speakText(example.en); // Speak only the English part
                    };
                    listItem.appendChild(readExampleButton);
                    examplesList.appendChild(listItem);
                });
                ruleDiv.appendChild(examplesList);
            });

            wordListContainer.appendChild(ruleDiv);
            noteElement.textContent = "استمع للأمثلة وتمرّن على النطق الصحيح.";

            noteElement.style.setProperty('--note-delay', `0.7s`);
            audioControl.style.setProperty('--button-delay', `1.0s`);
        }


        function getCategoryArabicName(categoryName) {
            switch (categoryName) {
                case 'friday': return 'كلمات الجمعة';
                case 'nouns': return 'الأسماء';
                case 'adjectives': return 'الصفات';
                case 'verbs': return 'الأفعال الأساسية';
                case 'pronouns': return 'الضمائر';
                case 'colors': return 'الألوان';
                case 'tenses': return 'الأزمنة'; 
                case 'pronunciation': return 'قواعد النطق';
                default: return '';
            }
        }


        // --- Audio Control ---
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

        // Initial load: Display "Friday" words
        window.addEventListener('load', () => {
            displayCategory('friday'); // Display Friday words on initial load

            audio.play().then(() => {
                isPlaying = true;
                audioControl.textContent = 'إيقاف الموسيقى';
            }).catch(e => {
                console.log("Audio autoplay prevented. Please use the button.");
                audioControl.textContent = 'تشغيل الموسيقى';
            });

            if (synth.onvoiceschanged !== undefined) {
                synth.onvoiceschanged = () => {
                    // Update voice list if needed
                };
            }
        });
    </script>
</body>
</html>
