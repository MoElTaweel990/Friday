<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>يوم جمعة سعيد - كلمات وجمل</title>
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
        .content-table { /* اسم عام للجداول */
            width: 100%;
            border-collapse: separate;
            border-spacing: 0 10px;
            margin-top: 20px;
            direction: rtl;
            animation: fadeIn 1s ease-out;
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
            text-align: center;
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
            transform: scale(1.02);
        }

        .english-text {
            color: #98FB98;
            font-weight: bold;
        }

        .arabic-text {
            color: #ADD8E6;
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

        // قائمة الحروف الإنجليزية
        const alphabetLetters = [
            "A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M",
            "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"
        ];

        // قائمة الكلمات الأساسية (يُفضل زيادة عدد الكلمات هنا لتنوع أكبر)
        const baseWords = [
            { en: "Apple", ar: "تفاحة" }, { en: "Ant", ar: "نملة" }, { en: "Ate", ar: "أكل" }, { en: "Always", ar: "دائماً" }, { en: "Are", ar: "يكون" },
            { en: "Ball", ar: "كرة" }, { en: "Boy", ar: "ولد" }, { en: "Big", ar: "كبير" }, { en: "Blue", ar: "أزرق" }, { en: "Book", ar: "كتاب" },
            { en: "Cat", ar: "قطة" }, { en: "Car", ar: "سيارة" }, { en: "Can", ar: "يستطيع" }, { en: "Coffee", ar: "قهوة" }, { en: "Cool", ar: "رائع" },
            { en: "Dog", ar: "كلب" }, { en: "Day", ar: "يوم" }, { en: "Down", ar: "أسفل" }, { en: "Done", ar: "انتهى" }, { en: "Door", ar: "باب" },
            { en: "Elephant", ar: "فيل" }, { en: "Eat", ar: "يأكل" }, { en: "Easy", ar: "سهل" }, { en: "Every", ar: "كل" }, { en: "Enjoy", ar: "استمتع" },
            { en: "Fish", ar: "سمكة" }, { en: "Fun", ar: "مرح" }, { en: "Fast", ar: "سريع" }, { en: "Find", ar: "يجد" }, { en: "Family", ar: "عائلة" },
            { en: "Go", ar: "يذهب" }, { en: "Green", ar: "أخضر" }, { en: "Good", ar: "جيد" }, { en: "Game", ar: "لعبة" }, { en: "Garden", ar: "حديقة" },
            { en: "House", ar: "منزل" }, { en: "Happy", ar: "سعيد" }, { en: "Hello", ar: "أهلاً" }, { en: "Hand", ar: "يد" }, { en: "Help", ar: "مساعدة" },
            { en: "Ice", ar: "ثلج" }, { en: "In", ar: "في" }, { en: "Idea", ar: "فكرة" }, { en: "Into", ar: "داخل" }, { en: "Island", ar: "جزيرة" },
            { en: "Jump", ar: "يقفز" }, { en: "Joy", ar: "فرح" }, { en: "Just", ar: "فقط" }, { en: "Join", ar: "ينضم" }, { en: "Juice", ar: "عصير" },
            { en: "Key", ar: "مفتاح" }, { en: "King", ar: "ملك" }, { en: "Keep", ar: "يحتفظ" }, { en: "Know", ar: "يعرف" }, { en: "Kind", ar: "طيب" },
            { en: "Lion", ar: "أسد" }, { en: "Love", ar: "حب" }, { en: "Light", ar: "ضوء" }, { en: "Long", ar: "طويل" }, { en: "Laugh", ar: "يضحك" },
            { en: "Monkey", ar: "قرد" }, { en: "Man", ar: "رجل" }, { en: "More", ar: "أكثر" }, { en: "Music", ar: "موسيقى" }, { en: "Morning", ar: "صباح" },
            { en: "New", ar: "جديد" }, { en: "Now", ar: "الآن" }, { en: "Night", ar: "ليل" }, { en: "Near", ar: "قريب" }, { en: "Nice", ar: "لطيف" },
            { en: "Orange", ar: "برتقال" }, { en: "Open", ar: "يفتح" }, { en: "Old", ar: "قديم" }, { en: "Over", ar: "فوق" }, { en: "One", ar: "واحد" },
            { en: "Pig", ar: "خنزير" }, { en: "Play", ar: "يلعب" }, { en: "Put", ar: "يضع" }, { en: "Pink", ar: "وردي" }, { en: "Phone", ar: "هاتف" },
            { en: "Queen", ar: "ملكة" }, { en: "Quick", ar: "سريع" }, { en: "Quiet", ar: "هادئ" }, { en: "Quite", ar: "تماماً" }, { en: "Question", ar: "سؤال" },
            { en: "Rabbit", ar: "أرنب" }, { en: "Red", ar: "أحمر" }, { en: "Run", ar: "يجري" }, { en: "Read", ar: "يقرأ" }, { en: "Right", ar: "صحيح" },
            { en: "Sun", ar: "شمس" }, { en: "Sing", ar: "يغني" }, { en: "Sweet", ar: "حلو" }, { en: "Smile", ar: "ابتسامة" }, { en: "Sleep", ar: "ينام" },
            { en: "Tree", ar: "شجرة" }, { en: "Talk", ar: "يتكلم" }, { en: "Time", ar: "وقت" }, { en: "True", ar: "صحيح" }, { en: "Thank", ar: "يشكر" },
            { en: "Umbrella", ar: "مظلة" }, { en: "Up", ar: "أعلى" }, { en: "Under", ar: "تحت" }, { en: "Useful", ar: "مفيد" }, { en: "Unicorn", ar: "وحيد القرن" },
            { en: "Van", ar: "فان" }, { en: "Very", ar: "جداً" }, { en: "Voice", ar: "صوت" }, { en: "Visit", ar: "يزور" }, { en: "View", ar: "منظر" },
            { en: "Water", ar: "ماء" }, { en: "Walk", ar: "يمشي" }, { en: "White", ar: "أبيض" }, { en: "Work", ar: "يعمل" }, { en: "Warm", ar: "دافئ" },
            { en: "X-ray", ar: "أشعة إكس" }, { en: "Xylophone", ar: "إكسيلوفون" }, { en: "Xenophobia", ar: "رهاب الأجانب" }, { en: "Xeric", ar: "جاف" }, { en: "Xerox", ar: "يصور" },
            { en: "Yellow", ar: "أصفر" }, { en: "Yes", ar: "نعم" }, { en: "You", ar: "أنت" }, { en: "Young", ar: "شاب" }, { en: "Yoga", ar: "يوغا" },
            { en: "Zebra", ar: "حمار وحشي" }, { en: "Zero", ar: "صفر" }, { en: "Zoo", ar: "حديقة حيوان" }, { en: "Zone", ar: "منطقة" }, { en: "Zip", ar: "سحاب" }
            // **يمكنك إضافة المزيد من الكلمات هنا لزيادة التنوع لكل حرف**
        ];
        
        // قائمة الجمل الإنجليزية الأساسية مع معانيها العربية
        const basePhrases = [
            // جمل عامة
            { en: "Hello, how are you?", ar: "أهلاً، كيف حالك؟" },
            { en: "Good morning.", ar: "صباح الخير." },
            { en: "Good afternoon.", ar: "مساء الخير (بعد الظهر)." },
            { en: "Good evening.", ar: "مساء الخير (مساءً)." },
            { en: "Good night.", ar: "تصبح على خير." },
            { en: "Thank you.", ar: "شكراً لك." },
            { en: "You're welcome.", ar: "على الرحب والسعة." },
            { en: "Excuse me.", ar: "عذرًا." },
            { en: "I'm sorry.", ar: "أنا آسف." },
            { en: "Please.", ar: "من فضلك." },
            { en: "Yes.", ar: "نعم." },
            { en: "No.", ar: "لا." },
            { en: "Maybe.", ar: "ربما." },
            { en: "I don't understand.", ar: "أنا لا أفهم." },
            { en: "Can you help me?", ar: "هل يمكنك مساعدتي؟" },
            { en: "What is your name?", ar: "ما اسمك؟" },
            { en: "My name is...", ar: "اسمي هو..." },
            { en: "Nice to meet you.", ar: "سعيد بلقائك." },
            { en: "How much is this?", ar: "بكم هذا؟" },
            { en: "Where is the restroom?", ar: "أين دورة المياه؟" },

            // جمل للعمل
            { en: "I need to finish this report.", ar: "أحتاج لإنهاء هذا التقرير." },
            { en: "Can we schedule a meeting?", ar: "هل يمكننا تحديد موعد لاجتماع؟" },
            { en: "I'll send you an email.", ar: "سأرسل لك بريدًا إلكترونيًا." },
            { en: "What's the deadline?", ar: "ما هو الموعد النهائي؟" },
            { en: "Let's discuss this further.", ar: "دعنا نناقش هذا بتفصيل أكثر." },
            { en: "I'll get back to you.", ar: "سأعود إليك لاحقًا." },
            { en: "Can you explain that again?", ar: "هل يمكنك شرح ذلك مرة أخرى؟" },
            { en: "I'm working on it.", ar: "أنا أعمل على ذلك." },
            { en: "This is urgent.", ar: "هذا أمر عاجل." },
            { en: "Good job!", ar: "عمل جيد!" },

            // جمل للمدرسة
            { en: "I have a question.", ar: "لدي سؤال." },
            { en: "Can you repeat that, please?", ar: "هل يمكنك تكرار ذلك، من فضلك؟" },
            { en: "I need help with my homework.", ar: "أحتاج مساعدة في واجبي." },
            { en: "What page are we on?", ar: "في أي صفحة نحن؟" },
            { en: "Can I borrow a pen?", ar: "هل يمكنني استعارة قلم؟" },
            { en: "The class starts at...", ar: "الحصة تبدأ الساعة..." },
            { en: "I'm ready to learn.", ar: "أنا مستعد للتعلم." },
            { en: "Let's study together.", ar: "دعنا ندرس معًا." },
            { en: "I passed the exam!", ar: "لقد اجتزت الامتحان!" },
            { en: "What's for lunch?", ar: "ماذا يوجد للغداء؟" },

            // جمل للشارع/المواقف اليومية
            { en: "Where is the nearest bank?", ar: "أين أقرب بنك؟" },
            { en: "How can I get to...?", ar: "كيف يمكنني الوصول إلى...؟" },
            { en: "Can you show me on the map?", ar: "هل يمكنك أن تريني على الخريطة؟" },
            { en: "It's too far to walk.", ar: "إنه بعيد جداً للمشي." },
            { en: "Is this the right way?", ar: "هل هذا هو الطريق الصحيح؟" },
            { en: "Watch out!", ar: "احذر!" },
            { en: "It's a beautiful day.", ar: "إنه يوم جميل." },
            { en: "Can I help you?", ar: "هل يمكنني مساعدتك؟" },
            { en: "I'm lost.", ar: "أنا تائه." },
            { en: "Have a good day!", ar: "أتمنى لك يومًا جيدًا!" }
        ];
        
        const wordsPerLetter = 20; // عدد الكلمات لكل حرف
        const alphabetPageWordsCount = alphabetLetters.length * wordsPerLetter; // إجمالي الكلمات في صفحة الحروف

        let allPhrases = []; // لتخزين الجمل فقط
        const desiredPhrasesCount = 1000 - alphabetPageWordsCount; // عدد الجمل المطلوب لملء الـ 1000 كلمة/جملة المتبقية
        if (desiredPhrasesCount < 0) { // لو عدد كلمات الحروف تجاوز الـ 1000
            desiredPhrasesCount = 0; // يبقى مش هنضيف جمل
        }

        const itemsPerPage = 20; // عدد العناصر (سطر في الجدول) في كل صفحة للجمل

        let currentPage = 1;
        let totalPages = 0;

        const wordsContainer = document.getElementById('wordsContainer');
        const prevPageBtn = document.getElementById('prevPage');
        const nextPageBtn = document = document.getElementById('nextPage');
        const pageInfoSpan = document.getElementById('pageInfo');
        const noteElement = document.getElementById('noteElement');
        const audio = document.getElementById('backgroundAudio');
        const audioControl = document.getElementById('audioControl');
        let isPlaying = false;
        let startDelay = 1.6;

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

        // دالة لإنشاء جدول وعرض الكلمات أو الجمل
        function createAndDisplayTable(title, data, isAlphabetTable = false) {
            const sectionTitle = document.createElement('h2');
            sectionTitle.textContent = title;
            sectionTitle.style.color = "#FFEB3B";
            sectionTitle.style.marginTop = "40px";
            sectionTitle.style.marginBottom = "20px";
            sectionTitle.style.textShadow = "2px 2px 4px rgba(0,0,0,0.4)";
            wordsContainer.appendChild(sectionTitle);

            const table = document.createElement('table');
            table.className = 'content-table';
            table.setAttribute('dir', 'rtl');

            const thead = document.createElement('thead');
            const headerRow = document.createElement('tr');
            const thAction = document.createElement('th'); thAction.textContent = 'استمع';
            const thEn = document.createElement('th'); thEn.textContent = isAlphabetTable ? 'الكلمة الإنجليزية' : 'الجملة الإنجليزية';
            const thAr = document.createElement('th'); thAr.textContent = 'المعنى العربي';
            
            headerRow.appendChild(thAction);
            headerRow.appendChild(thEn);
            headerRow.appendChild(thAr);
            thead.appendChild(headerRow);
            table.appendChild(thead);

            const tbody = document.createElement('tbody');
            data.forEach(item => {
                const tr = document.createElement('tr');
                const tdAction = document.createElement('td');
                const readBtn = document.createElement('button');
                readBtn.className = 'read-button';
                readBtn.textContent = 'استمع';
                readBtn.onclick = (event) => {
                    event.stopPropagation();
                    speakText(item.en);
                };
                tdAction.appendChild(readBtn);

                const tdEn = document.createElement('td');
                tdEn.className = 'english-text';
                tdEn.textContent = item.en;

                const tdAr = document.createElement('td');
                tdAr.className = 'arabic-text';
                tdAr.textContent = item.ar;
                
                tr.appendChild(tdAction);
                tr.appendChild(tdEn);
                tr.appendChild(tdAr);
                tbody.appendChild(tr);
            });
            table.appendChild(tbody);
            wordsContainer.appendChild(table);
        }

        // دالة لعرض المحتوى للصفحة الحالية
        function displayContentForPage(pageNumber) {
            wordsContainer.innerHTML = ''; // تفريغ المحتوى الحالي

            if (pageNumber === 1) {
                // الصفحة الأولى: عرض الكلمات لكل حرف
                alphabetLetters.forEach(letter => {
                    const wordsForLetter = baseWords.filter(word => word.en.startsWith(letter.toUpperCase()));
                    let selectedWords = [];

                    // كرر الكلمات لملء الـ 20 كلمة لو العدد مش كافي
                    let tempWordsPool = [];
                    while (tempWordsPool.length < wordsPerLetter) {
                        tempWordsPool = tempWordsPool.concat(wordsForLetter);
                        // لو مافيش كلمات للحرف ده أصلا، نستخدم كلمات عامة لتجنب اللانهائية
                        if (wordsForLetter.length === 0 && tempWordsPool.length === 0) {
                            tempWordsPool = tempWordsPool.concat(baseWords.slice(0, 5)); // 5 كلمات عامة
                        }
                    }
                    selectedWords = shuffleArray(tempWordsPool).slice(0, wordsPerLetter);

                    createAndDisplayTable(`كلمات تبدأ بحرف "${letter.toUpperCase()}"`, selectedWords, true);
                });
            } else {
                // الصفحات الأخرى: عرض الجمل اليومية
                const startIndex = (pageNumber - 2) * itemsPerPage; // -2 لأن الصفحة الأولى خاصة بالحروف
                const endIndex = Math.min(startIndex + itemsPerPage, allPhrases.length);
                const phrasesForCurrentPage = allPhrases.slice(startIndex, endIndex);
                
                if (phrasesForCurrentPage.length > 0) {
                    createAndDisplayTable("جمل بسيطة للاستخدام اليومي", phrasesForCurrentPage, false);
                } else {
                    wordsContainer.innerHTML = "<p style='font-size: 1.5em; color: #ADD8E6;'>لا توجد المزيد من الجمل لعرضها.</p>";
                }
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
            // تجهيز قائمة الجمل العشوائية
            let tempPhrasesPool = [];
            while (tempPhrasesPool.length < desiredPhrasesCount) {
                tempPhrasesPool = tempPhrasesPool.concat(basePhrases);
            }
            allPhrases = shuffleArray(tempPhrasesPool).slice(0, desiredPhrasesCount);

            // حساب إجمالي الصفحات
            // الصفحة الأولى مخصصة لكلمات الحروف.
            // عدد الصفحات الإضافية للجمل = ceil(عدد الجمل / الكلمات في الصفحة)
            totalPages = 1 + Math.ceil(allPhrases.length / itemsPerPage);
            if (allPhrases.length === 0 && alphabetPageWordsCount > 0) { // لو مفيش جمل بس فيه حروف
                totalPages = 1;
            } else if (allPhrases.length === 0 && alphabetPageWordsCount === 0) { // لو مفيش اي محتوى
                totalPages = 0;
            }


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
                    audioControl.textContent = 'إيقاف الموسيقى';
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
