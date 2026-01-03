[index.html](https://github.com/user-attachments/files/24414531/index.html)
<html lang="en">
<head>
<meta charset="UTF-8">
<title>JAAT CHEATS | Official Links</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Icons -->
<link rel="stylesheet"https://cdn.discordapp.com/attachments/1434459559727992852/1456911778146680852/image-3.png?ex=695a1654&is=6958c4d4&hm=b6b4bf029aed73a0b69a03aa07b08f7afbd7ab5dcc4e9e81a1190a5b41470b46">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family: 'Poppins', sans-serif;
}

body{
  height:100vh;
  overflow:hidden;
  background:#000;
  display:flex;
  align-items:center;
  justify-content:center;
  color:white;
}

/* PARTICLE BACKGROUND */
canvas{
  position:fixed;
  top:0;
  left:0;
  z-index:-1;
}

/* MAIN CARD */
.card{
  width:320px;
  background:rgba(255,255,255,0.08);
  border-radius:22px;
  padding:25px 20px;
  backdrop-filter: blur(12px);
  box-shadow:0 0 40px rgba(255,0,0,0.4);
  text-align:center;
}

/* PROFILE IMAGE */
.profile img{
  width:110px;
  height:110px;
  border-radius:50%;
  border:4px solid #ff2d2d;
  box-shadow:0 0 25px red;
}

/* TEXT */
h1{
  margin-top:15px;
  font-size:26px;
  letter-spacing:1px;
}

.status{
  color:#00ff6a;
  font-size:14px;
  margin:5px 0 20px;
}

/* LINKS */
.links{
  display:flex;
  flex-direction:column;
  gap:12px;
}

.links a{
  padding:12px;
  border-radius:14px;
  text-decoration:none;
  color:white;
  font-size:16px;
  display:flex;
  align-items:center;
  justify-content:center;
  gap:10px;
  transition:0.3s;
}

.links a:hover{
  transform:scale(1.07);
  box-shadow:0 0 20px currentColor;
}

/* COLORS */
.yt{background:rgba(255,0,0,0.2); color:#ff3b3b;}
.ig{background:rgba(255,0,200,0.2); color:#ff4fd8;}
.dc{background:rgba(80,120,255,0.2); color:#5b8cff;}
.tg{background:rgba(0,200,255,0.2); color:#00d9ff;}

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

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let particles = [];

for(let i=0;i<120;i++){
  particles.push({
    x:Math.random()*canvas.width,
    y:Math.random()*canvas.height,
    r:Math.random()*4+1,
    dx:(Math.random()-0.5)*1.5,
    dy:(Math.random()-0.5)*1.5,
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

window.onresize=()=>{
  canvas.width=window.innerWidth;
  canvas.height=window.innerHeight;
}
</script>

</body>
</html>
