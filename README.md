# ⚡ Powerbank Telemetry & Efficiency Benchmark Lab

A publicly accessible, standardized telemetry database and engineering benchmark for portable power banks. All units undergo controlled continuous discharge and recharge cycles to expose real usable energy, DC-DC converter efficiency, thermal behavior, and BMS limits.

**Total Units Tested:** 🔬 43 individual units across 31 models (from 5,000 mAh to 50,000 mAh)

*Note on Volumetric Density (Wh/liter): Gravimetric density (Wh/kg) is tracked precisely via digital scale. Volumetric density (Wh/L) is currently being estimated and will be added via caliper measurements soon!* 📐

---

## 🔬 Testing Methodology & Hardware Rig

* **Hardware Testbench:** Factory-calibrated ATORCH DL24P Programmable Electronic DC Load with PC telemetry logging. ⚡
* **Inline Diagnostic Testers:** High-precision inline USB-C power delivery testers logging real-time charging telemetry (V, A, W, mAh, mWh) with four-wire (Kelvin) sensing at terminals. 🔌
* **Standardized Harness:** Ultra-low resistance ADOL 60W 30cm Type-C direct link cable (<3.8V cut-off threshold) to eliminate parasitic cable voltage drop ($I^2R$ dissipation) from skewing BMS efficiency numbers. 🧪
* **Environmental Baseline:** Ambient room temperature stabilized at 21.5 °C ± 1.0 °C with open convective airflow. 🌡️
* **Discharge Profiles:** Standardized continuous active load runs at 5V/2A (10W baseline) for nominal pack capacity verification, alongside protocol-specific PD stress profiles (20W, 45W, 65W, 100W, and 140W EPR). 📊
* **Pack Discharge Efficiency Metric:** $(\text{Delivered Output Energy [Wh]} / \text{Rated Battery Pack Energy [Wh]}) \times 100$ 📈
* **Wall-to-Load (Round-Trip Cycle) Efficiency Metric:** $(\text{Delivered Output Energy [Wh]} / \text{Replenishment Input Energy [Wh]}) \times 100$ 🔄
* **Gravimetric Energy Density:** $\text{Delivered Output Energy [Wh]} / \text{Total Unit Weight [kg]}$ 🚀

---

## ⚡ Input Charging vs. Output Efficiency (Wall-to-Load Benchmark)

Direct comparison between energy pulled from the AC supply ($E_{\text{in}}$), labeled nominal pack capacity ($E_{\text{nominal}}$), and actual energy delivered to the load ($E_{\text{out}}$).

| Model | Labeled Pack | Input (Wall) | Output (Load) | Total Loss | Pack Discharge Eff. | Wall-to-Load Cycle Eff. | Diagnostic Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **INIU P771 Qi2 Magnetic (10k)** | 36.00 Wh | 38.00 Wh | 31.94 Wh | -6.06 Wh | **88.72%** | **84.05%** | 9.07V steady in; synchronous buck-boost; outstanding thermals |
| **Samsung 45W EB-P4520 (Unit 1)** | 74.00 Wh | **TBD** | 64.01 Wh | **-** | **86.50%** | **TBD** | Baseline reference run; pack discharge verified; input recharge pending |
| **Samsung 45W EB-P4520 (Unit 2)** | 74.00 Wh | 76.00 Wh | 60.39 Wh | -15.61 Wh | **81.61%** | **79.46%** | Second production sample; complete wall-to-load cycle verified |
| **AlzaPower Parade Gen2 100W (Run 2)** | 99.90 Wh | 111.88 Wh | 82.35 Wh | -29.53 Wh | **82.43%** | **73.60%** | Peak discharge pass; 16,232 mAh @ 5V/2A; reached clean 00% cut |
| **AlzaPower Parade Gen2 100W (Run 1)** | 99.90 Wh | 111.88 Wh | 81.07 Wh | -30.81 Wh | **81.15%** | **72.46%** | High thermal dissipation during 65W input replenishment stage |

---

## 🏆 Tier List Classification

### 🥇 S-Tier: Engineering Excellence (Sync Buck-Boost & Premium Chemistry)

* **INIU 45W w/ Cable (20,000 mAh / 74 Wh)** 🏆
**Measured:** 70.30 Wh | **Efficiency:** **95.00%** | **Weight:** 335.20 g | **Density:** **209.72 Wh/kg**
*Outstanding form-factor efficiency; class-leading gravimetric density; negligible converter resistance. Average of 2 units (69.36Wh & 71.23Wh; second unit hit 96.27% — new lab record).*
* **AlzaPower Vision 100W (10,000 mAh / 36 Wh)** 💡
**Measured:** 32.82 Wh | **Efficiency:** **91.17%** | **Weight:** 343.60 g | **Density:** **95.52 Wh/kg**
*Uncompromised rail stability throughout discharge; heavy CNC chassis reduces gravimetric score. Average of 4 units.*
* **ChoeTech Digital 22.5W (50,000 mAh / 185 Wh)** 🔋
**Measured:** 166.75 Wh | **Efficiency:** **90.14%** | **Weight:** 955.30 g | **Density:** **174.55 Wh/kg**
*Massive multi-cell parallel array; minimal voltage sag under load; 16h+ runtime.*
* **INIU P771 Qi2 25W (10,000 mAh / 36 Wh)** 🧲
**Measured:** 31.94 Wh | **Efficiency (Pack):** **88.72%** | **Cycle Efficiency:** **84.05%** | **Weight:** 215.00 g | **Density:** **148.56 Wh/kg**
*Qi2 magnetic ring; outstanding wired PD conversion efficiency; best wall-to-load cycle efficiency in the lab.*
* **CUKTECH 45W (20,000 mAh / 74 Wh)** ⚡
**Measured:** 64.09 Wh | **Efficiency:** **86.61%** | **Weight:** 496.90 g | **Density:** **128.98 Wh/kg**
*Robust thermal envelope; 21700 cell pack; synchronous buck-boost topology.*
* **Samsung 45W (EB-P4520) - Average (20,000 mAh / 74 Wh)** ⚡
**Measured:** 62.20 Wh | **Efficiency:** **84.05%** | **Weight:** 400.40 g | **Density:** **155.34 Wh/kg**
*Average of 2 units. True 5A PPS support; exceptionally clean voltage rails.*
* **INIU Pocket 10k P50 (10,000 mAh / 36 Wh)** 🎀
**Measured:** 30.56 Wh | **Efficiency:** **84.89%** | **Weight:** 162.00 g | **Density:** **188.64 Wh/kg**
*Ultra-light EDC companion; high volumetric & gravimetric efficiency; 45W support.*
* **Vention Magnetic Pink (5,000 mAh / 18.5 Wh)** 🌸
**Measured:** 15.71 Wh | **Efficiency:** **84.92%** | **Weight:** 126.40 g | **Density:** **124.29 Wh/kg**
*Compact 1S pouch pack; clean 5V step-down conversion.*
* **WG 20+ (20,000 mAh / 74 Wh)** 👑
**Measured:** 62.74 Wh | **Efficiency:** **84.78%** | **Weight:** 421.00 g | **Density:** **148.98 Wh/kg**
*Solid mid-range workhorse; highly stable buck-boost regulation.*
* **AlzaPower Vision 100W (20,000 mAh / 72 Wh)** ⚡
**Measured:** 60.62 Wh | **Efficiency:** **84.19%** | **Weight:** 477.90 g | **Density:** **126.85 Wh/kg**
*High output PD 3.0; rugged aluminum build; verified on primary unit.*
* **AlzaPower Parade 22.5W (20,000 mAh / 74 Wh)** ⚡
**Measured:** 62.27 Wh | **Efficiency:** **84.15%** | **Weight:** 415.00 g | **Density:** **150.05 Wh/kg**
*Gen1 architecture; stable Injoinic SoC telemetry; high-efficiency Li-Po pouch workhorse.*
* **Vention 165W TFT (20,000 mAh / 74 Wh)** 📺
**Measured:** 61.62 Wh | **Efficiency:** **83.27%** | **Weight:** 439.70 g | **Density:** **140.14 Wh/kg**
*Integrated color telemetry display; independent DC-DC lines; high current capability.*

---

### 🥈 A-Tier: Reliable Workhorses & Solid DC-DC Regulation

* **UGREEN 145W (25k)** — **74.49 Wh (82.77%)** | **150.94 Wh/kg** | *5S cylindrical 21700 cells; high surge current stability; sustained 100W PD.*
* **AlzaPower Qi2 Slim (5k)** — **15.30 Wh (82.70%)** | **122.20 Wh/kg** | *Ultra-thin magnetic pack; low inductor heating.*
* **PanzerGlass Empower Qi2 (10k)** — **31.80 Wh (82.60%)** | **162.74 Wh/kg** | *Qi2 MPP certified; solid wired efficiency.*
* **AlzaPower Parade Gen2 100W (27k)** — **81.16 Wh (81.21%)** | **152.31 Wh/kg** | *4 units: 81.07, 82.35, 81.21, 79.99 Wh. Wh in: 111.88, 112.00, 112.20, 111.88 (avg 111.99).*
* **O2 Built-in Cable (10k)** — **30.48 Wh (82.38%)** | **148.68 Wh/kg** | *Integrated Type-C tether; low trace resistance; 2.4A OCP on 9V.*
* **Samsung 45W EB-P4520 (Unit 2) (20k)** — **60.39 Wh (81.61% pack / 79.46% cycle)** | **150.82 Wh/kg** | *High-density 4S pack; full wall-to-load cycle verified (In 76.00 Wh).*
* **WG 10k QC/PD** — **30.10 Wh (81.35%)** | **136.82 Wh/kg** | *Standard 18W/20W PD commuter pack; clean rail regulation without transient spikes.*
* **Samsung 10k 25W PD (Beige)** — **30.00 Wh (81.08%)** | **135.14 Wh/kg** | *Dual USB-C; PPS support up to 2.77A.*
* **AlzaPower WorkMate 100W (20k)** — **59.99 Wh (81.07%)** | **138.61 Wh/kg** | *High continuous power delivery; rugged outer shell.*
* **AlzaPower Metal (40k)** — **119.69 Wh (80.87%)** | **151.33 Wh/kg** | *Massive aluminum chassis; zero thermal sag; massive reserve.*
* **O2 Spark 35W (10k)** — **28.97 Wh (80.47%)** | **166.59 Wh/kg** | *2S 21700 architecture minimizes Joule losses; supports PPS profiles.*
* **Samsung 10k Wireless** — **29.79 Wh (80.51%)** | **124.13 Wh/kg** | *Dual-coil Qi pad; solid wired baseline with direct harness.*
* **AlzaPower Vision 10k (30W)** — **28.46 Wh (79.06%)** | **119.73 Wh/kg** | *Average of 4 units (27.63, 28.18, 29.57, 28.44 Wh); higher idle PCB consumption.*

---

### 🥉 B-Tier: Moderate Efficiency & Elevated Losses

* **Vention Cables Yellow (5k)** — **14.10 Wh (76.22%)** | **109.13 Wh/kg** | *Built-in ribbon cables contribute slight resistive losses; slight voltage sag over 2.0A on 5V rail.*
* **Vention Mini 35W w/ Cable (10k)** — **29.15 Wh (75.71%)** | **165.16 Wh/kg** | *Compact, but runs hot under 30W+ continuous profiles.*
* **ROMOSS 65W Fast Charge (27k)** — **75.44 Wh (75.52%)** | **111.35 Wh/kg** | *Heavy plastic shell; basic conversion circuitry; safe sub-100Wh flight limit.*
* **AlzaPower Garnet 20k (White)** — **54.72 Wh (73.95%)** | **131.86 Wh/kg** | *Budget Li-Pol pack; significant thermal losses at 18W; drops abruptly from 15% to 0%.*
* **AlzaPower Parade Gen2 22.5W (20k)** — **53.86 Wh (71.81%)** | **131.53 Wh/kg** | *High internal resistance; early BMS low-voltage cut-off.*
* **UGREEN Qi2 Black (10k)** — **25.34 Wh (68.49%)** | **119.08 Wh/kg** | *High parasitic thermal dissipation in the magnetic charging stage.*

---

### 🛑 F-Tier: Critical Underperformance & Hardware Flaws

* **TRONIC PD/QC (Lidl - 10k)** — **18.20 Wh (49.19%)** | **82.80 Wh/kg** | *Critical failure: 18.8 Wh wasted as heat, abysmal conversion efficiency, severe voltage sag even under modest 10W load, and premature BMS shutdown.*

---

### 🔍 Key Engineering Takeaways & Pitfalls

1. **The Li-Pol "Voltage Sag" Trap (Parade Gen2 100W Case Study):** 🪫
A pack can deliver a solid ~82% energy efficiency at low currents (5V/2A), but completely fail under a 65W–100W laptop load. Soft Li-Pol pouches with elevated internal resistance experience severe V_drop = I × R_int. Under high amp draw, the cell terminal voltage drops below the BMS cutoff threshold (typically 3.0V/cell) well before the actual chemical energy is exhausted.
2. **Cylindrical 21700 Packs Rule High-Power PD:** ⚡
Units utilizing 4S/5S/6S configurations of 21700 cells maintain significantly flatter discharge curves and sustain high continuous wattage without premature low-voltage cutoffs.
3. **Display Telemetry Discrepancies:** 📺
Beware of smart screens that only display calculated wattage. Without dedicated voltage and amperage readouts, users cannot detect whether a device renegotiated to an inefficient 5V rail or whether active thermal throttling is taking place.
4. **Multi-Unit Testing Reveals Consistency:** 📊
The AlzaPower Vision 100W (10k) showed remarkable consistency across 4 units (within 1.27 Wh), while the Samsung 45W EB-P4520 showed wider variance (3.62 Wh between units), suggesting potential production tolerance issues.
5. **Input Energy (Wh In) Matters:** 🔌
The gap between labeled pack capacity and actual input energy reveals charger and BMS inefficiencies. The INIU P771 Qi2 pulled 38.00 Wh to deliver 31.94 Wh, while the Samsung 45W EB-P4520 Unit 2 pulled 76.00 Wh to deliver 60.39 Wh. The AlzaPower Parade Gen2 100W averaged 111.99 Wh in to deliver 81.16 Wh out.
