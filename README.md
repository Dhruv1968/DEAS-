<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DEAS | Home</title>
<link rel="stylesheet" href="deas.css">
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>
<body>
<style>
  /* Base Reset */
* { margin:0; padding:0; box-sizing:border-box; font-family:'Montserrat', sans-serif; }
body { background:#ffffff; color:#0d1b2a; }

/* Navbar */
nav { display:flex; justify-content:space-between; align-items:center; padding:1rem 2rem; background:#0d6efd; color:#fff; position:sticky; top:0; z-index:10; }
nav h1 { font-size:1.8rem; font-weight:bold; }
nav ul { display:flex; gap:1.5rem; list-style:none; }
nav ul li a { color:#fff; text-decoration:none; font-weight:500; }
nav ul li a.active, nav ul li a:hover { color:#ffd700; }

/* Hero Section */
.hero { text-align:center; padding:4rem 2rem; background:linear-gradient(135deg,#0d6efd,#ffe066); color:#0d1b2a; border-radius:15px; margin:1rem; box-shadow:0 8px 20px rgba(0,0,0,0.05);}
.hero h1 { font-size:2.8rem; margin-bottom:1rem; }
.hero p { font-size:1.2rem; margin-bottom:1.5rem; max-width:700px; margin:0 auto; }
.cta-btn {
  padding:0.8rem 2rem; border:none; border-radius:30px;
  font-weight:bold; font-size:1rem; cursor:pointer;
  background:linear-gradient(135deg,#ffd700,#ffbf00); color:#0d6efd;
  box-shadow:0 6px 15px rgba(0,0,0,0.1); transition:0.3s;
}
.cta-btn:hover { transform:scale(1.05); box-shadow:0 8px 20px rgba(0,0,0,0.15); }

/* Ticker Section */
.ticker-section { padding:1rem 2rem;  background:linear-gradient(135deg,#0d6efd,#ffe066); margin:1rem; border-radius:10px; overflow:hidden; box-shadow:0 4px 15px rgba(0,0,0,0.05);}
.ticker-wrapper { overflow:hidden; white-space:nowrap; position:relative; }
.ticker { display:inline-block; font-weight:bold; font-size:1rem; }

/* Portfolio Cards */
.portfolio-preview { padding:2rem; }
.portfolio-cards { display:flex; gap:1rem; overflow-x:auto; padding:1rem 0; }
.portfolio-card {
  background:#ffffff; padding:1rem; border-radius:15px;
  min-width:200px; box-shadow:0 4px 15px rgba(0,0,0,0.08); transition:0.3s;
}
.portfolio-card:hover { transform:translateY(-5px); box-shadow:0 8px 20px rgba(0,0,0,0.12);}
.portfolio-card h3 { color:#0d6efd; margin-bottom:0.5rem; }
.portfolio-card p { font-weight:bold; margin-bottom:0.5rem; }

/* Features Section */
.features-section { padding:2rem; }
.features { display:flex; flex-wrap:wrap; gap:1rem; justify-content:center; }
.feature-card {
  background:#ffffff; padding:1rem; border-radius:15px;
  width:200px; text-align:center; box-shadow:0 4px 15px rgba(0,0,0,0.08);
  transition:0.3s; text-decoration:none; color:#0d1b2a;
}
.feature-card:hover { transform:translateY(-5px); box-shadow:0 8px 20px rgba(0,0,0,0.12);}
.feature-logo { width:48px; margin-bottom:0.5rem; }

/* Footer */
footer { background:#0d6efd; color:#0d6efd; text-align:center; padding:2rem; margin-top:2rem; border-top:2px solid #ffd700;}
footer a { color:#0d6efd; text-decoration:none; margin:0 0.5rem; }
footer a:hover { color:#ffbf00; }

/* Responsive */
@media(max-width:768px){
  .hero h1 { font-size:2rem; }
  .cta-btn { width:80%; }
  .portfolio-cards { flex-direction:column; align-items:center; }
  .features { flex-direction:column; align-items:center; }
}

</style>

<nav>
  <h1>DEAS</h1>
  <ul>
    <li><a href="deas.html" class="active">Home</a></li>
    <li><a href="portfolio.html">Portfolio</a></li>
    <li><a href="performance.html">Performance</a></li>
    <li><a href="search.html">Search</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="contact.html">Contact</a></li>
    <li id="authLink"><a href="watchlist.html" class="get-started">Watchlist</a></li>
  </ul>
</nav>

<section class="hero">
  <h1>Manage Your Portfolio Like a Pro</h1>
  <p>Track, analyze, and optimize your investments with a modern, secure, and intuitive platform.</p>
  <button class="cta-btn" onclick="window.location.href='watchlist.html'">Watchlist</button>
</section>

<section class="ticker-section">
  <h2>Live Stock Ticker</h2>
  <div class="ticker-wrapper">
    <div class="ticker" id="stockTicker"></div>
  </div>
</section>

<section class="portfolio-preview">
  <h2>Your Portfolio at a Glance</h2>
  <div class="portfolio-cards" id="portfolioCards"></div>
</section>

<section class="section features-section">
  <h2>Features</h2>
  <div class="features">
    <a href="portfolio.html" class="feature-card">
      <img src="https://cdn-icons-png.flaticon.com/512/8399/8399394.png" class="feature-logo">
      <p>Real-time portfolio tracking & analytics</p>
    </a>
    <div class="feature-card">
      <img src="https://cdn-icons-png.flaticon.com/512/10401/10401813.png" class="feature-logo">
      <p>Customizable asset allocation & risk management</p>
    </div>
    <a href="performance.html" class="feature-card">
      <img src="https://img.icons8.com/color/48/000000/combo-chart.png" class="feature-logo">
      <p>Performance reports & visualizations</p>
    </a>
    <div class="feature-card">
      <img src="https://img.icons8.com/color/48/000000/lock.png" class="feature-logo">
      <p>Secure data storage & privacy</p>
    </div>
    <div class="feature-card">
      <img src="https://img.icons8.com/color/48/000000/smartphone-tablet.png" class="feature-logo">
      <p>Responsive design for all devices</p>
    </div>
  </div>
</section>

<footer>
  <p>Follow us on social media:</p>
  <div class="social-links">
    <a href="#"><i class="fab fa-twitter"></i> Twitter</a>
    <a href="#"><i class="fab fa-linkedin"></i> LinkedIn</a>
    <a href="#"><i class="fab fa-instagram"></i> Instagram</a>
  </div>
  <p>&copy; 2025 DEAS. All rights reserved.</p>
</footer>

<script>
const apiKey = "YOUR_ALPHA_VANTAGE_KEY"; // <-- Insert your Alpha Vantage API key
const stocks = ["RELIANCE.BSE", "TCS.BSE", "HDFC.BSE"];
const portfolioContainer = document.getElementById("portfolioCards");
const tickerEl = document.getElementById("stockTicker");

// Helper function to create a mini-chart
function createChart(canvasId, prices) {
  const ctx = document.getElementById(canvasId).getContext("2d");
  new Chart(ctx, {
    type: "line",
    data: { labels:["Day1","Day2","Day3","Day4","Day5"], datasets:[{label:"Price", data:prices, borderColor:"#0d6efd", backgroundColor:"rgba(13,110,253,0.2)", tension:0.3}] },
    options:{plugins:{legend:{display:false}}, responsive:true, maintainAspectRatio:false, scales:{x:{display:false}, y:{display:false}}}
  });
}

// Fetch stock data
async function loadStocks() {
  for (let i=0; i<stocks.length; i++) {
    const symbol = stocks[i];
    try {
      const res = await fetch(`https://www.alphavantage.co/query?function=GLOBAL_QUOTE&symbol=${symbol}&apikey=${apiKey}`);
      const data = await res.json();
      const quote = data["Global Quote"];
      if (!quote) continue;

      const name = symbol.split('.')[0];
      const price = parseFloat(quote["05. price"]);
      const changePercent = parseFloat(quote["10. change percent"]);

      // Update ticker
      const color = changePercent>=0?'green':'red';
      const arrow = changePercent>=0?'▲':'▼';
      tickerEl.innerHTML += `<span style="color:${color}">${name}: ₹${price.toFixed(2)} ${arrow}${Math.abs(changePercent)}%</span> &nbsp;&nbsp; | &nbsp;&nbsp;`;

      // Create portfolio card
      const card = document.createElement("div");
      card.classList.add("portfolio-card");
      card.innerHTML = `
        <h3>${name}</h3>
        <p><strong>Price:</strong> ₹${price.toFixed(2)}</p>
        <p><strong>Gain:</strong> <span style="color:${color}">${arrow}${Math.abs(changePercent)}%</span></p>
        <canvas id="chart${i}" width="200" height="80"></canvas>
      `;
      portfolioContainer.appendChild(card);

      // Mini-chart placeholder
      createChart(`chart${i}`, [price-5, price-3, price-1, price-2, price]);

    } catch(e) { console.error(e); }
  }
}

loadStocks();

// Ticker animation
let pos = 0;
function moveTicker() {
  pos--;
  if (Math.abs(pos) > tickerEl.scrollWidth/2) pos = 0;
  tickerEl.style.transform = `translateX(${pos}px)`;
  requestAnimationFrame(moveTicker);
}
moveTicker();

</script>
<script src="auth.js"></script>
</body>
</html>
