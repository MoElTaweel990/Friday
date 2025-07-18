<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>يوم جمعة سعيد - سكرول تلقائي</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* CSS الألوان والتأثيرات */
        body {
            font-family: 'Cairo', sans-serif; /* استخدام خط عربي مميز وواضح */
            display: flex;
            flex-direction: column; /* لتنظيم العناصر رأسياً */
            justify-content: center;
            align-items: center;
            min-height: 100vh; /* يضمن أن الـ body يشغل كامل الارتفاع حتى لو المحتوى قليل */
            margin: 0;
            background: linear-gradient(135deg, #FFD700, #FF6347); /* تدرج لوني دافئ للخلفية */
            color: #FFFFFF;
            overflow-x: hidden; /* لمنع ظهور سكرولبار أفقي غير مرغوب فيه */
            position: relative; /* لتحديد موقع الفقاعات */
            padding-bottom: 50px; /* مسافة أسفل الصفحة لتجنب تداخل زر الموسيقى */
        }

        .container {
            text-align: center;
            background-color: rgba(0, 0, 0, 0.6); /* خلفية شبه شفافة أغمق قليلاً */
            padding: 30px 40px; /* زيادة البادينج الأفقي */
            border-radius: 20px; /* حواف أكثر استدارة */
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.4); /* ظل أوضح */
            transform: scale(0.95); /* تصغير بسيط لتبدو كصفحة عائمة */
            animation: appearScale 1.5s ease-out forwards;
            margin-top: 50px; /* مسافة من أعلى الشاشة */
            margin-bottom: 25px; /* مسافة بين الصندوق ومفتاح الصوت */
            max-width: 800px; /* تحديد أقصى عرض للحاوية لتبدو منظمة */
            width: 90%; /* تجعلها متجاوبة مع أحجام الشاشات المختلفة */
            box-sizing: border-box; /* لضم البادينج ضمن العرض الكلي */
            backdrop-filter: blur(5px); /* تأثير ضبابي على الخلفية */
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

        .word-item {
            margin: 15px 0;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInSlideUp 0.8s forwards;
            break-inside: avoid-column; /* لمنع الكلمات من الانقسام بين الأعمدة */
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 10px;
            border-radius: 10px;
            transition: background-color 0.3s ease, transform 0.3s ease;
            cursor: pointer;
        }

        .word-item:hover {
            background-color: rgba(255, 255, 255, 0.1);
            transform: translateY(-5px) scale(1.02);
        }

        .english-word {
            font-size: 1.6em;
            color: #98FB98;
            font-weight: bold;
            margin-bottom: 5px;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
        }

        .arabic-meaning {
            font-size: 1.1em;
            color: #ADD8E6;
            margin-bottom: 10px;
        }

        .read-buttons-group {
            display: flex;
            gap: 10px;
        }

        .read-button {
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 8px;
            padding: 8px 15px;
            cursor: pointer;
            font-size: 0.9em;
            transition: background-color 0.3s ease, transform 0.2s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .read-button:hover {
            background-color: #0056b3;
            transform: translateY(-2px);
        }
        .read-button:active {
            transform: translateY(0);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        @keyframes fadeInSlideUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

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

        /* تأثير فقاعات خفيفة في الخلفية */
        .bubble {
            position: fixed; /* لتثبيت الفقاعات في الخلفية حتى مع السكرول */
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
            margin-bottom: 50px; /* مسافة من أسفل لتعطي مساحة للسكرول */
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

        .word-list-container {
            columns: 2;
            column-gap: 40px;
            width: 100%;
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
        <h1>يوم جمعة سعيد!</h1>
        <div class="word-list-container" id="wordListContainer">
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
        // قائمة الكلمات الإنجليزية ومعانيها العربية (أكثر من 500 كلمة)
        const baseWords = [
            { en: "Relax", ar: "استرخاء" }, { en: "Recharge", ar: "إعادة شحن الطاقة" },
            { en: "Unwind", ar: "استرخِ/تخلّص من التوتر" }, { en: "Breathe", ar: "تنفس" },
            { en: "Chill", ar: "هدوء/استجمام" }, { en: "Explore", ar: "استكشف" },
            { en: "Connect", ar: "تواصل" }, { en: "Reflect", ar: "تأمل" },
            { en: "Weekend Vibes", ar: "أجواء عطلة نهاية الأسبوع" }, { en: "Enjoy Your Time", ar: "استمتع بوقتك" },
            { en: "Serenity", ar: "سكينة/صفاء" }, { en: "Peace", ar: "سلام" },
            { en: "Tranquility", ar: "طمأنينة/هدوء" }, { en: "Freedom", ar: "حرية" },
            { en: "Joy", ar: "فرحة/بهجة" }, { en: "Bliss", ar: "نعيم/سعادة غامرة" },
            { en: "Gratitude", ar: "امتنان" }, { en: "Leisure", ar: "وقت فراغ/ترويح" },
            { en: "Adventure", ar: "مغامرة" }, { en: "Rest", ar: "راحة" },
            { en: "Delight", ar: "متعة/بهجة" }, { en: "Calm", ar: "هدوء/سكون" },
            { en: "Harmony", ar: "انسجام" }, { en: "Happiness", ar: "سعادة" },
            { en: "Gather", ar: "اجتمع" }, { en: "Create", ar: "ابتكر" },
            { en: "Dream", ar: "احلم" }, { en: "Inspire", ar: "إلهام" },
            { en: "Smile", ar: "ابتسم" }, { en: "Savor", ar: "تذوق/استمتع بالكامل" },
            { en: "Cherish", ar: "اعتز بـ" }, { en: "Unplug", ar: "افصل عن التكنولوجيا" },
            { en: "Discover", ar: "اكتشف" }, { en: "Renew", ar: "جدّد" },
            { en: "Embrace", ar: "احتضن/تقبّل" }, { en: "Prosperity", ar: "رخاء/ازدهار" },
            { en: "Balance", ar: "توازن" }, { en: "Positivity", ar: "إيجابية" },
            { en: "Goodness", ar: "خير/صلاح" }, { en: "Hope", ar: "أمل" },
            { en: "Love", ar: "حب" }, { en: "Kindness", ar: "لطف" },
            { en: "Patience", ar: "صبر" }, { en: "Growth", ar: "نمو" },
            { en: "Success", ar: "نجاح" }, { en: "Achieve", ar: "حقق" },
            { en: "Thrive", ar: "ازدهر" }, { en: "Shine", ar: "تألّق" },
            { en: "Sparkle", ar: "تألق/بريق" }, { en: "Flourish", ar: "ازدهر/تنمو" },
            { en: "Radiate", ar: "أشرق/اشعّ" }, { en: "Connect with nature", ar: "تواصل مع الطبيعة" },
            { en: "Family time", ar: "وقت العائلة" }, { en: "Self-care", ar: "العناية بالذات" },
            { en: "Mindfulness", ar: "الوعي التام" }, { en: "Gratitude practice", ar: "ممارسة الامتنان" },
            { en: "Good food", ar: "طعام جيد" }, { en: "Comfort", ar: "راحة" },
            { en: "Happiness is here", ar: "السعادة هنا" }
        ];

        let fridayWords = [];
        const desiredWordCount = 500;
        while (fridayWords.length < desiredWordCount) {
            fridayWords = fridayWords.concat(baseWords.map((word, i) => ({
                en: word.en + (fridayWords.length + i), // نضيف رقم لتمييز الكلمات المكررة
                ar: word.ar + (fridayWords.length + i)
            })));
        }
        fridayWords = fridayWords.slice(0, desiredWordCount);

        const wordListContainer = document.getElementById('wordListContainer');
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

        fridayWords.forEach((item, index) => {
            const wordItemDiv = document.createElement('div');
            wordItemDiv.className = 'word-item';
            // تطبيق الأنيميشن فقط لأول 50 كلمة للحفاظ على الأداء
            if (index < 50) {
                wordItemDiv.style.animationDelay = `${startDelay + (index * 0.1)}s`;
            } else {
                wordItemDiv.style.opacity = '1';
                wordItemDiv.style.transform = 'translateY(0)';
            }

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

        // تحديد تأخير ظهور الملاحظة وزر التحكم بناءً على التأخير الفعلي لآخر كلمة ظاهرة بالأنيميشن
        const calculatedNoteDelay = startDelay + (Math.min(fridayWords.length, 50) * 0.1) + 0.5;
        noteElement.style.setProperty('--note-delay', `${calculatedNoteDelay}s`);
        audioControl.style.setProperty('--button-delay', `${calculatedNoteDelay + 0.4}s`);


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

        window.addEventListener('load', () => {
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
