<div align="center">

<br/>

<h1>GigPulse India</h1>

<p>Interactive Workforce BI Dashboard — Indian Gig Economy Intelligence</p>

<br/>

[![Platform](https://img.shields.io/badge/Platform-Google%20Apps%20Script-4285F4?style=for-the-badge&logo=google&logoColor=white)](#)
[![Charts](https://img.shields.io/badge/Charts-Google%20Charts%20API-e67e00?style=for-the-badge&logo=google&logoColor=white)](#)
[![AI](https://img.shields.io/badge/AI-Google%20Gemini-1a7f37?style=for-the-badge&logo=google&logoColor=white)](#)
[![Workers](https://img.shields.io/badge/Dataset-50%2C000%20Gig%20Workers-0057B8?style=for-the-badge&logoColor=white)](#)
[![License](https://img.shields.io/badge/License-MIT-c0392b?style=for-the-badge&logoColor=white)](#)

<br/>

> A free, lightweight, interactive Business Intelligence web app built entirely on **Google Workspace** — transforming raw survey data of **50,000 Indian gig economy workers** into an executive-ready dashboard with live filters, KPI metrics, interactive charts, and AI-generated insights.

<br/>

---

<div align="center">

### 🔴 [→ Open Live Dashboard ←](https://script.google.com/macros/s/AKfycbx8kE4xGE5e4aQ5hQHYjPbmOppAizPdLJ3lPpwkcuE7boa_-S4EdPXMKTZ7zWsDB94u/exec)

**Click to explore 50,000 gig workers — live, filtered, interactive.**

💡 *If you see a Google Drive error, open in an incognito / private window — it will load correctly.*

</div>

---

<br/>

```
No servers. No costs. No raw data exposure. Just insight.
```

<br/>

---

</div>

## 💡 Why a Web App Instead of a Standard Sheet?

```
┌─────────────────────────────────────────────────────────────────────────┐
│                        DESIGN DECISIONS                                 │
├──────────────────────────────┬──────────────────────────────────────────┤
│  💸  100% Free & Hosted      │  Runs inside the browser via Google      │
│                              │  Apps Script — zero server costs          │
├──────────────────────────────┼──────────────────────────────────────────┤
│  🔒  Data Security           │  End-users interact with the dashboard   │
│                              │  URL — raw Sheet data stays hidden        │
├──────────────────────────────┼──────────────────────────────────────────┤
│  📱  Mobile-Friendly UI      │  Bootstrap 5 — clean on laptops,         │
│                              │  tablets, and smartphones                 │
├──────────────────────────────┼──────────────────────────────────────────┤
│  ⚡  Instant Filtering       │  Slice by Year, City Tier, Platform,     │
│                              │  Gender, Migrant Status — no reloads     │
└──────────────────────────────┴──────────────────────────────────────────┘
```

---

## Executive Highlights & Design Decisions

| Pillar | Strategic Decision | Technical Architecture |
| :--- | :--- | :--- |
| **Zero-Cost Compute** | 100% Free Cloud Execution | Runs in-browser via Google Apps Script V8 and client-side vector memory. |
| **Sub-5ms Slicing** | Instant Reactive UI | Compact 15-dimension vector payload eliminates server roundtrips upon filter changes. |
| **Tier-1 Aesthetics** | Strategy Consulting UX | Minimalist dark masthead, crisp typographic hierarchy, and custom editorial chart palettes. |
| **Enterprise Security** | Protected Underlying Assets | End-users interact solely through the Web App UI; underlying Google Sheet assets remain private. |

---

## 📸 Executive Dashboard Showcase

### 1. Strategic Segmentation & Executive KPIs
*Features the masthead status box, 8-filter parameter console, 6 executive summary KPI tiles, and the AI-driven macro signals feed.*
![Executive Overview & Filter Console](01_executive_overview_filters_kpi.png)

### 2. Financial Architecture & Platform Dynamics
*Tracks historical net income trajectories (2023–2026), platform sector concentration donuts, operator compensation benchmarks, and state-level earnings indices.*
![Financial Trajectory & Sector Share](02_financial_trajectory_sector_analytics.png)

### 3. Labor Intensity & Workload Economics
*Visualizes daily operating duration vs. monthly take-home realization via high-density subsampled scatter plots and multi-year tenure indexing.*
![Labor Intensity Scatter & Tenure Index](03_labor_intensity_scatter_distribution.png)

### 4. Vulnerability & Social Protection Analysis
*Breaks down reported worker grievances, social security/insurance penetration rates, annual injury exposure, and educational attainment profiles.*
![Grievance Analytics & Social Protection](04_welfare_grievances_social_protection.png)

---

## Analytical Matrix & Features

* **Multivariate Filter Console (8 Live Dimensions):**
  * **Platform Sector:** Food Delivery, Ride Hailing, Logistics, Quick Commerce, Home Services, Bike Taxi, Hyperlocal
  * **Experience Tier:** Entry-level ($\le 1\text{y}$), Associate ($1\text{--}3\text{y}$), Mid-Senior ($3\text{--}5\text{y}$), Senior ($5\text{--}8\text{y}$), Lead / Veteran ($8\text{y}+$)
  * **State / Geography:** 17 Indian States & Union Territories
  * **City Tier:** Tier 1, Tier 2, Tier 3 Urban Clusters
  * **Migrant Status:** Inter/Intra-state Migrant vs. Native Resident Workers
  * **Gender:** Male, Female demographic splits
  * **Vehicle / Asset Type:** Motorcycle, Car (EMI/Loan), Auto-rickshaw, Scooter, E-bike, Mini truck
  * **Social Security Coverage:** No coverage, Platform PF, ESI, State Welfare Schemes
* **Executive Summary Benchmarks:** Real-time updates for active cohort size, median net take-home, average earnings, average daily operating hours, 12-month injury rate, and uninsured ratio.
* **Macroeconomic Signal Feed:** Dynamically generated bullet insights analyzing top-earning states, dominant platform sectors, vulnerability ratios, and segment elasticity.

---
---

### Raw Data Source
> The underlying Google Sheet (`india_gig_economy_platform_workers_v2`) — end-users never see this; they only interact with the dashboard URL.

![Data Source](data-source.png)

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      GOOGLE SHEET                           │
│              raw_data tab · 2,500+ rows                     │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                    Code.gs (Backend)                        │
│   getData() · Fetch · Clean · Normalize · Return JSON       │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                  JavaScript.html (Client)                   │
│   Filter Logic · Google Charts API · Dynamic Redraws        │
└──────────┬────────────────────────────────────┬────────────┘
           │                                    │
           ▼                                    ▼
┌──────────────────────┐            ┌───────────────────────┐
│     Index.html       │            │       css.html        │
│  Navbar · Filters    │            │  KPI Cards · Layout   │
│  KPI Tiles · Charts  │            │  Gradients · Responsive│
└──────────────────────┘            └───────────────────────┘
```

**4 modular files — no framework overhead:**

| File | Role |
|:---|:---|
| `Code.gs` | Server-side — fetches, cleans, and normalizes Sheet data into JSON |
| `Index.html` | Main layout — navbar, filters, KPI tiles, chart containers |
| `JavaScript.html` | Client-side — filter actions and Google Charts rendering logic |
| `css.html` | Styling — KPI cards, gradients, responsive layout rules |

---

## 🚀 4-Step Deployment Guide

### Step 1 — Prepare Google Sheet
1. Create a Google Sheet and import `india_gig_economy_platform_workers_v2.csv`.
2. Confirm the header row contains standard fields: `worker_id`, `survey_year`, `platform_type`, `state`, `city_tier`, `monthly_net_income_inr`, etc.

### Step 2 — Open Apps Script
In Google Sheets, navigate to **Extensions** $\rightarrow$ **Apps Script**. Rename your project to `GigPulse-Executive-BI`.

### Step 3 — Add Project Files
Create 4 files matching the repository source:
* `Code.gs` *(Backend microservice & cache handlers)*
* `Index.html` *(Executive layout structure)*
* `css.html` *(Corporate design tokens & styling)*
* `JavaScript.html` *(In-memory computation & chart rendering)*

Save all files (`Ctrl + S` / `Cmd + S`).

### Step 4 — Deploy Web Application
1. Click **Deploy** $\rightarrow$ **New deployment**.
2. Select **Web app** (via the gear icon).
3. Set **Execute as** to `Me` and **Who has access** to `Anyone`.
4. Authorize Google Workspace permissions and access your live deployment URL.

Click **Deploy** → authorize permissions → open your live URL.

---

## 🤖 Built with Gemini AI

This project was engineered using **Google Gemini** as an AI technical co-pilot and strategy consultant—prompting, reviewing, benchmarking performance, and refining each architectural layer iteratively.

### Key Engineering Prompts Used

**1. High-Throughput Backend & Vector Serialization (`Code.gs`)**
> *"Act as an enterprise Google Apps Script architect. Optimize data ingestion for a 50,000-row Google Sheet dataset (`india_gig_economy_platform_workers_v2`). Avoid bulky JSON objects; serialize the exact 15 required analytical dimensions into compact vector arrays. Implement a 6-hour CacheService layer with chunking so initial load executes in under 2 seconds."*

**2. 0ms Client-Side In-Memory Engine (`JavaScript.html`)**
> *"Refactor the frontend to eliminate slow server roundtrips on filter changes. Load the 50,000-row vector matrix into browser memory on startup and write a sub-5ms JavaScript loop that filters across 8 dimensions (Platform Sector, Tenure Tier, State, City Tier, Migrant Status, Gender, Vehicle Type, Social Security) and recomputes all KPI aggregations instantly."*

**3. Strategy Consulting UI/UX Design System (`css.html` & `Index.html`)**
> *"Transform the UI from a generic dashboard into a Tier-1 strategy consulting portal (McKinsey/BCG executive style). Implement a dark corporate masthead (`#0A192F`), Inter & Plus Jakarta Sans typography, minimalist card elevation, custom editorial chart palettes (deep navy, strategic teal, warning amber, risk rose), and a clean executive signal feed."*

**4. Performance-Safe Data Visualization**
> *"Configure 10+ Google Charts (time-series lines, donuts, horizontal category rankings, and stacked bars). For the high-density work-intensity scatter plot (50k points), implement intelligent sub-sampling to 1,000 points to ensure smooth 60 FPS rendering without browser canvas freezing."*

---
*All generated code, memory allocations, and visual tokens were audited, validated, and tested against live 50,000-record benchmarks prior to production deployment.*

---

## 💻 Tech Stack

```
┌──────────────────────────────────────────────────────────────┐
│                     GIGPULSE TECH STACK                      │
├──────────────────────┬───────────────────────────────────────┤
│  Backend             │  Google Apps Script                   │
│  Frontend            │  Bootstrap 5, Google Charts API       │
│  AI Insights         │  Google Gemini                        │
│  Data Source         │  Google Sheets (raw_data tab)         │
│  Hosting             │  Google Apps Script Web App (free)    │
└──────────────────────┴───────────────────────────────────────┘
```

---

<div align="center">

*GigPulse India — Built on Google. Powered by Gemini. Free to deploy.*

<br/>

[![License: MIT](https://img.shields.io/badge/License-MIT-1a7f37?style=flat-square)](#)

</div>
