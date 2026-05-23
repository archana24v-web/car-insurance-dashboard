# 🛡️ PremiumLens — Auto Insurance Comparison Dashboard

An interactive single-page car insurance comparison dashboard comparing **6 major US carriers** with live premium calculations, discount stacking, and agent checklists.

## 🔗 Live Demo

> Enable GitHub Pages to get your public URL:
> `https://archana24v-web.github.io/car-insurance-dashboard/`

## 📦 Features

- **6 Carriers**: Geico, Progressive, State Farm, Allstate, Liberty Mutual, USAA
- **Live recalculation** on every input change
- **Profile inputs**: Age, state, vehicle class, mileage, credit tier, marital status, coverage level, accident/violation/DUI history
- **9 discount types**: Bundle, telematics, multi-vehicle, paperless/autopay, good student, loyalty, military, new car, anti-theft
- **Multiplicative discount stacking** (mirrors real underwriting math)
- **Age-25 milestone callout** — shows expected % rate drop and estimated savings
- **Ranked comparison table** with relative price bars
- **Per-carrier discount breakdown cards**
- **Discount matrix** — max published discounts across all carriers
- **12-item document checklist** (interactive, click to check off)
- **12-item agent question checklist** — questions to verify every eligible discount
- **Light + Dark mode**
- **Fully responsive** — works on mobile
- **No backend, no install** — pure HTML/CSS/JS, runs anywhere

## 🚀 How to Run

**Option 1 — Locally:**
```
Download index.html → double-click → opens in any browser
```

**Option 2 — GitHub Pages (free public URL):**
1. Go to repo **Settings → Pages**
2. Source: `Deploy from branch` → `main` → `/ (root)`
3. Save → wait ~2 min → your URL is live

## 📊 How the Model Works

Each carrier's 2025–26 US average base rate is multiplied through a transparent chain:

```
base × stateFactor × coverageLevel × ageMult × vehicleClass
     × mileage × maritalStatus × creditTier
     × accidentMult × violationMult × duiMult × yearsLicensedMult
```

Then discounts stack **multiplicatively** (not additively):
```
finalPrice = adjustedBase × (1 - disc1) × (1 - disc2) × ...
```

## ⚠️ Disclaimer

All estimates are directional only, based on published 2025–26 industry averages. Pull real quotes from at least 3 carriers before making any decisions. USAA is available only to military members, veterans, and their families.

## 🛠️ Built With

- Vanilla HTML/CSS/JavaScript — no frameworks, no dependencies
- Data sourced from Bankrate, NerdWallet, Insurify, LendingTree (2025–26)

---
*Built as a data engineering side project to demonstrate transparent insurance pricing models.*
