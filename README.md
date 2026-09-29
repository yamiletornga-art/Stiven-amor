# Stiven-amor
<!doctype html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Para Stiven ♡ — Nuestra pequeña aventura</title>
<style>
:root{
  --pink:#ff8fb3; --rose:#ff5f91; --cream:#fff8f3; --wine:#5a1832;
  --purple:#7c5cff; --shadow:0 18px 50px rgba(70,20,45,.18);
}
*{box-sizing:border-box}
html,body{margin:0;min-height:100%;font-family:system-ui,-apple-system,Segoe UI,Roboto,sans-serif;background:#14091b;color:#fff}
body{overflow-x:hidden}
button{font:inherit}
.screen{
  min-height:100vh;display:none;align-items:center;justify-content:center;
  padding:28px;position:relative;overflow:hidden;
  background:
   radial-gradient(circle at 15% 15%,rgba(255,143,179,.22),transparent 28%),
   radial-gradient(circle at 85% 80%,rgba(124,92,255,.22),transparent 30%),
   linear-gradient(135deg,#170b20,#32132e 55%,#130918);
}
.screen.active{display:flex;animation:in .65s ease both}
@keyframes in{from{opacity:0;transform:translateY(18px) scale(.98)}to{opacity:1;transform:none}}
.card{
  width:min(900px,100%);background:rgba(255,248,243,.95);color:var(--wine);
  border:1px solid rgba(255,255,255,.45);border-radius:30px;padding:34px;
  box-shadow:var(--shadow);position:relative;z-index:3;
}
.hero{text-align:center;background:linear-gradient(145deg,#fff8f3,#ffe8ef)}
.badge{display:inline-block;padding:8px 14px;border-radius:999px;background:#ffe0ea;color:#9b3158;font-weight:800;font-size:.82rem}
h1{font-size:clamp(2.1rem,7vw,4.8rem);line-height:.98;margin:18px 0 10px}
h2{font-size:clamp(1.7rem,4vw,2.6rem);margin:0 0 12px}
p{line-height:1.75;font-size:1.04rem}
.subtitle{opacity:.75}
.btn{
  border:0;border-radius:999px;padding:14px 22px;font-weight:850;cursor:pointer;
  background:linear-gradient(135deg,var(--rose),#ffb0c9);color:#fff;
  box-shadow:0 10px 25px rgba(255,95,145,.28);transition:.2s;
}
.btn:hover{transform:translateY(-2px) scale(1.02)}
.btn.secondary{background:#fff;color:var(--wine);border:1px solid #ffd0dd}
.btnrow{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin-top:22px}
.photo-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin:22px 0}
.photo-grid img{width:100%;height:240px;object-fit:cover;border-radius:20px;box-shadow:0 8px 22px #6d274122}
@media(max-width:650px){.photo-grid{grid-template-columns:1fr}.photo-grid img{height:270px}}
.letter{font-family:Georgia,serif;font-size:1.12rem}
.signature{font-weight:800;font-size:1.2rem}
.progress{position:fixed;top:12px;left:50%;transform:translateX(-50%);z-index:10;display:flex;gap:7px}
.dot{width:9px;height:9px;border-radius:50%;background:#ffffff55}.dot.on{background:#fff}
.poem-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
@media(max-width:760px){.poem-grid{grid-template-columns:1fr}}
.poem{
  min-height:150px;border:0;border-radius:22px;padding:20px;text-align:left;
  background:linear-gradient(145deg,#fff,#fff0f5);color:var(--wine);
  box-shadow:0 10px 25px #5a183214;cursor:pointer;transition:.2s;
}
.poem:hover{transform:translateY(-4px)}
.poem .secret{display:none;margin-top:12px;line-height:1.65;font-family:Georgia,serif}
.poem.open .secret{display:block}
.poem.open .tap{display:none}
.memory{display:grid;grid-template-columns:1fr 1fr;gap:18px;align-items:center}
@media(max-width:700px){.memory{grid-template-columns:1fr}}
.memory img{width:100%;max-height:430px;object-fit:cover;border-radius:25px}
.flower{position:absolute;font-size:2rem;animation:float 7s linear infinite;opacity:.75;z-index:1}
@keyframes float{from{transform:translateY(110vh) rotate(0deg)}to{transform:translateY(-20vh) rotate(360deg)}}
.heart{font-size:5rem;filter:drop-shadow(0 0 18px #ff6c9d88);animation:pulse 1.6s infinite}
@keyframes pulse{50%{transform:scale(1.12)}}
.quiz label{display:block;background:#fff0f5;padding:13px 16px;border-radius:15px;margin:9px 0;cursor:pointer}
.quiz input{accent-color:#ff5f91;margin-right:9px}
.result{font-weight:800;text-align:center;min-height:30px}
#music{position:fixed;left:-9999px;top:-9999px;width:1px;height:1px}
.small{font-size:.82rem;opacity:.65;text-align:center;margin-top:18px}
</style>
</head>
<body>

<div id="music"></div>
<div class="progress" id="progress"></div>

<section class="screen active" data-step="0">
  <span class="flower" style="left:8%;animation-delay:0s">🌸</span>
  <span class="flower" style="left:80%;animation-delay:2s">🌷</span>
  <span class="flower" style="left:45%;animation-delay:4s">🌹</span>
  <div class="card hero">
    <span class="badge">NIVEL 01 · UNA AVENTURA SOLO PARA TI</span>
    <div class="heart">♡</div>
    <h1>Stiven,<br>esto es para ti.</h1>
    <p class="subtitle">Pulsa el botón para comenzar nuestra pequeña historia.</p>
    <div class="btnrow">
      <button class="btn" onclick="startGame()">▶ Comenzar aventura</button>
    </div>
    <p class="small">Consejo: activa el sonido para escuchar la canción de fondo.</p>
  </div>
</section>

<section class="screen" data-step="1">
  <div class="card">
    <span class="badge">NIVEL 02 · CARTA DESBLOQUEADA 💌</span>
    <h2>Para el niño que hace bonito mi mundo</h2>
    <div class="letter">
      <p>Mi amor:</p>
      <p>Si pudiera guardar un momento para volver a él cada vez que te extraño, escogería cualquiera en el que estemos juntos. Porque contigo hasta lo sencillo se vuelve especial: una mirada, una sonrisa, una foto, una conversación que se alarga sin darnos cuenta.</p>
      <p>Quiero que sepas que eres una parte muy bonita de mi historia. No porque todo tenga que ser perfecto, sino porque contigo quiero seguir descubriendo, aprendiendo, riendo y construyendo recuerdos.</p>
      <p>Esta página es pequeña comparada con todo lo que siento, pero la hice para que, cuando la abras, recuerdes algo muy sencillo:</p>
      <p><strong>te quiero, te elijo y me encanta compartir mi mundo contigo. ♡</strong></p>
      <p class="signature">Con todo mi cariño,<br>tu niña. 🌷</p>
    </div>
    <div class="photo-grid">
      <img src="fotos/foto1.jpg" alt="Nuestro recuerdo 1">
      <img src="fotos/foto2.jpg" alt="Nuestro recuerdo 2">
      <img src="fotos/foto3.jpg" alt="Nuestro recuerdo 3">
    </div>
    <div class="btnrow"><button class="btn" onclick="next()">Abrir siguiente página →</button></div>
  </div>
</section>

<section class="screen" data-step="2">
  <div class="card">
    <span class="badge">NIVEL 03 · TOCA PARA DESCUBRIR ✨</span>
    <h2>Pequeños poemas escondidos</h2>
    <p>Hay tres corazones. Toca cada uno para revelar lo que guardan.</p>
    <div class="poem-grid">
      <button class="poem" onclick="this.classList.toggle('open')">
        <strong>🌙 Si fueras una noche...</strong>
        <div class="tap">Tócame para leer</div>
        <div class="secret">serías esa noche tranquila que no quiero que termine, porque incluso en silencio haces que todo se sienta en casa.</div>
      </button>
      <button class="poem" onclick="this.classList.toggle('open')">
        <strong>🌻 Si fueras un recuerdo...</strong>
        <div class="tap">Tócame para leer</div>
        <div class="secret">serías de esos que uno guarda con cuidado, no para vivir en el pasado, sino para sonreír cada vez que vuelve a pensarlo.</div>
      </button>
      <button class="poem" onclick="this.classList.toggle('open')">
        <strong>💗 Si fueras una canción...</strong>
        <div class="tap">Tócame para leer</div>
        <div class="secret">serías mi parte favorita: la que llega sin avisar, cambia el ritmo de todo y hace que quiera quedarme un poquito más.</div>
      </button>
    </div>
    <div class="btnrow"><button class="btn" onclick="next()">Seguir la aventura →</button></div>
  </div>
</section>

<section class="screen" data-step="3">
  <div class="card">
    <span class="badge">NIVEL 04 · RECUERDOS 📸</span>
    <div class="memory">
      <img src="fotos/foto2.jpg" alt="Un recuerdo juntos">
      <div>
        <h2>Lo que más me gusta de nosotros</h2>
        <p>No es una sola foto ni un solo día. Es esa colección de instantes que, juntos, forman algo que solo nosotros entendemos.</p>
        <p>Y si pudiera pedir un deseo para el futuro, sería sencillo: <strong>más momentos que algún día podamos mirar y decir “¿te acuerdas?”</strong></p>
        <button class="btn" onclick="next()">Tengo otro nivel para ti →</button>
      </div>
    </div>
  </div>
</section>

<section class="screen" data-step="4">
  <div class="card quiz">
    <span class="badge">NIVEL 05 · MINI JUEGO 🕹️</span>
    <h2>¿Qué tan bien conoces este corazón? 💘</h2>
    <p>Elige la respuesta que más te guste. No hay respuestas incorrectas.</p>
    <p><strong>Pregunta 1:</strong> ¿Qué quiero coleccionar contigo?</p>
    <label><input type="radio" name="q1" value="a"> Momentos y recuerdos</label>
    <label><input type="radio" name="q1" value="b"> Tickets de supermercado 😂</label>
    <label><input type="radio" name="q1" value="c"> Solo puntos en un videojuego</label>

    <p><strong>Pregunta 2:</strong> ¿Qué palabra resume mejor esta página?</p>
    <label><input type="radio" name="q2" value="a"> Amor</label>
    <label><input type="radio" name="q2" value="b"> Caos</label>
    <label><input type="radio" name="q2" value="c"> Tarea</label>

    <div class="btnrow"><button class="btn" onclick="checkQuiz()">Desbloquear recompensa 🎁</button></div>
    <div class="result" id="result"></div>
  </div>
</section>

<section class="screen" data-step="5">
  <span class="flower" style="left:12%;animation-delay:0s">🌹</span>
  <span class="flower" style="left:30%;animation-delay:1.4s">🌸</span>
  <span class="flower" style="left:52%;animation-delay:2.8s">🌷</span>
  <span class="flower" style="left:74%;animation-delay:4.2s">🌺</span>
  <div class="card hero">
    <span class="badge">NIVEL FINAL · RECOMPENSA DESBLOQUEADA 💖</span>
    <div class="heart">💗</div>
    <h2>Stiven, llegaste hasta el final.</h2>
    <p>Y si esto fuera un videojuego, mi recompensa favorita no sería ganar...</p>
    <p><strong>sería seguir jugando la historia contigo.</strong></p>
    <p>Gracias por existir en mi vida, por los momentos compartidos y por todos los que todavía nos faltan.</p>
    <p style="font-family:Georgia,serif;font-size:1.35rem">“Si el mundo fuera infinito,<br>te volvería a buscar en cada versión de él.”</p>
    <div class="photo-grid">
      <img src="fotos/foto3.jpg" alt="Nuestro recuerdo final">
    </div>
    <p class="signature">Fin de la partida...<br>o quizá apenas comienza. 🌹</p>
    <div class="btnrow">
      <button class="btn" onclick="restart()">↻ Volver al inicio</button>
      <button class="btn secondary" onclick="toggleMusic()">♫ Música</button>
    </div>
  </div>
</section>

<script>
let step=0;
const screens=[...document.querySelectorAll('.screen')];
const progress=document.getElementById('progress');
let player=null, musicStarted=false;

function drawProgress(){
  progress.innerHTML=screens.map((_,i)=>`<span class="dot ${i===step?'on':''}"></span>`).join('');
}
function show(n){
  step=Math.max(0,Math.min(n,screens.length-1));
  screens.forEach((s,i)=>s.classList.toggle('active',i===step));
  drawProgress();
  window.scrollTo({top:0,behavior:'smooth'});
}
function next(){ show(step+1); }
function restart(){ show(0); }

function loadYouTube(){
  if(window.YT && YT.Player){
    createPlayer(); return;
  }
  const tag=document.createElement('script');
  tag.src='https://www.youtube.com/iframe_api';
  document.head.appendChild(tag);
  window.onYouTubeIframeAPIReady=createPlayer;
}
function createPlayer(){
  if(player) return;
  player=new YT.Player('music',{
    height:'1',width:'1',
    videoId:'mskcCXoMFtQ',
    playerVars:{autoplay:0,controls:0,loop:1,playlist:'mskcCXoMFtQ',playsinline:1}
  });
}
function startGame(){
  show(1);
  loadYouTube();
  setTimeout(()=>{ if(player){player.playVideo(); musicStarted=true;} },800);
}
function toggleMusic(){
  if(!player){loadYouTube();return;}
  const state=player.getPlayerState();
  if(state===1){player.pauseVideo();} else {player.playVideo();musicStarted=true;}
}
function checkQuiz(){
  const q1=document.querySelector('input[name="q1"]:checked')?.value;
  const q2=document.querySelector('input[name="q2"]:checked')?.value;
  const result=document.getElementById('result');
  if(q1==='a' && q2==='a'){
    result.textContent='🎉 ¡Recompensa desbloqueada! Sabía que lo sabías. 💖';
    setTimeout(next,900);
  }else{
    result.textContent='🥹 Casi... vuelve a intentarlo, mi amor.';
  }
}
drawProgress();
</script>
</body>
</html>
