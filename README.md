# SankhyaGrid (सांख्य) v0.5.0

**Grid Intelligence Platform for Indian DISCOMs**

Last-mile distribution visibility, AI-driven insights, and a telemetry marketplace — from 220kV substation to individual homes, EVs, and solar inverters.

👉 **[Live Demo](https://gagandeepkukreja.github.io/SankhyaGrid/)**

---

## What It Does

SankhyaGrid fills a critical blind spot in India's power grid. While SCADA exists at the transmission level, there is near-zero digital visibility at the feeder, transformer, and consumer level — exactly where AT&C losses, outages, and DER chaos happen.

This platform provides:
- Real-time monitoring of every asset from substation to socket
- AI-powered fault detection, theft flagging, and overload prediction
- EV and solar DER management with curtailment controls
- A built-in telemetry device marketplace connecting DISCOMs to Indian suppliers

---

## Features (17 built)

### Grid Visibility
- **GIS Network View** — Leaflet + CARTO Voyager map with real Chhattisgarh coordinates. Toggleable asset layers, connection lines, click-to-inspect.
- **Real-Time Monitoring** — Feeder table (V, I, kW, PF, losses, sparklines) + transformer card grid. 5-second refresh.
- **Network Overview** — KPI strip, single-line diagram, AT&C loss monitor with theft flags.
- **Asset Analytics** — 48 half-hourly consumption bars, solar generation overlay, solar/grid split by period, net demand curve.

### AI & Prediction
- **Alerts & Fault Detection** — Critical/Warning/AI Insight tiers. Overload, voltage, thermal, theft, EV, weather types.
- **Predictive Modelling** — Weather-linked forecasts, EV load prediction, transformer overload risk table, historical EV heatmap.
- **EV Charging Spike Detection** — Flags sudden consumption spikes as potential unregistered EV charging with confidence %.
- **AI Document Extraction** — Upload PDF/JPG/PNG/DOCX. Simulated OCR + LLM pipeline extracts structured asset data.

### DER & Control
- **DER Management** — EV curtail/enable toggles, solar monitoring, energy balance visualization.
- **Industry / IPP Monitoring** — Real CG industries (SAIL, BALCO, NTPC) with contract demand, solar capacity, load profiles.

### Marketplace
- **Telemetry Marketplace** — 24 devices from Indian/global suppliers (Genus, HPL, Secure, L&T, Schneider, ABB, Siemens, BEL, Delta, Exicom). Search, filter by asset type, prices in ₹, REQUEST INFO with state tracking.
- **Per-Asset Recommendations** — Click any asset on the map to see top 3 matching telemetry devices in the sidebar.

### Platform
- **Sector Mode Selector** — Generation / Transmission / Distribution. Distribution is fully built; others show coming-soon with planned capabilities.
- **Hindi / English Toggle** — 60+ translated UI strings. हिं/EN button in header.
- **Light / Dark Theme** — Full 20+ token color system. Warm industrial palette (default light).
- **Mobile Responsive** — All grids collapse, tables scroll, GIS stacks vertically.

---

## Real Grid Data

Built on actual Chhattisgarh electricity infrastructure data:

| Asset Type | Count | Source |
|---|---|---|
| 220/132kV Transmission Substations | 4 | CSPTCL Grid Map |
| 33/11kV Distribution Substations | 20 | KUSUM Component-A |
| 11kV/0.4kV Distribution Transformers | 30 | Modelled (250-630 kVA) |
| Consumer Clusters | 12 | Modelled (180-600 HH) |
| Industries / IPP | 8 | Real CG industries |
| EV Chargers & Charge Parks | 8 | Modelled |
| Solar Parks & Rooftop (KUSUM) | 7 | KUSUM scheme |
| **Total Assets on Map** | **89** | |

**Divisions covered:** Raipur, Korba, Durg/Bhilai, Bilaspur

**Real substations:** Kara, Seonikala, Mana, Dharsiwa, Saragaon, Tilda, Korba East (BALCO), Katghora, Chhuri, Pali, Kartala, Supela, Gondwara, Rajnandgaon, Bemetara, Bilaspur City, Mungeli, Pendra Road, Takhatpur

**Real industries:** Bhilai Steel Plant (SAIL, 45 MW), BALCO Aluminium (Vedanta, 25 MW), NTPC Korba STPS (2600 MW), ACC Cement Jamul, Siltara Industrial Park, Raipur Urla Industrial Area, Bilaspur Rice & Agro Mills, Rajnandgaon Textile Cluster

---

## Tech Stack

**Current (MVP Demo)**
- React 18 via CDN (single `index.html`, zero build step)
- Leaflet + CARTO Voyager tiles for GIS
- Simulated real-time data (5s refresh cycle)
- GitHub Pages hosting

**Production Roadmap**
- FastAPI + Celery + Redis (backend)
- InfluxDB (time-series telemetry) + PostgreSQL (metadata)
- MQTT Broker (Mosquitto) for device ingestion
- Sarvam AI for Hindi OCR + LLM extraction
- PyPSA for grid simulation
- Yotta / CtrlS sovereign Indian cloud deployment
- Kubernetes K3s + Docker

---

## Design

**Warm Industrial** — purposefully distinct from generic AI-generated dashboards.

- **Typography:** DM Sans (clean, professional)
- **Palette:** Off-white (#f7f5f2) base, dark navy (#1a2744) header, terracotta (#c4532a) alerts, steel teal (#2a7d8c) data, sage green (#6b8f71) healthy, gold (#d4a843) warnings
- **Map:** CARTO Voyager light tiles (professional GIS look)
- **Cards:** White with subtle shadows and left accent borders (no neon glow)

---

## Deploy

Single `index.html` file. Enable GitHub Pages on the `main` branch — that's it.

---

## Revenue Model

| Stream | Model | Indicative Pricing |
|---|---|---|
| Platform SaaS | Per asset/month | ₹500-2K/asset |
| Predictive Module | Premium add-on | ₹2-5L/month |
| Theft Detection | Outcome-based | 5-10% of recovered |
| AI Document Extraction | Per document | ₹2-5/doc |
| Marketplace Listings | Annual fee | ₹50K-2L/year |
| Lead Generation | Per qualified lead | ₹500-2K/lead |
| EV Detection Alerts | Subscription | ₹1-3L/month |

---

## Roadmap

- [x] MVP dashboard with 17 features
- [x] Real Chhattisgarh grid data (CSPTCL + KUSUM)
- [x] Telemetry marketplace (24 devices)
- [x] Hindi/English bilingual UI
- [x] Warm industrial visual redesign
- [ ] Production backend (FastAPI + InfluxDB + MQTT)
- [ ] CSPDCL pilot (Raipur division)
- [ ] Real telemetry integration
- [ ] Sarvam AI Hindi OCR pipeline
- [ ] PyPSA grid simulation layer
- [ ] Generation & Transmission modules
- [ ] Multi-state DISCOM onboarding

---

with ❤️ made in India
