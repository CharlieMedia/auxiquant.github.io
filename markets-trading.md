---
layout: default
title: Markets & Trading
---

<div class="markets-trading-section">
  <h1>Markets & Trading</h1>
  
  <div class="section-container">
    <div class="markets-section">
      <h2>Market Overview</h2>
      <p>Access real-time market data, trends, and analysis across multiple asset classes:</p>
      <ul>
        <li>Stock Markets</li>
        <li>Cryptocurrency Markets</li>
        <li>Forex Markets</li>
        <li>Commodities</li>
      </ul>
    </div>

    <div class="trading-section">
      <h2>Trading Tools</h2>
      <p>Powerful trading tools and features to enhance your trading experience:</p>
      <ul>
        <li>Advanced Charting</li>
        <li>Technical Analysis</li>
        <li>Real-time Alerts</li>
        <li>Trading Signals</li>
      </ul>
    </div>
  </div>
</div>

<style>
.markets-trading-section {
  padding: 2rem;
  max-width: 2000px;
  width: 98%;
  margin: 0 auto;
}

.section-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.markets-section, .trading-section {
  background-color: #252526;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

h1 {
  color: #4CAF50;
  font-size: 2.5rem;
  margin-bottom: 2rem;
}

h2 {
  color: #4CAF50;
  font-size: 1.8rem;
  margin-bottom: 1rem;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  color: #d4d4d4;
  padding: 0.5rem 0;
  border-bottom: 1px solid #333;
}

li:last-child {
  border-bottom: none;
}

@media (max-width: 768px) {
  .markets-trading-section {
    padding: 1rem;
  }
  
  .section-container {
    grid-template-columns: 1fr;
  }
}
</style> 