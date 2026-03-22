<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
<title>Murder Mystery 3D</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700;900&family=Crimson+Pro:ital,wght@0,300;0,400;1,300&display=swap');
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent;}
:root{--blood:#8b0000;--gold:#c9a84c;--card:#13100d;--border:#2a2218;--text:#d4c9a8;--muted:#7a6e58;}
html,body{width:100%;height:100%;overflow:hidden;background:#07050a;color:var(--text);font-family:'Crimson Pro',serif;touch-action:none;}
#c3d{position:fixed;top:0;left:0;width:100%;height:100%;display:none;z-index:1;}
.screen{display:none;position:fixed;inset:0;z-index:50;flex-direction:column;align-items:center;justify-content:center;padding:1.5rem;background:#07050a;}
.screen.active{display:flex;}
#s-title{text-align:center;gap:1.8rem;}
.blade{font-size:2.8rem;display:inline-block;animation:fl 3s ease-in-out infinite;}
@keyframes fl{0%,100%{transform:rotate(-15deg) translateY(0);}50%{transform:rotate(-15deg) translateY(-10px);}}
h1{font-family:'Cinzel',serif;font-weight:900;font-size:clamp(2.8rem,9vw,5.5rem);line-height:.95;letter-spacing:.04em;color:#fff;text-shadow:0 0 50px rgba(139,0,0,.5),0 3px 0 var(--blood);}
h1 em{color:var(--blood);font-style:normal;}
.tagline{font-style:italic;color:var(--muted);letter-spacing:.25em;text-transform:uppercase;font-size:1rem;}
.ornament{color:var(--muted);letter-spacing:.4em;font-size:.8rem;}
.menu{display:flex;flex-direction:column;gap:.9rem;width:100%;max-width:300px;}
.btn{font-family:'Cinzel',serif;font-size:.95rem;letter-spacing:.1em;padding:.9rem 1.8rem;border:1px solid var(--border);background:var(--card);color:var(--text);cursor:pointer;}
.btn-red{background:var(--blood);border-color:var(--blood);color:#fff;}
.panel{background:var(--card);border:1px solid var(--border);padding:2.2rem;width:100%;max-width:400px;position:relative;}
.panel::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--gold),transparent);}
.panel h2{font-family:'Cinzel',serif;font-size:1.3rem;color:var(--gold);margin-bottom:1.4rem;letter-spacing:.1em;}
label{display:block;font-size:.75rem;letter-spacing:.2em;text-transform:uppercase;color:var(--muted);margin-bottom:.45rem;}
input[type=text]{width:100%;background:rgba(255,255,255,.03);border:1px solid var(--border);color:var(--text);font-family:'Crimson Pro',serif;font-size:1.1rem;padding:.7rem .9rem;outline:none;}
input[type=text]:focus{border-color:var(--gold);}
input[type=text]::placeholder{color:var(--muted);}
.field{margin-bottom:1.1rem;}
.link-btn{background:none;border:none;color:var(--muted);cursor:pointer;font-family:'Crimson Pro',serif;font-style:italic;font-size:.95rem;margin-top:.8rem;}
.codebox{background:rgba(139,0,0,.12);border:1px solid var(--blood);padding:1.2rem;text-align:center;margin:1.3rem 0;}
.codebox small{font-size:.7rem;letter-spacing:.25em;text-transform:uppercase;color:var(--muted);display:block;margin-bottom:.4rem;}
.codebox strong{font-family:'Cinzel',serif;font-size:2.8rem;letter-spacing:.35em;color:#fff;}
#s-lobby,#s-join-lobby{gap:1.2rem;}
.lobby-wrap{background:var(--card);border:1px solid var(--border);padding:1.8rem;width:100%;max-width:480px;position:relative;}
.lobby-wrap::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--gold),transparent);}
.lobby-top{display:flex;justify-content:space-between;align-items:center;margin-bottom:1.2rem;}
.lobby-top h2{font-family:'Cinzel',serif;font-size:1.15rem;color:var(--gold);letter-spacing:.1em;}
.pcount{font-size:.82rem;color:var(--muted);}
.plist{list-style:none;min-height:60px;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.3rem;}
.pitem{display:flex;align-items:center;gap:.7rem;padding:.55rem .9rem;background:rgba(255,255,255,.02);border:1px solid var(--border);}
.pdot{width:7px;height:7px;border-radius:50%;background:var(--blood);flex-shrink:0;}
.pdot.gold{background:var(--gold);}
.pname{flex:1;font-size:1rem;}
.ptag{font-size:.68rem;letter-spacing:.12em;text-transform:uppercase;color:var(--gold);}
.hint{font-size:.83rem;color:var(--muted);font-style:italic;margin-bottom:1rem;text-align:center;}
/* countdown */
#s-countdown{gap:.5rem;}
#cdn{font-family:'Cinzel',serif;font-size:clamp(7rem,28vw,14rem);color:#fff;line-height:1;text-shadow:0 0 80px rgba(139,0,0,.8);}
#cdn.red{color:var(--blood);}
#cdsub{font-family:'Cinzel',serif;font-size:.9rem;letter-spacing:.3em;color:var(--muted);text-transform:uppercase;}
/* role */
#s-role{gap:1.6rem;}
.rc{background:var(--card);border:1px solid var(--border);padding:2.8rem 2.4rem;width:100%;max-width:340px;text-align:center;position:relative;}
.rc::before,.rc::after{content:'';position:absolute;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--blood),transparent);}
.rc::before{top:0;}.rc::after{bottom:0;}
.ri{font-size:3.5rem;display:block;margin-bottom:1rem;}
.rl{font-family:'Cinzel',serif;font-size:2rem;font-weight:900;letter-spacing:.08em;margin-bottom:.6rem;}
.rl.murderer{color:var(--blood);}
.rl.innocent{color:#8ab4a0;}
.rd{font-style:italic;color:var(--muted);font-size:1rem;line-height:1.6;}
.rh{font-size:.75rem;color:var(--muted);letter-spacing:.1em;opacity:.6;}
.rh2{font-size:.8rem;color:var(--blood);margin-top:6px;letter-spacing:.06em;}
/* overlay */
.overlay{position:fixed;inset:0;background:rgba(7,5,10,.96);z-index:200;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:2rem;}
.overlay.hide{display:none;}
.ov-icon{font-size:3.5rem;margin-bottom:.9rem;}
.ov-title{font-family:'Cinzel',serif;font-size:clamp(1.4rem,5vw,2.3rem);font-weight:700;margin-bottom:.7rem;}
.ov-sub{font-style:italic;color:var(--muted);font-size:1.05rem;max-width:380px;line-height:1.65;margin-bottom:1.8rem;}
/* toast */
.toast{position:fixed;top:1.3rem;right:1.3rem;background:var(--card);border:1px solid var(--gold);padding:.65rem 1.1rem;font-size:.97rem;z-index:500;max-width:260px;animation:ti .3s ease,to .3s ease 2.6s forwards;}
@keyframes ti{from{transform:translateX(110%);opacity:0;}to{transform:none;opacity:1;}}
@keyframes to{to{transform:translateX(20px);opacity:0;}}
/* connecting */
.connecting{position:fixed;inset:0;background:rgba(7,5,10,.97);z-index:600;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:1rem;}
.connecting.hide{display:none;}
.spinner{width:40px;height:40px;border:3px solid var(--border);border-top-color:var(--blood);border-radius:50%;animation:spin 1s linear infinite;}
@keyframes spin{to{transform:rotate(360deg);}}
.conn-txt{font-family:'Cinzel',serif;font-size:.9rem;letter-spacing:.15em;color:var(--muted);}

/* ── HUD ── */
#hud{position:fixed;top:0;left:0;width:100%;height:100%;z-index:10;pointer-events:none;display:none;}
#xhair{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);width:14px;height:14px;}
#xhair::before,#xhair::after{content:'';position:absolute;background:rgba(255,210,100,.9);}
#xhair::before{width:2px;height:100%;left:50%;transform:translateX(-50%);}
#xhair::after{height:2px;width:100%;top:50%;transform:translateY(-50%);}
#rolepill{position:absolute;top:14px;right:14px;padding:6px 16px;font-family:'Cinzel',serif;font-size:.78rem;letter-spacing:.12em;text-transform:uppercase;border:1px solid;border-radius:2px;background:rgba(0,0,0,.9);}
#rolepill.murderer{border-color:var(--blood);color:#ff4444;}
#rolepill.innocent{border-color:#334488;color:#aabbff;}
#rolepill.sheriff{border-color:var(--gold);color:var(--gold);}
/* safe badge */
#safepill{position:absolute;top:50px;right:14px;padding:5px 14px;font-family:'Cinzel',serif;font-size:.75rem;letter-spacing:.1em;border-radius:2px;background:rgba(0,80,0,.5);border:1px solid #226622;color:#55ee55;display:none;}
/* hotbar */
#hotbar{position:absolute;bottom:48px;left:50%;transform:translateX(-50%);display:flex;gap:6px;}
.hs{width:58px;height:58px;background:rgba(0,0,0,.85);border:2px solid #333;border-radius:3px;display:flex;flex-direction:column;align-items:center;justify-content:center;font-size:1.55rem;position:relative;pointer-events:all;cursor:pointer;}
.hs.on{border-color:var(--gold);}
.hs.off{display:none;}
.hk{position:absolute;top:3px;left:5px;font-size:.52rem;color:#555;font-family:'Cinzel',serif;}
#ctrl{position:absolute;bottom:12px;left:50%;transform:translateX(-50%);background:rgba(0,0,0,.72);border:1px solid #1a1208;color:#4a3820;font-size:10px;letter-spacing:.09em;padding:5px 14px;font-family:'Cinzel',serif;white-space:nowrap;}
#escbtn{position:absolute;bottom:12px;right:14px;padding:8px 14px;background:rgba(0,0,0,.8);border:1px solid #333;color:#555;cursor:pointer;font-family:'Cinzel',serif;font-size:.72rem;letter-spacing:.1em;pointer-events:all;border-radius:2px;}
/* mobile joystick */
#jzone{position:absolute;bottom:80px;left:20px;width:110px;height:110px;pointer-events:all;display:none;}
#jbase{position:absolute;inset:0;border-radius:50%;background:rgba(0,0,0,.35);border:2px solid rgba(201,168,76,.25);}
#jknob{position:absolute;width:44px;height:44px;border-radius:50%;background:rgba(139,0,0,.6);border:2px solid rgba(201,168,76,.5);top:33px;left:33px;}
#lzone{position:absolute;right:0;top:0;width:55%;height:100%;pointer-events:all;display:none;}
/* use button mobile */
#usebtn{position:absolute;bottom:80px;right:140px;width:64px;height:64px;border-radius:50%;background:rgba(139,0,0,.6);border:2px solid var(--blood);color:#fff;font-size:1.4rem;display:none;align-items:center;justify-content:center;pointer-events:all;cursor:pointer;}
/* dead */
#dead{position:fixed;inset:0;z-index:30;display:none;flex-direction:column;align-items:center;justify-content:center;gap:14px;background:rgba(0,0,0,.65);backdrop-filter:blur(3px);}
#dead h2{font-family:'Cinzel',serif;font-size:2rem;color:var(--blood);}
#dead p{color:var(--muted);font-style:italic;font-size:.9rem;}
.sb{padding:9px 24px;background:rgba(0,0,0,.8);border:1px solid #333;color:#888;cursor:pointer;font-family:'Cinzel',serif;font-size:.78rem;letter-spacing:.12em;pointer-events:all;}
#specbar{position:fixed;bottom:18px;left:50%;transform:translateX(-50%);z-index:31;background:rgba(0,0,0,.85);border:1px solid #333;color:#888;padding:5px 16px;font-size:.76rem;letter-spacing:.1em;display:none;pointer-events:none;font-family:'Cinzel',serif;}
#flash{position:fixed;inset:0;background:rgba(139,0,0,.45);z-index:100;display:none;pointer-events:none;}
#notif{position:fixed;top:50%;left:50%;transform:translate(-50%,-50%);background:rgba(0,0,0,.92);border:1px solid var(--blood);color:#fff;padding:12px 32px;font-family:'Cinzel',serif;font-size:.95rem;letter-spacing:.1em;z-index:150;display:none;text-align:center;border-radius:2px;max-width:80vw;}
</style>
</head>
<body>

<div class="connecting" id="conn"><div class="spinner"></div><div class="conn-txt">VERBINDE…</div></div>

<div id="kick-dialog" style="display:none;position:fixed;inset:0;background:rgba(0,0,0,.75);z-index:400;align-items:center;justify-content:center;">
  <div style="background:var(--card);border:1px solid var(--gold);padding:2rem;text-align:center;max-width:280px;width:90%;">
    <div style="font-family:'Cinzel',serif;font-size:.95rem;color:var(--gold);margin-bottom:.8rem;">Spieler kicken?</div>
    <div id="kick-name" style="font-size:1rem;margin-bottom:1.4rem;color:var(--text);"></div>
    <div style="display:flex;gap:.8rem;justify-content:center;">
      <button class="btn btn-red" onclick="confirmKick()">Kicken</button>
      <button class="btn" onclick="document.getElementById('kick-dialog').style.display='none'">Abbrechen</button>
    </div>
  </div>
</div>

<div id="s-title" class="screen">
  <span class="blade">🗡️</span>
  <div><h1>MURDER<br><em>MYSTERY</em></h1><p class="tagline">Ein Mörder unter Euch</p></div>
  <div class="ornament">— ✦ —</div>
  <div class="menu">
    <button class="btn btn-red" onclick="go('s-host')">🔑 Spiel erstellen</button>
    <button class="btn" onclick="go('s-join')">🚪 Mit Code beitreten</button>
  </div>
</div>

<div id="s-host" class="screen">
  <div class="panel">
    <h2>🔑 Spiel erstellen</h2>
    <div class="field"><label>Dein Name</label><input type="text" id="host-name" placeholder="Name…" maxlength="16"></div>
    <div class="codebox"><small>Lobby-Code</small><strong id="new-code">—</strong></div>
    <button class="btn btn-red" onclick="createLobby()" style="width:100%">Erstellen →</button><br>
    <button class="link-btn" onclick="go('s-title')">← Zurück</button>
  </div>
</div>

<div id="s-join" class="screen">
  <div class="panel">
    <h2>🚪 Beitreten</h2>
    <div class="field"><label>Dein Name</label><input type="text" id="join-name" placeholder="Name…" maxlength="16"></div>
    <div class="field"><label>Code</label><input type="text" id="join-code" placeholder="4829" maxlength="6" style="letter-spacing:.3em;font-size:1.5rem;text-align:center;"></div>
    <button class="btn btn-red" onclick="joinLobby()" style="width:100%">Beitreten →</button><br>
    <button class="link-btn" onclick="go('s-title')">← Zurück</button>
  </div>
</div>

<div id="s-lobby" class="screen">
  <div class="lobby-wrap">
    <div class="lobby-top"><h2>⚔️ Lobby</h2><span class="pcount" id="hcount">1 Spieler</span></div>
    <div class="codebox" style="margin-bottom:1.3rem;"><small>Code teilen</small><strong id="h-code-show">—</strong></div>
    <ul class="plist" id="hplist"></ul>
    <p class="hint">Min. 2 Spieler</p>
    <button class="btn btn-red" onclick="startGame()" style="width:100%">🗡️ Starten</button><br>
    <button class="link-btn" onclick="resetAll()">← Verlassen</button>
  </div>
</div>

<div id="s-join-lobby" class="screen">
  <div class="lobby-wrap">
    <div class="lobby-top"><h2>⏳ Lobby</h2><span class="pcount" id="jcount">—</span></div>
    <div class="codebox" style="margin-bottom:1.3rem;"><small>Code</small><strong id="j-code-show">—</strong></div>
    <ul class="plist" id="jplist"></ul>
    <p class="hint">Warte auf Host…</p>
    <button class="link-btn" onclick="resetAll()">← Verlassen</button>
  </div>
</div>

<div id="s-countdown" class="screen">
  <div id="cdn">10</div>
  <div id="cdsub">Spiel beginnt…</div>
</div>

<div id="s-role" class="screen">
  <div class="rc">
    <span class="ri" id="r-icon">🗡️</span>
    <div class="rl" id="r-label">—</div>
    <div class="rd" id="r-desc">—</div>
  </div>
  <div class="rh">Nur du siehst das</div>
  <div class="rh2">Welt in <span id="r-cd">3</span>s…</div>
</div>

<div class="overlay hide" id="overlay">
  <div class="ov-icon" id="ov-icon">⚰️</div>
  <div class="ov-title" id="ov-title">—</div>
  <div class="ov-sub" id="ov-sub">—</div>
  <button class="btn btn-red" onclick="resetAll()">🏠 Hauptmenü</button>
</div>

<canvas id="c3d"></canvas>

<div id="hud">
  <div id="xhair"></div>
  <div id="rolepill" class="innocent">—</div>
  <div id="safepill">⭐ SHERIFF</div>
  <div id="hotbar">
    <div class="hs on"  id="slot0" onclick="selSlot(0)"><span class="hk">1</span><span id="s0i">✊</span></div>
    <div class="hs off" id="slot1" onclick="selSlot(1)"><span class="hk">2</span><span id="s1i">🗡️</span></div>
    <div class="hs off" id="slot2" onclick="selSlot(2)"><span class="hk">3</span><span id="s2i">🛡️</span></div>
  </div>
  <!-- mobile joystick -->
  <div id="jzone"><div id="jbase"></div><div id="jknob"></div></div>
  <div id="lzone"></div>
  <button id="usebtn" onclick="useItem()">⚔️</button>
  <div id="ctrl">WASD · Leertaste Springen · 1/2/3 Item · Klick/E Benutzen</div>
  <button id="escbtn" onclick="leaveGame()" style="display:none;">☰ Verlassen</button>
</div>

<div id="dead">
  <h2>☠️ Tot</h2>
  <p id="deadmsg">Du wurdest ermordet.</p>
  <div style="display:flex;gap:8px;margin-top:6px;">
    <button class="sb" onclick="specPrev()">◀ [O]</button>
    <button class="sb" onclick="specNext()">[P] ▶</button>
  </div>
  <button class="sb" style="margin-top:10px;border-color:var(--blood);color:#ff6666;" onclick="leaveGame()">🚪 Verlassen</button>
  <button class="sb" style="margin-top:10px;border-color:var(--blood);color:#ff6666;" onclick="leaveGame()">🚪 Verlassen</button>
</div>
<div id="specbar">Spectating: <span id="specname">—</span></div>
<div id="flash"></div>
<div id="notif"></div>

<script>
/* ═══════════════════════════════════════
   GLOBAL STATE
═══════════════════════════════════════ */
const G={
  name:'',code:'',myRole:'innocent',myIdx:0,isHost:false,
  running:false,alive:true,isSafe:false,
  specIdx:0,curSlot:0,viewMode:0,
  yaw:0,pitch:0,velY:0,onGround:true,pLocked:false,
  shDropped:false,hasShield:false,
  speedMul:1.0,
};
const KEYS={};
const PP=new THREE.Vector3(2,1.7,2);

/* ── util ── */
window.go=id=>{document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));document.getElementById(id)?.classList.add('active');};
window.toast=m=>{const e=document.createElement('div');e.className='toast';e.textContent=m;document.body.appendChild(e);setTimeout(()=>e.remove(),3200);};
const flashRed=()=>{const f=document.getElementById('flash');f.style.display='block';setTimeout(()=>f.style.display='none',400);};
const notif=(msg,dur)=>{const n=document.getElementById('notif');n.textContent=msg;n.style.display='block';clearTimeout(n._t);n._t=setTimeout(()=>n.style.display='none',dur||2000);};
const showOv=(icon,title,sub)=>{document.getElementById('ov-icon').textContent=icon;document.getElementById('ov-title').textContent=title;document.getElementById('ov-sub').textContent=sub;document.getElementById('overlay').classList.remove('hide');};

/* ═══════════════════════════════════════
   THREE.JS — iPad optimised
   - pixelRatio capped at 1
   - fog reduced
   - no shadows
   - low poly counts
   - shared geometries
═══════════════════════════════════════ */
let renderer,scene,camera,clock;
let myChar=null;
let fpHand=null; // first-person hand mesh attached to world
const others={}; // name->{g,lL,lR,aL,aR,sm,label,corpse,blood,alive,wt}
const WALLS=[];
let shieldDropMesh=null,shieldDropPos={x:0,z:0};
let loopStarted=false;
let walkT=0;
const _mv=new THREE.Vector3(),_cd=new THREE.Vector3(),_cr=new THREE.Vector3();

/* shared geometries — create once */
const GEO={
  body:   new THREE.BoxGeometry(.48,.68,.24),
  head:   new THREE.BoxGeometry(.36,.36,.36),
  eye:    new THREE.BoxGeometry(.08,.06,.04),
  leg:    new THREE.BoxGeometry(.2,.5,.2),
  arm:    new THREE.BoxGeometry(.16,.52,.16),
  corpse: new THREE.BoxGeometry(.48,.12,1.1),
  blood:  new THREE.CylinderGeometry(.5,.5,.02,8),
  coin:   new THREE.CylinderGeometry(.22,.22,.09,8),
  // shield drop
  shBody: new THREE.BoxGeometry(.6,.7,.08),
  shBoss: new THREE.SphereGeometry(.12,6,6),
  // knife
  kBlade: new THREE.BoxGeometry(.05,.38,.08),
  kHand:  new THREE.BoxGeometry(.07,.18,.1),
  // hat top
  htBrim: new THREE.CylinderGeometry(.27,.27,.06,8),
  htCrown:new THREE.CylinderGeometry(.15,.17,.32,8),
};

function lam(c){return new THREE.MeshLambertMaterial({color:c});}
function lame(c,e,ei){const m=lam(c);m.emissive.set(e);m.emissiveIntensity=ei;return m;}

// shared mats
const MAT={
  sand:lam(0xc8aa6e),sand2:lam(0xb89850),road:lam(0x8a7850),side:lam(0xa08860),
  w:[lam(0xc0a060),lam(0xb09050),lam(0xd0b070),lam(0xa88840)],
  roof:[lam(0x886030),lam(0x7a5428)],
  door:lam(0x5a3818),win:lame(0x405060,0x203040,.8),winL:lame(0x806828,0x604010,.7),
  slab:lam(0x8a7040),wood:lam(0x5a3818),glow:lame(0xffee88,0xffcc44,1),
  cactus:lam(0x3a6030),rock:lam(0x887060),
  pants:lam(0x3a2c1a),face:lam(0xf0c080),eye:lam(0x111111),
  blood:lame(0x8b0000,0x440000,.3),
  knife:lame(0xcccccc,0x888888,.3),knifeH:lam(0x5a3818),
  shield:lame(0x4488cc,0x224488,.4),shBoss:lam(0x888888),
  skins:[lam(0xe8c888),lam(0xcc3333),lam(0x3355cc),lam(0xc9a84c),lam(0x222222),lam(0xeeeeee),lam(0x226622),lam(0x552288)],
  hBk:lam(0x111111),hGl:lame(0xc9a84c,0x664400,.4),hBl:lam(0x223388),
};
const HATS=['none','top','cap','none','top','cap','none','top'];
const SPAWNS=[[2,2],[9,6],[-9,-6],[13,-11],[-6,13],[18,1],[-16,8],[4,-20]];
const SKINC=[0xe8c888,0xcc3333,0x3355cc,0xc9a84c,0x222222,0xeeeeee,0x226622,0x552288];

window.initThree=function(){
  if(renderer)return;
  const canvas=document.getElementById('c3d');
  renderer=new THREE.WebGLRenderer({antialias:false,canvas,powerPreference:'high-performance'});
  // iPad: cap at 1x pixel ratio for performance
  renderer.setPixelRatio(1);
  renderer.setSize(innerWidth,innerHeight);
  renderer.shadowMap.enabled=false;

  scene=new THREE.Scene();
  scene.background=new THREE.Color(0xd4a96a);
  scene.fog=new THREE.FogExp2(0xc8a060,.014); // slightly denser fog = less draw calls

  camera=new THREE.PerspectiveCamera(70,innerWidth/innerHeight,.1,120); // shorter far plane
  camera.rotation.order='YXZ';
  clock=new THREE.Clock();

  window.addEventListener('resize',()=>{
    camera.aspect=innerWidth/innerHeight;
    camera.updateProjectionMatrix();
    renderer.setSize(innerWidth,innerHeight);
  });
  buildMap();
  setupInput();
  if(!loopStarted){loopStarted=true;gameLoop();}
};

/* ── MAP ── */
function B(mat,w,h,d,x,y,z){
  const m=new THREE.Mesh(new THREE.BoxGeometry(w,h,d),mat);
  m.position.set(x,y,z);scene.add(m);return m;
}
function C(mat,rt,rb,h,sg,x,y,z){
  const m=new THREE.Mesh(new THREE.CylinderGeometry(rt,rb,h,sg),mat);
  m.position.set(x,y,z);scene.add(m);return m;
}

function buildMap(){
  B(MAT.sand,500,.2,500,0,0,0);
  [[-30,-20],[25,15],[-10,35],[40,-30],[-45,10],[15,-45]].forEach(([x,z])=>B(MAT.sand2,16,.07,12,x,.05,z));
  B(MAT.road,8,.1,220,0,.05,0);B(MAT.road,220,.1,8,0,.05,0);
  B(MAT.road,6,.1,100,-42,.05,7);B(MAT.road,6,.1,100,42,.05,-7);
  B(MAT.road,100,.1,6,7,.05,42);B(MAT.road,100,.1,6,-7,.05,-42);
  B(MAT.side,1.5,.07,220,4.8,.04,0);B(MAT.side,1.5,.07,220,-4.8,.04,0);
  B(MAT.side,220,.07,1.5,0,.04,4.8);B(MAT.side,220,.07,1.5,0,.04,-4.8);
  let bi=0;
  function bld(cx,cz,bw,bd,fl,lit){
    const wm=MAT.w[bi%4],rm=MAT.roof[bi%2],win=lit?MAT.winL:MAT.win;bi++;
    const H=3.2,tH=fl*H;
    B(wm,bw,tH,bd,cx,tH/2,cz);
    if(fl>1)B(MAT.slab,bw+.1,.1,bd+.1,cx,H,cz);
    B(rm,bw+.4,.3,bd+.4,cx,tH+.15,cz);
    const wc=Math.min(3,Math.floor(bw/2.5));
    for(let f=0;f<fl;f++){
      const wy=f*H+1.9;
      for(let i=0;i<wc;i++){
        const wx=cx-bw/2+bw/(wc+1)*(i+1);
        B(win,.78,1,.07,wx,wy,cz+bd/2+.04);
        B(win,.78,1,.07,wx,wy,cz-bd/2-.04);
      }
    }
    B(MAT.door,1.1,2.1,.1,cx,1.05,cz+bd/2+.05);
    WALLS.push({cx,cz,hw:bw/2,hd:bd/2});
  }
  bld(-22,-22,8,7,2,false);bld(22,-22,6,6,2,true);
  bld(-22,22,7,8,2,false); bld(22,22,8,7,1,true);
  bld(-42,0,7,6,2,false);  bld(42,0,6,7,2,true);
  bld(0,-42,8,6,1,false);  bld(0,42,6,8,2,true);
  bld(-35,-42,5,5,1,false); bld(35,42,5,5,1,true);
  bld(55,-22,7,6,1,false);  bld(-55,22,6,5,2,true);
  bld(0,-70,16,12,2,false); // mansion further away
  bld(55,22,6,6,1,false);   bld(-55,-22,7,5,1,true);
  bld(0,65,8,7,1,false);    bld(70,0,6,6,1,true);
  // cacti (low poly)
  [[-12,-14],[28,10],[-28,-10],[48,16],[-48,-16],[14,-35],[-14,35],[58,7],[-58,-7],[25,-25],[-25,25],[40,40],[-40,-40],[60,-30],[-60,30]].forEach(([x,z])=>{
    C(MAT.cactus,.18,.2,2.2,6,x,1.1,z);
    C(MAT.cactus,.1,.12,1,5,x+.45,1.4,z);
    C(MAT.cactus,.1,.12,1,5,x-.45,1.6,z);
  });
  // rocks
  [[-18,25,1.2],[18,-25,.9],[-32,10,1.4],[32,-10,1.1],[50,30,1.3],[-50,-30,.9],[5,-55,1.5],[65,10,1.0]].forEach(([x,z,s])=>B(MAT.rock,s*1.4,s*.8,s*1.2,x,s*.4,z));
  // lamps (merged into fewer draw calls — just emissive spheres + posts)
  [[-4,16],[4,16],[-4,-16],[4,-16],[-4,36],[4,36],[-4,-36],[4,-36],[16,4],[16,-4],[-16,4],[-16,-4],[36,4],[36,-4],[-36,4],[-36,-4],[52,4],[-52,4],[4,52],[-4,-52]].forEach(([x,z])=>{
    C(MAT.wood,.06,.08,3.2,5,x,1.6,z);
    const b=new THREE.Mesh(new THREE.SphereGeometry(.1,5,5),MAT.glow);b.position.set(x,3.1,z);scene.add(b);
  });
  scene.add(new THREE.AmbientLight(0xffe0a0,2.2));
  const sun=new THREE.DirectionalLight(0xfff0c0,1.3);sun.position.set(30,60,10);scene.add(sun);
}

/* ── CHAR BUILDER ── */
function mkChar(idx){
  const g=new THREE.Group();
  const bodySkin=new THREE.MeshLambertMaterial({color:0xcc3333});
  // feet at Y=0, body goes up
  const body=new THREE.Mesh(GEO.body,bodySkin);body.position.y=.84;g.add(body);
  const head=new THREE.Mesh(GEO.head,MAT.face);head.position.y=1.38;g.add(head);
  // eyes on NEGATIVE Z = front of character
  [-.09,.09].forEach(sx=>{const e=new THREE.Mesh(GEO.eye,MAT.eye);e.position.set(sx,1.38,-.19);g.add(e);});
  const lL=new THREE.Mesh(GEO.leg,MAT.pants);lL.position.set(-.12,.25,0);g.add(lL);
  const lR=new THREE.Mesh(GEO.leg,MAT.pants);lR.position.set(.12,.25,0);g.add(lR);
  const aL=new THREE.Mesh(GEO.arm,bodySkin);aL.position.set(-.34,.84,0);g.add(aL);
  const aR=new THREE.Mesh(GEO.arm,bodySkin);aR.position.set(.34,.84,0);g.add(aR);
  const hand=new THREE.Group();hand.position.set(.38,.7,-.15);hand.scale.set(.7,.7,.7);g.add(hand);
  addHat(g,'top');
  scene.add(g);
  return{g,body,head,lL,lR,aL,aR,hand,sm:bodySkin};
}

function addHat(g,id){
  const hg=new THREE.Group();
  hg.add(new THREE.Mesh(GEO.htBrim,MAT.hBk));
  const cr=new THREE.Mesh(GEO.htCrown,MAT.hBk);cr.position.y=.22;hg.add(cr);
  hg.position.set(0,1.62,0);g.add(hg);
}

function setHandItem(hand,type){
  while(hand.children.length)hand.remove(hand.children[0]);
  // also update first-person hand
  if(fpHand){while(fpHand.children.length)fpHand.remove(fpHand.children[0]);}
  if(type==='knife'){
    const b=new THREE.Mesh(GEO.kBlade,MAT.knife);b.position.y=.25;hand.add(b);
    const h=new THREE.Mesh(GEO.kHand,MAT.knifeH);h.position.y=-.02;hand.add(h);
    if(fpHand){
      // bigger, visible in first person
      const fb=new THREE.Mesh(new THREE.BoxGeometry(.06,.5,.1),MAT.knife);fb.position.set(0,.05,0);fpHand.add(fb);
      const fh=new THREE.Mesh(new THREE.BoxGeometry(.09,.22,.12),MAT.knifeH);fh.position.set(0,-.18,0);fpHand.add(fh);
    }
  } else if(type==='shield'){
    const s=new THREE.Mesh(GEO.shBody,MAT.shield);s.position.y=.3;hand.add(s);
    const bo=new THREE.Mesh(GEO.shBoss,MAT.shBoss);bo.position.y=.3;hand.add(bo);
    if(fpHand){
      const fs=new THREE.Mesh(new THREE.BoxGeometry(.7,.8,.1),MAT.shield);fpHand.add(fs);
      const fb=new THREE.Mesh(new THREE.SphereGeometry(.1,6,6),MAT.shBoss);fpHand.add(fb);
    }
  }
}

/* ── NAME LABEL ── */
function mkLabel(name){
  const cv=document.createElement('canvas');cv.width=200;cv.height=48;
  const ctx=cv.getContext('2d');
  ctx.fillStyle='rgba(0,0,0,.8)';ctx.beginPath();ctx.roundRect(2,2,196,44,7);ctx.fill();
  ctx.fillStyle='#ffe0a0';ctx.font='bold 22px Georgia,serif';
  ctx.textAlign='center';ctx.textBaseline='middle';ctx.fillText(name,100,24);
  const sp=new THREE.Sprite(new THREE.SpriteMaterial({map:new THREE.CanvasTexture(cv),depthTest:false,transparent:true,opacity:0}));
  sp.scale.set(2,.48,1);return sp;
}

// tag sprite above name (SHERIFF / knife icon)
function mkTag(text,color){
  const cv=document.createElement('canvas');cv.width=160;cv.height=40;
  const ctx=cv.getContext('2d');
  ctx.fillStyle=color||'rgba(201,168,76,.85)';ctx.beginPath();ctx.roundRect(2,2,156,36,6);ctx.fill();
  ctx.fillStyle='#000';ctx.font='bold 20px Georgia,serif';
  ctx.textAlign='center';ctx.textBaseline='middle';ctx.fillText(text,80,20);
  const sp=new THREE.Sprite(new THREE.SpriteMaterial({map:new THREE.CanvasTexture(cv),depthTest:false,transparent:true,opacity:0}));
  sp.scale.set(1.6,.4,1);return sp;
}

/* ── SHIELD DROP MESH ── */
function mkShieldDropMesh(){
  const g=new THREE.Group();
  // anonymous corpse lying on ground (no name shown)
  const corpse=new THREE.Mesh(new THREE.BoxGeometry(.48,.12,1.1),new THREE.MeshLambertMaterial({color:0xcc3333}));corpse.position.y=.06;g.add(corpse);
  const chead=new THREE.Mesh(new THREE.BoxGeometry(.36,.12,.36),new THREE.MeshLambertMaterial({color:0xf0c080}));chead.position.set(0,.06,.55);g.add(chead);
  const blood=new THREE.Mesh(GEO.blood,MAT.blood);blood.position.y=.01;g.add(blood);
  // shield lying on top of corpse
  const s=new THREE.Mesh(GEO.shBody,MAT.shield);s.position.set(0,.22,0);s.rotation.x=Math.PI/2;g.add(s);
  const bo=new THREE.Mesh(GEO.shBoss,MAT.shBoss);bo.position.set(0,.23,0);g.add(bo);
  scene.add(g);return g;
}

/* ── KILL CHAR ── */
function killChar(ot){
  ot.alive=false;
  ['body','head','aL','aR','lL','lR'].forEach(k=>{if(ot[k])ot[k].visible=false;});
  ot.g.children.filter(c=>c.isGroup).forEach(c=>c.visible=false);
  if(ot.corpse)ot.corpse.visible=true;
  if(ot.blood)ot.blood.visible=true;
  ot.g.rotation.z=Math.PI/2;
  if(ot.label)ot.label.visible=false;
  if(ot.tag)ot.tag.visible=false; // hide SHERIFF tag on death
  ot.hasSheriff=false;
}

/* ── COLLISION — solid walls, player never goes inside ── */
function collide(p){
  p.x=Math.max(-95,Math.min(95,p.x));p.z=Math.max(-95,Math.min(95,p.z));
  for(const w of WALLS){
    const mg=.55;
    const dx=p.x-w.cx, dz=p.z-w.cz;
    const ox=w.hw+mg-Math.abs(dx);
    const oz=w.hd+mg-Math.abs(dz);
    if(ox>0&&oz>0){
      if(ox<oz) p.x+=ox*Math.sign(dx||.001);
      else       p.z+=oz*Math.sign(dz||.001);
    }
  }
}

/* ── ROLE HUD ── */
function setupRoleHUD(){
  const rp=document.getElementById('rolepill');
  rp.className=G.myRole;
  if(G.myRole==='murderer') rp.textContent='🔴 MÖRDER';
  else if(G.myRole==='sheriff') rp.textContent='⭐ SHERIFF';
  else rp.textContent='🔵 UNSCHULDIG';
  const s1=document.getElementById('slot1'),s2=document.getElementById('slot2');
  if(G.myRole==='murderer'){
    // knife starts locked, shield unlocked
    s1.classList.add('off');document.getElementById('s1i').textContent='🗡️';
    s2.classList.remove('off');document.getElementById('s2i').textContent='🛡️';
  } else if(G.myRole==='sheriff'){
    s1.classList.remove('off');document.getElementById('s1i').textContent='🗡️';
    s2.classList.add('off');
  } else {
    s1.classList.add('off');s2.classList.add('off');
  }
  selSlot(0);
}

window.selSlot=function(i){
  G.curSlot=i;
  document.querySelectorAll('.hs').forEach((s,idx)=>s.classList.toggle('on',idx===i));
  if(!myChar)return;
  if(G.myRole==='murderer'){
    if(i===1&&G.shDropped){
      setHandItem(myChar.hand,'knife');
      window.fbSetKnife&&window.fbSetKnife(1);
    } else if(i===2&&!G.shDropped){
      setHandItem(myChar.hand,'shield');
      window.fbSetKnife&&window.fbSetKnife(2);
    } else {
      setHandItem(myChar.hand,'');
      window.fbSetKnife&&window.fbSetKnife(0);
    }
  } else if(G.myRole==='sheriff'){
    if(i===1){
      setHandItem(myChar.hand,'knife');
      window.fbSetKnife&&window.fbSetKnife(1);
    } else {
      setHandItem(myChar.hand,'');
      window.fbSetKnife&&window.fbSetKnife(0);
    }
  } else {
    setHandItem(myChar.hand,'');
    window.fbSetKnife&&window.fbSetKnife(0);
  }
};

/* ── USE ITEM ── */
window.useItem=async function(){
  if(!G.alive||!G.running)return;
  if(G.myRole==='murderer'){
    if(!G.shDropped){
      // drop shield (must be on slot 2)
      if(G.curSlot!==2)return;
      window.fbDropShield&&window.fbDropShield(PP.x,PP.z);
      G.shDropped=true;
      // hide shield slot, show knife slot
      document.getElementById('slot2').classList.add('off');
      document.getElementById('slot1').classList.remove('off');
      // go to slot 0 (empty hand) — player must manually switch to knife
      G.curSlot=0;
      document.querySelectorAll('.hs').forEach((s,idx)=>s.classList.toggle('on',idx===0));
      setHandItem(myChar.hand,'');
      window.fbSetKnife&&window.fbSetKnife(0);
    } else {
      // shield dropped — same kill logic as sheriff
      const best=nearestAlive(2.6);
      if(best){
        flashRed();notif('🔪 '+best,1500);
        window.fbKill&&window.fbKill(best);
      }
    }
  } else if(G.myRole==='sheriff'){
    if(G.curSlot===1){
      const best=nearestAlive(2.6);
      if(best){
        const targetRole=window._roles&&window._roles[best];
        if(targetRole==='murderer'){
          flashRed();notif('✅ Mörder gestoppt!',3000);
          window.fbKillMurderer&&window.fbKillMurderer(best);
        } else {
          // wrong target — innocent dies AND sheriff slows down
          flashRed();notif('❌ Falsches Ziel! Du wirst langsamer.',2000);
          window.fbKill&&window.fbKill(best);
          G.speedMul=0.35;
          setTimeout(()=>{G.speedMul=1.0;},8000);
        }
      }
    }
  } else {
    if(G.myRole==='murderer'){notif('❌ Du kannst das Schild nicht nehmen!',1200);return;}
    if(shieldDropMesh&&!G.hasShield){
      const dx=PP.x-shieldDropPos.x,dz=PP.z-shieldDropPos.z;
      if(Math.sqrt(dx*dx+dz*dz)<2.5){
        window.fbPickShield&&window.fbPickShield();
        G.hasShield=true;G.myRole='sheriff';
        if(shieldDropMesh){scene.remove(shieldDropMesh);shieldDropMesh=null;}
        document.getElementById('slot1').classList.remove('off');
        document.getElementById('s1i').textContent='🗡️';
        document.getElementById('safepill').style.display='block';
        setupRoleHUD();
        selSlot(1); // auto equip sword
      } else notif('Näher herangehen!',800);
    }
  }
};

function nearestAlive(maxD){
  let best=null,bd=maxD;
  Object.entries(others).forEach(([name,ot])=>{
    if(!ot.alive)return;
    const ox=ot.g.position.x, oz=ot.g.position.z;
    // if other player is still at 0,0 (not yet received position), skip
    if(ox===0&&oz===0)return;
    const dx=ox-PP.x,dz=oz-PP.z;
    const d=Math.sqrt(dx*dx+dz*dz);
    if(d<bd){bd=d;best=name;}
  });
  return best;
}

/* ── DEAD ── */
function showDead(msg){
  document.getElementById('dead').style.display='flex';
  document.getElementById('specbar').style.display='block';
  document.getElementById('deadmsg').textContent=msg||'Du wurdest ermordet.';
  const eb=document.getElementById('escbtn');if(eb)eb.style.display='block';
  if(document.pointerLockElement)document.exitPointerLock();
  G.specIdx=0;updSpec();
}
function updSpec(){
  const k=Object.keys(others).filter(n=>others[n].alive);
  document.getElementById('specname').textContent=k.length?k[((G.specIdx%k.length)+k.length)%k.length]:'Niemand';
}
window.specNext=()=>{G.specIdx++;updSpec();};
window.specPrev=()=>{G.specIdx--;updSpec();};

/* ── START WORLD ── */
window.startWorld=function(lobby){
  Object.values(others).forEach(o=>scene.remove(o.g));
  Object.keys(others).forEach(k=>delete others[k]);
  if(myChar){scene.remove(myChar.g);myChar=null;}
  if(shieldDropMesh){scene.remove(shieldDropMesh);shieldDropMesh=null;}

  G.alive=true;G.curSlot=0;G.shDropped=false;G.hasShield=false;G.isSafe=false;
  G.yaw=0;G.pitch=0;G.velY=0;G.onGround=true;
  document.getElementById('dead').style.display='none';
  document.getElementById('specbar').style.display='none';
  document.getElementById('overlay').classList.add('hide');
  document.getElementById('safepill').style.display='none';

  const myP=lobby.players.find(p=>p.name===G.name);
  PP.set(myP?.pos?.x||2,1.7,myP?.pos?.z||2);
  G.myIdx=lobby.players.findIndex(p=>p.name===G.name);

  myChar=mkChar(G.myIdx);myChar.g.visible=false;
  // first-person hand group
  if(fpHand)scene.remove(fpHand);
  fpHand=new THREE.Group();scene.add(fpHand);

  const bldOthers=new THREE.MeshLambertMaterial({color:0x8b0000,emissive:0x440000,emissiveIntensity:.3});
  lobby.players.forEach((p,i)=>{
    if(p.name===G.name)return;
    const ch=mkChar(i);
    const lbl=mkLabel(p.name);lbl.position.set(0,1.75,0);ch.g.add(lbl);
    const tag=mkTag('','rgba(0,0,0,0)');tag.position.set(0,2.22,0);tag.visible=false;ch.g.add(tag);
    const corp=new THREE.Mesh(GEO.corpse,ch.sm);corp.position.set(0,.06,0);corp.visible=false;ch.g.add(corp);
    const bl=new THREE.Mesh(GEO.blood,MAT.blood);bl.position.set(0,.02,0);bl.visible=false;ch.g.add(bl);
    if(p.pos)ch.g.position.set(p.pos.x,0,p.pos.z);
    others[p.name]={...ch,label:lbl,tag,corpse:corp,blood:bl,alive:!p.elim,wt:0,hasSheriff:false,hasKnife:false};
    // show knife tag immediately if murderer (everyone sees who the murderer is? NO — only show after they equip)
    // knife tag shown via Firebase update when murderer equips
  });

  setupRoleHUD();
  // everyone starts with hand equipped
  if(myChar) setTimeout(()=>{selSlot(0);},200);
  document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));
  document.getElementById('c3d').style.display='block';
  document.getElementById('hud').style.display='block';
  G.running=true;

  // show mobile controls on touch device
  const isTouch='ontouchstart' in window;
  if(isTouch){
    document.getElementById('jzone').style.display='block';
    document.getElementById('lzone').style.display='block';
    document.getElementById('usebtn').style.display='flex';
    document.getElementById('xhair').style.display='none';
    document.getElementById('ctrl').style.display='none';
  }

  // trigger pointer lock on desktop only
  if(!isTouch) setTimeout(()=>document.getElementById('c3d').requestPointerLock(),200);
};

/* ── INPUT ── */
function setupInput(){
  // keyboard
  document.addEventListener('keydown',e=>{
    KEYS[e.code]=true;
    if(!G.running)return;
    if(e.code==='Digit1')selSlot(0);
    if(e.code==='Digit2'){const s=document.getElementById('slot1');if(!s.classList.contains('off'))selSlot(1);}
    if(e.code==='Digit3'){const s=document.getElementById('slot2');if(!s.classList.contains('off'))selSlot(2);}
    if(e.code==='KeyE')window.useItem();
    if(e.code==='Escape')window.leaveGame?.();
    if(e.code==='KeyP'&&!G.alive)window.specNext();
    if(e.code==='KeyO'&&!G.alive)window.specPrev();
  });
  document.addEventListener('keyup',e=>{KEYS[e.code]=false;});
  // mouse look
  document.addEventListener('mousemove',e=>{
    if(!G.pLocked||!G.running)return;
    G.yaw-=e.movementX*.0022;G.pitch-=e.movementY*.0022;
    G.pitch=Math.max(-Math.PI/2+.05,Math.min(Math.PI/2-.05,G.pitch));
  });
  document.addEventListener('pointerlockchange',()=>G.pLocked=!!document.pointerLockElement);
  document.getElementById('c3d').addEventListener('click',()=>{
    if(!G.running)return;
    if(!G.pLocked){document.getElementById('c3d').requestPointerLock();return;}
    window.useItem();
  });

  // MOBILE JOYSTICK
  const jzone=document.getElementById('jzone');
  const jknob=document.getElementById('jknob');
  let jOrig={x:0,y:0},jDelta={x:0,y:0};
  jzone.addEventListener('touchstart',e=>{e.preventDefault();const t=e.touches[0];jOrig={x:t.clientX,y:t.clientY};jDelta={x:0,y:0};},{passive:false});
  jzone.addEventListener('touchmove',e=>{
    e.preventDefault();const t=e.touches[0];
    const dx=t.clientX-jOrig.x,dy=t.clientY-jOrig.y;
    const R=45,dist=Math.min(Math.sqrt(dx*dx+dy*dy),R),ang=Math.atan2(dy,dx);
    jDelta={x:Math.cos(ang)*dist/R,y:Math.sin(ang)*dist/R};
    jknob.style.left=(33+jDelta.x*33)+'px';jknob.style.top=(33+jDelta.y*33)+'px';
  },{passive:false});
  const stopJ=()=>{jDelta={x:0,y:0};jknob.style.left='33px';jknob.style.top='33px';};
  jzone.addEventListener('touchend',stopJ);jzone.addEventListener('touchcancel',stopJ);
  window._jDelta=jDelta;

  // LOOK ZONE
  const lzone=document.getElementById('lzone');
  let lLast={x:0,y:0},lActive=false;
  lzone.addEventListener('touchstart',e=>{e.preventDefault();lActive=true;const t=e.touches[0];lLast={x:t.clientX,y:t.clientY};},{passive:false});
  lzone.addEventListener('touchmove',e=>{
    e.preventDefault();if(!lActive||!G.running)return;
    const t=e.touches[0];
    G.yaw-=(t.clientX-lLast.x)*.006;
    G.pitch-=(t.clientY-lLast.y)*.006;
    G.pitch=Math.max(-Math.PI/2+.05,Math.min(Math.PI/2-.05,G.pitch));
    lLast={x:t.clientX,y:t.clientY};
  },{passive:false});
  lzone.addEventListener('touchend',()=>lActive=false);
  lzone.addEventListener('touchcancel',()=>lActive=false);
}

/* ── GAME LOOP ── */
function gameLoop(){
  requestAnimationFrame(gameLoop);
  if(!renderer||!G.running){if(renderer)renderer.render(scene,camera);return;}
  const dt=Math.min(clock.getDelta(),.05);
  const t=clock.elapsedTime;

  // SPECTATE
  if(!G.alive){
    const k=Object.keys(others).filter(n=>others[n].alive);
    if(k.length){
      const idx=((G.specIdx%k.length)+k.length)%k.length;
      const ot=others[k[idx]];
      if(ot){
        const angle=ot.g.rotation.y;
        camera.position.set(ot.g.position.x+Math.sin(angle)*5,ot.g.position.y+2.5,ot.g.position.z+Math.cos(angle)*5);
        camera.lookAt(ot.g.position.x,ot.g.position.y+1.2,ot.g.position.z);
      }
    }
    updSpec();
    tickOthers(dt);renderer.render(scene,camera);return;
  }

  // MOVE — keyboard + joystick
  const jd=window._jDelta||{x:0,y:0};
  _cd.set(Math.sin(G.yaw),0,Math.cos(G.yaw));
  _cr.set(Math.cos(G.yaw),0,-Math.sin(G.yaw));
  _mv.set(0,0,0);
  if(KEYS['KeyW']||KEYS['ArrowUp'])   _mv.sub(_cd);
  if(KEYS['KeyS']||KEYS['ArrowDown']) _mv.add(_cd);
  if(KEYS['KeyA']||KEYS['ArrowLeft']) _mv.sub(_cr);
  if(KEYS['KeyD']||KEYS['ArrowRight'])_mv.add(_cr);
  // joystick
  if(Math.abs(jd.x)>.05||Math.abs(jd.y)>.05){
    _mv.addScaledVector(_cr,jd.x);
    _mv.addScaledVector(_cd,-jd.y);
  }
  const mov=_mv.lengthSq()>.001;
  const spd=5.5*(G.speedMul||1.0);
  if(mov){walkT+=dt*7;_mv.normalize().multiplyScalar(spd*dt);PP.x+=_mv.x;PP.z+=_mv.z;}else walkT*=.85;
  if(KEYS['Space']&&G.onGround){G.velY=7;G.onGround=false;}
  G.velY-=18*dt;PP.y+=G.velY*dt;
  if(PP.y<=1.7){PP.y=1.7;G.velY=0;G.onGround=true;}
  collide(PP);

  // CAMERA — first person
  camera.position.copy(PP);
  camera.rotation.y=G.yaw;
  camera.rotation.x=G.pitch;
  if(myChar)myChar.g.visible=false;

  // First-person hand — bottom right, follows camera
  if(fpHand){
    const hOff=new THREE.Vector3(.32,-.30,-.48);
    hOff.applyEuler(new THREE.Euler(G.pitch,G.yaw,0,'YXZ'));
    fpHand.position.set(PP.x+hOff.x,PP.y+hOff.y,PP.z+hOff.z);
    fpHand.rotation.order='YXZ';
    fpHand.rotation.y=G.yaw+Math.PI;
    fpHand.rotation.x=G.pitch*.3;
  }

  // MY CHAR
  if(myChar){
    myChar.g.position.set(PP.x,PP.y-1.7,PP.z);
    myChar.g.rotation.y=G.yaw;
    myChar.g.visible=false;
    if(mov){myChar.lL.rotation.x=Math.sin(walkT)*.55;myChar.lR.rotation.x=-Math.sin(walkT)*.55;myChar.aL.rotation.x=-Math.sin(walkT)*.45;myChar.aR.rotation.x=Math.sin(walkT)*.45;}
    else{myChar.lL.rotation.x*=.8;myChar.lR.rotation.x*=.8;myChar.aL.rotation.x*=.8;myChar.aR.rotation.x*=.8;}
  }

  // SHIELD DROP BOB
  if(shieldDropMesh){shieldDropMesh.rotation.y+=dt*0.3;}

  tickOthers(dt);
  renderer.render(scene,camera);
}

function tickOthers(dt){
  Object.values(others).forEach(ot=>{
    if(!ot.alive)return;
    ot.wt+=dt*3;
    if(ot.lL)ot.lL.rotation.x=Math.sin(ot.wt)*.3;
    if(ot.lR)ot.lR.rotation.x=-Math.sin(ot.wt)*.3;
    const dx=PP.x-ot.g.position.x,dz=PP.z-ot.g.position.z;
    const dist=Math.sqrt(dx*dx+dz*dz);
    // name only within 8m
    const tgt=dist<8?Math.min(1,(8-dist)/3):0;
    if(ot.label)ot.label.material.opacity+=(tgt-ot.label.material.opacity)*.15;
    // sheriff tag always visible, others hidden
    if(ot.tag)ot.tag.material.opacity=ot.hasSheriff?1:0;
  });
}

// exposed callbacks
window.killOther=name=>{const ot=others[name];if(ot)killChar(ot);};
window.updateOtherPos=(name,x,y,z,ry)=>{
  const ot=others[name];if(!ot)return;
  ot.g.position.x=x;
  ot.g.position.z=z;
  if(y!==undefined)ot.g.position.y=y-1.7;
  if(ry!==undefined){
    let diff=ry-(ot.g.rotation.y||0);
    while(diff>Math.PI)diff-=Math.PI*2;
    while(diff<-Math.PI)diff+=Math.PI*2;
    ot.g.rotation.y+=diff*.25;
  }
};
window.updateOtherTag=(name,type)=>{
  const ot=others[name];if(!ot)return;
  if(type==='sheriff'){
    ot.hasSheriff=true;
    if(ot.tag){
      const cv=document.createElement('canvas');cv.width=180;cv.height=44;
      const ctx=cv.getContext('2d');
      ctx.fillStyle='rgba(201,168,76,.95)';ctx.beginPath();ctx.roundRect(2,2,176,40,8);ctx.fill();
      ctx.fillStyle='#000';ctx.font='bold 22px Georgia,serif';
      ctx.textAlign='center';ctx.textBaseline='middle';ctx.fillText('⭐ SHERIFF',90,22);
      ot.tag.material.map=new THREE.CanvasTexture(cv);ot.tag.material.needsUpdate=true;
      ot.tag.material.opacity=1; // always visible
      ot.tag.visible=true;
    }
  } else if(type==='knife'){
    ot.hasKnife=true;
    if(ot.hand){
      while(ot.hand.children.length)ot.hand.remove(ot.hand.children[0]);
      const b=new THREE.Mesh(GEO.kBlade,MAT.knife);b.position.y=.25;ot.hand.add(b);
      const h=new THREE.Mesh(GEO.kHand,MAT.knifeH);h.position.y=-.02;ot.hand.add(h);
    }
  } else if(type==='shield'){
    if(ot.hand){
      while(ot.hand.children.length)ot.hand.remove(ot.hand.children[0]);
      const s=new THREE.Mesh(GEO.shBody,MAT.shield);s.position.y=.3;ot.hand.add(s);
      const bo=new THREE.Mesh(GEO.shBoss,MAT.shBoss);bo.position.y=.3;ot.hand.add(bo);
    }
  } else if(type==='noknife'){
    ot.hasKnife=false;
    if(ot.hand){while(ot.hand.children.length)ot.hand.remove(ot.hand.children[0]);}
  }
};
window.onShieldDrop=(x,z)=>{
  G.shDropped=true;shieldDropPos={x,z};
  // everyone sees shield — murderer sees it but can't pick it up
  if(!shieldDropMesh)shieldDropMesh=mkShieldDropMesh();
  shieldDropMesh.position.set(x,.4,z);
};
window.onShieldPickedUp=()=>{
  if(shieldDropMesh){scene.remove(shieldDropMesh);shieldDropMesh=null;}
  // murderer keeps shDropped=true so he can still kill!
  if(G.myRole!=='murderer') G.shDropped=false;
  shieldDropPos={x:0,z:0};
};
window.onSelfKilled=msg=>{G.alive=false;showDead(msg||'Du wurdest ermordet.');};
window.gameOver=(winner,mName)=>{
  G.running=false;
  if(document.pointerLockElement)document.exitPointerLock();
  document.getElementById('hud').style.display='none';
  document.getElementById('dead').style.display='none';
  document.getElementById('specbar').style.display='none';
  const icon=winner==='murderer'?'🩸':'🔍';
  const title=winner==='murderer'?'DER MÖRDER GEWINNT':'GERECHTIGKEIT SIEGT';
  const sub=winner==='murderer'?mName+' entkommt unerkannt.':'Der Mörder wurde gestoppt!';
  showOv(icon,title,sub);
  setTimeout(()=>window.resetAll(),5000);
};
</script>

<!-- Firebase module -->
<script type="module">
import{initializeApp}from"https://www.gstatic.com/firebasejs/10.12.0/firebase-app.js";
import{getDatabase,ref,set,get,onValue,update,remove}from"https://www.gstatic.com/firebasejs/10.12.0/firebase-database.js";
const FB={apiKey:"AIzaSyAtLemnwT80X4DbEEVUQzOCezGcPFjxHzs",authDomain:"murdermysery-8bbe3.firebaseapp.com",databaseURL:"https://murdermysery-8bbe3-default-rtdb.firebaseio.com",projectId:"murdermysery-8bbe3",storageBucket:"murdermysery-8bbe3.firebasestorage.app",messagingSenderId:"74585023201",appId:"1:74585023201:web:c691c0919a1db66a52cda0"};
const app=initializeApp(FB);
const db=getDatabase(app);
document.getElementById('conn').classList.add('hide');
document.getElementById('s-title').classList.add('active');

const AV=['🎩','🕵️','👑','🦹','🧙','🥀','⚔️','🌹'];
let unsub=null;
let kickTarget=null;
const lRef=c=>ref(db,'mm3d3/'+c);
const getL=async c=>{const s=await get(lRef(c));return s.exists()?s.val():null;};
const saveL=(c,d)=>set(lRef(c),d);
const updL=(c,d)=>update(lRef(c),d);
const delL=c=>remove(lRef(c));
function watchL(code,cb){if(unsub)unsub();unsub=onValue(lRef(code),s=>{if(s.exists())cb(s.val());});}
function mkCode(){return String(Math.floor(1000+Math.random()*9000));}
document.getElementById('new-code').textContent=mkCode();

window.showKick=function(name){
  if(!G.isHost||name===G.name)return;
  kickTarget=name;
  document.getElementById('kick-name').textContent=name;
  document.getElementById('kick-dialog').style.display='flex';
};
window.confirmKick=async function(){
  document.getElementById('kick-dialog').style.display='none';
  if(!kickTarget)return;
  const l=await getL(G.code);if(!l)return;
  if(!l.kicked)l.kicked=[];
  l.kicked.push(kickTarget);
  l.players=l.players.filter(p=>p.name!==kickTarget);
  await saveL(G.code,l);
  kickTarget=null;
};

window.createLobby=async()=>{
  const name=document.getElementById('host-name').value.trim();
  if(!name){window.toast('Name eingeben!');return;}
  const code=document.getElementById('new-code').textContent;
  G.name=name;G.code=code;G.isHost=true;G.myIdx=0;
  const sp=window.SPAWNS?.[0]||{x:2,z:2};
  await saveL(code,{code,host:name,started:0,phase:'lobby',roles:{},
    players:[{name,avatar:AV[0],isHost:1,elim:0,role:null,safe:0,pos:{x:sp[0]||2,z:sp[1]||2}}],ts:Date.now()});
  document.getElementById('h-code-show').textContent=code;
  window.go('s-lobby');
  let prevNames=[];
  watchL(code,l=>{
    if(!l)return;
    const curNames=l.players.map(p=>p.name);
    prevNames.forEach(n=>{if(!curNames.includes(n)&&n!==G.name)window.toast('👋 '+n+' hat verlassen.');});
    prevNames=curNames;
    document.getElementById('hcount').textContent=l.players.length+' Spieler';
    document.getElementById('hplist').innerHTML=l.players.map((p,i)=>
      `<li class="pitem" onclick="showKick('${p.name}')" style="cursor:${G.isHost&&i>0?'pointer':'default'}">
        <div class="pdot ${i===0?'gold':''}"></div>
        <span class="pname">${p.avatar} ${p.name}</span>
        ${i===0?'<span class="ptag">HOST</span>':G.isHost?'<span class="ptag" style="color:var(--blood)">KICK</span>':''}
      </li>`
    ).join('');
    if(l.phase==='countdown'){if(unsub)unsub();startCD(l);}
  });
};

window.joinLobby=async()=>{
  const name=document.getElementById('join-name').value.trim();
  const code=document.getElementById('join-code').value.trim();
  if(!name||!code){window.toast('Name und Code eingeben!');return;}
  const l=await getL(code);
  if(!l){window.toast('Lobby nicht gefunden!');return;}
  if(l.started){window.toast('Läuft bereits.');return;}
  if(l.players.find(p=>p.name===name)){window.toast('Name vergeben!');return;}
  const idx=l.players.length;
  const SPAWNS=[[2,2],[9,6],[-9,-6],[13,-11],[-6,13],[18,1],[-16,8],[4,-20]];
  const sp=SPAWNS[idx%SPAWNS.length];
  l.players.push({name,avatar:AV[idx%AV.length],isHost:0,elim:0,role:null,safe:0,pos:{x:sp[0],z:sp[1]}});
  await saveL(code,l);
  G.name=name;G.code=code;G.isHost=false;G.myIdx=idx;
  document.getElementById('j-code-show').textContent=code;
  window.go('s-join-lobby');
  watchL(code,ll=>{
    if(!ll){window.toast('Lobby geschlossen!');window.resetAll();return;}
    if(ll.kicked&&ll.kicked.includes(G.name)){window.toast('Du wurdest gekickt!');window.resetAll();return;}
    document.getElementById('jcount').textContent=ll.players.length+' Spieler';
    document.getElementById('jplist').innerHTML=ll.players.map(p=>
      `<li class="pitem"><div class="pdot ${p.isHost?'gold':''}"></div><span class="pname">${p.avatar} ${p.name}</span>${p.isHost?'<span class="ptag">HOST</span>':''}</li>`
    ).join('');
    if(ll.phase==='countdown'){if(unsub)unsub();startCD(ll);}
  });
};

window.startGame=async()=>{
  const l=await getL(G.code);if(!l)return;
  if(l.players.length<2){window.toast('Min. 2 Spieler!');return;}
  const roles={};
  const murdererIdx=Math.floor(Math.random()*l.players.length);
  l.players.forEach((p,i)=>{p.role=i===murdererIdx?'murderer':'innocent';roles[p.name]=p.role;});
  l.roles=roles;l.started=1;l.phase='countdown';
  l.shield={dropped:false,x:0,z:0};
  await saveL(G.code,l);
  startCD(l);
};

function startCD(l){
  window.go('s-countdown');
  let n=10;
  const el=document.getElementById('cdn');
  el.textContent=n;el.classList.remove('red');
  const iv=setInterval(()=>{
    n--;el.textContent=n;
    if(n<=5)el.classList.add('red');
    if(n<=0){clearInterval(iv);G.myRole=l.roles[G.name]||'innocent';showRole(l);}
  },1000);
}

function showRole(l){
  const RD={murderer:{icon:'🗡️',label:'MÖRDER',desc:'Töte alle. Droppe das Schild — wer es aufhebt wird Sheriff!'},innocent:{icon:'🕊️',label:'UNSCHULDIG',desc:'Finde das Schild — du wirst Sheriff und bekommst ein Messer!'}};
  const r=RD[G.myRole]||RD.innocent;
  document.getElementById('r-icon').textContent=r.icon;
  const rl=document.getElementById('r-label');rl.textContent=r.label;rl.className='rl '+G.myRole;
  document.getElementById('r-desc').textContent=r.desc;
  window.go('s-role');
  let c=3;document.getElementById('r-cd').textContent=c;
  const iv=setInterval(()=>{c--;document.getElementById('r-cd').textContent=c;if(c<=0){clearInterval(iv);enterWorld(l);}},1000);
}

function enterWorld(l){
  window._roles=l.roles;
  G.myIdx=l.players.findIndex(p=>p.name===G.name);
  window.initThree();
  setTimeout(()=>{
    window.startWorld(l);
    // pos sync - 100ms for smooth movement
    const posIv=setInterval(async()=>{
      if(!G.running){clearInterval(posIv);return;}
      if(G.myIdx<0)return;
      await updL(G.code,{
        [`players/${G.myIdx}/pos`]:{x:Math.round(PP.x*10)/10,y:Math.round(PP.y*10)/10,z:Math.round(PP.z*10)/10},
        [`players/${G.myIdx}/ry`]:+G.yaw.toFixed(3)
      });
    },100);

    // auto-drop shield after 2 minutes if murderer hasn't dropped it
    if(G.myRole==='murderer'){
      setTimeout(async()=>{
        if(!G.running||G.shDropped)return;
        window.fbDropShield&&window.fbDropShield(PP.x,PP.z);
        G.shDropped=true;
        document.getElementById('slot2').classList.add('off');
        document.getElementById('slot1').classList.remove('off');
        G.curSlot=0;
        document.querySelectorAll('.hs').forEach((s,idx)=>s.classList.toggle('on',idx===0));
        if(myChar){setHandItem(myChar.hand,'');window.fbSetKnife&&window.fbSetKnife(0);}
      },120000);
    }

    watchL(G.code,ll=>{
      if(!ll||!G.running)return;
      ll.players.forEach(p=>{
        if(p.name===G.name){if(p.elim&&G.alive){G.alive=false;window.onSelfKilled('Du wurdest ermordet.');} return;}
        if(p.pos)window.updateOtherPos(p.name,p.pos.x,p.pos.y,p.pos.z,p.ry);
        if(p.elim)window.killOther(p.name);
        if(p.isSheriff){window.updateOtherTag(p.name,'sheriff');if(window._roles)window._roles[p.name]='sheriff';}
        if(p.knifeOut===1)window.updateOtherTag(p.name,'knife');
        else if(p.knifeOut===2)window.updateOtherTag(p.name,'shield');
        else window.updateOtherTag(p.name,'noknife');
      });
      // remove players who left
      Object.keys(others).forEach(name=>{
        if(!ll.players.find(p=>p.name===name))window.killOther(name);
      });
      if(ll.shield?.dropped){
        if(!G.shDropped){
          G.shDropped=true;
          window.onShieldDrop(ll.shield.x,ll.shield.z);
        }
      }
      if(ll.shield&&!ll.shield.dropped&&G.shDropped){
        window.onShieldPickedUp();
      }
      if(ll.phase==='ended'){
        const mn=ll.players.find(p=>p.role==='murderer')?.name||'?';
        window.gameOver(ll.winner||'murderer',mn);
      }
    });
  },150);
}

// FB actions
window.fbKillMurderer=async name=>{
  const l=await getL(G.code);if(!l)return;
  const ti=l.players.findIndex(p=>p.name===name);if(ti<0)return;
  await updL(G.code,{[`players/${ti}/elim`]:1,phase:'ended',winner:'innocents'});
};
window.fbKillSelf=async()=>{
  if(G.myIdx<0)return;
  await updL(G.code,{[`players/${G.myIdx}/elim`]:1});
  // check if murderer now wins
  const l=await getL(G.code);if(!l)return;
  const aliveNM=l.players.filter(p=>!p.elim&&p.role!=='murderer');
  if(aliveNM.length===0)await updL(G.code,{phase:'ended',winner:'murderer'});
};
window.fbKill=async name=>{
  const l=await getL(G.code);if(!l)return;
  const ti=l.players.findIndex(p=>p.name===name);if(ti<0)return;
  const victim=l.players[ti];
  if(!victim||victim.elim)return; // already dead
  const updates={[`players/${ti}/elim`]:1};
  // if sheriff is killed, drop shield at their position
  if(victim.isSheriff&&victim.pos){
    updates['shield']={dropped:true,x:victim.pos.x||0,z:victim.pos.z||0};
  }
  await updL(G.code,updates);
  const l2=await getL(G.code);
  const aliveNonMurder=l2.players.filter(p=>!p.elim&&p.role!=='murderer');
  if(aliveNonMurder.length===0)await updL(G.code,{phase:'ended',winner:'murderer'});
};

// Kill nearest using Firebase live positions
window.fbKillNearest=async()=>{
  const l=await getL(G.code);if(!l)return;
  let best=null,bd=99;
  l.players.forEach(p=>{
    if(p.name===G.name||p.elim||p.role==='murderer')return;
    if(!p.pos)return;
    const dx=p.pos.x-PP.x, dz=p.pos.z-PP.z;
    const d=Math.sqrt(dx*dx+dz*dz);
    if(d<bd){bd=d;best=p.name;}
  });
  if(best&&bd<8){
    flashRed();notif('🔪 '+best,1500);
    window.fbKill(best);
  } else {
    notif('Zu weit!',800);
  }
};
window.fbSetKnife=async(val)=>{
  if(G.myIdx<0)return;
  await updL(G.code,{[`players/${G.myIdx}/knifeOut`]:val||0});
};
window.fbDropShield=async(x,z)=>{
  await updL(G.code,{shield:{dropped:true,x,z}});
  if(G.myIdx>=0)await updL(G.code,{[`players/${G.myIdx}/shieldDropped`]:1});
};
window.fbPickShield=async()=>{
  // shield picked up → remove from ground, mark player as sheriff
  await updL(G.code,{shield:{dropped:false,x:0,z:0}});
  if(G.myIdx>=0)await updL(G.code,{[`players/${G.myIdx}/safe`]:1,[`players/${G.myIdx}/isSheriff`]:1});
};

window.leaveGame=async()=>{
  if(unsub)unsub();G.running=false;
  if(G.isHost){
    await delL(G.code);
  } else {
    const l=await getL(G.code);
    if(l){
      if(G.myIdx>=0)await updL(G.code,{[`players/${G.myIdx}/elim`]:1});
      setTimeout(async()=>{
        const l2=await getL(G.code);
        if(l2){l2.players=l2.players.filter(p=>p.name!==G.name);await saveL(G.code,l2);}
      },500);
    }
  }
  window.resetAll();
};
window.resetAll=async()=>{
  G.running=false;
  // if in a lobby but game not started, remove self from Firebase
  if(G.code&&!G.isHost){
    try{
      const l=await getL(G.code);
      if(l&&!l.started){
        l.players=l.players.filter(p=>p.name!==G.name);
        await saveL(G.code,l);
      }
    }catch(e){}
  }
  if(unsub){unsub();unsub=null;}
  document.getElementById('c3d').style.display='none';
  document.getElementById('hud').style.display='none';
  document.getElementById('dead').style.display='none';
  document.getElementById('specbar').style.display='none';
  document.getElementById('overlay').classList.add('hide');
  document.getElementById('new-code').textContent=mkCode();
  ['host-name','join-name','join-code'].forEach(id=>{const e=document.getElementById(id);if(e)e.value='';});
  G.code='';G.name='';G.isHost=false;
  window.go('s-title');
};
</script>
</body>
</html>
