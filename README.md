<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Anjali ❤️</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    overflow:hidden;
    height:100vh;
    background:linear-gradient(135deg,#0f0c29,#302b63,#24243e);
    font-family:'Georgia',serif;
}

/* Loading Screen */

.loading-screen{
    position:fixed;
    inset:0;
    background:#000;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    color:white;
    z-index:9999;
    transition:opacity 1.5s;
}

.loading-screen h1{
    font-size:35px;
    letter-spacing:3px;
    margin-bottom:20px;
    text-align:center;
}

.typewriter{
    font-size:18px;
    border-right:2px solid white;
    white-space:nowrap;
    overflow:hidden;
    width:0;
    animation:
      typing 4s steps(40,end) forwards,
      blink .8s infinite;
}

@keyframes typing{
    from{width:0;}
    to{width:300px;}
}

@keyframes blink{
    50%{
        border-color:transparent;
    }
}

/* Main */

.main{
    display:none;
    height:100vh;
    justify-content:center;
    align-items:center;
    position:relative;
}

/* Stars */

.stars{
    position:absolute;
    width:100%;
    height:100%;
}

.star{
    position:absolute;
    width:3px;
    height:3px;
    background:white;
    border-radius:50%;
    animation:twinkle 2s infinite alternate;
}

@keyframes twinkle{
    from{
        opacity:.2;
    }
    to{
        opacity:1;
    }
}

/* Folded Paper */

.paper{
    width:280px;
    height:280px;
    position:relative;
    cursor:pointer;
    animation:float 4s ease-in-out infinite;
}

@keyframes float{
    0%,100%{
        transform:translateY(0);
    }
    50%{
        transform:translateY(-15px);
    }
}

.triangle{
    position:absolute;
    width:50%;
    height:50%;
    background:#ead6c4;
    border:2px solid #b08d72;
    transition:2s ease;
}

.top{
    top:0;
    left:25%;
    clip-path:polygon(50% 0%,100% 100%,0% 100%);
    transform-origin:bottom;
}

.bottom{
    bottom:0;
    left:25%;
    clip-path:polygon(50% 100%,100% 0%,0% 0%);
    transform-origin:top;
}

.left{
    left:0;
    top:25%;
    clip-path
