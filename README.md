# ⚡ Powerbank Telemetry & Efficiency Benchmark Lab

A publicly accessible, standardized telemetry database and engineering benchmark for portable power banks. All units undergo controlled continuous discharge and recharge cycles to expose real usable energy, DC-DC converter efficiency, thermal behavior, and BMS limits.

**Total Units Tested:** 🔬 45 individual units across **33 models** (from 5,000 mAh to 50,000 mAh)

---

## ⚡ Input Charging vs. Output Efficiency (Wall-to-Load Benchmark)

| Model | Labeled Pack | Input (Wall) | Output (Load) | Total Loss | Pack Discharge Eff. | Wall-to-Load Cycle Eff. | Diagnostic Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **INIU P771 Qi2 Magnetic (10k)** | 36.00 Wh | 38.00 Wh | 31.94 Wh | -6.06 Wh | **88.72%** | **84.05%** | 9.07V steady in; synchronous buck-boost; outstanding thermals |
| **Samsung 45W EB-P4520 (Unit 1)** | 74.00 Wh | **TBD** | 64.01 Wh | **-** | **86.50%** | **TBD** | Baseline reference run; pack discharge verified; input recharge pending |
| **Samsung 45W EB-P4520 (Unit 2)** | 74.00 Wh | 76.00 Wh | 60.39 Wh | -15.61 Wh | **81.61%** | **79.46%** | Second production sample; complete wall-to-load cycle verified |
| **UGREEN Nexode 200W (25k)** 🆕 | 90.00 Wh | 99.00 Wh | 72.29 Wh | -26.71 Wh | **80.32%** | **73.02%** | Full cycle: 9.07V in (10,939 mAh) → 15,133 mAh @ 5V/2A out; 5S 21700 cell pack |
| **AlzaPower Parade Gen2 100W (Run 2)** | 99.90 Wh | 111.88 Wh | 82.35 Wh | -29.53 Wh | **82.43%** | **73.60%** | Peak discharge pass; 16,232 mAh @ 5V/2A; reached clean 00% cut |
| **AlzaPower Parade Gen2 100W (Run 1)** | 99.90 Wh | 111.88 Wh | 81.07 Wh | -30.81 Wh | **81.15%** | **72.46%** | High thermal dissipation during 65W input replenishment stage |
| **Vention 35W Dash Series (9V Stress)** 💀 | 38.50 Wh | 35.00 Wh | 26.59 Wh | -8.41 Wh | **69.07%** | **75.98%** | **F-Tier Failure:** 20W input absorbed only 35Wh; 3x thermal shutdowns (OTP) under 24W load |

---

## 🏆 Full 7-Tier Classification & Standards

### ⚡ S-Tier: Engineering Excellence
- **UGREEN Nexode 200W (25k)** — **72.29 Wh (80.32%)** | **127.95 Wh/kg** | *Dual independent buck-boost converters (100W+100W simultaneous without reset) + 140W EPR 28V/5A single-port. 65W fast input.*
- **INIU 45W w/ Cable (20k)** — **70.30 Wh (95.00%)** | **209.72 Wh/kg** | *Laboratory record holder. Average efficiency 95.00% (second unit hit 96.27%), exceptional gravimetric density 209.72 Wh/kg.*
- **AlzaPower Vision 100W (10k)** — **32.82 Wh (91.17%)** | **95.52 Wh/kg**
- **ChoeTech Digital 22.5W (50k)** — **166.75 Wh (90.14%)** | **174.55 Wh/kg**
- **INIU P771 Qi2 25W (10k)** — **31.94 Wh (88.72%)** | **148.56 Wh/kg**

### 🔋 A-Tier: Exceptional Efficiency
- **Samsung 20k 45W (EB-P4520)** — **62.20 Wh (84.05%)** | **155.34 Wh/kg** | *Best-in-class symmetrical multiport: 22W+22W dual split, no 5V drop. High-voltage PPS support.*
- **CUKTECH 45W / 55W (20k)** — **64.09 Wh (86.61%)** | **128.98 Wh/kg** | *Very high efficiency (86.61%), great 40W input and PPS. Only reason it's not S is the 5V / 3A multiport drop.*
- **INIU Pocket 10k (P50)** — **30.56 Wh (84.89%)** | **188.64 Wh/kg** | *Best size-to-power ratio for EDC (162 g, 188 Wh/kg, 45W PD in a pocket).*
- **AlzaPower Vision 100W (20k)** — **60.62 Wh (84.19%)** | **126.85 Wh/kg** | *High 100W single-port power, 65W input and 84.19% efficiency.*
- **WG 20+ (20k) & AlzaPower Parade 22.5W (20k)** — **62.74 Wh (84.78%)** | **148.98 Wh/kg** | *Very good conversion efficiency (~84.1–84.8%), stable Injoinic electronics.*
- **Vention Magnetic Wireless 20W Pink (5k)** — **15.71 Wh (84.92%)** | **124.29 Wh/kg** | *Peak efficiency in 5k format (84.92%) and clean 5V regulation.*

### 💎 B-Tier: Very Good Daily Drivers
- **UGREEN 145W (25k)** — **74.49 Wh (82.77%)** | **150.94 Wh/kg** | *Travel workhorse. PD 3.1 140W, great 100W + 45W split, and 65W input. 82.77% efficiency is very solid at this power level.*
- **Vention 165W TFT (20k)** — **61.62 Wh (83.27%)** | **140.14 Wh/kg** | *Great color TFT display and paper split 100W + 65W, efficiency 83.27%. Not in A/S due to heating and poorer stability at peak load.*
- **AlzaPower WorkMate 100W (20k)** — **59.99 Wh (81.07%)** | **138.61 Wh/kg** | *Clean multiport logic (holds 65W for a laptop even when other ports are occupied), efficiency 81.07%.*
- **AlzaPower Parade Gen2 100W (27k)** — **81.16 Wh (81.21%)** | **152.31 Wh/kg** | *Excellent capacity under the flight limit (99.9 Wh) and fast 96W input, but unstable power distribution when the battery drops below 45%.*
- **Samsung 10k 25W PD (Beige)** — **30.00 Wh (81.08%)** | **135.14 Wh/kg** | *Symmetrical 9W + 9W split and fast 25W input, reliable foundation.*
- **PanzerGlass Empower Qi2 (10k), O2 Built-in Cable (10k), WG 10k QC/PD, AlzaPower Qi2 Slim (5k)** — *Solid average with 81-82.7% efficiency.*

### 🔹 C-Tier: Standard Workhorses
- **AlzaPower Metal 40k** — **119.69 Wh (80.87%)** | **151.33 Wh/kg**
- **Samsung 10k Wireless** — **29.79 Wh (80.51%)** | **124.13 Wh/kg**
- **O2 Spark 35W (10k)** — **28.97 Wh (80.47%)** | **166.59 Wh/kg**
- **AlzaPower Vision 10k (30W)** — **28.46 Wh (79.06%)** | **119.73 Wh/kg**

### 📉 D-Tier: Mediocre Efficiency
- **Vention Cables Yellow (5k)** — **14.10 Wh (76.22%)** | **109.13 Wh/kg**
- **ROMOSS 65W Fast Charge (27k)** — **75.44 Wh (75.52%)** | **111.35 Wh/kg**
- **AlzaPower Garnet 20k (White)** — **54.72 Wh (73.95%)** | **131.86 Wh/kg**

### ⚠️ E-Tier: Poor Efficiency & Elevated Losses
- **AlzaPower Parade Gen2 22.5W (20k)** — **53.86 Wh (71.81%)** | **131.53 Wh/kg**
- **UGREEN Qi2 Black (10k)** — **25.34 Wh (68.49%)** | **119.08 Wh/kg**

### 💀 F-Tier: Critical Underperformance & Hardware Flaws
- **Vention Mini 35W w/ Cable (10k)** 💀 — **26.59 Wh @ 9V (69.07%) / 29.15 Wh @ 5V (75.71%)** | **165.16 Wh/kg** | *3x thermal OTP shutdowns (code 188), fake 35W claim, ~8k mAh real cell.*
- **TRONIC PD/QC (Lidl - 10k)** 💀 — **18.20 Wh (49.19%)** | **82.80 Wh/kg** | *Severe voltage collapse to 9.9V, 18.8Wh heat waste.*
