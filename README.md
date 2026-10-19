














<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Windows 12 — Wild Berry Ultimate Edition</title>
<style>
:root{--accent:#ff2a7a;--glow:rgba(255,42,122,.4);--glass:rgba(18,9,30,.78);--border:rgba(255,255,255,.15);--text:#fff}
*{box-sizing:border-box;margin:0;font-family:"Segoe UI",system-ui,sans-serif;user-select:none}
html,body{height:100%;overflow:hidden;color:var(--text);background:#09020f}
body{background:radial-gradient(ellipse at 18% 15%,#ff2a75 0,#3a0050 38%,#0d001a 78%);transition:background .8s cubic-bezier(0.4, 0, 0.2, 1)}
button,input,textarea{font:inherit}button{cursor:pointer;color:white;border:1px solid #ffffff22;background:#ffffff12;border-radius:12px;padding:8px 14px;transition:all .25s ease}button:hover{background:#ffffff25;border-color:var(--accent);transform:translateY(-1px);box-shadow:0 4px 12px var(--glow)}
#boot{position:fixed;inset:0;z-index:99999;background:radial-gradient(circle at 50% 45%,#260b35,#06020c 58%);display:flex;align-items:center;justify-content:center;flex-direction:column;transition:opacity .8s ease,visibility .8s ease}
#boot.hide{opacity:0;visibility:hidden;pointer-events:none}
.boot-mark{width:112px;height:112px;position:relative;display:grid;place-items:center;animation:bootFloat 3s ease-in-out infinite}
.boot-mark svg{width:76px;filter:drop-shadow(0 0 25px var(--glow));animation:markPulse 2.5s ease-in-out infinite}
.boot-ring{position:absolute;inset:0;border:1.5px solid #ffffff20;border-radius:31px;transform:rotate(45deg);box-shadow:0 0 40px var(--glow),inset 0 0 25px #ff2a7a10;animation:ringSpin 7s linear infinite}
.boot-ring:before,.boot-ring:after{content:"";position:absolute;border-radius:50%;width:8px;height:8px;background:#00f2fe;box-shadow:0 0 18px #00f2fe}
.boot-ring:before{top:10px;left:10px}.boot-ring:after{right:10px;bottom:10px;background:var(--accent);box-shadow:0 0 18px var(--accent)}
.boot-name{margin-top:35px;font-size:13px;letter-spacing:7px;color:#ffffffb8;text-shadow:0 0 22px var(--glow)}
@keyframes ringSpin{to{transform:rotate(405deg)}}@keyframes bootFloat{50%{transform:translateY(-8px)}}@keyframes markPulse{50%{transform:scale(1.08);opacity:.85}}
#desktop{position:absolute;inset:0 0 72px;padding:18px;display:flex;flex-flow:column wrap;align-content:flex-start;gap:12px}
.dicon{width:88px;height:90px;border:1px solid transparent;border-radius:14px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:7px;cursor:pointer;background:#ffffff03;transition:all .25s cubic-bezier(0.4,0,0.2,1)}
.dicon:hover{background:#ffffff15;border-color:var(--accent);transform:translateY(-4px);box-shadow:0 10px 30px var(--glow)}
.dicon b{font-size:31px;font-weight:400}.dicon span{font-size:11px;text-align:center;text-shadow:0 1px 4px #000}
.widget{position:absolute;right:22px;width:250px;padding:16px;border:1px solid var(--border);border-radius:20px;background:var(--glass);backdrop-filter:blur(25px);box-shadow:0 15px 40px #0006;z-index:3;cursor:move;transition:opacity .3s ease}
.widget h4{font-size:12px;color:#00f2fe;margin-bottom:10px;display:flex;justify-content:space-between;align-items:center}.widget small{font-size:11px;color:#ffffffb0}.widget input,.widget textarea{background:transparent;color:white;border:0;outline:0;width:100%;resize:vertical}
#weather{top:22px}#performance{top:180px}#quicknote{top:340px}
#taskwrap{position:fixed;bottom:10px;left:0;right:0;z-index:10000;display:flex;justify-content:center;pointer-events:none}
#taskbar{pointer-events:auto;min-height:56px;padding:8px 14px;display:flex;align-items:center;gap:8px;background:var(--glass);backdrop-filter:blur(30px);border:1px solid var(--border);border-radius:24px;box-shadow:0 12px 45px #0008}
#startbtn{width:40px;height:40px;display:grid;place-items:center;border-radius:14px;background:linear-gradient(135deg,var(--accent),#8e00ff);cursor:pointer;box-shadow:0 0 18px var(--glow);transition:transform .2s ease}
#startbtn:hover{transform:scale(1.05)}
#tbapps{display:flex;gap:6px}.tbapp{width:38px;height:38px;border-radius:12px;display:grid;place-items:center;background:#ffffff0d;cursor:pointer;transition:background .2s}.tbapp:hover{background:#ffffff20}.tbapp.active{border-bottom:3px solid var(--accent)}
#clock{font-size:12px;padding:0 8px;white-space:nowrap;cursor:pointer}
#startmenu,#quick{position:fixed;z-index:9999;display:none;background:var(--glass);backdrop-filter:blur(35px);border:1px solid var(--border);box-shadow:0 25px 70px #000a;border-radius:26px;padding:22px;animation:menuPop .25s cubic-bezier(0.16, 1, 0.3, 1)}
@keyframes menuPop{from{opacity:0;transform:scale(0.95) translateY(10px)}to{opacity:1;transform:scale(1) translateY(0)}}
#startmenu{width:min(580px,94vw);height:min(580px,78vh);bottom:78px;left:50%;transform:translateX(-50%);flex-direction:column}
#startmenu.show{display:flex}#quick{bottom:78px;right:18px;width:310px}#quick.show{display:block}
#startsearch{width:100%;padding:12px 16px;border-radius:14px;background:#ffffff12;border:1px solid var(--border);color:white;outline:none;margin-bottom:16px}
#appgrid{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;overflow:auto}
.startapp{min-height:82px;display:flex;flex-direction:column;gap:6px;align-items:center;justify-content:center;border-radius:14px;background:#ffffff08;cursor:pointer;font-size:11px;transition:all .2s}
.startapp b{font-size:25px;font-weight:400}.startapp:hover{background:#ffffff20;transform:translateY(-2px)}
#startfooter{margin-top:auto;border-top:1px solid #ffffff1c;padding-top:14px;display:flex;justify-content:space-between;align-items:center;font-size:12px}
.window{position:absolute;z-index:100;background:var(--glass);backdrop-filter:blur(32px);border:1px solid var(--border);border-radius:18px;box-shadow:0 25px 65px #0009,0 0 25px #ff2a7a16;display:flex;flex-direction:column;overflow:hidden;min-width:320px;min-height:240px;animation:winIn .25s cubic-bezier(0.16, 1, 0.3, 1)}
@keyframes winIn{from{opacity:0;transform:scale(0.94) translateY(12px)}to{opacity:1;transform:scale(1) translateY(0)}}
.window.min{display:none}.whead{height:44px;flex-shrink:0;display:flex;align-items:center;justify-content:space-between;padding:0 14px;background:#ffffff08;border-bottom:1px solid #ffffff12;cursor:move}
.wtitle{font-size:12px;font-weight:650}.wcontrols{display:flex;gap:8px}.wcontrols button{width:13px;height:13px;padding:0;border:0;border-radius:50%;font-size:0;cursor:pointer;transition:transform .15s}.wcontrols button:hover{transform:scale(1.15)}.minb{background:#ffbd2e}.maxb{background:#27c93f}.closeb{background:#ff5f56}
.wbody{padding:14px;flex:1;min-height:0;overflow:auto;display:flex;flex-direction:column;gap:12px}
input,textarea,select{color:white;background:#ffffff10;border:1px solid #ffffff25;border-radius:10px;padding:10px;outline:none;transition:border-color .2s}input:focus,textarea:focus,select:focus{border-color:var(--accent)}textarea{resize:vertical}
.row{display:flex;gap:8px;align-items:center}.grow{flex:1;min-width:0}
.browserbar{display:flex;gap:8px}.browserbar input{flex:1;min-width:0}
.browser-home{flex:1;min-height:240px;border:1px solid #ffffff20;border-radius:16px;padding:24px;background:radial-gradient(circle at 50% 0%,#4b124f,#130b20 65%);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:14px;text-align:center}
.browser-logo{font-size:44px;filter:drop-shadow(0 0 20px var(--glow))}.browser-search{display:flex;width:min(620px,100%);gap:8px}.browser-search input{flex:1;min-width:0;background:#ffffff13;border-radius:24px;padding:13px 18px}.browser-shortcuts{display:flex;gap:10px;flex-wrap:wrap;justify-content:center}.browser-shortcuts button{min-width:110px}.browser-status{font-size:11px;color:#ffffff90;display:flex;justify-content:space-between;gap:8px;flex-wrap:wrap}.browser-history{display:flex;gap:6px;flex-wrap:wrap}
.permission-overlay{position:fixed;inset:0;background:#05010bc9;backdrop-filter:blur(12px);z-index:200000;display:none;align-items:center;justify-content:center;padding:18px}
.permission-overlay.show{display:flex}
.permission-card{width:min(440px,96vw);padding:24px;border:1px solid var(--border);border-radius:22px;background:linear-gradient(145deg,#281137,#100817);box-shadow:0 25px 80px #000b}
.permission-card h2{margin-bottom:10px}.permission-card p{font-size:13px;color:#ffffffb5;line-height:1.6;margin:8px 0 16px}.permission-actions{display:flex;gap:8px;justify-content:flex-end;flex-wrap:wrap}.permission-actions .accent{background:var(--accent)}
.cardgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:10px}.card{padding:14px;border:1px solid #ffffff18;background:#ffffff08;border-radius:14px;cursor:pointer;transition:all .2s}.card:hover{border-color:var(--accent);background:#ffffff14;transform:translateY(-2px)}.card strong{display:block;margin-bottom:6px}.muted{font-size:11px;color:#ffffff9c}
.term{background:#08020f;color:#00f2fe;font:12px/1.6 Consolas,monospace;white-space:pre-wrap;overflow:auto;flex:1;padding:12px;border-radius:10px;min-height:150px}
.calcgrid{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;flex:1}.calcgrid button{font-size:18px}.accent{background:var(--accent)}
#toast{position:fixed;bottom:85px;left:50%;transform:translateX(-50%);padding:10px 18px;background:#170d24;border:1px solid var(--border);border-radius:12px;z-index:100000;display:none;font-size:12px;box-shadow:0 10px 30px #0006;animation:toastIn .2s ease}
@keyframes toastIn{from{opacity:0;transform:translate(-50%,10px)}to{opacity:1;transform:translate(-50%,0)}}
@media(max-width:650px){.widget{display:none}#taskbar{max-width:96vw;gap:5px;padding:6px}#appgrid{grid-template-columns:repeat(3,1fr)}.window{max-width:96vw!important;max-height:82vh!important;left:2vw!important;top:5vh!important}.dicon{width:74px;height:78px}}
</style>
</head>
<body>
<div id="boot">
  <div class="boot-mark"><div class="boot-ring"></div><svg viewBox="0 0 100 100" aria-label="Windows"><defs><linearGradient id="g" x1="0" y1="0" x2="1" y2="1"><stop stop-color="#ff2a7a"/><stop offset=".52" stop-color="#00f2fe"/><stop offset="1" stop-color="#b000ff"/></linearGradient></defs><path fill="url(#g)" d="M7 12 46 7v39H7zM54 6l39-6v46H54zM7 54h39v39L7 88zM54 54h39v46l-39-6z"/></svg></div>
  <div class="boot-name">WILD BERRY</div>
</div>
<div id="desktop">
  <div class="dicon" onclick="openApp('pc')"><b>💻</b><span>Bu Bilgisayar</span></div>
  <div class="dicon" onclick="openApp('browser')"><b>🌐</b><span>Berry Browser</span></div>
  <div class="dicon" onclick="openApp('store')"><b>🛍️</b><span>Uygulama Merkezi</span></div>
  <div class="dicon" onclick="openApp('files')"><b>📁</b><span>Dosyalar</span></div>
  <div class="dicon" onclick="openApp('terminal')"><b>⌨️</b><span>Terminal</span></div>
  <div class="dicon" onclick="openApp('editor')"><b>📝</b><span>Metin Editörü</span></div>
  <div class="dicon" onclick="openApp('paint')"><b>🎨</b><span>Wild Paint</span></div>
  <div class="dicon" onclick="openApp('calc')"><b>🧮</b><span>Hesap Makinesi</span></div>
  <div class="dicon" onclick="openApp('media')"><b>🎵</b><span>Medya Merkezi</span></div>
  <div class="dicon" onclick="openApp('calendar')"><b>📅</b><span>Takvim</span></div>
  <div class="dicon" onclick="openApp('tasks')"><b>☑️</b><span>Görevler</span></div>
  <div class="dicon" onclick="openApp('settings')"><b>⚙️</b><span>Ayarlar</span></div>
  <div class="dicon" onclick="openApp('snake')"><b>🐍</b><span>Yılan Oyunu</span></div>
  <div class="dicon" onclick="openApp('spacegame')"><b>🚀</b><span>Uzay Savaşı</span></div>
</div>

<div class="widget" id="weather" onmousedown="dragWidget(event, 'weather')">
  <h4>📍 HAVA DURUMU <span id="city-name" style="font-size:10px;cursor:pointer;color:#00f2fe;" onclick="changeCity()">[İstanbul]</span></h4>
  <div style="font-size:25px;font-weight:750;color:var(--accent)" id="weather-temp">18°C · Parçalı Bulutlu</div>
  <small>Şehir değiştirmek için üstüne tıkla.</small>
</div>

<div class="widget" id="performance" onmousedown="dragWidget(event, 'performance')">
  <h4>⚡ SİSTEM PANELİ</h4>
  <small>CPU / Bellek Durumu</small>
  <div style="height:6px;background:#ffffff18;border-radius:9px;margin:8px 0"><div id="cpu-bar" style="width:42%;height:100%;background:linear-gradient(90deg,var(--accent),#00f2fe);border-radius:9px;transition:width 0.5s"></div></div>
  <small id="cpu-text">CPU: %42 · RAM: %60</small>
</div>

<div class="widget" id="quicknote" onmousedown="dragWidget(event, 'quicknote')">
  <h4>📌 HIZLI NOTLAR</h4>
  <textarea id="widget-note" rows="3" placeholder="Notlarını buraya yaz..."></textarea>
</div>

<div id="startmenu">
  <input id="startsearch" placeholder="Uygulama ara..." oninput="filterApps(this.value)">
  <div style="font-size:11px;color:var(--accent);font-weight:700;margin-bottom:10px;letter-spacing:1px">UYGULAMALAR</div>
  <div id="appgrid"></div>
  <div id="startfooter"><span>👤 WildBerry Kullanıcısı</span><button onclick="restartSystem()">⟳ Yeniden başlat</button></div>
</div>

<div id="quick">
  <strong style="color:#00f2fe">Hızlı Ayarlar</strong>
  <div class="cardgrid" style="margin-top:12px">
    <div class="card quick-toggle" data-setting="wifi" onclick="toggleQuickSetting(this,'📶 Wi-Fi')">📶<br>Wi-Fi <small>Kapalı</small></div>
    <div class="card quick-toggle" data-setting="bluetooth" onclick="toggleQuickSetting(this,'ᛒ Bluetooth')">ᛒ<br>Bluetooth <small>Kapalı</small></div>
    <div class="card quick-toggle" data-setting="focus" onclick="toggleFocus(this)">🌙<br>Odak modu <small>Kapalı</small></div>
    <div class="card quick-toggle" data-setting="night" onclick="toggleNight(this)">🌌<br>Gece ışığı <small>Kapalı</small></div>
    <div class="card" onclick="openApp('settings')">⚙️<br>Ayarlar</div>
    <div class="card" onclick="openApp('privacy')">🛡️<br>Gizlilik</div>
  </div>
  <div style="margin-top:14px"><label for="volume-control" style="font-size:12px">🔊 Ses düzeyi <span id="volume-label">70%</span></label><input id="volume-control" type="range" min="0" max="100" value="70" style="width:100%;padding:0;margin-top:8px" oninput="document.getElementById('volume-label').textContent=this.value+'%';localStorage.setItem('wb-volume',this.value)"></div>
  <div style="margin-top:12px"><label for="brightness-control" style="font-size:12px">☀️ Parlaklık <span id="brightness-label">100%</span></label><input id="brightness-control" type="range" min="55" max="120" value="100" style="width:100%;padding:0;margin-top:8px" oninput="document.getElementById('brightness-label').textContent=this.value+'%';document.body.style.filter='brightness('+this.value/100+')';localStorage.setItem('wb-brightness',this.value)"></div>
</div>

<div id="taskwrap"><div id="taskbar">
  <div id="startbtn" onclick="toggleStart()"><svg width="20" height="20" viewBox="0 0 100 100"><path fill="white" d="M7 12 46 7v39H7zM54 6l39-6v46H54zM7 54h39v39L7 88zM54 54h39v46l-39-6z"/></svg></div>
  <div style="height:25px;width:1px;background:#ffffff25"></div><div id="tbapps"></div>
  <div style="height:25px;width:1px;background:#ffffff25"></div><button title="Bildirimler ve izinler" onclick="openApp('privacy')" style="padding:8px 10px">🔔</button><div id="clock" onclick="toggleQuick()">🔊 📶 <span id="time">00:00</span></div>
</div></div>

<div id="permission-overlay" class="permission-overlay"><div class="permission-card"><div style="font-size:34px;margin-bottom:10px">🔔</div><h2>Wild Berry izinleri</h2><p>Bildirimleri açmak ister misin?</p><div class="permission-actions"><button onclick="dismissPermissionPrompt()">Şimdi değil</button><button class="accent" onclick="dismissPermissionPrompt();openApp('privacy');requestNotifications()">Bildirim iznini yönet</button></div></div></div><div id="toast"></div>

<script>
const apps={
 pc:['💻','Bu Bilgisayar'],browser:['🌐','Berry Browser'],store:['🛍️','Uygulama Merkezi'],files:['📁','Dosya Gezgini'],terminal:['⌨️','Terminal'],editor:['📝','Metin Editörü'],paint:['🎨','Wild Paint'],calc:['🧮','Hesap Makinesi'],media:['🎵','Medya Merkezi'],calendar:['📅','Takvim'],tasks:['☑️','Görevler'],settings:['⚙️','Ayarlar'],privacy:['🛡️','Gizlilik ve İzinler'],snake:['🐍','Yılan Oyunu'],spacegame:['🚀','Uzay Savaşı']
};
const windows={},filesDB=JSON.parse(localStorage.getItem('wb-files')||'null')||[
{name:'SistemLoglari.txt',content:'Windows 12 Wild Berry\n[OK] Arayüz başlatıldı\n[OK] Masaüstü hazır'}, {name:'Notlar.txt',content:'Wild Berry notların burada.'}
];
function persist(){localStorage.setItem('wb-files',JSON.stringify(filesDB))}
function toast(t){let el=document.getElementById('toast');el.textContent=t;el.style.display='block';clearTimeout(window.toastTimer);window.toastTimer=setTimeout(()=>el.style.display='none',2300)}
function toggleStart(){document.getElementById('startmenu').classList.toggle('show');document.getElementById('quick').classList.remove('show')}
function toggleQuick(){document.getElementById('quick').classList.toggle('show');document.getElementById('startmenu').classList.remove('show')}
function restartSystem(){location.reload()}
function toggleQuickSetting(el,label){let on=el.dataset.on!=='1';el.dataset.on=on?'1':'0';el.style.borderColor=on?'var(--accent)':'';let small=el.querySelector('small');if(small)small.textContent=on?'Açık':'Kapalı';localStorage.setItem('wb-'+el.dataset.setting,on?'1':'0');toast(label+(on?' açıldı':' kapatıldı'))}
function toggleFocus(el){let on=el.dataset.on!=='1';el.dataset.on=on?'1':'0';el.style.borderColor=on?'var(--accent)':'';el.querySelector('small').textContent=on?'Açık':'Kapalı';document.querySelectorAll('.widget').forEach(w=>w.style.opacity=on?'.18':'1');localStorage.setItem('wb-focus',on?'1':'0');toast(on?'Odak modu açık':'Odak modu kapalı')}
function toggleNight(el){let on=el.dataset.on!=='1';el.dataset.on=on?'1':'0';el.style.borderColor=on?'var(--accent)':'';el.querySelector('small').textContent=on?'Açık':'Kapalı';document.body.style.filter=on?'sepia(.22) brightness(.86)':'';localStorage.setItem('wb-night',on?'1':'0');toast(on?'Gece ışığı açıldı':'Gece ışığı kapatıldı')}
function filterApps(q){document.querySelectorAll('.startapp').forEach(e=>e.style.display=e.textContent.toLowerCase().includes(q.toLowerCase())?'flex':'none')}
function renderStart(){document.getElementById('appgrid').innerHTML=Object.entries(apps).map(([id,a])=>`<div class="startapp" onclick="openApp('${id}');toggleStart()"><b>${a[0]}</b><span>${a[1]}</span></div>`).join('')}
renderStart();

function dragWidget(e, id) {
  if(e.target.tagName==='TEXTAREA'||e.target.tagName==='SPAN') return;
  let w = document.getElementById(id);
  w.style.zIndex = ++z;
  let shiftX = e.clientX - w.getBoundingClientRect().left;
  let shiftY = e.clientY - w.getBoundingClientRect().top;
  function moveAt(pageX, pageY) {
    w.style.left = pageX - shiftX + 'px';
    w.style.top = pageY - shiftY + 'px';
    w.style.right = 'auto';
  }
  function onMouseMove(event) { moveAt(event.pageX, event.pageY); }
  document.addEventListener('mousemove', onMouseMove);
  document.onmouseup = function() {
    document.removeEventListener('mousemove', onMouseMove);
    document.onmouseup = null;
  };
}

function changeCity() {
  let c = prompt("Hava durumu için şehir adı girin:", "İstanbul");
  if(c) {
    document.getElementById('city-name').textContent = "[" + c + "]";
    let randomTemp = Math.floor(Math.random() * 25) + 5;
    document.getElementById('weather-temp').textContent = randomTemp + "°C · Parçalı Bulutlu";
    toast(c + " güncellendi.");
  }
}

setInterval(() => {
  let cpu = Math.floor(Math.random() * 40) + 20;
  let ram = Math.floor(Math.random() * 20) + 50;
  let bar = document.getElementById('cpu-bar');
  let txt = document.getElementById('cpu-text');
  if(bar && txt) {
    bar.style.width = cpu + '%';
    txt.textContent = `CPU: %${cpu} · RAM: %${ram}`;
  }
}, 3000);

function openApp(id,data=null){
 if(windows[id]){windows[id].classList.remove('min');windows[id].style.zIndex=++z; if(id==='editor'&&data!==null)document.getElementById('editor-text').value=data;return}
 const w=document.createElement('div');w.className='window';w.id='win-'+id;w.style.zIndex=++z;w.style.left=(12+Math.random()*12)+'%';w.style.top=(8+Math.random()*10)+'%';
 let title=apps[id]?.[1]||'Uygulama',body='',size=['850px','560px'];
 const btn=(label,fn)=>`<button onclick="${fn}">${label}</button>`;
 switch(id){
 case'pc':case'files':body=`<div class="row"><input id="newfile-name" placeholder="Yeni dosya adı.txt" class="grow">${btn('＋ Dosya oluştur',"createFile()")}<label class="card" style="padding:8px">Dosya yükle<input type="file" hidden onchange="uploadFile(event)"></label></div><div class="cardgrid" id="file-list"></div><p class="muted">Dosyalar tarayıcıda saklanır.</p>`;size=['650px','440px'];break;
 case'browser':body=`<div class="browserbar"><button title="Geri" onclick="browserBack()">←</button><button title="İleri" onclick="browserForward()">→</button><button title="Ana sayfa" onclick="browserHome()">⌂</button><input id="browser-url" value="" placeholder="Ara veya adres yaz..." onkeydown="if(event.key==='Enter')browse()"><button title="Yenile" onclick="browse()">⟳</button><button class="accent" onclick="browse()">Git ↗</button></div><div class="browser-home" id="browser-home"><div class="browser-logo">🌐</div><h2 style="font-size:28px">Berry Browser</h2><p class="muted">Hızlı web merkezi.</p><div class="browser-search"><input id="browser-home-search" placeholder="Google'da ara..." onkeydown="if(event.key==='Enter'){document.getElementById('browser-url').value=this.value;browse()}"><button class="accent" onclick="document.getElementById('browser-url').value=document.getElementById('browser-home-search').value;browse()">Ara</button></div><div class="browser-shortcuts"><button onclick="browserSearchEngine('google')">🔎 Google</button><button onclick="browserSearchEngine('bing')">🟦 Bing</button><button onclick="browserSearchEngine('duck')">🦆 DuckDuckGo</button><button onclick="browserSearchYouTube()">▶ YouTube</button></div><div class="browser-history" id="browser-bookmarks"></div></div><div class="row" style="flex-wrap:wrap"><button onclick="browserBookmark()">☆ Favorilere ekle</button><button onclick="browserOpenHistory()">🕘 Son aramalar</button><button onclick="openApp('privacy')">🛡️ Site izinleri</button></div><div class="browser-status"><span id="browser-status-text">Hazır.</span><span>🌐 Varsayılan Tarayıcı</span></div>`;size=['980px','650px'];break;
 case'store':body=`<h3>Uygulama Merkezi</h3><p class="muted">Wild Berry yerleşik araçları.</p><div class="cardgrid">${Object.entries(apps).filter(([k])=>k!=='store').map(([k,a])=>`<div class="card" onclick="openApp('${k}')"><strong>${a[0]}${a[1]}</strong><span class="muted">Açmak için tıkla</span></div>`).join('')}</div>`;size=['700px','520px'];break;
 case'terminal':body=`<div class="term" id="term-log">Windows 12 Wild Berry Shell [Build 2026.10]\n'help' komutuyla başlayın.\n</div><div class="row"><span style="font:12px Consolas">WB&gt;</span><input class="grow" id="term-input" onkeydown="terminalKey(event)" placeholder="Komut yaz..."></div>`;size=['650px','420px'];break;
 case'editor':body=`<div class="row"><input id="editor-name" value="YeniNot.txt" class="grow" placeholder="Dosya adı"><button onclick="saveEditor()">💾 Kaydet</button><button onclick="downloadEditor()">İndir</button></div><textarea id="editor-text" style="flex:1;min-height:250px;background:#08020f;color:#00f2fe;font:13px Consolas" placeholder="Metin yaz..."></textarea>`;size=['650px','470px'];if(data!==null)setTimeout(()=>{let e=document.getElementById('editor-text');if(e)e.value=data},20);break;
 case'paint':body=`<div class="row"><input type="color" id="paint-color" value="#ff2a7a"><input type="range" id="paint-size" min="1" max="30" value="5"><button onclick="clearPaint()">Temizle</button><button onclick="savePaint()">PNG indir</button></div><canvas id="paint-canvas" width="700" height="380" style="background:white;border-radius:10px;max-width:100%;cursor:crosshair;touch-action:none"></canvas>`;size=['760px','520px'];break;
 case'calc':body=`<input id="calc-display" value="0" readonly style="font-size:25px;text-align:right"><div class="calcgrid">${['7','8','9','÷','4','5','6','×','1','2','3','−','C','0','.','=','+','−','×','÷'].map(v=>`<button onclick="calcPress('${v}')">${v}</button>`).join('')}</div>`;size=['310px','430px'];break;
 case'media':body=`<div style="text-align:center;padding:25px"><div style="font-size:65px">🎧</div><h3>Medya Merkezi</h3><p class="muted">Yerel ses veya video dosyası oynat</p><input type="file" accept="audio/*,video/*" onchange="loadMedia(event)"><video id="media-player" controls style="width:100%;max-height:270px;display:none"></video><audio id="audio-player" controls style="width:100%;display:none"></audio></div>`;size=['500px','400px'];break;
 case'calendar':body=`<h3 id="cal-title"></h3><input type="date" id="calendar-date"><p class="muted">Tarih seçebilirsin.</p><div id="calendar-now"></div>`;size=['400px','300px'];break;
 case'tasks':body=`<div class="row"><input id="task-input" class="grow" placeholder="Yeni görev..." onkeydown="if(event.key==='Enter')addTask()"><button onclick="addTask()">Ekle</button></div><div id="task-list"></div>`;size=['450px','400px'];break;
 case'settings':body=`<h3>🎨 Görünüm ve sistem</h3><div class="cardgrid"><div class="card" onclick="wall('berry')"><strong>🍓 Wild Berry</strong></div><div class="card" onclick="wall('aurora')"><strong>🌌 Aurora</strong></div><div class="card" onclick="wall('cyber')"><strong>⚡ Cyberpunk</strong></div><div class="card" onclick="wall('dark')"><strong>🌑 Minimal Dark</strong></div></div><div class="row"><label>Vurgu rengi</label><input type="color" value="#ff2a7a" onchange="accent(this.value);localStorage.setItem('wb-accent',this.value)"></div><div class="row"><label>Görev çubuğu</label><select onchange="document.getElementById('taskwrap').style.justifyContent=this.value;localStorage.setItem('wb-taskpos',this.value)"><option value="center">Ortada</option><option value="flex-start">Solda</option><option value="flex-end">Sağda</option></select></div>`;size=['520px','490px'];break;
 case'privacy':body=`<h3>🛡️ Gizlilik ve izinler</h3><p class="muted">İzinler kapalıdır.</p><div class="cardgrid"><div class="card"><strong>🔔 Bildirimler</strong><button onclick="requestNotifications()">İzin iste</button></div><div class="card"><strong>📍 Konum</strong><button onclick="requestLocation()">İzin iste</button></div><div class="card"><strong>🎙️ Mikrofon</strong><button onclick="requestMedia('audio')">İzin iste</button></div><div class="card"><strong>📷 Kamera</strong><button onclick="requestMedia('video')">İzin iste</button></div></div><p id="permission-status" class="muted">Henüz izin istenmedi.</p>`;size=['600px','500px'];break;
 case'snake':body=`<canvas id="snake-canvas" width="320" height="320" style="display:block;margin:auto;background:#08020f;border:1px solid var(--accent);border-radius:10px"></canvas><p class="muted">Yön tuşlarıyla oyna.</p>`;size=['370px','420px'];break;
 case'spacegame':body=`<div style="display:flex;justify-content:space-between;align-items:center;font-weight:bold;margin-bottom:5px"><span>SKOR: <span id="space-score">0</span></span><span>CAN: <span id="space-lives" style="color:#ff5f56">❤️❤️❤️</span></span></div><canvas id="space-canvas" width="600" height="340" style="max-width:100%;background:#03010a;border:1px solid var(--accent);border-radius:10px"></canvas><p class="muted">A/D veya Sol/Sağ ile hareket et, Space tuşu ile ateş et! Asteroitlerden kaç.</p>`;size=['650px','470px'];break;
 }
 w.innerHTML=`<div class="whead" onmousedown="dragWindow(event,'${id}')"><div class="wtitle">${title}</div><div class="wcontrols"><button class="minb" title="Küçült" onclick="minApp('${id}')"></button><button class="maxb" title="Büyüt" onclick="maxApp('${id}')"></button><button class="closeb" title="Kapat" onclick="closeApp('${id}')"></button></div></div><div class="wbody">${body}</div>`;
 w.style.width=size[0];w.style.height=size[1];document.body.appendChild(w);windows[id]=w;
 const t=document.createElement('div');t.className='tbapp active';t.id='tb-'+id;t.textContent=apps[id][0];t.title=title;t.onclick=()=>{if(w.classList.contains('min'))w.classList.remove('min');else w.classList.add('min');w.style.zIndex=++z};document.getElementById('tbapps').appendChild(t);
 if(id==='pc'||id==='files')renderFiles();if(id==='browser')renderBrowserBookmarks();if(id==='paint')initPaint();if(id==='snake')initSnake();if(id==='spacegame')initSpace();if(id==='calendar')initCalendar();if(id==='tasks')renderTasks();
}
let z=1000;
function closeApp(id){
 if(id==='snake') clearInterval(snakeTimer);
 if(id==='spacegame') clearInterval(spaceTimer);
 windows[id]?.remove();delete windows[id];document.getElementById('tb-'+id)?.remove()
}
function minApp(id){windows[id]?.classList.add('min')}
function maxApp(id){let w=windows[id];if(!w)return;if(w.dataset.max==='1'){w.style.left=w.dataset.left;w.style.top=w.dataset.top;w.style.width=w.dataset.width;w.style.height=w.dataset.height;w.dataset.max='0'}else{w.dataset.left=w.style.left;w.dataset.top=w.style.top;w.dataset.width=w.style.width;w.dataset.height=w.style.height;w.style.left='0';w.style.top='0';w.style.width='100vw';w.style.height='calc(100vh - 68px)';w.dataset.max='1'}w.classList.remove('min')}
function dragWindow(e,id){if(e.target.tagName==='BUTTON')return;let w=windows[id];w.style.zIndex=++z;let x=e.clientX-w.offsetLeft,y=e.clientY-w.offsetTop;function move(ev){w.style.left=Math.max(0,ev.clientX-x)+'px';w.style.top=Math.max(0,ev.clientY-y)+'px'}function up(){document.removeEventListener('mousemove',move);document.removeEventListener('mouseup',up)}document.addEventListener('mousemove',move);document.addEventListener('mouseup',up)}
let browserHistory=JSON.parse(localStorage.getItem('wb-browser-history')||'[]'),browserIndex=-1;
function normalizeWebInput(raw){let v=String(raw||'').trim();if(!v)return '';if(/^https?:\/\//i.test(v))return v;if(/^[\w.-]+\.[a-z]{2,}(?::\d+)?(?:\/.*)?$/i.test(v)&&!v.includes(' '))return 'https://'+v;return 'https://www.google.com/search?q='+encodeURIComponent(v)}
function openBrowserURL(url,label){if(!url)return;let win=window.open(url,'_blank');if(!win){toast('Yeni sekme engellendi.');return}try{win.opener=null}catch(e){}browserHistory.unshift({label:label||url,url,time:new Date().toLocaleString('tr-TR')});browserHistory=browserHistory.slice(0,30);localStorage.setItem('wb-browser-history',JSON.stringify(browserHistory));browserIndex=0;let st=document.getElementById('browser-status-text');if(st)st.textContent='Açıldı: '+(label||url);renderBrowserBookmarks();toast('Yeni sekmede açıldı.')}
function browse(){const inp=document.getElementById('browser-url');const raw=inp?.value.trim();if(!raw)return toast('Arama veya adres yaz.');const url=normalizeWebInput(raw);openBrowserURL(url,raw);const home=document.getElementById('browser-home-search');if(home)home.value=raw}
function searchWeb(q){let inp=document.getElementById('browser-url');let query=(q||inp?.value||'').trim();if(!query)return toast('Kelime yaz.');if(inp)inp.value=query;openBrowserURL('https://www.google.com/search?q='+encodeURIComponent(query),'Google: '+query)}
function browserSearchEngine(engine){let inp=document.getElementById('browser-url'),home=document.getElementById('browser-home-search');let q=(home?.value||inp?.value||'').trim();if(!q){toast('Önce arama kelimesi yaz.');(home||inp)?.focus();return}if(inp)inp.value=q;let base=engine==='bing'?'https://www.bing.com/search?q=':engine==='duck'?'https://duckduckgo.com/?q=':'https://www.google.com/search?q=';openBrowserURL(base+encodeURIComponent(q),q)}
function browserSearchYouTube(){let home=document.getElementById('browser-home-search'),inp=document.getElementById('browser-url');let q=(home?.value||inp?.value||'').trim();if(!q){q=prompt('YouTube’da ne aramak istiyorsun?','');if(q===null)return;q=q.trim()}if(!q)return toast('Boş bırakılamaz.');if(inp)inp.value=q;openBrowserURL('https://www.youtube.com/results?search_query='+encodeURIComponent(q),'YouTube: '+q)}
function searchYouTube(){browserSearchYouTube()}
function goYouTube(){openBrowserURL('https://www.youtube.com/','YouTube')}
function openExternal(){browse()}
function browserBack(){if(browserHistory.length>1){let item=browserHistory[1];openBrowserURL(item.url,item.label)}else toast('Geri sayfa yok.')}
function browserForward(){toast('İleri gezinme tarayıcı üzerinden yapılır.')}
function browserHome(){let inp=document.getElementById('browser-url'),home=document.getElementById('browser-home-search');if(inp)inp.value='';if(home)home.value='';let h=document.getElementById('browser-home');if(h)h.style.display='flex'}
function browserBookmark(){let inp=document.getElementById('browser-url');let raw=inp?.value.trim();if(!raw)return toast('Önce adres aç.');let url=normalizeWebInput(raw);let list=JSON.parse(localStorage.getItem('wb-browser-bookmarks')||'[]');if(!list.some(x=>x.url===url)){list.unshift({label:raw,url});localStorage.setItem('wb-browser-bookmarks',JSON.stringify(list.slice(0,20)))}renderBrowserBookmarks();toast('Favorilere eklendi.')}
function renderBrowserBookmarks(){let el=document.getElementById('browser-bookmarks');if(!el)return;let list=JSON.parse(localStorage.getItem('wb-browser-bookmarks')||'[]');el.innerHTML=list.map((x,i)=>`<button onclick="openBrowserURL('${x.url.replace(/'/g,'%27')}','${escapeHTML(x.label).replace(/'/g,'&#39;')}')">☆ ${escapeHTML(x.label.slice(0,24))}</button>`).join('')}
function browserOpenHistory(){let list=JSON.parse(localStorage.getItem('wb-browser-history')||'[]');if(!list.length)return toast('Geçmiş yok.');let html=list.slice(0,12).map(x=>`${x.time} — ${x.label}`).join('\n');alert('Son Aramalar\n\n'+html)}
function requestNotifications(){if(!('Notification'in window))return toast('Desteklenmiyor.');Notification.requestPermission().then(p=>toast('Bildirim izni: '+p))}
function setPermissionStatus(t){let e=document.getElementById('permission-status');if(e)e.textContent=t;toast(t)}
function requestLocation(){if(!navigator.geolocation)return setPermissionStatus('Desteklenmiyor.');navigator.geolocation.getCurrentPosition(p=>setPermissionStatus('Konum alındı.'),e=>setPermissionStatus('Reddedildi.'))}
async function requestMedia(kind){try{let s=await navigator.mediaDevices.getUserMedia({audio:kind==='audio',video:kind==='video'});s.getTracks().forEach(t=>t.stop());setPermissionStatus('Erişim başarılı.')}catch(e){setPermissionStatus('Reddedildi.')}}
function showPermissionPrompt(){if(localStorage.getItem('wb-permission-prompted'))return;localStorage.setItem('wb-permission-prompted','1');document.getElementById('permission-overlay')?.classList.add('show')}
function dismissPermissionPrompt(){document.getElementById('permission-overlay')?.classList.remove('show')}
function renderFiles(){let el=document.getElementById('file-list');if(!el)return;el.innerHTML=filesDB.map((f,i)=>`<div class="card"><strong>📄 ${escapeHTML(f.name)}</strong><p class="muted">${f.content.length} karakter</p><div class="row" style="margin-top:8px"><button onclick="openApp('editor',filesDB[${i}].content)">Aç</button><button onclick="deleteFile(${i})">Sil</button></div></div>`).join('')||'<p class="muted">Dosya yok.</p>'}
function escapeHTML(s){return String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]))}
function createFile(){let n=document.getElementById('newfile-name').value.trim();if(!n)return toast('Dosya adı gir.');filesDB.push({name:n,content:''});persist();renderFiles()}
function deleteFile(i){filesDB.splice(i,1);persist();renderFiles()}
function uploadFile(e){let f=e.target.files[0];if(!f)return;let r=new FileReader();r.onload=()=>{filesDB.push({name:f.name,content:String(r.result)});persist();renderFiles();toast('Eklendi')};r.readAsText(f)}
function saveEditor(){let n=document.getElementById('editor-name').value||'YeniNot.txt',c=document.getElementById('editor-text').value;let i=filesDB.findIndex(f=>f.name===n);if(i>=0)filesDB[i].content=c;else filesDB.push({name:n,content:c});persist();toast('Kaydedildi')}
function downloadEditor(){let c=document.getElementById('editor-text').value,n=document.getElementById('editor-name').value||'not.txt';download(n,c,'text/plain;charset=utf-8')}
function download(name,content,type){let a=document.createElement('a');a.href=URL.createObjectURL(new Blob([content],{type}));a.download=name;a.click();URL.revokeObjectURL(a.href)}
function terminalKey(e){if(e.key!=='Enter')return;let input=document.getElementById('term-input'),log=document.getElementById('term-log'),c=input.value.trim(),out='';if(c==='help')out='help, clear, date, ver, dir, whoami, restart';else if(c==='clear'){log.textContent='';input.value='';return}else if(c==='date')out=new Date().toLocaleString();else if(c==='ver')out='Windows 12 Wild Berry [Build 2026.10]';else if(c==='dir')out=filesDB.map(f=>f.name).join('\n')||'Klasör boş';else if(c==='whoami')out='WildBerry\\Administrator';else if(c==='restart')return restartSystem();else if(c)out=`'${c}' tanınmayan komut.`;log.textContent+=`\nWB> ${c}\n${out}\n`;input.value='';log.scrollTop=log.scrollHeight}
let expr='';function calcPress(v){let d=document.getElementById('calc-display');if(!d)return;if(v==='C'){expr='';d.value='0';return}if(v==='='){try{if(!/^[0-9+*/(). ×÷−-]+$/.test(expr))throw 0;let safe=expr.replace(/×/g,'*').replace(/÷/g,'/').replace(/−/g,'-');if(!safe.trim())return;let result=Function('"use strict";return ('+safe+')')();if(!Number.isFinite(result))throw 0;expr=String(result);d.value=expr}catch{d.value='Hata';expr=''}return}expr+=v;d.value=expr}
function accent(c){document.documentElement.style.setProperty('--accent',c);document.documentElement.style.setProperty('--glow',c+'66')}
function wall(w){document.body.style.background=w==='aurora'?'linear-gradient(135deg,#050515,#120b2e,#00a8b8,#4facfe)':w==='cyber'?'linear-gradient(45deg,#0d001a,#2a0036,#ff0055,#ffcc00)':w==='dark'?'linear-gradient(135deg,#1a1a24,#08080c)':'radial-gradient(ellipse at 18% 15%,#ff2a75 0,#3a0050 38%,#0d001a 78%)'}
function initPaint(){let c=document.getElementById('paint-canvas');if(!c)return;let ctx=c.getContext('2d'),down=false;c.onpointerdown=e=>{down=true;c.setPointerCapture(e.pointerId);ctx.beginPath();ctx.moveTo(e.offsetX,e.offsetY)};c.onpointerup=()=>down=false;c.onpointermove=e=>{if(!down)return;ctx.strokeStyle=document.getElementById('paint-color').value;ctx.lineWidth=document.getElementById('paint-size').value;ctx.lineCap='round';ctx.lineTo(e.offsetX,e.offsetY);ctx.stroke()}}
function clearPaint(){let c=document.getElementById('paint-canvas');c?.getContext('2d').clearRect(0,0,c.width,c.height)}
function savePaint(){let c=document.getElementById('paint-canvas');let a=document.createElement('a');a.download='wild-paint.png';a.href=c.toDataURL('image/png');a.click()}

let snakeTimer,spaceTimer;
function initSnake(){let c=document.getElementById('snake-canvas');if(!c)return;clearInterval(snakeTimer);let ctx=c.getContext('2d'),s=[{x:10,y:10}],food={x:15,y:15},dx=1,dy=0;window.onkeydown=e=>{if(e.key==='ArrowUp'&&dy===0){dx=0;dy=-1}if(e.key==='ArrowDown'&&dy===0){dx=0;dy=1}if(e.key==='ArrowLeft'&&dx===0){dx=-1;dy=0}if(e.key==='ArrowRight'&&dx===0){dx=1;dy=0}};snakeTimer=setInterval(()=>{if(!document.getElementById('snake-canvas'))return clearInterval(snakeTimer);let h={x:s[0].x+dx,y:s[0].y+dy};if(h.x<0||h.x>=20||h.y<0||h.y>=20||s.some(p=>p.x===h.x&&p.y===h.y)){s=[{x:10,y:10}];dx=1;dy=0;return}s.unshift(h);if(h.x===food.x&&h.y===food.y)food={x:Math.random()*20|0,y:Math.random()*20|0};else s.pop();ctx.fillStyle='#08020f';ctx.fillRect(0,0,320,320);ctx.fillStyle='#00f2fe';ctx.fillRect(food.x*16,food.y*16,13,13);ctx.fillStyle='#ff2a7a';s.forEach(p=>ctx.fillRect(p.x*16,p.y*16,13,13))},130)}

// Geliştirilmiş 2D Uzay Savaşı Oyunu
function initSpace(){
  let c=document.getElementById('space-canvas');if(!c)return;clearInterval(spaceTimer);
  let ctx=c.getContext('2d'),x=270,bullets=[],enemies=[],asteroids=[],stars=[],score=0,lives=3,keys={};
  for(let i=0;i<50;i++) stars.push({x:Math.random()*c.width,y:Math.random()*c.height,size:Math.random()*2,speed:Math.random()*1.5+0.5});
  window.onkeydown=e=>{keys[e.key.toLowerCase()]=true;if(e.key===' ')bullets.push({x:x+18,y:300});};
  window.onkeyup=e=>keys[e.key.toLowerCase()]=false;
  
  spaceTimer=setInterval(()=>{
    if(!document.getElementById('space-canvas'))return clearInterval(spaceTimer);
    if(keys.arrowleft||keys.a)x=Math.max(0,x-6);
    if(keys.arrowright||keys.d)x=Math.min(c.width-40,x+6);
    if(Math.random()<.03) enemies.push({x:Math.random()*(c.width-30),y:-25,speed:Math.random()*2+1.5});
    if(Math.random()<.015) asteroids.push({x:Math.random()*(c.width-35),y:-35,size:Math.random()*15+15,speed:Math.random()*1+1});

    ctx.fillStyle='#03010a';ctx.fillRect(0,0,c.width,c.height);
    
    ctx.fillStyle='white';stars.forEach(s=>{s.y+=s.speed;if(s.y>c.height)s.y=0;ctx.fillRect(s.x,s.y,s.size,s.size)});
    
    ctx.fillStyle='#00f2fe';ctx.beginPath();ctx.moveTo(x+20,295);ctx.lineTo(x,330);ctx.lineTo(x+40,330);ctx.fill();
    ctx.fillStyle='#ff2a7a';ctx.shadowBlur=10;ctx.shadowColor='#ff2a7a';
    bullets.forEach(b=>{b.y-=9;ctx.fillRect(b.x,b.y,4,12)});
    ctx.shadowBlur=0;
    
    ctx.fillStyle='#ffcc00';
    enemies.forEach((e,i)=>{
      e.y+=e.speed;ctx.fillRect(e.x,e.y,26,26);
      if(Math.abs(e.x-x)<25&&Math.abs(e.y-300)<20){lives--;enemies.splice(i,1);if(lives<=0){alert('Oyun Bitti! Skorun: '+score);score=0;lives=3;}}
      bullets.forEach((b,j)=>{if(b.x>e.x&&b.x<e.x+26&&b.y>e.y&&b.y<e.y+26){enemies.splice(i,1);bullets.splice(j,1);score+=15;}});
    });

    ctx.fillStyle='#888';
    asteroids.forEach((a,i)=>{
      a.y+=a.speed;ctx.beginPath();ctx.arc(a.x,a.y,a.size,0,Math.PI*2);ctx.fill();
      if(Math.abs(a.x-x)<a.size+15&&Math.abs(a.y-300)<a.size+15){lives--;asteroids.splice(i,1);if(lives<=0){alert('Oyun Bitti! Skorun: '+score);score=0;lives=3;}}
    });

    bullets=bullets.filter(b=>b.y>0);enemies=enemies.filter(e=>e.y<c.height);asteroids=asteroids.filter(a=>a.y<c.height);
    document.getElementById('space-score').textContent=score;
    document.getElementById('space-lives').textContent='❤️'.repeat(Math.max(0,lives));
  },1000/60);
}

function loadMedia(e){let f=e.target.files[0];if(!f)return;let el=f.type.startsWith('video')?document.getElementById('media-player'):document.getElementById('audio-player');el.src=URL.createObjectURL(f);el.style.display='block';el.play().catch(()=>{})}
function initCalendar(){let d=new Date();document.getElementById('cal-title').textContent=d.toLocaleDateString('tr-TR',{weekday:'long',year:'numeric',month:'long',day:'numeric'});document.getElementById('calendar-date').value=d.toISOString().slice(0,10);document.getElementById('calendar-now').textContent='Bugün: '+d.toLocaleDateString('tr-TR')}
function addTask(){let i=document.getElementById('task-input');if(!i?.value.trim())return;let tasks=JSON.parse(localStorage.getItem('wb-tasks')||'[]');tasks.push(i.value.trim());localStorage.setItem('wb-tasks',JSON.stringify(tasks));i.value='';renderTasks()}
function renderTasks(){let el=document.getElementById('task-list');if(!el)return;let tasks=JSON.parse(localStorage.getItem('wb-tasks')||'[]');el.innerHTML=tasks.map((t,i)=>`<div class="card row"><span class="grow">${escapeHTML(t)}</span><button onclick="removeTask(${i})">✓</button></div>`).join('')}
function removeTask(i){let t=JSON.parse(localStorage.getItem('wb-tasks')||'[]');t.splice(i,1);localStorage.setItem('wb-tasks',JSON.stringify(t));renderTasks()}
document.getElementById('widget-note').value=localStorage.getItem('wb-note')||'';document.getElementById('widget-note').addEventListener('input',e=>localStorage.setItem('wb-note',e.target.value));
document.getElementById('time').textContent=new Date().toLocaleTimeString('tr-TR',{hour:'2-digit',minute:'2-digit'});setInterval(()=>document.getElementById('time').textContent=new Date().toLocaleTimeString('tr-TR',{hour:'2-digit',minute:'2-digit'}),1000);
window.addEventListener('load',()=>{setTimeout(()=>document.getElementById('boot').classList.add('hide'),1800);setTimeout(showPermissionPrompt,2400);let a=localStorage.getItem('wb-accent');if(a)accent(a);let p=localStorage.getItem('wb-taskpos');if(p)document.getElementById('taskwrap').style.justifyContent=p;let v=localStorage.getItem('wb-volume');if(v!==null){document.getElementById('volume-control').value=v;document.getElementById('volume-label').textContent=v+'%'}let b=localStorage.getItem('wb-brightness');if(b!==null){document.getElementById('brightness-control').value=b;document.getElementById('brightness-label').textContent=b+'%';document.body.style.filter='brightness('+b/100+')'}});
</script>
</body>
</html>
