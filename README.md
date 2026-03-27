# India EV Aftersales Strategy — Data-Driven Analysis

**Identifying ₹680 Crore in untapped value across India's EV service network**

Built by **Bhanu** | B.Tech Mechanical Engineering (Automotive) | Delhi Technological University 2027

---

## What This Project Is

India's EV market is growing fast — but the aftersales infrastructure (service centers, warranty management, spare parts) is not built to profitably support the fleet that's coming. This project applies a consulting-style hypothesis-driven framework to identify where OEMs are losing money and what they can do about it.

**Central question:** Can India's top EV OEMs improve aftersales EBITDA by 8–12 percentage points by FY27?

---

## 3 Key Findings

**Finding 1 — The market opportunity is massive and being missed**
India's EV aftersales TAM reaches ₹38,000 Crore by FY30 based on a 64 lakh cumulative fleet at ₹8,500 average annual spend per vehicle. OEMs are currently capturing less than 20% of this potential.

**Finding 2 — Tier-3 service centers are structurally unprofitable**
65% of Tier-3 service centers operate below breakeven every month. They need 145 jobs/month to cover fixed costs but receive only ~70 on average — a 2× gap that fixed infrastructure cannot bridge without a fundamental model change.

**Finding 3 — 32% of warranty spend is avoidable**
Battery (45%) and Power Electronics (40%) warranty claims are OTA-avoidable. An active software deflection program could save ₹70 Crore annually across the industry — Tesla already resolves 35–40% of service visits this way.

**Monte Carlo addition:** Ran 10,000 simulations on battery warranty reserves for a 50,000-vehicle fleet. P50 = ₹21.9 Cr | P90 = ₹28.9 Cr. Most OEMs over-provision by ~18–25% using global benchmarks instead of India-specific failure rates.

---

## 3 Recommendations

| Move | Action | Annual Impact | Timeline |
|---|---|---|---|
| 1 | Parts pricing correction on 40 high-velocity SKUs (8–12% increase) | ₹480 Cr/yr | 0–6 months |
| 2 | OTA software deflection program for Battery + Power Electronics | ₹200 Cr/yr | 6–18 months |
| 3 | Replace Tier-3 fixed centers with mobile service vans | ₹160 Cr/yr | 12–24 months |

**Combined: ₹680 Crore annual EBITDA improvement — 2.1× current estimated ₹320 Crore**

---

## Project Structure

```
ev-aftersales-india/
│
├── data/
│   ├── ev_sales.csv              # 10,000 EV sales records (simulated)
│   ├── service_centers.csv       # 200 centers × 36 months = 7,200 rows
│   └── warranty_claims.csv       # 50,000 warranty claim records
│
├── notebooks/
│   ├── 01_generate_data.ipynb    # Dataset generation with realistic benchmarks
│   ├── 02_market_sizing.ipynb    # TAM projection FY22–30
│   ├── 03_dealer_analysis.ipynb  # Profitability and breakeven modeling
│   ├── 04_warranty_analysis.ipynb# Component cost, OTA savings, climate analysis
│   └── 05_monte_carlo.ipynb      # Warranty reserve simulation (10,000 runs)
│
├── charts/
│   ├── chart1_market_growth.png  # EV fleet growth + aftersales TAM
│   ├── chart2_dealer_profit.png  # Scatter plot: profit vs throughput by tier
│   ├── chart3_warranty.png       # Warranty cost by component
│   ├── chart4_ota.png            # OTA-avoidable vs workshop spend
│   └── chart5_monte_carlo.png    # Monte Carlo distribution (P10/P50/P90)
│
├── deck/
│   └── EV_Aftersales_Strategy_Bhanu.pdf   # 10-slide consulting-style deck
│
└── README.md
```

---

## Data Sources & Assumptions

This project uses simulated data generated from publicly available benchmarks. All assumptions are documented in the notebooks.

| Dataset | Basis | Records |
|---|---|---|
| EV Sales Registry | VAHAN portal fleet data, SMEV 2023–24 market share | 10,000 |
| Service Center Operations | Indian auto service industry benchmarks (Maruti, Tata aftersales reports) | 7,200 |
| Warranty Claims | Global EV warranty data, Tesla/Rivian public disclosures, FAME-II incident data | 50,000 |

**Key assumptions:**
- Average annual aftersales spend per vehicle: ₹8,500 (conservative, based on Maruti aftersales revenue / fleet benchmarks)
- Service contribution margin: 45% (blended labor + parts, industry standard)
- Battery failure rate: mean 8%, std 2% (global EV data, adjusted for India climate)
- OTA avoidability rates: Battery 45%, Power Electronics 40%, others 12–20% (Tesla benchmark proxy)

---

## Tools Used

- **Python** — pandas, numpy, matplotlib, seaborn, scipy (Monte Carlo)
- **Power BI** — interactive dashboard with 3 slicers (OEM, city tier, component)
- **PowerPoint** — 10-slide consulting-style deck

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/yourusername/ev-aftersales-india.git
cd ev-aftersales-india

# Install dependencies
pip install pandas numpy matplotlib seaborn scipy jupyter

# Generate all 3 datasets first
jupyter notebook notebooks/01_generate_data.ipynb

# Then run analysis notebooks in order
jupyter notebook notebooks/02_market_sizing.ipynb
jupyter notebook notebooks/03_dealer_analysis.ipynb
jupyter notebook notebooks/04_warranty_analysis.ipynb
jupyter notebook notebooks/05_monte_carlo.ipynb
```

---


---

## About Me

I'm a 3rd year Mechanical Engineering student (Automotive specialisation) at DTU with experience in data operations (JCB India), financial analysis (Prasuta Ventures / Motilal Oswal), and R&D (DRDO). This project was built to apply consulting-style structured thinking to a real India-market problem.

Open to internship and placement opportunities in **consulting, strategy, and analytics**.

Connect on LinkedIn: https://www.linkedin.com/in/bhanu-sharma-b0b434282/

---

*Data simulated from industry benchmarks for analytical purposes. All figures are estimates based on publicly available sources.*
