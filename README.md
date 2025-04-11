<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>HOME</title>

    <style>

/* WHOLE BODY */   

      body {
          margin: 0;
          background: linear-gradient(135deg, #348f50, #56b4d3); 
          color: white;
          font-family: 'Segoe UI', sans-serif;
          text-align: center;
          padding: 20px;
          animation: fadeIn 1s ease-in forwards;
          justify-content: center;
      }

      html {
          scroll-behavior: smooth;          
      }                    
                
                  /* Allow long words and elements to wrap and prevent overflow */
     
     .container-one hero fade-in {
        word-wrap: break-word;
        overflow-wrap: break-word;
        width: 100%;
        max-width: 100%;
        box-sizing: border-box;
   }   
      pre {
       white-space: pre-wrap; /* wrap long lines in <pre> */
       word-wrap: break-word;
  }

/* CONTAINER 1 */

      .container-one {
          background: rgba(0, 0, 0, 0.25);
          margin: 30px auto;
          border-radius: 16px;
          box-shadow: 0 10px 24px rgba(0, 0, 0, 0.4);
          padding: 25px;
          max-width: 900px;
          min-height: 10px;
          justify-content: center;
          align-items: center;
      }

      .container-one h1 {
          font-size: 3rem;
          color: #ffcc00;
          text-align: center;
          margin: 0;
      }

/* CONTAINER 2 */  

      .about {
          background: rgba(0, 0, 0, 0.25);
          margin: 30px auto;
          border-radius: 16px;
          box-shadow: 0 10px 24px rgba(0, 0, 0, 0.4);
          padding: 25px;
          max-width: 900px;
          min-height: 10px;
          justify-content: center;
          align-items: center;
      }

      .about h2 {
          color: #ffcc00;
      }

/* CONTAINER 3 */

      .project-container {
          display: flex;
          justify-content: center;
          gap: 20px; 
          flex-wrap: wrap;
      }

      .project-card {
          background: rgba(0, 0, 0, 0.25);
          width: 320px;
          padding: 20px;
          border-radius: 10px;
          text-align: center;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: space-between;
          transition: transform 0.3s ease, box-shadow 0.3s ease;
      }

      .project-card h2 {
          color: #FFD700;
          margin-bottom: 10px;
          font-weight: bold;
      }

      .project-card p {
          color: white;
          margin-bottom: auto;
          text-align: center;
          max-width: 90%;
      }

      .project-container h2 {
          color: #FFD700;
      }

      .project-card button:hover, .container-one button:hover {
      transform: scale(1.05);
    }

/* NAVI BAR */

      header {
          display: flex;
          justify-content: space-between;
          align-items: center;
          padding: 15px 10%;
          background: #333;
          color: white;
          animation: slideDown 0.8s ease-out;
      }

      nav {
          display: flex;
          gap: 20px;
      }

      nav a, nav button {
          background: none;
          border: none;
          font-size: 1.2rem;
          cursor: pointer;
          transition: color 0.3s;
          color: white;
          text-decoration: none;
      }

      nav a:hover, nav button:hover {
          color: #FFD700;
      }

/* BUTTONS STYLE */

      .hero button, .project-card button {
          background: #333;
          color: white;
          border: none;
          padding: 12px 25px;
          font-size: 1.2rem;
          margin-top: 20px;
          cursor: pointer;
          border-radius: 25px;
          transition: all 0.3s, transform 0.2s;
          font-weight: bold;
      }

/* LIGHT MODE / DARK MODE STYLE  */ 

      .toggle-switch {
          position: relative;
          width: 60px;
          height: 32px;
          border-radius: 999px;
          border: 1px solid white;
          background: linear-gradient(to right, #FFD700, #FFA500);
          cursor: pointer;
          transition: background 0.3s;
          display: flex;
          align-items: center;
          padding: 0 5px;
      }

      .toggle-thumb {
          position: absolute;
          width: 28px;
          height: 28px;
          border-radius: 50%;
          background: white;
          display: flex;
          align-items: center;
          justify-content: center;
          font-size: 16px;
          top: 2px;
          left: 2px;
          transition: all 0.5s ease;
      }

      .toggle-switch.dark {
          background: linear-gradient(to right, #2a2a2a, #1a1a1a);
      }

      .toggle-switch.dark .toggle-thumb {
          left: 40px;
          background: #111;
          color: white;
      }

/* LIGHT/DARK MODE COLOR CHANGE */     

      body.dark-mode {
          background: black;
      }

      body.dark-mode .container-one,
      body.dark-mode .project-card,
      body.dark-mode .about {
          background: black; 
          border: 1px solid white;
          box-shadow: 9px 9px 14px rgba(233, 233, 233, 0.3);
      }

/* EFFECTS */     

      .fade-in {
          opacity: 0;
          transform: translateY(20px);
          transition: opacity 0.8s ease, transform 0.8s ease;
      }

      .fade-in.visible {
          opacity: 1;
          transform: translateY(0);
      }

      @keyframes slideDown {
        from { transform: translateY(-100px); opacity: 0; }
        to { transform: translateY(0); opacity: 1; }
      }

    </style>
</head>
<body>
<!-- HEADER -->
<header>
  <nav>
    <a href="http://localhost:7700/HomePage.html">Home</a>
    <button onclick="scrollToSection('about')">About</button>
    <button onclick="scrollToSection('projects')">Projects</button>
    <button onclick="alert('Contact section not yet defined!')">Contact</button>
  </nav>
        <div class="toggle-switch" onclick="toggleMode(this)">
        <div class="toggle-thumb">☀️</div>
        </div>
</header>

  <div class="container-one hero fade-in">
    <h1>Welcome to CodeHek</h1>
    <p>We write code that works (most of the time). Student-built sites with 99.9% less caffeine crashes.</p>
    <button onclick="scrollToSection('about')">Explore Our Works</button>
  </div>

  <div class="about fade-in hero" id="about">

      <h2>About Us</h2>
    <p>We’re three web design students who accidentally formed a group and decided to roll with it.</p>
    <button onclick="location.href='01 - About Us Interface.html'">Meet the Brains</button>
  </div>

  <div class="container-one hero fade-in" id="projects">
    <div class="project-container">
      <h2>Our Projects</h2>
    </div>
    <div class="project-container fade-in">
      <div class="project-card">
          <h2>HTML</h2>
          <p>HTML is the standard language used to create and structure web pages.</p>
          <button onclick="location.href='02 - Html Interface.html'">Open</button>
      </div>
      <div class="project-card fade-in">
          <h2>CSS</h2>
          <p>CSS is a style sheet language used to style the layout, colors, and design of web pages.</p>
          <button onclick="location.href='02 - Css Interface.html'">Open</button>
      </div>
        <div class="project-card fade-in">
          <h2>JavaScript</h2>
          <p>JavaScript is used to create dynamic and interactive elements on web pages.</p>
          <button onclick="location.href='02 - Js interface.html'">Open</button>
      </div>
    </div>
  </div>

  <footer style="text-align: center;">
    <p><br>&copy; 2025 CodeHEK. All Rights Reserved.</p>
  </footer>

  <script>
    function toggleMode(el) {
      const body = document.body;
      const thumb = el.querySelector('.toggle-thumb');
      const isDark = body.classList.toggle('dark-mode');
      el.classList.toggle('dark', isDark);
      thumb.textContent = isDark ? '🌙' : '☀️';
      localStorage.setItem('theme', isDark ? 'dark' : 'light'); /* THIS LINE SAVES USERS CHOICE */  
    }

    function scrollToSection(id) {
      const section = document.getElementById(id);
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
      }
    }

    function scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    const faders = document.querySelectorAll('.fade-in');
    const options = {
      threshold: 0.2,
      rootMargin: "0px 0px -20px 0px"
    };

    const appearOnScroll = new IntersectionObserver((entries, observer) => {
      entries.forEach(entry => {
        if (!entry.isIntersecting) return;
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      });
    }, options);

    faders.forEach(fader => {
      appearOnScroll.observe(fader);
    });

/* THIS BLOCK SAVED THE THEME EVERY PAGE LOAD */ 

    window.addEventListener('DOMContentLoaded', () => {
      const theme = localStorage.getItem('theme');
      const toggle = document.querySelector('.toggle-switch');
      const thumb = toggle.querySelector('.toggle-thumb');
      if (theme === 'dark') {
        document.body.classList.add('dark-mode');
        toggle.classList.add('dark');
        thumb.textContent = '🌙';
      }
    });
  </script>

</body>
</html>

