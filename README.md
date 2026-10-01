
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LORE AUDIO</title>
<meta name="description" content="LORE AUDIO X Series — 15,000 RMS / 20,000 WATT yüksek performanslı subwooferlar.">
<style>
:root{--bg:#050505;--panel:#0b0b0d;--line:#242428;--red:#ff1838;--red2:#ff4b61;--white:#f5f5f5;--muted:#929298}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth;width:100%}
body{background:var(--bg);color:var(--white);font-family:Inter,Arial,Helvetica,sans-serif;overflow-x:hidden;width:100%}
body:before{content:"";position:fixed;inset:0;pointer-events:none;background:radial-gradient(circle at 50% 20%,rgba(255,24,56,.09),transparent 35%),linear-gradient(90deg,rgba(255,255,255,.018) 1px,transparent 1px),linear-gradient(rgba(255,255,255,.018) 1px,transparent 1px);background-size:auto,80px 80px;z-index:-1}
a{color:inherit;text-decoration:none}
.nav{height:78px;position:fixed;top:0;left:0;right:0;z-index:20;display:flex;align-items:center;justify-content:space-between;padding:0 5vw;background:rgba(5,5,5,.65);backdrop-filter:blur(18px);border-bottom:1px solid rgba(255,255,255,.07);width:100%}
.logo{font-size:21px;font-weight:900;letter-spacing:.18em}.logo span{color:var(--red)}
.navlinks{display:flex;gap:32px;color:#aaa;font-size:12px;letter-spacing:.12em;text-transform:uppercase}.navlinks a:hover{color:#fff}
.cart{border:1px solid #333;padding:11px 17px;border-radius:999px;font-size:11px;letter-spacing:.12em}.cart b{color:var(--red)}
.hero{min-height:100vh;padding:150px 5vw 80px;display:grid;grid-template-columns:1fr 1fr;align-items:center;gap:30px;width:100%}
.eyebrow{color:var(--red);font-size:11px;font-weight:800;letter-spacing:.32em;text-transform:uppercase;margin-bottom:22px}
h1{font-size:clamp(64px,10vw,150px);line-height:.82;letter-spacing:-.075em;font-weight:950}
h1 span{display:block;color:transparent;-webkit-text-stroke:1px #777}
.hero p{max-width:100%;margin:34px 0;color:#aaa;line-height:1.75;font-size:15px}
.btn{display:inline-flex;align-items:center;gap:15px;background:var(--red);padding:16px 22px;border-radius:4px;font-weight:800;font-size:12px;letter-spacing:.14em;text-transform:uppercase;transition:.25s}.btn:hover{transform:translateY(-3px);box-shadow:0 15px 40px rgba(255,24,56,.25)}
.heroVisual{height:570px;position:relative;display:grid;place-items:center;width:100%}
.glow{position:absolute;width:480px;height:480px;border-radius:50%;background:radial-gradient(circle,rgba(255,24,56,.18),transparent 65%);filter:blur(18px)}

.section{padding:130px 5vw;border-top:1px solid #161619;width:100%}
.sectionHead{display:flex;justify-content:space-between;align-items:end;gap:30px;margin-bottom:40px}
.sectionHead h2{font-size:clamp(40px,6vw,86px);letter-spacing:-.06em;line-height:.9}.sectionHead p{max-width:500px;color:#888;line-height:1.7;font-size:13px}
.specs{display:grid;grid-template-columns:repeat(4,1fr);border-top:1px solid var(--line);border-bottom:1px solid var(--line);width:100%}
.spec{padding:32px 24px;border-right:1px solid var(--line)}.spec:last-child{border-right:0}.spec strong{font-size:42px;letter-spacing:-.05em}.spec small{display:block;color:#777;font-size:10px;letter-spacing:.2em;text-transform:uppercase;margin-top:8px}

.explodeWrap{height:250vh;position:relative;width:100%}
.sticky{position:sticky;top:0;height:100vh;overflow:hidden;display:flex;align-items:center;justify-content:center}
.explodeTitle{position:absolute;left:5vw;top:16vh;z-index:5}.explodeTitle h2{font-size:clamp(45px,7vw,100px);line-height:.82;letter-spacing:-.06em}.explodeTitle p{color:#888;margin-top:20px;max-width:330px;font-size:13px;line-height:1.7}
.explode{width:min(450px,65vw);aspect-ratio:1;position:relative;transform:scale(calc(0.85 + var(--p)*0.15))}

.part{
  position:absolute;
  left:50%;
  top:50%;
  transform:translate(-50%, -50%) translateY(calc(var(--p) * var(--dy))) scale(calc(1 - var(--p) * 0.05));
  transition:transform 0.05s linear;
  display:flex;
  align-items:center;
  justify-content:center;
}

.p-frame{
  width:100%; height:100%;
  border-radius:50%;
  border:24px solid #141416;
  box-shadow:inset 0 0 0 4px #333, 0 0 25px rgba(0,0,0,0.8);
  background:radial-gradient(circle, transparent 58%, #1c1c20 60%, #0a0a0c 100%);
}

.p-cone{
  width:80%; height:80%;
  border-radius:50%;
  background:radial-gradient(circle at 50% 50%, #151518 0%, #28282d 35%, #0d0d0e 70%);
  border:4px solid #2a2a30;
  box-shadow:inset 0 0 30px #000;
}

.p-cap{
  width:36%; height:36%;
  border-radius:50%;
  background:radial-gradient(circle at 35% 30%, #3a3a40, #111 60%, #050507 90%);
  border:2px solid #555;
  box-shadow:0 10px 25px rgba(0,0,0,0.9);
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
}
.cap-brand{
  color:#fff;
  font-weight:900;
  font-size:clamp(10px, 1.8vw, 14px);
  letter-spacing:0.15em;
  text-shadow:0 0 8px rgba(255,24,56,0.6);
  user-select:none;
}
.cap-brand span{color:var(--red)}

.p-spider{
  width:65%; height:65%;
  border-radius:50%;
  border:8px dashed #ff1838;
  background:radial-gradient(circle, transparent 30%, rgba(255,24,56,0.25) 31%, transparent 70%);
  box-shadow:0 0 15px rgba(0,0,0,0.5);
}

.p-coil{
  width:28%; height:32%;
  border-radius:4px;
  border:4px solid #ff1838;
  background:repeating-linear-gradient(0deg, #ff1838, #ff1838 4px, #ff1838 5px, #5c3a19 7px);
  box-shadow:0 0 20px rgba(212,175,55,0.3);
}

.p-basket{
  width:88%; height:88%;
  border-radius:50%;
  border:12px solid #1f1f24;
  border-left-color:transparent;
  border-right-color:transparent;
  transform:translate(-50%, -50%) translateY(calc(var(--p) * var(--dy))) rotate(45deg);
}

.p-motor{
  width:48%; height:48%;
  border-radius:50%;
  background:radial-gradient(circle, #2a2a2e 0%, #0f0f12 70%, #000 100%);
  border:8px solid #222226;
  box-shadow:0 0 30px #000;
}

.label{position:absolute;color:#888;font-size:10px;letter-spacing:.2em;text-transform:uppercase;white-space:nowrap;pointer-events:none}
.l-cap{left:-20%; top:20%}
.l-cone{right:-25%; top:32%}
.l-spider{left:-25%; top:48%}
.l-coil{right:-25%; top:60%}
.l-basket{left:-20%; top:72%}
.l-motor{right:-20%; top:85%}

.explodeInfo{position:absolute;right:5vw;bottom:15vh;text-align:right;color:#777;font-size:11px;letter-spacing:.14em}.explodeInfo b{display:block;color:#fff;font-size:16px;margin-top:8px}

.x-promo-banner {
  width: 100%;
  margin: 0 0 50px 0;
  border: 1px solid var(--line);
  border-radius: 12px;
  overflow: hidden;
  background: #08080a;
  box-shadow: 0 15px 35px rgba(0,0,0,0.8);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
}

.x-promo-banner:hover {
  border-color: var(--red);
  box-shadow: 0 20px 45px rgba(255, 24, 56, 0.15);
}

.x-promo-banner img {
  width: 100%;
  height: auto;
  display: block;
  object-fit: contain;
}

.x-series-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
  width: 100%;
}

.x-card {
  background: linear-gradient(145deg, #0d0d0f, #050505);
  border: 1px solid var(--line);
  padding: 35px 25px;
  border-radius: 6px;
  text-align: center;
  position: relative;
  transition: transform 0.3s ease, border-color 0.3s ease, box-shadow 0.3s ease;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.x-card:hover {
  transform: translateY(-8px);
  border-color: var(--red);
  box-shadow: 0 15px 35px rgba(255, 24, 56, 0.15);
}

.x-card.featured {
  border-color: var(--red);
  background: linear-gradient(145deg, #12090c, #050505);
}

.x-badge {
  position: absolute;
  top: -12px;
  right: 20px;
  background: var(--red);
  color: #fff;
  font-size: 9px;
  font-weight: 900;
  padding: 4px 10px;
  border-radius: 20px;
  letter-spacing: 0.15em;
  text-transform: uppercase;
}

.x-card img {
  width: 100%;
  max-width: 100%;
  margin: 0 auto 20px;
  display: block;
  filter: drop-shadow(0 15px 25px rgba(0,0,0,0.8));
  transition: transform 0.3s ease;
}

.x-card:hover img {
  transform: scale(1.05);
}

.x-card h3 {
  font-size: 32px;
  font-weight: 900;
  letter-spacing: -0.04em;
  margin-bottom: 15px;
}

.x-specs-list {
  list-style: none;
  padding: 0;
  margin: 20px 0;
  border-top: 1px solid rgba(255,255,255,0.05);
}

.x-specs-list li {
  padding: 12px 0;
  border-bottom: 1px solid rgba(255,255,255,0.05);
  font-size: 13px;
  color: #aaa;
  display: flex;
  justify-content: space-between;
}

.x-specs-list li strong {
  color: #fff;
}

.product{display:grid;grid-template-columns:1.15fr .85fr;gap:80px;align-items:start;width:100%}
.productImage{border:1px solid #222;background:linear-gradient(145deg,#0d0d0f,#050505);padding:40px;min-height:580px;display:grid;place-items:center;width:100%}
.productInfo .eyebrow{margin-bottom:12px}.productInfo h2{font-size:clamp(48px,6vw,90px);letter-spacing:-.07em}.productInfo>p{color:#999;line-height:1.8;margin:25px 0 35px}
.price{font-size:54px;font-weight:900;letter-spacing:-.06em}.stock{display:flex;align-items:center;gap:10px;margin:18px 0 30px;font-size:11px;color:#aaa;text-transform:uppercase;letter-spacing:.12em}.dot{width:8px;height:8px;border-radius:50%;background:#c26c1c;box-shadow:0 0 12px #c26c1c}
.qty{display:flex;gap:10px;margin-bottom:12px}.qty button{width:45px;height:45px;border:1px solid #333;background:#0b0b0c;color:#fff;font-size:18px;cursor:pointer}.qty span{width:55px;display:grid;place-items:center;border:1px solid #333}.buy{width:100%;justify-content:center;border:0;cursor:pointer}
.notice{font-size:10px;color:#666;margin-top:15px;line-height:1.6}
.footer{padding:70px 5vw;border-top:1px solid #1c1c20;display:flex;justify-content:space-between;color:#666;font-size:10px;letter-spacing:.14em;text-transform:uppercase;width:100%}

.realX8{
  width:100%;
  height:auto;
  display:block;
  object-fit:contain;
  border-radius:6px;
  filter:drop-shadow(0 35px 55px rgba(0,0,0,.72));
  transition:transform .45s ease,filter .45s ease;
}
.heroVisual .realX8{width:100%;transform:scale(1.03)}
.heroVisual .realX8:hover{transform:scale(1.06);filter:drop-shadow(0 40px 70px rgba(255,24,56,.16))}
.productImage .realX8{width:100%}

@media(max-width:850px){
  .navlinks{display:none}
  .hero{grid-template-columns:1fr;padding-top:130px}
  .heroVisual{height:430px}
  .specs{grid-template-columns:1fr 1fr}
  .spec:nth-child(2){border-right:0}
  .spec:nth-child(-n+2){border-bottom:1px solid var(--line)}
  .explodeTitle{top:10vh;left:5vw}
  .explodeInfo{right:5vw;bottom:7vh}
  .product{grid-template-columns:1fr;gap:35px}
  .productImage{min-height:420px}
  .heroVisual .realX8{width:100%}
  .x-series-grid{grid-template-columns:1fr}
  .footer{flex-direction:column;gap:18px}
}
</style>
</head>
<body>
<nav class="nav">
  <a class="logo" href="#">LORE <span>AUDIO</span></a>
  <div class="navlinks"><a href="#technology">Teknoloji</a><a href="#inside">İç Yapı</a><a href="#x-series">X Series</a><a href="#x6">X6</a><a href="#x7">X7</a><a href="#x8">X8</a></div>
  <a class="cart" href="#x8">SEPET <b id="cartCount">0</b></a>
</nav>

<header class="hero">
  <div>
    <div class="eyebrow">ENGINEERED FOR PRESSURE</div>
    <h1>X8<span>15000 RMS</span></h1>
    <p>LORE AUDIO X8, yüksek SPL ve derin bas için tasarlanmış ekstrem sınıf bir subwoofer konseptidir. 15.000 RMS ve 20.000 WATT maksimum güç iddiasını taşıyan, ağır hizmet tipi motor ve yüksek excursion odaklı yapı.</p>
    <a class="btn" href="#x8">X8'İ İNCELE →</a>
  </div>
  <div class="heroVisual">
    <div class="glow"></div>
    <img class="realX8" src="https://www.image2url.com/r2/default/images/1790821930673-c3fa41b5-6a57-41a7-95d4-eb176922a29e.jfif" alt="LORE AUDIO X8 Subwoofer">
  </div>
</header>

<section class="specs" id="technology">
  <div class="spec"><strong>15000</strong><small>RMS Güç</small></div>
  <div class="spec"><strong>20000</strong><small>Tepe Gücü (W)</small></div>
  <div class="spec"><strong>6"</strong><small>Alüminyum Bobin</small></div>
  <div class="spec"><strong>152dB</strong><small>Hassasiyet (1W/1M)</small></div>
</section>

<section class="explodeWrap" id="inside">
  <div class="sticky">
    <div class="explodeTitle">
      <div class="eyebrow">İÇ MÜHENDİSLİK</div>
      <h2>DEMONTE<br>MİMARİ</h2>
      <p>Aşağı kaydırarak LORE AUDIO X8'in yüksek bas basıncı üreten hassas iç katmanlarını ve mühendislik detaylarını inceleyin.</p>
    </div>

    <div class="explode" id="explodeSub">
      <div class="part p-frame" style="--dy:-220px">
        <span class="label l-frame">Dış Çerçeve / Conta</span>
      </div>
      <div class="part p-cap" style="--dy:-140px">
        <div class="cap-brand">LORE <span>AUDIO</span></div>
        <span class="label l-cap">Göbek Kapağı</span>
      </div>
      <div class="part p-cone" style="--dy:-70px">
        <span class="label l-cone">Ağır Hizmet Konisi</span>
      </div>
      <div class="part p-spider" style="--dy:0px">
        <span class="label l-spider">Çift Örümcek</span>
      </div>
      <div class="part p-coil" style="--dy:70px">
        <span class="label l-coil">6" CCAW Bobin</span>
      </div>
      <div class="part p-basket" style="--dy:140px">
        <span class="label l-basket">Alüminyum Sepet</span>
      </div>
      <div class="part p-motor" style="--dy:220px">
        <span class="label l-motor">Üçlü Mıknatıs Motor</span>
      </div>
    </div>

    <div class="explodeInfo">
      YÜKSEK BAS HASSASİYETİ
      <b>X8 SERİSİ</b>
    </div>
  </div>
</section>

<section class="section" id="x-series">
  <div class="sectionHead">
    <div>
      <div class="eyebrow">LINEUP</div>
      <h2>X SERIES</h2>
    </div>
    <p>Ekstrem basınç ve yarışma standartları için özel olarak mühendisliği yapılmış X Serisi performans canavarları.</p>
  </div>

  <div class="x-promo-banner">
    <img src="https://www.image2url.com/r2/default/images/1790831606439-a22ba8f1-5316-4ff3-bcda-84501024c21f.png" alt="LORE AUDIO X Series Lineup Showcase">
  </div>

  <div class="x-series-grid">
    <div class="x-card">
      <div>
        <img class="realX8" src="https://www.image2url.com/r2/default/images/1790833112671-69550471-bab7-4089-b492-76cbbdbf87a8.png" alt="LORE AUDIO X6 Subwoofer">
        <h3>X6 SUBWOOFER</h3>
        <p style="font-size: 12px; color: #888;">Ekstrem basınç sürücüsü.</p>
        <ul class="x-specs-list">
          <li><span>Maksimum Güç:</span> <strong>8.000 WATT</strong></li>
          <li><span>RMS Güç:</span> <strong>6.000 RMS</strong></li>
          <li><span>Ses Bobini:</span> <strong>4" Voice Coil</strong></li>
        </ul>
      </div>
      <a class="btn" href="#x6" style="justify-content: center; margin-top: 15px;">İNCELE</a>
    </div>

    <div class="x-card">
      <div>
        <img class="realX8" src="https://www.image2url.com/r2/default/images/1790833129928-cd555ade-82b1-4157-b288-c7f7f14fc03e.png" alt="LORE AUDIO X7 Subwoofer">
        <h3>X7 SUBWOOFER</h3>
        <p style="font-size: 12px; color: #888;">Üst düzey dengeli SPL gücü.</p>
        <ul class="x-specs-list">
          <li><span>Maksimum Güç:</span> <strong>12.000 WATT</strong></li>
          <li><span>RMS Güç:</span> <strong>9.000 RMS</strong></li>
          <li><span>Ses Bobini:</span> <strong>4.5" Voice Coil</strong></li>
        </ul>
      </div>
      <a class="btn" href="#x7" style="justify-content: center; margin-top: 15px;">İNCELE</a>
    </div>

    <div class="x-card featured">
      <div class="x-badge">FLAGSHIP</div>
      <div>
        <img class="realX8" src="https://www.image2url.com/r2/default/images/1790833158380-53034ebf-0df6-41b4-9faa-eb52feb4dc10.png" alt="LORE AUDIO X8 Subwoofer">
        <h3>X8 SUBWOOFER</h3>
        <p style="font-size: 12px; color: #888;">Sınırları zorlayan yok edici amiral gemisi.</p>
        <ul class="x-specs-list">
          <li><span>Maksimum Güç:</span> <strong>20.000 WATT</strong></li>
          <li><span>RMS Güç:</span> <strong>15.000 RMS</strong></li>
          <li><span>Ses Bobini:</span> <strong>6" Voice Coil</strong></li>
        </ul>
      </div>
      <a class="btn" href="#x8" style="justify-content: center; margin-top: 15px;">İNCELE</a>
    </div>
  </div>
</section>

<section class="section product" id="x6">
  <div class="productImage">
    <img class="realX8" src="https://www.image2url.com/r2/default/images/1790833112671-69550471-bab7-4089-b492-76cbbdbf87a8.png" alt="LORE AUDIO X6 Subwoofer">
  </div>
  <div class="productInfo">
    <div class="eyebrow">HIGH PERFORMANCE BASS</div>
    <h2>LORE AUDIO X6</h2>
    <p>Kendi sınıfının en hırslı modellerinden biri. 4 inç yüksek sıcaklık toleranslı bobin yapısı ve optimize edilmiş soğutma blokları sayesinde uzun süreli bas performansını stabil tutar.</p>
    <div class="price">$1100</div>
    <div class="stock"><span class="dot"></span> Çok Yakında Stokta — Hızlı Kargo</div>
    <div class="qty">
      <button onclick="changeQtyX6(-1)">-</button>
      <span id="qtyValX6">1</span>
      <button onclick="changeQtyX6(1)">+</button>
    </div>
    <button class="btn buy" onclick="addToCartX6()">SEPETE EKLE</button>
    <div class="notice">* Profesyonel montaj ve uygun güçte amfi kullanımı tavsiye edilir. (Amfi: 1 ohM 6000W-8000W)</div>
    <div class="notice" style="font-size: 12px; color: rgba(255, 59, 24, 0.959); line-height: 1.5; font-family: sans-serif;">
      <strong style="font-size: 13px; color: #faf7f7; display: block; margin-bottom: 4px;">Technical Features:</strong>
      <ul style="margin: 0; padding-left: 16px; list-style-type: disc;">
        <li><strong>RMS Power:</strong> 6000 W</li>
        <li><strong>Peak Power:</strong> 8000 W</li>
        <li><strong>Voice Coil:</strong> 4" Voice Coil</li>
        <li><strong>Xmax (BL 50%):</strong> 28 mm (One Way)</li>
        <li><strong>Xmax (BL 100%):</strong> 57 mm (One Way)</li>
        <li><strong>Re:</strong> 1.0 + 1.0 Ω</li>
        <li><strong>Fs:</strong> 24.8 Hz</li>
        <li><strong>Qts:</strong> 0.295</li>
        <li><strong>Sd:</strong> 1150 cm²</li>
        <li><strong>Vas:</strong> 117 L</li>
        <li><strong>BL:</strong> 17.4 T·m</li>
        <li><strong>Sens (1W/1m):</strong> 98.7 dB</li>
        <li><strong>Sens (2.83Vrms/1m):</strong> 109.2 dB</li>
        <li><strong>Impedance:</strong> 1.0 + 1.0 Ohm</li>
      </ul>
    </div>
  </div>
</section>

<section class="section product" id="x7">
  <div class="productImage">
    <img class="realX8" src="https://www.image2url.com/r2/default/images/1790833129928-cd555ade-82b1-4157-b288-c7f7f14fc03e.png" alt="LORE AUDIO X7 Subwoofer">
  </div>
  <div class="productInfo">
    <div class="eyebrow">UNMATCHED POWER & PRECISION</div>
    <h2>LORE AUDIO X7</h2>
    <p>Ağır hizmet kullanım şartları ve yarışma sistemleri için geliştirildi. 4.5 inç özel sarım bobini ile agresif ısı dağılımı sağlarken en alt frekanslarda bile yüksek bas kontrolü sunar.</p>
    <div class="price">$2200</div>
    <div class="stock"><span class="dot"></span> Çok Yakında Stokta — Hızlı Kargo</div>
    <div class="qty">
      <button onclick="changeQtyX7(-1)">-</button>
      <span id="qtyValX7">1</span>
      <button onclick="changeQtyX7(1)">+</button>
    </div>
    <button class="btn buy" onclick="addToCartX7()">SEPETE EKLE</button>
    <div class="notice">* Profesyonel montaj ve uygun güçte amfi kullanımı tavsiye edilir. (Amfi: 1 ohM 9000W-12000W)</div>
    <div class="notice" style="font-size: 12px; color: rgba(255, 59, 24, 0.959); line-height: 1.5; font-family: sans-serif;">
      <strong style="font-size: 13px; color: #faf7f7; display: block; margin-bottom: 4px;">Technical Features:</strong>
      <ul style="margin: 0; padding-left: 16px; list-style-type: disc;">
        <li><strong>RMS Power:</strong> 9000 W</li>
        <li><strong>Peak Power:</strong> 12000 W</li>
        <li><strong>Voice Coil:</strong> 4.5" Voice Coil</li>
        <li><strong>Xmax (BL 50%):</strong> 36 mm (One Way)</li>
        <li><strong>Xmax (BL 100%):</strong> 72 mm (One Way)</li>
        <li><strong>Re:</strong> 0.7 + 0.7 Ω</li>
        <li><strong>Fs:</strong> 21.2 Hz</li>
        <li><strong>Qts:</strong> 0.259</li>
        <li><strong>Sd:</strong> 1280 cm²</li>
        <li><strong>Vas:</strong> 148 L</li>
        <li><strong>BL:</strong> 22.1 T·m</li>
        <li><strong>Sens (1W/1m):</strong> 113.7 dB</li>
        <li><strong>Sens (2.83Vrms/1m):</strong> 119.4 dB</li>
        <li><strong>Impedance:</strong> 0.7 + 0.7 Ohm</li>
      </ul>
    </div>
  </div>
</section>

<section class="section product" id="x8">
  <div class="productImage">
    <img class="realX8" src="https://www.image2url.com/r2/default/images/1790833158380-53034ebf-0df6-41b4-9faa-eb52feb4dc10.png" alt="LORE AUDIO X8 Subwoofer">
  </div>
  <div class="productInfo">
    <div class="eyebrow">DESTROY YOUR CAR</div>
    <h2>LORE AUDIO X8</h2>
    <p>Rakipleri geride bırakmak için özel olarak üretildi. Yüksek ısılara dayanıklı ses bobini ve esnek örümcek yapısı sayesinde uzun süreli yüksek güç altındaki performansını korur.</p>
    <div class="price">$2999</div>
    <div class="stock"><span class="dot"></span> Çok Yakında Stokta — Hızlı Kargo</div>
    <div class="qty">
      <button onclick="changeQty(-1)">-</button>
      <span id="qtyVal">1</span>
      <button onclick="changeQty(1)">+</button>
    </div>
    <button class="btn buy" onclick="addToCart()">SEPETE EKLE</button>
    <div class="notice">* Profesyonel montaj ve uygun güçte amfi kullanımı tavsiye edilir. (Amfi: 1 ohM 15000W-20000W)</div>
    <div class="notice" style="font-size: 12px; color: rgba(255, 59, 24, 0.959); line-height: 1.5; font-family: sans-serif;">
      <strong style="font-size: 13px; color: #faf7f7; display: block; margin-bottom: 4px;">Technical Features:</strong>
      <ul style="margin: 0; padding-left: 16px; list-style-type: disc;">
        <li><strong>RMS Power:</strong> 15000 W</li>
        <li><strong>Peak Power:</strong> 20000 W</li>
        <li><strong>Xmax (BL 50%):</strong> 42 mm (One Way)</li>
        <li><strong>Xmax (BL 100%):</strong> 84 mm (One Way)</li>
        <li><strong>Re:</strong> 0.5 + 0.5 Ω</li>
        <li><strong>Fs:</strong> 15.6 Hz</li>
        <li><strong>Qts:</strong> 0.146</li>
        <li><strong>Sd:</strong> 1392 cm²</li>
        <li><strong>Vas:</strong> 196 L / 6.93 ft³</li>
        <li><strong>BL:</strong> 36.9 T·m</li>
        <li><strong>Sens (1W/1m):</strong> 152.1 dB</li>
        <li><strong>Sens (2.83Vrms/1m):</strong> 156.4 dB</li>
        <li><strong>Impedance:</strong> 0.5 + 0.5 Ohm</li>
      </ul>
    </div>
  </div>
</section>

<footer class="footer">
  <div>© 2026 LORE AUDIO. TÜM HAKLARI SAKLIDIR.</div>
  <div>TESTOSTERONE PERFORMANCE CAR AUDIO SYSTEMS</div>
</footer>

<script>
window.addEventListener('scroll', () => {
  const wrap = document.getElementById('inside');
  const rect = wrap.getBoundingClientRect();
  const total = wrap.offsetHeight - window.innerHeight;
  let progress = -rect.top / total;
  
  if (progress < 0) progress = 0;
  if (progress > 1) progress = 1;
  
  document.getElementById('explodeSub').style.setProperty('--p', progress);
});

let cart = 0;

let qty = 1;
function changeQty(v) {
  qty += v;
  if (qty < 1) qty = 1;
  document.getElementById('qtyVal').innerText = qty;
}
function addToCart() {
  cart += qty;
  document.getElementById('cartCount').innerText = cart;
  alert('X8 sepete eklendi!');
}

let qtyX7 = 1;
function changeQtyX7(v) {
  qtyX7 += v;
  if (qtyX7 < 1) qtyX7 = 1;
  document.getElementById('qtyValX7').innerText = qtyX7;
}
function addToCartX7() {
  cart += qtyX7;
  document.getElementById('cartCount').innerText = cart;
  alert('X7 sepete eklendi!');
}

let qtyX6 = 1;
function changeQtyX6(v) {
  qtyX6 += v;
  if (qtyX6 < 1) qtyX6 = 1;
  document.getElementById('qtyValX6').innerText = qtyX6;
}
function addToCartX6() {
  cart += qtyX6;
  document.getElementById('cartCount').innerText = cart;
  alert('X6 sepete eklendi!');
}
</script>
</body>
</html>
