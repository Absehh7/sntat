<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تسجيل الدخول إلى سنتات</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            direction: rtl;
        }
        .container {
            max-width: 400px;
            margin: 50px auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
        }
        img {
            width: 150px;
            margin-bottom: 15px;
        }
        input, button {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        button {
            background-color: green;
            color: white;
            cursor: pointer;
        }
        #countdown {
            font-size: 20px;
            margin-top: 10px;
            color: red;
            display: none;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>تسجيل الدخول إلى سنتات</h2>
    <img src="https://tgrbah.neocities.org/logosnt.jpg" alt="شعار سنتات">
    <br>
    <input type="text" id="username" placeholder="اسم المستخدم">
    <input type="password" id="password" placeholder="كلمة المرور">
    <button onclick="startCountdown()">تسجيل الدخول</button>
    <p id="countdown">تبقى <span id="time">60</span> ثانية...</p>
</div>

<script>
    function startCountdown() {
        document.getElementById("countdown").style.display = "block";
        let timeLeft = 60;
        let timer = setInterval(function () {
            timeLeft--;
            document.getElementById("time").textContent = timeLeft;
            if (timeLeft <= 0) {
                clearInterval(timer);
                alert("انتهى الوقت! سيتم توجيهك الآن.");
                // يمكنك إعادة توجيه المستخدم لصفحة أخرى بعد انتهاء العد
                // window.location.href = "صفحة_أخرى.html";
            }
        }, 1000);
    }
</script>

</body>
</html>
