[index .html](https://github.com/user-attachments/files/26383319/index.html)
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Murder Mystery 3D</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700;900&family=Crimson+Pro:ital,wght@0,300;0,400;1,300&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent;}
html,body{width:100%;height:100%;overflow:hidden;background:#07050a;color:var(--gtext);font-family:'Crimson Pro',serif;touch-action:none;}
:root{--blood:#8b0000;--gold:#c9a84c;--gcard:#13100d;--gborder:#2a2218;--gtext:#d4c9a8;--gmuted:#7a6e58;}
#c3d{position:fixed;top:0;left:0;width:100%;height:100%;display:none;z-index:1;}
.gscreen{display:none;position:fixed;inset:0;z-index:50;flex-direction:column;align-items:center;justify-content:center;padding:1.5rem;background:#07050a;}
.gscreen.active{display:flex;}
#gs-title{text-align:center;gap:1.8rem;}
.gblade{font-size:2.8rem;display:inline-block;animation:gfl 3s ease-in-out infinite;}
@keyframes gfl{0%,100%{transform:rotate(-15deg) translateY(0);}50%{transform:rotate(-15deg) translateY(-10px);}}
h1{font-family:'Cinzel',serif;font-weight:900;font-size:clamp(2.8rem,9vw,5.5rem);line-height:.95;letter-spacing:.04em;color:#fff;text-shadow:0 0 50px rgba(139,0,0,.5),0 3px 0 var(--blood);}
h1 em{color:var(--blood);font-style:normal;}
.gtagline{font-style:italic;color:var(--gmuted);letter-spacing:.25em;text-transform:uppercase;font-size:1rem;}
.gornament{color:var(--gmuted);letter-spacing:.4em;font-size:.8rem;}
.gmenu{display:flex;flex-direction:column;gap:.9rem;width:100%;max-width:300px;}
.gbtn{font-family:'Cinzel',serif;font-size:.95rem;letter-spacing:.1em;padding:.9rem 1.8rem;border:1px solid var(--gborder);background:var(--gcard);color:var(--gtext);cursor:pointer;}
.gbtn-red{background:var(--blood);border-color:var(--blood);color:#fff;}
.gpanel{background:var(--gcard);border:1px solid var(--gborder);padding:2.2rem;width:100%;max-width:400px;position:relative;}
.gpanel::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--gold),transparent);}
h2{font-family:'Cinzel',serif;font-size:1.3rem;color:var(--gold);margin-bottom:1.4rem;letter-spacing:.1em;}
label{display:block;font-size:.75rem;letter-spacing:.2em;text-transform:uppercase;color:var(--gmuted);margin-bottom:.45rem;}
input[type=text]{width:100%;background:rgba(255,255,255,.03);border:1px solid var(--gborder);color:var(--gtext);font-family:'Crimson Pro',serif;font-size:1.1rem;padding:.7rem .9rem;outline:none;}
input[type=text]:focus{border-color:var(--gold);}
input[type=text]::placeholder{color:var(--gmuted);}
.gfield{margin-bottom:1.1rem;}
.glink-btn{background:none;border:none;color:var(--gmuted);cursor:pointer;font-family:'Crimson Pro',serif;font-style:italic;font-size:.95rem;margin-top:.8rem;}
.gcodebox{background:rgba(139,0,0,.12);border:1px solid var(--blood);padding:1.2rem;text-align:center;margin:1.3rem 0;}
.gcodebox small{font-size:.7rem;letter-spacing:.25em;text-transform:uppercase;color:var(--gmuted);display:block;margin-bottom:.4rem;}
.gcodebox strong{font-family:'Cinzel',serif;font-size:2.8rem;letter-spacing:.35em;color:#fff;}
#gs-lobby,#gs-join-lobby{gap:1.2rem;}
.globby-wrap{background:var(--gcard);border:1px solid var(--gborder);padding:1.8rem;width:100%;max-width:480px;position:relative;}
.globby-wrap::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--gold),transparent);}
.globby-top{display:flex;justify-content:space-between;align-items:center;margin-bottom:1.2rem;}
.gpcount{font-size:.82rem;color:var(--gmuted);}
.gplist{list-style:none;min-height:60px;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.3rem;}
.gpitem{display:flex;align-items:center;gap:.7rem;padding:.55rem .9rem;background:rgba(255,255,255,.02);border:1px solid var(--gborder);}
.gpdot{width:7px;height:7px;border-radius:50%;background:var(--blood);flex-shrink:0;}
.gpdot.gold{background:var(--gold);}
.gpname{flex:1;font-size:1rem;}
.gptag{font-size:.68rem;letter-spacing:.12em;text-transform:uppercase;color:var(--gold);}
.ghint{font-size:.83rem;color:var(--gmuted);font-style:italic;margin-bottom:1rem;text-align:center;}
#gs-countdown{gap:.5rem;}
#gcdn{font-family:'Cinzel',serif;font-size:clamp(7rem,28vw,14rem);color:#fff;line-height:1;text-shadow:0 0 80px rgba(139,0,0,.8);}
#gcdn.red{color:var(--blood);}
#gcdsub{font-family:'Cinzel',serif;font-size:.9rem;letter-spacing:.3em;color:var(--gmuted);text-transform:uppercase;}
#gs-role{gap:1.6rem;}
.grc{background:var(--gcard);border:1px solid var(--gborder);padding:2.8rem 2.4rem;width:100%;max-width:340px;text-align:center;position:relative;}
.grc::before,.grc::after{content:'';position:absolute;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--blood),transparent);}
.grc::before{top:0;}.grc::after{bottom:0;}
.gri{font-size:3.5rem;display:block;margin-bottom:1rem;}
.grl{font-family:'Cinzel',serif;font-size:2rem;font-weight:900;letter-spacing:.08em;margin-bottom:.6rem;}
.grl.murderer{color:var(--blood);}
.grl.innocent{color:#8ab4a0;}
.grl.sheriff{color:var(--gold);}
.grd{font-style:italic;color:var(--gmuted);font-size:1rem;line-height:1.6;}
.grh{font-size:.75rem;color:var(--gmuted);letter-spacing:.1em;opacity:.6;}
.grh2{font-size:.8rem;color:var(--blood);margin-top:6px;letter-spacing:.06em;}
.goverlay{position:fixed;inset:0;background:rgba(7,5,10,.96);z-index:200;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:2rem;}
.goverlay.hide{display:none;}
.gov-icon{font-size:3.5rem;margin-bottom:.9rem;}
.gov-title{font-family:'Cinzel',serif;font-size:clamp(1.4rem,5vw,2.3rem);font-weight:700;margin-bottom:.7rem;}
.gov-sub{font-style:italic;color:var(--gmuted);font-size:1.05rem;max-width:380px;line-height:1.65;margin-bottom:1.8rem;}
.gtoast{position:fixed;top:1.3rem;right:1.3rem;background:var(--gcard);border:1px solid var(--gold);padding:.65rem 1.1rem;font-size:.97rem;z-index:500;max-width:260px;animation:gti .3s ease,gto .3s ease 2.6s forwards;}
@keyframes gti{from{transform:translateX(110%);opacity:0;}to{transform:none;opacity:1;}}
@keyframes gto{to{transform:translateX(20px);opacity:0;}}
.gconn{position:fixed;inset:0;background:rgba(7,5,10,.97);z-index:600;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:1rem;}
.gconn.hide{display:none;}
.gspinner{width:40px;height:40px;border:3px solid var(--gborder);border-top-color:var(--blood);border-radius:50%;animation:gspin 1s linear infinite;}
@keyframes gspin{to{transform:rotate(360deg);}}
.gconn-txt{font-family:'Cinzel',serif;font-size:.9rem;letter-spacing:.15em;color:var(--gmuted);}
#ghud{position:fixed;top:0;left:0;width:100%;height:100%;z-index:10;pointer-events:none;display:none;}
#gxhair{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);width:14px;height:14px;}
#gxhair::before,#gxhair::after{content:'';position:absolute;background:rgba(255,210,100,.9);}
#gxhair::before{width:2px;height:100%;left:50%;transform:translateX(-50%);}
#gxhair::after{height:2px;width:100%;top:50%;transform:translateY(-50%);}
#grolepill{position:absolute;top:14px;right:14px;padding:6px 16px;font-family:'Cinzel',serif;font-size:.78rem;letter-spacing:.12em;text-transform:uppercase;border:1px solid;border-radius:2px;background:rgba(0,0,0,.9);}
#grolepill.murderer{border-color:var(--blood);color:#ff4444;}
#grolepill.innocent{border-color:#334488;color:#aabbff;}
#grolepill.sheriff{border-color:var(--gold);color:var(--gold);}
#gsafepill{position:absolute;top:50px;right:14px;padding:5px 14px;font-family:'Cinzel',serif;font-size:.75rem;letter-spacing:.1em;border-radius:2px;background:rgba(0,80,0,.5);border:1px solid #226622;color:#55ee55;display:none;}
#gshieldtimer{position:absolute;top:90px;right:14px;padding:5px 14px;font-family:'Cinzel',serif;font-size:.75rem;letter-spacing:.1em;border-radius:2px;background:rgba(139,0,0,.5);border:1px solid var(--blood);color:#ff6666;display:none;}
#ghotbar{position:absolute;bottom:48px;left:50%;transform:translateX(-50%);display:flex;gap:6px;}
.ghs{width:58px;height:58px;background:rgba(0,0,0,.85);border:2px solid #333;border-radius:3px;display:flex;flex-direction:column;align-items:center;justify-content:center;font-size:1.55rem;position:relative;pointer-events:all;cursor:pointer;}
.ghs.on{border-color:var(--gold);}
.ghs.off{display:none;}
.ghk{position:absolute;top:3px;left:5px;font-size:.52rem;color:#555;font-family:'Cinzel',serif;}
#gctrl{position:absolute;bottom:12px;left:50%;transform:translateX(-50%);background:rgba(0,0,0,.72);border:1px solid #1a1208;color:#4a3820;font-size:10px;letter-spacing:.09em;padding:5px 14px;font-family:'Cinzel',serif;white-space:nowrap;}
#gescbtn{position:absolute;bottom:12px;right:14px;padding:8px 14px;background:rgba(0,0,0,.8);border:1px solid #333;color:#555;cursor:pointer;font-family:'Cinzel',serif;font-size:.72rem;letter-spacing:.1em;pointer-events:all;border-radius:2px;display:none;}
#gjzone{position:absolute;bottom:80px;left:20px;width:110px;height:110px;pointer-events:all;display:none;}
#gjbase{position:absolute;inset:0;border-radius:50%;background:rgba(0,0,0,.35);border:2px solid rgba(201,168,76,.25);}
#gjknob{position:absolute;width:44px;height:44px;border-radius:50%;background:rgba(139,0,0,.6);border:2px solid rgba(201,168,76,.5);top:33px;left:33px;}
#glzone{position:absolute;right:0;top:0;width:55%;height:100%;pointer-events:all;display:none;}
#gusebtn{position:absolute;bottom:80px;right:140px;width:64px;height:64px;border-radius:50%;background:rgba(139,0,0,.6);border:2px solid var(--blood);color:#fff;font-size:1.4rem;display:none;align-items:center;justify-content:center;pointer-events:all;cursor:pointer;}
#gdead{position:fixed;inset:0;z-index:30;display:none;flex-direction:column;align-items:center;justify-content:center;gap:14px;background:rgba(0,0,0,.65);backdrop-filter:blur(3px);}
#gdead h2{font-family:'Cinzel',serif;font-size:2rem;color:var(--blood);}
#gdead p{color:var(--gmuted);font-style:italic;font-size:.9rem;}
.gsb{padding:9px 24px;background:rgba(0,0,0,.8);border:1px solid #333;color:#888;cursor:pointer;font-family:'Cinzel',serif;font-size:.78rem;letter-spacing:.12em;pointer-events:all;}
#gspecbar{position:fixed;bottom:18px;left:50%;transform:translateX(-50%);z-index:31;background:rgba(0,0,0,.85);border:1px solid #333;color:#888;padding:5px 16px;font-size:.76rem;letter-spacing:.1em;display:none;pointer-events:none;font-family:'Cinzel',serif;}
#gflash{position:fixed;inset:0;background:rgba(139,0,0,.45);z-index:100;display:none;pointer-events:none;}
#gnotif{position:fixed;top:50%;left:50%;transform:translate(-50%,-50%);background:rgba(0,0,0,.92);border:1px solid var(--blood);color:#fff;padding:12px 32px;font-family:'Cinzel',serif;font-size:.95rem;letter-spacing:.1em;z-index:150;display:none;text-align:center;border-radius:2px;max-width:80vw;}
#gkick-dialog{display:none;position:fixed;inset:0;background:rgba(0,0,0,.75);z-index:400;align-items:center;justify-content:center;}
</style>
</head>
<body>

<div class="gconn" id="gconn"><div class="gspinner"></div><div class="gconn-txt">VERBINDE…</div></div>

<div id="gkick-dialog">
  <div style="background:var(--gcard);border:1px solid var(--gold);padding:2rem;text-align:center;max-width:280px;width:90%;">
    <div style="font-family:'Cinzel',serif;font-size:.95rem;color:var(--gold);margin-bottom:.8rem;">Spieler kicken?</div>
    <div id="gkick-name" style="font-size:1rem;margin-bottom:1.4rem;color:var(--gtext);"></div>
    <div style="display:flex;gap:.8rem;justify-content:center;">
      <button class="gbtn gbtn-red" id="gkick-confirm-btn">Kicken</button>
      <button class="gbtn" id="gkick-cancel-btn">Abbrechen</button>
    </div>
  </div>
</div>

<div id="gs-title" class="gscreen">
  <span class="gblade">🗡️</span>
  <div><h1>MURDER<br><em>MYSTERY</em></h1><p class="gtagline">Ein Mörder unter Euch</p></div>
  <div class="gornament">— ✦ —</div>
  <div class="gmenu">
    <button class="gbtn gbtn-red" id="gbtn-host">🔑 Spiel erstellen</button>
    <button class="gbtn" id="gbtn-join">🚪 Mit Code beitreten</button>
  </div>
</div>

<div id="gs-host" class="gscreen">
  <div class="gpanel">
    <h2>🔑 Spiel erstellen</h2>
    <div class="gfield"><label>Dein Name</label><input type="text" id="ghost-name" placeholder="Name…" maxlength="16"></div>
    <div class="gcodebox"><small>Lobby-Code</small><strong id="gnew-code">—</strong></div>
    <button class="gbtn gbtn-red" id="gbtn-create" style="width:100%">Erstellen →</button><br>
    <button class="glink-btn" id="gbtn-back-host">← Zurück</button>
  </div>
</div>

<div id="gs-join" class="gscreen">
  <div class="gpanel">
    <h2>🚪 Beitreten</h2>
    <div class="gfield"><label>Dein Name</label><input type="text" id="gjoin-name" placeholder="Name…" maxlength="16"></div>
    <div class="gfield"><label>Code</label><input type="text" id="gjoin-code" placeholder="4829" maxlength="6" style="letter-spacing:.3em;font-size:1.5rem;text-align:center;"></div>
    <button class="gbtn gbtn-red" id="gbtn-joinlobby" style="width:100%">Beitreten →</button><br>
    <button class="glink-btn" id="gbtn-back-join">← Zurück</button>
  </div>
</div>

<div id="gs-lobby" class="gscreen">
  <div class="globby-wrap">
    <div class="globby-top"><h2>⚔️ Lobby</h2><span class="gpcount" id="ghcount">1 Spieler</span></div>
    <div class="gcodebox" style="margin-bottom:1.3rem;"><small>Code teilen</small><strong id="gh-code-show">—</strong></div>
    <ul class="gplist" id="ghplist"></ul>
    <p class="ghint">Min. 3 Spieler</p>
    <button class="gbtn gbtn-red" id="gbtn-start" style="width:100%">🗡️ Starten</button><br>
    <button class="glink-btn" id="gbtn-leave-host">← Verlassen</button>
  </div>
</div>

<div id="gs-join-lobby" class="gscreen">
  <div class="globby-wrap">
    <div class="globby-top"><h2>⏳ Lobby</h2><span class="gpcount" id="gjcount">—</span></div>
    <div class="gcodebox" style="margin-bottom:1.3rem;"><small>Code</small><strong id="gj-code-show">—</strong></div>
    <ul class="gplist" id="gjplist"></ul>
    <p class="ghint">Warte auf Host…</p>
    <button class="glink-btn" id="gbtn-leave-join">← Verlassen</button>
  </div>
</div>

<div id="gs-countdown" class="gscreen">
  <div id="gcdn">10</div>
  <div id="gcdsub">Spiel beginnt…</div>
</div>

<div id="gs-role" class="gscreen">
  <div class="grc">
    <span class="gri" id="gr-icon">🗡️</span>
    <div class="grl" id="gr-label">—</div>
    <div class="grd" id="gr-desc">—</div>
  </div>
  <div class="grh">Nur du siehst das</div>
  <div class="grh2">Welt in <span id="gr-cd">3</span>s…</div>
</div>

<div class="goverlay hide" id="goverlay">
  <div class="gov-icon" id="gov-icon">⚰️</div>
  <div class="gov-title" id="gov-title">—</div>
  <div class="gov-sub" id="gov-sub">—</div>
  <button class="gbtn gbtn-red" id="gbtn-mainmenu">🏠 Hauptmenü</button>
</div>

<canvas id="c3d"></canvas>

<div id="ghud">
  <div id="gxhair"></div>
  <div id="grolepill" class="innocent">—</div>
  <div id="gsafepill">⭐ SHERIFF</div>
  <div id="gshieldtimer">🛡️ Schild droppen: <span id="gshield-sec">60</span>s</div>
  <div id="ghotbar">
    <div class="ghs on"  id="gslot0"><span class="ghk">1</span><span id="gs0i">✊</span></div>
    <div class="ghs off" id="gslot1"><span class="ghk">2</span><span id="gs1i">🗡️</span></div>
    <div class="ghs off" id="gslot2"><span class="ghk">3</span><span id="gs2i">🛡️</span></div>
  </div>
  <div id="gjzone"><div id="gjbase"></div><div id="gjknob"></div></div>
  <div id="glzone"></div>
  <button id="gusebtn">⚔️</button>
  <div id="gctrl">WASD · Leertaste Springen · 1/2/3 Item · Klick/E Benutzen</div>
  <button id="gescbtn">☰ Verlassen</button>
</div>

<div id="gdead">
  <h2>☠️ Tot</h2>
  <p id="gdeadmsg">Du wurdest ermordet.</p>
  <div style="display:flex;gap:8px;margin-top:6px;">
    <button class="gsb" id="gspec-prev">◀ [O]</button>
    <button class="gsb" id="gspec-next">[P] ▶</button>
  </div>
  <button class="gsb" id="gdeadleave" style="margin-top:10px;border-color:var(--blood);color:#ff6666;">🚪 Verlassen</button>
</div>
<div id="gspecbar">Spectating: <span id="gspecname">—</span></div>
<div id="gflash"></div>
<div id="gnotif"></div>

<!-- THREE.JS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>

<!-- FIREBASE (compat / global) -->
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-database-compat.js"></script>

<script>
// ── Firebase init ──
const FB={apiKey:"AIzaSyAtLemnwT80X4DbEEVUQzOCezGcPFjxHzs",authDomain:"murdermysery-8bbe3.firebaseapp.com",databaseURL:"https://murdermysery-8bbe3-default-rtdb.firebaseio.com",projectId:"murdermysery-8bbe3",storageBucket:"murdermysery-8bbe3.firebasestorage.app",messagingSenderId:"74585023201",appId:"1:74585023201:web:c691c0919a1db66a52cda0"};
firebase.initializeApp(FB);
const db=firebase.database();

const lRef=c=>db.ref('mm3d3v2/'+c);
const getL=c=>lRef(c).once('value').then(s=>s.exists()?s.val():null);
const saveL=(c,d)=>lRef(c).set(d);
const updL=(c,d)=>lRef(c).update(d);
const delL=c=>lRef(c).remove();
let unsub=null;
function watchL(code,cb){if(unsub)unsub();const r=lRef(code);r.on('value',s=>{if(s.exists())cb(s.val());});unsub=()=>r.off('value');}

/* ═══════════════════════════════════════
   GLOBAL STATE
═══════════════════════════════════════ */
const G={
  name:'',code:'',myRole:'innocent',myIdx:0,isHost:false,
  running:false,alive:true,
  specIdx:0,curSlot:0,
  yaw:0,pitch:0,velY:0,onGround:true,pLocked:false,
  shDropped:false,hasShield:false,
  speedMul:1.0,
};
const KEYS={};
const PP=new THREE.Vector3(2,1.7,2);

/* ── util ── */
const ggo=id=>{document.querySelectorAll('.gscreen').forEach(s=>s.classList.remove('active'));document.getElementById(id)?.classList.add('active');};
const gtoast=m=>{const e=document.createElement('div');e.className='gtoast';e.textContent=m;document.body.appendChild(e);setTimeout(()=>e.remove(),3200);};
const flashRed=()=>{const f=document.getElementById('gflash');f.style.display='block';setTimeout(()=>f.style.display='none',400);};
const notif=(msg,dur)=>{const n=document.getElementById('gnotif');n.textContent=msg;n.style.display='block';clearTimeout(n._t);n._t=setTimeout(()=>n.style.display='none',dur||2000);};
const showOv=(icon,title,sub)=>{document.getElementById('gov-icon').textContent=icon;document.getElementById('gov-title').textContent=title;document.getElementById('gov-sub').textContent=sub;document.getElementById('goverlay').classList.remove('hide');};

/* ═══════════════════════════════════════
   THREE.JS
═══════════════════════════════════════ */
let renderer,scene,camera,clock;
let myChar=null,fpHand=null;
const others={};
const WALLS=[];
let shieldDropMesh=null,shieldDropPos={x:0,z:0};
let loopStarted=false,walkT=0;
const _mv=new THREE.Vector3(),_cd=new THREE.Vector3(),_cr=new THREE.Vector3();

const GEO={
  body:new THREE.BoxGeometry(.48,.68,.24),head:new THREE.BoxGeometry(.36,.36,.36),
  eye:new THREE.BoxGeometry(.08,.06,.04),leg:new THREE.BoxGeometry(.2,.5,.2),
  arm:new THREE.BoxGeometry(.16,.52,.16),corpse:new THREE.BoxGeometry(.48,.12,1.1),
  blood:new THREE.CylinderGeometry(.5,.5,.02,8),coin:new THREE.CylinderGeometry(.22,.22,.09,8),
  shBody:new THREE.BoxGeometry(.6,.7,.08),shBoss:new THREE.SphereGeometry(.12,6,6),
  kBlade:new THREE.BoxGeometry(.05,.38,.08),kHand:new THREE.BoxGeometry(.07,.18,.1),
  htBrim:new THREE.CylinderGeometry(.27,.27,.06,8),htCrown:new THREE.CylinderGeometry(.15,.17,.32,8),
};
function lam(c){return new THREE.MeshLambertMaterial({color:c});}
function lame(c,e,ei){const m=lam(c);m.emissive.set(e);m.emissiveIntensity=ei;return m;}
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
  hBk:lam(0x111111),
};
const SPAWNS=[[2,2],[9,6],[-9,-6],[13,-11],[-6,13],[18,1],[-16,8],[4,-20],[20,-5],[-20,5],[0,15],[0,-15],[12,12],[-12,-12],[15,-8],[-15,8]];

function initThree(){
  if(renderer)return;
  const canvas=document.getElementById('c3d');
  renderer=new THREE.WebGLRenderer({antialias:false,canvas,powerPreference:'high-performance'});
  renderer.setPixelRatio(1);renderer.setSize(innerWidth,innerHeight);renderer.shadowMap.enabled=false;
  scene=new THREE.Scene();scene.background=new THREE.Color(0xd4a96a);scene.fog=new THREE.FogExp2(0xc8a060,.014);
  camera=new THREE.PerspectiveCamera(70,innerWidth/innerHeight,.1,120);camera.rotation.order='YXZ';
  clock=new THREE.Clock();
  window.addEventListener('resize',()=>{camera.aspect=innerWidth/innerHeight;camera.updateProjectionMatrix();renderer.setSize(innerWidth,innerHeight);});
  buildMap();setupInput();
  if(!loopStarted){loopStarted=true;gameLoop();}
}

function B(mat,w,h,d,x,y,z){const m=new THREE.Mesh(new THREE.BoxGeometry(w,h,d),mat);m.position.set(x,y,z);scene.add(m);return m;}
function C(mat,rt,rb,h,sg,x,y,z){const m=new THREE.Mesh(new THREE.CylinderGeometry(rt,rb,h,sg),mat);m.position.set(x,y,z);scene.add(m);return m;}

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
    B(wm,bw,tH,bd,cx,tH/2,cz);if(fl>1)B(MAT.slab,bw+.1,.1,bd+.1,cx,H,cz);
    B(rm,bw+.4,.3,bd+.4,cx,tH+.15,cz);
    const wc=Math.min(3,Math.floor(bw/2.5));
    for(let f=0;f<fl;f++){const wy=f*H+1.9;for(let i=0;i<wc;i++){const wx=cx-bw/2+bw/(wc+1)*(i+1);B(win,.78,1,.07,wx,wy,cz+bd/2+.04);B(win,.78,1,.07,wx,wy,cz-bd/2-.04);}}
    B(MAT.door,1.1,2.1,.1,cx,1.05,cz+bd/2+.05);WALLS.push({cx,cz,hw:bw/2,hd:bd/2});
  }
  bld(-22,-22,8,7,2,false);bld(22,-22,6,6,2,true);bld(-22,22,7,8,2,false);bld(22,22,8,7,1,true);
  bld(-42,0,7,6,2,false);bld(42,0,6,7,2,true);bld(0,-42,8,6,1,false);bld(0,42,6,8,2,true);
  bld(-35,-42,5,5,1,false);bld(35,42,5,5,1,true);bld(55,-22,7,6,1,false);bld(-55,22,6,5,2,true);
  bld(0,-70,16,12,2,false);bld(55,22,6,6,1,false);bld(-55,-22,7,5,1,true);bld(0,65,8,7,1,false);bld(70,0,6,6,1,true);
  [[-12,-14],[28,10],[-28,-10],[48,16],[-48,-16],[14,-35],[-14,35],[58,7],[-58,-7],[25,-25],[-25,25],[40,40],[-40,-40],[60,-30],[-60,30]].forEach(([x,z])=>{
    C(MAT.cactus,.18,.2,2.2,6,x,1.1,z);C(MAT.cactus,.1,.12,1,5,x+.45,1.4,z);C(MAT.cactus,.1,.12,1,5,x-.45,1.6,z);
  });
  [[-18,25,1.2],[18,-25,.9],[-32,10,1.4],[32,-10,1.1],[50,30,1.3],[-50,-30,.9],[5,-55,1.5],[65,10,1.0]].forEach(([x,z,s])=>B(MAT.rock,s*1.4,s*.8,s*1.2,x,s*.4,z));
  [[-4,16],[4,16],[-4,-16],[4,-16],[-4,36],[4,36],[-4,-36],[4,-36],[16,4],[16,-4],[-16,4],[-16,-4],[36,4],[36,-4],[-36,4],[-36,-4],[52,4],[-52,4],[4,52],[-4,-52]].forEach(([x,z])=>{
    C(MAT.wood,.06,.08,3.2,5,x,1.6,z);
    const b=new THREE.Mesh(new THREE.SphereGeometry(.1,5,5),MAT.glow);b.position.set(x,3.1,z);scene.add(b);
  });
  scene.add(new THREE.AmbientLight(0xffe0a0,2.2));
  const sun=new THREE.DirectionalLight(0xfff0c0,1.3);sun.position.set(30,60,10);scene.add(sun);
}

function mkChar(idx){
  const g=new THREE.Group();
  const bodySkin=new THREE.MeshLambertMaterial({color:0xcc3333});
  const body=new THREE.Mesh(GEO.body,bodySkin);body.position.y=.84;g.add(body);
  const head=new THREE.Mesh(GEO.head,MAT.face);head.position.y=1.38;g.add(head);
  [-.09,.09].forEach(sx=>{const e=new THREE.Mesh(GEO.eye,MAT.eye);e.position.set(sx,1.38,-.19);g.add(e);});
  const lL=new THREE.Mesh(GEO.leg,MAT.pants);lL.position.set(-.12,.25,0);g.add(lL);
  const lR=new THREE.Mesh(GEO.leg,MAT.pants);lR.position.set(.12,.25,0);g.add(lR);
  const aL=new THREE.Mesh(GEO.arm,bodySkin);aL.position.set(-.34,.84,0);g.add(aL);
  const aR=new THREE.Mesh(GEO.arm,bodySkin);aR.position.set(.34,.84,0);g.add(aR);
  const hand=new THREE.Group();hand.position.set(.38,.7,-.15);hand.scale.set(.7,.7,.7);g.add(hand);
  const hg=new THREE.Group();
  hg.add(new THREE.Mesh(GEO.htBrim,MAT.hBk));
  const cr=new THREE.Mesh(GEO.htCrown,MAT.hBk);cr.position.y=.22;hg.add(cr);
  hg.position.set(0,1.62,0);g.add(hg);
  scene.add(g);
  return{g,body,head,lL,lR,aL,aR,hand,sm:bodySkin};
}

function setHandItem(hand,type){
  while(hand.children.length)hand.remove(hand.children[0]);
  if(fpHand){while(fpHand.children.length)fpHand.remove(fpHand.children[0]);}
  if(type==='knife'){
    const b=new THREE.Mesh(GEO.kBlade,MAT.knife);b.position.y=.25;hand.add(b);
    const h=new THREE.Mesh(GEO.kHand,MAT.knifeH);h.position.y=-.02;hand.add(h);
    if(fpHand){const fb=new THREE.Mesh(new THREE.BoxGeometry(.06,.5,.1),MAT.knife);fb.position.set(0,.05,0);fpHand.add(fb);const fh=new THREE.Mesh(new THREE.BoxGeometry(.09,.22,.12),MAT.knifeH);fh.position.set(0,-.18,0);fpHand.add(fh);}
  } else if(type==='shield'){
    const s=new THREE.Mesh(GEO.shBody,MAT.shield);s.position.y=.3;hand.add(s);
    const bo=new THREE.Mesh(GEO.shBoss,MAT.shBoss);bo.position.y=.3;hand.add(bo);
    if(fpHand){const fs=new THREE.Mesh(new THREE.BoxGeometry(.7,.8,.1),MAT.shield);fpHand.add(fs);const fb=new THREE.Mesh(new THREE.SphereGeometry(.1,6,6),MAT.shBoss);fpHand.add(fb);}
  }
}

function mkLabel(name){
  const cv=document.createElement('canvas');cv.width=200;cv.height=48;
  const ctx=cv.getContext('2d');
  ctx.fillStyle='rgba(0,0,0,.8)';ctx.beginPath();ctx.roundRect(2,2,196,44,7);ctx.fill();
  ctx.fillStyle='#ffe0a0';ctx.font='bold 22px Georgia,serif';
  ctx.textAlign='center';ctx.textBaseline='middle';ctx.fillText(name,100,24);
  const sp=new THREE.Sprite(new THREE.SpriteMaterial({map:new THREE.CanvasTexture(cv),depthTest:false,transparent:true,opacity:0}));
  sp.scale.set(2,.48,1);return sp;
}

function mkTag(text,color){
  const cv=document.createElement('canvas');cv.width=160;cv.height=40;
  const ctx=cv.getContext('2d');
  ctx.fillStyle=color||'rgba(201,168,76,.85)';ctx.beginPath();ctx.roundRect(2,2,156,36,6);ctx.fill();
  ctx.fillStyle='#000';ctx.font='bold 20px Georgia,serif';
  ctx.textAlign='center';ctx.textBaseline='middle';ctx.fillText(text,80,20);
  const sp=new THREE.Sprite(new THREE.SpriteMaterial({map:new THREE.CanvasTexture(cv),depthTest:false,transparent:true,opacity:0}));
  sp.scale.set(1.6,.4,1);return sp;
}

function mkShieldDropMesh(withCorpse){
  const g=new THREE.Group();
  if(withCorpse){
    const corpse=new THREE.Mesh(new THREE.BoxGeometry(.48,.12,1.1),new THREE.MeshLambertMaterial({color:0xcc3333}));corpse.position.y=.06;g.add(corpse);
    const chead=new THREE.Mesh(new THREE.BoxGeometry(.36,.12,.36),new THREE.MeshLambertMaterial({color:0xf0c080}));chead.position.set(0,.06,.55);g.add(chead);
    const blood=new THREE.Mesh(GEO.blood,MAT.blood);blood.position.y=.01;g.add(blood);
  }
  const s=new THREE.Mesh(GEO.shBody,MAT.shield);s.position.set(0,.18,0);s.rotation.x=Math.PI/2;g.add(s);
  const bo=new THREE.Mesh(GEO.shBoss,MAT.shBoss);bo.position.set(0,.19,0);g.add(bo);
  scene.add(g);return g;
}

function killChar(ot){
  ot.alive=false;
  ['body','head','aL','aR','lL','lR'].forEach(k=>{if(ot[k])ot[k].visible=false;});
  ot.g.children.filter(c=>c.isGroup).forEach(c=>c.visible=false);
  if(ot.corpse)ot.corpse.visible=true;if(ot.blood)ot.blood.visible=true;
  ot.g.rotation.z=Math.PI/2;
  if(ot.label)ot.label.visible=false;if(ot.tag)ot.tag.visible=false;
  ot.hasSheriff=false;
}

function collide(p){
  p.x=Math.max(-95,Math.min(95,p.x));p.z=Math.max(-95,Math.min(95,p.z));
  for(const w of WALLS){
    const mg=.55,dx=p.x-w.cx,dz=p.z-w.cz;
    const ox=w.hw+mg-Math.abs(dx),oz=w.hd+mg-Math.abs(dz);
    if(ox>0&&oz>0){if(ox<oz)p.x+=ox*Math.sign(dx||.001);else p.z+=oz*Math.sign(dz||.001);}
  }
}

function setupRoleHUD(){
  const rp=document.getElementById('grolepill');
  rp.className=G.myRole;
  if(G.myRole==='murderer')rp.textContent='🔴 MÖRDER';
  else if(G.myRole==='sheriff')rp.textContent='⭐ SHERIFF';
  else rp.textContent='🔵 UNSCHULDIG';
  const s1=document.getElementById('gslot1'),s2=document.getElementById('gslot2');
  if(G.myRole==='murderer'){
    s1.classList.add('off');document.getElementById('gs1i').textContent='🗡️';
    s2.classList.remove('off');document.getElementById('gs2i').textContent='🛡️';
    setTimeout(()=>{selSlot(2);},300);
    startShieldTimer();
  } else if(G.myRole==='sheriff'){
    s1.classList.remove('off');document.getElementById('gs1i').textContent='🗡️';s2.classList.add('off');
  } else {
    s1.classList.add('off');s2.classList.add('off');
    selSlot(0);
  }
}

let shieldTimerInterval=null;
function startShieldTimer(){
  const timerEl=document.getElementById('gshieldtimer');
  const secEl=document.getElementById('gshield-sec');
  timerEl.style.display='block';
  let sec=60;secEl.textContent=sec;
  shieldTimerInterval=setInterval(async()=>{
    if(G.shDropped){clearInterval(shieldTimerInterval);timerEl.style.display='none';return;}
    sec--;secEl.textContent=sec;
    if(sec<=0){
      clearInterval(shieldTimerInterval);timerEl.style.display='none';
      if(!G.shDropped){
        notif('⚠️ Schild fliegt runter!',2000);
        fbDropShield(PP.x,PP.z);
        G.shDropped=true;
        document.getElementById('gslot2').classList.add('off');
        document.getElementById('gslot1').classList.remove('off');
        G.curSlot=0;document.querySelectorAll('.ghs').forEach((s,idx)=>s.classList.toggle('on',idx===0));
        if(myChar){setHandItem(myChar.hand,'');fbSetKnife(0);}
      }
    }
  },1000);
}

function selSlot(i){
  G.curSlot=i;
  document.querySelectorAll('.ghs').forEach((s,idx)=>s.classList.toggle('on',idx===i));
  if(!myChar)return;
  if(G.myRole==='murderer'){
    if(i===1&&G.shDropped){setHandItem(myChar.hand,'knife');fbSetKnife(1);}
    else if(i===2&&!G.shDropped){setHandItem(myChar.hand,'shield');fbSetKnife(2);}
    else{setHandItem(myChar.hand,'');fbSetKnife(0);}
  } else if(G.myRole==='sheriff'){
    if(i===1){setHandItem(myChar.hand,'knife');fbSetKnife(1);}
    else{setHandItem(myChar.hand,'');fbSetKnife(0);}
  } else {
    setHandItem(myChar.hand,'');fbSetKnife(0);
  }
}

async function useItem(){
  if(!G.alive||!G.running)return;
  if(G.myRole==='murderer'){
    if(!G.shDropped){
      if(G.curSlot!==2){notif('Slot 3 wählen (🛡️) um Schild zu droppen!',1500);return;}
      fbDropShield(PP.x,PP.z);
      G.shDropped=true;
      clearInterval(shieldTimerInterval);
      document.getElementById('gshieldtimer').style.display='none';
      document.getElementById('gslot2').classList.add('off');
      document.getElementById('gslot1').classList.remove('off');
      G.curSlot=0;document.querySelectorAll('.ghs').forEach((s,idx)=>s.classList.toggle('on',idx===0));
      setHandItem(myChar.hand,'');fbSetKnife(0);
      notif('🛡️ Schild versteckt! Messer freigeschaltet — jetzt töten!',2500);
    } else {
      if(G.curSlot!==1){notif('Slot 2 wählen (🗡️) um zu töten!',1000);return;}
      const best=nearestAlive(2.6);
      if(best){flashRed();notif('🔪 '+best,1500);fbKill(best);}
      else notif('Niemand in Reichweite!',800);
    }
  } else if(G.myRole==='sheriff'){
    if(G.curSlot===1){
      const best=nearestAlive(2.6);
      if(best){
        const targetRole=window._roles&&window._roles[best];
        if(targetRole==='murderer'){flashRed();notif('✅ Mörder gestoppt!',3000);fbKillMurderer(best);}
        else{flashRed();notif('❌ Falsches Ziel! Du wirst langsamer.',2000);fbKill(best);G.speedMul=0.35;setTimeout(()=>{G.speedMul=1.0;},8000);}
      }
    }
  } else {
    if(shieldDropMesh&&!G.hasShield){
      const dx=PP.x-shieldDropPos.x,dz=PP.z-shieldDropPos.z;
      if(Math.sqrt(dx*dx+dz*dz)<2.5){
        fbPickShield();
        G.hasShield=true;G.myRole='sheriff';
        if(shieldDropMesh){scene.remove(shieldDropMesh);shieldDropMesh=null;}
        document.getElementById('gsafepill').style.display='block';
        setupRoleHUD();
        notif('⭐ Du bist jetzt Sheriff! Du hast ein Messer bekommen.',2500);
      } else notif('Näher ans Schild herangehen!',800);
    } else if(!shieldDropMesh){
      notif('Das Schild wurde noch nicht gedroppt…',1000);
    }
  }
}

function nearestAlive(maxD){
  let best=null,bd=maxD;
  Object.entries(others).forEach(([name,ot])=>{
    if(!ot.alive)return;
    const ox=ot.g.position.x,oz=ot.g.position.z;
    if(ox===0&&oz===0)return;
    const dx=ox-PP.x,dz=oz-PP.z,d=Math.sqrt(dx*dx+dz*dz);
    if(d<bd){bd=d;best=name;}
  });
  return best;
}

function showDead(msg){
  document.getElementById('gdead').style.display='flex';
  document.getElementById('gspecbar').style.display='block';
  document.getElementById('gdeadmsg').textContent=msg||'Du wurdest ermordet.';
  const eb=document.getElementById('gescbtn');if(eb)eb.style.display='block';
  if(document.pointerLockElement)document.exitPointerLock();
  G.specIdx=0;updSpec();
}
function updSpec(){
  const k=Object.keys(others).filter(n=>others[n].alive);
  document.getElementById('gspecname').textContent=k.length?k[((G.specIdx%k.length)+k.length)%k.length]:'Niemand';
}

function startWorld(lobby){
  Object.values(others).forEach(o=>scene.remove(o.g));
  Object.keys(others).forEach(k=>delete others[k]);
  if(myChar){scene.remove(myChar.g);myChar=null;}
  if(shieldDropMesh){scene.remove(shieldDropMesh);shieldDropMesh=null;}
  G.alive=true;G.curSlot=0;G.shDropped=false;G.hasShield=false;
  G.yaw=0;G.pitch=0;G.velY=0;G.onGround=true;
  document.getElementById('gdead').style.display='none';
  document.getElementById('gspecbar').style.display='none';
  document.getElementById('goverlay').classList.add('hide');
  document.getElementById('gsafepill').style.display='none';
  document.getElementById('gshieldtimer').style.display='none';
  const myP=lobby.players.find(p=>p.name===G.name);
  PP.set(myP?.pos?.x||2,1.7,myP?.pos?.z||2);
  G.myIdx=lobby.players.findIndex(p=>p.name===G.name);
  myChar=mkChar(G.myIdx);myChar.g.visible=false;
  if(fpHand)scene.remove(fpHand);
  fpHand=new THREE.Group();scene.add(fpHand);
  lobby.players.forEach((p,i)=>{
    if(p.name===G.name)return;
    const ch=mkChar(i);
    const lbl=mkLabel(p.name);lbl.position.set(0,1.75,0);ch.g.add(lbl);
    const tag=mkTag('','rgba(0,0,0,0)');tag.position.set(0,2.22,0);tag.visible=false;ch.g.add(tag);
    const corp=new THREE.Mesh(GEO.corpse,ch.sm);corp.position.set(0,.06,0);corp.visible=false;ch.g.add(corp);
    const bl=new THREE.Mesh(GEO.blood,MAT.blood);bl.position.set(0,.02,0);bl.visible=false;ch.g.add(bl);
    if(p.pos)ch.g.position.set(p.pos.x,0,p.pos.z);
    others[p.name]={...ch,label:lbl,tag,corpse:corp,blood:bl,alive:!p.elim,wt:0,hasSheriff:false,hasKnife:false};
  });
  setupRoleHUD();
  if(myChar)setTimeout(()=>{selSlot(0);},200);
  document.querySelectorAll('.gscreen').forEach(s=>s.classList.remove('active'));
  document.getElementById('c3d').style.display='block';
  document.getElementById('ghud').style.display='block';
  G.running=true;
  const isTouch='ontouchstart' in window;
  if(isTouch){
    document.getElementById('gjzone').style.display='block';
    document.getElementById('glzone').style.display='block';
    document.getElementById('gusebtn').style.display='flex';
    document.getElementById('gxhair').style.display='none';
    document.getElementById('gctrl').style.display='none';
  }
  if(!isTouch)setTimeout(()=>document.getElementById('c3d').requestPointerLock(),200);
}

function setupInput(){
  document.addEventListener('keydown',e=>{
    KEYS[e.code]=true;if(!G.running)return;
    if(e.code==='Digit1')selSlot(0);
    if(e.code==='Digit2'){const s=document.getElementById('gslot1');if(!s.classList.contains('off'))selSlot(1);}
    if(e.code==='Digit3'){const s=document.getElementById('gslot2');if(!s.classList.contains('off'))selSlot(2);}
    if(e.code==='KeyE')useItem();
    if(e.code==='Escape')leaveGame();
    if(e.code==='KeyP'&&!G.alive){G.specIdx++;updSpec();}
    if(e.code==='KeyO'&&!G.alive){G.specIdx--;updSpec();}
  });
  document.addEventListener('keyup',e=>{KEYS[e.code]=false;});
  document.addEventListener('mousemove',e=>{
    if(!G.pLocked||!G.running)return;
    G.yaw-=e.movementX*.0022;G.pitch-=e.movementY*.0022;
    G.pitch=Math.max(-Math.PI/2+.05,Math.min(Math.PI/2-.05,G.pitch));
  });
  document.addEventListener('pointerlockchange',()=>G.pLocked=!!document.pointerLockElement);
  document.getElementById('c3d').addEventListener('click',()=>{
    if(!G.running)return;
    if(!G.pLocked){document.getElementById('c3d').requestPointerLock();return;}
    useItem();
  });
  const jzone=document.getElementById('gjzone'),jknob=document.getElementById('gjknob');
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
  const lzone=document.getElementById('glzone');let lLast={x:0,y:0},lActive=false;
  lzone.addEventListener('touchstart',e=>{e.preventDefault();lActive=true;const t=e.touches[0];lLast={x:t.clientX,y:t.clientY};},{passive:false});
  lzone.addEventListener('touchmove',e=>{
    e.preventDefault();if(!lActive||!G.running)return;const t=e.touches[0];
    G.yaw-=(t.clientX-lLast.x)*.006;G.pitch-=(t.clientY-lLast.y)*.006;
    G.pitch=Math.max(-Math.PI/2+.05,Math.min(Math.PI/2-.05,G.pitch));lLast={x:t.clientX,y:t.clientY};
  },{passive:false});
  lzone.addEventListener('touchend',()=>lActive=false);lzone.addEventListener('touchcancel',()=>lActive=false);
  document.getElementById('gusebtn').addEventListener('click',()=>useItem());
  document.getElementById('gspec-prev').addEventListener('click',()=>{G.specIdx--;updSpec();});
  document.getElementById('gspec-next').addEventListener('click',()=>{G.specIdx++;updSpec();});
}

function gameLoop(){
  requestAnimationFrame(gameLoop);
  if(!renderer||!G.running){if(renderer)renderer.render(scene,camera);return;}
  const dt=Math.min(clock.getDelta(),.05);
  if(!G.alive){
    const k=Object.keys(others).filter(n=>others[n].alive);
    if(k.length){
      const idx=((G.specIdx%k.length)+k.length)%k.length;
      const ot=others[k[idx]];
      if(ot){const angle=ot.g.rotation.y;camera.position.set(ot.g.position.x+Math.sin(angle)*5,ot.g.position.y+2.5,ot.g.position.z+Math.cos(angle)*5);camera.lookAt(ot.g.position.x,ot.g.position.y+1.2,ot.g.position.z);}
    }
    updSpec();tickOthers(dt);renderer.render(scene,camera);return;
  }
  const jd=window._jDelta||{x:0,y:0};
  _cd.set(Math.sin(G.yaw),0,Math.cos(G.yaw));_cr.set(Math.cos(G.yaw),0,-Math.sin(G.yaw));_mv.set(0,0,0);
  if(KEYS['KeyW']||KEYS['ArrowUp'])_mv.sub(_cd);if(KEYS['KeyS']||KEYS['ArrowDown'])_mv.add(_cd);
  if(KEYS['KeyA']||KEYS['ArrowLeft'])_mv.sub(_cr);if(KEYS['KeyD']||KEYS['ArrowRight'])_mv.add(_cr);
  if(Math.abs(jd.x)>.05||Math.abs(jd.y)>.05){_mv.addScaledVector(_cr,jd.x);_mv.addScaledVector(_cd,-jd.y);}
  const mov=_mv.lengthSq()>.001;
  const spd=5.5*(G.speedMul||1.0);
  if(mov){walkT+=dt*7;_mv.normalize().multiplyScalar(spd*dt);PP.x+=_mv.x;PP.z+=_mv.z;}else walkT*=.85;
  if(KEYS['Space']&&G.onGround){G.velY=7;G.onGround=false;}
  G.velY-=18*dt;PP.y+=G.velY*dt;if(PP.y<=1.7){PP.y=1.7;G.velY=0;G.onGround=true;}
  collide(PP);
  camera.position.copy(PP);camera.rotation.y=G.yaw;camera.rotation.x=G.pitch;
  if(myChar)myChar.g.visible=false;
  if(fpHand){
    const hOff=new THREE.Vector3(.32,-.30,-.48);
    hOff.applyEuler(new THREE.Euler(G.pitch,G.yaw,0,'YXZ'));
    fpHand.position.set(PP.x+hOff.x,PP.y+hOff.y,PP.z+hOff.z);
    fpHand.rotation.order='YXZ';fpHand.rotation.y=G.yaw+Math.PI;fpHand.rotation.x=G.pitch*.3;
  }
  if(myChar){
    myChar.g.position.set(PP.x,PP.y-1.7,PP.z);myChar.g.rotation.y=G.yaw;myChar.g.visible=false;
    if(mov){myChar.lL.rotation.x=Math.sin(walkT)*.55;myChar.lR.rotation.x=-Math.sin(walkT)*.55;myChar.aL.rotation.x=-Math.sin(walkT)*.45;myChar.aR.rotation.x=Math.sin(walkT)*.45;}
    else{myChar.lL.rotation.x*=.8;myChar.lR.rotation.x*=.8;myChar.aL.rotation.x*=.8;myChar.aR.rotation.x*=.8;}
  }
  if(shieldDropMesh)shieldDropMesh.rotation.y+=dt*0.3;
  tickOthers(dt);renderer.render(scene,camera);
}

function tickOthers(dt){
  Object.values(others).forEach(ot=>{
    if(!ot.alive)return;
    ot.wt+=dt*3;
    if(ot.lL)ot.lL.rotation.x=Math.sin(ot.wt)*.3;
    if(ot.lR)ot.lR.rotation.x=-Math.sin(ot.wt)*.3;
    const dx=PP.x-ot.g.position.x,dz=PP.z-ot.g.position.z;
    const dist=Math.sqrt(dx*dx+dz*dz);
    const isMoving=ot.lastPos&&(Math.abs(ot.g.position.x-ot.lastPos.x)>0.05||Math.abs(ot.g.position.z-ot.lastPos.z)>0.05);
    ot.lastPos={x:ot.g.position.x,z:ot.g.position.z};
    const tgt=dist<8&&!isMoving?Math.min(1,(8-dist)/3):0;
    if(ot.label)ot.label.material.opacity+=(tgt-ot.label.material.opacity)*.15;
    const sheriffTgt=ot.hasSheriff&&dist<15?1:0;
    if(ot.tag)ot.tag.material.opacity+=(sheriffTgt-ot.tag.material.opacity)*.15;
  });
}

// ── FIREBASE ACTIONS ──
async function fbKillMurderer(name){
  const l=await getL(G.code);if(!l)return;
  const ti=l.players.findIndex(p=>p.name===name);if(ti<0)return;
  await updL(G.code,{[`players/${ti}/elim`]:1,phase:'ended',winner:'innocents'});
}
async function fbKill(name){
  const l=await getL(G.code);if(!l)return;
  const ti=l.players.findIndex(p=>p.name===name);if(ti<0)return;
  const victim=l.players[ti];if(!victim||victim.elim)return;
  const updates={[`players/${ti}/elim`]:1};
  if(victim.isSheriff&&victim.pos){updates['shield']={dropped:true,fromDeath:true,x:victim.pos.x||0,z:victim.pos.z||0};}
  await updL(G.code,updates);
  const l2=await getL(G.code);
  const alive=l2.players.filter(p=>!p.elim&&p.role!=='murderer');
  if(alive.length===0)await updL(G.code,{phase:'ended',winner:'murderer'});
}
async function fbSetKnife(val){
  if(G.myIdx<0)return;
  await updL(G.code,{[`players/${G.myIdx}/knifeOut`]:val||0});
}
async function fbDropShield(x,z){
  await updL(G.code,{shield:{dropped:true,x,z}});
  if(G.myIdx>=0)await updL(G.code,{[`players/${G.myIdx}/shieldDropped`]:1});
}
async function fbPickShield(){
  await updL(G.code,{shield:{dropped:false,x:0,z:0}});
  if(G.myIdx>=0)await updL(G.code,{[`players/${G.myIdx}/safe`]:1,[`players/${G.myIdx}/isSheriff`]:1});
}

// ── UI EVENTS ──
const AV=['🎩','🕵️','👑','🦹','🧙','🥀','⚔️','🌹','🎭','🦇','🌙','🔮'];
let kickTarget=null;

document.getElementById('gbtn-host').addEventListener('click',()=>ggo('gs-host'));
document.getElementById('gbtn-join').addEventListener('click',()=>ggo('gs-join'));
document.getElementById('gbtn-back-host').addEventListener('click',()=>ggo('gs-title'));
document.getElementById('gbtn-back-join').addEventListener('click',()=>ggo('gs-title'));
document.getElementById('gbtn-mainmenu').addEventListener('click',()=>resetAll());
document.getElementById('gescbtn').addEventListener('click',()=>leaveGame());
document.getElementById('gdeadleave').addEventListener('click',()=>leaveGame());
document.getElementById('gkick-confirm-btn').addEventListener('click',()=>confirmKick());
document.getElementById('gkick-cancel-btn').addEventListener('click',()=>{document.getElementById('gkick-dialog').style.display='none';});
document.getElementById('gslot0').addEventListener('click',()=>selSlot(0));
document.getElementById('gslot1').addEventListener('click',()=>{if(!document.getElementById('gslot1').classList.contains('off'))selSlot(1);});
document.getElementById('gslot2').addEventListener('click',()=>{if(!document.getElementById('gslot2').classList.contains('off'))selSlot(2);});

function showKick(name){
  if(!G.isHost||name===G.name)return;
  kickTarget=name;
  document.getElementById('gkick-name').textContent=name;
  document.getElementById('gkick-dialog').style.display='flex';
}
async function confirmKick(){
  document.getElementById('gkick-dialog').style.display='none';
  if(!kickTarget)return;
  const l=await getL(G.code);if(!l)return;
  if(!l.kicked)l.kicked=[];
  l.kicked.push(kickTarget);l.players=l.players.filter(p=>p.name!==kickTarget);
  await saveL(G.code,l);kickTarget=null;
}
window._showKick=showKick;

document.getElementById('gbtn-create').addEventListener('click',async()=>{
  const name=document.getElementById('ghost-name').value.trim();
  if(!name){gtoast('Name eingeben!');return;}
  const code=document.getElementById('gnew-code').textContent;
  G.name=name;G.code=code;G.isHost=true;G.myIdx=0;
  const sp=SPAWNS[0];
  await saveL(code,{code,host:name,started:0,phase:'lobby',roles:{},
    players:[{name,avatar:AV[0],isHost:1,elim:0,role:null,safe:0,pos:{x:sp[0],z:sp[1]}}],ts:Date.now()});
  document.getElementById('gh-code-show').textContent=code;
  ggo('gs-lobby');
  let prevNames=[];
  watchL(code,l=>{
    if(!l)return;
    const curNames=l.players.map(p=>p.name);
    prevNames.forEach(n=>{if(!curNames.includes(n)&&n!==G.name)gtoast('👋 '+n+' hat verlassen.');});
    prevNames=curNames;
    document.getElementById('ghcount').textContent=l.players.length+' Spieler';
    document.getElementById('ghplist').innerHTML=l.players.map((p,i)=>
      `<li class="gpitem" onclick="window._showKick&&window._showKick('${p.name}')" style="cursor:${G.isHost&&i>0?'pointer':'default'}">
        <div class="gpdot ${i===0?'gold':''}"></div>
        <span class="gpname">${p.avatar} ${p.name}</span>
        ${i===0?'<span class="gptag">HOST</span>':G.isHost?'<span class="gptag" style="color:var(--blood)">KICK</span>':''}
      </li>`
    ).join('');
    if(l.phase==='countdown'){if(unsub)unsub();startCD(l);}
  });
});

document.getElementById('gbtn-joinlobby').addEventListener('click',async()=>{
  const name=document.getElementById('gjoin-name').value.trim();
  const code=document.getElementById('gjoin-code').value.trim();
  if(!name||!code){gtoast('Name und Code eingeben!');return;}
  const l=await getL(code);
  if(!l){gtoast('Lobby nicht gefunden!');return;}
  if(l.started){gtoast('Läuft bereits.');return;}
  if(l.players.find(p=>p.name===name)){gtoast('Name vergeben!');return;}
  const idx=l.players.length;
  const sp=SPAWNS[idx%SPAWNS.length];
  l.players.push({name,avatar:AV[idx%AV.length],isHost:0,elim:0,role:null,safe:0,pos:{x:sp[0],z:sp[1]}});
  await saveL(code,l);
  G.name=name;G.code=code;G.isHost=false;G.myIdx=idx;
  document.getElementById('gj-code-show').textContent=code;
  ggo('gs-join-lobby');
  watchL(code,ll=>{
    if(!ll){gtoast('Lobby geschlossen!');resetAll();return;}
    if(ll.kicked&&ll.kicked.includes(G.name)){gtoast('Du wurdest gekickt!');resetAll();return;}
    document.getElementById('gjcount').textContent=ll.players.length+' Spieler';
    document.getElementById('gjplist').innerHTML=ll.players.map(p=>
      `<li class="gpitem"><div class="gpdot ${p.isHost?'gold':''}"></div><span class="gpname">${p.avatar} ${p.name}</span>${p.isHost?'<span class="gptag">HOST</span>':''}</li>`
    ).join('');
    if(ll.phase==='countdown'){if(unsub)unsub();startCD(ll);}
  });
});

document.getElementById('gbtn-start').addEventListener('click',async()=>{
  const l=await getL(G.code);if(!l)return;
  if(l.players.length<3){gtoast('Min. 3 Spieler!');return;}
  const murdererIdx=Math.floor(Math.random()*l.players.length);
  l.players.forEach((p,i)=>{p.role=i===murdererIdx?'murderer':'innocent';});
  l.roles={};l.players.forEach(p=>{l.roles[p.name]=p.role;});
  l.started=1;l.phase='countdown';
  l.shield={dropped:false,x:0,z:0};
  await saveL(G.code,l);startCD(l);
});

document.getElementById('gbtn-leave-host').addEventListener('click',()=>resetAll());
document.getElementById('gbtn-leave-join').addEventListener('click',()=>resetAll());

function startCD(l){
  ggo('gs-countdown');let n=10;
  const el=document.getElementById('gcdn');el.textContent=n;el.classList.remove('red');
  const iv=setInterval(()=>{n--;el.textContent=n;if(n<=5)el.classList.add('red');if(n<=0){clearInterval(iv);G.myRole=l.roles[G.name]||'innocent';showRole(l);}},1000);
}

function showRole(l){
  const RD={
    murderer:{icon:'🗡️',label:'MÖRDER',desc:'Du trägst das Schild! Verstecke es irgendwo (Slot 3 wählen → E drücken) — innerhalb 60 Sekunden! Danach bekommst du dein Messer.'},
    innocent:{icon:'🕊️',label:'UNSCHULDIG',desc:'Der Mörder versteckt das Schild irgendwo auf der Karte. Finde es und drücke E — du wirst Sheriff und bekommst ein Messer!'}
  };
  const r=RD[G.myRole]||RD.innocent;
  document.getElementById('gr-icon').textContent=r.icon;
  const rl=document.getElementById('gr-label');rl.textContent=r.label;rl.className='grl '+G.myRole;
  document.getElementById('gr-desc').textContent=r.desc;
  ggo('gs-role');
  let c=4;document.getElementById('gr-cd').textContent=c;
  const iv=setInterval(()=>{c--;document.getElementById('gr-cd').textContent=c;if(c<=0){clearInterval(iv);enterWorld(l);}},1000);
}

function enterWorld(l){
  window._roles=l.roles;
  G.myIdx=l.players.findIndex(p=>p.name===G.name);
  initThree();
  setTimeout(()=>{
    startWorld(l);
    const posIv=setInterval(async()=>{
      if(!G.running){clearInterval(posIv);return;}
      if(G.myIdx<0)return;
      await updL(G.code,{
        [`players/${G.myIdx}/pos`]:{x:Math.round(PP.x*10)/10,y:Math.round(PP.y*10)/10,z:Math.round(PP.z*10)/10},
        [`players/${G.myIdx}/ry`]:+G.yaw.toFixed(3)
      });
    },100);

    watchL(G.code,ll=>{
      if(!ll||!G.running)return;
      ll.players.forEach(p=>{
        if(p.name===G.name){if(p.elim&&G.alive){G.alive=false;onSelfKilled('Du wurdest ermordet.');} return;}
        if(p.pos)updateOtherPos(p.name,p.pos.x,p.pos.y,p.pos.z,p.ry);
        if(p.elim)killOther(p.name);
        if(p.isSheriff){updateOtherTag(p.name,'sheriff');if(window._roles)window._roles[p.name]='sheriff';}
        if(p.knifeOut===1)updateOtherTag(p.name,'knife');
        else if(p.knifeOut===2)updateOtherTag(p.name,'shield');
        else updateOtherTag(p.name,'noknife');
      });
      Object.keys(others).forEach(name=>{if(!ll.players.find(p=>p.name===name))killOther(name);});
      if(ll.shield?.dropped){
        if(!G.shDropped){G.shDropped=true;onShieldDrop(ll.shield.x,ll.shield.z,ll.shield.fromDeath);}
      }
      if(ll.shield&&!ll.shield.dropped&&G.shDropped&&G.myRole!=='murderer'){onShieldPickedUp();}
      if(ll.phase==='ended'){
        const mn=ll.players.find(p=>p.role==='murderer')?.name||'?';
        gameOver(ll.winner||'murderer',mn);
      }
    });
  },150);
}

function killOther(name){const ot=others[name];if(ot)killChar(ot);}
function updateOtherPos(name,x,y,z,ry){
  const ot=others[name];if(!ot)return;
  ot.g.position.x=x;ot.g.position.z=z;
  if(y!==undefined)ot.g.position.y=y-1.7;
  if(ry!==undefined){let diff=ry-(ot.g.rotation.y||0);while(diff>Math.PI)diff-=Math.PI*2;while(diff<-Math.PI)diff+=Math.PI*2;ot.g.rotation.y+=diff*.25;}
}
function updateOtherTag(name,type){
  const ot=others[name];if(!ot)return;
  if(type==='sheriff'){
    ot.hasSheriff=true;
    if(ot.tag){
      const cv=document.createElement('canvas');cv.width=180;cv.height=44;
      const ctx=cv.getContext('2d');
      ctx.fillStyle='rgba(201,168,76,.95)';ctx.beginPath();ctx.roundRect(2,2,176,40,8);ctx.fill();
      ctx.fillStyle='#000';ctx.font='bold 22px Georgia,serif';ctx.textAlign='center';ctx.textBaseline='middle';ctx.fillText('⭐ SHERIFF',90,22);
      ot.tag.material.map=new THREE.CanvasTexture(cv);ot.tag.material.needsUpdate=true;ot.tag.material.opacity=1;ot.tag.visible=true;
    }
  } else if(type==='knife'){
    ot.hasKnife=true;
    if(ot.hand){while(ot.hand.children.length)ot.hand.remove(ot.hand.children[0]);
    const b=new THREE.Mesh(GEO.kBlade,MAT.knife);b.position.y=.25;ot.hand.add(b);
    const h=new THREE.Mesh(GEO.kHand,MAT.knifeH);h.position.y=-.02;ot.hand.add(h);}
  } else if(type==='shield'){
    if(ot.hand){while(ot.hand.children.length)ot.hand.remove(ot.hand.children[0]);
    const s=new THREE.Mesh(GEO.shBody,MAT.shield);s.position.y=.3;ot.hand.add(s);
    const bo=new THREE.Mesh(GEO.shBoss,MAT.shBoss);bo.position.y=.3;ot.hand.add(bo);}
  } else if(type==='noknife'){
    ot.hasKnife=false;if(ot.hand){while(ot.hand.children.length)ot.hand.remove(ot.hand.children[0]);}
  }
}
function onShieldDrop(x,z,fromSheriffDeath){
  G.shDropped=true;shieldDropPos={x,z};
  if(!shieldDropMesh){shieldDropMesh=mkShieldDropMesh(!!fromSheriffDeath);}
  shieldDropMesh.position.set(x,.1,z);
  if(G.myRole==='innocent'){
    notif('🛡️ Das Schild wurde irgendwo versteckt! Finde es und drücke E.',3500);
  }
}
function onShieldPickedUp(){
  if(shieldDropMesh){scene.remove(shieldDropMesh);shieldDropMesh=null;}
  if(G.myRole!=='murderer')G.shDropped=false;
  shieldDropPos={x:0,z:0};
}
function onSelfKilled(msg){G.alive=false;showDead(msg||'Du wurdest ermordet.');}
function gameOver(winner,mName){
  G.running=false;
  if(document.pointerLockElement)document.exitPointerLock();
  document.getElementById('ghud').style.display='none';
  document.getElementById('gdead').style.display='none';
  document.getElementById('gspecbar').style.display='none';
  const icon=winner==='murderer'?'🩸':'🔍';
  const title=winner==='murderer'?'DER MÖRDER GEWINNT':'GERECHTIGKEIT SIEGT';
  const sub=winner==='murderer'?mName+' entkommt unerkannt.':'Der Mörder wurde gestoppt!';
  showOv(icon,title,sub);
  setTimeout(()=>resetAll(),8000);
}

async function leaveGame(){
  if(unsub)unsub();G.running=false;clearInterval(shieldTimerInterval);
  if(G.isHost){await delL(G.code);}
  else{
    const l=await getL(G.code);
    if(l){
      if(G.myIdx>=0)await updL(G.code,{[`players/${G.myIdx}/elim`]:1});
      setTimeout(async()=>{const l2=await getL(G.code);if(l2){l2.players=l2.players.filter(p=>p.name!==G.name);await saveL(G.code,l2);}},500);
    }
  }
  resetAll();
}

async function resetAll(){
  G.running=false;clearInterval(shieldTimerInterval);
  if(G.code&&!G.isHost){
    const l=await getL(G.code);
    if(l&&!l.started){l.players=l.players.filter(p=>p.name!==G.name);await saveL(G.code,l);}
  }
  if(unsub){unsub();unsub=null;}
  document.getElementById('c3d').style.display='none';
  document.getElementById('ghud').style.display='none';
  document.getElementById('gdead').style.display='none';
  document.getElementById('gspecbar').style.display='none';
  document.getElementById('goverlay').classList.add('hide');
  document.getElementById('gnew-code').textContent=mkCode();
  ['ghost-name','gjoin-name','gjoin-code'].forEach(id=>{const e=document.getElementById(id);if(e)e.value='';});
  G.code='';G.name='';G.isHost=false;
  ggo('gs-title');
}

// ── INIT ──
function mkCode(){return String(Math.floor(1000+Math.random()*9000));}
document.getElementById('gconn').classList.add('hide');
document.getElementById('gnew-code').textContent=mkCode();
ggo('gs-title');
</script>
</body>
</html>
