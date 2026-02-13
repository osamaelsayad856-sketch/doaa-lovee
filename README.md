<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>دعاء ♾️ كوتي موتي بوتي</title>

<!-- خط شيك -->
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;600&display=swap" rel="stylesheet">

<style>
body{
    margin:0;
    font-family:'Cairo', sans-serif;
    background: radial-gradient(circle at top,#1e1e2f,#0f0f1a);
    color:white;
    text-align:center;
    overflow-x:hidden;
}

.page{
    display:none;
    padding:80px 20px;
    opacity:0;
    transform:translateY(20px);
    transition:1s ease;
}

.active{
    display:block;
    opacity:1;
    transform:translateY(0);
}

h1{
    font-weight:600;
    font-size:34px;
}

p{
    font-weight:300;
    font-size:20px;
    line-height:1.8;
    max-width:700px;
    margin:auto;
}

button{
    padding:12px 30px;
    font-size:18px;
    border:none;
    border-radius:40px;
    background:linear-gradient(45deg,#ff4b5c,#ff758c);
    color:white;
    cursor:pointer;
    margin-top:40px;
    transition:.4s;
}

button:hover{
    transform:scale(1.1);
    box-shadow:0 10px 25px rgba(255,118,140,.4);
}

img{
    width:260px;
    border-radius:20px;
    margin:15px;
    box-shadow:0 20px 40px rgba(0,0,0,.5);
    transition:.5s;
}

img:hover{
    transform:scale(1.05);
}

#slider{
    display:flex;
    justify-content:center;
    flex-wrap:wrap;
}

.fadeText{
    animation:fadeIn 2s ease forwards;
}

@keyframes fadeIn{
    from{opacity:0;}
    to{opacity:1;}
}

.heart{
    position:fixed;
    bottom:-20px;
    color:#ff4b5c;
    animation:float 6s linear infinite;
}

@keyframes float{
    0%{transform:translateY(0);}
    100%{transform:translateY(-110vh);}
}

#counter{
    margin-top:30px;
    font-size:22px;
}
</style>
</head>
<body>

<audio id="bgMusic" loop>
    <source src="song.mp3" type="audio/mpeg">
</audio>

<!-- الصفحة الأولى -->
<div id="page1" class="page active">
    <h1 class="fadeText">إلى دعاء… ❤️</h1>
    <p class="fadeText">
        من 2021 بدأت قصة مختلفة…  
        قصة فيها أمان، ضحكة، وراحة.  
        قصة اسمها كوتي موتي بوتي.
    </p>
    <button onclick="startLove()">ابدأي الرحلة ♾️</button>
</div>

<!-- الصور -->
<div id="page2" class="page">
    <h1>أجمل لحظاتنا</h1>
    <div id="slider">
        <img src="photo1.jpg">
        <img src="photo2.jpg">
        <img src="photo3.jpg">
    </div>
    <button onclick="nextPage(3)">كمّلي…</button>
</div>

<!-- الرسالة -->
<div id="page3" class="page">
    <h1>رسالة ليكي</h1>
    <p>
        يا دعاء…  
        يمكن مش دايمًا بعرف أقول كل اللي جوايا،  
        بس الحقيقة إن وجودك في حياتي هو أجمل حاجة حصلتلي.  
        <br><br>
        يمكن الناس كلها تناديكي دعاء…  
        بس أنا بس اللي ليا أقولك  
        <strong>كوتي موتي بوتي ❤️</strong>
    </p>
    <button onclick="nextPage(4)">آخر حاجة…</button>
</div>

<!-- الطلب -->
<div id="page4" class="page">
    <h1>تحبي نكمّل بقية عمرنا سوا؟ 💍</h1>
    <button onclick="finalPage()">أيوه ♾️</button>
</div>

<!-- النهاية -->
<div id="page5" class="page">
    <h1>كوتي موتي بوتي للأبد ❤️</h1>
    <div id="counter"></div>
</div>

<script>
function nextPage(page){
    document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
    document.getElementById('page'+page).classList.add('active');
}

function startLove(){
    document.getElementById('bgMusic').play();
    nextPage(2);
}

function finalPage(){
    nextPage(5);
    updateCounter();
}

function updateCounter(){
    const startDate = new Date("2021-01-01");
    const today = new Date();
    const diffTime = today - startDate;
    const days = Math.floor(diffTime / (1000 * 60 * 60 * 24));
    document.getElementById("counter").innerHTML =
    "مرّ على حبنا " + days + " يوم من السعادة ♾️";
}

function createHeart(){
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML="❤";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=Math.random()*25+15+"px";
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),6000);
}
setInterval(createHeart,500);
</script>

</body>
</html>
