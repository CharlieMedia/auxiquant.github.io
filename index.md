---
layout: home
title: ""
---

<nav class="main-nav">
  <div class="nav-container">
    <div class="logo">
      <img src="/assets/images/logo.png" alt="AuxiQuant Logo">
    </div>
    <ul class="nav-links">
      <li><a href="/" class="active">Home</a></li>
      <li><a href="/markets">Markets</a></li>
      <li><a href="/trading">Trading</a></li>
      <li><a href="/portfolio">Portfolio</a></li>
      <li><a href="/strategies">Strategies</a></li>
      <li><a href="/research">Research</a></li>
      <li><a href="/blog">Blog</a></li>
      <li><a href="/support">Support & Contact</a></li>
    </ul>
  </div>
</nav>

<div class="hero">
  <div class="hero-content">
    <h1>Welcome to AuxiQuant</h1>
    <h2>The Future of Quant Intelligence</h2>
    <p>Combining AI, quantitative analytics, and domain expertise for smarter trading decisions</p>
    <div class="cta-buttons">
      <a href="/trading" class="cta-primary">Start Trading</a>
      <a href="/about" class="cta-secondary">Learn More</a>
    </div>
  </div>
</div>

<div class="about-section">
  <h2>About AuxiQuant</h2>
  <p>AuxiQuant is shaping the future of quant intelligence!</p>
  <p>We combine the power of advanced AI, quantitative analytics, and domain expertise to help organizations make smarter, faster, and more precise decisions. Whether in finance, operations, strategy, or research, our solutions are designed to amplify intelligence and unlock deeper insights from complex data.</p>
  <p>With a foundation in innovation and a commitment to clarity, AuxiQuant empowers businesses and teams to move beyond guesswork — into a future where data-driven intelligence leads the way.</p>
  <p class="tagline">AuxiQuant: The Future of Quant Intelligence.</p>
</div>

<style>
body {
  background-color: #1e1e1e;
  color: #d4d4d4;
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}

.main-nav {
  background-color: #252526;
  box-shadow: 0 2px 4px rgba(0,0,0,0.3);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo img {
  height: 60px;
  width: auto;
  margin: 0.5rem 0;
}

.nav-links {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
  gap: 1.5rem;
  flex-wrap: wrap;
  justify-content: center;
}

.nav-links a {
  text-decoration: none;
  color: #d4d4d4;
  font-weight: 500;
  padding: 0.5rem 0.8rem;
  border-radius: 4px;
  transition: all 0.3s ease;
  font-size: 0.95rem;
  white-space: nowrap;
}

.nav-links a:hover {
  color: #4CAF50;
  background-color: #2d2d2d;
}

.nav-links a.active {
  color: #4CAF50;
  background-color: #2d2d2d;
}

.hero {
  background-color: #252526;
  padding: 5rem 2rem 4rem;
  text-align: center;
  margin-bottom: 2rem;
  border-bottom: 1px solid #333;
  width: 95%;
  max-width: 1800px;
  margin-left: auto;
  margin-right: auto;
  box-sizing: border-box;
}

.hero-content {
  width: 100%;
  margin: 0 auto;
  padding: 0;
}

.hero h1 {
  font-size: 3.5rem;
  color: #4CAF50;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.hero h2 {
  font-size: 2.2rem;
  color: #d4d4d4;
  margin-bottom: 1rem;
  font-weight: 500;
}

.hero p {
  color: #d4d4d4;
  font-size: 1.3rem;
  line-height: 1.6;
  margin-bottom: 1.5rem;
  width: 90%;
  margin-left: auto;
  margin-right: auto;
}

.cta-buttons {
  margin-top: 2rem;
  display: flex;
  gap: 1rem;
  justify-content: center;
}

.cta-primary, .cta-secondary {
  padding: 0.8rem 2rem;
  border-radius: 4px;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s ease;
}

.cta-primary {
  background-color: #4CAF50;
  color: #ffffff;
}

.cta-secondary {
  background-color: #2d2d2d;
  color: #4CAF50;
  border: 2px solid #4CAF50;
}

.cta-primary:hover {
  background-color: #45a049;
}

.cta-secondary:hover {
  background-color: #333;
}

.about-section {
  width: 95%;
  max-width: 1800px;
  margin: 0 auto;
  padding: 3rem 2rem;
  background-color: #252526;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  box-sizing: border-box;
}

.about-section h2 {
  color: #4CAF50;
  margin-bottom: 1.5rem;
  font-size: 2.2rem;
}

.about-section p {
  color: #d4d4d4;
  line-height: 1.6;
  margin-bottom: 1rem;
  font-size: 1.1rem;
  width: 90%;
  margin-left: auto;
  margin-right: auto;
}

.tagline {
  font-weight: bold;
  color: #4CAF50;
  font-size: 1.2em;
  margin-top: 2rem;
}

@media (max-width: 1600px) {
  .hero, .about-section {
    width: 98%;
  }
}

@media (max-width: 1400px) {
  .hero, .about-section {
    width: 98%;
  }
}

@media (max-width: 1200px) {
  .hero, .about-section {
    width: 98%;
  }
}

@media (max-width: 768px) {
  .nav-container {
    flex-direction: column;
    gap: 1rem;
  }
  
  .nav-links {
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
    width: 100%;
  }
  
  .nav-links a {
    width: 100%;
    text-align: center;
    padding: 0.8rem;
  }
  
  .hero, .about-section {
    width: 98%;
    padding: 4rem 1rem 3rem;
  }
  
  .hero-content {
    padding: 0;
  }
  
  .hero h1 {
    font-size: 2.5rem;
  }
  
  .hero h2 {
    font-size: 1.8rem;
  }
  
  .hero p, .about-section p {
    width: 100%;
  }
  
  .about-section h2 {
    font-size: 1.8rem;
  }
  
  .cta-buttons {
    flex-direction: column;
  }
}
</style> 