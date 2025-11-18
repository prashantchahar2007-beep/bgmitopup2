<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>777 Level Up | BGMI & Free Fire Top-Up</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      min-height: 100vh;
      background: radial-gradient(circle at top, #111827 0, #020617 45%, #000 100%);
      color: #f9fafb;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }

    .container {
      width: 100%;
      max-width: 520px;
      background: rgba(15, 23, 42, 0.96);
      border-radius: 18px;
      padding: 18px 18px 22px;
      box-shadow: 0 18px 45px rgba(0, 0, 0, 0.75);
      border: 1px solid rgba(148, 163, 184, 0.25);
      backdrop-filter: blur(10px);
    }

    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 14px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .brand-logo {
      width: 34px;
      height: 34px;
      border-radius: 12px;
      background: radial-gradient(circle at top, #22c55e, #15803d);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #020617;
      font-weight: 800;
      font-size: 16px;
    }

    .brand-title {
      font-size: 18px;
      font-weight: 700;
    }

    .brand-sub {
      font-size: 11px;
      color: #9ca3af;
    }

    .badge {
      font-size: 11px;
      padding: 4px 9px;
      border-radius: 999px;
      background: rgba(34, 197, 94, 0.16);
      color: #22c55e;
      border: 1px solid rgba(34, 197, 94, 0.5);
    }

    .tagline {
      font-size: 13px;
      color: #9ca3af;
      margin-bottom: 16px;
    }

    label {
      font-size: 13px;
      margin-bottom: 6px;
      display: block;
    }

    input,
    select {
      width: 100%;
      padding: 10px 12px;
      border-radius: 10px;
      border: 1px solid #1f2937;
      background: #020617;
      color: #e5e7eb;
      margin-bottom: 14px;
      outline: none;
      font-size: 13px;
    }

    input:focus,
    select:focus {
      border-color: #3b82f6;
      box-shadow: 0 0 0 1px rgba(59, 130, 246, 0.4);
    }

    .pill-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 10px;
      margin-bottom: 8px;
    }

    .pill {
      padding: 9px 9px 8px;
      border-radius: 10px;
      border: 1px solid #111827;
      background: #020617;
      cursor: pointer;
      transition: 0.15s;
      font-size: 12px;
    }

    .pill-title {
      font-weight: 600;
      margin-bottom: 2px;
    }

    .pill-meta {
      font-size: 11px;
      color: #9ca3af;
    }

    .pill-price {
      font-size: 12px;
      margin-top: 4px;
      color: #22c55e;
      font-weight: 600;
    }

    .pill.active {
      border-color: #22c55e;
      background: radial-gradient(circle at top left, rgba(34,197,94,0.18), #020617);
    }

    .summary {
      margin-top: 8px;
      padding: 10px 12px;
      border-radius: 10px;
      background: #020617;
      border: 1px dashed rgba(148, 163, 184, 0.5);
      font-size: 13px;
      color: #e5e7eb;
    }

    .summary strong {
      color: #22c55e;
    }

    .total-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 10px;
      font-size: 14px;
    }

    .total-label {
      color: #9ca3af;
    }

    .total-amount {
      font-size: 16px;
      font-weight: 700;
    }

    .info {
      margin-top: 8px;
      font-size: 11px;
      color: #9ca3af;
      line-height: 1.4;
    }

    .btn-primary {
      width: 100%;
      margin-top: 14px;
      padding: 11px 14px;
      border-radius: 999px;
      border: none;
      background: linear-gradient(135deg, #22c55e, #16a34a);
      color: #020617;
      font-weight: 700;
      font-size: 14px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      transition: 0.15s;
    }

    .btn-primary:hover {
      filter: brightness(1.06);
      transform: translateY(-1px);
      box-shadow: 0 10px 25px rgba(34, 197, 94, 0.35);
    }

    .btn-subtext {
      font-size: 11px;
      color: rgba(15,23,42,0.9);
    }

    .disclaimer {
      margin-top: 10px;
      font-size: 11px;
      color: #6b7280;
      line-height: 1.4;
    }

    /* Payment section */
    .payment-section {
      margin-top: 16px;
      padding-top: 12px;
      border-top: 1px solid rgba(31,41,55,0.8);
      display: none;
    }

    .payment-title {
      font-size: 14px;
      font-weight: 600;
      margin-bottom: 6px;
    }

    .upi-row {
      display: flex;
      gap: 10px;
      margin-top: 6px;
      margin-bottom: 10px;
      align-items: center;
    }

    .upi-id-box {
      flex: 1;
      padding: 8px 10px;
      background: #020617;
      border-radius: 10px;
      border: 1px solid #1f2937;
      font-size: 12px;
      color: #e5e7eb;
    }

    .copy-btn {
      font-size: 11px;
      padding: 7px 10px;
      border-radius: 999px;
      border: none;
      background: #1d4ed8;
      color: #e5e7eb;
      cursor: pointer;
    }

    .qr-box {
      margin-top: 8px;
      padding: 8px;
      border-radius: 10px;
      border: 1px solid #1f2937;
      background: #020617;
      font-size: 11px;
      color: #9ca3af;
      text-align: center;
    }

    .qr-box img {
      max-width: 180px;
      width: 100%;
      border-radius: 8px;
      margin-bottom: 6px;
    }

    .utr-note {
      font-size: 11px;
      color: #9ca3af;
      margin-bottom: 6px;
    }

    .small-input {
      font-size: 12px;
      margin-bottom: 8px;
    }

    .success-msg {
      margin-top: 6px;
      font-size: 11px;
      color: #22c55e;
      display: none;
    }

    @media (max-width: 480px) {
      .container {
        padding: 16px 14px 20px;
      }
      .brand-title {
        font-size: 16px;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="header">
      <div class="brand">
        <div class="brand-logo">77</div>
        <div>
          <div class="brand-title">777 Level Up</div>
          <div class="brand-sub">BGMI & Free Fire UC / Diamonds</div>
        </div>
      </div>
      <div class="badge">Direct Top-Up</div>
    </div>

    <p class="tagline">
      Step 1: Details fill karein · Step 2: Pack choose karein · Step 3: UPI se payment karein & UTR number submit karein.
    </p>

    <label for="game">Select Game</label>
    <select id="game">
      <option value="BGMI">BGMI</option>
      <option value="Free Fire">Free Fire</option>
    </select>

    <label for="playerId">Player ID / UID</label>
    <input type="text" id="playerId" placeholder="Enter your in-game Player ID / UID">

    <label>Choose Pack (Demo + Regular)</label>

    <div class="pill-grid" id="packsGrid"></div>

    <div class="summary" id="summaryBox">
      Selected — <strong>None</strong><br>
      Total: ₹0
    </div>

    <div class="total-row">
      <span class="total-label">Total Payable</span>
      <span class="total-amount" id="totalAmount">₹0</span>
    </div>

    <p class="info">
      Tip: Player ID/UID dhyaan se check karein. Galat ID par top-up hone par refund possible nahi hota. Hum kabhi bhi password ya OTP nahi maangte.
    </p>

    <button class="btn-primary" type="button" id="continueBtn">
      Show UPI / QR
      <span class="btn-subtext">(Step 2: Payment)</span>
    </button>

    <!-- Payment section (Step 2) -->
    <div class="payment-section" id="paymentSection">
      <div class="payment-title">Step 2 · Pay using UPI</div>
      <p class="utr-note">
        Neeche diye gaye UPI ID ya QR se exact amount pay karein. Payment complete hone ke baad UPI Transaction / UTR number yahan fill karein.
      </p>

      <div class="upi-row">
        <div class="upi-id-box">
          <strong>UPI ID:</strong> <span id="upiIdText">chandrawati-12@bpunity</span>
        </div>
        <button class="copy-btn" type="button" id="copyUpiBtn">Copy</button>
      </div>

      <div class="qr-box">
        <img src="10813.jpg" alt="UPI QR">
        <p>QR scan karke payment karein ya UPI ID use karein.</p>
      </div>

      <div style="margin-top:10px;">
        <label class="small-input" for="utrInput">UPI Transaction / UTR Number</label>
        <input type="text" id="utrInput" placeholder="Enter UPI transaction ID">
      </div>

      <button class="btn-primary" type="button" id="submitUtrBtn">
        Submit Payment Details
        <span class="btn-subtext">(Step 3: Complete Request)</span>
      </button>

      <div class="success-msg" id="successMsg">
        Your payment details are recorded. Please wait 5–15 minutes for top-up. Agar issue ho to payment screenshot ke sath contact karein.
      </div>
    </div>

    <p class="disclaimer">
      By continuing, you agree to our Terms & Privacy Policy. This website is not affiliated with or endorsed by BGMI, Garena or any other game publishers. Delivery time may vary during peak events or server issues.
    </p>
  </div>

  <script>
    const packs = [
      { id: 1, name: "Demo Pack", uc: "75 UC", price: 39, note: "Try service – cheap test pack" },
      { id: 2, name: "Demo Plus", uc: "300 UC", price: 150, note: "Starter value pack" },
      { id: 3, name: "Basic Pack", uc: "500 UC", price: 249, note: "Perfect for small events" },
      { id: 4, name: "Pro Pack", uc: "700 UC", price: 399, note: "For regular players" },
      { id: 5, name: "Elite Pack", uc: "900 UC", price: 499, note: "Good for crates & spins" },
      { id: 6, name: "Mega Pack", uc: "1300 UC", price: 699, note: "Rank push / elite plus" },
      { id: 7, name: "Ultra Pack", uc: "2000 UC", price: 899, note: "Big events & crates" },
      { id: 8, name: "Diamond Pack", uc: "2500 UC", price: 1099, note: "High value for spenders" },
      { id: 9, name: "Galaxy Pack", uc: "3000 UC", price: 1399, note: "For rare item hunters" },
      { id: 10, name: "Legend Pack", uc: "3500 UC", price: 1699, note: "Max value combo" }
    ];

    const packsGrid = document.getElementById('packsGrid');
    const summaryBox = document.getElementById('summaryBox');
    const totalAmountEl = document.getElementById('totalAmount');
    const continueBtn = document.getElementById('continueBtn');
    const playerIdInput = document.getElementById('playerId');
    const gameSelect = document.getElementById('game');
    const paymentSection = document.getElementById('paymentSection');
    const copyUpiBtn = document.getElementById('copyUpiBtn');
    const utrInput = document.getElementById('utrInput');
    const submitUtrBtn = document.getElementById('submitUtrBtn');
    const successMsg = document.getElementById('successMsg');

    let selectedPack = null;

    function renderPacks() {
      packsGrid.innerHTML = "";
      packs.forEach(pack => {
        const div = document.createElement('div');
        div.className = 'pill';
        div.dataset.id = pack.id;

        div.innerHTML = `
          <div class="pill-title">${pack.name}</div>
          <div class="pill-meta">${pack.uc}</div>
          <div class="pill-price">₹${pack.price}</div>
        `;

        div.addEventListener('click', () => {
          document.querySelectorAll('.pill').forEach(p => p.classList.remove('active'));
          div.classList.add('active');

          selectedPack = { ...pack };

          summaryBox.innerHTML = `
            Selected — <strong>${selectedPack.name} (${selectedPack.uc})</strong><br>
            Note: ${selectedPack.note}<br>
            Total: ₹${selectedPack.price}
          `;

          totalAmountEl.textContent = '₹' + selectedPack.price;
        });

        packsGrid.appendChild(div);
      });
    }

    renderPacks();

    continueBtn.addEventListener('click', () => {
      const playerId = playerIdInput.value.trim();

      if (!playerId) {
        alert('Please enter your Player ID / UID.');
        return;
      }

      if (!selectedPack) {
        alert('Please select a pack.');
        return;
      }

      const game = gameSelect.value;

      const confirmMsg =
        'Game: ' + game +
        '\nPlayer ID: ' + playerId +
        '\nPack: ' + selectedPack.name + ' (' + selectedPack.uc + ')' +
        '\nAmount: ₹' + selectedPack.price +
        '\n\nStep 2: UPI ID / QR se payment karein, phir UPI transaction ID niche submit karein.';

      if (!confirm(confirmMsg)) {
        return;
      }

      paymentSection.style.display = 'block';
      paymentSection.scrollIntoView({ behavior: 'smooth' });
    });

    copyUpiBtn.addEventListener('click', () => {
      const upi = "chandrawati-12@bpunity";
      navigator.clipboard.writeText(upi).then(() => {
        copyUpiBtn.textContent = "Copied";
        setTimeout(() => copyUpiBtn.textContent = "Copy", 1500);
      }).catch(() => {
        alert("Copy failed, UPI ID manually copy karein.");
      });
    });

    submitUtrBtn.addEventListener('click', () => {
      const playerId = playerIdInput.value.trim();
      const game = gameSelect.value;
      const utr = utrInput.value.trim();

      if (!utr) {
        alert('Please enter your UPI Transaction / UTR number.');
        return;
      }

      if (!selectedPack || !playerId) {
        alert('Please fill game, player ID and pack first.');
        return;
      }

      console.log({
        game,
        playerId,
        pack: selectedPack,
        utr
      });

      successMsg.style.display = 'block';
      utrInput.value = "";
      alert(
        'Details submitted.\n\nGame: ' + game +
        '\nPlayer ID: ' + playerId +
        '\nPack: ' + selectedPack.name + ' (' + selectedPack.uc + ')' +
        '\nAmount: ₹' + selectedPack.price +
        '\nUTR: ' + utr +
        '\n\nAb tum payment verify karke manual top-up kar sakte ho.'
      );
    });
  </script>

</body>
</html>
