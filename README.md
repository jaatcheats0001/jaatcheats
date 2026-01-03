<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>JAAT CHEATS | Official Links</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Font Awesome Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:'Poppins', sans-serif;
}

body{
  height:100vh;
  background:#000;
  display:flex;
  align-items:center;
  justify-content:center;
  color:#fff;
  overflow:hidden;
}

/* PARTICLES */
canvas{
  position:fixed;
  inset:0;
  z-index:-1;
}

/* CARD */
.card{
  width:340px;
  background:rgba(255,255,255,0.08);
  border-radius:26px;
  padding:30px 22px;
  backdrop-filter:blur(15px);
  box-shadow:
    0 0 40px rgba(255,0,0,0.35),
    inset 0 0 20px rgba(255,255,255,0.05);
  text-align:center;
}

/* PROFILE */
.profile img{
  width:120px;
  height:120px;
  border-radius:50%;
  border:4px solid #ff2d2d;
  box-shadow:0 0 30px red;
}

/* TEXT */
h1{
  margin-top:18px;
  font-size:26px;
  letter-spacing:1px;
}

.status{
  margin:6px 0 22px;
  color:#00ff6a;
  font-size:14px;
}

/* LINKS */
.links{
  display:flex;
  flex-direction:column;
  gap:14px;
}

.links a{
  padding:14px;
  border-radius:16px;
  text-decoration:none;
  color:white;
  font-size:16px;
  display:flex;
  align-items:center;
  justify-content:center;
  gap:12px;
  transition:0.35s;
  position:relative;
  overflow:hidden;
}

.links a::after{
  content:"";
  position:absolute;
  inset:0;
  background:linear-gradient(120deg, transparent, rgba(255,255,255,0.25), transparent);
  transform:translateX(-100%);
}

.links a:hover::after{
  transform:translateX(100%);
  transition:0.6s;
}

.links a:hover{
  transform:scale(1.08);
  box-shadow:0 0 25px currentColor;
}

/* COLORS */
.yt{background:rgba(255,0,0,0.25); color:#ff3b3b;}
.ig{background:rgba(255,0,200,0.25); color:#ff4fd8;}
.dc{background:rgba(80,120,255,0.25); color:#5b8cff;}
.tg{background:rgba(0,200,255,0.25); color:#00d9ff;}
</style>
</head>

<body>

<canvas id="particles"></canvas>

<div class="card">
  <div class="profile">
    <img src="https://cdn.discordapp.com/attachments/1434459559727992852/1456911778146680852/image-3.png?ex=695a1654&is=6958c4d4&hm=b6b4bf029aed73a0b69a03aa07b08f7afbd7ab5dcc4e9e81a1190a5b41470b46">
  </div>

  <h1>JAAT CHEATS</h1>
  <div class="status">● Official Social Links</div>

  <div class="links">
    <a class="yt" href="https://youtube.com/@axynshotz99" target="_blank">
      <i class="fab fa-youtube"></i> YouTube
    </a>

    <a class="ig" href="https://www.instagram.com/axynshotz99" target="_blank">
      <i class="fab fa-instagram"></i> Instagram
    </a>

    <a class="dc" href="https://discord.gg/VY8GASaWHG" target="_blank">
      <i class="fab fa-discord"></i> Discord
    </a>

    <a class="tg" href="#" target="_blank">
      <i class="fab fa-telegram"></i> Telegram
    </a>
  </div>
</div>

<script>
const canvas = document.getElementById("particles");
const ctx = canvas.getContext("2d");

function resize(){
  canvas.width = innerWidth;
  canvas.height = innerHeight;
}
resize();
window.addEventListener("resize", resize);

let particles = [];

for(let i=0;i<120;i++){
  particles.push({
    x:Math.random()*canvas.width,
    y:Math.random()*canvas.height,
    r:Math.random()*4+1,
    dx:(Math.random()-0.5)*1.3,
    dy:(Math.random()-0.5)*1.3,
    color:`hsl(${Math.random()*360},100%,60%)`
  });
}

function animate(){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  particles.forEach(p=>{
    ctx.beginPath();
    ctx.arc(p.x,p.y,p.r,0,Math.PI*2);
    ctx.fillStyle=p.color;
    ctx.fill();

    p.x+=p.dx;
    p.y+=p.dy;

    if(p.x<0||p.x>canvas.width) p.dx*=-1;
    if(p.y<0||p.y>canvas.height) p.dy*=-1;
  });
  requestAnimationFrame(animate);
}
animate();
</script>

</body>
</html>
