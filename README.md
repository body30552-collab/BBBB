<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>رسالة خاصة لمنّة ✨</title>
    <style>
        body { background: #f0f2f5; font-family: 'Segoe UI', Tahoma, sans-serif; text-align: center; margin: 0; padding: 20px; }
        .container { max-width: 500px; margin: auto; background: white; padding: 30px; border-radius: 20px; box-shadow: 0 10px 25px rgba(0,0,0,0.1); }
        .step { display: none; }
        .active { display: block; }
        video { width: 100%; border-radius: 15px; margin-top: 15px; background: #000; }
        h1 { color: #1c1e21; font-size: 1.8rem; }
        p { font-size: 1.2rem; color: #606770; line-height: 1.6; }
        button { background: #42b72a; color: white; border: none; padding: 12px 25px; border-radius: 10px; font-size: 1.1rem; cursor: pointer; margin-top: 20px; width: 100%; }
        input { width: 90%; padding: 12px; margin-top: 10px; border: 1px solid #ddd; border-radius: 10px; text-align: center; font-size: 1rem; }
    </style>
</head>
<body>

<div class="container">
    <!-- المرحلة 0: الباسورد -->
    <div id="step0" class="step active">
        <h1>رسالة لمنّة 🌟</h1>
        <p>اكتبي الباسورد عشان تشوفي </p>
        <input type="password" id="passInput" placeholder="الباسورد هنا..">
        <button onclick="checkPass()">دخول</button>
    </div>

    <!-- المرحلة 1: الفيديو الأول -->
    <div id="step1" class="step">
        <p>أنا آسف كدا 😂😂😂</p>
        <video controls><source src="WhatsApp Video1.mp4" type="video/mp4"></video>
        <p>أول فيديو عشان نصفي النفوس يا ست منّة</p>
        <button onclick="nextStep(1, 2)">شوفي اللي بعده</button>
    </div>

    <!-- المرحلة 2: الفيديو الثاني -->
    <div id="step2" class="step">
        <p>أنا آسف كدا 😂😂😂</p>
        <video controls><source src="WhatsApp Video2.mp4" type="video/mp4"></video>
        <p>وده التاني متزعليش وبعدين مش لاقي فديو بصراحه غير دا اوعي احمد يشوفه </p>
        <button onclick="nextStep(2, 3)">لسه فيه واحد كمان..</button>
    </div>

    <!-- المرحلة 3: الفيديو الثالث -->
    <div id="step3" class="step">
        <p>أنا آسف كدا 😂😂😂</p>
        <video controls><source src="WhatsApp Video3.mp4" type="video/mp4"></video>
        <p>آخر واحد بقى.. خلاص كدة صافي يا لبن؟</p>
        <button onclick="celebrate()">صالحيني بقى! 🤝</button>
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
<script>
    // الباسورد (تقدر تغيره براحتك)
    const CORRECT_PASSWORD = "MENNA"; 

    function checkPass() {
        const input = document.getElementById('passInput').value;
        if(input === CORRECT_PASSWORD) {
            nextStep(0, 1);
        } else {
            alert('الباسورد غلط!');
        }
    }

    function nextStep(current, next) {
        document.getElementById('step' + current).classList.remove('active');
        document.getElementById('step' + next).classList.add('active');
        window.scrollTo(0,0);
    }

    function celebrate() {
        confetti({ particleCount: 150, spread: 70, origin: { y: 0.6 } });
        alert('أجدع صديقة والله! ❤️');
    }
</script>
</body>
</html>
