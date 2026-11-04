<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#000000">
<title>Hotel Jagdamba Family Restaurant & Dhaba</title>
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700;900&family=Montserrat:wght@500;600;700;800&family=Hind:wght@500;600;700&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
<style>
:root{--g:linear-gradient(90deg,#bf953f,#fcf6ba,#b38728,#fcf6ba,#aa771c);--gold:#c9a24a;--gl:#fcf6ba;--box:#0c0c0c;--ln:#262626;--veg:#00c853;--nv:#ff3b3b;--mute:#a8a29a}
*{box-sizing:border-box;-webkit-tap-highlight-color:transparent}
body{margin:0;background:#000;color:#fff;font-family:'Montserrat','Hind',sans-serif;padding-bottom:110px}
button,input,select{font-family:inherit}
:focus-visible{outline:2px solid var(--gl);outline-offset:2px}
.hero{text-align:center;padding:calc(env(safe-area-inset-top,0px) + 46px) 16px 38px;background:linear-gradient(180deg,rgba(0,0,0,.55),rgba(0,0,0,.7) 60%,#000),url('https://images.unsplash.com/photo-1585937421612-70a008356fbe?auto=format&fit=crop&w=1200&q=70') center/cover;border-bottom:2px solid var(--gold);border-radius:0 0 30px 30px}
.hero h1{font-family:'Cinzel',serif;font-size:30px;line-height:1.15;margin:12px 0 0;letter-spacing:2px;background:var(--g);-webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent}
.sub{display:flex;align-items:center;justify-content:center;gap:10px;margin-top:10px;color:var(--gl);font-size:12px;font-weight:700;letter-spacing:4px}
.sub i{height:1px;width:34px;background:var(--gold)}
.tagline{color:#e6d9a8;font-size:14px;margin-top:10px;font-weight:600}
.tbl{display:none;margin:14px auto 0;width:max-content;padding:6px 18px;border-radius:30px;border:1px solid var(--gold);color:var(--gl);font-weight:700}
.sticky{position:sticky;top:0;z-index:50;background:#000;padding:12px 14px 8px}
.search{width:100%;padding:13px 16px;border-radius:14px;border:1.5px solid #2c2c2c;background:#101010;color:#fff;font-size:15px;margin-bottom:10px}
.types{display:flex;gap:8px;margin-bottom:10px}
.tb{flex:1;padding:9px;border-radius:30px;border:1.5px solid #333;background:#111;color:#bbb;font-weight:800;font-size:12px;cursor:pointer;display:flex;gap:6px;align-items:center;justify-content:center}
.tb b{width:10px;height:10px;border-radius:2px}
.tb.on{background:var(--g);color:#000;border-color:transparent}
.tb.v.on{background:var(--veg);color:#fff}.tb.n.on{background:var(--nv);color:#fff}
.cats{display:flex;gap:8px;overflow-x:auto;scrollbar-width:none}.cats::-webkit-scrollbar{display:none}
.chip{padding:9px 18px;border-radius:30px;border:1px solid #333;background:#111;color:#bbb;font-weight:700;font-size:13px;white-space:nowrap;cursor:pointer}
.chip.on{background:var(--g);color:#000;border-color:transparent}
.sec{font-family:'Cinzel',serif;color:var(--gl);font-size:19px;margin:22px 16px 4px;letter-spacing:1px}
.item{display:flex;gap:14px;background:var(--box);margin:12px 14px;border-radius:18px;border:1px solid var(--ln);padding:13px;align-items:center}
.item img{width:84px;height:84px;border-radius:13px;object-fit:cover;border:1px solid #333;background:#111;flex:none}
.inf{flex:1;min-width:0}
.name{font-weight:800;font-size:16px;line-height:1.25}
.vd{display:inline-grid;place-items:center;width:14px;height:14px;border:1.5px solid var(--veg);border-radius:3px;margin-right:6px;vertical-align:-1px}
.vd i{width:6px;height:6px;border-radius:50%;background:var(--veg)}.vd.n{border-color:var(--nv)}.vd.n i{background:var(--nv)}
.desc{font-size:12.5px;color:var(--mute);margin:4px 0 7px;line-height:1.4;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}
.row{display:flex;justify-content:space-between;align-items:center}
.price{color:var(--gl);font-weight:800;font-size:18px}
.add{padding:8px 24px;border-radius:12px;border:1.5px solid var(--gold);background:transparent;color:var(--gl);font-weight:800;cursor:pointer}
.add:active{background:var(--g);color:#000}
.qty{display:flex;align-items:center;background:var(--g);color:#000;border-radius:12px;font-weight:800}
.qty button{background:none;border:0;font-size:20px;width:36px;height:34px;cursor:pointer;color:#000;font-weight:800}
.qty span{min-width:20px;text-align:center}
.item.sold{opacity:.5}.item.sold img{filter:grayscale(1)}.soldtag{color:#999;font-weight:700;font-size:13px}
.empty{text-align:center;color:#777;padding:44px 20px}
.sk{height:110px;margin:12px 14px;border-radius:18px;background:linear-gradient(90deg,#101010 25%,#1a1a1a 50%,#101010 75%);background-size:200% 100%;animation:sh 1.3s infinite}@keyframes sh{to{background-position:-200% 0}}
.call{margin:28px 14px;padding:22px;text-align:center;border:1px solid var(--gold);border-radius:20px;background:var(--box)}
.call h3{font-family:'Cinzel',serif;margin:0 0 14px;color:var(--gl)}
.call a{display:block;background:var(--g);color:#000;font-weight:800;padding:14px;border-radius:40px;text-decoration:none}
.bar{position:fixed;left:14px;right:14px;bottom:calc(env(safe-area-inset-bottom,0px) + 14px);height:64px;background:var(--g);color:#000;border-radius:18px;display:none;align-items:center;justify-content:space-between;padding:0 22px;font-weight:800;z-index:90;cursor:pointer;box-shadow:0 8px 30px rgba(201,162,74,.35);animation:rise .3s ease}
@keyframes rise{from{transform:translateY(30px);opacity:0}}
.bar small{display:block;font-size:12px;font-weight:700;opacity:.75}.bar b{font-size:21px}
.ov{position:fixed;inset:0;background:rgba(0,0,0,.94);display:none;z-index:200;overflow-y:auto}.ov.open{display:block}
.sheet{background:#080808;margin:3vh auto;width:92%;max-width:480px;border:1.5px solid var(--gold);border-radius:24px;padding:24px 20px}
.sheet h2{font-family:'Cinzel',serif;color:var(--gl);margin:0 0 12px;text-align:center}
.ln{display:flex;justify-content:space-between;gap:10px;padding:9px 0;border-bottom:1px dashed #2b2b2b;font-size:14px;font-weight:600}
.ln .c button{background:none;border:1px solid var(--gold);color:var(--gl);width:26px;height:26px;border-radius:8px;margin-left:6px;cursor:pointer}
.tot{display:flex;justify-content:space-between;font-family:'Cinzel',serif;font-size:22px;color:var(--gl);margin:12px 0 14px}
.seg{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:10px}
.seg button{padding:12px;border-radius:12px;border:1.5px solid #333;background:#000;color:#ccc;font-weight:700;font-size:13px;cursor:pointer}
.seg button.on{background:var(--g);color:#000;border-color:transparent}
.inp{width:100%;padding:14px;margin-bottom:10px;border-radius:12px;border:1.5px solid #333;background:#000;color:#fff;font-size:15px;font-weight:600}
.go{display:block;width:100%;padding:16px;border-radius:14px;border:0;background:var(--g);color:#000;font-weight:800;font-size:16px;cursor:pointer;text-align:center;text-decoration:none;margin-top:8px}
.go.alt{background:#151515;color:#fff;border:1.5px solid #333}.go.wa{background:#25d366;color:#fff}
.back{display:block;margin:12px auto 0;background:none;border:0;color:#888;text-decoration:underline;cursor:pointer}
.err{color:#ff6b6b;font-size:13px;min-height:18px;margin:0 0 4px}
.bill{background:#000;border:2.5px solid var(--gold);border-radius:20px;padding:16px;color:#fff}
.bi{border:1px solid rgba(201,162,74,.45);border-radius:14px;padding:18px 16px}
.bh{text-align:center}
.bh h1{font-family:'Cinzel',serif;font-size:22px;margin:6px 0 0;color:var(--gold);letter-spacing:2px;line-height:1.2}
.bh p{margin:6px 0 0;color:var(--gl);font-size:11px;letter-spacing:4px;font-weight:700}
.bh .ph{font-size:13px;margin-top:8px;color:var(--gl);font-weight:600}
.dv{height:1px;background:repeating-linear-gradient(90deg,var(--gold) 0 6px,transparent 6px 12px);margin:14px 0;opacity:.7}
.meta{display:grid;grid-template-columns:1fr 1fr;gap:8px 16px;font-size:12.5px}
.meta div{display:flex;justify-content:space-between;gap:8px}.meta span{color:#bdb6a6}.meta b{text-align:right}
table{width:100%;border-collapse:collapse;font-size:13px}
th{color:var(--gl);text-align:left;padding:8px 4px;border-bottom:1px dashed rgba(201,162,74,.5);font-size:12px}
th:nth-child(n+2),td:nth-child(n+2){text-align:right}
td{padding:9px 4px;border-bottom:1px dashed rgba(255,255,255,.1);font-weight:600}
.dt{display:inline-block;width:10px;height:10px;border-radius:2px;margin-right:7px}
.sm{display:flex;justify-content:space-between;font-size:13px;padding:4px;color:#cfc8b8}
.gt{display:flex;justify-content:space-between;font-family:'Cinzel',serif;font-size:25px;color:var(--gold);font-weight:900;padding:10px 4px 6px}
.ps{margin-top:10px;padding:14px;border-radius:12px;border:1.5px solid var(--gold);background:rgba(201,162,74,.07)}
.ps b{display:block;font-family:'Cinzel',serif;color:var(--gold);font-size:16px;letter-spacing:1px}.ps small{color:#cfc8b8;font-size:12px}
.qrw{display:none;margin-top:12px;gap:14px;align-items:center}
.qrb{background:#fff;padding:9px;border-radius:12px;line-height:0;flex:none}
.qrw p{margin:0;font-size:12.5px;color:#cfc8b8;line-height:1.5}.qrw p strong{color:var(--gl)}
.thanks{text-align:center;color:var(--gl);font-size:13px;margin-top:14px;font-weight:600}
.toast{position:fixed;top:16px;left:50%;transform:translateX(-50%);background:var(--gold);color:#000;padding:10px 18px;border-radius:30px;font-weight:700;font-size:13px;z-index:500;display:none}
@media print{body>*:not(#qrOv){display:none!important}.no{display:none!important}}
@media (prefers-reduced-motion:reduce){*{animation:none!important}}
</style>
</head>
<body>

<header class="hero">
  <svg width="64" height="64" viewBox="0 0 64 64" aria-hidden="true"><circle cx="32" cy="32" r="29" fill="#000" stroke="#c9a24a" stroke-width="2.5"/><circle cx="32" cy="32" r="24" fill="none" stroke="#c9a24a" stroke-width=".8"/><text x="32" y="40" text-anchor="middle" font-family="Cinzel,serif" font-weight="900" font-size="22" fill="#fcf6ba">HJ</text></svg>
  <h1>Hotel Jagdamba</h1>
  <div class="sub"><i></i>FAMILY RESTAURANT & DHABA<i></i></div>
  <div class="tagline">स्वाद जो दिल जीत ले</div>
  <div class="tbl" id="tbl"></div>
</header>

<div class="sticky">
  <input class="search" id="q" type="search" placeholder="डिश खोजें… (paneer, thali, chai)" aria-label="Search">
  <div class="types">
    <button class="tb on" data-t="all"><b style="background:linear-gradient(90deg,#00c853 50%,#ff3b3b 50%)"></b>सभी</button>
    <button class="tb v" data-t="veg"><b style="background:var(--veg)"></b>Veg</button>
    <button class="tb n" data-t="nv"><b style="background:var(--nv)"></b>Non-Veg</button>
  </div>
  <div class="cats" id="cats"></div>
</div>

<main id="menu"><div class="sk"></div><div class="sk"></div><div class="sk"></div></main>

<section class="call"><h3>कोई ख़ास रिक्वेस्ट?</h3><a id="callBtn" href="#">होटल जगदंबा को कॉल करें</a></section>

<div class="bar" id="bar"><div><small id="bc"></small><b id="bt">₹0</b></div><span>ऑर्डर देखें ›</span></div>

<div class="ov" id="cartOv"><div class="sheet">
  <h2>आपका ऑर्डर</h2>
  <div id="lines"></div>
  <div class="tot"><span>सब-टोटल</span><span id="sub">₹0</span></div>
  <div class="seg" id="modeSeg"><button data-m="Dining" class="on">🍽️ होटल में</button><button data-m="Delivery">🛵 डिलीवरी</button></div>
  <input class="inp" id="nm" placeholder="आपका नाम" autocomplete="name">
  <input class="inp" id="info" placeholder="टेबल नंबर">
  <input class="inp" id="ph" placeholder="मोबाइल नंबर" inputmode="tel">
  <p class="err" id="err"></p>
  <button class="go" id="mkBill">बिल बनाएँ ›</button>
  <button class="back" id="closeCart">वापस जाएँ</button>
</div></div>

<div class="ov" id="billOv"><div class="sheet" style="padding:14px">
  <div class="bill" id="bill"><div class="bi">
    <div class="bh">
      <svg width="46" height="46" viewBox="0 0 64 64"><circle cx="32" cy="32" r="29" fill="#000" stroke="#c9a24a" stroke-width="3"/><text x="32" y="40" text-anchor="middle" font-family="Cinzel,serif" font-weight="900" font-size="22" fill="#fcf6ba">HJ</text></svg>
      <h1>HOTEL JAGDAMBA</h1><p>FAMILY RESTAURANT & DHABA</p><div class="ph" id="bph"></div>
    </div>
    <div class="dv"></div>
    <div class="meta" id="meta"></div>
    <div class="dv"></div>
    <table><thead><tr><th>आइटम</th><th>मात्रा</th><th>रेट</th><th>रकम</th></tr></thead><tbody id="bbody"></tbody></table>
    <div id="bsums"></div>
    <div class="gt"><span>कुल बिल</span><span id="bgt"></span></div>
    <div class="ps"><b id="psT"></b><small id="psS"></small></div>
    <div class="qrw" id="qrw"><div class="qrb"><div id="qrimg"></div></div><p><strong>QR स्कैन करके पे करें</strong><br>PhonePe, GPay, Paytm — कोई भी UPI ऐप। रकम अपने-आप भर जाएगी।</p></div>
    <div class="thanks">🙏 धन्यवाद! फिर पधारिए।</div>
  </div></div>
  <div class="seg" id="paySeg" style="margin-top:14px"><button data-p="UPI" class="on">📲 UPI से पे करें</button><button data-p="Cash">💵 होटल में पे करें</button></div>
  <a class="go" id="upiApp" href="#">UPI ऐप खोलें</a>
  <button class="go wa" id="sendWA">WhatsApp पर ऑर्डर भेजें</button>
  <button class="go alt" id="dlPdf">बिल PDF डाउनलोड करें</button>
  <button class="back" id="editOrder">ऑर्डर बदलें</button>
</div></div>

<div class="ov" id="qrOv"><div class="sheet" style="text-align:center">
  <h2>Permanent QR</h2>
  <p style="color:#aaa;font-size:13px;margin-top:0">यह QR कभी नहीं बदलेगा। Sheet अपडेट करते ही मेन्यू अपने-आप अपडेट हो जाएगा।</p>
  <div style="background:#fff;display:inline-block;padding:16px;border-radius:16px;color:#000"><div id="admQR" style="line-height:0"></div><div style="font-family:Cinzel,serif;font-weight:900;margin-top:10px">Scan • Order • Enjoy</div><div style="font-size:12px">Hotel Jagdamba Family Restaurant & Dhaba</div></div>
  <input class="inp no" id="admT" placeholder="टेबल नंबर (optional)" style="margin-top:14px">
  <button class="go no" id="admMk">QR बनाएँ</button>
  <button class="go alt no" onclick="print()">Print / Save PDF</button>
</div></div>
<div class="toast" id="toast"></div>

<script>
/* ===== SETTINGS ===== */
const SHEET="https://docs.google.com/spreadsheets/d/1oHvoI-9h5rkgcrmlrSXAIO05UxIRBHwhDT2bMtUSMKo/export?format=csv";
const WA_NO="918700176034";
const CALL_NO="8700176034";
const UPI_ID="Q334332463@ybl";
const UPI_NAME="Hotel Jagdamba";
const GST_PCT=0, DELIVERY_FEE=0, FREE_DELIVERY_ABOVE=0;

const $=id=>document.getElementById(id);
const esc=s=>String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const PH="data:image/svg+xml;utf8,"+encodeURIComponent('<svg xmlns="http://www.w3.org/2000/svg" width="84" height="84"><rect width="84" height="84" fill="#111"/><text x="42" y="54" font-size="32" text-anchor="middle">🍛</text></svg>');
let items=[],cart={},cat="All",type="all",mode="Dining",pay="UPI",order=null;
const P=new URLSearchParams(location.search);

function parseCSV(t){const R=[];let r=[],c="",q=false;for(let i=0;i<t.length;i++){const h=t[i];if(q){if(h=='"'){if(t[i+1]=='"'){c+='"';i++}else q=false}else c+=h}else if(h=='"')q=true;else if(h==','){r.push(c);c=""}else if(h=='\n'||h=='\r'){if(h=='\r'&&t[i+1]=='\n')i++;r.push(c);R.push(r);r=[];c=""}else c+=h}if(c||r.length){r.push(c);R.push(r)}return R}
function build(t){return parseCSV(t).slice(1).filter(r=>r[0]&&r[0].trim()).map((c,i)=>({id:i,name:c[0].trim(),price:parseInt(c[1])||0,cat:(c[2]||"Menu").trim(),nv:/non/i.test(c[3]||""),desc:(c[4]||"").trim(),img:(c[5]||"").trim(),sold:/^\s*(no|n|sold|sold out|out|unavailable|0|false)\s*$/i.test(c[6]||"")}))}
async function load(){
  try{const r=await fetch(SHEET+"&t="+Date.now());if(!r.ok)throw 0;const t=await r.text();items=build(t);try{localStorage.setItem("jd_menu",t)}catch(e){}}
  catch(e){try{const t=localStorage.getItem("jd_menu");if(t){items=build(t);toast("ऑफ़लाइन — पिछला मेन्यू")}}catch(_){}}
  try{const s=JSON.parse(localStorage.getItem("jd_cart")||"{}");for(const k in s)if(items[k]&&!items[k].sold)cart[k]=s[k]}catch(e){}
  cats();render();sync();
}
function cats(){$("cats").innerHTML=["All",...new Set(items.map(i=>i.cat))].map(c=>`<button class="chip ${c===cat?"on":""}" data-c="${esc(c)}">${c==="All"?"सब कुछ":esc(c)}</button>`).join("")}
function render(){
  const q=$("q").value.trim().toLowerCase();
  const L=items.filter(i=>(cat==="All"||i.cat===cat)&&(type==="all"||(type==="nv")===i.nv)&&(!q||(i.name+" "+i.desc).toLowerCase().includes(q)));
  if(!L.length){$("menu").innerHTML='<div class="empty">🍽️<br>कोई डिश नहीं मिली।</div>';return}
  let h="",last="";
  L.forEach(i=>{
    if(cat==="All"&&i.cat!==last){h+=`<div class="sec">${esc(i.cat)}</div>`;last=i.cat}
    const n=cart[i.id]||0;
    h+=`<article class="item ${i.sold?"sold":""}"><img loading="lazy" src="${esc(i.img)||PH}" alt="${esc(i.name)}" onerror="this.onerror=null;this.src='${PH}'"><div class="inf"><div class="name"><span class="vd ${i.nv?"n":""}"><i></i></span>${esc(i.name)}</div><div class="desc">${esc(i.desc)}</div><div class="row"><span class="price">₹${i.price}</span>${i.sold?'<span class="soldtag">Sold out</span>':n?`<div class="qty"><button data-q="${i.id}" data-d="-1" aria-label="कम">−</button><span>${n}</span><button data-q="${i.id}" data-d="1" aria-label="ज़्यादा">+</button></div>`:`<button class="add" data-q="${i.id}" data-d="1">ADD</button>`}</div></div></article>`;
  });
  $("menu").innerHTML=h;
}
function sub(){let t=0,c=0;for(const k in cart){if(!items[k]||items[k].sold){delete cart[k];continue}t+=cart[k]*items[k].price;c+=cart[k]}return{t,c}}
function bill(){const{t}=sub();const gst=Math.round(t*GST_PCT/100);const del=(mode==="Delivery"&&t>0&&DELIVERY_FEE&&!(FREE_DELIVERY_ABOVE&&t>=FREE_DELIVERY_ABOVE))?DELIVERY_FEE:0;return{sub:t,gst,del,grand:t+gst+del}}
function sync(){const{t,c}=sub();$("bar").style.display=c?"flex":"none";$("bc").textContent=c+" आइटम";$("bt").textContent="₹"+t;$("sub").textContent="₹"+t;try{localStorage.setItem("jd_cart",JSON.stringify(cart))}catch(e){}}
function change(id,d){cart[id]=(cart[id]||0)+d;if(cart[id]<=0)delete cart[id];render();sync();if($("cartOv").classList.contains("open"))lines()}
function lines(){const k=Object.keys(cart);if(!k.length){$("cartOv").classList.remove("open");return}$("lines").innerHTML=k.map(i=>`<div class="ln"><span>${esc(items[i].name)}</span><span class="c">₹${items[i].price*cart[i]} <button data-q="${i}" data-d="-1">−</button> ${cart[i]} <button data-q="${i}" data-d="1">+</button></span></div>`).join("");sync()}
function setMode(m){mode=m;document.querySelectorAll("#modeSeg button").forEach(b=>b.classList.toggle("on",b.dataset.m===m));$("info").placeholder=m==="Dining"?"टेबल नंबर":"पूरा पता (Address)"}

function makeBill(){
  const name=$("nm").value.trim(),info=$("info").value.trim(),ph=$("ph").value.trim();
  if(!name||!info){$("err").textContent="कृपया नाम और "+(mode==="Dining"?"टेबल नंबर":"पता")+" भरें।";return}
  if(mode==="Delivery"&&ph.replace(/\D/g,"").length<10){$("err").textContent="सही मोबाइल नंबर डालें।";return}
  $("err").textContent="";
  const d=new Date();
  order={id:"JD"+String(d.getTime()).slice(-6),name,info,ph,mode,date:d.toLocaleDateString("en-IN")};
  $("bph").textContent="📞 "+CALL_NO;
  $("meta").innerHTML=`<div><span>ऑर्डर नं.</span><b>${order.id}</b></div><div><span>तारीख</span><b>${order.date}</b></div><div><span>ग्राहक</span><b>${esc(name)}</b></div><div><span>${mode==="Dining"?"टेबल":"प्रकार"}</span><b>${mode==="Dining"?esc(info):"Delivery"}</b></div>${mode==="Delivery"?`<div style="grid-column:1/-1"><span>पता</span><b>${esc(info)}</b></div>`:""}`;
  $("bbody").innerHTML=Object.keys(cart).map(k=>{const i=items[k];return`<tr><td><span class="dt" style="background:${i.nv?"#ff3b3b":"#00c853"}"></span>${esc(i.name)}</td><td>${cart[k]}</td><td>₹${i.price}</td><td>₹${i.price*cart[k]}</td></tr>`}).join("");
  const B=bill();
  $("bsums").innerHTML=`<div class="sm"><span>सब-टोटल</span><span>₹${B.sub}</span></div>`+(GST_PCT?`<div class="sm"><span>GST (${GST_PCT}%)</span><span>₹${B.gst}</span></div>`:"")+(B.del?`<div class="sm"><span>Delivery</span><span>₹${B.del}</span></div>`:"");
  $("bgt").textContent="₹"+B.grand;
  $("cartOv").classList.remove("open");$("billOv").classList.add("open");$("billOv").scrollTop=0;
  setPay(pay);
}
function upiLink(){return`upi://pay?pa=${encodeURIComponent(UPI_ID)}&pn=${encodeURIComponent(UPI_NAME)}&am=${bill().grand}&cu=INR&tn=${encodeURIComponent("Order "+order.id)}`}
function setPay(p){
  pay=p;document.querySelectorAll("#paySeg button").forEach(b=>b.classList.toggle("on",b.dataset.p===p));
  const u=p==="UPI";
  $("psT").textContent=u?"💳 UPI पेमेंट":"💵 होटल में पेमेंट";
  $("psS").textContent=u?"पे करने के बाद स्क्रीनशॉट WhatsApp पर भेजें। काउंटर पर पेमेंट वेरीफाई होगा।":"खाने के बाद काउंटर पर पेमेंट करें।";
  $("qrw").style.display=u?"flex":"none";$("upiApp").style.display=u?"block":"none";
  if(u){$("qrimg").innerHTML="";new QRCode($("qrimg"),{text:upiLink(),width:130,height:130,correctLevel:QRCode.CorrectLevel.M});$("upiApp").href=upiLink()}
}
function sendWA(){
  const B=bill();let L="";for(const k in cart){const i=items[k];L+=`${i.nv?"🔴":"🟢"} *${i.name}* (x${cart[k]}) - ₹${i.price*cart[k]}\n`}
  const m=`🍽️ *नया डिजिटल ऑर्डर*\n━━━━━━━━━━━━━━\n🏨 *Hotel Jagdamba Family Restaurant & Dhaba*\n🧾 *ऑर्डर नं.:* ${order.id}\n\n👤 *नाम:* ${order.name}\n🍴 *प्रकार:* ${order.mode}\n📍 *${order.mode==="Dining"?"टेबल नं.":"पता"}:* ${order.info}\n${order.mode==="Delivery"?`📞 *मोबाइल:* ${order.ph}\n`:""}\n📋 *ऑर्डर:*\n${L}\n${GST_PCT?`GST: ₹${B.gst}\n`:""}${B.del?`Delivery: ₹${B.del}\n`:""}💵 *कुल बिल: ₹${B.grand}*\n💳 *पेमेंट:* ${pay==="UPI"?"UPI — स्क्रीनशॉट भेजेंगे":"होटल में"}\n━━━━━━━━━━━━━━\n🙏 *धन्यवाद!*`;
  window.open("https://wa.me/"+WA_NO+"?text="+encodeURIComponent(m),"_blank");
  cart={};sync();render();toast("ऑर्डर भेज दिया गया ✔");
}
async function dlPdf(){
  const b=$("dlPdf");b.textContent="बन रहा है…";
  try{
    const cv=await html2canvas($("bill"),{backgroundColor:"#000",scale:2});
    const {jsPDF}=window.jspdf;const w=190,h=cv.height*w/cv.width,H=Math.max(297,h+20);
    const pdf=new jsPDF({unit:"mm",format:[210,H]});
    pdf.setFillColor(0,0,0);pdf.rect(0,0,210,H,"F");
    pdf.addImage(cv.toDataURL("image/jpeg",.95),"JPEG",10,10,w,h);
    pdf.save("Jagdamba-Bill-"+order.id+".pdf");
  }catch(e){toast("PDF नहीं बन पाया — स्क्रीनशॉट ले लें")}
  b.textContent="बिल PDF डाउनलोड करें";
}
function toast(m){const t=$("toast");t.textContent=m;t.style.display="block";setTimeout(()=>t.style.display="none",2600)}
function admQR(){const b=location.origin+location.pathname,t=$("admT").value.trim();$("admQR").innerHTML="";new QRCode($("admQR"),{text:t?b+"?table="+encodeURIComponent(t):b,width:230,height:230,correctLevel:QRCode.CorrectLevel.H})}

$("q").oninput=render;
document.querySelector(".types").onclick=e=>{const b=e.target.closest(".tb");if(!b)return;type=b.dataset.t;document.querySelectorAll(".tb").forEach(x=>x.classList.toggle("on",x===b));render()};
$("cats").onclick=e=>{const b=e.target.closest(".chip");if(!b)return;cat=b.dataset.c;cats();render()};
document.addEventListener("click",e=>{const b=e.target.closest("[data-q]");if(b)change(+b.dataset.q,+b.dataset.d)});
$("bar").onclick=()=>{lines();$("cartOv").classList.add("open")};
$("closeCart").onclick=()=>$("cartOv").classList.remove("open");
$("modeSeg").onclick=e=>{const b=e.target.closest("button");if(b)setMode(b.dataset.m)};
$("mkBill").onclick=makeBill;
$("paySeg").onclick=e=>{const b=e.target.closest("button");if(b)setPay(b.dataset.p)};
$("sendWA").onclick=sendWA;$("dlPdf").onclick=dlPdf;
$("editOrder").onclick=()=>{$("billOv").classList.remove("open");lines();$("cartOv").classList.add("open")};
$("admMk").onclick=admQR;
$("callBtn").href="tel:"+CALL_NO;
if(P.get("table")){$("tbl").style.display="block";$("tbl").textContent="टेबल नं. "+P.get("table");$("info").value=P.get("table")}
if(P.has("admin")){$("qrOv").classList.add("open");admQR()}
load();
</script>
</body>
</html>
