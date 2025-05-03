<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Epic Web Design</title>
  <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Raleway', sans-serif;
      color: #333;
      background-color: #f8f9fa;
      scroll-behavior: smooth;
    }

    header {
      background: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e') center/cover no-repeat;
      height: 100vh;
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
    }

    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(0, 0, 0, 0.8);
      padding: 10px 0;
      z-index: 1000;
    }

    nav ul {
      display: flex;
      justify-content: center;
      list-style: none;
    }

    nav ul li {
      margin: 0 20px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s;
    }

    nav ul li a:hover {
      color: #ffd700;
    }

    header h1 {
      font-size: 4rem;
      animation: fadeIn 2s ease-in-out;
    }

    header p {
      font-size: 1.5rem;
      margin-top: 20px;
      animation: fadeIn 3s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    section {
      padding: 80px 20px;
      max-width: 1200px;
      margin: auto;
    }

    .about, .services, .contact {
      text-align: center;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
      margin-top: 40px;
    }

    .card {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }

    .card:hover {
      transform: translateY(-10px);
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 15px;
    }

    .gallery img {
      width: 100%;
      border-radius: 10px;
    }

    .contact form {
      max-width: 600px;
      margin: auto;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .contact input, .contact textarea {
      padding: 15px;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .contact button {
      background-color: #007BFF;
      color: white;
      padding: 15px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .contact button:hover {
      background-color: #0056b3;
    }

    footer {
      background: #222;
      color: #ccc;
      text-align: center;
      padding: 30px 0;
    }

    .modal-checkbox {
      display: none;
    }

    .modal {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.8);
      display: flex;
      justify-content: center;
      align-items: center;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s;
    }

    .modal-content {
      background: white;
      padding: 40px;
      border-radius: 12px;
      text-align: center;
      max-width: 500px;
    }

    .modal-checkbox:checked + .modal {
      opacity: 1;
      pointer-events: auto;
    }

    .modal-close {
      display: inline-block;
      margin-top: 20px;
      padding: 10px 20px;
      background: #333;
      color: white;
      border-radius: 8px;
      cursor: pointer;
    }

  </style>
</head>
<body>

  <nav>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#gallery">Gallery</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <header>
    <h1>Epic Web Design</h1>
    <p>We build digital dreams into beautiful realities.</p>
  </header>

  <section id="about" class="about">
    <h2>About Us</h2>
    <p>We are a passionate team of designers and developers crafting top-notch websites for modern brands.</p>
  </section>

  <section id="services" class="services">
    <h2>Our Services</h2>
    <div class="services-grid">
      <div class="card">🖥️ Web Design</div>
      <div class="card">📱 App Development</div>
      <div class="card">💼 SEO & Marketing</div>
      <div class="card">🎨 Branding</div>
    </div>
  </section>

  <section id="gallery" class="gallery">
    <h2>Gallery</h2>
    <div class="gallery">
      <img src="https://source.unsplash.com/400x300/?website,design" alt="">
      <img src="https://source.unsplash.com/400x300/?coding,html" alt="">
      <img src="https://source.unsplash.com/400x300/?technology,web" alt="">
      <img src="https://source.unsplash.com/400x300/?developer,workspace" alt="">
    </div>
  </section>

  <section id="contact" class="contact">
    <h2>Contact Us</h2>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message" rows="5" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2025 Epic Web Design. All rights reserved.</p>
  </footer>

  <!-- Modal (CSS Only) -->
  <input type="checkbox" id="modal-toggle" class="modal-checkbox">
  <label for="modal-toggle" class="modal">
    <div class="modal-content">
      <h2>Welcome to Epic!</h2>
      <p>Thanks for visiting our site. Enjoy the design!</p>
      <label for="modal-toggle" class="modal-close">Close</label>
    </div>
  </label>

</body>
</html>
