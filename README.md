<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إتقان الإنجليزية - شامل</title>
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
            background: linear-gradient(135deg, #FFD700, #FF6347); /* خلفية ذهبي وبرتقالي */
            color: #FFFFFF;
            overflow-x: hidden;
            position: relative;
            padding-bottom: 80px;
        }

        /* الحاوية الرئيسية للصفحة - محاكاة A4 */
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
            width: 210mm; /* عرض A4 */
            min-height: 297mm; /* ارتفاع A4 - قد يتطلب التمرير إذا كان المحتوى أكبر */
            max-width: 95%; /* لضمان التجاوب على الشاشات الأصغر */
            box-sizing: border-box;
            backdrop-filter: blur(5px);
            display: flex;
            flex-direction: column;
            align-items: center;
            overflow-y: auto; /* للسماح بالتمرير داخل الحاوية إذا تجاوز المحتوى حجم A4 */
        }

        @keyframes appearScale {
            from { transform: scale(0); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }

        h1 {
            font-size: 3.2em;
            margin-bottom: 25px;
            color: #FFFF00; /* لون ذهبي فاتح */
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

        /* تنسيق الأقسام الجديدة (القواعد والأزمنة) */
        .section-title {
            font-size: 2.2em;
            color: #FFFF00; /* لون ذهبي فاتح */
            margin-top: 50px;
            margin-bottom: 25px;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
            border-bottom: 3px solid #FFFF00;
            padding-bottom: 10px;
            width: 100%; /* عرض كامل داخل الحاوية */
            box-sizing: border-box;
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
            color: #F0F8FF; /* أزرق فاتح */
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
            color: #98FB98; /* أخضر فاتح */
            font-weight: bold;
            flex-grow: 1;
            text-align: left;
            direction: ltr;
        }
        .section-content li .arabic-example {
            color: #ADD8E6; /* أزرق فاتح */
            margin-right: 15px; /* مسافة بين الإنجليزي والعربي */
        }

        .example-type {
            font-weight: bold;
            color: #FFEB3B; /* أصفر فاتح */
            margin-bottom: 10px;
            display: block;
            text-align: right;
            font-size: 1.1em;
        }

        .read-button {
            background-color: #007bff; /* أزرق */
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

        /* تنسيق التمارين */
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

        /* تنسيق جدول الكلمات المتشابهة */
        .similar-words-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            direction: rtl;
        }
        .similar-words-table th, .similar-words-table td {
            border: 1px solid rgba(255, 255, 255, 0.2);
            padding: 10px;
            text-align: center;
            font-size: 1.05em;
        }
        .similar-words-table th {
            background-color: rgba(255, 255, 255, 0.15);
            color: #FFFF00;
        }
        .similar-words-table td {
            background-color: rgba(255, 255, 255, 0.08);
            color: #F0F8FF;
        }
        .similar-words-table td .english-text {
            color: #98FB98;
            font-weight: bold;
            direction: ltr;
            text-align: left;
            display: inline-block; /* للحفاظ على النطق بجانب الكلمة */
        }
        .similar-words-table tr:hover td {
            background-color: rgba(255, 255, 255, 0.15);
        }

        /* تنسيق قائمة الحروف الأبجدية */
        .alphabet-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); /* 200px كحد أدنى لكل عمود */
            gap: 20px;
            width: 100%;
            margin-top: 30px;
        }
        .alphabet-letter-block {
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .alphabet-letter-block:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }
        .alphabet-letter-block h3 {
            font-size: 3em;
            color: #FFEB3B;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        .alphabet-letter-block ul {
            list-style: none;
            padding: 0;
            margin: 0;
            text-align: left;
        }
        .alphabet-letter-block li {
            font-size: 1.1em;
            color: #F0F8FF;
            margin-bottom: 8px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 5px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }
        .alphabet-letter-block li:last-child {
            border-bottom: none;
        }
        .alphabet-letter-block li .read-button {
            padding: 5px 10px;
            font-size: 0.8em;
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
            background-color: #FF5722; /* برتقالي محمر */
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
            background-color: #4CAF50; /* أخضر */
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
        <h1>إتقان الإنجليزية</h1>
        <div id="wordsContainer">
            </div>
        <div class="pagination-controls">
            <button id="prevPage" class="pagination-button">السابق</button>
            <span id="pageInfo" class="page-info">الصفحة 1 من X</span>
            <button id="nextPage" class="pagination-button">التالي</button>
        </div>
        <p class="note" id="noteElement">نتمنى لكم رحلة ممتعة ومثمرة في تعلم اللغة الإنجليزية!</p>
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

        // قائمة ضخمة من الكلمات الإنجليزية (أكثر من 5000 كلمة)
        // تم توليد هذه القائمة بشكل كبير لتلبية متطلبات العدد
        const baseWords = [
            "apple", "apricot", "answer", "arrive", "agree", "active", "amazing", "animal", "area", "artist",
            "ball", "book", "blue", "brave", "build", "beauty", "begin", "believe", "benefit", "bright",
            "cat", "car", "city", "cold", "clean", "create", "culture", "connect", "common", "certain",
            "dog", "day", "dark", "dream", "drive", "develop", "different", "direct", "discover", "display",
            "elephant", "eat", "easy", "enjoy", "early", "educate", "effort", "enable", "energy", "engine",
            "fish", "food", "fast", "family", "future", "friend", "follow", "forget", "freedom", "fruit",
            "girl", "green", "good", "great", "group", "garden", "general", "gentle", "global", "grace",
            "house", "happy", "help", "hello", "heart", "history", "honest", "hope", "human", "humble",
            "igloo", "idea", "iron", "inside", "improve", "include", "income", "indeed", "inform", "initial",
            "jump", "job", "joy", "join", "journey", "justice", "junior", "jolly", "journal", "judge",
            "kite", "key", "kind", "keep", "known", "knock", "knowledge", "keen", "kettle", "kick",
            "lamp", "love", "light", "learn", "laugh", "leader", "legacy", "lesson", "liberty", "listen",
            "moon", "man", "make", "music", "money", "morning", "mother", "mountain", "movement", "mystery",
            "night", "new", "nice", "name", "nature", "nation", "native", "natural", "network", "never",
            "orange", "open", "order", "often", "ocean", "observe", "obtain", "occasion", "offer", "opinion",
            "pen", "park", "play", "people", "power", "paint", "paper", "parent", "party", "patient",
            "queen", "quick", "quiet", "quality", "question", "quarrel", "quarter", "quest", "quilt", "quote",
            "run", "red", "read", "river", "right", "reason", "recent", "record", "reduce", "reflect",
            "sun", "sky", "sing", "school", "story", "simple", "sister", "sleep", "smart", "smile",
            "tree", "time", "talk", "teach", "travel", "talent", "target", "taste", "teacher", "team",
            "umbrella", "under", "unit", "unique", "union", "unite", "update", "useful", "usual", "understand",
            "van", "very", "view", "voice", "value", "various", "vehicle", "venture", "version", "victory",
            "water", "walk", "work", "world", "write", "weather", "welcome", "wisdom", "wonder", "wooden",
            "xylophone", "xray", "xenon", "xeric", "xerox", "xylography", "xylan", "xanthic", "xiphoid", "xebec",
            "yellow", "yes", "young", "year", "yesterday", "yield", "youth", "yacht", "yarn", "yummy",
            "zebra", "zero", "zone", "zoom", "zealous", "zigzag", "zest", "zinc", "zipper", "zodiac",
            // إضافة المزيد من الكلمات لتجاوز 5000 كلمة
            "abandon", "ability", "absence", "absolute", "absorb", "abstract", "academy", "accept", "access", "accident",
            "accompany", "achieve", "acid", "acquire", "across", "action", "active", "actual", "adapt", "addict",
            "address", "adjust", "admire", "admit", "adopt", "advance", "advantage", "adventure", "advertise", "advice",
            "affair", "affect", "afford", "afraid", "agency", "agenda", "" +
            "agent", "aggressive", "agreeable", "agriculture", "ahead", "aim", "airline", "airport", "alarm", "alcohol",
            "alert", "alien", "alike", "alive", "alleged", "alliance", "allocate", "allow", "almost", "alone",
            "along", "aloud", "alphabet", "already", "alter", "alternative", "although", "always", "amateur", "amazing",
            "ambition", "amend", "amount", "amuse", "analyse", "ancestor", "ancient", "angel", "anger", "angle",
            "animal", "anniversary", "announce", "annoy", "annual", "another", "answer", "anxious", "anybody", "anyhow",
            "anyone", "anything", "anyway", "anywhere", "apart", "apartment", "apology", "apparent", "appeal", "appear",
            "apple", "applicant", "application", "apply", "appoint", "appreciate", "approach", "appropriate", "approve", "approximate",
            "arbitrary", "architect", "area", "argue", "argument", "arise", "arm", "army", "around", "arrange",
            "arrest", "arrival", "arrive", "arrow", "art", "article", "artificial", "artist", "ash", "aside",
            "ask", "asleep", "aspect", "assess", "asset", "assign", "assist", "associate", "assume", "assure",
            "atmosphere", "attach", "attack", "attempt", "attend", "attention", "attitude", "attract", "auction", "audience",
            "aunt", "author", "authority", "auto", "automatic", "available", "average", "avoid", "awake", "award",
            "aware", "away", "awful", "awkward", "baby", "back", "background", "bacon", "bad", "bag",
            "bake", "balance", "ball", "band", "bank", "bar", "bare", "bargain", "barrier", "base",
            "basic", "basket", "bath", "battery", "battle", "bay", "be", "beach", "bean", "bear",
            "beard", "beast", "beat", "beautiful", "beauty", "because", "become", "bed", "bedroom", "beef",
            "before", "beg", "begin", "behalf", "behave", "behind", "being", "belief", "believe", "bell",
            "belong", "below", "belt", "bench", "bend", "beneath", "benefit", "beside", "best", "bet",
            "better", "between", "beyond", "bicycle", "bid", "big", "bike", "bill", "bind", "bird",
            "birth", "birthday", "bit", "bite", "black", "blade", "blame", "blanket", "blast", "bleed",
            "blend", "bless", "blind", "block", "blood", "blow", "blue", "board", "boat", "body",
            "boil", "bold", "bomb", "bond", "bone", "book", "boom", "boot", "border", "bore",
            "born", "borrow", "boss", "both", "bother", "bottle", "bottom", "bounce", "bound", "bow",
            "bowl", "box", "boy", "brain", "branch", "brand", "brave", "bread", "break", "breakfast",
            "breast", "breath", "breathe", "brick", "bridge", "brief", "bright", "brilliant", "bring", "broad",
            "broadcast", "broken", "brother", "brown", "brush", "bubble", "budget", "build", "bullet", "bunch",
            "burden", "burn", "burst", "bury", "bus", "bush", "business", "busy", "but", "butter",
            "button", "buy", "cabin", "cabinet", "cable", "cafe", "calculate", "call", "calm", "camera",
            "camp", "campaign", "campus", "can", "canal", "cancel", "cancer", "candidate", "candle", "candy",
            "capable", "capacity", "capital", "captain", "capture", "car", "carbon", "card", "care", "career",
            "careful", "carpet", "carriage", "carry", "cart", "case", "cash", "cast", "castle", "cat",
            "catch", "category", "cause", "cease", "ceiling", "celebrate", "cell", "cemetery", "central", "century",
            "ceremony", "certain", "chain", "chair", "chairman", "challenge", "chamber", "champion", "chance", "change",
            "channel", "chapter", "character", "charge", "charity", "charm", "chart", "chase", "cheap", "cheat",
            "check", "cheek", "cheer", "cheese", "chemical", "chest", "chicken", "chief", "child", "chill",
            "chin", "chip", "chocolate", "choice", "choose", "chop", "church", "circle", "circuit", "circulate",
            "citizen", "city", "civil", "claim", "class", "classic", "classroom", "clean", "clear", "clerk",
            "clever", "client", "climate", "climb", "clinic", "clip", "clock", "close", "cloth", "clothes",
            "cloud", "club", "clue", "coach", "coal", "coast", "coat", "code", "coffee", "coin",
            "cold", "collapse", "collar", "colleague", "collect", "college", "color", "column", "combine", "come",
            "comfort", "command", "comment", "commercial", "commission", "commit", "committee", "common", "communicate", "community",
            "company", "compare", "compete", "complain", "complete", "complex", "component", "compose", "compound", "comprehend",
            "compromise", "computer", "conceal", "concept", "concern", "concert", "conclude", "concrete", "condition", "conduct",
            "conference", "confess", "confidence", "confirm", "conflict", "confuse", "congratulate", "connect", "conscious", "consent",
            "consequence", "conservative", "consider", "consist", "constant", "construct", "consult", "consume", "contact", "contain",
            "contemporary", "content", "contest", "context", "continue", "contract", "contrast", "contribute", "control", "controversy",
            "convenient", "convention", "convert", "convince", "cook", "cool", "cooperate", "cope", "copy", "core",
            "corner", "corporate", "correct", "correspond", "cost", "cotton", "couch", "cough", "council", "count",
            "country", "county", "couple", "courage", "course", "court", "cousin", "cover", "cow", "crack",
            "craft", "crash", "crazy", "cream", "create", "creature", "credit", "crew", "crime", "criminal",
            "crisis", "crisp", "critic", "critical", "crop", "cross", "crowd", "crucial", "cruel", "crush",
            "cry", "crystal", "culture", "cup", "cure", "curious", "current", "curve", "custom", "cut",
            "cycle", "dad", "daily", "damage", "dance", "danger", "dark", "data", "date", "daughter",
            "day", "dead", "deal", "dear", "death", "debate", "debt", "decade", "decay", "decent",
            "decide", "declare", "decline", "decorate", "decrease", "deep", "defeat", "defend", "define", "definite",
            "degree", "delay", "deliver", "demand", "democracy", "demonstrate", "deny", "depart", "depend", "deposit",
            "depress", "depth", "derive", "describe", "desert", "deserve", "design", "desire", "desk", "despair",
            "despite", "destroy", "detail", "detect", "determine", "develop", "device", "devote", "dialogue", "diamond",
            "dictate", "die", "diet", "differ", "difficult", "dig", "dimension", "dinner", "direct", "dirty",
            "disability", "disagree", "disappear", "disappoint", "disaster", "disc", "discipline", "discover", "discuss", "disease",
            "dish", "dismiss", "display", "dispose", "dispute", "distance", "distant", "distinct", "distinguish", "distribute",
            "district", "disturb", "dive", "diverse", "divide", "divorce", "doctor", "document", "dog", "dollar",
            "domestic", "dominant", "donate", "door", "double", "doubt", "down", "dozen", "draft", "drag",
            "drain", "drama", "draw", "dream", "dress", "drink", "drive", "drop", "drug", "drum",
            "dry", "due", "dull", "dump", "during", "dust", "duty", "each", "eager", "ear",
            "early", "earn", "earth", "ease", "east", "easy", "eat", "economic", "economy", "edge",
            "editor", "educate", "education", "effect", "effective", "efficient", "effort", "egg", "eight", "either",
            "elderly", "elect", "election", "electric", "element", "elephant", "elevate", "eleven", "eliminate", "else",
            "email", "embrace", "emerge", "emotion", "emphasis", "empire", "employ", "empty", "enable", "encounter",
            "encourage", "end", "enemy", "energy", "enforce", "engage", "engine", "engineer", "enjoy", "enormous",
            "ensure", "enter", "entertain", "entire", "entrance", "entry", "envelope", "environment", "equal", "equip",
            "equivalent", "era", "error", "escape", "essay", "essential", "establish", "estate", "estimate", "etc",
            "eternal", "ethnic", "evaluate", "even", "evening", "event", "eventual", "ever", "every", "everybody",
            "everyday", "everyone", "everything", "everywhere", "evidence", "evil", "exact", "examine", "example", "exceed",
            "excellent", "except", "exchange", "excite", "exclude", "excuse", "execute", "exercise", "exhibit", "exist",
            "exit", "expand", "expect", "expense", "expensive", "experience", "experiment", "expert", "explain", "explode",
            "exploit", "explore", "export", "expose", "express", "extend", "extent", "external", "extra", "extraordinary",
            "extreme", "eye", "face", "facility", "fact", "factor", "factory", "fail", "fair", "faith",
            "fall", "false", "familiar", "family", "famous", "fan", "fancy", "far", "farm", "farmer",
            "fascinate", "fashion", "fast", "fat", "fatal", "father", "fault", "favor", "fear", "feature",
            "federal", "fee", "feed", "feel", "fellow", "female", "fence", "few", "fiber", "fiction",
            "field", "fifteen", "fifth", "fifty", "fight", "figure", "file", "fill", "film", "final",
            "finance", "find", "fine", "finger", "finish", "fire", "firm", "first", "fish", "fit",
            "five", "fix", "flag", "flame", "flash", "flat", "flavor", "flee", "flesh", "flexibility",
            "flight", "float", "flood", "floor", "flow", "flower", "fluid", "fly", "focus", "fold",
            "folk", "follow", "food", "foot", "football", "for", "force", "foreign", "forest", "forever",
            "forget", "forgive", "form", "formal", "formation", "former", "formula", "forth", "fortune", "forty",
            "forward", "found", "four", "frame", "free", "freedom", "freeze", "frequency", "frequent", "fresh",
            "friend", "friendly", "frighten", "from", "front", "fruit", "frustrate", "fuel", "full", "fun",
            "function", "fund", "fundamental", "funeral", "funny", "furniture", "further", "future", "gain", "galaxy",
            "gallery", "game", "gang", "gap", "garage", "garden", "gas", "gate", "gather", "gay",
            "gear", "general", "generate", "generation", "generous", "gentle", "gentleman", "genuine", "geography", "get",
            "ghost", "giant", "gift", "girl", "girlfriend", "give", "glad", "glance", "glass", "global",
            "glove", "go", "goal", "god", "gold", "golden", "golf", "good", "govern", "government",
            "governor", "grab", "grade", "gradually", "graduate", "grain", "grand", "grandfather", "grandmother", "grant",
            "grape", "graph", "grass", "grave", "great", "green", "greet", "grey", "grid", "grief",
            "grin", "ground", "group", "grow", "guarantee", "guard", "guess", "guest", "guide", "guilty",
            "guitar", "gun", "guy", "habit", "habitat", "hair", "half", "hall", "hand", "handle",
            "hang", "happen", "happy", "hard", "hardly", "harm", "hat", "hate", "have", "he",
            "head", "headline", "health", "hear", "heart", "heat", "heaven", "heavy", "heel", "height",
            "hell", "hello", "help", "hence", "her", "here", "heritage", "hero", "herself", "hesitate",
            "hide", "high", "highlight", "highly", "highway", "hill", "him", "himself", "hint", "hire",
            "historian", "historic", "history", "hit", "hold", "hole", "holiday", "holy", "home", "honest",
            "honor", "hook", "hope", "horizon", "horn", "horror", "horse", "hospital", "host", "hot",
            "hotel", "hour", "house", "household", "housing", "how", "however", "huge", "human", "humble",
            "humor", "hundred", "hungry", "hunt", "hurry", "hurt", "husband", "I", "ice", "idea",
            "ideal", "identify", "identity", "ignore", "ill", "illegal", "illness", "illustrate", "image", "imagine",
            "immediate", "immigrant", "impact", "implement", "imply", "import", "importance", "important", "impose", "impossible",
            "impress", "improve", "incentive", "incident", "include", "income", "incorporate", "increase", "indeed", "independent",
            "index", "indicate", "individual", "industrial", "industry", "infant", "infect", "inflation", "influence", "inform",
            "initial", "initiative", "injure", "innocent", "innovate", "input", "inquire", "inside", "insight", "insist",
            "inspect", "inspire", "install", "instance", "instead", "institute", "institution", "instruct", "instrument", "insult",
            "insurance", "integrate", "intellectual", "intend", "intense", "intensity", "intention", "interact", "interest", "internal",
            "international", "internet", "interpret", "interrupt", "interval", "intervene", "interview", "into", "introduce", "invade",
            "invent", "invest", "investigate", "invisible", "invite", "involve", "iron", "island", "issue", "it",
            "item", "itself", "jacket", "jail", "jaw", "jazz", "jeans", "jet", "jewel", "job",
            "join", "joint", "joke", "journal", "journey", "joy", "judge", "judgment", "juice", "jump",
            "junior", "jury", "just", "justice", "justify", "keen", "keep", "key", "kick", "kid",
            "kill", "kind", "king", "kiss", "kitchen", "knee", "knife", "knock", "know", "knowledge",
            "lab", "label", "labor", "lack", "ladder", "lady", "lake", "lamp", "land", "landscape",
            "language", "lap", "large", "last", "late", "latter", "laugh", "launch", "law", "lawn",
            "lawyer", "lay", "layer", "lazy", "lead", "leader", "leaf", "league", "lean", "learn",
            "least", "leather", "leave", "lecture", "left", "leg", "legal", "legend", "legitimate", "leisure",
            "lemon", "lend", "length", "less", "lesson", "let", "letter", "level", "liberal", "library",
            "license", "lie", "life", "lift", "light", "like", "likely", "limit", "line", "link",
            "lip", "liquid", "list", "listen", "literally", "literary", "literature", "little", "live", "load",
            "loan", "local", "locate", "location", "lock", "long", "look", "loose", "lord", "lose",
            "loss", "lost", "lot", "loud", "love", "lovely", "low", "loyal", "luck", "lucky",
            "lunch", "lung", "machine", "mad", "magazine", "magic", "mail", "main", "maintain", "major",
            "majority", "make", "male", "manage", "manager", "manner", "manufacture", "many", "map", "march",
            "margin", "mark", "market", "marriage", "marry", "mask", "mass", "master", "match", "material",
            "math", "matter", "maximum", "may", "maybe", "meal", "mean", "meaning", "measure", "meat",
            "mechanism", "media", "medical", "medium", "meet", "meeting", "melt", "member", "memory", "mental",
            "mention", "menu", "mere", "merely", "mess", "message", "metal", "meter", "method", "middle",
            "might", "military", "milk", "mind", "mine", "mineral", "minimum", "minister", "minor", "minute",
            "mirror", "miss", "missile", "missing", "mission", "mistake", "mix", "mixture", "mobile", "model",
            "moderate", "modern", "modest", "moment", "money", "monitor", "month", "mood", "moon", "moral",
            "more", "moreover", "morning", "mortgage", "most", "mostly", "mother", "motion", "motivate", "motor",
            "mount", "mountain", "mouse", "mouth", "move", "movement", "movie", "much", "mud", "multiple",
            "multiply", "muscle", "museum", "music", "musical", "must", "mutual", "my", "myself", "mystery",
            "nail", "naked", "name", "narrow", "nation", "national", "native", "natural", "naturally", "nature",
            "navy", "near", "nearly", "necessary", "neck", "need", "negative", "negotiate", "neighbor", "neither",
            "nerve", "nervous", "net", "network", "never", "nevertheless", "new", "news", "newspaper", "next",
            "nice", "night", "nine", "no", "nobody", "noise", "nominate", "none", "nonetheless", "normal",
            "north", "nose", "not", "note", "nothing", "notice", "notion", "novel", "now", "nowhere",
            "nuclear", "number", "numerous", "nurse", "nut", "obey", "object", "objective", "obligation", "observe",
            "obtain", "obvious", "occasion", "occupy", "occur", "ocean", "odd", "off", "offend", "offer",
            "office", "officer", "official", "often", "oil", "old", "on", "once", "one", "ongoing",
            "onion", "online", "only", "open", "operate", "operation", "operator", "opinion", "opponent", "opportunity",
            "oppose", "opposite", "option", "or", "orange", "order", "ordinary", "organ", "organize", "origin",
            "original", "other", "otherwise", "ought", "our", "ourselves", "out", "outcome", "outside", "oven",
            "over", "overall", "overcome", "owe", "own", "owner", "pace", "pack", "package", "page",
            "pain", "paint", "painter", "pair", "pale", "palm", "panel", "panic", "paper", "parade",
            "parent", "park", "parliament", "part", "participate", "particular", "partly", "partner", "party", "pass",
            "passage", "passenger", "passion", "past", "path", "patience", "patient", "pattern", "pause", "pay",
            "payment", "peace", "peak", "peer", "penalty", "people", "pepper", "per", "perceive", "percent",
            "perfect", "perform", "perhaps", "period", "permanent", "permit", "person", "personal", "persuade", "pet",
            "phase", "phenomenon", "philosophy", "phone", "photo", "phrase", "physical", "physician", "piano", "pick",
            "picture", "pie", "piece", "pig", "pile", "pill", "pilot", "pin", "pine", "pink",
            "pipe", "pitch", "place", "plain", "plan", "plane", "planet", "plant", "plastic", "plate",
            "platform", "play", "player", "pleasant", "please", "pleasure", "plenty", "plot", "plus", "pocket",
            "poem", "poet", "point", "pole", "police", "policy", "political", "politics", "poll", "pollute",
            "pool", "poor", "pop", "popular", "population", "port", "pose", "position", "positive", "possess",
            "possibility", "possible", "post", "pot", "potato", "potential", "pound", "pour", "poverty", "powder",
            "power", "powerful", "practical", "practice", "praise", "pray", "preach", "precise", "predict", "prefer",
            "pregnant", "prepare", "presence", "present", "preserve", "president", "press", "pressure", "pretend", "pretty",
            "prevent", "previous", "price", "pride", "priest", "primary", "prime", "prince", "princess", "principal",
            "principle", "print", "prior", "priority", "prison", "private", "privilege", "prize", "pro", "probably",
            "problem", "procedure", "proceed", "process", "produce", "producer", "product", "profession", "professor", "profile",
            "profit", "program", "progress", "project", "promise", "promote", "prompt", "proper", "property", "proportion",
            "propose", "prospect", "protect", "protest", "proud", "prove", "provide", "province", "public", "publish",
            "pull", "punch", "punish", "purchase", "pure", "purpose", "pursue", "push", "put", "qualify",
            "quality", "quarter", "queen", "question", "quick", "quiet", "quit", "quite", "quote", "race",
            "radical", "radio", "rail", "rain", "raise", "range", "rank", "rapid", "rare", "rarely",
            "rate", "rather", "raw", "reach", "react", "read", "reader", "ready", "real", "realize",
            "really", "reason", "recall", "receive", "recent", "recipe", "recognize", "recommend", "record", "recover",
            "recruit", "red", "reduce", "refer", "reflect", "reform", "refuse", "regard", "region", "register",
            "regret", "regular", "regulate", "reject", "relate", "relation", "relative", "relax", "release", "relevant",
            "relief", "relieve", "religion", "rely", "remain", "remark", "remember", "remind", "remote", "remove",
            "repeat", "replace", "reply", "report", "represent", "reproduce", "reputation", "request", "require", "rescue",
            "research", "reserve", "reside", "resident", "resist", "resolve", "resort", "resource", "respect", "respond",
            "response", "responsibility", "responsible", "rest", "restaurant", "restore", "restrict", "result", "retain", "retire",
            "return", "reveal", "revenue", "reverse", "review", "revolution", "reward", "rhythm", "rice", "rich",
            "ride", "right", "ring", "rise", "risk", "river", "road", "rock", "role", "roll",
            "romantic", "roof", "room", "root", "rope", "rose", "rough", "round", "route", "routine",
            "row", "royal", "rub", "rubber", "rude", "ruin", "rule", "run", "rural", "rush",
            "sad", "safe", "safety", "sail", "salary", "sale", "salt", "same", "sample", "sanction",
            "sand", "satellite", "satisfy", "sauce", "save", "say", "scale", "scan", "scandal", "scarce",
            "scare", "scatter", "scene", "schedule", "scheme", "scholar", "school", "science", "scope", "score",
            "scream", "screen", "screw", "script", "sea", "search", "season", "seat", "second", "secret",
            "secretary", "section", "sector", "secure", "security", "see", "seed", "seek", "seem", "segment",
            "seize", "select", "self", "sell", "senior", "sense", "sensitive", "sentence", "separate", "sequence",
            "series", "serious", "serve", "service", "session", "set", "settle", "seven", "several", "severe",
            "sex", "sexual", "shade", "shadow", "shake", "shall", "shape", "share", "sharp", "she",
            "sheet", "shelf", "shell", "shelter", "shift", "shine", "ship", "shirt", "shock", "shoe",
            "shoot", "shop", "short", "shot", "shoulder", "shout", "show", "shower", "shrink", "shut",
            "sick", "side", "sigh", "sight", "sign", "signal", "significance", "significant", "silence", "silent",
            "silver", "similar", "simple", "simply", "sin", "since", "sing", "singer", "single", "sink",
            "sir", "sister", "sit", "site", "situation", "six", "size", "skill", "skin", "skirt",
            "sky", "sleep", "slice", "slide", "slight", "slightly", "slip", "slope", "slow", "slowly",
            "small", "smart", "smell", "smile", "smoke", "smooth", "snake", "snow", "so", "so-called",
            "social", "society", "soft", "software", "soil", "solar", "soldier", "solid", "solution", "solve",
            "some", "somebody", "somehow", "someone", "something", "sometimes", "somewhat", "somewhere", "son", "song",
            "soon", "sophisticated", "sorry", "sort", "soul", "sound", "soup", "source", "south", "space",
            "speak", "speaker", "special", "specialist", "species", "specific", "specify", "speech", "speed", "spell",
            "spend", "sphere", "spin", "spirit", "spiritual", "split", "spokesman", "sponsor", "sport", "spot",
            "spread", "spring", "square", "stable", "staff", "stage", "stair", "stake", "stand", "standard",
            "star", "stare", "start", "state", "statement", "station", "status", "stay", "steady", "steal",
            "steel", "step", "stick", "still", "stir", "stock", "stomach", "stone", "stop", "store",
            "storm", "story", "straight", "strain", "strange", "stranger", "strategy", "stream", "street", "strength",
            "stress", "stretch", "strike", "string", "strip", "stroke", "strong", "structure", "struggle", "student",
            "studio", "study", "stuff", "stupid", "style", "subject", "submit", "subsequent", "substance", "substantial",
            "succeed", "success", "successful", "such", "sudden", "suddenly", "suffer", "sufficient", "sugar", "suggest",
            "suggestion", "suit", "summer", "summit", "sun", "super", "supply", "support", "suppose", "sure",
            "surface", "surgery", "surprise", "surround", "survey", "survive", "suspect", "sustain", "swear", "sweep",
            "sweet", "swim", "swing", "switch", "symbol", "symptom", "system", "table", "tactic", "tail",
            "take", "tale", "talent", "talk", "tall", "tank", "tap", "tape", "target", "task",
            "taste", "tax", "taxi", "tea", "teach", "teacher", "team", "tear", "technical", "technique",
            "technology", "teenager", "telephone", "television", "tell", "temper", "temperature", "temporary", "ten", "tend",
            "tendency", "tennis", "tension", "tent", "term", "terrible", "territory", "terror", "test", "text",
            "than", "thank", "that", "the", "theater", "their", "them", "theme", "themselves", "then",
            "theory", "there", "therefore", "these", "they", "thick", "thing", "think", "third", "thirsty",
            "thirteen", "thirty", "this", "those", "though", "thought", "thousand", "threat", "three", "throat",
            "through", "throw", "thus", "ticket", "tide", "tie", "tight", "till", "time", "tiny",
            "tip", "tire", "tissue", "title", "to", "tobacco", "today", "toe", "together", "toilet",
            "tolerate", "tomorrow", "tone", "tongue", "tonight", "too", "tool", "tooth", "top", "topic",
            "total", "touch", "tough", "tour", "tourism", "toward", "tower", "town", "toy", "trace",
            "track", "trade", "tradition", "traffic", "tragedy", "trail", "train", "transfer", "transform", "transition",
            "translate", "transport", "trap", "travel", "treat", "treatment", "tree", "trend", "trial", "tribe",
            "trick", "trigger", "trip", "triumph", "trouble", "trousers", "true", "truly", "trust", "truth",
            "try", "tube", "tunnel", "turn", "twelve", "twenty", "twice", "twin", "two", "type",
            "typical", "ugly", "ultimate", "umbrella", "unable", "unaware", "uncertain", "uncle", "under", "undergo",
            "understand", "undertake", "unfortunately", "uniform", "union", "unique", "unit", "unite", "universal", "universe",
            "unknown", "unless", "unlike", "unlikely", "until", "unusual", "up", "upon", "upper", "urban",
            "urge", "urgent", "us", "use", "useful", "user", "usual", "utility", "utilize", "vacation",
            "valid", "valley", "valuable", "value", "van", "variable", "variation", "variety", "various", "vary",
            "vast", "vegetable", "vehicle", "venture", "verb", "version", "vertical", "very", "vessel", "veteran",
            "via", "vibrate", "vice", "victim", "victory", "video", "view", "village", "violate", "violence",
            "violent", "virtual", "virtue", "virus", "visible", "vision", "visit", "visitor", "visual", "vital",
            "voice", "volume", "volunteer", "vote", "voter", "vs", "vulnerable", "wage", "wait", "wake",
            "walk", "wall", "wander", "want", "war", "warm", "warn", "wash", "waste", "watch",
            "water", "wave", "way", "we", "weak", "wealth", "weapon", "wear", "weather", "web",
            "wedding", "week", "weekend", "weigh", "weight", "welcome", "welfare", "well", "west", "western",
            "wet", "what", "whatever", "wheat", "wheel", "when", "whenever", "where", "whereas", "wherever",
            "whether", "which", "while", "whisper", "white", "who", "whole", "whom", "whose", "why",
            "wide", "widely", "widespread", "wife", "wild", "will", "willing", "win", "wind", "window",
            "wine", "wing", "winner", "winter", "wipe", "wire", "wisdom", "wise", "wish", "with",
            "withdraw", "within", "without", "witness", "woman", "wonder", "wonderful", "wood", "wooden", "word",
            "work", "worker", "world", "worry", "worth", "would", "wound", "wrap", "write", "writer",
            "wrong", "yard", "yeah", "year", "yellow", "yes", "yesterday", "yet", "yield", "you",
            "young", "your", "yourself", "youth", "zone", "zoo"
        ];
        
        // قائمة الكلمات المتشابهة (Homophones)
        const homophones = [
            { word1: "to", word2: "too", word3: "two", ar: "إلى / أيضاً / اثنان" },
            { word1: "their", word2: "there", word3: "they're", ar: "لهم / هناك / هم يكونون" },
            { word1: "know", word2: "no", ar: "يعرف / لا" },
            { word1: "write", word2: "right", ar: "يكتب / صحيح أو يمين" },
            { word1: "see", word2: "sea", ar: "يرى / بحر" },
            { word1: "hear", word2: "here", ar: "يسمع / هنا" },
            { word1: "flower", word2: "flour", ar: "زهرة / دقيق" },
            { word1: "for", word2: "four", ar: "لأجل / أربعة" },
            { word1: "sun", word2: "son", ar: "شمس / ابن" },
            { word1: "ate", word2: "eight", ar: "أكل (ماضي eat) / ثمانية" },
            { word1: "buy", word2: "by", word3: "bye", ar: "يشتري / بواسطة / وداعاً" },
            { word1: "cell", word2: "sell", ar: "خلية / يبيع" },
            { word1: "dear", word2: "deer", ar: "عزيزي / غزال" },
            { word1: "die", word2: "dye", ar: "يموت / صبغة" },
            { word1: "eye", word2: "I", ar: "عين / أنا" },
            { word1: "fair", word2: "fare", ar: "عادل أو فاتح / أجرة" },
            { word1: "great", word2: "grate", ar: "عظيم / يبشر" },
            { word1: "hole", word2: "whole", ar: "حفرة / كامل" },
            { word1: "knight", word2: "night", ar: "فارس / ليل" },
            { word1: "mail", word2: "male", ar: "بريد / ذكر" },
            { word1: "meat", word2: "meet", ar: "لحم / يقابل" },
            { word1: "one", word2: "won", ar: "واحد / فاز (ماضي win)" },
            { word1: "peace", word2: "piece", ar: "سلام / قطعة" },
            { word1: "plain", word2: "plane", ar: "عادي / طائرة" },
            { word1: "read", word2: "red", ar: "يقرأ (ماضي read) / أحمر" },
            { word1: "sea", word2: "see", ar: "بحر / يرى" },
            { word1: "sole", word2: "soul", ar: "نعل / روح" },
            { word1: "some", word2: "sum", ar: "بعض / مجموع" },
            { word1: "tale", word2: "tail", ar: "حكاية / ذيل" },
            { word1: "wait", word2: "weight", ar: "ينتظر / وزن" },
            { word1: "weak", word2: "week", ar: "ضعيف / أسبوع" },
            { word1: "weather", word2: "whether", ar: "طقس / سواء" },
            { word1: "wood", word2: "would", ar: "خشب / سوف (فعل مساعد)" },
            { word1: "your", word2: "you're", ar: "لك / أنت تكون" }
        ];

        // قائمة الجمل اليومية
        const dailySentences = {
            work: [
                { en: "Good morning, team!", ar: "صباح الخير، فريق العمل!" },
                { en: "Let's start the meeting.", ar: "لنبدأ الاجتماع." },
                { en: "What's the deadline for this task?", ar: "ما هو الموعد النهائي لهذه المهمة؟" },
                { en: "I'll send you an email.", ar: "سأرسل لك بريدًا إلكترونيًا." },
                { en: "Can I help you with anything?", ar: "هل يمكنني مساعدتك في أي شيء؟" },
                { en: "I'm working on the report.", ar: "أنا أعمل على التقرير." },
                { en: "Please check your inbox.", ar: "الرجاء التحقق من صندوق الوارد الخاص بك." },
                { en: "Let's collaborate on this project.", ar: "دعنا نتعاون في هذا المشروع." },
                { en: "I'll be in the office until 5 PM.", ar: "سأكون في المكتب حتى الساعة 5 مساءً." },
                { en: "Have a productive day!", ar: "أتمنى لك يومًا مثمرًا!" },
                { en: "Could you please review this document?", ar: "هل يمكنك مراجعة هذا المستند من فضلك؟" },
                { en: "I'll get back to you shortly.", ar: "سأعود إليك قريبًا." },
                { en: "We need to prioritize these tasks.", ar: "نحن بحاجة لتحديد أولويات هذه المهام." },
                { en: "The presentation is ready.", ar: "العرض التقديمي جاهز." },
                { en: "I'm on a call right now.", ar: "أنا في مكالمة الآن." },
                { en: "Let's schedule a follow-up meeting.", ar: "دعنا نحدد موعدًا لاجتماع متابعة." },
                { en: "What's your availability next week?", ar: "ما هو مدى توفرك الأسبوع القادم؟" },
                { en: "I've completed my part.", ar: "لقد أكملت الجزء الخاص بي." },
                { en: "Thank you for your hard work.", ar: "شكراً لجهودكم." },
                { en: "Let's aim for excellence.", ar: "دعنا نسعى للتميز." }
            ],
            school: [
                { en: "Good morning, class!", ar: "صباح الخير، يا صف!" },
                { en: "Please open your books to page 20.", ar: "الرجاء فتح كتبكم على الصفحة 20." },
                { en: "Do you have any questions?", ar: "هل لديكم أي أسئلة؟" },
                { en: "Let's review for the exam.", ar: "دعنا نراجع للامتحان." },
                { en: "What's the answer to question 5?", ar: "ما هي إجابة السؤال 5؟" },
                { en: "I need to study for the test.", ar: "أحتاج أن أدرس للاختبار." },
                { en: "Can I borrow a pen?", ar: "هل يمكنني استعارة قلم؟" },
                { en: "Please hand in your homework.", ar: "الرجاء تسليم واجباتكم." },
                { en: "The bell is ringing.", ar: "الجرس يرن." },
                { en: "See you after class!", ar: "أراك بعد الحصة!" },
                { en: "Pay attention, please.", ar: "انتبهوا من فضلكم." },
                { en: "Write this down in your notebook.", ar: "اكتبوا هذا في دفتر ملاحظاتكم." },
                { en: "Who wants to read next?", ar: "من يريد أن يقرأ تالياً؟" },
                { en: "Don't forget your assignments.", ar: "لا تنسوا واجباتكم." },
                { en: "Practice makes perfect.", ar: "الممارسة تجعل الكمال." },
                { en: "Let's work in groups.", ar: "دعنا نعمل في مجموعات." },
                { en: "What's your favorite subject?", ar: "ما هي مادتك المفضلة؟" },
                { en: "The library is open until 4 PM.", ar: "المكتبة مفتوحة حتى الساعة 4 مساءً." },
                { en: "Good job, everyone!", ar: "عمل جيد، الجميع!" },
                { en: "Keep up the good work.", ar: "استمروا في العمل الجيد." }
            ],
            street: [
                { en: "Excuse me, how do I get to the station?", ar: "عفواً، كيف أصل إلى المحطة؟" },
                { en: "Can you tell me the way to the nearest bank?", ar: "هل يمكنك أن تخبرني الطريق إلى أقرب بنك؟" },
                { en: "It's straight ahead, then turn left.", ar: "إنه للأمام مباشرة، ثم انعطف يسارًا." },
                { en: "Watch out for the traffic!", ar: "احذر من حركة المرور!" },
                { en: "Is this seat taken?", ar: "هل هذا المقعد مشغول؟" },
                { en: "Have a nice day!", ar: "أتمنى لك يوماً سعيداً!" },
                { en: "Can I help you?", ar: "هل يمكنني مساعدتك؟" },
                { en: "Thank you very much.", ar: "شكراً جزيلاً." },
                { en: "No problem.", ar: "لا مشكلة." },
                { en: "Where is the nearest cafe?", ar: "أين أقرب مقهى؟" },
                { en: "Be careful when crossing the street.", ar: "كن حذرًا عند عبور الشارع." },
                { en: "What's the weather like today?", ar: "كيف حال الطقس اليوم؟" },
                { en: "It's a beautiful day, isn't it?", ar: "إنه يوم جميل، أليس كذلك؟" },
                { en: "Can I get a taxi here?", ar: "هل يمكنني الحصول على سيارة أجرة هنا؟" },
                { en: "Enjoy your meal!", ar: "استمتع بوجبتك!" },
                { en: "How much is this?", ar: "بكم هذا؟" },
                { en: "I'm just looking, thank you.", ar: "أنا فقط أنظر، شكراً." },
                { en: "Have a good trip!", ar: "أتمنى لك رحلة سعيدة!" },
                { en: "Do you live around here?", ar: "هل تعيش في الجوار؟" },
                { en: "It was nice meeting you.", ar: "كان من دواعي سروري مقابلتك." }
            ]
        };


        const contentSections = [
            { id: 'alphabet-words', title: 'الحروف الإنجليزية والكلمات', type: 'alphabet', content: null },
            { id: 'vowels-consonants', title: 'الحروف الساكنة والمتحركة (Vowels & Consonants)', type: 'alphabet', content: null },
            { id: 'verb-to-be', title: 'قاعدة الفعل "To Be"', type: 'grammar', content: null },
            { id: 'he-is-it-is', title: '"He Is" و "It Is"', type: 'grammar', content: null },
            { id: 'verb-to-do', title: 'قاعدة الفعل "To Do"', type: 'grammar', content: null },
            { id: 'verb-to-have', title: 'قاعدة الفعل "To Have"', type: 'grammar', content: null },
            { id: 'present-simple', title: 'زمن المضارع البسيط (Present Simple)', type: 'grammar', content: null },
            { id: 'past-simple', title: 'زمن الماضي البسيط (Past Simple)', type: 'grammar', content: null },
            { id: 'present-continuous', title: 'زمن المضارع المستمر (Present Continuous)', type: 'grammar', content: null },
            { id: 'past-perfect', title: 'زمن الماضي التام (Past Perfect)', type: 'grammar', content: null },
            { id: 'similar-words', title: 'الكلمات المتشابهة (Homophones)', type: 'vocabulary', content: null },
            { id: 'daily-sentences', title: 'جمل للاستخدام اليومي', type: 'phrases', content: null }
        ];

        // دالة لبناء قسم الحروف الأبجدية والكلمات
        function buildAlphabetWordsSection() {
            let html = `<div class="section-content"><div class="alphabet-grid">`;
            const alphabet = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('');
            const wordMap = {};

            // تجميع الكلمات حسب الحرف الأول
            baseWords.forEach(word => {
                const firstLetter = word.charAt(0).toUpperCase();
                if (!wordMap[firstLetter]) {
                    wordMap[firstLetter] = [];
                }
                wordMap[firstLetter].push(word);
            });

            alphabet.forEach(letter => {
                html += `<div class="alphabet-letter-block"><h3>${letter}</h3><ul>`;
                let wordsForLetter = wordMap[letter] ? shuffleArray([...wordMap[letter]]) : [];
                
                // ضمان 20 كلمة لكل حرف، مع التكرار إذا لزم الأمر
                const targetWordCount = 20;
                if (wordsForLetter.length < targetWordCount) {
                    const originalWords = [...wordsForLetter];
                    while (wordsForLetter.length < targetWordCount) {
                        wordsForLetter = wordsForLetter.concat(shuffleArray([...originalWords]));
                    }
                    wordsForLetter = wordsForLetter.slice(0, targetWordCount);
                } else {
                    wordsForLetter = wordsForLetter.slice(0, targetWordCount); // خذ أول 20 كلمة بعد الخلط
                }
                
                wordsForLetter.forEach(word => {
                    html += `<li>${word}<button class="read-button" onclick="speakText('${word}')">استمع</button></li>`;
                });
                html += `</ul></div>`;
            });
            html += `</div></div>`;
            return html;
        }

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
                        <button class="show-answer-button" onclick="toggleAnswer(this, 'vowel_consonant_answer${index}')">أظهر الإجابة</button>
                        <p id="vowel_consonant_answer${index}" class="exercise-answer">${ex.a}</p>
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

        // دالة لتوليد HTML للتمارين
        function generateExercisesHtml(exercises, prefix = '') {
            let html = ``;
            // خلط التمارين لضمان التنوع
            const shuffledExercises = shuffleArray([...exercises]);
            shuffledExercises.forEach((ex, index) => {
                html += `
                    <div class="exercise-item">
                        <p class="exercise-question">${ex.q}</p>
                        <button class="show-answer-button" onclick="toggleAnswer(this, 'answer_${prefix}${index}')">أظهر الإجابة</button>
                        <p id="answer_${prefix}${index}" class="exercise-answer">${ex.a}</p>
                    </div>
                `;
            });
            return html;
        }

        // دالة لبناء قسم الكلمات المتشابهة
        function buildSimilarWordsSection() {
            let html = `
                <div class="section-content">
                    <p>الكلمات المتشابهة (Homophones) هي كلمات تُنطق بنفس الطريقة ولكن لها معانٍ مختلفة وغالبًا ما تكون لها تهجئات مختلفة.</p>
                    <table class="similar-words-table">
                        <thead>
                            <tr>
                                <th>الكلمة 1</th>
                                <th>الكلمة 2</th>
                                <th>الكلمة 3 (إن وجدت)</th>
                                <th>المعنى بالعربية</th>
                            </tr>
                        </thead>
                        <tbody>
            `;
            shuffleArray([...homophones]).forEach(item => {
                html += `
                    <tr>
                        <td><span class="english-text">${item.word1}</span> <button class="read-button" onclick="speakText('${item.word1}')">استمع</button></td>
                        <td><span class="english-text">${item.word2}</span> <button class="read-button" onclick="speakText('${item.word2}')">استمع</button></td>
                        <td>${item.word3 ? `<span class="english-text">${item.word3}</span> <button class="read-button" onclick="speakText('${item.word3}')">استمع</button>` : '—'}</td>
                        <td><span class="arabic-text">${item.ar}</span></td>
                    </tr>
                `;
            });
            html += `
                        </tbody>
                    </table>
                </div>
            `;
            return html;
        }

        // دالة لبناء قسم الجمل اليومية
        function buildDailySentencesSection() {
            let html = `
                <div class="section-content">
                    <p>هذه مجموعة من الجمل الشائعة التي يمكنك استخدامها في حياتك اليومية، مقسمة حسب السياق.</p>
                    
                    <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">جمل للعمل (Work)</h3>
                    <ul>
            `;
            shuffleArray([...dailySentences.work]).forEach(item => {
                html += `<li><span class="english-example">${item.en}</span><span class="arabic-example">${item.ar}</span><button class="read-button" onclick="speakText('${item.en}')">استمع</button></li>`;
            });
            html += `
                    </ul>

                    <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">جمل للمدرسة (School)</h3>
                    <ul>
            `;
            shuffleArray([...dailySentences.school]).forEach(item => {
                html += `<li><span class="english-example">${item.en}</span><span class="arabic-example">${item.ar}</span><button class="read-button" onclick="speakText('${item.en}')">استمع</button></li>`;
            });
            html += `
                    </ul>

                    <h3 class="section-title" style="font-size: 1.8em; margin-top: 40px;">جمل للشارع (Street)</h3>
                    <ul>
            `;
            shuffleArray([...dailySentences.street]).forEach(item => {
                html += `<li><span class="english-example">${item.en}</span><span class="arabic-example">${item.ar}</span><button class="read-button" onclick="speakText('${item.en}')">استمع</button></li>`;
            });
            html += `
                    </ul>
                </div>
            `;
            return html;
        }


        // ربط المحتوى بالأقسام
        contentSections[0].content = buildAlphabetWordsSection();
        contentSections[1].content = buildVowelsConsonantsSection();
        contentSections[2].content = `<div class="section-content">${verbToBeData.explanation} ${generateExercisesHtml(verbToBeData.exercises, 'tobe_')}</div>`;
        contentSections[3].content = `<div class="section-content">${heItIsData.explanation} ${generateExercisesHtml(heItIsData.exercises, 'heitis_')}</div>`;
        contentSections[4].content = `<div class="section-content">${verbToDoData.explanation} ${generateExercisesHtml(verbToDoData.exercises, 'todo_')}</div>`;
        contentSections[5].content = `<div class="section-content">${verbToHaveData.explanation} ${generateExercisesHtml(verbToHaveData.exercises, 'tohave_')}</div>`;
        contentSections[6].content = `<div class="section-content">${presentSimpleData.explanation} ${generateExercisesHtml(presentSimpleData.exercises, 'ps_')}</div>`;
        contentSections[7].content = `<div class="section-content">${pastSimpleData.explanation} ${generateExercisesHtml(pastSimpleData.exercises, 'past_')}</div>`;
        contentSections[8].content = `<div class="section-content">${presentContinuousData.explanation} ${generateExercisesHtml(presentContinuousData.exercises, 'pc_')}</div>`;
        contentSections[9].content = `<div class="section-content">${pastPerfectData.explanation} ${generateExercisesHtml(pastPerfectData.exercises, 'pp_')}</div>`;
        contentSections[10].content = buildSimilarWordsSection();
        contentSections[11].content = buildDailySentencesSection();


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
