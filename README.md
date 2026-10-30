<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مفاجأة لنادية 💗</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap');
        
        body {
            background: linear-gradient(135deg, #4a0012, #8b0029);
            color: white;
            font-family: 'Cairo', sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            flex-direction: column;
        }
        .card {
            background: rgba(0, 0, 0, 0.6);
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            width: 90%;
            max-width: 450px;
            margin: 20px 0;
            backdrop-filter: blur(5px);
        }
        input {
            padding: 12px;
            width: 80%;
            border-radius: 20px;
            border: none;
            text-align: center;
            margin: 15px 0;
            font-size: 16px;
            outline: none;
        }
        button {
            background-color: #ff4d79;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 20px;
            cursor: pointer;
            font-size: 16px;
            font-weight: bold;
            transition: 0.3s;
        }
        button:hover {
            background-color: #e60039;
        }
        .love-text {
            font-size: 15px;
            line-height: 1.8;
            text-align: justify;
            text-justify: inter-word;
            padding: 10px;
        }
        .timer-box {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
            margin-top: 20px;
        }
        .time-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px;
            border-radius: 10px;
        }
        .time-num {
            font-size: 18px;
            font-weight: bold;
            color: #ff4d79;
        }
        .time-label {
            font-size: 12px;
        }
        .hidden { display: none; }
    </style>
</head>
<body>

    <!-- شاشة الباسورد -->
    <div class="card" id="login-screen">
        <h2>البسورد هوا تاريخ ارتبطنا🫂💗</h2>
        <input type="password" id="password" placeholder="أدخلي كلمة السر...">
        <br>
        <button onclick="checkPassword()">افتحي قلبي ❤️</button>
    </div>

    <!-- المحتوى الرئيسي -->
    <div class="card hidden" id="main-content">
        <h2>إلى أغلى حاجة في حياتي 💗</h2>
        
        <div class="love-text">
            انتي مش مجرد بنت💗 في حياتي انتي الحياة كلها وانا من أول يوم شوفتك فيه وأنا حاسس إني لقيت💗 الجزء اللي ناقص مني اللي طول عمري بدور عليه انتي اللي غيرتي كل حاجة جوايا خليتيني أحب التفاصيل الصغيرة وأضحك من قلبى لمجرد إنك جنبي كل لحظة معاك بتبقي بالنسبة ليا عمر كامل مليان سعادة أنا عارف إن الدنيا مش دايما سهلة وإن في مشاكل💗 وخناقات بس بجد ولا حاجة تستاهل إني أخسرك فيها لأنك أغلى من أي حاجة وأجمل من أي كلام أنا بحبك بطريقة يمكن عمري ما أعرف أوصفها بس كل اللي أقدر أقوله إنك💗 سبب راحتي وسبب ابتسامتي وإنك أغلى حلم اتحقق في حياتي انتي عارفه ان وجودك 💗في حياتي هو اجمل حاجه حصلتلي من اول يوم عرفتك والدنيا بقت أهدى كده كان ربنا بعتهالي عشان يطمن قلبي انتي الراحه اللي بدور عليها في كل💗 لحظه الحنيه اللي بتنسيني تعب الدنيا كل ما تبعدي بحس اني ناقص نصي كل ما تضحكي بحس ان الدنيا كلها بتضحكلي 💗 بحبك في كل حال في ضحكك وزعلك وصمتك انتي مش مجرد حبيبتي انتي انا بحبك يناديه💗
        </div>

        <hr style="border: 0.5px solid rgba(255,255,255,0.2); margin: 20px 0;">

        <h3>حكايتنا بدأت من هنا 🎀</h3>
        <p style="font-size: 14px; color: #ff80a0;">8 / 3 / 2025</p>
        <p style="font-size: 13px;">الوقت من بداية حكايتنا لحد يوم عيد ميلادك (15/11/2025):</p>

        <!-- العداد الزمني -->
        <div class="timer-box">
            <div class="time-card">
                <div class="time-num" id="days">0</div>
                <div class="time-label">يوم</div>
            </div>
            <div class="time-card">
                <div class="time-num" id="hours">0</div>
                <div class="time-label">ساعة</div>
            </div>
            <div class="time-card">
                <div class="time-num" id="minutes">0</div>
                <div class="time-label">دقيقة</div>
            </div>
            <div class="time-card">
                <div class="time-num" id="seconds">0</div>
                <div class="time-label">ثانية</div>
            </div>
        </div>
    </div>

    <script>
        function checkPassword() {
            const inputPass = document.getElementById('password').value.trim();
            
            // الباسورد المقبول بأكثر من صيغة (8/3/2025 أو 08032025 أو 832025)
            if (inputPass === "8/3/2025" || inputPass === "08032025" || inputPass === "832025") {
                document.getElementById('login-screen').classList.add('hidden');
                document.getElementById('main-content').classList.remove('hidden');
                startTimer();
            } else {جربيربحيحة                alert("كلمة السر غير صحيحة، جربي تاريخ ارتباطنا تاني يا نادية 💗");
            }
        }

        function startTimer() {
            // تاريخ الارتباط: 8 مارس 2025
            const startDate = new Date("2025-03-08T00:00:00");
            // تاريخ عيد الميلاد: 15 نوفمبر 2025
            const endDate = new Date("2025-11-15T00:00:00");

            const diffTime = Math.abs(endDate - startDate);
            
            const totalDays = Math.floor(diffTime / (1000 * 60 * 60 * 24));
            const totalHours = Math.floor((diffTime % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const totalMinutes = Math.floor((diffTime % (1000 * 60 * 60)) / (1000 * 60));
            const totalSeconds = Math.floor((diffTime % (1000 * 60)) / 1000);

            document.getElementById("days").innerText = totalDays;
            document.getElementById("hours").innerText = totalHours;
            document.getElementById("minutes").innerText = totalMinutes;
            document.getElementById("seconds").innerText = totalSeconds;
        }
    </script>
</body>
</html>
