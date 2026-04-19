<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بدايتنا ❤️</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div id="login-screen" class="container">
        <div class="heart-box">
            <img src="https://via.placeholder.com/80" alt="Profile" class="profile-img">
            <h2>جاهزة؟ 😉</h2>
            <p>my everything ❤️</p>
            <input type="password" id="password" placeholder="باسورد...">
            <button onclick="checkPassword()">Unlock 🔐</button>
        </div>
    </div>

    <div id="main-content" class="container hidden">
        <div class="card">
            <h1 class="title">بدايتنا ❤️</h1>
            
            <div class="timer-label">سوا من 2026-04-10</div>
            
            <div class="timer">
                <div class="time-box"><span id="days">0</span><p>يوم</p></div>
                <div class="time-box"><span id="hours">0</span><p>ساعة</p></div>
                <div class="time-box"><span id="minutes">0</span><p>دقيقة</p></div>
                <div class="time-box"><span id="seconds">0</span><p>ثانية</p></div>
            </div>
            <p class="subtitle">كل ثانية بتعدي وأنت في قلبي ❤️</p>

            <div class="message-section">
                <div class="msg-card">
                    <p>بحبك بكل حاجة في حياتي، وحقك عليا لو ضايقتك..</p>
                    <p>تعالي نفتكر كل حاجة بينا هنا ونبدأ بداية جديدة</p>
                    <span class="love-text">loveee youuu ❤️</span>
                </div>
            </div>

            <div class="gallery">
                <img src="https://via.placeholder.com/400x500" alt="Memory 1">
                <p class="img-caption">بحبك</p>
                <img src="https://via.placeholder.com/400x500" alt="Memory 2">
                <p class="img-caption">ربنا يخليكي ليا</p>
            </div>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    margin: 0;
    padding: 0;
    background-color: #7d0016; /* لون أحمر داكن مثل الفيديو */
    color: white;
    font-family: 'Arial', sans-serif;
    display: flex;
    justify-content: center;
    min-height: 100vh;
}

.container {
    width: 100%;
    max-width: 450px;
    padding: 20px;
    text-align: center;
}

.hidden { display: none; }

.heart-box {
    margin-top: 50%;
    background: rgba(0, 0, 0, 0.2);
    padding: 30px;
    border-radius: 30px;
    backdrop-filter: blur(5px);
}

.profile-img {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    border: 2px solid #ff4d6d;
}

input {
    width: 80%;
    padding: 12px;
    border-radius: 20px;
    border: none;
    margin: 15px 0;
}

button {
    background-color: #ff4d6d;
    color: white;
    border: none;
    padding: 10px 40px;
    border-radius: 20px;
    cursor: pointer;
    font-weight: bold;
}

.timer {
    display: flex;
    justify-content: space-between;
    margin: 25px 0;
}

.time-box {
    background: rgba(255, 255, 255, 0.1);
    padding: 10px;
    border-radius: 15px;
    flex: 1;
    margin: 0 5px;
}

.time-box span { font-size: 1.8rem; font-weight: bold; display: block; }

.msg-card {
    background: rgba(255, 255, 255, 0.1);
    padding: 20px;
    border-radius: 20px;
    margin: 20px 0;
    line-height: 1.6;
}

.gallery img {
    width: 100%;
    border-radius: 20px;
    margin-top: 15px;
}

.img-caption { margin-top: 5px; font-size: 0.9rem; opacity: 0.8; }
// التاريخ المطلوب: 10 أبريل 2026
const startDate = new Date("April 10, 2026 00:00:00").getTime();

function checkPassword() {
    const pass = document.getElementById("password").value;
    // الباسورد هو love كما في الفيديو
    if (pass.toLowerCase() === "love") {
        document.getElementById("login-screen").style.display = "none";
        document.getElementById("main-content").classList.remove("hidden");
        startTimer();
    } else {
        alert("كلمة السر خطأ!");
    }
}

function startTimer() {
    setInterval(() => {
        const now = new Date().getTime();
        const diff = now - startDate;

        // عرض النتائج في الموقع
        document.getElementById("days").innerText = days;
        document.getElementById("hours").innerText = hours;
        document.getElementById("minutes").innerText = minutes;
        document.getElementById("seconds").innerText = seconds;
    }, 1000);
}
