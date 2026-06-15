<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>my cutie Birthday ❤️</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: 'Georgia', serif;
}

body{
    background:linear-gradient(135deg,#fce4ec,#ffe0e0);
    display:flex;
    justify-content:center;
    align-items:center;
    min-height:100vh;
    overflow:hidden;
}

/* First Paper */

.paper{
    width:260px;
    height:260px;
    position:relative;
    cursor:pointer;
    animation:float 3s ease-in-out infinite;
}

.triangle{
    position:absolute;
    width:50%;
    height:50%;
    background:#e8d5c4;
    border:1px solid #b89d88;
    transition:2s;
}

.top{
    top:0;
    left:25%;
    clip-path:polygon(50% 0%,100% 100%,0% 100%);
    transform-origin:bottom;
}

.left{
    left:0;
    top:25%;
    clip-path:polygon(0% 50%,100% 0%,100% 100%);
    transform-origin:right;
}

.right{
    right:0;
    top:25%;
    clip-path:polygon(100% 50%,0% 0%,0% 100%);
    transform-origin:left;
}

.bottom{
    bottom:0;
    left:25%;
    clip-path:polygon(50% 100%,100% 0%,0% 0%);
    transform-origin:top;
}

.heart{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    font-size:55px;
}

.paper.open .top{
    transform:rotateX(-180deg);
}

.paper.open .left{
    transform:rotateY(-180deg);
}

.paper.open .right{
    transform:rotateY(180deg);
}

.paper.open .bottom{
    transform:rotateX(180deg);
}

@keyframes float{
    0%,100%{transform:translateY(0);}
    50%{transform:translateY(-10px);}
}

/* Letter */

.letter{
    position:absolute;
    width:90%;
    max-width:400px;
    background:#f5e6c8;
    padding:25px;
    border-radius:15px;
    text-align:center;
    display:none;
    animation:fade 2s forwards;
    box-shadow:0 10px 30px rgba(0,0,0,0.2);
}

@keyframes fade{
    from{
        opacity:0;
        transform:scale(0.7);
    }
    to{
        opacity:1;
        transform:scale(1);
    }
}

h1{
    color:#7b2d26;
    margin-bottom:20px;
}

.rose{
    font-size:70px;
    margin:15px 0;
}

p{
    color:#5a3d2b;
    line-height:1.8;
    font-size:18px;
}
</style>
</head>

<body>

<!-- Opening Paper -->
<div class="paper" onclick="openLetter()" id="paper">

    <div class="triangle top"></div>
    <div class="triangle left"></div>
    <div class="triangle right"></div>
    <div class="triangle bottom"></div>

    <div class="heart">❤️</div>

</div>

<!-- Letter -->
<div class="letter" id="letter">

    <h1>DEAR BESTIE</h1>

    <div class="rose">🌹</div>

    <p>
        Dear Anjali,<br><br>

        Tum meri jann se bhi jyada pyari dost ho.
        Main tumhe kabhi khona nahi chahta hu.
        Tum meri life ki sabse khoobsurat dosti ho.
        Chahe hum kitna bhi ladein,
        tum hamesha mere dil ke sabse kareeb rahogi.<br><br>

        Thank you meri life mein aane ke liye.
        Happy Birthday Anjali. ❤️<br><br>

        🎂✨ Hamesha khush rehna meri bestie. ✨🎂
    </p>

</div>

<script>
function openLetter(){
    document.getElementById("paper").classList.add("open");

    setTimeout(()=>{
        document.getElementById("paper").style.display="none";
        document.getElementById("letter").style.display="block";
    },2000);
}
</script>

</body>
</html>
