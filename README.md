# 🛡 CYBERMON — Global SOC Dashboard

> **Real-time cybersecurity intelligence dashboard** — live CVE feeds, CISA KEV alerts, dark web leak tracking, nation-state APT monitoring, and active conflict zone cyber surge detection. Single HTML file. No server. No build step.

![Status](https://img.shields.io/badge/status-live-brightgreen) ![Sources](https://img.shields.io/badge/sources-8%20live%20feeds-blue) ![Deploy](https://img.shields.io/badge/deploy-GitHub%20Pages-black)

---

## 🌐 Live Demo

**[→ tenet-dev-ai.github.io/CYBERMON-/](https://tenet-dev-ai.github.io/CYBERMON-/)**

---

## 📸 Features

### 🗺 Live World Map
- D3.js + TopoJSON world map as the dominant centerpiece
- Real-time attack arc animations between source and target countries
- Color-coded threat dots: APT (red), Dark Web leaks (dark red), C2 botnets (orange), Critical CVEs (amber), CISA KEV (purple)
- Clickable countries open a full intelligence profile panel

### 📡 Live Data Sources
| Source | Data | Refresh |
|--------|------|---------|
| **NVD NIST** | Latest CVEs with CVSS scores | Every 1 hr |
| **CISA KEV** | Known Exploited Vulnerabilities catalog | Every 1 hr |
| **BleepingComputer** | Breaking security news | Every 10 min |
| **The Hacker News** | Threat intelligence | Every 10 min |
| **Krebs on Security** | Investigative reporting | Every 10 min |
| **SANS ISC** | Daily threat handlers | Every 10 min |
| **CISA Advisories** | Official US government alerts | Every 10 min |
| **Schneier on Security** | Security analysis | Every 10 min |
| **ransomware.live** | Dark web victim tracker | Every 5 min |

### 🧠 Three Intelligence Modes
- 🟢 **Beginner** — Plain English explanations on every threat event. No jargon.
- 🔵 **Professional** — Full CVE/KEV data, TTPs, IOCs, raw feed data.
- 🔴 **Warfare** — Nation-state APT, ICS/SCADA, critical infrastructure only.

### ⚔ Active Conflict Zone Tracker
Real-time cyber surge tracking for active conflicts:
- 🇺🇦 Ukraine–Russia War (Sandworm, APT28, Gamaredon)
- 🇮🇱 Israel–Hamas / Iran Proxy War (Charming Kitten, Moses Staff)
- 🇹🇼 China–Taiwan Tensions (Volt Typhoon, Salt Typhoon)
- 🇰🇵 DPRK Global Crypto Heists (Lazarus Group, Kimsuky)
- 🇧🇾 Russia–NATO Hybrid Warfare (Fancy Bear, GRU Unit 74455)
- 🇾🇪 Middle East Escalation (OilRig, MuddyWater)

### 🏛 Most-Targeted Organisations
Curated threat intelligence on high-value targets across:
- 🏥 Healthcare (Change Healthcare, NHS, Ascension Health)
- ⚡ Energy / ICS (Ukraine Power Grid, Colonial Pipeline, Saudi Aramco)
- 🏦 Financial (Bybit, SWIFT Network, ICBC)
- 🛡 Defence / Gov (SolarWinds, Microsoft Exchange, Pentagon)
- 📡 Telecom (AT&T/Verizon Salt Typhoon, Kyivstar, Viasat)

### 🌍 Country Intelligence Profiles
66-country threat database. Click any country on the map for:
- Cyber Exposure Index (0–100 live score)
- Origin / Target / APT+DW sub-scores
- Active APT intelligence from live RSS feeds
- Dark web leaks from ransomware.live
- CISA KEV vendor exposure
- Country profile (population, capital, region)
- IPv4 infrastructure data (BGPView)
- Expert intelligence brief

---

## 🛠 Tech Stack

| Component | Technology |
|-----------|-----------|
| World Map | D3.js v7 + TopoJSON |
| Attack Arcs | Canvas API animation loop |
| Fonts | Share Tech Mono · Rajdhani · Barlow Condensed |
| HTTP | XMLHttpRequest (no fetch — Android compatible) |
| CORS Proxies | corsproxy.io · codetabs.com · cors.eu.org |
| RSS Parsing | rss2json.com + DOMParser fallback |
| Layout | CSS Grid (desktop) · Flexbox (mobile) |
| Deployment | GitHub Pages / Vercel static |

**Zero dependencies to install. No npm. No build step. Pure HTML/CSS/JS.**

---

## 🚀 Deployment

### GitHub Pages (recommended)
1. Fork or upload `index.html` to a GitHub repo
2. Go to **Settings → Pages → Deploy from branch → main / root**
3. Your site is live at `https://username.github.io/repo-name/`

> ⚠️ Make sure the file is named **`index.html`** (all lowercase)

### Local
Just open `index.html` in any modern browser. Chrome recommended.

---

## 📱 Mobile Support

Fully responsive. On mobile (< 900px):
- Compact world map at top
- Bottom navigation bar: Intel · Vuln · News · Wars · Map · Diag
- ⚔ Wars & Orgs panel with conflict zone tracker
- All live feeds active

> On Android, open directly in Chrome for best CORS proxy performance.

---

## 🔧 Network Architecture

All data fetches use XMLHttpRequest with a 3-proxy fallback chain:

```
Direct request
  → corsproxy.io (confirmed ~48ms)
  → codetabs.com (confirmed ~856ms)
  → cors.eu.org  (confirmed ~1968ms)
```

RSS feeds use rss2json.com first, then raw XML via proxy + DOMParser.

Run the built-in **🔧 Diagnostics panel** to test all endpoints on your network.

---

## 🗂 Project Structure

```
CYBERMON-/
├── index.html      ← Entire application (single file)
└── README.md       ← This file
```

---

## 📊 Data Sources & Attribution

| Source | License / Terms |
|--------|----------------|
| NVD NIST | Public domain (US Government) |
| CISA KEV | Public domain (US Government) |
| ransomware.live | OSINT — publicly available dark web data |
| BleepingComputer | RSS feed — editorial content |
| The Hacker News | RSS feed — editorial content |
| Krebs on Security | RSS feed — editorial content |
| SANS ISC | RSS feed — editorial content |
| Schneier on Security | RSS feed — editorial content |
| BGPView | Free API |
| restcountries.com | Open Data |

---

## ⚠️ Disclaimer

CYBERMON is an **OSINT (Open Source Intelligence) tool**. All data displayed is sourced from publicly available feeds and APIs. Dark web victim data from ransomware.live is already publicly disclosed on threat actor leak sites. This tool is for **educational and defensive security awareness purposes only**.

---

## 👤 Author

**S3DFX-CYBER** 

[![GitHub](https://img.shields.io/badge/GitHub-S3DFX--CYBER-181717?logo=github)](https://github.com/S3DFX-CYBER)

---

*Built with real threat intelligence. Powered by open data. No keys required.*
