RENZO’S LAB V21 — COMPLETE GALAXY TERMINAL

This package preserves the full V19.1 dashboard and its two inline JavaScript blocks.
It restores the Netlify project configuration and the Binance/Bybit relay function
from V18, and moves the exact same embedded galaxy background into its own file.
The smaller V20 rewrite was NOT substituted for the original dashboard.

GITHUB / NETLIFY FILES — upload ALL of these to the ROOT of a new GitHub repo:
  index.html
  galaxy-background.webp
  netlify.toml
  netlify/functions/binance.js

To deploy on Netlify:
1. Connect the GitHub repo with Netlify > Add new project > Import an existing project.
2. Set Base directory empty, Build command empty, Publish directory: .
3. Deploy the project. Netlify should pick up netlify.toml and the functions folder.
4. Check https://YOUR-SITE.netlify.app/.netlify/functions/binance?symbol=BTCUSDT&period=5m
   Result should be JSON. The relay may report unavailable metrics if public APIs
   are blocked or unavailable; it never fabricates missing exchange data.

The dashboard displays public market information, not private wallet attribution.
Open interest alone cannot identify whether new positions are longs or shorts.
Signals are informational and do not predict trades with guaranteed accuracy.
No private API credentials are included. Do not upload secrets to GitHub.

BUILD CHECKS: HTML structure and both inline JS scripts parsed; serverless
function syntax checked; Netlify path and archive contents verified. Browser
render checks are offline and cannot prove live API availability. Live Netlify
provisioning, every third-party feed, and signal accuracy remain unverified.
