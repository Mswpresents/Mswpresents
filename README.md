<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>「 ┈━═.•°αηкυѕн уα∂αν°•.═━┈ 」</title>

  <link href="https://fonts.googleapis.com/css2?family=Sacramento&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <link rel="stylesheet" href="https://unpkg.com/aos@2.3.1/dist/aos.css" />

  <style>
    :root {
      --primary-color: #ffd700;
      --primary-glow: rgba(255, 215, 0, 0.5);
      --bg-dark: #0d1b2a;
      --bg-light: #1b263b;
      --text-color: #ffffff;
      --card-bg: rgba(27, 38, 59, 0.8);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: radial-gradient(ellipse at bottom, var(--bg-light) 0%, var(--bg-dark) 100%);
      color: var(--text-color);
      overflow-x: hidden;
      perspective: 1000px;
      min-height: 100vh;
    }

    ::-webkit-scrollbar {
      width: 8px;
    }
    
    ::-webkit-scrollbar-track {
      background: var(--bg-dark);
    }
    
    ::-webkit-scrollbar-thumb {
      background: var(--primary-color);
      border-radius: 10px;
      transition: all 0.3s;
    }
    
    ::-webkit-scrollbar-thumb:hover {
      background: var(--primary-glow);
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    h2 {
      font-family: 'Sacramento', cursive;
      color: var(--primary-color);
      font-size: 3.5em;
      text-shadow: 0 0 15px var(--primary-color);
      margin: 2rem 0;
      text-align: center;
    }

    .header {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
    }

    .header-content {
      text-align: center;
      z-index: 2;
    }

    .profile-wrapper {
      margin: 30px auto;
      perspective: 1500px;
      width: 220px;
      height: 220px;
    }

    .profile-card {
      width: 100%;
      height: 100%;
      position: relative;
      transform-style: preserve-3d;
      transition: transform 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    }

    .profile-wrapper:hover .profile-card {
      transform: rotateY(180deg);
    }

    .profile-front, .profile-back {
      position: absolute;
      width: 100%;
      height: 100%;
      backface-visibility: hidden;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      transform-style: preserve-3d;
    }

    .profile-front {
      background: radial-gradient(circle at 30% 30%, var(--bg-light), var(--bg-dark));
      border: 4px solid var(--primary-color);
      box-shadow: 
        0 0 30px var(--primary-glow),
        inset 0 0 20px var(--primary-color);
      animation: float 6s ease-in-out infinite;
    }

    .profile-front img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%;
      transition: all 0.5s;
    }

    .profile-back {
      background: radial-gradient(circle at 70% 70%, var(--bg-light), var(--bg-dark));
      border: 4px solid var(--primary-color);
      transform: rotateY(180deg);
      box-shadow: 
        0 0 30px var(--primary-glow),
        inset 0 0 20px var(--primary-color);
      padding: 20px;
      flex-direction: column;
    }

    .profile-back p {
      color: var(--primary-color);
      font-size: 16px;
      margin-bottom: 12px;
      font-family: 'Sacramento', cursive;
      font-weight: bold;
    }

    .profile-social {
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .profile-social a {
      color: var(--text-color);
      font-size: 24px;
      transition: all 0.3s;
    }

    .profile-social a:hover {
      color: var(--primary-color);
      transform: scale(1.3) translateY(-5px);
      filter: drop-shadow(0 0 8px var(--primary-glow));
    }

    @keyframes float {
      0% { 
        transform: translateY(0) rotate(0deg); 
      }
      50% { 
        transform: translateY(-15px) rotate(2deg); 
      }
      100% { 
        transform: translateY(0) rotate(0deg); 
      }
    }

    .typing {
      margin: 30px auto;
      text-align: center;
      position: relative;
      z-index: 2;
    }

    .typing img {
      filter: drop-shadow(0 0 8px var(--primary-glow));
      max-width: 100%;
    }

    .social-icons {
      text-align: center;
      margin: 40px 0;
      transform-style: preserve-3d;
    }

    .social-icons a {
      margin: 0 15px;
      font-size: 32px;
      color: var(--text-color);
      transition: all 0.3s;
      display: inline-block;
    }

    .social-icons a:hover {
      color: var(--primary-color);
      transform: translateY(-15px) rotateY(30deg);
      text-shadow: 0 15px 30px var(--primary-glow);
    }

    .stats-section {
      text-align: center;
      padding: 80px 0;
      perspective: 1500px;
    }

    .stats-container {
      display: flex;
      flex-direction: column;
      gap: 60px;
      max-width: 800px;
      margin: 0 auto;
    }

    .stat-card {
      position: relative;
      transform-style: preserve-3d;
      transition: transform 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      padding: 10px;
      border-radius: 16px;
      background: rgba(13, 27, 42, 0.5);
      backdrop-filter: blur(5px);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
    }

    .stat-card::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: 16px;
      padding: 2px;
      background: linear-gradient(45deg, transparent, var(--primary-color), transparent);
      -webkit-mask: 
        linear-gradient(#fff 0 0) content-box, 
        linear-gradient(#fff 0 0);
      -webkit-mask-composite: xor;
      mask-composite: exclude;
      z-index: -1;
    }

    .stat-card img {
      border-radius: 12px;
      width: 100%;
      display: block;
      transition: all 0.6s;
      transform-style: preserve-3d;
      filter: drop-shadow(0 10px 20px rgba(0, 0, 0, 0.3));
    }

    .stat-card:hover {
      transform: translateY(-10px);
    }

    .stat-card:hover img {
      transform: scale(1.02) translateZ(20px);
      filter: drop-shadow(0 15px 30px rgba(0, 0, 0, 0.4));
    }

    .section-divider {
      width: 80%;
      height: 2px;
      margin: 60px auto;
      background: linear-gradient(to right, transparent, var(--primary-color), transparent);
      position: relative;
      overflow: visible;
    }

    .section-divider::before {
      content: '✧';
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: var(--bg-dark);
      padding: 0 20px;
      color: var(--primary-color);
      font-size: 1.5em;
    }

    .profile-views {
      margin: 80px 0;
      text-align: center;
      perspective: 1500px;
    }

    .profile-views img {
      border-radius: 10px;
      padding: 10px 20px;
      background: rgba(27, 38, 59, 0.7);
      box-shadow: 0 0 30px rgba(255, 215, 0, 0.2);
      transform-style: preserve-3d;
      transition: all 0.5s;
      border: 1px solid var(--primary-color);
    }

    .profile-views img:hover {
      transform: scale(1.05) translateZ(20px);
      box-shadow: 0 0 40px rgba(255, 215, 0, 0.4);
    }

    .glow {
      text-shadow: 0 0 15px var(--primary-color);
      animation: pulse 3s infinite;
    }

    @keyframes pulse {
      0% { text-shadow: 0 0 15px var(--primary-color); }
      50% { text-shadow: 0 0 25px var(--primary-color), 0 0 40px var(--primary-glow); }
      100% { text-shadow: 0 0 15px var(--primary-color); }
    }

    .parallax-bg {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: -1;
    }

    .star {
      position: absolute;
      background-color: #ffffff;
      border-radius: 50%;
      filter: drop-shadow(0 0 6px rgba(255, 255, 255, 0.8));
    }

    .shooting-star {
      position: absolute;
      width: 4px;
      height: 4px;
      border-radius: 50%;
      background: linear-gradient(45deg, var(--primary-color), white);
      filter: drop-shadow(0 0 10px var(--primary-color));
      animation: shooting 8s linear infinite;
      opacity: 0;
    }

    .shooting-star::before {
      content: '';
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 50px;
      height: 1px;
      background: linear-gradient(90deg, var(--primary-color), transparent);
      right: 1px;
    }

    @keyframes shooting {
      0% {
        transform: translate(0, 0) rotate(315deg);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      20% {
        transform: translate(-100px, 100px) rotate(315deg);
        opacity: 0;
      }
      100% {
        transform: translate(-100px, 100px) rotate(315deg);
        opacity: 0;
      }
    }

    @keyframes twinkle {
      0%, 100% { opacity: 0.2; transform: scale(0.8); }
      50% { opacity: 1; transform: scale(1.2); }
    }

    @media (max-width: 768px) {
      h2 {
        font-size: 2.8em;
      }
      
      .social-icons a {
        margin: 0 10px;
        font-size: 28px;
      }
    }

    @media (max-width: 480px) {
      h2 {
        font-size: 2.2em;
      }
      
      .profile-wrapper {
        width: 180px;
        height: 180px;
      }
      
      .social-icons a {
        margin: 0 8px;
        font-size: 24px;
      }
    }
  </style>
</head>
<body>
  <div class="parallax-bg" id="stars"></div>

  <div class="header">
    <div class="header-content">
      <h2 data-aos="fade-down" data-aos-duration="1500">──「 ┈━═.•°αηкυѕн уα∂αν°•.═━┈ 」──</h2>

      <div class="profile-wrapper" data-aos="zoom-in" data-aos-duration="1200">
        <div class="profile-card">
          <div class="profile-front">
            <img src="https://i.ibb.co/VYGLLrSC/Chat-GPT-Image-Apr-5-2025-10-50-19-PM.png" alt="Ankush Yadav"
                onerror="this.onerror=null;this.src='https://i.ibb.co/VYGLLrSC/Chat-GPT-Image-Apr-5-2025-10-50-19-PM.png';" />
          </div>
          <div class="profile-back">
            <p>Connect with me</p>
            <div class="profile-social">
              <a href="https://instagram.com/lt.ankush" target="_blank"><i class="fab fa-instagram"></i></a>
              <a href="https://telegram.me/Coder_ankushBot" target="_blank"><i class="fab fa-telegram"></i></a>
              <a href="https://github.com/Mswpresents" target="_blank"><i class="fab fa-github"></i></a>
              <a href="mailto:contact@ankushyadav.com" target="_blank"><i class="fas fa-envelope"></i></a>
            </div>
          </div>
        </div>
      </div>

      <div class="typing" data-aos="fade-up" data-aos-delay="300">
        <img src="https://readme-typing-svg.demolab.com?font=Sacramento&color=FFD700&size=30&center=true&vCenter=true&width=550&lines= My+Name+is;Ankush+Yadav;He/him;Computer+Engineering+Student;Indian+Frontend+Dev;NDA+Lover+:3;Power+Metal+Lover+%3C3;function+findQuestion(42)" alt="Typing Animation">
      </div>

      <div class="social-icons" data-aos="fade-up" data-aos-delay="500">
        <a href="https://instagram.com/lt.ankush" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
        <a href="https://telegram.me/Coder_ankushBot" target="_blank" aria-label="Telegram"><i class="fab fa-telegram"></i></a>
        <a href="https://github.com/Mswpresents" target="_blank" aria-label="GitHub"><i class="fab fa-github"></i></a>
      </div>
    </div>
  </div>

  <div class="section-divider" data-aos="fade-in"></div>

  <div class="stats-section container">
    <h2 class="glow" data-aos="fade-up">💜 GitHub •••</h2>
    
    <div class="stats-container">
      <div class="stat-card" data-aos="fade-right" data-aos-delay="200" data-aos-duration="1000">
        <img src="https://github-readme-stats.vercel.app/api?username=Mswpresents&hide=prs&count_public=true&show_icons=true&theme=algolia" alt="GitHub Stats">
      </div>
      
      <div class="stat-card" data-aos="fade-left" data-aos-delay="400" data-aos-duration="1000">
        <img src="https://github-readme-streak-stats.herokuapp.com?user=Mswpresents&theme=tokyonight" alt="Streak Stats">
      </div>
      
      <div class="stat-card" data-aos="fade-right" data-aos-delay="600" data-aos-duration="1000">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mswpresents&layout=compact&theme=tokyonight" alt="Top Languages">
      </div>
      
      <div class="stat-card" data-aos="fade-left" data-aos-delay="800" data-aos-duration="1000">
        <img src="https://github-stats-alpha.vercel.app/api/?username=Mswpresents&cc=000&tc=fff&ic=fff&bc=000" alt="GitHub Details">
      </div>
      
      <div class="stat-card" data-aos="zoom-in" data-aos-delay="1000" data-aos-duration="1000">
        <img src="https://github-profile-trophy.vercel.app/?username=Mswpresents&theme=darkhub" alt="GitHub Trophies">
      </div>
    </div>
  </div>
  
  <div style="margin: 200px 0;"></div>
  
  <div class="profile-views" data-aos="fade-up" data-aos-duration="2000">
    <h2 class="glow">👀 Profile Views</h2>
    <img src="https://profile-counter.glitch.me/Mswpresents/count.svg" alt="Visitor Count" data-aos="zoom-in">
  </div>

  <div class="section-divider" data-aos="fade-in"></div>

  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script>
    AOS.init({
      duration: 1200,
      once: false,
      mirror: true,
      anchorPlacement: 'top-center',
      easing: 'ease-out-cubic'
    });

    function createStarryBackground() {
      const starsContainer = document.getElementById('stars');
      const starCount = 200;
      const shootingStarCount = 5;
      
      for (let i = 0; i < starCount; i++) {
        const star = document.createElement('div');
        star.className = 'star';
        
        const size = Math.random() * 3;
        star.style.width = `${size}px`;
        star.style.height = `${size}px`;
        star.style.left = `${Math.random() * 100}%`;
        star.style.top = `${Math.random() * 100}%`;
        
        star.style.animation = `twinkle ${3 + Math.random() * 4}s infinite ${Math.random() * 5}s`;
        
        starsContainer.appendChild(star);
      }
      
      for (let i = 0; i < shootingStarCount; i++) {
        const shootingStar = document.createElement('div');
        shootingStar.className = 'shooting-star';
        
        shootingStar.style.left = `${Math.random() * 100}%`;
        shootingStar.style.top = `${Math.random() * 50}%`;
        
        shootingStar.style.animationDelay = `${Math.random() * 15}s`;
        
        starsContainer.appendChild(shootingStar);
      }
    }
    
    createStarryBackground();
    
    window.addEventListener('scroll', function() {
      const scrolled = window.pageYOffset;
      const stats = document.querySelectorAll('.stat-card');
      const stars = document.querySelectorAll('.star');
      
      stats.forEach((stat, index) => {
        const speed = 0.05 + (index * 0.01);
        stat.style.transform = `translateY(${scrolled * speed}px) rotateX(${scrolled * 0.01}deg)`;
      });
      
      stars.forEach((star, index) => {
        if (index % 3 === 0) {
          const speed = 0.02;
          const x = scrolled * speed * (index % 2 === 0 ? 1 : -1);
          star.style.transform = `translateX(${x}px)`;
        }
      });
    });
  </script>
</body>
</html>
