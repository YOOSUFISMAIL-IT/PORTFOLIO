<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- Font Awesome 6 -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" />
  <!-- Google Fonts: Anta -->
  <link href="https://fonts.googleapis.com/css2?family=Anta&display=swap" rel="stylesheet" />
  <title>ISMAIL | Portfolio</title>
  <style>
    /* ===== ROOT VARIABLES (FIXED) ===== */
    :root {
      --bg-color: #1f242e;
      --second-bg-color: #323946;
      --text-color: #fff;
      --main-color: #0ef;
      --box-shadow: 0 0 1rem rgba(0, 0, 0, 0.3);
      --box-shadow-hover: 0 0 2rem var(--main-color);
      --secondary-color: #ccc;
      --dark-color: #ddd;
      --abc-color: rgba(0, 0, 0, 0.7);
      --main-color2: #0ef;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      list-style-type: none;
      text-decoration: none;
      border: none;
      outline: none;
      font-family: "Anta", sans-serif;
    }

    html {
      font-size: 62.5%;
      overflow-x: hidden;
      scroll-behavior: smooth;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-color);
    }

    section {
      min-height: 100vh;
      padding: 12rem 9% 4rem;
    }

    span {
      color: var(--main-color);
    }

    /* Header */
    .header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      padding: 2rem 9%;
      background-color: rgba(31, 36, 46, 0.95);
      backdrop-filter: blur(10px);
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
    }

    .logo {
      font-size: 2.8rem;
      font-weight: 700;
      color: var(--text-color);
      letter-spacing: 1px;
    }

    .logo span {
      color: var(--main-color);
    }

    nav a {
      font-size: 1.7rem;
      color: var(--text-color);
      margin-left: 4rem;
      transition: 0.3s;
      font-weight: 500;
    }

    nav a:hover,
    nav a.active {
      color: var(--main-color);
      text-shadow: 0 0 8px rgba(0, 238, 255, 0.5);
    }

    /* Home Section */
    .home {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 5rem;
      flex-wrap: wrap;
    }
    .home-content {
      flex: 1;
    }
    .home-content h1 {
      font-size: 5.6rem;
      font-weight: 700;
      line-height: 1.2;
    }
    .home-content h3 {
      font-size: 3.2rem;
      font-weight: 700;
      margin: 1rem 0;
    }
    .home-content p {
      font-size: 1.6rem;
      margin: 2rem 0 3rem;
      line-height: 1.6;
    }
    .btn {
      display: inline-block;
      padding: 1.2rem 2.8rem;
      background: var(--main-color);
      border-radius: 4rem;
      font-size: 1.6rem;
      color: var(--bg-color);
      font-weight: 600;
      transition: 0.3s;
      box-shadow: 0 0 1rem var(--main-color);
      cursor: pointer;
    }
    .btn:hover {
      box-shadow: none;
      transform: translateY(-3px);
    }
    .home-img {
      flex: 1;
      text-align: center;
    }
    .home-img img {
      width: 70%;
      border-radius: 50%;
      box-shadow: 0 0 2rem var(--main-color);
      animation: float 3s ease-in-out infinite;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-2rem); }
      100% { transform: translateY(0); }
    }

    /* Social Media Icons */
    .social-media {
      margin: 2rem 0;
    }
    .social-icons a,
    .social-media a {
      display: inline-flex;
      justify-content: center;
      align-items: center;
      width: 4rem;
      height: 4rem;
      background: transparent;
      border: 0.2rem solid var(--main-color);
      border-radius: 50%;
      font-size: 2rem;
      color: var(--main-color);
      margin: 0 1rem 1rem 0;
      transition: 0.5s ease;
    }
    .social-icons a:hover,
    .social-media a:hover {
      background: var(--main-color);
      color: var(--second-bg-color);
      box-shadow: 0 0 1rem var(--main-color);
    }

    /* About Section */
    .about {
      background-color: var(--second-bg-color);
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 5rem;
      flex-wrap: wrap;
    }
    .about-img img {
      width: 25vw;
      border-radius: 2rem;
      box-shadow: 0 0 1rem var(--main-color);
      min-width: 200px;
    }
    .about-content h2 {
      font-size: 4rem;
    }
    .about-content h3 {
      font-size: 2.6rem;
      margin: 1rem 0;
    }
    .about-content p {
      font-size: 1.6rem;
      line-height: 1.6;
      margin: 2rem 0;
    }
    #moreText {
      display: none;
    }
    #moreText.show {
      display: block;
    }

    /* Skills Section */
    .skills h2 {
      font-size: 4rem;
      text-align: center;
      margin-bottom: 5rem;
    }
    .skills-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 3rem;
    }
    .skill-category {
      background-color: var(--second-bg-color);
      padding: 3.5rem;
      border-radius: 2rem;
      transition: 0.5s ease;
    }
    .skill-category:hover {
      transform: scale(1.03);
      box-shadow: var(--box-shadow-hover);
    }
    .skill-category h3 {
      font-size: 2.5rem;
      margin-bottom: 1.5rem;
      text-align: center;
    }
    .skill {
      margin-bottom: 1.5rem;
    }
    .skill-name {
      font-size: 1.75rem;
      display: flex;
      justify-content: space-between;
      margin-bottom: 0.875rem;
      font-weight: 500;
    }
    .skill-bar {
      width: 100%;
      height: 7.5px;
      background-color: var(--main-color);
      border-radius: 5px;
      overflow: hidden;
    }
    .skill-level {
      width: 0;
      height: 100%;
      background: var(--text-color);
      transition: width 1.5s ease-out;
    }

    /* Portfolio */
    .portfolio h2 {
      font-size: 4rem;
      text-align: center;
      margin-bottom: 4rem;
    }
    .portfolio-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2.5rem;
    }
    .portfolio-item {
      background: var(--second-bg-color);
      border-radius: 2rem;
      overflow: hidden;
      transition: 0.3s;
    }
    .portfolio-item:hover {
      transform: translateY(-8px);
    }
    .portfolio-item img {
      width: 100%;
      height: 220px;
      object-fit: cover;
    }
    .portfolio-info {
      padding: 1.8rem;
    }
    .portfolio-info h3 {
      font-size: 2rem;
    }
    .portfolio-info p {
      font-size: 1.4rem;
      margin: 0.5rem 0 1rem;
    }
    .portfolio-info a {
      color: var(--main-color);
      font-size: 1.4rem;
      font-weight: 600;
    }

    /* Certifications */
    .certifications {
      background: var(--second-bg-color);
    }
    .certifications h2 {
      font-size: 4rem;
      text-align: center;
      margin-bottom: 5rem;
    }
    .certifications-container {
      position: relative;
      max-width: 100%;
      margin: 0 auto 7rem;
    }
    .certifications-container::before {
      content: '';
      position: absolute;
      left: 30px;
      top: 0;
      height: 100%;
      width: 2px;
      background-color: var(--main-color);
      z-index: 1;
    }
    .experience-item {
      position: relative;
      margin-bottom: 4.375rem;
      padding-left: 80px;
    }
    .experience-date {
      position: absolute;
      left: 0;
      top: 0;
      width: 65px;
      height: 65px;
      border-radius: 1rem;
      padding: 0.875rem;
      background-color: var(--bg-color);
      color: white;
      text-align: center;
      font-weight: 600;
      box-shadow: var(--box-shadow);
      z-index: 2;
      font-size: 3rem;
    }
    .experience-date i {
      color: var(--main-color);
    }
    .experience-content {
      display: flex;
      background-color: var(--bg-color);
      padding: 1.5rem;
      border-radius: 1rem;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      position: relative;
    }
    .experience-content::before {
      content: "";
      position: absolute;
      top: 0;
      left: -10px;
      width: 6px;
      height: 100%;
      background: var(--main-color);
      border-radius: 6px 0 0 6px;
    }
    .experience-content .content {
      width: 60%;
    }
    .experience-content .content h3 {
      font-size: 2.45rem;
      color: var(--main-color);
      margin-bottom: 0.875rem;
    }
    .experience-content .content h4 {
      font-size: 1.825rem;
      color: var(--secondary-color);
      margin-bottom: 1rem;
      font-weight: 500;
    }
    .experience-content .content p {
      font-size: 1.5rem;
      margin-bottom: 1rem;
    }
    .experience-content .cert-img {
      position: relative;
      width: 35%;
      height: 180px;
      overflow: hidden;
      border-radius: 1rem;
    }
    .experience-content .cert-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .cert-img .img-layer {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, rgba(0,238,255,0.8), rgba(0,100,255,0.9));
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      gap: 1rem;
      transform: translateY(100%);
      transition: 0.4s ease;
    }
    .cert-img:hover .img-layer {
      transform: translateY(0);
    }
    .img-layer button {
      background: var(--bg-color);
      color: var(--main-color);
      border: 1px solid var(--main-color);
      padding: 0.6rem 1.2rem;
      border-radius: 3rem;
      cursor: pointer;
      font-size: 1.2rem;
      font-weight: bold;
      transition: 0.3s;
    }
    .img-layer button:hover {
      background: var(--main-color);
      color: var(--bg-color);
      box-shadow: 0 0 1rem var(--main-color);
    }

    /* Contact */
    .contact h2 {
      font-size: 4rem;
      text-align: center;
      margin-bottom: 3rem;
    }
    .contact form {
      max-width: 70rem;
      margin: 1rem auto;
      text-align: center;
    }
    .contact form .input-box {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
    }
    .contact form .input-box input,
    .contact form textarea {
      width: 100%;
      padding: 1.5rem;
      font-size: 1.6rem;
      color: var(--text-color);
      background: var(--second-bg-color);
      border-radius: 0.8rem;
      margin: 0.7rem 0;
      transition: 0.3s;
    }
    .contact form .input-box input:focus,
    .contact form textarea:focus {
      transform: scale(1.01);
      box-shadow: var(--box-shadow-hover);
    }
    .contact form .input-box input {
      width: 49%;
    }
    .contact form textarea {
      resize: none;
    }
    .contact form .btn {
      margin-top: 2rem;
      cursor: pointer;
    }

    /* Footer */
    .footer {
      display: flex;
      padding: 3rem 2rem;
      background: var(--second-bg-color);
      flex-wrap: wrap;
      flex-direction: column;
      align-items: center;
    }
    .footer-container {
      display: flex;
      width: 100%;
      padding: 0 9%;
      flex-wrap: wrap;
      justify-content: space-between;
    }
    .footer-title {
      font-size: 2.5rem;
      padding: 2rem 0;
      color: var(--main-color);
    }
    .footer-column {
      width: 24%;
      padding: 0 1rem 2rem 0;
    }
    .footer-column p {
      font-size: 1.75rem;
      padding: 1rem 0;
    }
    .footer-links a {
      color: var(--text-color);
      font-size: 1.75rem;
      padding: 1rem 0;
      display: block;
      transition: 0.3s;
    }
    .footer-links a:hover {
      color: var(--main-color);
      padding-left: 5px;
    }
    .foot-note {
      width: 100%;
      text-align: center;
      padding-top: 2rem;
      margin-top: 2rem;
      border-top: 1px solid var(--main-color);
    }
    .footer-text p {
      font-size: 1.6rem;
    }
    .footer-text a {
      color: var(--main-color);
    }

    /* Modal */
    .modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.95);
      z-index: 2000;
      justify-content: center;
      align-items: center;
    }
    .modal-content {
      position: relative;
      background: var(--second-bg-color);
      max-width: 90%;
      max-height: 90%;
      border-radius: 2rem;
      padding: 2rem;
      animation: fadeIn 0.3s;
    }
    .modal-close {
      position: absolute;
      top: 1rem;
      right: 2rem;
      font-size: 3rem;
      background: none;
      border: none;
      color: var(--text-color);
      cursor: pointer;
    }
    .modal-close:hover {
      color: var(--main-color);
    }
    .modal-body {
      text-align: center;
    }
    .modal-body img {
      max-width: 100%;
      max-height: 80vh;
    }
    .modal-body iframe {
      width: 80vw;
      height: 80vh;
      border: none;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    /* Responsive */
    @media (max-width: 991px) {
      html { font-size: 55%; }
      .header { padding: 2rem 4%; }
      section { padding: 10rem 4% 2rem; }
      .footer-container { padding: 0 4%; }
      .footer-column { width: 48%; }
    }
    @media (max-width: 768px) {
      .home, .about { flex-direction: column; text-align: center; }
      .home-img img, .about-img img { width: 60%; }
      nav a { margin-left: 2rem; font-size: 1.5rem; }
      .contact form .input-box input { width: 100%; }
      .experience-content .content, .experience-content .cert-img { width: 100%; text-align: center; }
      .cert-img { margin-top: 1rem; }
    }
    @media (max-width: 450px) {
      html { font-size: 50%; }
      .header { flex-direction: column; gap: 1rem; padding: 1.5rem; }
      nav a { margin: 0 1rem; }
      .footer-column { width: 100%; }
    }
  </style>
</head>
<body>
  <header class="header">
    <a href="#" class="logo">Y.M. <span>ISMAIL</span></a>
    <nav>
      <a href="#home" class="active">HOME</a>
      <a href="#about">ABOUT</a>
      <a href="#skills">SKILLS</a>
      <a href="#portfolio">PORTFOLIO</a>
      <a href="#certifications">Certifications</a>
      <a href="#contact">CONTACT</a>
    </nav>
  </header>

  <!-- Home Section -->
  <section class="home" id="home">
    <div class="home-content">
      <h3>Hello, It's Me</h3>
      <h1>ISMAIL</h1>
      <h3>And I'm a <span>Software & Full-stack Developer</span></h3>
      <p>I am an aspiring IT professional with a strong passion for technology, problem-solving, and continuous learning. I am actively developing my knowledge in programming, networking, and software development while building a solid foundation in core IT skills.</p>
      <div class="social-media">
        <a href="https://www.facebook.com/share/199ub1b9PB/"><i class="fa-brands fa-facebook-f"></i></a>
        <a href="https://github.com/ismail9148"><i class="fa-brands fa-github"></i></a>
        <a href="https://www.instagram.com/accounts/onetap/"><i class="fa-brands fa-instagram"></i></a>
        <a href="https://www.linkedin.com/in/yoosuf-ismail-056705282"><i class="fa-brands fa-linkedin-in"></i></a>
      </div>
      <a href="https://drive.google.com/file/d/16zZwl9h54iYHd9LxvNq2JEEPDXApzpwv/view?usp=sharing" class="btn">Download CV</a>
    </div>
    <div class="home-img">
      <img src="images/img1.jpg" alt="Profile Image">
    </div>
  </section>

  <!-- About Section -->
  <section class="about" id="about">
    <div class="about-img">
      <img src="images/img1.jpg" alt="About Me">
    </div>
    <div class="about-content">
      <h2>About <span>Me</span></h2>
      <h3>Aspiring IT Professional</h3>
      <p>I am Yoosuf Mohamed Ismail, a 27-year-old from Sri Lanka. I completed my Advanced Level education at KM/Al-Asraq M.M.V and am currently pursuing a Bachelor of Arts degree at South Eastern University of Sri Lanka. I have a strong passion for technology and a keen interest in developing my knowledge and skills in the IT field.</p>
      <span id="moreText">
        <h3>Education</h3>
        <p>Bachelor of Arts degree at South Eastern University of Sri Lanka.</p>
        <p>Cyber Security Master Course, MarsTech Campus (2024)</p>
        <p>Artificial Intelligence Master Course, MarsTech Campus (2024)</p>
      </span>
      <button class="btn" id="readMoreBtn">Read More</button>
    </div>
  </section>

  <!-- Skills Section -->
  <section class="skills" id="skills">
    <h2>Skills & <span>Technologies</span></h2>
    <div class="skills-container">
      <div class="skill-category"><h3>Frontend</h3>
        <div class="skill"><span class="skill-name">HTML5<span>95%</span></span><div class="skill-bar"><div class="skill-level" data-level="95%"></div></div></div>
        <div class="skill"><span class="skill-name">CSS3<span>90%</span></span><div class="skill-bar"><div class="skill-level" data-level="90%"></div></div></div>
        <div class="skill"><span class="skill-name">JavaScript<span>80%</span></span><div class="skill-bar"><div class="skill-level" data-level="80%"></div></div></div>
      </div>
      <div class="skill-category"><h3>Backend</h3>
        <div class="skill"><span class="skill-name">Java<span>15%</span></span><div class="skill-bar"><div class="skill-level" data-level="15%"></div></div></div>
        <div class="skill"><span class="skill-name">PHP<span>85%</span></span><div class="skill-bar"><div class="skill-level" data-level="85%"></div></div></div>
        <div class="skill"><span class="skill-name">Python<span>45%</span></span><div class="skill-bar"><div class="skill-level" data-level="45%"></div></div></div>
      </div>
      <div class="skill-category"><h3>Networking</h3>
        <div class="skill"><span class="skill-name">Fundamental<span>85%</span></span><div class="skill-bar"><div class="skill-level" data-level="85%"></div></div></div>
        <div class="skill"><span class="skill-name">CCNA<span>70%</span></span><div class="skill-bar"><div class="skill-level" data-level="70%"></div></div></div>
        <div class="skill"><span class="skill-name">SOC<span>60%</span></span><div class="skill-bar"><div class="skill-level" data-level="60%"></div></div></div>
      </div>
      <div class="skill-category"><h3>Hardware</h3>
        <div class="skill"><span class="skill-name">Devices<span>90%</span></span><div class="skill-bar"><div class="skill-level" data-level="90%"></div></div></div>
        <div class="skill"><span class="skill-name">Assembly<span>75%</span></span><div class="skill-bar"><div class="skill-level" data-level="75%"></div></div></div>
        <div class="skill"><span class="skill-name">Server Mgmt<span>60%</span></span><div class="skill-bar"><div class="skill-level" data-level="60%"></div></div></div>
      </div>
      <div class="skill-category"><h3>Cyber Security</h3>
        <div class="skill"><span class="skill-name">Linux<span>70%</span></span><div class="skill-bar"><div class="skill-level" data-level="70%"></div></div></div>
        <div class="skill"><span class="skill-name">Network Security<span>60%</span></span><div class="skill-bar"><div class="skill-level" data-level="60%"></div></div></div>
        <div class="skill"><span class="skill-name">C Programming<span>55%</span></span><div class="skill-bar"><div class="skill-level" data-level="55%"></div></div></div>
      </div>
      <div class="skill-category"><h3>Tools</h3>
        <div class="skill"><span class="skill-name">Git<span>80%</span></span><div class="skill-bar"><div class="skill-level" data-level="80%"></div></div></div>
        <div class="skill"><span class="skill-name">VS Code<span>90%</span></span><div class="skill-bar"><div class="skill-level" data-level="90%"></div></div></div>
        <div class="skill"><span class="skill-name">PyCharm<span>55%</span></span><div class="skill-bar"><div class="skill-level" data-level="55%"></div></div></div>
      </div>
    </div>
  </section>

  <!-- Portfolio Section -->
  <section class="portfolio" id="portfolio">
    <h2>Latest <span>Projects</span></h2>
    <div class="portfolio-container">
      <div class="portfolio-item">
        <img src="images/ima3.png" alt="Jewellery Website">
        <div class="portfolio-info"><h3>Fullstack Jewellery Website</h3><p>MERN stack with Stripe integration, JWT auth, and real-time inventory.</p><a href="#"><i class="fas fa-external-link-alt"></i> View</a></div>
      </div>
      <div class="portfolio-item">
        <img src="images/img4.png" alt="Portfolio Builder">
        <div class="portfolio-info"><h3>Portfolio Builder</h3><p>Drag‑drop tool for developers to create stunning portfolio pages.</p><a href="#"><i class="fas fa-external-link-alt"></i> View</a></div>
      </div>
      <div class="portfolio-item">
        <img src="https://placehold.co/600x400/323946/0ef?text=AI+Chatbot" alt="AI Chatbot">
        <div class="portfolio-info"><h3>AI Support Chatbot</h3><p>Python + OpenAI API, deployed on cloud with a sleek React frontend.</p><a href="#"><i class="fas fa-external-link-alt"></i> Live Demo</a></div>
      </div>
    </div>
  </section>

  <!-- Certifications -->
  <section class="certifications" id="certifications">
    <h2><span>Certifications</span></h2>
    <div class="certifications-container">
      <div class="experience-item"><div class="experience-date"><i class="fas fa-award"></i></div><div class="experience-content"><div class="content"><h3>BACHELOR OF ARTS HONOURS IN GEOGRAPHY</h3><h4>SOUTH EASTERN UNIVERSITY OF SRI LANKA</h4></div><div class="cert-img"><img src="images/ime5.jpg" alt="Certificate"><div class="img-layer"><button onclick="openCertificateModal('images/img5.jpg')">View Certificate</button></div></div></div></div>
      <div class="experience-item"><div class="experience-date"><i class="fas fa-award"></i></div><div class="experience-content"><div class="content"><h3>FRONT-END WEB DEVELOPMENT</h3><h4>UNIVERSITY OF MORATUWA</h4><p>Successfully Completed The Front-End Web Development online Learning Programme</p></div><div class="cert-img"><img src="images/img7.jpg.png" alt="Frontend Cert"><div class="img-layer"><button onclick="openCertificateModal('images/img6.pdf')">View Certificate</button><button onclick="openCertificateModal('images/img6.pdf')">View Transcript</button></div></div></div></div>
      <div class="experience-item"><div class="experience-date"><i class="fas fa-award"></i></div><div class="experience-content"><div class="content"><h3>WEB DESIGN FOR BEGINNERS</h3><h4>UNIVERSITY OF MORATUWA</h4><p>successfully completed the Web Design For Beginners</p></div><div class="cert-img"><img src="images/img8.jpg.png" alt="Web Design"><div class="img-layer"><button onclick="openCertificateModal('images/img23.pdf')">View Certificate</button></div></div></div></div>
      <div class="experience-item"><div class="experience-date"><i class="fas fa-award"></i></div><div class="experience-content"><div class="content"><h3>AI FUNDAMENTALS WITH IBM SKILLS BUILD</h3><h4>CISCO NETWORKING ACADEMY</h4><p>Successfully Completed AI Fundamentals With IBM Skills Build</p></div><div class="cert-img"><img src="images/img9.png" alt="AI Cert"><div class="img-layer"><button onclick="openCertificateModal('images/img24.pdf')">View Certificate</button></div></div></div></div>
      <div class="experience-item"><div class="experience-date"><i class="fas fa-award"></i></div><div class="experience-content"><div class="content"><h3>DATA SECURITY POSTURE MANAGEMENT FUNDAMENTALS</h3><h4>SECURITI</h4><p>Successfully Completed the Data Security Posture Management Fundamentals</p></div><div class="cert-img"><img src="images/img10.png" alt="DSPM"><div class="img-layer"><button onclick="openCertificateModal('images/img22.pdf')">View Certificate</button></div></div></div></div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="contact" id="contact">
    <h2>Contact <span>Me!</span></h2>
    <form id="contactForm">
      <div class="input-box"><input type="text" id="fullName" placeholder="Full Name" required><input type="email" id="emailAddress" placeholder="Email Address" required></div>
      <div class="input-box"><input type="number" id="mobileNumber" placeholder="Mobile Number"><input type="text" id="emailSubject" placeholder="Email Subject"></div>
      <textarea id="yourMessage" cols="30" rows="10" placeholder="Your Message"></textarea>
      <input type="submit" value="Send Message" class="btn">
    </form>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="footer-container">
      <div class="footer-column"><h3 class="footer-title">ISMAIL</h3><p>Tech enthusiast passionate about problem-solving, continuous learning, and creating innovative solutions.</p><div class="social-icons"><a href="https://www.facebook.com/share/199ub1b9PB/"><i class="fa-brands fa-facebook-f"></i></a><a href="https://github.com/ismail9148"><i class="fa-brands fa-github"></i></a><a href="https://www.instagram.com/accounts/onetap/"><i class="fa-brands fa-instagram"></i></a><a href="https://www.linkedin.com/in/yoosuf-ismail-056705282"><i class="fa-brands fa-linkedin-in"></i></a></div></div>
      <div class="footer-column"><h4 class="footer-title">Solutions</h4><div class="footer-links"><a href="#">Web Development</a><a href="#">Graphic Design</a><a href="#">Software Development</a></div></div>
      <div class="footer-column"><h4 class="footer-title">Company</h4><div class="footer-links"><a href="#about">About Us</a><a href="#">Research</a><a href="#">Careers</a><a href="#">News</a></div></div>
      <div class="footer-column"><h4 class="footer-title">Contact Info</h4><p><i class="fas fa-map-marker-alt"></i> Ninthavur, Sri Lanka</p><p><i class="fas fa-phone"></i> +94 752005028</p><p><i class="fas fa-envelope"></i> yoosufismail.it@gmail.com</p></div>
    </div>
    <div class="foot-note"><div class="footer-text"><p>Copyright © 2026 by <a href="#">ISMAIL</a> | All Rights Reserved</p></div></div>
  </footer>

  <!-- Certificate Modal -->
  <div class="modal" id="certificate-modal">
    <div class="modal-content"><button class="modal-close" onclick="closeModal()">×</button><div class="modal-body" id="modal-body"></div></div>
  </div>

  <script>
    // ----- Skill Bar Animation on Scroll -----
    const skillLevels = document.querySelectorAll('.skill-level');
    function animateSkills() {
      skillLevels.forEach(bar => {
        const level = bar.getAttribute('data-level');
        if (level && bar.style.width !== level) {
          const rect = bar.getBoundingClientRect();
          if (rect.top < window.innerHeight - 50) {
            bar.style.width = level;
          }
        }
      });
    }
    window.addEventListener('scroll', animateSkills);
    window.addEventListener('load', animateSkills);

    // ----- Modal Functions for Certificates -----
    window.openCertificateModal = function(src) {
      const modal = document.getElementById('certificate-modal');
      const modalBody = document.getElementById('modal-body');
      if (src.match(/\.(jpeg|jpg|png|gif|webp)$/i)) {
        modalBody.innerHTML = `<img src="${src}" alt="Certificate">`;
      } else if (src.match(/\.pdf$/i)) {
        modalBody.innerHTML = `<iframe src="${src}" title="Certificate PDF"></iframe>`;
      } else {
        modalBody.innerHTML = `<p>Preview not available.</p>`;
      }
      modal.style.display = 'flex';
    };
    window.closeModal = function() {
      const modal = document.getElementById('certificate-modal');
      modal.style.display = 'none';
      document.getElementById('modal-body').innerHTML = '';
    };
    // Close modal on outside click
    window.onclick = function(e) {
      const modal = document.getElementById('certificate-modal');
      if (e.target === modal) closeModal();
    };

    // ----- Read More Toggle -----
    const readMoreBtn = document.getElementById('readMoreBtn');
    const moreText = document.getElementById('moreText');
    if (readMoreBtn) {
      readMoreBtn.addEventListener('click', () => {
        moreText.classList.toggle('show');
        readMoreBtn.textContent = moreText.classList.contains('show') ? 'Read Less' : 'Read More';
      });
    }

    // ----- Active Link Highlight on Scroll -----
    const sections = document.querySelectorAll('section');
    const navLinks = document.querySelectorAll('nav a');
    window.addEventListener('scroll', () => {
      let current = '';
      sections.forEach(section => {
        const sectionTop = section.offsetTop - 150;
        const sectionHeight = section.clientHeight;
        if (pageYOffset >= sectionTop && pageYOffset < sectionTop + sectionHeight) {
          current = section.getAttribute('id');
        }
      });
      navLinks.forEach(link => {
        link.classList.remove('active');
        if (link.getAttribute('href').slice(1) === current) {
          link.classList.add('active');
        }
      });
    });

    // ----- Contact Form Submission (Demo Alert) -----
    const contactForm = document.getElementById('contactForm');
    if (contactForm) {
      contactForm.addEventListener('submit', function(e) {
        e.preventDefault();
        alert('Thank you! Your message has been sent. (Demo)');
        this.reset();
      });
    }
  </script>
</body>
</html>
