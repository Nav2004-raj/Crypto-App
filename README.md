# 🚀 Crypto Tracker

A responsive, real-time cryptocurrency tracking web app built with React. Browse live prices for 100+ coins, search and sort the market, and dive into a coin's 7-day price chart — all powered by the CoinGecko API.

**🔗 Live Demo:** [[crypto-app-mu-gold.vercel.app]
**💻 Repo:** [github.com/Nav2004-raj/Crypto-App]

---

## ✨ Features

- **Live market data** — pulls the top 100 coins by market cap from CoinGecko, auto-refreshing every 3 seconds
- **Search** — instantly filter coins by name or symbol
- **Sort** — by rank, name, price (asc/desc), 24h change, or market cap
- **Grid / List view toggle** — switch layouts based on preference
- **Coin detail page** — dedicated route per coin (`/coin/:id`) with:
  - Current price, 24h high/low, and % change
  - Interactive **7-day price chart** (Recharts `LineChart`)
  - Market cap, 24h volume, circulating supply, and total supply
- **Responsive design** — clean UI across mobile, tablet, and desktop
- **Client-side routing** — powered by React Router (`react-router` v7)

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| UI Library | React 19 |
| Build Tool | Vite |
| Styling | CSS |
| Routing | React Router v7 |
| Charts | Recharts |
| Data Source | [CoinGecko API] |
| Deployment | Vercel |
| Linting | ESLint |

---

## 📂 Project Structure

```
src/
├── api/
│   └── coinGecko.js       # API calls: fetchCryptos, fetchCoinData, fetchChartData
├── components/
│   └── CryptoCard.jsx     # Reusable coin card (grid/list item)
├── pages/
│   ├── Home.jsx           # Main listing page — search, sort, view toggle
│   └── CoinDetail.jsx     # Individual coin page with chart + stats
├── utils/
│   └── formatter.js       # Price & market cap formatting helpers
├── App.jsx                # Route definitions
└── main.jsx                # App entry point
```

---

## ⚙️ Getting Started

Clone the repo and install dependencies:

```bash
git clone https://github.com/Nav2004-raj/Crypto-App.git
cd Crypto-App
npm install
```

Run the dev server:

```bash
npm run dev
```

Build for production:

```bash
npm run build
```

No API key required — CoinGecko's public endpoints are used directly.

---

## 🧠 What I Learned Building This

- Structuring a multi-page React app with **React Router** and dynamic route params (`/coin/:id`)
- Managing multiple pieces of async state (loading, list, filters) with `useState` + `useEffect`
- Debouncing/polling live data safely with `setInterval` inside `useEffect` cleanup
- Transforming raw API data into chart-friendly formats for **Recharts**
- Writing small, reusable utility functions (`formatPrice`, `formatMarketCap`) instead of repeating logic across components

---

## 🚧 Possible Improvements

- Add pagination or infinite scroll instead of a fixed 100-coin fetch
- Debounce search input to reduce re-renders
- Add a favorites/watchlist feature with local storage
- Handle CoinGecko API rate limits with caching or a backend proxy
- Add unit tests for utility functions

---

## 📄 License

This project is open source and available for learning purposes.

---

## 🙋 Connect

Built by **Navneet** — frontend developer.
Feel free to reach out or check out more projects on [GitHub](https://github.com/Nav2004-raj).
