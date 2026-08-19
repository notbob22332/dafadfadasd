<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#111827">
  <title>Fernbrook Food</title>
  <link rel="stylesheet" href="./styles.css">
</head>
<body>
  <div id="toast" class="toast" role="status"></div>

  <header class="topbar">
    <a class="brand" href="#" onclick="go('order');return false;">
      <span class="brand-mark">F</span>
      <span>Fernbrook Food</span>
    </a>
    <div class="top-actions">
      <button id="cartButton" class="cart-button" onclick="openCart()">Cart <span id="cartCount">0</span></button>
      <button id="accountButton" class="ghost-button" onclick="openAccount()">Account</button>
    </div>
  </header>

  <main>
    <section id="authView" class="auth-shell">
      <div class="auth-card">
        <div class="eyebrow">FERNBROOK FOOD</div>
        <h1 id="authTitle">Welcome back.</h1>
        <p id="authSubtitle">Sign in with your Fernbrook account to order lunch.</p>

        <div class="auth-tabs">
          <button class="active" id="loginTab" onclick="setAuthMode('login')">Login</button>
          <button id="signupTab" onclick="setAuthMode('signup')">Sign Up</button>
        </div>

        <form id="loginForm" onsubmit="requestLogin(event)">
          <label>Email <span class="muted">(or use first name + year level)</span>
            <input id="loginEmail" type="email" placeholder="you@fernbrook.com.au">
          </label>
          <div class="or"><span>OR</span></div>
          <div class="two">
            <label>First name<input id="loginFirstName" type="text" placeholder="First name"></label>
            <label>Year level<select id="loginYear"><option value="">Select</option><option>7</option><option>8</option><option>9</option><option>10</option><option>11</option><option>12</option></select></label>
          </div>
          <button class="primary full" type="submit">Send verification code</button>
        </form>

        <form id="signupForm" class="hidden" onsubmit="requestSignup(event)">
          <label>Email address<input id="signupEmail" type="email" placeholder="you@fernbrook.com.au" required></label>
          <label>First name<input id="signupFirstName" type="text" placeholder="First name" required></label>
          <label>Year level<select id="signupYear" required><option value="">Select</option><option>7</option><option>8</option><option>9</option><option>10</option><option>11</option><option>12</option></select></label>
          <button class="primary full" type="submit">Create account</button>
        </form>

        <form id="verifyForm" class="hidden" onsubmit="verifyCode(event)">
          <div class="code-icon">✉</div>
          <h2>Check your email</h2>
          <p>We sent a 6-digit verification code to <strong id="verifyEmail"></strong>.</p>
          <label>Verification code<input id="verificationCode" inputmode="numeric" maxlength="6" placeholder="000000" required></label>
          <button class="primary full" type="submit">Verify & continue</button>
          <button class="text-button" type="button" onclick="backToAuth()">Use different details</button>
        </form>
        <p id="authError" class="error"></p>
      </div>
    </section>

    <section id="appView" class="hidden">
      <nav class="nav">
        <button data-page="order" onclick="go('order')">Order</button>
        <button data-page="subscriptions" onclick="go('subscriptions')">Subscriptions</button>
        <button data-page="deals" onclick="go('deals')">Deals</button>
        <button data-page="menu" onclick="go('menu')">Menu</button>
        <button data-page="about" onclick="go('about')">About Us</button>
      </nav>

      <section id="page-order" class="page">
        <div class="hero">
          <div>
            <div class="eyebrow">LUNCH, SORTED.</div>
            <h1>Order from your favourite local spots.</h1>
            <p>Choose from multiple restaurants and put everything into one order.</p>
          </div>
          <button class="primary" onclick="openCart()">View cart <span id="heroCartCount">0</span></button>
        </div>
        <div id="restaurants" class="restaurant-grid"></div>
      </section>

      <section id="page-menu" class="page hidden">
        <div class="page-heading"><div><div class="eyebrow">EVERYTHING IN ONE PLACE</div><h1>Menu</h1><p>Prices shown include the current website markup.</p></div></div>
        <div id="menuContent"></div>
      </section>

      <section id="page-deals" class="page hidden">
        <div class="page-heading"><div><div class="eyebrow">SAVE MORE</div><h1>Deals</h1><p>Keep an eye out for limited-time offers.</p></div></div>
        <div id="dealsContent" class="cards"></div>
      </section>

      <section id="page-subscriptions" class="page hidden">
        <div class="page-heading"><div><div class="eyebrow">REPEAT ORDERS</div><h1>Subscriptions</h1><p>Subscription options will appear here when available.</p></div></div>
        <div id="subscriptionsContent" class="cards"></div>
      </section>

      <section id="page-about" class="page hidden">
        <div class="about-grid">
          <div>
            <div class="eyebrow">HOW IT WORKS</div>
            <h1>Lunch without the lunchtime hassle.</h1>
            <p class="lead">Fernbrook Food makes it easier to order lunch from participating local restaurants.</p>
          </div>
          <div class="steps">
            <article><span>01</span><h3>Place your order</h3><p>Choose items from one or several restaurants and check out in one cart.</p></article>
            <article><span>02</span><h3>We collect it</h3><p>During lunch, Miles receives the order and goes to the selected restaurant or restaurants to collect the food.</p></article>
            <article><span>03</span><h3>Meet at the agreed location</h3><p>The food is brought back and delivered or handed over at the agreed location.</p></article>
          </div>
        </div>
      </section>
    </section>
  </main>

  <div id="cartModal" class="modal hidden">
    <div class="modal-panel">
      <button class="modal-close" onclick="closeCart()">×</button>
      <div id="cartStep"></div>
    </div>
  </div>

  <script src="./app.js"></script>
</body>
</html>