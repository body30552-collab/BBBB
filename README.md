<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أحلى ذكريات الشلة 🎬</title>
    <style>
        body {
            background-color: #f8f9fa;
            color: #333;
            font-family: 'Segoe UI', Tahoma, sans-serif;
            text-align: center;
            padding: 20px;
            margin: 0;
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        h1 { color: #2d3436; font-size: 1.8rem; }
        .media-box {
            margin: 20px 0;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        video {
            width: 100%;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            background: black; /* عشان لو الفيديو متحملش */
        }
        p.message { font-size: 1.1rem; line-height: 1.7; color: #606770; }
        button {
            background: #00b894;
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 10px;
            font-weight: bold;
            cursor: pointer;
            font-size: 1.1rem;
            margin-top: 15px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>يا منّة.. صافي يا لبن؟ 🤝</h1>
        <p class="message">
            شوفي الفيديوهات دي وافتكري أيامنا الحلوة.. <br>
            عملت لك الصفحة دي مخصوص عشان أقولك إنك صديقة غالية، <br>
            ومش عايزين الزعل يطول أكتر من كدة.
        </p>
        
        <div class="media-box">
            
            <!-- الفيديو الأول -->
            <video controls>
                <source src="WhatsApp Video1.mp4" type="video/mp4">
                متصفحك لا يدعم الفيديو.
            </video>

            <!-- الفيديو الثاني -->
            <video controls>
                <source src="WhatsApp Video2.mp4" type="video/mp4">
                متصفحك لا يدعم الفيديو.
            </video>

            <!-- الفيديو الثالث (الجديد) -->
            <video controls>
                <source src="WhatsApp Video3.mp4" type="video/mp4">
                متصفحك لا يدعم الفيديو.
            </video>

        </div>

        <p class="message"><b>أجدع صديقة والله، ما تبيش قفوشة بقى! ✨</b></p>
        <button onclick="makeConfetti()">خلاص حصل خير 🕊️</button>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
    <script>
        function makeConfetti() {
            confetti({ particleCount: 150, spread: 70, origin: { y: 0.6 } });
            setTimeout(() => { alert('أجدع صديقة في الدنيا والله! ❤️'); }, 500);
        }
    </script>
</body>
</html>
