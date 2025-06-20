---
layout: null
title: "Portfolio"
permalink: /portfolio/
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>{{ page.title }}</title>
  <link rel="stylesheet" href="{{ site.baseurl }}/assets/main.css">
  <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
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

    .portfolio-section {
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

    .strategies-container {
      display: flex;
      flex-direction: column;
      gap: 2rem;
    }

    .strategy-card {
      background-color: #252526;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }

    .strategy-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 1.5rem;
    }

    .strategy-title {
      color: #4CAF50;
      font-size: 1.8rem;
      margin: 0;
    }

    .strategy-metrics {
      background-color: #2d2d2d;
      padding: 1rem;
      border-radius: 6px;
      min-width: 200px;
    }

    .metric {
      margin-bottom: 0.5rem;
    }

    .metric:last-child {
      margin-bottom: 0;
    }

    .metric-label {
      color: #d4d4d4;
      font-size: 0.9rem;
    }

    .metric-value {
      color: #4CAF50;
      font-weight: 600;
      font-size: 1.1rem;
    }

    .highlights {
      background-color: #2d2d2d;
      padding: 1.5rem;
      border-radius: 6px;
      margin-top: 1.5rem;
    }

    .highlights h4 {
      color: #4CAF50;
      margin-top: 0;
      margin-bottom: 1rem;
    }

    .highlights ul {
      list-style-type: none;
      padding: 0;
      margin: 0;
    }

    .highlights li {
      color: #d4d4d4;
      padding: 0.5rem 0;
      border-bottom: 1px solid #333;
    }

    .highlights li:last-child {
      border-bottom: none;
    }

    .performance-chart {
      background-color: #252526;
      padding: 2rem;
      border-radius: 8px;
      margin-top: 2rem;
    }

    .chart-title {
      color: #4CAF50;
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
    }

    .chart-legend {
      display: flex;
      gap: 2rem;
      margin-top: 1rem;
      justify-content: center;
    }

    .legend-item {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      color: #d4d4d4;
    }

    .legend-color {
      width: 20px;
      height: 20px;
      border-radius: 4px;
    }

    .usage-section {
      background-color: #252526;
      padding: 2rem;
      border-radius: 8px;
      margin-top: 2rem;
    }

    .usage-section h2 {
      color: #4CAF50;
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
    }

    .usage-section ul {
      list-style-type: none;
      padding: 0;
      margin: 0;
    }

    .usage-section li {
      color: #d4d4d4;
      padding: 0.5rem 0;
      border-bottom: 1px solid #333;
    }

    .usage-section li:last-child {
      border-bottom: none;
    }

    .contact-note {
      text-align: center;
      margin-top: 2rem;
      font-style: italic;
      color: #4CAF50;
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
      
      .portfolio-section {
        padding: 1rem;
        margin-top: 140px;
      }

      .strategy-header {
        flex-direction: column;
        gap: 1rem;
      }

      .strategy-metrics {
        width: 100%;
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
        <li><a href="{{ site.baseurl }}/portfolio" class="active">Portfolio</a></li>
        <li><a href="{{ site.baseurl }}/strategies-research">Strategies & Research</a></li>
        <li><a href="{{ site.baseurl }}/blog">Blog</a></li>
        <li><a href="{{ site.baseurl }}/support">Support</a></li>
      </ul>
    </div>
  </nav>

  <div class="portfolio-section">
    <div class="intro-section">
      <h1>Portfolio Overview</h1>
      <p>Explore how AuxiQuant's strategies perform across different markets and risk profiles. We present transparent, data-driven performance metrics for each portfolio we manage or simulate.</p>
    </div>

    <div class="strategies-container">
      <div class="strategy-card">
        <div class="strategy-header">
          <h2 class="strategy-title">1️⃣ Momentum Rotation Portfolio</h2>
          <div class="strategy-metrics">
            <div class="metric">
              <div class="metric-label">Market</div>
              <div class="metric-value">US Equities</div>
            </div>
            <div class="metric">
              <div class="metric-label">Type</div>
              <div class="metric-value">Simulated</div>
            </div>
            <div class="metric">
              <div class="metric-label">2024 YTD Return</div>
              <div class="metric-value">+18.7%</div>
            </div>
            <div class="metric">
              <div class="metric-label">Sharpe Ratio</div>
              <div class="metric-value">1.45</div>
            </div>
          </div>
        </div>
        <div class="highlights">
          <h4>Highlights:</h4>
          <ul>
            <li>Focused on top-performing sector ETFs</li>
            <li>Adaptive filters to exclude overheated assets</li>
            <li>Strong track record during trending markets</li>
          </ul>
        </div>
      </div>

      <div class="strategy-card">
        <div class="strategy-header">
          <h2 class="strategy-title">2️⃣ AI Sentiment Reversal Portfolio</h2>
          <div class="strategy-metrics">
            <div class="metric">
              <div class="metric-label">Market</div>
              <div class="metric-value">US Stocks & ETFs</div>
            </div>
            <div class="metric">
              <div class="metric-label">Type</div>
              <div class="metric-value">Backtested (2019–2024)</div>
            </div>
            <div class="metric">
              <div class="metric-label">Backtest CAGR</div>
              <div class="metric-value">22.3%</div>
            </div>
          </div>
        </div>
        <div class="highlights">
          <h4>Highlights:</h4>
          <ul>
            <li>Uses NLP-based AI to identify overreactions</li>
            <li>Pairs short-term sentiment spikes with technical indicators</li>
            <li>Excellent short-term alpha generator</li>
          </ul>
        </div>
      </div>

      <div class="strategy-card">
        <div class="strategy-header">
          <h2 class="strategy-title">3️⃣ Volatility Breakout System</h2>
          <div class="strategy-metrics">
            <div class="metric">
              <div class="metric-label">Market</div>
              <div class="metric-value">Crypto (BTC, ETH, SOL)</div>
            </div>
            <div class="metric">
              <div class="metric-label">Type</div>
              <div class="metric-value">Simulated (Paper Trading)</div>
            </div>
            <div class="metric">
              <div class="metric-label">2024 Sim Return (YTD)</div>
              <div class="metric-value">+34.2%</div>
            </div>
          </div>
        </div>
        <div class="highlights">
          <h4>Highlights:</h4>
          <ul>
            <li>Real-time volatility detection using deep learning</li>
            <li>Configurable for scalping or swing trading</li>
            <li>Built-in trailing stop and re-entry logic</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="performance-chart">
      <h2 class="chart-title">📈 Cumulative Performance Comparison</h2>
      <div id="performanceChart" style="width:100%; height:400px;"></div>
      <div class="chart-legend">
        <div class="legend-item">
          <div class="legend-color" style="background-color: #4CAF50;"></div>
          <span>Momentum Rotation</span>
        </div>
        <div class="legend-item">
          <div class="legend-color" style="background-color: #2196F3;"></div>
          <span>Sentiment Reversal</span>
        </div>
        <div class="legend-item">
          <div class="legend-color" style="background-color: #f44336;"></div>
          <span>Breakout System</span>
        </div>
      </div>
    </div>

    <div class="usage-section">
      <h2>💡 How to Use This Page</h2>
      <ul>
        <li>Track simulated vs. real-time performance</li>
        <li>Understand risk-reward tradeoffs</li>
        <li>Contact AuxiQuant to run custom simulations for their own use cases</li>
      </ul>
    </div>

    <p class="contact-note">📩 <em>Interested in building your own AI portfolio? Reach out at <a href="mailto:support@auxiquant.com">support@auxiquant.com</a></em></p>
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

  <script>
    // Sample data for the performance chart
    const dates = Array.from({length: 12}, (_, i) => {
      const date = new Date();
      date.setMonth(date.getMonth() - (11 - i));
      return date.toISOString().slice(0, 7);
    });

    const momentumData = {
      x: dates,
      y: [100, 105, 108, 112, 115, 118, 122, 125, 128, 132, 135, 118.7],
      name: 'Momentum Rotation',
      type: 'scatter',
      line: {color: '#4CAF50'}
    };

    const sentimentData = {
      x: dates,
      y: [100, 103, 107, 110, 114, 118, 122, 126, 130, 134, 138, 122.3],
      name: 'Sentiment Reversal',
      type: 'scatter',
      line: {color: '#2196F3'}
    };

    const breakoutData = {
      x: dates,
      y: [100, 102, 105, 108, 112, 116, 120, 125, 130, 135, 140, 134.2],
      name: 'Breakout System',
      type: 'scatter',
      line: {color: '#f44336'}
    };

    const layout = {
      paper_bgcolor: 'rgba(0,0,0,0)',
      plot_bgcolor: 'rgba(0,0,0,0)',
      font: {
        color: '#d4d4d4'
      },
      xaxis: {
        gridcolor: '#333',
        zerolinecolor: '#333'
      },
      yaxis: {
        gridcolor: '#333',
        zerolinecolor: '#333',
        tickformat: '.0f'
      },
      margin: {
        l: 50,
        r: 50,
        b: 50,
        t: 50,
        pad: 4
      },
      showlegend: false
    };

    Plotly.newPlot('performanceChart', [momentumData, sentimentData, breakoutData], layout);
  </script>
</body>
</html> 