
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ISNAS</title>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0; padding: 0;
      font-family: 'Outfit', sans-serif;
    }

    body {
      background: radial-gradient(circle at top left, #1f1c2c, #928dab);
      color: white;
      overflow-x: hidden;
    }

    header {
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      background: rgba(0,0,0,0.5);
      padding: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 10;
    }

    header h1 {
      font-size: 1.4rem;
    }

    .hero {
      padding-top: 80px;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      text-align: center;
      position: relative;
      z-index: 1;
    }

    .hero h2 {
      font-size: 2rem;
      animation: typing 4s steps(20) infinite, blink 0.5s step-end infinite alternate;
      white-space: nowrap;
      overflow: hidden;
      border-right: 2px solid white;
      width: fit-content;
      margin: auto;
    }

    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }

    @keyframes blink {
      50% { border-color: transparent; }
    }

    .blob-bg {
      position: absolute;
      top: -100px;
      left: 50%;
      transform: translateX(-50%);
      width: 500px;
      height: 500px;
      background: linear-gradient(135deg, #8e44ad, #3498db);
      border-radius: 50%;
      filter: blur(120px);
      z-index: 0;
      animation: moveBlob 12s infinite linear alternate;
    }

    @keyframes moveBlob {
      0% { transform: translateX(-50%) translateY(0); }
      50% { transform: translateX(-45%) translateY(30px); }
      100% { transform: translateX(-55%) translateY(-20px); }
    }

    .section {
      padding: 4rem 1rem;
      text-align: center;
    }

    .cards {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
      margin-top: 2rem;
    }

    .card {
      background: rgba(255,255,255,0.08);
      border-radius: 1.5rem;
      padding: 2rem;
      box-shadow: 0 10px 20px rgba(0,0,0,0.3);
      transform: perspective(500px) rotateY(0deg);
      transition: transform 0.6s ease, box-shadow 0.3s ease;
    }

    .card:hover {
      transform: perspective(500px) rotateY(10deg);
      box-shadow: 0 15px 25px rgba(0,0,0,0.6);
    }

    .tabs {
      margin-top: 3rem;
    }

    .tab-buttons {
      display: flex;
      justify-content: center;
      gap: 1rem;
    }

    .tab-buttons button {
      padding: 0.5rem 1rem;
      border: none;
      background: white;
      color: #222;
      border-radius: 1rem;
      cursor: pointer;
    }

    .tab-content {
      margin-top: 2rem;
      display: none;
    }

    .tab-content.active {
      display: block;
    }

    .form {
      max-width: 400px;
      margin: auto;
      background: rgba(255,255,255,0.07);
      border-radius: 1rem;
      padding: 2rem;
      margin-top: 2rem;
    }

    .form-group {
      position: relative;
      margin-bottom: 2rem;
    }

    .form-group input,
    .form-group textarea {
      width: 100%;
      padding: 1rem 0.5rem;
      background: transparent;
      border: none;
      border-bottom: 2px solid white;
      color: white;
      font-size: 1rem;
    }

    .form-group label {
      position: absolute;
      top: 1rem;
      left: 0.5rem;
      color: #aaa;
      pointer-events: none;
      transition: all 0.3s ease;
    }

    .form-group input:focus + label,
    .form-group input:not(:placeholder-shown) + label,
    .form-group textarea:focus + label,
    .form-group textarea:not(:placeholder-shown) + label {
      top: -1rem;
      font-size: 0.8rem;
      color: #f0f0f0;
    }

    .form button {
      padding: 0.7rem 1.5rem;
      background: white;
      color: black;
      border: none;
      border-radius: 1rem;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s ease;
    }

    .form button:hover {
      background: #ddd;
    }

    footer {
      text-align: center;
      padding: 2rem 1rem;
      background: rgba(0,0,0,0.3);
    }
  </style>
</head>
<body>

  <div class="blob-bg"></div>

  <header>
    <h1>ISNAS❤️MINFA</h1>
    <nav>
      <a href="#features" style="margin-right: 1rem;">Features</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h2>WELCOME TO ISNAS'S WORLD...</h2>
  </section>

  <section id="features" class="section">
    <h2>Unique Features</h2>
    <div class="cards">
      <div class="card">🌈  ISMI UI + MI</div>
      <div class="card">⚡ Typewriter Text</div>
      <div class="card">📱 100% Mobile Optimized</div>
    </div>

    <div class="tabs">
      <div class="tab-buttons">
        <button onclick="showTab(0)">Tech</button>
        <button onclick="showTab(1)">Design</button>
      </div>
      <div class="tab-content active">We use the latest HTML5, CSS3, and JS for blazing speed.</div>
      <div class="tab-content">Our design philosophy blends minimalism with magic.</div>
    </div>
  </section>

  <section id="contact" class="section">
    <h2>CONTACT US</h2>
<div class="tabs">
      <div class="tab-buttons">
        <button onclick="showTab(0)">076-1444-674</button>
       
      </div>
      <div class="tab-content active">We use the latest HTML5, CSS3, and JS for blazing speed.</div>
      <div class="tab-content">Our design philosophy blends minimalism with magic.</div>
    </div>

    <form class="form">
      <div class="form-group">
        <input type="text" placeholder=" " required>
        <label>Your Name</label>
      </div>
      <div class="form-group">
        <input type="email" placeholder=" " required>
        <label>Email</label>
      </div>
      <div class="form-group">
        <textarea placeholder=" " rows="3" required></textarea>
        <label>Your Message</label>
      </div>
      <button>Send Message</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2025 UniquePhoneX. Made with ❤️ for mobile</p>
  </footer>

  <script>
    function showTab(index) {
      const tabs = document.querySelectorAll('.tab-content');
      tabs.forEach((tab, i) => {
        tab.classList.toggle('active', i === index);
      });
    }
  </script>

</body>
</html>
