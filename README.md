<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Cyrus Kuiyaki - Criminology Services</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />
  <style>
    :root {
      --light-bg: #f4f4f4;
      --light-text: #1a1a40;
      --light-card-bg: #fff;
      --light-accent: #333399;

      --dark-bg: #121827;
      --dark-text: #e0e6f0;
      --dark-card-bg: #1e2434;
      --dark-accent: #8899ff;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: var(--light-bg);
      color: var(--light-text);
      scroll-behavior: smooth;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    body.dark-mode {
      background: var(--dark-bg);
      color: var(--dark-text);
    }

    header {
      background: var(--light-text);
      color: var(--light-bg);
      padding: 2rem;
      text-align: center;
      position: relative;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    body.dark-mode header {
      background: var(--dark-text);
      color: var(--dark-bg);
    }

    header h1 {
      margin: 0;
      font-size: 2.5rem;
    }

    header p {
      margin-top: 0.5rem;
      font-size: 1.2rem;
    }

    #greeting {
      margin-top: 0.8rem;
      font-style: italic;
      font-size: 1.1rem;
      color: var(--light-accent);
      transition: color 0.3s ease;
    }

    body.dark-mode #greeting {
      color: var(--dark-accent);
    }

    nav {
      margin-top: 1rem;
    }

    nav button {
      background: var(--light-accent);
      color: var(--light-bg);
      border: none;
      padding: 0.5rem 1rem;
      margin: 0 5px;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    nav button:hover {
      background: #5555cc;
    }

    body.dark-mode nav button {
      background: var(--dark-accent);
      color: var(--dark-bg);
    }

    body.dark-mode nav button:hover {
      background: #6677ff;
    }

    section {
      padding: 2rem;
      text-align: center;
    }

    .card {
      background: var(--light-card-bg);
      border-radius: 12px;
      padding: 1.5rem;
      margin: 1rem;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      display: inline-block;
      width: 280px;
      vertical-align: top;
      transition: background-color 0.3s ease, color 0.3s ease;
      color: var(--light-text);
    }

    body.dark-mode .card {
      background: var(--dark-card-bg);
      color: var(--dark-text);
      box-shadow: 0 5px 15px rgba(0,0,0,0.7);
    }

    .card img {
      width: 100%;
      border-radius: 8px;
    }

    .contact a {
      color: #0066cc;
      text-decoration: none;
      transition: color 0.3s ease;
    }

    body.dark-mode .contact a {
      color: #99bbff;
    }

    .interactive {
      background: #e2e2ff;
      padding: 2rem;
      margin-top: 2rem;
      transition: background-color 0.3s ease;
    }

    body.dark-mode .interactive {
      background: #202744;
    }

    footer {
      background: var(--light-text);
      color: var(--light-bg);
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    body.dark-mode footer {
      background: var(--dark-text);
      color: var(--dark-bg);
    }

    button.call-btn {
      padding: 10px 20px;
      border: none;
      background-color: var(--light-text);
      color: var(--light-bg);
      font-size: 1rem;
      border-radius: 8px;
      cursor: pointer;
      margin: 5px;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    button.call-btn:hover {
      background-color: #3333aa;
    }

    body.dark-mode button.call-btn {
      background-color: var(--dark-text);
      color: var(--dark-bg);
    }

    body.dark-mode button.call-btn:hover {
      background-color: #4455dd;
    }

    /* Carousel styles */
    .carousel-container {
      max-width: 600px;
      margin: 0 auto;
      position: relative;
      background: var(--light-card-bg);
      border-radius: 12px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      overflow: hidden;
      padding: 1rem;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    body.dark-mode .carousel-container {
      background: var(--dark-card-bg);
      box-shadow: 0 5px 15px rgba(0,0,0,0.7);
      color: var(--dark-text);
    }

    .carousel-slide {
      display: flex;
      transition: transform 0.5s ease-in-out;
    }

    .project-card {
      min-width: 100%;
      box-sizing: border-box;
      padding: 1rem;
      text-align: left;
      color: inherit;
    }

    .project-card img {
      width: 100%;
      border-radius: 8px;
      margin-bottom: 1rem;
    }

    .carousel-buttons {
      text-align: center;
      margin-top: 1rem;
    }

    .carousel-buttons button {
      background: var(--light-text);
      border: none;
      color: var(--light-bg);
      padding: 8px 16px;
      margin: 0 8px;
      border-radius: 6px;
      cursor: pointer;
      font-size: 1rem;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    .carousel-buttons button:hover {
      background: #3333aa;
    }

    body.dark-mode .carousel-buttons button {
      background: var(--dark-text);
      color: var(--dark-bg);
    }

    body.dark-mode .carousel-buttons button:hover {
      background: #4455dd;
    }

    /* Dark mode toggle button */
    #darkModeToggle {
      position: absolute;
      top: 1rem;
      right: 1rem;
      background: transparent;
      border: 2px solid var(--light-bg);
      color: var(--light-bg);
      padding: 0.3rem 0.6rem;
      border-radius: 6px;
      cursor: pointer;
      font-weight: bold;
      font-size: 0.9rem;
      transition: all 0.3s ease;
      user-select: none;
    }

    #darkModeToggle:hover {
      background: var(--light-bg);
      color: var(--light-text);
    }

    body.dark-mode #darkModeToggle {
      border-color: var(--dark-bg);
      color: var(--dark-bg);
    }

    body.dark-mode #darkModeToggle:hover {
      background: var(--dark-bg);
      color: var(--dark-text);
    }
  </style>
</head>
<body>
  <header class="animate__animated animate__fadeInDown">
    <h1>Cyrus Kuiyaki</h1>
    <p>Criminology & Legal Services Consultant</p>
    <div id="greeting"></div>
    <nav>
      <button onclick="scrollToSection('about')">About</button>
      <button onclick="scrollToSection('services')">Services</button>
      <button onclick="scrollToSection('projects')">Former Projects</button>
      <button onclick="scrollToSection('contact')">Contact</button>
    </nav>
    <button id="darkModeToggle" aria-label="Toggle Dark Mode">🌙 Dark Mode</button>
  </header>

  <section id="about" class="about animate__animated animate__fadeInUp">
    <h2>About Cyrus</h2>
    <p>Cyrus Kuiyaki is an experienced criminology professional who has served as a Probation Officer and worked with the Nairobi County Council. With strong connections in the legal field, Cyrus can link you with experienced lawyers for your needs.</p>
  </section>

  <section id="services" class="services animate__animated animate__fadeInUp animate__delay-1s">
    <h2>Our Services</h2>
    <div class="card">
      <img src="https://via.placeholder.com/280x180?text=Investigations" alt="Investigation" />
      <h3>Criminal Investigations</h3>
      <p>Professional help with investigating criminal cases and background checks.</p>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/280x180?text=Probation" alt="Probation" />
      <h3>Probation Services</h3>
      <p>Rehabilitation and follow-up support for individuals on probation.</p>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/280x180?text=Legal+Referrals" alt="Legal Referrals" />
      <h3>Legal Referrals</h3>
      <p>Connecting you with trusted lawyers to handle your legal matters.</p>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/280x180?text=Crime+Prevention" alt="Crime Prevention" />
      <h3>Crime Prevention Advice</h3>
      <p>Guidance and workshops on reducing crime risks for individuals and communities.</p>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/280x180?text=Rehabilitation" alt="Rehabilitation" />
      <h3>Rehabilitation Programs</h3>
      <p>Support for offenders aiming to reintegrate into society successfully.</p>
    </div>
  </section>

  <section id="projects" class="projects animate__animated animate__fadeInUp animate__delay-2s">
    <h2>Former Work Projects</h2>
    <div class="carousel-container">
      <div class="carousel-slide" id="carouselSlide">
        <div class="project-card">
          <img src="https://via.placeholder.com/600x300?text=Community+Outreach" alt="Community Outreach" />
          <h3>Community Outreach Program</h3>
          <p>Designed and led community workshops to educate youth on crime prevention.</p>
        </div>
        <div class="project-card">
          <img src="https://via.placeholder.com/600x300?text=Probation+System" alt="Probation System" />
          <h3>Probation Management System</h3>
          <p>Implemented a new tracking system for probation officers to improve rehabilitation follow-up.</p>
        </div>
        <div class="project-card">
          <img src="https://via.placeholder.com/600x300?text=Legal+Liaison" alt="Legal Liaison" />
          <h3>Legal Liaison Services</h3>
          <p>Facilitated partnerships between law enforcement and legal experts for case management.</p>
        </div>
      </div>
      <div class="carousel-buttons">
        <button onclick="prevProject()">Previous</button>
        <button onclick="nextProject()">Next</button>
      </div>
    </div>
  </section>

  <section id="contact" class="contact animate__animated animate__fadeInUp animate__delay-3s">
    <h2>Contact Cyrus</h2>
    <p>If you want to get in touch, call Cyrus at <a href="tel:0700695101">0700 695 101</a></p>
    <button class="call-btn" onclick="window.location.href='tel:0700695101'">Call Now</button>
  </section>

  <footer>
    <p>&copy; 2025 Cyrus Kuiyaki - All Rights Reserved</p>
  </footer>

  <script>
    // Scroll to section function for navigation buttons
    function scrollToSection(id) {
      const element = document.getElementById(id);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    }

    // Dark mode toggle
    const darkModeToggle = document.getElementById('darkModeToggle');
    darkModeToggle.addEventListener('click', () => {
      document.body.classList.toggle('dark-mode');
      if(document.body.classList.contains('dark-mode')){
        darkModeToggle.textContent = '☀️ Light Mode';
      } else {
        darkModeToggle.textContent = '🌙 Dark Mode';
      }
    });

    // Carousel functionality for Former Work Projects
    const carouselSlide = document.getElementById('carouselSlide');
    const projects = carouselSlide.children;
    let currentIndex = 0;

    function updateCarousel() {
      const offset = -currentIndex * 100;
      carouselSlide.style.transform = `translateX(${offset}%)`;
    }

    function prevProject() {
      currentIndex = (currentIndex === 0) ? projects.length - 1 : currentIndex - 1;
      updateCarousel();
    }

    function nextProject() {
      currentIndex = (currentIndex === projects.length - 1) ? 0 : currentIndex + 1;
      updateCarousel();
    }

    // Optional: greet user based on time of day
    const greetingEl = document.getElementById('greeting');
    const hour = new Date().getHours();
    let greetText = '';
    if (hour < 12) greetText = 'Good morning!';
    else if (hour < 18) greetText = 'Good afternoon!';
    else greetText = 'Good evening!';
    greetingEl.textContent = greetText;
  </script>
</body>
</html>
