# ⚡ Powerbank Telemetry & Efficiency Benchmark Lab

A publicly accessible, standardized telemetry database and rigorous engineering benchmark for portable power banks. All units undergo controlled continuous discharge and recharge cycles to expose real usable energy, DC-DC converter topology, multi-port voltage sag, thermal throttling, and cell architecture.

**Total Units Tested:** 🔬 44 individual runs/units across **32 models** (from 5,000 mAh EDC units to massive 50,000 mAh field packs).

---

## 🏆 r/UsbCHardware Standardized 100-Point Scoring Model

Every tested power bank receives a definitive score (0–100 pts) based on critical engineering requirements:

1. **Power Output & Topology (25 pts):** Continuous wattage ceiling (up to 10 pts for 140W+ EPR) + Multi-port architecture (15 pts for true independent buck-boost converters with zero voltage drop vs. severe 2.5 pts penalty for collapsing all rails to 5V).
2. **Protocols & Input Speed (20 pts):** Full 5A PPS support (10 pts) + PD 3.1 EPR (5 pts) + High-speed input without thermal throttling (5 pts).
3. **Lab Measured Wh Efficiency & Density (20 pts):** Measured DL24P discharge efficiency (12 pts) + Gravimetric density Wh/kg (8 pts).
4. **Cell Chemistry & Anti-Swelling (15 pts):** Steel cylindrical 21700 / 18650 cells with mechanical CID pressure vents (15 pts - zero swelling risk) vs. reinforced 2S/High-Density packs (9 pts) vs. standard soft pouch cells (5 pts) vs. low-grade e-waste (0 pts).
5. **Thermals & Load Stability (10 pts):** Rock-solid voltage delivery to 0% cut (10 pts) vs. voltage instability below 45% (6 pts) vs. OTP shutdown crashes (0 pts / Disqualification).
6. **Usability: Low-Power Mode & Telemetry (10 pts):** Low-Power Mode (5 pts - dedicated/manual lock for wearables) + Live telemetry display/budíky (up to 5 pts for color TFT live wattmeters showing V, A, W, and runtime).

---

## ⚡ Input Charging vs. Output Efficiency (Wall-to-Load Benchmark)

| Model | Labeled Pack | Input (Wall) | Output (Load) | Total Loss | Pack Discharge Eff. | Wall-to-Load Cycle Eff. | Circuitry & Diagnostic Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **INIU P771 Qi2 Magnetic (10k)** | 36.00 Wh | 38.00 Wh | 31.94 Wh | -6.06 Wh | **88.72%** | **84.05%** | 9.07V steady in; synchronous buck-boost; outstanding thermals |
| **Samsung 45W EB-P4520 (Unit 1)** | 74.00 Wh | **TBD** | 64.01 Wh | **-** | **86.50%** | **TBD** | Baseline reference run; pack discharge verified; input recharge pending |
| **Samsung 45W EB-P4520 (Unit 2)** | 74.00 Wh | 76.00 Wh | 60.39 Wh | -15.61 Wh | **81.61%** | **79.46%** | Second production sample; complete wall-to-load cycle verified |
| **UGREEN Nexode 200W (25k)** 🆕 | 90.00 Wh | 99.00 Wh | 72.29 Wh | -26.71 Wh | **80.32%** | **73.02%** | Full cycle: 9.07V in (10,939 mAh) → 15,133 mAh @ 5V/2A out; 5S 21700 cell pack |
| **AlzaPower Parade Gen2 100W (Run 2)** | 99.90 Wh | 111.88 Wh | 82.35 Wh | -29.53 Wh | **82.43%** | **73.60%** | Peak discharge pass; 16,232 mAh @ 5V/2A; reached clean 00% cut |
| **AlzaPower Parade Gen2 100W (Run 1)** | 99.90 Wh | 111.88 Wh | 81.07 Wh | -30.81 Wh | **81.15%** | **72.46%** | High thermal dissipation during 65W input replenishment stage |
| **Vention 35W Dash Series (9V Stress)** 💀 | 38.50 Wh | 35.00 Wh | 26.59 Wh | -8.41 Wh | **69.07%** | **75.98%** | **F-Tier Failure:** 20W input absorbed only 35Wh; 3x thermal shutdowns (OTP) under 24W load |

---

## 🏆 Full 7-Tier Leaderboard (Scores out of 100)

### ⚡ S-Tier: Absolute Technological Elite (Score ≥ 85.0)
*True independent multi-port rails, steel cylindrical 21700 cells, full PPS, and high continuous power.*
- **UGREEN Nexode 200W (25k)** — **94.5 pts** | **72.29 Wh (80.32%)** | **127.95 Wh/kg** | *5S 21700 cells, dual independent buck-boost (100W+100W without reset or 5V drop), 140W EPR profile, full 5A PPS, TFT live wattmeter, 3s Low-Power Mode.*
- **UGREEN 145W (25k)** — **93.7 pts** | **74.49 Wh (82.77%)** | **150.94 Wh/kg** | *21700 cells, independent 100W + 45W split, 65W fast input without throttling, full 5A PPS, 3s Low-Power Mode.*
- **AlzaPower WorkMate 100W (20k)** — **84.8 pts** | **59.99 Wh (83.32%)** | **138.61 Wh/kg** | *4x 21700 cells (72 Wh pack). Best AlzaPower tested: independent multi-port rail (zero 5V drop!), Low-Power Mode, and telemetry display showing V and A. Deductions only for lacking 5A PPS (locked to 3A).*

### 🔋 A-Tier: Top Work and Daily Models (Score 75.0 – 84.9)
*High continuous output, cylindrical cells or advanced 2S packs, excellent regulation.*
- **AlzaPower Vision 100W (20k)** — **78.9 pts** | **60.62 Wh (84.19%)** | **126.85 Wh/kg** | *4x 21700 cells, full 5A PPS, color TFT live wattmeter (V, A, W, time), Low-Power Mode, full-speed input without throttling. Penalized only for shared rail 5V drop on multi-port.*
- **AlzaPower Vision 100W (10k)** — **78.6 pts** | **32.82 Wh (91.17%)** | **95.52 Wh/kg** | *2x 21700 cells, exceptional 91.17% discharge efficiency, full 5A PPS, color TFT live wattmeter, Low-Power Mode. Penalized for 5V multi-port drop and high mass (343 g).*
- **CUKTECH 45W PB200N (20k)** — **67.3 pts** *(High B-Tier)* | **64.09 Wh (86.61%)** | **128.98 Wh/kg** | *2S Li-Po block (7.4V), full 5A PPS (up to 55W Xiaomi Turbo), dedicated 2-hour Low-Power Mode (double-click), integrated lanyard cable.*

### 💎 B-Tier: Solid Daily Drivers with Minor Compromises (Score 65.0 – 74.9)
- **O2 Spark 35W (10k)** — **69.5 pts** | **28.97 Wh (80.47%)** | **166.59 Wh/kg** | *Heavy-duty 2x 21700 cells delivering up to 40W peak headroom without voltage sag. Lacks Low-Power Mode.*
- **INIU 45W w/ Cable (20k)** — **67.9 pts** | **70.30 Wh (95.00%)** | **209.72 Wh/kg** | *Lab efficiency record holder (96.27% peak), extreme density, 5A PPS, built-in cable, auto Low-Power Mode. Penalized for soft pouch cells and shared rail.*
- **Samsung 45W EB-P4520 (20k)** — **66.5 pts** | **62.20 Wh (84.05%)** | **155.34 Wh/kg** | *Symmetrical 22W + 22W split (no 5V drop) and full 5A PPS. Penalized for soft pouch cells and lack of dedicated Low-Power Mode.*
- **AlzaPower Parade Gen2 100W (27k)** — **63.5 pts** *(High C-Tier)* | **81.16 Wh (81.21%)** | **152.31 Wh/kg** | *Huge 99.9 Wh pack, 100W in/out, Low-Power Mode, but soft pouch cell, 5V multi-port drop, and severe voltage instability below 45% SoC.*

### 🔹 C-Tier: Older Foundations & Multi-Flaw Units (Score 50.0 – 64.9)
- **AlzaPower Vision 10k (30W)** — **50.5 pts** | **28.46 Wh (79.06%)** | **119.73 Wh/kg** | *Has 21700 cells, but suffers a triple failure: 5V multi-port drop, severe thermal throttling during recharge (drops to 15–22W), and NO Low-Power Mode.*
- **ChoeTech Digital 22.5W (50k)** — **58.2 pts** | **166.75 Wh (90.14%)** | **174.55 Wh/kg** | *Massive parallel cell block with high low-current efficiency, but capped at 22.5W and sags under sustained 20W loads.*
- **WG 10k QC/PD** — **54.2 pts** | **30.10 Wh (81.35%)** | **136.82 Wh/kg** | *Standard 20W baseline pouch bank.*

### 📉 D-Tier: Severe Constraints & Prehistoric Inputs (Score 40.0 – 49.9)
- **AlzaPower Parade Gen2 22.5W (20k)** — **46.6 pts** | **53.86 Wh (71.81%)** | **131.53 Wh/kg** | *Has Low-Power Mode, but crippled by 71.81% efficiency, prehistoric 18W input, and 5V multi-port drop.*
- **ChoeTech PD20W (5k)** — **43.8 pts** | **13.93 Wh (75.28%)** | **137.78 Wh/kg** (101.10 g) | *Pocket plug design, but crippled by severe recharge quirk: only charges from legacy 5V USB-A adapters; completely refuses handshake on USB-C PD chargers.*
- **AlzaPower Garnet 20k (White)** — **39.4 pts** *(E-Tier)* | **54.72 Wh (73.95%)** | **131.86 Wh/kg** | *Soft pouch cell, prehistoric 18W input, 5V multi-port drop, NO Low-Power Mode.*

### 💀 F-Tier: Disqualified / Hardware Failures (Score < 30.0 or OTP Lockout)
- **Vention Mini 35W w/ Cable (10k)** 💀 — **0.0 pts (Disqualified)** | **26.59 Wh @ 9V (69.07%)** | *Immediate 0.355V voltage sag, collapsed to 69.07% efficiency, and triggered 3 consecutive Over-Temperature Protection (OTP) shutdowns flashing error 188 under a modest 24W load.*
- **TRONIC 10k (Lidl)** 💀 — **21.6 pts (Disqualified)** | **18.20 Wh (49.19%)** | **82.80 Wh/kg** | *Catastrophic 49.19% efficiency, voltage collapses below 4.5V under a basic 2A load. Low-grade dangerous e-waste.*
