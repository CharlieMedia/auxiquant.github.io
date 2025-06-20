---
layout: null
title: "Blog"
permalink: /blog/
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>{{ page.title }}</title>
  <link rel="stylesheet" href="{{ site.baseurl }}/assets/main.css">
  <style>
    body {
      background-color: #1e1e1e;
      color: #d4d4d4;
      margin: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
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
      max-width: 1400px;
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

    .blog-section {
      padding: 2rem;
      max-width: 1400px;
      width: 98%;
      margin: 100px auto 2rem;
      flex: 1;
    }

    .intro-section {
      background-color: #252526;
      padding: 2rem;
      border-radius: 8px;
      margin-bottom: 2rem;
      text-align: center;
      font-size: 1.2rem;
      line-height: 1.6;
      color: #d4d4d4;
    }

    .posts-section {
      background-color: #252526;
      padding: 2rem;
      border-radius: 8px;
      margin-bottom: 2rem;
    }

    .posts-section h2 {
      color: #4CAF50;
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
    }

    .post-list {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .post-item {
      padding: 1.5rem;
      margin-bottom: 1.5rem;
      background-color: #2d2d2d;
      border-radius: 6px;
      transition: transform 0.3s ease;
    }

    .post-item:hover {
      transform: translateY(-2px);
    }

    .post-item:last-child {
      margin-bottom: 0;
    }

    .post-item h3 {
      margin: 0 0 0.5rem 0;
    }

    .post-item h3 a {
      color: #4CAF50;
      text-decoration: none;
      font-size: 1.4rem;
    }

    .post-item h3 a:hover {
      text-decoration: underline;
    }

    .post-meta {
      color: #888;
      font-size: 0.9rem;
      margin-bottom: 1rem;
    }

    .post-excerpt {
      color: #d4d4d4;
      line-height: 1.6;
    }

    .topics-section {
      background-color: #252526;
      padding: 2rem;
      border-radius: 8px;
      margin-bottom: 2rem;
    }

    .topics-section h2 {
      color: #4CAF50;
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
    }

    .topics-list {
      list-style: none;
      padding: 0;
      margin: 0;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1rem;
    }

    .topic-item {
      background-color: #2d2d2d;
      padding: 1rem;
      border-radius: 6px;
      color: #d4d4d4;
    }

    .contribute-section {
      background-color: #252526;
      padding: 2rem;
      border-radius: 8px;
      margin-bottom: 2rem;
      text-align: center;
    }

    .contribute-section h2 {
      color: #4CAF50;
      font-size: 1.8rem;
      margin-bottom: 1rem;
    }

    .contribute-section p {
      color: #d4d4d4;
      margin-bottom: 1rem;
    }

    .contribute-section a {
      color: #4CAF50;
      text-decoration: none;
    }

    .contribute-section a:hover {
      text-decoration: underline;
    }

    .notification {
      text-align: center;
      color: #4CAF50;
      font-style: italic;
      margin-top: 2rem;
    }

    .site-footer {
      background-color: #252526;
      padding: 2rem 0;
      margin-top: auto;
    }

    .footer-content {
      max-width: 1400px;
      margin: 0 auto;
      padding: 0 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .footer-text {
      color: #d4d4d4;
      margin: 0;
    }

    .footer-links {
      display: flex;
      gap: 2rem;
    }

    .footer-link {
      color: #d4d4d4;
      text-decoration: none;
      transition: color 0.3s ease;
    }

    .footer-link:hover {
      color: #4CAF50;
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
      
      .blog-section {
        padding: 1rem;
        margin-top: 140px;
      }

      .topics-list {
        grid-template-columns: 1fr;
      }

      .footer-content {
        flex-direction: column;
        text-align: center;
      }
    }
  </style>
</head>
<body>
  <nav class="main-nav">
    <div class="nav-container">
      <div class="logo">
        <img src="{{ site.baseurl }}/assets/images/logo.png" alt="AuxiQuant Logo">
      </div>
      <ul class="nav-links">
        <li><a href="{{ site.baseurl }}/">Home</a></li>
        <li><a href="{{ site.baseurl }}/markets-trading">Markets & Trading</a></li>
        <li><a href="{{ site.baseurl }}/portfolio">Portfolio</a></li>
        <li><a href="{{ site.baseurl }}/strategies-research">Strategies & Research</a></li>
        <li><a href="{{ site.baseurl }}/blog" class="active">Blog</a></li>
        <li><a href="{{ site.baseurl }}/support">Support</a></li>
      </ul>
    </div>
  </nav>

  <div class="blog-section">
    <div class="intro-section">
      <h1>📝 AuxiQuant Insights Blog</h1>
      <p>Welcome to the AuxiQuant Blog — where data meets domain expertise.</p>
      <p>Here, we share thoughts on quantitative trading, AI in finance, strategy design, risk models, and market trends. Each post offers actionable insights, grounded in data and experimentation.</p>
    </div>

    <div class="posts-section">
      <h2>📰 Recent Posts</h2>
      <ul class="post-list">
        {% for post in site.posts %}
          <li class="post-item">
            <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
            <div class="post-meta">
              <strong>{{ post.date | date: "%B %d, %Y" }}</strong> | {{ post.category }}
            </div>
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
          </li>
        {% endfor %}
      </ul>
    </div>

    <div class="topics-section">
      <h2>🧠 Topics We Cover</h2>
      <ul class="topics-list">
        <li class="topic-item">📈 Quant Strategy Design & Backtesting</li>
        <li class="topic-item">🧮 Machine Learning in Finance</li>
        <li class="topic-item">🧬 Large Language Models (LLMs) & Sentiment Analysis</li>
        <li class="topic-item">🔍 Macro Analysis & AI Predictions</li>
        <li class="topic-item">💼 Building Robust Trading Systems</li>
      </ul>
    </div>

    <div class="contribute-section">
      <h2>📤 Want to Contribute?</h2>
      <p>We're open to publishing quality guest posts related to quantitative finance, AI/ML, or markets. Reach out at <a href="mailto:support@auxiquant.com">support@auxiquant.com</a></p>
    </div>

    <p class="notification">🔔 <em>Stay tuned! New articles are published regularly.</em></p>
  </div>

  <footer class="site-footer">
    <div class="footer-content">
      <p class="footer-text">© 2024 AuxiQuant. All rights reserved.</p>
      <div class="footer-links">
        <a href="#" class="footer-link">Privacy Policy</a>
        <a href="#" class="footer-link">Terms of Service</a>
        <a href="#" class="footer-link">Contact Us</a>
      </div>
    </div>
  </footer>
</body>
</html> 