<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0" />
  <title>BGMiLoots - Cheapest UC Deals</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #0f0f0f;
      color: #facc15;
    }
    .container {
      max-width: 1000px;
      margin: auto;
      padding: 2rem;
    }
    h1, h2 {
      text-align: center;
      color: #fcd34d;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1rem;
      margin-top: 2rem;
    }
    .card {
      background: linear-gradient(to bottom right, #92400e, #facc15);
      color: #111;
      border-radius: 12px;
      padding: 1rem;
      text-align: center;
      transition: transform 0.2s;
      cursor: pointer;
      min-width: 180px;
    }
    .card:hover {
      transform: scale(1.05);
    }
    .button {
      background-color: #000;
      color: #facc15;
      padding: 0.5rem 1rem;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      margin-top: 1rem;
    }
    .button:hover {
      background-color: #d97706;
    }
    .hidden {
      display: none;
    }
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
    }
    .center {
      text-align: center;
    }
    #preview {
      max-width: 256px;
      margin-top: 10px;
      display: none;
      border-radius: 8px;
      border: 2px dashed #facc15;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>BGMiLoots - Cheapest UC Deals</h1>
    <p class="center">💸 512 users bought UC today!</p>

    <div id="ucSection" class="grid"></div>

    <div id="formSection" class="hidden">
      <h2>Fill Your Details</h2>
      <p id="selectedText"></p>
      <label for="bgmiId">BGMI ID</label>
      <input type="text" id="bgmiId" class="input" placeholder="Enter your BGMI ID" />
      <label for="email">Email</label>
      <input type="email" id="email" class="input" placeholder="Enter your Email for receipt" />
      <button class="button" onclick="showQR()">Pay Here</button>
      <button class="button" onclick="resetAll()">← Go Back</button>
    </div>

    <div id="qrSection" class="hidden center">
      <h2>Scan & Pay</h2>
      <p>UPI ID: <strong>Dhamapayhere@fam</strong></p>
      <img src="https://i.postimg.cc/Qdsqz4sX/Screenshot-20250531-204225-Fam-App.jpg" alt="QR code to pay via UPI" class="qr-img" />
      <p style="font-size: 1.3rem; font-weight: bold;">📸 Take screenshot of QR code and pay by scanning in your payment app</p>
      <input type="file" accept="image/*" class="input" onchange="previewImage(event)" />
      <img id="preview" alt="Payment screenshot preview" />
      <button class="button" onclick="showSuccess()">Submit Payment Screenshot</button>
      <button class="button" onclick="resetAll()">← Back to Home</button>
    </div>

    <div id="successSection" class="hidden center">
      <!-- Filled by JS -->
    </div>
  </div>

  <script>
    const ucOptions = [
      { id: 1, uc: 600, price: 200, image: "https://i.postimg.cc/cL5qyxGm/images-1.png" },
      { id: 2, uc: 2000, price: 500, image: "https://i.postimg.cc/cL5qyxGm/images-1.png" },
      { id: 3, uc: 4600, price: 1000, image: "https://i.postimg.cc/cL5qyxGm/images-1.png" },
      { id: 4, uc: 6000, price: 1500, image: "https://i.postimg.cc/cL5qyxGm/images-1.png" },
    ];

    let selectedUC = null;

    const ucSection = document.getElementById("ucSection");
    const formSection = document.getElementById("formSection");
    const qrSection = document.getElementById("qrSection");
    const successSection = document.getElementById("successSection");

    ucOptions.forEach(option => {
      const div = document.createElement("div");
      div.className = "card";
      div.innerHTML = `
        <img src="${option.image}" alt="${option.uc} UC" width="80" height="80"/>
        <h3>${option.uc} UC</h3>
        <p>Rs. ${option.price}</p>
        <button class="button">Buy Now</button>
      `;
      div.onclick = () => selectUC(option);
      ucSection.appendChild(div);
    });

    function selectUC(option) {
      selectedUC = option;
      document.getElementById("selectedText").innerText = `Selected: ${option.uc} UC - Rs. ${option.price}`;
      ucSection.classList.add("hidden");
      formSection.classList.remove("hidden");
    }

    function isValidEmail(email) {
      return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
    }

    function showQR() {
      const bgmiId = document.getElementById("bgmiId").value.trim();
      const email = document.getElementById("email").value.trim();

      if (!bgmiId || !email) {
        alert("Please enter BGMI ID and Email");
        return;
      }

      if (!isValidEmail(email)) {
        alert("Please enter a valid email address");
        return;
      }

      formSection.classList.add("hidden");
      qrSection.classList.remove("hidden");
    }

    function previewImage(event) {
      const file = event.target.files[0];
      const reader = new FileReader();
      reader.onload = function(e) {
        const img = document.getElementById("preview");
        img.src = e.target.result;
        img.style.display = "block";
      };
      if (file) {
        reader.readAsDataURL(file);
      }
    }

    function showSuccess() {
      qrSection.classList.add("hidden");
      successSection.classList.remove("hidden");
      successSection.innerHTML = `
        <h2>⏳ Processing your payment...</h2>
        <p>Please wait...</p>
      `;
      setTimeout(() => {
        successSection.innerHTML = `
          <h2>✅️ Payment Successful!</h2>
          <p>Your UC will be delivered in 10–20 minutes.</p>
          <p>Keep your email receipt safe for support.</p>
          <button class="button" onclick="resetAll()">← Back to Home</button>
        `;
      }, 2000);
    }

    function resetAll() {
      selectedUC = null;
      document.getElementById("bgmiId").value = "";
      document.getElementById("email").value = "";
      document.getElementById("preview").style.display = "none";
      ucSection.classList.remove("hidden");
      formSection.classList.add("hidden");
      qrSection.classList.add("hidden");
      successSection.classList.add("hidden");
    }
  </script>
</body>
</html>
