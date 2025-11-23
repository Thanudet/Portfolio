<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Alien Portfolio - Thanudet</title>

<style>
/* ================= GLOBAL STYLE ================= */
body {
    margin: 0;
    font-family: 'Orbitron', sans-serif;
    background: #02010a;
    color: #fff;
    overflow-x: hidden;
}

/* โหลดฟอนต์ล้ำ ๆ */
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap');

/* ================= STAR BACKGROUND ================= */
.stars {
    width: 2px;
    height: 2px;
    background: white;
    border-radius: 50%;
    position: absolute;
    animation: starMove 10s linear infinite;
}
@keyframes starMove {
    from { transform: translateY(0); }
    to { transform: translateY(100vh); }
}

#star-container {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    z-index: -1;
}

/* ================= HEADER ================= */
header {
    text-align: center;
    padding: 100px 20px;
}

.glitch {
    font-size: 3em;
    font-weight: 700;
    text-transform: uppercase;
    position: relative;
    color: #00eaff;
    animation: glow 2s infinite alternate;
}

@keyframes glow {
    from { text-shadow: 0 0 10px #00eaff; }
    to   { text-shadow: 0 0 25px #04c9ff; }
}

/* ================= UFO ANIMATION ================= */
.ufo {
    position: absolute;
    top: 120px;
    left: -150px;
    width: 120px;
    animation: fly 10s infinite ease-in-out;
}

@keyframes fly {
    0%   { transform: translateX(-200px) translateY(0) rotate(0deg); }
    50%  { transform: translateX(120vw) translateY(40px) rotate(5deg); }
    100% { transform: translateX(-200px) translateY(0) rotate(0deg); }
}

/* ================= SECTIONS ================= */
section {
    padding: 60px 20px;
    max-width: 900px;
    margin: auto;
}

h2 {
    font-size: 2em;
    color: #7df9ff;
    text-shadow: 0 0 10px #7df9ff;
    margin-bottom: 15px;
}

.box {
    background: rgba(255, 255, 255, 0.05);
    padding: 20px;
    border-radius: 12px;
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    animation: floatBox 4s infinite ease-in-out alternate;
}

@keyframes floatBox {
    from { transform: translateY(0); }
    to   { transform: translateY(-8px); }
}

ul li {
    margin: 8px 0;
    padding: 10px;
    background: rgba(0,255,255,0.05);
    border-left: 4px solid #00eaff;
    border-radius: 6px;
}

/* ================= CONTACT ================= */
a {
    color: #00eaff;
    text-decoration: none;
}

a:hover {
    text-shadow: 0 0 10px #00eaff;
}

/* ================= FOOTER ================= */
footer {
    text-align: center;
    padding: 30px;
    margin-top: 40px;
    border-top: 1px solid rgba(255,255,255,0.1);
}
</style>
</head>
<body>

<!-- สุ่มดาว -->
<div id="star-container"></div>

<!-- UFO บิน -->
<img src="https://i.postimg.cc/8C1G6cSY/ufo.png" class="ufo">

<header>
    <h1 class="glitch">Thanudet Kham-auppala</h1>
    <p>ธนูเดช คำอุปละ • Alien-Proof Developer 👽</p>
</header>

<section>
    <h2>👽 เกี่ยวกับฉัน</h2>
    <div class="box">
        <p>สวัสดี! ผม “ธนูเดช คำอุปละ (Thanudet)”  
        นักศึกษาคณะเทคโนโลยีสารสนเทศ สาขาวิชาวิทยาการคอมพิวเตอร์ มหาวิทยาลัยพะเยา</p>

        <p>ผมชอบทำเว็บ ทำแอนิเมชัน และเขียนโค้ดสไตล์เอเลี่ยน ๆ แบบนี้  
        ถ้าโลกโดนบุก — ผมพร้อมเขียนโปรแกรมสู้ครับ 🤣👾</p>
    </div>
</section>

<section>
    <h2>🚀 การศึกษา</h2>
    <div class="box">
        <p>มหาวิทยาลัยพะเยา  
        คณะเทคโนโลยีสารสนเทศ  
        สาขาวิชาวิทยาการคอมพิวเตอร์</p>
    </div>
</section>

<section>
    <h2>🛸 ทักษะ</h2>
    <div class="box">
        <ul>
            <li>HTML, CSS, JavaScript (เขียนเว็บแบบเอเลี่ยนได้)</li>
            <li>Python Programming</li>
            <li>Database & SQL</li>
            <li>Algorithm & Problem Solving ระดับยานแม่</li>
        </ul>
    </div>
</section>

<section>
    <h2>📡 ติดต่อ</h2>
    <div class="box">
        <p>Email: <a href="mailto:67024773@up.ac.th">67024773@up.ac.th</a></p>
    </div>
</section>

<footer>
    © 2025 Thanudet – Protected by Alien Force 👽🛡️
</footer>

<script>
/* สร้างดาวแบบสุ่มให้เต็มท้องฟ้า */
const starContainer = document.getElementById("star-container");

for (let i = 0; i < 150; i++) {
    let s = document.createElement("div");
    s.classList.add("stars");
    s.style.left = Math.random()*100 + "vw";
    s.style.top  = Math.random()*100 + "vh";
    s.style.animationDuration = (Math.random()*5 + 5) + "s";
    starContainer.appendChild(s);
}
</script>

</body>
</html>
