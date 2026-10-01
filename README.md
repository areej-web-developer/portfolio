<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Loom & Line | Clothing Store</title>
<meta name="description" content="Everyday clothing for men, women and kids. Free exchange within 7 days.">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 40 40'%3E%3Crect width='40' height='40' rx='9' fill='%231d2547'/%3E%3Cpath d='M20 20v-2c0-1.4 3-2 3-4.5a3 3 0 1 0-6 0M20 20 8 28h24z' fill='none' stroke='white' stroke-width='2' stroke-linejoin='round'/%3E%3Cpath d='M11 33h18' stroke='%23b3342f' stroke-width='2.5' stroke-linecap='round'/%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@500;700;800&family=DM+Sans:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{--ink:#1d2547;--paper:#f6f4f1;--line:#e0dcd6;--madder:#b3342f;--muted:#5f6478;--card:#fff;--sand:#ecdfd0;--sky:#dbe3f3;--rose:#f1d6d3}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth}
body{font-family:"DM Sans",system-ui,sans-serif;color:var(--ink);background:var(--paper);line-height:1.6}
h1,h2,h3,.logo{font-family:"Bricolage Grotesque",system-ui,sans-serif;line-height:1.1}
a{color:inherit}
:focus-visible{outline:3px solid var(--madder);outline-offset:2px}
.sr{position:absolute;left:-9999px}
.promo{background:var(--ink);color:#fff;text-align:center;padding:8px 5vw;font-size:.9rem}
.site-header{position:sticky;top:0;z-index:10;display:flex;align-items:center;gap:24px;padding:12px 5vw;background:rgba(246,244,241,.94);backdrop-filter:blur(8px);border-bottom:1px solid var(--line)}
.logo{display:flex;align-items:center;gap:10px;font-weight:800;font-size:1.4rem;text-decoration:none;margin-right:auto}
.site-header nav{display:flex;gap:22px}
.site-header nav a{text-decoration:none;color:var(--muted);font-weight:500}
.site-header nav a:hover{color:var(--madder)}
.cart-btn,.btn,.chip{font:inherit;cursor:pointer}
.cart-btn{border:0;background:var(--ink);color:#fff;padding:9px 16px;border-radius:999px}
.btn{display:inline-block;background:var(--ink);color:#fff;border:0;padding:13px 26px;border-radius:999px;text-decoration:none;font-weight:500;transition:background .2s}
.btn:hover{background:var(--madder)}
.btn.light{background:transparent;color:var(--ink);border:1.5px solid var(--ink)}
.btn.light:hover{background:var(--ink);color:#fff}
.hero{display:grid;grid-template-columns:1.1fr .9fr;gap:40px;align-items:center;padding:7vh 5vw 8vh;background:linear-gradient(120deg,var(--sand) 0%,var(--paper) 70%)}
.hero h1{font-size:clamp(2.6rem,6.5vw,5.4rem);font-weight:800;letter-spacing:-.03em;margin-bottom:20px}
.hero p{max-width:46ch;color:var(--muted);font-size:1.15rem;margin-bottom:28px}
.hero .btns{display:flex;gap:12px;flex-wrap:wrap}
.collage{position:relative;height:min(460px,60vw) }
.arch{position:absolute;border-radius:200px 200px 16px 16px;display:grid;place-items:center}
.arch svg{width:62%  }
.a1{left:0;top:8%;width:52%;height:84%;background:var(--ink);color:var(--sky)}
.a2{right:0;top:0;width:44%;height:56%;background:var(--madder);color:var(--rose)}
.a3{right:6%;bottom:0;width:38%;height:38%;background:#c28a2c;color:#fbeed2;border-radius:200px 200px 12px 12px}
.trust{display:flex;justify-content:space-around;flex-wrap:wrap;gap:12px;padding:18px 5vw;background:var(--ink);color:#fff;font-weight:500;font-size:.95rem}
.section{padding:72px 5vw}
.section h2{font-size:2.2rem;font-weight:800;letter-spacing:-.02em;margin-bottom:8px}
.sub{color:var(--muted);margin-bottom:28px}
.cats{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.cat{border:0;border-radius:16px;padding:28px;min-height:190px;display:flex;flex-direction:column;justify-content:flex-end;text-align:left;font:inherit;cursor:pointer;color:var(--ink);transition:transform .2s}
.cat:hover{transform:translateY(-4px)}
.cat h3{font-size:1.7rem}
.cat span{font-size:.95rem;color:var(--muted)}
.filters{display:flex;flex-wrap:wrap;gap:10px;margin-bottom:28px;align-items:center}
.chip{border:1px solid var(--line);background:var(--card);padding:8px 18px;border-radius:999px;color:var(--ink)}
.chip.active{background:var(--ink);color:#fff;border-color:var(--ink)}
.search{margin-left:auto}
input,textarea{font:inherit;width:100%;padding:11px 14px;border:1px solid var(--line);border-radius:10px;background:var(--card)}
.search input{width:240px;border-radius:999px}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(235px,1fr));gap:26px}
.card{background:var(--card);border-radius:16px;overflow:hidden;display:flex;flex-direction:column;transition:box-shadow .2s,transform .2s}
.card:hover{box-shadow:0 14px 34px rgba(29,37,71,.14);transform:translateY(-3px)}
.pic{position:relative;aspect-ratio:4/5;display:grid;place-items:center}
.pic svg{width:58%;filter:drop-shadow(0 8px 10px rgba(0,0,0,.18))} 
.badge{position:absolute;top:12px;left:12px;background:var(--madder);color:#fff;font-size:.78rem;font-weight:500;padding:3px 10px;border-radius:999px}
.badge.new{background:var(--ink)}
.info{padding:16px;display:flex;flex-direction:column;gap:8px}
.info h3{font-size:1.05rem}
.price{font-weight:700}
.price s{color:var(--muted);font-weight:400;margin-left:6px}
.row{display:flex;gap:8px}
.row select{flex:1;padding:9px;border:1px solid var(--line);border-radius:999px;font:inherit;background:#fff}
.row .btn{padding:9px 20px}
.empty{color:var(--muted)}
.about{display:grid;grid-template-columns:1fr 1fr;gap:48px;background:var(--sky)}
.about p{max-width:55ch;margin-bottom:20px}
.facts{list-style:none;padding:0;align-self:center}
.facts li{padding:16px 0;border-bottom:1px solid rgba(29,37,71,.2);font-weight:500;font-size:1.1rem}
.reviews{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.review{background:var(--card);border-radius:16px;padding:24px}
.review p{margin-bottom:14px}
.stars{color:#c28a2c;letter-spacing:2px}
.news{background:var(--madder);color:#fff;text-align:center}
.news p{margin:0 auto 20px;max-width:46ch}
.news form{display:flex;gap:10px;justify-content:center;flex-wrap:wrap}
.news input{max-width:320px;border:0;border-radius:999px}
.news .btn{background:var(--ink)}
details{border-bottom:1px solid var(--line);padding:14px 0;max-width:720px}
summary{cursor:pointer;font-weight:500}
details p{margin-top:8px;color:var(--muted)}
.contact{display:grid;grid-template-columns:1fr 1fr;gap:48px}
.contact p{max-width:50ch;margin-bottom:20px}
form{display:grid;gap:14px}
form label{display:grid;gap:4px;font-weight:500}
.formMsg{min-height:1.5em;font-weight:500}
.site-footer{display:flex;justify-content:space-between;flex-wrap:wrap;gap:12px;padding:28px 5vw;background:var(--ink);color:#c9cde0}
.drawer{position:fixed;top:0;right:0;width:min(400px,100%);height:100%;background:var(--card);box-shadow:-8px 0 30px rgba(0,0,0,.18);padding:22px;display:flex;flex-direction:column;gap:14px;z-index:20}
.drawer[hidden]{display:none}
.drawer-head{display:flex;justify-content:space-between;align-items:center}
.drawer-head button{background:none;border:0;font:inherit;cursor:pointer;text-decoration:underline}
#cartItems{list-style:none;padding:0;flex:1;overflow:auto}
#cartItems li{display:flex;justify-content:space-between;gap:10px;padding:12px 0;border-bottom:1px solid var(--line)}
#cartItems button{border:1px solid var(--line);background:none;border-radius:50%;cursor:pointer;width:28px;height:28px}
@media(max-width:820px){.site-header nav{display:none}.hero,.about,.contact{grid-template-columns:1fr}.cats,.reviews{grid-template-columns:1fr}.search{margin-left:0;width:100%}.search input{width:100%}.collage{height:320px}}
@media(prefers-reduced-motion:reduce){html{scroll-behavior:auto}*{transition:none!important}}
</style>
</head>
<body>
<div class="promo">Free exchange within 7 days. Cash on delivery available.</div>
<header class="site-header">
  <a class="logo" href="#top" aria-label="Loom & Line home"><svg viewBox="0 0 40 40" width="38" height="38" aria-hidden="true"><rect width="40" height="40" rx="9" fill="#1d2547"/><path d="M20 20v-2c0-1.4 3-2 3-4.5a3 3 0 1 0-6 0" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"/><path d="M20 20 8 28h24z" fill="none" stroke="#fff" stroke-width="2" stroke-linejoin="round"/><path d="M11 33h18" stroke="#b3342f" stroke-width="2.5" stroke-linecap="round"/></svg><span>Loom & Line</span></a>
  <nav aria-label="Main"><a href="#shop">Shop</a><a href="#about">About</a><a href="#reviews">Reviews</a><a href="#policies">Shipping</a><a href="#contact">Contact</a></nav>
  <button class="cart-btn" id="openCart" aria-label="Open cart">Cart (<span id="cartCount">0</span>)</button>
</header>

<main id="top">
  <section class="hero">
    <div>
      <h1>Clothes cut for how you actually live.</h1>
      <p>Cotton, linen and denim basics for men, women and kids. Soft fabrics, honest prices, delivered to your door.</p>
      <div class="btns"><a class="btn" href="#shop">Shop new arrivals</a><a class="btn light" href="#contact">Ask about sizing</a></div>
    </div>
    <div class="collage" aria-hidden="true">
      <div class="arch a1"><img src="areej.avif" alt="Blue linen shirt" width="200" ></svg></div>
      <div class="arch a2"><svg viewBox="0 0 100 100"><path fill="currentColor" d="M38 8H46Q50 14 54 8H62L66 30 60 36 78 92H22L40 36 34 30Z"/></svg></div>
      <div class="arch a3"><svg viewBox="0 0 100 100"><path fill="currentColor" d="M30 10H70L74 92H54L50 40 46 92H26Z"/></svg></div>
    </div>
  </section>

  <div class="trust"><span>Free exchange</span><span>Cash on delivery</span><span>Ships in 1-2 days</span><span>Hand-checked quality</span></div>

  <section class="section">
    <h2>Shop by who it's for</h2>
    <p class="sub">Pick a category to jump straight to the products.</p>
    <div class="cats">
      <button class="cat" data-jump="men" style="background:var(--sky)"><h3>Men</h3><span>Shirts, denim and kurtas</span></button>
      <button class="cat" data-jump="women" style="background:var(--rose)"><h3>Women</h3><span>Dresses, suits and tees</span></button>
      <button class="cat" data-jump="kids" style="background:var(--sand)"><h3>Kids</h3><span>Hoodies and shorts, sizes 2-12</span></button>
    </div>
  </section>

  <section id="shop" class="section" style="padding-top:0">
    <h2>Shop</h2>
    <div class="filters" role="group" aria-label="Filter by category">
      <button class="chip active" data-cat="all">All</button><button class="chip" data-cat="men">Men</button><button class="chip" data-cat="women">Women</button><button class="chip" data-cat="kids">Kids</button>
      <label class="search"><span class="sr">Search products</span><input id="search" type="search" placeholder="Search products"></label>
    </div>
    <div class="grid" id="grid"></div>
    <p id="empty" class="empty" hidden>No products match. Clear the search or pick another category.</p>
  </section>

  <section id="about" class="section about">
    <div><h2>About us</h2><p>We are a family-run clothing store. Every piece is checked by hand before it ships, and every size has a measurement chart so you know the fit before you buy.</p><a class="btn" href="#contact">Talk to us</a></div>
    <ul class="facts"><li>Free exchange within 7 days</li><li>Cash on delivery available</li><li>Orders ship in 1-2 working days</li></ul>
  </section>

  <section id="reviews" class="section">
    <h2>What customers say</h2>
    <p class="sub">Sample reviews. Replace them with your own customers' words.</p>
    <div class="reviews">
      <div class="review"><div class="stars">&#9733;&#9733;&#9733;&#9733;&#9733;</div><p>The linen shirt fits exactly like the size chart said. Arrived in two days.</p><strong>Ahmed R.</strong></div>
      <div class="review"><div class="stars">&#9733;&#9733;&#9733;&#9733;&#9733;</div><p>Lovely fabric and the exchange was easy when I needed a bigger size.</p><strong>Sana K.</strong></div>
      <div class="review"><div class="stars">&#9733;&#9733;&#9733;&#9733;&#9733;</div><p>My son wears the hoodie every day. Still looks new after many washes.</p><strong>Bilal M.</strong></div>
    </div>
  </section>

  <section class="section news">
    <h2>Get 10% off your first order</h2>
    <p>Join our list for new arrivals and sale alerts. No spam.</p>
    <form id="newsForm"><label class="sr" for="nemail">Email</label><input id="nemail" type="email" placeholder="Your email" required><button class="btn" type="submit">Join the list</button></form>
    <p class="formMsg" id="newsMsg" role="status"></p>
  </section>

  <section id="policies" class="section">
    <h2>Shipping & returns</h2>
    <details><summary>How long does delivery take?</summary><p>2-5 working days in major cities, up to 7 elsewhere.</p></details>
    <details><summary>Can I exchange an item?</summary><p>Yes. Unworn items with tags can be exchanged within 7 days of delivery.</p></details>
    <details><summary>Which sizes do you offer?</summary><p>S to XL for adults and 2-12 years for kids. Each product lists exact measurements.</p></details>
    <details><summary>How do I pay?</summary><p>Card, bank transfer, mobile wallet or cash on delivery.</p></details>
  </section>

  <section id="contact" class="section contact">
    <div><h2>Contact</h2><p>Questions about sizing or an order? Message us and we reply within a few hours.</p><a class="btn" id="waLink" href="https://wa.me/923001234567" target="_blank" rel="noopener">Chat on WhatsApp</a></div>
    <form id="contactForm">
      <label>Name<input name="name" required></label>
      <label>Email<input name="email" type="email" required></label>
      <label>Message<textarea name="message" rows="4" required></textarea></label>
      <button class="btn" type="submit">Send message</button>
      <p class="formMsg" id="formMsg" role="status"></p>
    </form>
  </section>
</main>

<footer class="site-footer"><p>&copy; <span id="year"></span> Loom & Line. All rights reserved.</p><p><a href="#policies">Privacy policy</a> | <a href="#policies">Terms</a></p></footer>

<aside class="drawer" id="drawer" aria-label="Shopping cart" hidden>
  <div class="drawer-head"><h2>Your cart</h2><button id="closeCart" aria-label="Close cart">Close</button></div>
  <ul id="cartItems"></ul>
  <p>Total: <strong id="cartTotal">Rs 0</strong></p>
  <button class="btn" id="checkout">Order on WhatsApp</button>
</aside>

<script>
// ===== Edit these for your store =====
const WHATSAPP_NUMBER = "923001234567"; // country code + number, no + or spaces
const CURRENCY = "Rs";

// type: top | dress | bottom. Add old (old price) and badge ("New" or "Sale") if you like.
const products = [
  { id: 1, name: "Linen shirt", cat: "men", type: "top", price: 3200, tint: "#dbe3f3", color: "#3d4a7a", badge: "New", sizes: ["S","M","L","XL"] },
  { id: 2, name: "Straight denim", cat: "men", type: "bottom", price: 4500, old: 5200, tint: "#e4e7f0", color: "#27325c", badge: "Sale", sizes: ["30","32","34","36"] },
  { id: 3, name: "Cotton kurta", cat: "men", type: "top", price: 3800, tint: "#ecdfd0", color: "#6b7a99", sizes: ["S","M","L","XL"] },
  { id: 4, name: "Wrap dress", cat: "women", type: "dress", price: 5200, tint: "#f1d6d3", color: "#b3342f", badge: "New", sizes: ["S","M","L"] },
  { id: 5, name: "Printed lawn suit", cat: "women", type: "dress", price: 6400, old: 7500, tint: "#efe2e8", color: "#8a5a6e", badge: "Sale", sizes: ["S","M","L"] },
  { id: 6, name: "Everyday tee", cat: "women", type: "top", price: 1800, tint: "#dcebe3", color: "#4d6b5c", sizes: ["S","M","L","XL"] },
  { id: 7, name: "Kids hoodie", cat: "kids", type: "top", price: 2600, tint: "#f6e8c8", color: "#c28a2c", badge: "New", sizes: ["2-4","5-7","8-10","11-12"] },
  { id: 8, name: "Kids denim shorts", cat: "kids", type: "bottom", price: 2100, tint: "#dbe3f3", color: "#3d4a7a", sizes: ["2-4","5-7","8-10","11-12"] },
];
const shapes = {
  top: "M30 12 42 8Q50 16 58 8L70 12 90 30 78 42 70 36V90H30V36L22 42 10 30Z",
  dress: "M38 8H46Q50 14 54 8H62L66 30 60 36 78 92H22L40 36 34 30Z",
  bottom: "M30 10H70L74 92H54L50 40 46 92H26Z"
};

const $ = id => document.getElementById(id);
const money = n => `${CURRENCY} ${n.toLocaleString()}`;
let cart = [];
try { cart = JSON.parse(localStorage.getItem("cart")) || []; } catch (e) { cart = []; }
let category = "all";

function renderProducts() {
  const q = $("search").value.trim().toLowerCase();
  const list = products.filter(p => (category === "all" || p.cat === category) && p.name.toLowerCase().includes(q));
  $("grid").innerHTML = list.map(p => `
    <article class="card">
      <div class="pic" style="background:${p.tint}">
        ${p.badge ? `<span class="badge ${p.badge === "New" ? "new" : ""}">${p.badge}</span>` : ""}
        <svg viewBox="0 0 100 100" aria-hidden="true"><path fill="${p.color}" d="${shapes[p.type]}"/></svg>
      </div>
      <div class="info">
        <h3>${p.name}</h3>
        <span class="price">${money(p.price)}${p.old ? `<s>${money(p.old)}</s>` : ""}</span>
        <div class="row">
          <select id="size-${p.id}" aria-label="Size for ${p.name}">${p.sizes.map(s => `<option>${s}</option>`).join("")}</select>
          <button class="btn" data-add="${p.id}">Add</button>
        </div>
      </div>
    </article>`).join("");
  $("empty").hidden = list.length > 0;
}

function setCategory(c) {
  category = c;
  document.querySelectorAll(".chip").forEach(x => x.classList.toggle("active", x.dataset.cat === c));
  renderProducts();
}

function saveCart() {
  try { localStorage.setItem("cart", JSON.stringify(cart)); } catch (e) {}
  renderCart();
}

function renderCart() {
  $("cartCount").textContent = cart.reduce((n, i) => n + i.qty, 0);
  $("cartItems").innerHTML = cart.length ? cart.map((i, idx) => `
    <li><span>${i.name} (${i.size})<br><small>${money(i.price)} x ${i.qty}</small></span>
    <span><button data-dec="${idx}" aria-label="Remove one">-</button> <button data-inc="${idx}" aria-label="Add one">+</button></span></li>`).join("")
    : "<li>Your cart is empty. Add something from the shop.</li>";
  $("cartTotal").textContent = money(cart.reduce((s, i) => s + i.price * i.qty, 0));
}

document.addEventListener("click", e => {
  const t = e.target.closest("button");
  if (!t) return;
  if (t.dataset.cat) setCategory(t.dataset.cat);
  if (t.dataset.jump) { setCategory(t.dataset.jump); $("shop").scrollIntoView(); }
  if (t.dataset.add) {
    const p = products.find(x => x.id == t.dataset.add);
    const size = $("size-" + p.id).value;
    const found = cart.find(i => i.id === p.id && i.size === size);
    found ? found.qty++ : cart.push({ id: p.id, name: p.name, price: p.price, size, qty: 1 });
    saveCart();
    $("drawer").hidden = false;
  }
  if (t.dataset.inc) { cart[t.dataset.inc].qty++; saveCart(); }
  if (t.dataset.dec) { if (--cart[t.dataset.dec].qty <= 0) cart.splice(t.dataset.dec, 1); saveCart(); }
});

$("search").addEventListener("input", renderProducts);
$("openCart").onclick = () => $("drawer").hidden = false;
$("closeCart").onclick = () => $("drawer").hidden = true;

$("checkout").onclick = () => {
  if (!cart.length) return;
  const lines = cart.map(i => `${i.qty} x ${i.name} (${i.size}) - ${money(i.price * i.qty)}`).join("%0A");
  const total = money(cart.reduce((s, i) => s + i.price * i.qty, 0));
  window.open(`https://wa.me/${WHATSAPP_NUMBER}?text=New order:%0A${lines}%0ATotal: ${total}`, "_blank");
};

// Demo only. Connect these forms to Formspree, Netlify Forms or your backend.
$("contactForm").addEventListener("submit", e => { e.preventDefault(); $("formMsg").textContent = "Thanks. We will reply soon."; e.target.reset(); });
$("newsForm").addEventListener("submit", e => { e.preventDefault(); $("newsMsg").textContent = "You're on the list."; e.target.reset(); });

$("waLink").href = `https://wa.me/${WHATSAPP_NUMBER}`;
$("year").textContent = new Date().getFullYear();
renderProducts();
renderCart();
</script>
</body>
</html>
