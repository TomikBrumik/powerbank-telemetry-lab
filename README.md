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

### ⚡ S-Tier: Absolute Technological Elite
- **UGREEN Nexode 200W (25k)** — **72.29 Wh (80.32%)** | **127.95 Wh/kg** | *Dual independent buck-boost converters (100W+100W simultaneous without reset), 140W EPR profile, and 65W input.*
- **UGREEN 145W (25k)** — **74.49 Wh (82.77%)** | **150.94 Wh/kg** | *Top laptop reference with independent 100W + 45W split, fast 65W input, and honest cells.*
- **INIU 45W w/ Cable (20k)** — **70.30 Wh (95.00%)** | **209.72 Wh/kg** | *Laboratory record holder. Average efficiency 95.00% (second unit hit 96.27%), exceptional gravimetric density 209.72 Wh/kg.*
- **INIU P771 Qi2.2 25W (10k)** — **31.94 Wh (88.72%)** | **148.56 Wh/kg** | *Most modern magnetic charging with full Qi2.2 certification (25W), excellent wired efficiency (88.72%), and top thermal management with record wall-to-load cycle efficiency (84.05%).*

### 🔋 A-Tier: Top Work and Daily Models
- **Vention 165W TFT (20k)** — **61.62 Wh (83.27%)** | **140.14 Wh/kg** | *Paper split 100W + 65W, color TFT display, and high overall power ceiling.*
- **AlzaPower Vision 100W (10k & 20k)** — **32.82 Wh (91.17%) & 60.62 Wh (84.19%)** | *Full 100W input and output, but immediate severe thermal throttling during its own charging (drops power to 15–22 W). Also suffers from 5V drop when sharing C-C ports.*
- **Samsung 45W EB-P4520 (20k)** — **62.20 Wh (84.05%)** | **155.34 Wh/kg** | *Perfect symmetrical 22W + 22W split without 5V drop, and full 5A PPS support for Super Fast Charging 2.0 (45W for Samsung devices).*
- **AlzaPower WorkMate 100W (20k)** — **59.99 Wh (81.07%)** | **138.61 Wh/kg** | *Great internal port distribution and power allocation, but completely lacks 5A PPS (locks modern phones to fixed 9V / 3A).*
- **CUKTECH 45W / 55W (20k)** — **64.09 Wh (86.61%)** | **128.98 Wh/kg** | *Excellent internal efficiency (86.61%), full 5A PPS, and 40W input.*
- **INIU Pocket 10k (P50)** — **30.56 Wh (84.89%)** | **188.64 Wh/kg** | *Pocket EDC (162 g, 188 Wh/kg) with full 45W for phones and fast charging of the power bank itself.*

### 💎 B-Tier: Strong Models with a Minor Compromise
- **AlzaPower Metal 40k** — **119.69 Wh (80.87%)** | **151.33 Wh/kg** | *Moved up due to 100W power and a durable aluminum body, but suffers from poor power sharing when multiple devices are plugged in at once.*
- **O2 Spark 35W (10k)** — **28.97 Wh (80.47%)** | **166.59 Wh/kg** | *Hidden talent. Thanks to quality 21700 cells and converter headroom, it can push up to 40W at peak.*
- **AlzaPower Parade Gen2 100W (27k)** — **81.16 Wh (81.21%)** | **152.31 Wh/kg** | *Huge 99.9 Wh capacity and 100W input & output (both ways), but suffers from unstable behavior and power sharing when discharged below 45%.*
- **Samsung 10k 25W PD (Beige)** — **30.00 Wh (81.08%)** | **135.14 Wh/kg** | *Reliable foundation with 9W+9W split and 25W input.*
- **PanzerGlass Empower Qi2 (10k)** — **31.80 Wh (82.60%)** | **162.74 Wh/kg** | *Honest Qi2 wireless with 82.6% efficiency.*
- **O2 Built-in Cable 10k** — **30.48 Wh (82.38%)** | **148.68 Wh/kg** | *Practical city bank with 82.38% efficiency.*

### 🔹 C-Tier: Capacity Workhorses & Older Foundations
- **ROMOSS 65W Fast Charge (27k)** — **75.44 Wh (75.52%)** | **111.35 Wh/kg** | *The body is large and efficiency lags (75.52%), but it safely delivers an honest 65W.*
- **ChoeTech Digital 22.5W (50k)** — **166.75 Wh (90.14%)** | **174.55 Wh/kg** | *Super efficiency (90.14%) driven by a massive parallel cell array (50,000 mAh / 185 Wh) with LED display and 3 ports. However, the total output is limited to 22.5W, and forum reviews suggest real-world output often caps around 15W.*
- **WG 10k QC/PD** — **30.10 Wh (81.35%)** | **136.82 Wh/kg** | *Standard 20W base.*
- **AlzaPower Vision 10k (30W)** — **28.46 Wh (79.06%)** | **119.73 Wh/kg** | *Older 30W concept.*
- **Samsung 10k Wireless** — **29.79 Wh (80.51%)** | **124.13 Wh/kg** | *Older slow wireless.*

### 📉 D-Tier: Outdated Concepts & Weak Magnets
- **ChoeTech PD20W (5k)** — **13.93 Wh (75.28%)** | **-** | *Small, compact design with a built-in USB-C connector directly on the body. The catch? It has a slow charging quirk.*
- **WG 20+ (20k)** — **62.74 Wh (84.78%)** | **148.98 Wh/kg** | *Outdated 20W concept with slow 18W input from the wall and 5V drop with multiple devices.*
- **Vention 5k (No Built-in Cable)** — **14.10 Wh (76.22%)** | **109.13 Wh/kg** | *Basic model without any built-in cables, average efficiency.*
- **Vention Magnetic Wireless 20W Pink (5k)** — **15.71 Wh (84.92%)** | **124.29 Wh/kg** | *Old heating 7.5W wireless charging masked as a magnet.*
- **AlzaPower Qi2 Slim (5k)** — **15.30 Wh (82.70%)** | **122.20 Wh/kg** | *Extremely thin, but limited by a small pack and 5V/3A sharing.*

### ⚠️ E-Tier: Heat Generators & Prehistoric Models
- **AlzaPower Garnet 20k (White)** — **54.72 Wh (73.95%)** | **131.86 Wh/kg** | *Shares a miserable efficiency, prehistoric 18W input (takes forever to charge), and 5V drop under load.*
- **AlzaPower Parade Gen2 22.5W (20k)** — **53.86 Wh (71.81%)** | **131.53 Wh/kg** | *Shares miserable efficiency, prehistoric 18W input, and 5V drop under load. Ends up with a tragic 71.81% efficiency on the 5V/2A test.*
- **UGREEN Qi2 Black (10k)** — **25.34 Wh (68.49%)** | **119.08 Wh/kg** | *Messed up thermal design of the coil and converter with 68.49% efficiency.*

### 💀 F-Tier: Disqualified / Load Failures
- **Vention Mini 35W w/ Cable (10k)** 💀 — **26.59 Wh @ 9V (69.07%) / 29.15 Wh @ 5V (75.71%)** | **165.16 Wh/kg** | *Passed at 5V/2A (75.71%), but when loaded at the declared 9V / 2.77A, the converter totally collapsed to 69.07% and started to boil.*
- **TRONIC 10k (Lidl)** 💀 — **18.20 Wh (49.19%)** | **82.80 Wh/kg** | *Catastrophic efficiency 49.19% (only 18.2 Wh from 37 Wh), massive voltage drop under load. Absolute e-waste.*
