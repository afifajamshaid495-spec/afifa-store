# afifa-store
My E commerce website IT- project 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Afifa Store | Tech Accessories</title>
<style>
:root {
  --bg: #0b0b12;
  --panel: #141420;
  --text: #f7f5ff;
  --purple: #a855f7;
  --pink: #ec4899;
  --muted: #aaa8bd;
}
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html { scroll-behavior: smooth; }
body {
  font-family: Arial, sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
}
a { color: inherit; text-decoration: none; }
button, input, select { font: inherit; }
button { cursor: pointer; border: 0; }
.wrap {
  width: min(1140px, 92%);
  margin: auto;
}
.topbar {
  background: #08080d;
  color: #d8d5e6;
  text-align: center;
  padding: 8px;
  font-size: 12px;
}
header {
  position: sticky;
  top: 0;
  z-index: 20;
  background: #0b0b12;
  border-bottom: 1px solid #2b293b;
}
.nav {
  min-height: 72px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 15px;
}
.logo {
  font-size: 24px;
  font-weight: 900;
}
.logo span { color: var(--purple); }
.navlinks {
  display: flex;
  gap: 20px;
  font-size: 14px;
}
.navlinks a:hover { color: #d8aaff; }
.icon-btn {
  background: #1b1b2a;
  color: white;
  border: 1px solid #2b293b;
  border-radius: 10px;
  padding: 10px;
}
.hero {
  padding: 65px 0;
  background: radial-gradient(
    ellipse at 80% 20%,
    #412050,
    transparent 45%
  );
}
.hero-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 30px;
}
.eyebrow {
  color: #d8b4fe;
  background: #21172d;
  border-radius: 30px;
  padding: 7px 12px;
  font-size: 12px;
}
h1 {
  font-size: clamp(40px, 6vw, 68px);
  line-height: 1.1;
  margin: 22px 0;
}
.gradient {
  background: linear-gradient(90deg, #d8b4fe, #f9a8d4);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}
.hero p {
  color: var(--muted);
  font-size: 17px;
}
.btn-row {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin-top: 25px;
}
.btn {
  display: inline-block;
  padding: 12px 18px;
  border-radius: 10px;
  font-weight: bold;
}
.btn-primary {
  background: linear-gradient(110deg, var(--purple), var(--pink));
  color: white;
}
.btn-secondary {
  background: #1b1b2a;
  border: 1px solid #2b293b;
}
.hero-art {
  min-height: 300px;
  display: grid;
  place-items: center;
}
.hero-card {
  width: 100%;
  max-width: 380px;
  padding: 25px;
  border: 1px solid #5b426e;
  border-radius: 25px;
  background: linear-gradient(145deg, #27233a, #13131d);
  text-align: center;
}
.hero-product {
  font-size: 110px;
}
.hero-card h3 {
  font-size: 27px;
}
.section { padding: 60px 0; }
.section-head { margin-bottom: 25px; }
.kicker {
  color: #d8aaff;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-size: 12px;
}
h2 {
  font-size: clamp(28px, 4vw, 40px);
}
.section-head p {
  color: var(--muted);
  margin-top: 8px;
}
.categories {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 15px;
}
.category {
  padding: 22px;
  border-radius: 16px;
  border: 1px solid #2b293b;
  background: var(--panel);
}
.category .emoji {
  display: block;
  font-size: 35px;
}
.category small { color: var(--muted); }
.shop-tools {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
  margin: 20px 0;
}
.search, .filter {
  background: var(--panel);
  border: 1px solid #2b293b;
  color: white;
  border-radius: 10px;
  padding: 12px;
}
.search { flex: 1; min-width: 180px; }
.products {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
}
.product {
  background: var(--panel);
  border: 1px solid #2b293b;
  border-radius: 16px;
  overflow: hidden;
}
.product-art {
  height: 150px;
  display: grid;
  place-items: center;
  font-size: 65px;
  background: radial-gradient(circle, #352344, #1a1828);
}
.product-info { padding: 15px; }
.product-category {
  color: #c084fc;
  font-size: 11px;
  text-transform: uppercase;
}
.product h3 { margin: 5px 0; font-size: 16px; }
.product-desc { color: var(--muted); font-size: 12px; }
.price-row { margin: 10px 0; }
.price { font-size: 19px; font-weight: bold; }
.old-price {
  color: #77748b;
  text-decoration: line-through;
  font-size: 12px;
}
.add-btn {
  width: 100%;
  padding: 10px;
  background: #282035;
  color: #ead8ff;
  border-radius: 9px;
  font-weight: bold;
}
.add-btn:hover {
  background: linear-gradient(100deg, var(--purple), var(--pink));
  color: white;
}
@media(max-width:800px) {
  .hero-grid { grid-template-columns: 1fr; }
  .hero-copy { text-align: center; }
  .btn-row { justify-content: center; }
  .categories, .products { grid-template-columns: repeat(2, 1fr); }
  .navlinks { gap: 10px; font-size: 12px; }
}
@media(max-width:480px) {
  .navlinks { gap: 7px; }
  .logo { font-size: 19px; }
  .hero { padding: 40px 0; }
  .categories, .products { gap: 10px; }
  .product-info { padding: 10px; }
}
</style>
</head>
<div class="topbar">✨ WELCOME TO AFIFA STORE — TECH FOR YOUR STYLE</div>

<header>
  <div class="wrap nav">
    <a class="logo" href="#home">AFIFA<span>STORE.</span></a>
    <nav class="navlinks">
      <a href="#home">Home</a>
      <a href="#categories">Categories</a>
      <a href="#shop">Shop</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
    <button class="icon-btn" onclick="openCart()">
      🛒 Cart (<span id="cartCount">0</span>)
    </button>
  </div>
</header>

<section class="hero" id="home">
  <div class="wrap hero-grid">
    <div class="hero-copy">
      <span class="eyebrow">⚡ YOUR TECH, YOUR STYLE</span>
      <h1>Small accessories.<br>
        <span class="gradient">Big energy.</span>
      </h1>
      <p>
        Discover stylish headphones, earbuds, mobile covers
        and everyday tech accessories at Afifa Store.
      </p>
      <div class="btn-row">
        <a class="btn btn-primary" href="#shop">Shop Products →</a>
        <a class="btn btn-secondary" href="#categories">Explore Categories</a>
      </div>
    </div>
    <div class="hero-art">
      <div class="hero-card">
        <div class="kicker">FEATURED PRODUCT</div>
        <h3>Wireless Headphones</h3>
        <div class="hero-product">🎧</div>
        <h3>Rs. 3,499</h3>
        <p>Sample price — confirm before ordering.</p>
      </div>
    </div>
  </div>
</section>

<section class="section" id="categories">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Explore our collection</div>
      <h2>Shop by Category</h2>
    </div>
    <div class="categories">
      <a class="category" href="#shop">
        <span class="emoji">🎧</span>
        <strong>Headphones</strong><br>
        <small>Music and gaming</small>
      </a>
      <a class="category" href="#shop">
        <span class="emoji">🎵</span>
        <strong>Earbuds</strong><br>
        <small>Compact sound</small>
      </a>
      <a class="category" href="#shop">
        <span class="emoji">📱</span>
        <strong>Mobile Covers</strong><br>
        <small>Protect your phone</small>
      </a>
      <a class="category" href="#shop">
        <span class="emoji">🔌</span>
        <strong>Accessories</strong><br>
        <small>Everyday essentials</small>
      </a>
    </div>
  </div>
</section>

<section class="section" id="shop">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Find your favourites</div>
      <h2>Our Products</h2>
      <p>Prices are examples for this student project.</p>
    </div>

    <div class="shop-tools">
      <input id="searchInput" class="search"
        placeholder="Search products..."
        oninput="renderProducts()">

      <select id="categoryFilter" class="filter"
        onchange="renderProducts()">
        <option value="All">All Categories</option>
        <option value="Headphones">Headphones</option>
        <option value="Earbuds">Earbuds</option>
        <option value="Mobile Covers">Mobile Covers</option>
        <option value="Accessories">Accessories</option>
      </select>

      <select id="sortFilter" class="filter"
        onchange="renderProducts()">
        <option value="featured">Featured</option>
        <option value="low">Price: Low to High</option>
        <option value="high">Price: High to Low</option>
      </select>
    </div>

    <div class="products" id="productsGrid"></div>
  </div>
</section>

<section class="section" id="about">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">About our store</div>
      <h2>Technology meets style.</h2>
    </div>
    <p>
      Afifa Store is an e-commerce website project created to
      showcase headphones, earbuds, mobile covers and accessories.
      It demonstrates responsive web design, product search,
      category filtering and shopping cart functionality.
    </p>
  </div>
</section>

<section class="section" id="contact">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Get in touch</div>
      <h2>Contact Afifa Store</h2>
    </div>
    <p>📱 WhatsApp: 03281308347</p>
    <p>✉️ Email: afifajamshaid495@gmail.com</p>
    <div class="btn-row">
      <a class="btn btn-primary"
        href="https://wa.me/923281308347" target="_blank">
        Chat on WhatsApp
      </a>
      <a class="btn btn-secondary"
        href="mailto:afifajamshaid495@gmail.com">
        Send Email
      </a>
    </div>
  </div>
</section>

<footer class="section">
  <div class="wrap">
    <a class="logo" href="#home">AFIFA<span>STORE.</span></a>
    <p>© 2026 Afifa Store. Student portfolio project.</p>
  </div>
</footer>

<div id="cartBox" style="display:none;padding:25px">
  <h2>Your Shopping Cart</h2>
  <div id="cartItems"></div>
  <h3 id="cartTotal">Total: Rs. 0</h3>
  <button class="btn btn-primary" onclick="sendOrder()">
    Send Order on WhatsApp
  </button>
  <button class="btn btn-secondary" onclick="closeCart()">
    Close Cart
  </button>
</div>

const products = [
  {id:1,name:"Wireless Bass Headphones",category:"Headphones",price:3499,old:4299,emoji:"🎧"},
  {id:2,name:"Bluetooth Earbuds",category:"Earbuds",price:2299,old:2999,emoji:"🎵"},
  {id:3,name:"Premium Phone Cover",category:"Mobile Covers",price:599,old:799,emoji:"📱"},
  {id:4,name:"Clear Protective Cover",category:"Mobile Covers",price:449,old:599,emoji:"📲"},
  {id:5,name:"Gaming Headset",category:"Headphones",price:2899,old:3599,emoji:"🎮"},
  {id:6,name:"Charging Cable",category:"Accessories",price:399,old:549,emoji:"🔌"},
  {id:7,name:"Phone Stand",category:"Accessories",price:699,old:899,emoji:"📐"},
  {id:8,name:"Sport Wireless Earbuds",category:"Earbuds",price:1799,old:2299,emoji:"🎶"},
  {id:9,name:"Protective Phone Case",category:"Mobile Covers",price:999,old:1299,emoji:"🛡️"},
  {id:10,name:"Studio Headphones",category:"Headphones",price:3999,old:4999,emoji:"🎧"},
  {id:11,name:"USB-C Adapter",category:"Accessories",price:549,old:699,emoji:"🔋"},
  {id:12,name:"Patterned Phone Cover",category:"Mobile Covers",price:699,old:899,emoji:"🌸"}
];

const cart = {};

function money(price) {
  return "Rs. " + price.toLocaleString("en-PK");
}

function renderProducts() {
  const search = document.getElementById("searchInput")
    .value.toLowerCase().trim();

  const category = document.getElementById("categoryFilter").value;
  const sort = document.getElementById("sortFilter").value;

  let list = products.filter(p =>
    (category === "All" || p.category === category) &&
    (p.name + " " + p.category).toLowerCase().includes(search)
  );

  if (sort === "low") list.sort((a,b) => a.price-b.price);
  if (sort === "high") list.sort((a,b) => b.price-a.price);

  const grid = document.getElementById("productsGrid");

  if (!list.length) {
    grid.innerHTML = "<p>No products found. Try another search.</p>";
    return;
  }

  grid.innerHTML = list.map(p => `
    <article class="product">
      <div class="product-art">${p.emoji}</div>
      <div class="product-info">
        <div class="product-category">${p.category}</div>
        <h3>${p.name}</h3>
        <p class="product-desc">A stylish everyday tech accessory.</p>
        <div class="price-row">
          <span class="price">${money(p.price)}</span>
          <span class="old-price">${money(p.old)}</span>
        </div>
        <button class="add-btn" onclick="addToCart(${p.id})">
          + Add to Cart
        </button>
      </div>
    </article>
  `).join("");
}

function addToCart(id) {
  cart[id] = (cart[id] || 0) + 1;
  updateCart();
  alert("Product added to your cart!");
}

function updateCart() {
  const entries = Object.entries(cart);
  const count = entries.reduce((sum, item) => sum + item[1], 0);

  document.getElementById("cartCount").textContent = count;

  let total = 0;
  let html = "";

  entries.forEach(([id, qty]) => {
    const p = products.find(x => x.id === Number(id));
    total += p.price * qty;

    html += `
      <p style="margin:12px 0">
        ${p.emoji} ${p.name} × ${qty}
        — ${money(p.price * qty)}
        <button onclick="changeQty(${p.id},-1)">−</button>
        <button onclick="changeQty(${p.id},1)">+</button>
      </p>
    `;
  });

  document.getElementById("cartItems").innerHTML =
    html || "<p>Your cart is empty.</p>";

  document.getElementById("cartTotal").textContent =
    "Total: " + money(total);
}

function changeQty(id, change) {
  cart[id] = (cart[id] || 0) + change;
  if (cart[id] <= 0) delete cart[id];
  updateCart();
}

function openCart() {
  document.getElementById("cartBox").style.display = "block";
  updateCart();
  document.getElementById("cartBox").scrollIntoView();
}

function closeCart() {
  document.getElementById("cartBox").style.display = "none";
}

function sendOrder() {
  const entries = Object.entries(cart);

  if (!entries.length) {
    alert("Please add a product to your cart first.");
    return;
  }

  let total = 0;
  const lines = entries.map(([id, qty]) => {
    const p = products.find(x => x.id === Number(id));
    total += p.price * qty;
    return `${p.name} x ${qty} = ${money(p.price * qty)}`;
  });

  const message =
    "Hi Afifa Store! I want to enquire about this order:\n\n" +
    lines.join("\n") +
    "\n\nEstimated total: " + money(total) +
    "\nPlease confirm availability, prices and delivery.";

  const url = "https://wa.me/923281308347?text=" 
    

renderProducts();
updateCart();
</script>
</body>
</html>
  
