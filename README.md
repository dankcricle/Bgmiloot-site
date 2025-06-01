<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>BGMI Unified Portal</title>
  <link href="https://fonts.googleapis.com/css2?family=Teko:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #000;
      color: #facc15;
    }
    nav {
      background-color: #111;
      padding: 1rem 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    nav img { height: 40px; }
    nav a {
      color: #facc15;
      margin-left: 2rem;
      text-decoration: none;
      font-weight: bold;
    }
    .hero-img {
      width: 100%;
      height: 300px;
      object-fit: cover;
      border-bottom: 4px solid #facc15;
    }
    section { padding: 2rem; }
    h1, h2, h3 {
      font-family: 'Teko', sans-serif;
      text-align: center;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1rem;
      margin-top: 2rem;
    }
    .card {
      background: rgba(255,255,255,0.05);
      border: 1px solid #facc15;
      border-radius: 12px;
      padding: 1rem;
      text-align: center;
      transition: transform 0.3s, box-shadow 0.3s;
      cursor: pointer;
    }
    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
    }
    .card img {
      width: 100%;
      height: 120px;
      object-fit: cover;
      border-radius: 8px;
      margin-bottom: 0.5rem;
    }
    .button {
      background-color: #000;
      color: #facc15;
      padding: 0.5rem 1rem;
      border: 2px solid #facc15;
      border-radius: 6px;
      cursor: pointer;
      margin-top: 1rem;
    }
    .button:hover { background-color: #d97706; }
    .hidden { display: none; }
    .input {
      width: 100%;
      padding: 0.5rem;
      margin-bottom: 1rem;
      border: 2px solid #facc15;
      border-radius: 6px;
      background: #111;
      color: #facc15;
    }
    .qr-img {
      width: 256px;
      height: 256px;
      border: 4px solid #facc15;
      border-radius: 8px;
      margin: 1rem auto;
      display: block;
    }
    footer {
      background-color: #111;
      padding: 2rem;
      text-align: center;
      color: #aaa;
    }
    footer a { color: #facc15; text-decoration: none; }
    .support-button {
      position: fixed;
      bottom: 1rem;
      right: 1rem;
    }
    #processingSection {
      text-align: center;
      font-size: 1.2rem;
      padding: 2rem;
    }
  </style>
</head>
<body>
  <nav>
    <img src="https://i.postimg.cc/GhdQ3SWN/images-2.png" alt="BGMI Logo">
    <div>
      <a href="#rewards">🎁 Rewards</a>
      <a href="#ucdeals">💰 UC Deals</a>
    </div>
  </nav>

  <img src="https://i.postimg.cc/wTyrJrfB/images-1.jpg" class="hero-img" alt="BGMI Event Banner" />

  <section id="rewards">
    <h1>🎁 Free Rewards</h1>
    <p style="text-align: center">Collect exclusive daily rewards!</p>
    <div class="grid">
      <div class="card"><img src="https://i.postimg.cc/QCxHw5z6/images-3.jpg"><div>Outfit Skin<br><a class="button" href="#qrsection">Collect</a></div></div>
      <div class="card"><img src="https://i.postimg.cc/kG4gfCVz/images-4.jpg"><div>Crate Coupon<br><a class="button" href="#qrsection">Collect</a></div></div>
      <div class="card"><img src="https://i.postimg.cc/QxFM7XZW/1725605083-icon-UC-Bundle-11zon.png"><div>500 UC<br><a class="button" href="#qrsection">Collect</a></div></div>
      <div class="card"><img src="https://i.postimg.cc/gJcz2pKj/images-5.jpg"><div>Voice Pack<br><a class="button" href="#qrsection">Collect</a></div></div>
      <div class="card"><img src="https://i.postimg.cc/TYb6GhXQ/images-6.jpg"><div>Silver Fragments<br><a class="button" href="#qrsection">Collect</a></div></div>
    </div>
  </section>

  <section id="ucdeals">
    <h1>💰 Buy UC at Best Rates</h1>
    <p style="text-align: center">🔥 Trusted by 5000+ players</p>
    <div class="grid" id="ucSection"></div>

    <div id="formSection" class="hidden">
      <h2>Enter Your Details</h2>
      <p id="selectedText"></p>
      <input type="text" id="bgmiId" class="input" placeholder="BGMI ID" />
      <input type="email" id="email" class="input" placeholder="Email Address" />
      <button class="button" onclick="showQRSection()">Proceed to Pay</button>
      <button class="button" onclick="resetAll()">← Go Back</button>
    </div>

    <div id="qrSection" class="hidden center">
      <h2>Scan & Pay</h2>
      <p>UPI ID: <strong>Dhamapayhere@fam</strong></p>
      <img src="https://i.postimg.cc/VNZfvTZF/Screenshot-20250601-131409-Fam-App.jpg" alt="QR Code" class="qr-img" />
      <p style="text-align: center">Scan the QR code using any UPI app or use the UPI ID above.<br/>Then upload a screenshot as payment proof.</p>
      <input type="file" class="input" id="paymentScreenshot" accept="image/*" />
      <button class="button" onclick="showProcessing()">Submit Screenshot</button>
      <button class="button" onclick="resetAll()">← Back</button>
    </div>

    <div id="processingSection" class="hidden">
      <h2>🔄 Processing Your Payment</h2>
      <p>Please wait while we verify your payment. This usually takes a few seconds...</p>
    </div>

    <div id="successSection" class="hidden center">
      <h2>✅ Payment Successful!</h2>
      <p>UC will be credited within 10–20 minutes.</p>
      <p>Keep your email receipt for future reference.</p>
      <button class="button" onclick="resetAll()">← Home</button>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 BGMI Unified Portal. Not affiliated with KRAFTON or BATTLEGROUNDS MOBILE INDIA.</p>
    <p><a href="mailto:support@bgmi-portal.com">Contact Support</a></p>
  </footer>

  <div class="support-button">
    <button class="button">💬 Chat with Us</button>
  </div>

  <script>
    const ucOptions = [
      { uc: 600, price: 200 },
      { uc: 2000, price: 500 },
      { uc: 4600, price: 1000 },
      { uc: 6000, price: 1500 },
    ];

    let selectedUC = null;

    const ucSection = document.getElementById("ucSection");
    const formSection = document.getElementById("formSection");
    const qrSection = document.getElementById("qrSection");
    const successSection = document.getElementById("successSection");
    const processingSection = document.getElementById("processingSection");

    ucOptions.forEach(option => {
      const div = document.createElement("div");
      div.className = "card";
      div.innerHTML = `
        <img src="https://i.postimg.cc/QxFM7XZW/1725605083-icon-UC-Bundle-11zon.png">
        <h3>${option.uc} UC</h3>
        <p>Only Rs. ${option.price.toLocaleString("en-IN")}</p>
        <button class="button">Buy Now</button>
      `;
      div.querySelector(".button").addEventListener("click", (e) => {
        e.stopPropagation();
        selectUC(option);
      });
      ucSection.appendChild(div);
    });

    function selectUC(option) {
      selectedUC = option;
      document.getElementById("selectedText").innerText = `Selected: ${option.uc} UC - Rs. ${option.price.toLocaleString("en-IN")}`;
      ucSection.classList.add("hidden");
      formSection.classList.remove("hidden");
    }

    function showQRSection() {
      const bgmiId = document.getElementById("bgmiId").value;
      const email = document.getElementById("email").value;
      const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

      if (!bgmiId || !email || !emailRegex.test(email)) {
        alert("Please enter valid BGMI ID and Email.");
        return;
      }

      formSection.classList.add("hidden");
      qrSection.classList.remove("hidden");
    }

    function showProcessing() {
      const file = document.getElementById("paymentScreenshot").files[0];
      if (!file) {
        alert("Please upload a screenshot as proof of payment.");
        return;
      }

      qrSection.classList.add("hidden");
      processingSection.classList.remove("hidden");

      setTimeout(() => {
        processingSection.classList.add("hidden");
        successSection.classList.remove("hidden");
      }, 3000);
    }

    function resetAll() {
      selectedUC = null;
      document.getElementById("bgmiId").value = "";
      document.getElementById("email").value = "";
      document.getElementById("paymentScreenshot").value = "";
      ucSection.classList.remove("hidden");
      formSection.classList.add("hidden");
      qrSection.classList.add("hidden");
      successSection.classList.add("hidden");
      processingSection.classList.add("hidden");
    }
  </script>
</body>
</html>
