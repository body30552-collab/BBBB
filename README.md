<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>رسالة خاصة لمنّة ✨</title>
    <style>
        /* خلفية ناعمة بتدرج ألوان هادي */
        body { 
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%); 
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; 
            text-align: center; 
            margin: 0; 
            padding: 20px; 
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        /* حاوية المحتوى بشكل عصري */
        .container { 
            max-width: 450px; 
            width: 90%;
            background: rgba(255, 255, 255, 0.95); 
            padding: 35px; 
            border-radius: 30px; 
            box-shadow: 0 20px 40px rgba(0,0,0,0.15); 
            border: 1px solid rgba(255,255,255,0.3);
        }

        .step { display: none; animation: fadeIn 0.8s ease; }
        .active { display: block; }

        /* برواز الفيديو الشيك */
        .video-frame {
            padding: 10px;
            background: linear-gradient(45deg, #42b72a, #2ecc71);
            border-radius: 20px;
            margin: 20px 0;
            box-shadow: 0 8px 20px rgba(46, 204, 113, 0.3);
        }

        video { 
            width: 100%; 
            border-radius: 15px; 
            display: block;
            background: #000; 
        }

        h1 { color: #2c3e50; font-size: 1.8rem; margin-bottom: 15px; }
        p { font-size: 1.1rem; color: #576574; line-height: 1.6; font-weight: 500; }

        /* أزرار عصرية */
        button { 
            background: #42b72a; 
            color: white; 
            border: none; 
            padding: 15px 25px; 
            border-radius: 15px; 
            font-size: 1.1rem; 
            font-weight: bold;
            cursor: pointer; 
            transition: all 0.3s ease; 
            width: 100%;
            box-shadow: 0 4px 15px rgba(66, 183, 42, 0.3);
        }

        button:hover { 
            background: #36a420; 
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(66, 183, 42, 0.4);
        }

        /* خانة الباسورد */
        input { 
            width: 100%; 
            padding: 14px; 
            margin: 15px 0; 
            border: 2px solid #eee; 
            border-radius: 15px; 
            text-align: center; 
            font-size: 1.1rem; 
            box-sizing: border-box;
            transition: border-color 0.3s;
        }

        input:focus { border-color: #42b72a; outline: none; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

<div class="container">
    <!-- المرحلة 0: الباسورد -->
    <div id="step0" class="step active">
        <h1>رسالة لمنّة 🌟</h1>
        <p>اكتبي الباسورد عشان تشوفي المفاجأة</p>
        <input type="password" id="passInput" placeholder="كلمة السر هنا..">
        <button onclick="checkPass()">دخول</button>
    </div>

    <!-- المرحلة 1: الفيديو الأول -->
    <div id="step1" class="step">
        <p>أنا آسف  😂😂😂</p>
        <div class="video-frame">
            <video controls><source src="WhatsApp Video1.mp4" type="video/mp4"></video>
        </div>
        <p>أول فيديو عشان نصفي النفوس يا ست منّة</p>
        <button onclick="nextStep(1, 2)">شوفي اللي بعده ✨</button>
    </div>

    <!-- المرحلة 2: الفيديو الثاني -->
    <div id="step2" class="step">
        <p>أنا آسف  😂😂😂</p>
        <div class="video-frame">
            <video controls><source src="WhatsApp Video2.mp4" type="video/mp4"></video>
        </div>
        <p>وده التاني متزعليش.. وبعدين مش لاقي فيديو بصراحة غير دا، أوعي أحمد يشوفه! 🤫</p>
        <button onclick="nextStep(2, 3)">لسه فيه واحد كمان..</button>
    </div>

    <!-- المرحلة 3: الفيديو الثالث -->
    <div id="step3" class="step">
        <p>أنا آسف 😂😂😂</p>
        <div class="video-frame">
            <video controls><source src="WhatsApp Video3.mp4" type="video/mp4"></video>
        </div>
        <p>آخر واحد بقى.. خلاص كدة صافي يا لبن؟</p>
        <button onclick="celebrate()">صالحيني بقى! 🤝</button>
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
<script>
    const CORRECT_PASSWORD = "2006"; 

    function checkPass() {
        const input = document.getElementById('passInput').value;
        if(input.toUpperCase() === CORRECT_PASSWORD) {
            nextStep(0, 1);
        } else {
            alert('الباسورد غلط يا منّة! ركزي 😂');
        }
    }

    function nextStep(current, next) {
        document.getElementById('step' + current).classList.remove('active');
        document.getElementById('step' + next).classList.add('active');
        window.scrollTo(0,0);
    }

    function celebrate() {
        confetti({ 
            particleCount: 150, 
            spread: 70, 
            origin: { y: 0.6 },
            colors: ['#42b72a', '#2ecc71', '#ffffff']
        });
        alert('أجدع صديقة والله! ❤️');
    }
</script>
</body>
</html>
