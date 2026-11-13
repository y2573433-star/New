
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#080808">
<title>AL SOBKY | السبكي للعطور</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800;900&display=swap');

:root {
 --gold:#d6b36a;
 --black:#080808;
 --white:#f8f4e9;
}

*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{
 background:var(--black);
 color:var(--white);
 font-family:'Cairo',sans-serif;
 overflow-x:hidden;
}
button{font-family:inherit;cursor:pointer}
header{
 height:75px;
 padding:0 7%;
 display:flex;
 align-items:center;
 justify-content:space-between;
 border-bottom:1px solid #ffffff17;
 position:sticky;top:0;z-index:10;
 background:#080808ed;
 backdrop-filter:blur(15px);
}
.logo{font-size:23px;font-weight:900;color:var(--gold)}
.logo span{display:block;font-size:10px;letter-spacing:4px;text-align:center}
nav{display:flex;gap:25px}
nav a{color:#ddd;text-decoration:none;font-size:13px}
nav a:hover{color:var(--gold)}
.cart-btn{
 background:transparent;color:var(--gold);
 border:1px solid var(--gold);padding:9px 15px;
 border-radius:30px;
}
.hero{
 min-height:620px;
 display:flex;align-items:center;
 justify-content:space-around;
 padding:65px 8%;
 background:
 radial-gradient(ellipse at 75% 48%,#b38b3b25,transparent 40%),
 linear-gradient(120deg,#080808,#15120c,#080808);
 position:relative;overflow:hidden;
}
.hero-text{max-width:470px;z-index:2}
.small-title{color:var(--gold);letter-spacing:4px;font-size:12px}
.hero h1{font-size:clamp(38px,6vw,70px);line-height:1.35;margin:15px 0}
.hero h1 span{color:var(--gold)}
.hero p{color:#aaa;line-height:2;font-size:15px}
.main-btn{
 display:inline-block;margin-top:28px;
 background:linear-gradient(120deg,#b58a38,#f0d58c);
 color:#15100a;text-decoration:none;
 padding:13px 30px;border-radius:30px;font-weight:900;
 border:none;
}
.stage{
 width:300px;height:400px;
 display:flex;align-items:center;justify-content:center;
 perspective:900px;position:relative;
}
.glow{
 position:absolute;width:230px;height:230px;
 background:#d7a94145;filter:blur(65px);
 border-radius:50%;
 animation:pulse 3s infinite alternate;
}
@keyframes pulse{to{opacity:.3;transform:scale(.7)}}
.bottle{
 width:145px;height:230px;
 position:relative;z-index:1;
 border-radius:27px 27px 20px 20px;
 background:linear-gradient(100deg,#5b3d12,#e2bd62 25%,#9d7026 50%,#f4d88e 75%,#62451c);
 box-shadow:inset 8px 0 15px #fff5,inset -8px 0 20px #0009,
 0 25px 60px #d2a64b44;
 transform:rotateY(-15deg) rotateX(5deg);
 animation:float 4s ease-in-out infinite;
}
.bottle:before{
 content:"";position:absolute;top:-35px;left:49px;
 width:47px;height:38px;border-radius:5px 5px 2px 2px;
 background:linear-gradient(90deg,#777,#eee,#555);
 box-shadow:0 5px 12px #000;
}
.bottle:after{
 content:"";position:absolute;top:85px;left:0;
 width:100%;height:65px;
 background:#0b0b0b;opacity:.9;
}
.bottle-label{
 position:absolute;z-index:2;top:92px;width:100%;
 text-align:center;color:var(--gold);font-size:16px;
 font-weight:900;letter-spacing:2px;
}
@keyframes float{
 50%{transform:translateY(-15px) rotateY(12deg) rotateX(5deg)}
}
.section{padding:85px 7%;text-align:center}
.section-title{font-size:32px;margin-bottom:10px}
.section-title span{color:var(--gold)}
.subtitle{color:#888;font-size:13px;margin-bottom:45px}
.products{
 display:grid;
 grid-template-columns:repeat(auto-fit,minmax(210px,1fr));
 gap:25px;
}
.product{
 background:linear-gradient(145deg,#171717,#0c0c0c);
 border:1px solid #ffffff12;
 border-radius:17px;padding:25px 17px;
 transition:.4s;position:relative;overflow:hidden;
}
.product:hover{transform:translateY(-9px);border-color:#c6a35b66}
.mini-stage{
 height:200px;display:flex;align-items:center;
 justify-content:center;perspective:700px;
 position:relative;cursor:pointer;
}
.mini-light{
 position:absolute;width:130px;height:130px;
 background:var(--light);filter:blur(55px);
 opacity:0;transition:.5s;border-radius:50%;
}
.product.active .mini-light{opacity:.8}
.mini-bottle{
 width:85px;height:140px;
 border-radius:16px 16px 12px 12px;
 background:linear-gradient(100deg,#111,#242424,#090909);
 border:1px solid #ffffff30;
 position:relative;transition:.5s;
 box-shadow:inset 5px 0 12px #fff1,0 15px 30px #000;
 transform:rotateY(-12deg);
}
.mini-bottle:before{
 content:"";position:absolute;top:-24px;left:29px;
 width:27px;height:25px;background:linear-gradient(90deg,#555,#bbb,#555);
 border-radius:4px 4px 0 0;
}
.mini-bottle:after{
 content:"";position:absolute;top:52px;width:100%;height:40px;
 background:#070707;
}
.product.active .mini-bottle{
 background:linear-gradient(100deg,var(--light),#fff,var(--light));
 box-shadow:0 0 35px var(--light),inset 5px 0 12px #fff;
 transform:rotateY(12deg) scale(1.06);
}
.bottle-name{
 position:absolute;top:64px;width:100%;text-align:center;
 color:var(--gold);font-size:9px;z-index:2;
}
.product h3{font-size:18px;margin:12px 0 4px}
.product p{color:#888;font-size:12px}
.price{color:var(--gold);font-size:20px;font-weight:900;margin:13px}
.add-btn{
 width:100%;padding:11px;border:1px solid var(--gold);
 background:transparent;color:var(--gold);
 border-radius:8px;transition:.3s;
}
.add-btn:hover{background:var(--gold);color:#000}
.hint{color:#b89a59;font-size:11px;margin-top:8px}
.features{
 display:grid;grid-template-columns:repeat(3,1fr);
 gap:20px;margin-top:25px;
}
.feature{
 padding:25px 10px;border:1px solid #ffffff16;
 border-radius:12px;background:#111;
}
.feature b{color:var(--gold);font-size:22px}
.feature p{font-size:12px;color:#aaa;margin-top:8px}
footer{
 text-align:center;padding:40px 15px;
 border-top:1px solid #ffffff17;color:#888;
 font-size:12px;line-height:2.5;
}
.cart-panel{
 position:fixed;inset:0;z-index:30;
 background:#000a;display:none;justify-content:flex-end;
}
.cart-panel.show{display:flex}
.cart-content{
 width:min(400px,90%);height:100%;
 background:#111;padding:25px;overflow-y:auto;
 border-left:1px solid var(--gold);
}
.cart-head{display:flex;justify-content:space-between;
 align-items:center;margin-bottom:25px}
.cart-head h2{color:var(--gold)}
.close{background:none;color:white;border:0;font-size:28px}
.cart-item{
 display:flex;justify-content:space-between;gap:10px;
 border-bottom:1px solid #ffffff20;padding:15px 0;
 font-size:13px;
}
.cart-item button{background:none;color:#e66;border:0}
.total{font-size:20px;color:var(--gold);margin:25px 0}
.checkout{
 width:100%;background:#c8a451;color:#080808;
 border:0;padding:14px;border-radius:9px;font-weight:900;
}
.empty{color:#888;text-align:center;padding:35px 0}
@media(max-width:650px){
 header{padding:0 4%;height:65px}
 nav{gap:10px}nav a{font-size:10px}
 .logo{font-size:18px}
 .cart-btn{font-size:11px;padding:7px 10px}
 .hero{min-height:700px;flex-direction:column-reverse;
 text-align:center;padding:35px 5%}
 .stage{height:330px}
 .hero-text{margin-top:15px}
 .section{padding:65px 5%}
 .section-title{font-size:25px}
 .products{grid-template-columns:repeat(2,minmax(0,1fr));gap:12px}
 .product{padding:15px 9px}
 .mini-stage{height:160px}
 .mini-bottle{transform:scale(.85)}
 .product h3{font-size:15px}
 .features{grid-template-columns:1fr}
}
</style>
</head>

<body>

<header>
 <div class="logo">السبكي <span>AL SOBKY</span></div>
 <nav>
  <a href="#home">الرئيسية</a>
  <a href="#shop">العطور</a>
  <a href="#about">عن المتجر</a>
 </nav>
 <button class="cart-btn" onclick="openCart()">🛒 <span id="count">0</span></button>
</header>

<section class="hero" id="home">
 <div class="hero-text">
  <div class="small-title">LUXURY PERFUMES COLLECTION</div>
  <h1>عطرك...<br><span>هو هويتك</span></h1>
  <p>اكتشف عالم السبكي للعطور، حيث الفخامة تلتقي مع الأناقة، وكل رائحة لها حكاية.</p>
  <a class="main-btn" href="#shop">اكتشف مجموعتنا</a>
 </div>
 <div class="stage">
  <div class="glow"></div>
  <div class="bottle">
   <div class="bottle-label">AL SOBKY</div>
  </div>
 </div>
</section>

<section class="section" id="shop">
 <h2 class="section-title">مجموعة <span>العطور</span></h2>
 <p class="subtitle">اضغط على أي زجاجة لتكتشف نورها وفخامتها ✨</p>

 <div class="products" id="products"></div>
</section>

<section class="section" id="about">
 <h2 class="section-title">لماذا <span>السبكي؟</span></h2>
 <p class="subtitle">الفخامة في كل تفصيلة</p>
 <div class="features">
  <div class="feature">
   <b>✦</b><p>اختيارات عطور مميزة</p>
  </div>
  <div class="feature">
   <b>♛</b><p>تصميم وهوية فاخرة</p>
  </div>
  <div class="feature">
   <b>♡</b><p>تجربة تسوق سهلة</p>
  </div>
 </div>
</section>

<footer>
 <div class="logo">AL SOBKY</div>
 <p>السبكي للعطور - الفخامة تبدأ من هنا</p>
 <p>جميع الحقوق محفوظة © 2026</p>
</footer>

<div class="cart-panel" id="cartPanel" onclick="outsideClose(event)">
 <div class="cart-content">
  <div class="cart-head">
   <h2>🛒 سلة التسوق</h2>
   <button class="close" onclick="closeCart()">×</button>
  </div>
  <div id="cartItems"></div>
  <div class="total">الإجمالي: <span id="total">0</span> جنيه</div>
  <button class="checkout" onclick="checkout()">اطلب عبر واتساب</button>
 </div>
</div>

<script>
// عدّل أسماء العطور والأسعار من هنا
const perfumes = [
 {id:1,name:"ROYAL GOLD",desc:"عطر ملكي فاخر",price:450,light:"#e9b944"},
 {id:2,name:"BLACK OUD",desc:"رائحة شرقية مميزة",price:550,light:"#b78bff"},
 {id:3,name:"BLUE NIGHT",desc:"أناقة وانتعاش",price:380,light:"#36baff"},
 {id:4,name:"GOLDEN ELIXIR",desc:"لمسة من الفخامة",price:600,light:"#f6d36b"},
 {id:5,name:"DARK LEGEND",desc:"حضور لا يُنسى",price:500,light:"#ff5d77"},
 {id:6,name:"SILVER MIST",desc:"رائحة عصرية",price:420,light:"#a9d9e8"}
];

let cart = [];

function showProducts(){
 const box=document.getElementById("products");
 box.innerHTML=perfumes.map(p=>`
 <div class="product" id="p${p.id}" style="--light:${p.light}">
  <div class="mini-stage" onclick="lightBottle(${p.id})">
   <div class="mini-light"></div>
   <div class="mini-bottle">
    <div class="bottle-name">${p.name}</div>
   </div>
  </div>
  <h3>${p.name}</h3>
  <p>${p.desc}</p>
  <div class="price">${p.price} جنيه</div>
  <button class="add-btn" onclick="addToCart(${p.id})">+ أضف للسلة</button>
  <div class="hint">اضغط على الزجاجة لتضيء ✨</div>
 </div>`).join("");
}

function lightBottle(id){
 const card=document.getElementById("p"+id);
 card.classList.toggle("active");
}

function addToCart(id){
 const p=perfumes.find(x=>x.id===id);
 const item=cart.find(x=>x.id===id);
 if(item)item.qty++;
 else cart.push({...p,qty:1});
 updateCart();
}

function updateCart(){
 document.getElementById("count").textContent=
 cart.reduce((s,p)=>s+p.qty,0);

 document.getElementById("cartItems").innerHTML=
 cart.length ? cart.map(p=>`
 <div class="cart-item">
  <div>${p.name}<br>${p.price} جنيه × ${p.qty}</div>
  <div>
   <b>${p.price*p.qty} ج</b><br>
   <button onclick="removeItem(${p.id})">حذف</button>
  </div>
 </div>`).join("") :
 '<div class="empty">السلة فارغة حالياً 🛒</div>';

 document.getElementById("total").textContent=
 cart.reduce((s,p)=>s+p.price*p.qty,0);
}

function removeItem(id){
 cart=cart.filter(p=>p.id!==id);
 updateCart();
}

function openCart(){
 document.getElementById("cartPanel").classList.add("show");
}
function closeCart(){
 document.getElementById("cartPanel").classList.remove("show");
}
function outsideClose(e){
 if(e.target.id==="cartPanel")closeCart();
}

function checkout(){
 if(!cart.length){
  alert("أضف عطوراً إلى السلة أولاً");
  return;
 }

 // ضع رقم واتساب المتجر هنا بصيغة دولية بدون +
 const phone="201000000000";

 let message="مرحباً، أريد طلب العطور التالية من السبكي:\n\n";
 cart.forEach(p=>{
  message+=p.name+" - الكمية: "+p.qty+
  " - السعر: "+(p.price*p.qty)+" جنيه\n";
 });
 message+="\nالإجمالي: "+
 cart.reduce((s,p)=>s+p.price*p.qty,0)+" جنيه";

 window.open("https://wa.me/"+phone+
 "?text="+encodeURIComponent(message),"_blank");
}

showProducts();
updateCart();
</script>

</body>
</html>
