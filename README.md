# 🔋 Powerbank Telemetry & Efficiency Benchmark Lab

[![Dataset: CSV](https://img.shields.io/badge/Dataset-CSV-green.svg)](powerbank_telemetry_database.csv)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Testbench: ATORCH DL24P](https://img.shields.io/badge/Testbench-ATORCH%20DL24P-orange.svg)](#)

A publicly accessible, standardized telemetry database and engineering benchmark for portable powerbanks. All units undergo controlled constant-current/constant-power discharge tests to expose real usable energy, DC-DC converter efficiency, thermal behavior, and BMS limits.

*Note on Volumetric Density (Wh/liter): Gravimetric density (Wh/kg) is tracked precisely via digital scale. Volumetric density (Wh/L) is currently being estimated and will be added via caliper measurements soon!*

---

## 🔬 Testing Methodology & Equipment

* **Hardware Testbench:** ATORCH DL24P Programmable Electronic DC Load.
* **Inline Metering:** High-precision USB-C digital hardware testers for real-time charging telemetry (V, A, Wh input).
* **Standardized Harness:** Ultra-low resistance 30cm USB-C direct link cable with <3.8V cut-off threshold to eliminate cable IR-drop measurement distortion.
* **Continuous Monitoring:** Real-time logging of terminal voltage, line current, DCIR (internal resistance), and thermal dissipation.
* **Electrical Efficiency Metric (Discharge / Pack):** Measured Output Energy (Wh) / Rated Battery Pack Energy (Wh) * 100
* **Total Cycle Efficiency Metric (Wall-to-Load / Tam a zpět):** Measured Output Energy (Wh) / Measured Input Energy (Wh) * 100
* **Gravimetric Energy Density:** Measured Output Energy (Wh) / Total Unit Weight (kg)

---

## ⚡ Input Charging vs. Output Efficiency (Wall-to-Load Benchmark)

Porovnání energie odebrané ze sítě ($E_{\text{in}}$), nominální kapacity článků ($E_{\text{nominal}}$) a energie skutečně dodané do zátěže ($E_{\text{out}}$).

| Model | Nominál packu | Vstup ze sítě ($E_{\text{in}}$) | Výstup ($E_{\text{out}}$) | Účinnost z nominálu ($\eta_{\text{pack}}$) | Účinnost tam a zpět ($\eta_{\text{cycle}}$) | Poznámka k měření |
| :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| **INIU P771 Qi2 Magnetic 25W (10k)** | 36.0 Wh | 38.00 Wh | 31.94 Wh | **88.72%** | **84.05%** | Vstup 9.07V, špičkový synchronní DC-DC měnič |
| **Samsung 20k 45W EB-P4520 (Kus 2)** | 74.0 Wh | 76.00 Wh | 60.39 Wh | **81.61%** | **79.46%** | Vstup 76Wh, výstup 60.39Wh (Kus 1 drží v S-Tieru 64.01Wh / 86.5%) |
| **AlzaPower Parade Gen2 100W – Test 2** | 99.9 Wh | 111.88 Wh | 82.35 Wh | **82.43%** | **73.60%** | Samostatný cyklus 2 |
| **AlzaPower Parade Gen2 100W – Test 1** | 99.9 Wh | 111.88 Wh | 81.07 Wh | **81.15%** | **72.46%** | Samostatný cyklus 1 (Průměr Parade: 81.79% nominál / 73.03% cycle) |

---

## 🏆 Tier List Classification

### 🥇 S-Tier: Engineering Excellence (Sync Buck-Boost & Premium Chemistry)

* **INIU 45W Power Bank for iPhone (20,000 mAh / 74 Wh)** 👑  
  **Measured:** 69.36 Wh | **Efficiency:** **93.7%** *(All-time lab record)* | **Weight:** 335.2 g | **Density:** **206.9 Wh/kg**  
  *Ultra-compact high-density Li-Po architecture; exceptionally efficient synchronous DC-DC converter with negligible internal resistance.*
* **AlzaPower Vision 100W (10,000 mAh / 36 Wh)** 💡  
  **Measured:** 33.04 Wh | **Efficiency:** **91.8%** *(Avg of 2 units)* | **Weight:** 343.6 g | **Density:** **96.2 Wh/kg**  
  *Uncompromised rail stability throughout discharge; solid aluminum-polycarbonate chassis with integrated TFT display and flashlight.*
* **ChoeTech Digital 22.5W (50,000 mAh / 185 Wh)** 🔋  
  **Measured:** 166.75 Wh | **Efficiency:** **90.1%** | **Weight:** 955.3 g | **Density:** **174.6 Wh/kg**  
  *16h runtime, massive capacity.*
* **INIU P771 Qi2 25W Magnetic (10,000 mAh / 36 Wh)** 🧲  
  **Measured:** 31.94 Wh | **Efficiency (Pack):** **88.7%** | **Cycle Efficiency:** **84.1%** | **Weight:** 215.0 g | **Density:** **148.6 Wh/kg**  
  *36Wh pack nominal, 38Wh in -> 31.94Wh out, vynikající účinnost.*
* **CUKTECH 45W (20,000 mAh / 74 Wh)** 🏆  
  **Measured:** 64.09 Wh | **Efficiency:** **86.6%** | **Weight:** 496.9 g | **Density:** **129.0 Wh/kg**  
  *Synchronous buck-boost topology; minimal voltage ripple, precise microprocessor line telemetry.*
* **Samsung 20,000mAh 45W PD SFC 2.0 (EB-P4520) (20,000 mAh / 74 Wh)** ⚡  
  **Measured:** 64.01 Wh | **Efficiency:** **86.5%** | **Weight:** 400.4 g | **Density:** **159.9 Wh/kg**  
  *Kus 1: 64.01 Wh (86.5%). Kus 2 otestován na obousměrnou telemetrii: 76.00 Wh in -> 60.39 Wh out (81.6% pack eff, 79.5% cycle eff).*
* **Vention Magnetic Wireless 20W Pink (5,000 mAh / 18.5 Wh)** 🌸  
  **Measured:** 15.71 Wh | **Efficiency:** **84.9%** | **Weight:** 126.4 g | **Density:** **124.3 Wh/kg**  
  *Solid DC-DC conversion, previously misidentified as Ineo.*
* **INIU Pocket 10k P50 (10,000 mAh / 36 Wh)** 🎀  
  **Measured:** 30.56 Wh | **Efficiency:** **84.9%** | **Weight:** 162.0 g | **Density:** **188.6 Wh/kg**  
  *Exceptional density, 45W support.*
* **WG 20+ (20,000 mAh / 74 Wh)** 👑  
  **Measured:** 62.74 Wh | **Efficiency:** **84.8%** | **Weight:** 421.0 g | **Density:** **149.0 Wh/kg**  
  *New King of 20k, 6h 15m test runtime, precise output.*
* **AlzaPower Vision 100W (20,000 mAh / 72 Wh)** ⚡  
  **Measured:** 60.62 Wh | **Efficiency:** **84.2%** | **Weight:** 477.9 g | **Density:** **126.8 Wh/kg**  
  *Used healthy unit (Kus 1) for benchmark.*
* **AlzaPower Parade 22.5W (20,000 mAh / 74 Wh)** ⚡  
  **Measured:** 62.27 Wh | **Efficiency:** **84.1%** | **Weight:** 415.0 g | **Density:** **150.0 Wh/kg**  
  *Re-tested (USB-C 30cm), highly efficient Li-Po pouch workhorse.*
* **Vention 165W TFT (20,000 mAh / 74 Wh)** 📺  
  **Measured:** 61.62 Wh | **Efficiency:** **83.3%** | **Weight:** 439.7 g | **Density:** **140.1 Wh/kg**  
  *Independent DC-DC lines, dedicated telemetry IC.*

---

### 🥈 A-Tier: Reliable Workhorses & Solid DC-DC Regulation

* **UGreen 145W (25k)** — **74.49 Wh (82.8%)** | **150.9 Wh/kg** | *Sustained 100W PD.*
* **AlzaPower Qi2 Slim (5k)** — **15.30 Wh (82.7%)** | **122.2 Wh/kg** | *Exceptional compact Qi2 efficiency.*
* **PanzerGlass Empower Qi2 (10k)** — **31.80 Wh (82.6%)** | **162.7 Wh/kg** | *High efficiency for a wireless powerbank.*
* **O2 Built-in Cable (10k)** — **30.48 Wh (82.4%)** | **148.7 Wh/kg** | *Low-resistance flex cables, 2.4A OCP on 9V.*
* **AlzaPower Parade Gen2 100W (27k)** — **81.54 Wh (81.6%)** | **153.0 Wh/kg** | *Průměr ze 3 cyklů (81.07, 82.35 a 81.21 Wh), cycle eff 72.9%.*
* **WG 10k QC/PD** — **30.10 Wh (81.4%)** | **136.8 Wh/kg** | *Clean rail regulation without transient spikes.*
* **Samsung 10k 25W PD (Beige)** — **30.00 Wh (81.1%)** | **135.1 Wh/kg** | *High-efficiency 25W PPS/PD converter.*
* **AlzaPower WorkMate 100W (20k)** — **59.99 Wh (81.1%)** | **138.6 Wh/kg** | *Solid 100W performance.*
* **AlzaPower Metal (40k)** — **119.69 Wh (80.9%)** | **151.3 Wh/kg** | *Massive aluminum chassis, zero thermal sag.*
* **O2 Spark 35W (10k)** — **28.97 Wh (80.5%)** | **166.6 Wh/kg** | *2S 21700 architecture minimizes Joule losses.*
* **Samsung 10k Wireless** — **29.79 Wh (80.5%)** | **124.1 Wh/kg** | *Much better wired efficiency with direct harness.*
* **AlzaPower Vision 30W (10k)** — **28.46 Wh (79.1%)** | **119.7 Wh/kg** | *Average of 3 units.*

---

### 🥉 B-Tier: Compact Wireless, Specialized & Legacy Models

* **Vention Cables Yellow (5k)** — **14.10 Wh (76.2%)** | **109.1 Wh/kg** | *Slight voltage sag over 2.0A on 5V rail.*
* **Vention Mini 35W w/ Cable (10k)** — **29.15 Wh (75.7%)** | **165.2 Wh/kg** | *Compact, but standard efficiency.*
* **ROMOSS 65W Fast Charge (27k)** — **75.44 Wh (75.5%)** | **111.4 Wh/kg** | *Massive 65W brick, safe sub-100Wh flight limit.*
* **AlzaPower Garnet 22.5W White (20k)** — **54.72 Wh (73.9%)** | **131.9 Wh/kg** | *Drops from 15% to 0% abruptly.*
* **AlzaPower Parade Gen2 22.5W (20k)** — **53.86 Wh (71.8%)** | **131.5 Wh/kg** | *Lower efficiency compared to older generation.*
* **UGreen Qi2 Black (10k)** — **25.34 Wh (68.5%)** | **119.1 Wh/kg** | *Wireless coil circuit parasitic losses.*

---

### 🛑 F-Tier: Critical Hardware & Firmware Flaws

* **TRONIC PD/QC (Lidl - 10k)** — **18.20 Wh (49.2%)** | **82.8 Wh/kg** | *18.8Wh wasted as heat, fake CV gauge.*
