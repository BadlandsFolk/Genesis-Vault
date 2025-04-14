<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Badlands Folk | Genesis Vault Access</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #1a1a1a;
      color: #fdf6e3;
      font-family: 'Courier New', monospace;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      min-height: 100vh;
    }
    header {
      padding: 2rem;
      text-align: center;
    }
    h1 {
      font-size: 2.2rem;
      margin-bottom: 0.5rem;
    }
    p {
      font-size: 1rem;
      max-width: 90%;
    }
    .tiers {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
      padding: 1rem;
      width: 100%;
      max-width: 95%;
    }
    .tier {
      border: 1px solid #ccc;
      padding: 1rem;
      background: #222;
      border-radius: 8px;
    }
    .tier h2 {
      margin-top: 0;
      font-size: 1.2rem;
    }
    .tier p {
      margin: 0.5rem 0;
    }
    .tier a {
      display: inline-block;
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      background-color: #f57c00;
      color: #fff;
      text-decoration: none;
      border-radius: 5px;
    }
    #countdown {
      font-size: 1.2rem;
      margin: 1rem auto;
      color: #ffa726;
    }
    footer {
      margin-top: auto;
      padding: 2rem;
      font-size: 0.9rem;
      color: #888;
      text-align: center;
    }
  </style>
</head>
<body>
  <header>
    <h1>Genesis Vault: 24-Hour Access</h1>
    <p>For the next 24 hours, the gate is open. Your contribution grants permanent access to the Badlands Folk legacy: music, invention, ritual, power. Choose your tier and enter the fold.</p>
    <div id="countdown">Time remaining: 24:00:00</div>
  </header>

  <section class="tiers">
    <div class="tier">
      <h2>Wanderer’s Pledge – $1,000</h2>
      <p>Name etched in our code and vault. Eternal thanks and private updates.</p>
      <a href="https://paypal.me/badlandsfolk/1000" target="_blank">Buy Now</a>
    </div>
    <div class="tier">
      <h2>Seed of Resonance – $10,000</h2>
      <p>Exclusive relic + access to early drops and licensing of selected works.</p>
      <a href="https://paypal.me/badlandsfolk/10000" target="_blank">Buy Now</a>
    </div>
    <div class="tier">
      <h2>Corekeeper – $100,000</h2>
      <p>Pick 1 innovation to co-develop or license. Relic and creative rights included.</p>
      <a href="https://paypal.me/badlandsfolk/100000" target="_blank">Buy Now</a>
    </div>
    <div class="tier">
      <h2>Gatebreaker – $250,000</h2>
      <p>Executive-level access to all products and rituals. Legacy rights across Badlands Folk.</p>
      <a href="https://paypal.me/badlandsfolk/250000" target="_blank">Buy Now</a>
    </div>
    <div class="tier">
      <h2>Founder of Flame – $1,000,000</h2>
      <p>Everything. Name in every record. Physical relic. Founder seat. Co-creator status forever.</p>
      <a href="https://paypal.me/badlandsfolk/1000000" target="_blank">Buy Now</a>
    </div>
  </section>

  <footer>
    This opportunity closes 24 hours after the first tier is claimed.<br>
    You hold the key.
  </footer>

  <script>
    const countdownElement = document.getElementById('countdown');
    let timeRemaining = 24 * 60 * 60;

    function updateCountdown() {
      const hours = String(Math.floor(timeRemaining / 3600)).padStart(2, '0');
      const minutes = String(Math.floor((timeRemaining % 3600) / 60)).padStart(2, '0');
      const seconds = String(timeRemaining % 60).padStart(2, '0');
      countdownElement.textContent = `Time remaining: ${hours}:${minutes}:${seconds}`;
      if (timeRemaining > 0) {
        timeRemaining--;
        setTimeout(updateCountdown, 1000);
      } else {
        countdownElement.textContent = 'The vault is closed.';
      }
    }

    updateCountdown();
  </script>
</body>
</html>
