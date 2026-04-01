<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>All-in-One Website</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{
  font-family:Arial, sans-serif;
  background:#0f172a;
  color:#fff;
}

/* HEADER */
header{
  background:#020617;
  padding:20px;
  text-align:center;
}
header h1{font-size:28px}

/* NAV */
nav{
  display:flex;
  justify-content:center;
  gap:20px;
  background:#020617;
  padding:10px;
  flex-wrap:wrap;
}
nav a{
  color:#fff;
  text-decoration:none;
  font-weight:bold;
}
nav a:hover{color:#00ff99}

/* SECTIONS */
section{
  padding:40px 20px;
  max-width:1100px;
  margin:auto;
}

/* CARD */
.card{
  background:rgba(255,255,255,0.05);
  backdrop-filter:blur(10px);
  padding:20px;
  border-radius:12px;
  margin-bottom:20px;
  box-shadow:0 5px 20px rgba(0,0,0,0.3);
}

/* GRID */
.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:20px;
}

/* BUTTON */
button{
  padding:10px 16px;
  border:none;
  border-radius:6px;
  background:#00ff99;
  color:#000;
  cursor:pointer;
  font-weight:bold;
}
button:hover{
  background:#00cc77;
}

/* INPUT */
input{
  width:100%;
  padding:10px;
  margin:8px 0;
  border-radius:6px;
  border:none;
}

/* FOOTER */
footer{
  background:#020617;
  text-align:center;
  padding:15px;
}

/* LOGIN */
#loginBox{display:none}

/* CART */
#cartCount{
  position:fixed;
  top:10px;
  right:20px;
  background:#00ff99;
  color:#000;
  padding:8px 12px;
  border-radius:20px;
  font-weight:bold;
}

/* MOBILE */
@media(max-width:600px){
  header h1{font-size:22px}
}
</style>

</head>

<body>

<div id="cartCount">Cart: 0</div>

<header>
<h1>My All-in-One Website</h1>
<p>HTML • CSS • JavaScript</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#portfolio">Portfolio</a>
<a href="#shop">Shop</a>
<a href="#login">Login</a>
</nav>

<section id="home">
<div class="card">
<h2>About Me</h2>
<p>I am learning web development and building real projects.</p>
<button onclick="sayHi()">Say Hi</button>
</div>
</section>

<section id="portfolio">
<h2>Portfolio</h2>
<div class="grid">
<div class="card">Project 1<br>Website Design</div>
<div class="card">Project 2<br>Login Page</div>
<div class="card">Project 3<br>Shop UI</div>
</div>
</section>

<section id="shop">
<h2>Shop</h2>
<div class="grid">
<div class="card">
Product A<br>₹999<br>
<button onclick="addToCart()">Add to Cart</button>
</div>

<div class="card">
Product B<br>₹1499<br>
<button onclick="addToCart()">Add to Cart</button>
</div>
</div>
</section>

<section id="login">
<h2>Login</h2>

<button onclick="toggleLogin()">Open / Close Login</button>

<div class="card" id="loginBox">
<input type="text" placeholder="Username" id="user">
<input type="password" placeholder="Password" id="pass">
<button onclick="login()">Login</button>
<p id="msg"></p>
</div>

</section>

<footer>
<p>© 2026 My Website</p>
</footer>

<script>
let cart = 0;

/* SAY HI */
function sayHi(){
  alert("Welcome to my website 🚀");
}

/* CART */
function addToCart(){
  cart++;
  document.getElementById("cartCount").innerText = "Cart: " + cart;
}

/* LOGIN TOGGLE */
function toggleLogin(){
  let box = document.getElementById("loginBox");
  box.style.display = (box.style.display === "block") ? "none" : "block";
}

/* LOGIN SYSTEM */
function login(){
  let u = document.getElementById("user").value.trim();
  let p = document.getElementById("pass").value.trim();
  let msg = document.getElementById("msg");

  if(u === "admin" && p === "1234"){
    msg.style.color = "#00ff99";
    msg.innerText = "Login Success ✅";
  } else {
    msg.style.color = "red";
    msg.innerText = "Wrong Credentials ❌";
  }
}
</script>

</body>
</html>
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>All-in-One Website</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{
  font-family:Arial, sans-serif;
  background:#0f172a;
  color:#fff;
}

/* HEADER */
header{
  background:#020617;
  padding:20px;
  text-align:center;
}
header h1{font-size:28px}

/* NAV */
nav{
  display:flex;
  justify-content:center;
  gap:20px;
  background:#020617;
  padding:10px;
  flex-wrap:wrap;
}
nav a{
  color:#fff;
  text-decoration:none;
  font-weight:bold;
}
nav a:hover{color:#00ff99}

/* SECTIONS */
section{
  padding:40px 20px;
  max-width:1100px;
  margin:auto;
}

/* CARD */
.card{
  background:rgba(255,255,255,0.05);
  backdrop-filter:blur(10px);
  padding:20px;
  border-radius:12px;
  margin-bottom:20px;
  box-shadow:0 5px 20px rgba(0,0,0,0.3);
}

/* GRID */
.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:20px;
}

/* BUTTON */
button{
  padding:10px 16px;
  border:none;
  border-radius:6px;
  background:#00ff99;
  color:#000;
  cursor:pointer;
  font-weight:bold;
}
button:hover{
  background:#00cc77;
}

/* INPUT */
input{
  width:100%;
  padding:10px;
  margin:8px 0;
  border-radius:6px;
  border:none;
}

/* FOOTER */
footer{
  background:#020617;
  text-align:center;
  padding:15px;
}

/* LOGIN */
#loginBox{display:none}

/* CART */
#cartCount{
  position:fixed;
  top:10px;
  right:20px;
  background:#00ff99;
  color:#000;
  padding:8px 12px;
  border-radius:20px;
  font-weight:bold;
}

/* MOBILE */
@media(max-width:600px){
  header h1{font-size:22px}
}
</style>

</head>

<body>

<div id="cartCount">Cart: 0</div>

<header>
<h1>My All-in-One Website</h1>
<p>HTML • CSS • JavaScript</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#portfolio">Portfolio</a>
<a href="#shop">Shop</a>
<a href="#login">Login</a>
</nav>

<section id="home">
<div class="card">
<h2>About Me</h2>
<p>I am learning web development and building real projects.</p>
<button onclick="sayHi()">Say Hi</button>
</div>
</section>

<section id="portfolio">
<h2>Portfolio</h2>
<div class="grid">
<div class="card">Project 1<br>Website Design</div>
<div class="card">Project 2<br>Login Page</div>
<div class="card">Project 3<br>Shop UI</div>
</div>
</section>

<section id="shop">
<h2>Shop</h2>
<div class="grid">
<div class="card">
Product A<br>₹999<br>
<button onclick="addToCart()">Add to Cart</button>
</div>

<div class="card">
Product B<br>₹1499<br>
<button onclick="addToCart()">Add to Cart</button>
</div>
</div>
</section>

<section id="login">
<h2>Login</h2>

<button onclick="toggleLogin()">Open / Close Login</button>

<div class="card" id="loginBox">
<input type="text" placeholder="Username" id="user">
<input type="password" placeholder="Password" id="pass">
<button onclick="login()">Login</button>
<p id="msg"></p>
</div>

</section>

<footer>
<p>© 2026 My Website</p>
</footer>

<script>
let cart = 0;

/* SAY HI */
function sayHi(){
  alert("Welcome to my website 🚀");
}

/* CART */
function addToCart(){
  cart++;
  document.getElementById("cartCount").innerText = "Cart: " + cart;
}

/* LOGIN TOGGLE */
function toggleLogin(){
  let box = document.getElementById("loginBox");
  box.style.display = (box.style.display === "block") ? "none" : "block";
}

/* LOGIN SYSTEM */
function login(){
  let u = document.getElementById("user").value.trim();
  let p = document.getElementById("pass").value.trim();
  let msg = document.getElementById("msg");

  if(u === "admin" && p === "1234"){
    msg.style.color = "#00ff99";
    msg.innerText = "Login Success ✅";
  } else {
    msg.style.color = "red";
    msg.innerText = "Wrong Credentials ❌";
  }
}
</script>

</body>
</html>
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>All-in-One Website</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{
  font-family:Arial, sans-serif;
  background:#0f172a;
  color:#fff;
}

/* HEADER */
header{
  background:#020617;
  padding:20px;
  text-align:center;
}
header h1{font-size:28px}

/* NAV */
nav{
  display:flex;
  justify-content:center;
  gap:20px;
  background:#020617;
  padding:10px;
  flex-wrap:wrap;
}
nav a{
  color:#fff;
  text-decoration:none;
  font-weight:bold;
}
nav a:hover{color:#00ff99}

/* SECTIONS */
section{
  padding:40px 20px;
  max-width:1100px;
  margin:auto;
}

/* CARD */
.card{
  background:rgba(255,255,255,0.05);
  backdrop-filter:blur(10px);
  padding:20px;
  border-radius:12px;
  margin-bottom:20px;
  box-shadow:0 5px 20px rgba(0,0,0,0.3);
}

/* GRID */
.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:20px;
}

/* BUTTON */
button{
  padding:10px 16px;
  border:none;
  border-radius:6px;
  background:#00ff99;
  color:#000;
  cursor:pointer;
  font-weight:bold;
}
button:hover{
  background:#00cc77;
}

/* INPUT */
input{
  width:100%;
  padding:10px;
  margin:8px 0;
  border-radius:6px;
  border:none;
}

/* FOOTER */
footer{
  background:#020617;
  text-align:center;
  padding:15px;
}

/* LOGIN */
#loginBox{display:none}

/* CART */
#cartCount{
  position:fixed;
  top:10px;
  right:20px;
  background:#00ff99;
  color:#000;
  padding:8px 12px;
  border-radius:20px;
  font-weight:bold;
}

/* MOBILE */
@media(max-width:600px){
  header h1{font-size:22px}
}
</style>

</head>

<body>

<div id="cartCount">Cart: 0</div>

<header>
<h1>My All-in-One Website</h1>
<p>HTML • CSS • JavaScript</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#portfolio">Portfolio</a>
<a href="#shop">Shop</a>
<a href="#login">Login</a>
</nav>

<section id="home">
<div class="card">
<h2>About Me</h2>
<p>I am learning web development and building real projects.</p>
<button onclick="sayHi()">Say Hi</button>
</div>
</section>

<section id="portfolio">
<h2>Portfolio</h2>
<div class="grid">
<div class="card">Project 1<br>Website Design</div>
<div class="card">Project 2<br>Login Page</div>
<div class="card">Project 3<br>Shop UI</div>
</div>
</section>

<section id="shop">
<h2>Shop</h2>
<div class="grid">
<div class="card">
Product A<br>₹999<br>
<button onclick="addToCart()">Add to Cart</button>
</div>

<div class="card">
Product B<br>₹1499<br>
<button onclick="addToCart()">Add to Cart</button>
</div>
</div>
</section>

<section id="login">
<h2>Login</h2>

<button onclick="toggleLogin()">Open / Close Login</button>

<div class="card" id="loginBox">
<input type="text" placeholder="Username" id="user">
<input type="password" placeholder="Password" id="pass">
<button onclick="login()">Login</button>
<p id="msg"></p>
</div>

</section>

<footer>
<p>© 2026 My Website</p>
</footer>

<script>
let cart = 0;

/* SAY HI */
function sayHi(){
  alert("Welcome to my website 🚀");
}

/* CART */
function addToCart(){
  cart++;
  document.getElementById("cartCount").innerText = "Cart: " + cart;
}

/* LOGIN TOGGLE */
function toggleLogin(){
  let box = document.getElementById("loginBox");
  box.style.display = (box.style.display === "block") ? "none" : "block";
}

/* LOGIN SYSTEM */
function login(){
  let u = document.getElementById("user").value.trim();
  let p = document.getElementById("pass").value.trim();
  let msg = document.getElementById("msg");

  if(u === "admin" && p === "1234"){
    msg.style.color = "#00ff99";
    msg.innerText = "Login Success ✅";
  } else {
    msg.style.color = "red";
    msg.innerText = "Wrong Credentials ❌";
  }
}
</script>

</body>
</html>
