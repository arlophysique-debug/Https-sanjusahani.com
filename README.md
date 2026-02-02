<!DOCTYPE html><html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>All-in-One Website</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,Helvetica,sans-serif;background:#f5f5f5}
header{background:#111;color:#fff;padding:20px;text-align:center}
nav{display:flex;justify-content:center;gap:20px;background:#222;padding:10px;flex-wrap:wrap}
nav a{color:#fff;text-decoration:none;font-weight:bold}
nav a:hover{color:#00ff99}
section{padding:40px;max-width:1100px;margin:auto}
.card{background:#fff;padding:20px;border-radius:10px;box-shadow:0 5px 15px rgba(0,0,0,.1);margin-bottom:20px}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px}
button{padding:10px 16px;border:none;border-radius:6px;background:#111;color:#fff;cursor:pointer}
button:hover{background:#00aa66}
footer{background:#111;color:#fff;text-align:center;padding:15px}
input{width:100%;padding:10px;margin:8px 0}
#loginBox{display:none}
@media(max-width:600px){header h1{font-size:22px}}
</style>
</head>
<body><header>
<h1>My All‑in‑One Website</h1>
<p>HTML • CSS • JavaScript</p>
</header><nav>
<a href="#home">Home</a>
<a href="#portfolio">Portfolio</a>
<a href="#shop">Shop</a>
<a href="#login">Login</a>
</nav><section id="home">
<div class="card">
<h2>About Me</h2>
<p>I am learning web development and building real projects.</p>
<button onclick="alert('Welcome!')">Say Hi</button>
</div>
</section><section id="portfolio">
<h2>Portfolio</h2>
<div class="grid">
<div class="card">Project 1<br/>Website Design</div>
<div class="card">Project 2<br/>Login Page</div>
<div class="card">Project 3<br/>Shop UI</div>
</div>
</section><section id="shop">
<h2>Shop</h2>
<div class="grid">
<div class="card">Product A<br/>₹999<br/><button>Add to Cart</button></div>
<div class="card">Product B<br/>₹1499<br/><button>Add to Cart</button></div>
</div>
</section><section id="login">
<h2>Login</h2>
<div class="card" id="loginBox">
<input type="text" placeholder="Username" id="user" />
<input type="password" placeholder="Password" id="pass" />
<button onclick="login()">Login</button>
<p id="msg"></p>
</div>
<button onclick="showLogin()">Open Login</button>
</section><footer>
<p>© 2026 My Website</p>
</footer><script>
function showLogin(){document.getElementById('loginBox').style.display='block'}
function login(){
let u=document.getElementById('user').value;
let p=document.getElementById('pass').value;
if(u==='admin' && p==='1234'){document.getElementById('msg').innerText='Login Success'}
else{document.getElementById('msg').innerText='Wrong Credentials'}
}
</script></body>
</html>