#  Professional Work — Secret Weapon Trading Solution Pvt. Ltd.

> **1000+ commits across private company repositories (Aug 2025 – Present)**
> All source code is proprietary and confidential. This repository documents the work, architecture, and technical achievements from my time at Secret Weapon Trading Solution.

---

##  About Me

```
Name     →  Akanksha Shivaji Powar
Role     →  Software Developer
Company  →  Secret Weapon Trading Solution Pvt. Ltd.
Period   →  August 2025 – Present
Stack    →  Python · FastAPI · Next.js · Redis · WebSockets · InfluxDB · PostgreSQL
Location →  Kolhapur, Maharashtra, India
```

🌐 **Portfolio:** [portfolio.fenyxn.in](https://portfolio.fenyxn.in)
📧 **Email:** powarakanksha9188@gmail.com
🔗 **LinkedIn:** [linkedin.com/in/akanksha-powar](https://linkedin.com/in/akanksha-powar)

---

##  Company Overview

**Secret Weapon Trading Solution Pvt. Ltd.** is a fintech company building real-time market data platforms, trading automation systems, and enterprise management tools. I joined as a Software Developer and have been the primary developer across multiple production systems.

---

##  Projects

### 1. SpaceTime — Real-Time Market Data Platform

> *The most technically complex project I've worked on. 5+ months of active development.*

**What it does:**
A microservices-based market data platform that ingests and processes **10,000+ ticks per second** from a live DTN market feed, computes custom Space-Time Indicators, and streams everything to a multi-chart frontend in real time.

**Key Technical Achievements:**
-  Replaced pandas with **NumPy vectorized arrays** — 10x computation speed improvement
-  Built **Redis Pub/Sub pipeline** for zero-latency inter-service communication
-  Designed **message batching** at the API Gateway (TradingView-style) to handle peak market load
-  Implemented **backpressure handling** to prevent system overload during high-frequency data bursts
-  Built **10,000-entry Redis buffer queue** to eliminate data loss under peak throughput
-  WebSocket **auto-reconnect with exponential backoff** for reliable client recovery
-  **Keycloak JWT auth** with token refresh — resolved race conditions with session locking

**Space-Time Reversal Indicator — 4 Versions:**
```
v1 → Intensity + adaptive buffer with CV scaling
v2 → Price + intensity + momentum confirmation  
v3 → Intensity + high/low timeframe trend + volume gate
v4 → EMA crossover + choppy market filter + volume spike confirmation
```
All versions tested live on market during peak hours. Adaptive buffer uses 80:20 ratio with 1000-tick window.

**Frontend Charts (TradingView Lightweight Charts):**
- Smoothing line chart (SMA / EMA / ZLMA)
- Candlestick chart with OHLCV + multi-timeframe support
- Volume chart with intensity bars
- Spike detection chart
- Marker chart with reversal signals
- ZLMA volume series overlay (purple line)

**Tech Stack:**
`Python` `FastAPI` `Redis Pub/Sub` `InfluxDB v3` `PostgreSQL` `NumPy` `WebSockets` `Next.js` `TypeScript` `TradingView Lightweight Charts` `Socket.IO` `Keycloak` `Docker` `GitHub Actions` `Nginx` `AWS`

**Timeline:** Nov 2025 – May 2026 | **Commits:** 400+

---

### 2. TrendEdge — Automated Trading Platform

> *Zerodha-integrated trading automation with live order execution and forward testing.*

**What it does:**
A real-time trading automation system that auto-logs into Zerodha at 8:30 AM, subscribes to live KiteTicker WebSocket feeds, computes Supertrend + ATR signals, and executes equity and options orders automatically.

**Key Technical Achievements:**
-  **Auto-login at exactly 8:30 AM** — access token saved to PostgreSQL and reused to skip redundant logins
-  **Multi-symbol concurrent subscription** with one-by-one rate-limited registration
-  **Forward test mode** with virtual capital — simulates execution without real orders
-  **Option chain integration** — auto strike selection based on spot price and user-defined levels
-  **Auto expiry detection** for FNO derivatives
-  **Margin validation** before every order placement
-  **Trade logs** saved to PostgreSQL with IST timestamps
-  Live tested on Equity, FNO, and Options segments

**Indicators Built:**
```
Supertrend   →  Computed via StockStats library
ATR          →  Average True Range for volatility
Volume EMA   →  Spike detection for reversal confirmation
```

**Frontend:**
- Real-time dashboard with market time + open positions
- Trade logs page (live + historical, IST formatted)
- Portfolio page — holdings from Zerodha DEMAT
- Candlestick animation landing page with Keycloak SSO
- Fully responsive across mobile, tablet, desktop

**Tech Stack:**
`Python` `FastAPI` `Zerodha KiteTicker` `StockStats` `Socket.IO` `Next.js` `TypeScript` `PostgreSQL` `Keycloak` `Docker`

**Timeline:** Mar 2026 – Present | **Commits:** 250+

---

### 3. Company Management System — Enterprise Platform

> *Full internal operations platform — from invoicing to HR to email automation.*

**What it does:**
A comprehensive enterprise platform covering project tracking, client/developer invoicing, GST billing, salary slips, finance reports, expense management, and HR — with a desktop app (Electron) and email automation.

**Modules Built:**

| Module | Features |
|--------|----------|
| **Projects & Tasks** | Calendar scheduling, task assignment via Keycloak, comments, status tracking |
| **Invoicing** | GST/LUT invoices for Indian + foreign clients, PDF generation, preview mode |
| **Finance Reports** | GST sales, TDS, client payments, developer payments — all with filters |
| **HR & Payroll** | Employee management, salary slips with PF/ESIC auto-calculation |
| **Desktop App** | Electron wrapper — cross-platform native desktop application |
| **Email Automation** | Automated emails on invoice creation, project updates, task assignments |

**Key Technical Achievements:**
-  **GST/LUT invoice system** for both Indian clients (CGST/SGST) and foreign clients (LUT)
-  **PDF generation** with logo, signature, rupee symbol using canvas library
-  **Salary slip automation** — PF and ESIC auto-calculated from working days
-  **Developer profit ratio** — auto-adjusts to sum to 100% across developers
-  **Keycloak Google Login** — SSO with role-based groups
-  **Electron desktop app** — full feature parity with the web version
   **Fully responsive** mobile layout across all 15+ pages

**Tech Stack:**
`Python` `FastAPI` `Next.js` `TypeScript` `Electron` `PostgreSQL` `Keycloak` `Google OAuth` `PDF Canvas` `FullCalendar` `Email Automation`

**Timeline:** Apr 2026 – Present | **Commits:** 200+

---

### 4. Laboratory Management System — Clinical Lab Platform

> *Live deployed system for clinical labs — patient management with WhatsApp automation.*

**What it does:**
A full-stack lab management platform for clinical labs to manage patients, tests, billing, and reports — with automated WhatsApp notifications and Keycloak RBAC.

**Key Features:**
-  Patient registration, test tracking, report delivery
-  Automated WhatsApp notifications (Node.js microservice)
-  Keycloak group-based multi-lab RBAC
-  5 Docker containers — FastAPI, Next.js, PostgreSQL, Keycloak, WhatsApp
-  GitHub Actions CI/CD + Nginx + Certbot SSL on GCP

🔗 **Live:** [lab.fenyxn.in](https://lab.fenyxn.in)

**Tech Stack:**
`Python` `FastAPI` `Next.js` `PostgreSQL` `Keycloak` `WhatsApp API` `Node.js` `Docker` `GCP` `GitHub Actions`

---

### 5. Delta Exchange Automation

> *Multi-symbol crypto trading automation with Telegram alerts.*

**What it does:**
Automated trading system on Delta Exchange — executes orders across multiple crypto instruments simultaneously based on strategy signals, with real-time Telegram notifications.

**Key Features:**
- ₿ Multi-symbol concurrent execution
- ₿ Delta Exchange WebSocket for live market data
- ₿ Telegram Bot for trade alerts and P&L reports
- ₿ Async event loop for time-sensitive order execution

**Tech Stack:**
`Python` `FastAPI` `WebSockets` `Delta Exchange API` `Telegram Bot API`

---

## 🛠️ Full Tech Stack

```
Languages      →  Python · TypeScript · JavaScript · SQL
Backend        →  FastAPI · WebSockets · REST APIs · Microservices
Frontend       →  Next.js · React · TradingView Charts · Electron
Databases      →  PostgreSQL · Redis · InfluxDB v3
Auth           →  Keycloak · JWT · Google OAuth · RBAC
DevOps         →  Docker · GitHub Actions · Nginx · Certbot · SSH
Cloud          →  AWS · GCP · Linux Server Management
Fintech        →  Zerodha API · Delta Exchange · KiteTicker WebSocket
Indicators     →  Supertrend · ATR · SMA · EMA · ZLMA · NumPy
Messaging      →  Redis Pub/Sub · Socket.IO · Telegram Bot · WhatsApp API
```

---

## 📊 Work Timeline

```
Aug 2025   →  Joined Secret Weapon Trading Solution
Nov 2025   →  Started SpaceTime market data platform
Jan 2026   →  Keycloak integration + production deployment
Feb 2026   →  OHLCV candle system + multi-timeframe support
Mar 2026   →  Space-Time Reversal Indicator (v1 → v4)
Mar 2026   →  TrendEdge Supertrend trading platform
Apr 2026   →  Company Management System + Electron app
Apr 2026   →  Laboratory Management System (live)
May 2026   →  Finance module · HR · Email automation
```

---

##  Links

| | |
|---|---|
|  Portfolio | [portfolio.fenyxn.in](https://portfolio.fenyxn.in) |
|  Live Project | [lab.fenyxn.in](https://lab.fenyxn.in) |
|  LinkedIn | [linkedin.com/in/akanksha-powar](https://linkedin.com/in/akanksha-powar) |
|  Email | powarakanksha9188@gmail.com |

---

<div align="center">

*All source code is proprietary to Secret Weapon Trading Solution Pvt. Ltd.*
*This repository exists solely to document my professional contributions.*

**⭐ For detailed project breakdowns, visit [portfolio.fenyxn.in](https://portfolio.fenyxn.in)**

</div>
