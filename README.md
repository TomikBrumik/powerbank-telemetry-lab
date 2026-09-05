# 🔋 Powerbank Telemetry & Efficiency Benchmark Lab

[![Dataset: CSV](https://img.shields.io/badge/Dataset-CSV-green.svg)](powerbank_telemetry_database.csv)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Testbench: ATORCH DL24P](https://img.shields.io/badge/Testbench-ATORCH%20DL24P-orange.svg)](#)

A publicly accessible, standardized telemetry database and engineering benchmark for portable powerbanks. All units undergo controlled constant-current/constant-power discharge tests to expose real usable energy, DC-DC converter efficiency, thermal behavior, and BMS limits.

---

## 🔬 Testing Methodology & Equipment

* **Hardware Testbench:** ATORCH DL24P Programmable Electronic DC Load.
* **Standardized Harness (New Method):** Ultra-low resistance 30cm USB-C direct link cable with <3.8V cut-off threshold to eliminate cable IR-drop measurement distortion.
* **Continuous Monitoring:** Real-time logging of terminal voltage, line current, DCIR (internal resistance), and thermal dissipation.
* **Electrical Efficiency Metric:** Measured Output Energy (Wh) / Rated Battery Pack Energy (Wh) * 100
* **Gravimetric Energy Density:** Measured Output Energy (Wh) / Total Unit Weight (kg)

---

## 🏆 Tier List Classification

### 🥇 S-Tier: Engineering Excellence (Sync Buck-Boost & Premium Chemistry)

* **INIU 45W Power Bank for iPhone (20,000 mAh / 74 Wh)** 👑  
  **Measured:** 69.36 Wh | **Efficiency:** **93.7%** *(All-time lab record)* | **Weight:** 335.2 g | **Density:** **206.9 Wh/kg**  
  *Ultra-compact high-density Li-Po architecture; exceptionally efficient synchronous DC-DC converter with negligible internal resistance.*
* **AlzaPower Vision 10k PD 100W (10,000 mAh / 36 Wh)** 💡  
  **Measured:** 33.15 Wh | **Efficiency:** **92.1%** *(Avg of 2 units)* | **Weight:** 345.8 g | **Density:** **95.9 Wh/kg**  
  *Uncompromised rail stability throughout discharge; solid aluminum-polycarbonate chassis with integrated TFT display and flashlight.*
* **CUKTECH 20k 45W (20,000 mAh / 74 Wh)** 🏆  
  **Measured:** 64.09 Wh | **Efficiency:** **86.6%** | **Weight:** 496.9 g | **Density:** **129.0 Wh/kg**  
  *Synchronous buck-boost topology; minimal voltage ripple, precise microprocessor line telemetry.*
* **Samsung 20,000mAh 45W PD SFC 2.0 (EB-P4520) (20,000 mAh / 74 Wh)** ⚡  
  **Measured:** 64.01 Wh | **Efficiency:** **86.5%** | **Weight:** 400.4 g | **Density:** **159.9 Wh/kg**  
  *Triple USB-C port 45W Super Fast Charging 2.0 architecture; delivered 12,793 mAh over 6h 23m; stellar voltage regulation.*
* **WG 20+ (20,000 mAh / 74 Wh)** 👑  
  **Measured:** 62.74 Wh | **Efficiency:** **84.8%** | **Weight:** 421.0 g | **Density:** **149.0 Wh/kg**  
  *New king of the 20k category. Highly efficient internal hardware yielding massive usable energy over a 6h 15m runtime.*
* **AlzaPower Parade 22.5W (20,000 mAh / 74 Wh)** ⚡  
  **Measured:** 62.27 Wh | **Efficiency:** **84.2%** | **Weight:** 415.0 g | **Density:** **150.1 Wh/kg**  
  *Re-tested with 30cm harness. Exceptional DC-DC conversion, classic Li-Po pouch workhorse pulling real weight.*
* **UGreen 145W 25k (25,000 mAh / 90 Wh - 90597A)** 🔌  
  **Measured:** 74.49 Wh | **Efficiency:** **82.8%** | **Weight:** 493.5 g | **Density:** **150.9 Wh/kg**  
  *Industrial 5× 21700 cylindrical cells with ultra-low DCIR; firm 5.2A OCP limit; full PD 3.0 / PPS compatibility.*
* **Vention 165W TFT 20k (20,000 mAh / 74 Wh)** 📺  
  **Measured:** 61.62 Wh | **Efficiency:** **83.3%** | **Weight:** 439.7 g | **Density:** **140.1 Wh/kg**  
  *Independent DC-DC rail design eliminates port handshake resets; dedicated telemetry chip feeds real-time color TFT panel.*
* **AlzaPower Metal 40k (40,000 mAh / 148 Wh)** 🏗️  
  **Measured:** 119.69 Wh | **Efficiency:** **80.9%** | **Weight:** 790.9 g | **Density:** **151.3 Wh/kg**  
  *Heavy extruded aluminum chassis serves as a full-contact heatsink for MOSFETs and power inductors; zero thermal throttling across >12h run.*
* **O2 Spark 35W with Built-in Cable (10,000 mAh / 36 Wh)** ⚡  
  **Measured:** 28.97 Wh | **Efficiency:** **80.5%** | **Weight:** 173.9 g | **Density:** **166.6 Wh/kg**  
  *2S cell architecture (2× 21700, 7.2V) halves input stage current to drastically reduce I²R resistive thermal losses.*

---

### 🥈 A-Tier: Reliable Workhorses & Solid DC-DC Regulation

* **Pink Ineo (5,000 mAh / 18.5 Wh)** 🌸  
  **Measured:** 15.71 Wh | **Efficiency:** **84.9%** | **Weight:** 126.4 g | **Density:** **124.3 Wh/kg**  
  *Solid DC-DC conversion for a compact unit, very cute pink design with surprisingly great engineering inside.*
* **AlzaPower Qi2 Ultra Slim (5,000 mAh / 18.5 Wh)** — **15.30 Wh (82.7%)** | **122.2 Wh/kg** | *Exceptional step-up conversion efficiency for an ultra-compact Qi2 form factor.*
* **O2 Power Bank 10k 20W PD 3.0/QC (10,000 mAh / 37 Wh)** — **30.48 Wh (82.4%)** | **148.7 Wh/kg** | *Low-resistance integrated flex cables; clean analog OCP cutting at 2.4A on 9V rail.*
* **WG 10k QC3.0/PD/SM (10,000 mAh / 37 Wh)** — **30.10 Wh (81.4%)** | **136.8 Wh/kg** | *Firm rail regulation without transient voltage spikes during dynamic load switching.*
* **Samsung 10,000mAh 25W PD Beige (10,000 mAh / 37 Wh)** — **30.00 Wh (81.1%)** | **135.1 Wh/kg** | *High-efficiency 25W PPS/PD converter; rock-solid voltage regulation.*
* **AlzaPower Parade Gen2 27k PD 100W (27,000 mAh / 99.9 Wh)** — **80.47 Wh (80.5%)** | **151.0 Wh/kg** | *Heavy-duty 100W buck-boost converter; robust performance.*
* **Samsung 10k Wireless (EB-U1200CS) (10,000 mAh / 37 Wh)** — **29.79 Wh (80.5%)** | **124.1 Wh/kg** | *Re-tested with 30cm direct line. Wired efficiency improved massively compared to previous setups.*
* **ROMOSS 65W Fast Charge (27,000 mAh / 99.9 Wh)** — **75.44 Wh (75.5%)** | **111.4 Wh/kg** | *Solid 65W high-power brick with safe sub-100Wh flight rating.*

---

### 🥉 B-Tier: Compact Wireless, Specialized & Legacy Models

* **Vention with Cables – Yellow (5,000 mAh / 18.5 Wh)** — **14.10 Wh (76.2%)** | **109.1 Wh/kg** | *Minor voltage sag under sustained current draws exceeding 2.0A on 5V rail.*
* **AlzaPower Garnet 20k 22.5W White (20,000 mAh / 74 Wh)** — **54.72 Wh (73.9%)** | **131.9 Wh/kg** | *Modern chassis and ports, but poor internal components. Significant heat waste on DC-DC, battery drops abruptly from 15% to 0%.*
* **UGreen Qi2 – Black (10,000 mAh / 37 Wh)** — **25.34 Wh (68.5%)** | **119.1 Wh/kg** | *Wireless coil circuitry and thermal shielding create continuous parasitic losses on wired output.*

---

### 🛑 F-Tier: Critical Hardware & Firmware Flaws

* **TRONIC PD/QC (Lidl - 10,000 mAh / 37 Wh)** 🗑️  
  **Measured:** 18.20 Wh | **Efficiency:** **49.2%** 🔴 *(18.8 Wh lost entirely to waste heat)*
  * **Lying State-of-Charge Gauge:** Displays 4 solid LEDs while continuing to draw 6W in an infinite CV charge stage.
  * **Defective Minimum-Load Detection:** Abruptly cuts output below 2.5W loads.

---

## 📊 Comprehensive Energy Density Ranking

| Rank | Model | Rated Wh | Measured Wh | Efficiency | Weight | Energy Density | Cell Architecture |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| 🥇 **1.** | **INIU 45W for iPhone (20k)** | 74.0 Wh | 69.36 Wh | **93.7%** | 335.2 g | **206.9 Wh/kg** | High-Density Li-Po |
| 🥈 **2.** | **O2 Spark 35W (10k)** | 36.0 Wh | 28.97 Wh | **80.5%** | 173.9 g | **166.6 Wh/kg** | Li-Ion (2× 21700) |
| 🥉 **3.** | **Samsung 20k 45W (EB-P4520)** | 74.0 Wh | 64.01 Wh | **86.5%** | 400.4 g | **159.9 Wh/kg** | Li-Po Pouch |
| **4.** | **AlzaPower Metal 40k** | 148.0 Wh | 119.69 Wh | **80.9%** | 790.9 g | **151.3 Wh/kg** | Li-Po / Li-Ion |
| **5.** | **AlzaPower Parade Gen2 27k (100W)** | 99.9 Wh | 80.47 Wh | **80.5%** | 532.8 g | **151.0 Wh/kg** | Li-Po Pouch |
| **6.** | **UGreen 145W (25k - 90597A)** | 90.0 Wh | 74.49 Wh | **82.8%** | 493.5 g | **150.9 Wh/kg** | Li-Ion (5× 21700) |
| **7.** | **AlzaPower Parade 22.5W (20k)** | 74.0 Wh | 62.27 Wh | **84.2%** | 415.0 g | **150.1 Wh/kg** | Li-Po Pouch |
| **8.** | **WG 20+ (20k)** | 74.0 Wh | 62.74 Wh | **84.8%** | 421.0 g | **149.0 Wh/kg** | Li-Po Pouch |
| **9.** | **O2 Built-in Cables 20W (10k)** | 37.0 Wh | 30.48 Wh | **82.4%** | 205.0 g | **148.7 Wh/kg** | Li-Po Pouch |
| **10.** | **Vention 165W TFT (20k)** | 74.0 Wh | 61.62 Wh | **83.3%** | 439.7 g | **140.1 Wh/kg** | Li-Ion (21700) |
| **11.** | **WG 10k QC3.0/PD/SM** | 37.0 Wh | 30.10 Wh | **81.4%** | 220.0 g | **136.8 Wh/kg** | Li-Po Pouch |
| **12.** | **Samsung 10k 25W PD (Beige)** | 37.0 Wh | 30.00 Wh | **81.1%** | 222.0 g | **135.1 Wh/kg** | Li-Po Pouch |
| **13.** | **AlzaPower Garnet 20k (White)** | 74.0 Wh | 54.72 Wh | **73.9%** | 415.0 g | **131.9 Wh/kg** | Li-Po Pouch |
| **14.** | **CUKTECH 45W (20k)** | 74.0 Wh | 64.09 Wh | **86.6%** | 496.9 g | **129.0 Wh/kg** | Li-Ion |
| **15.** | **Pink Ineo (5k)** | 18.5 Wh | 15.71 Wh | **84.9%** | 126.4 g | **124.3 Wh/kg** | Li-Po (Cute Pink) |
| **16.** | **Samsung 10k Wireless** | 37.0 Wh | 29.79 Wh | **80.5%** | 240.0 g | **124.1 Wh/kg** | Li-Po + Qi coil |
| **17.** | **AlzaPower Qi2 Ultra Slim (5k)** | 18.5 Wh | 15.30 Wh | **82.7%** | 125.2 g | **122.2 Wh/kg** | Ultra-slim Li-Po |
| **18.** | **UGreen Qi2 – Black (10k)** | 37.0 Wh | 25.34 Wh | **68.5%** | 212.8 g | **119.1 Wh/kg** | Li-Po + Qi2 coil |
| **19.** | **ROMOSS 65W (27k)** | 99.9 Wh | 75.44 Wh | **75.5%** | 677.5 g | **111.4 Wh/kg** | Li-Po / High-Cap |
| **20.** | **Vention Cables – Yellow (5k)** | 18.5 Wh | 14.10 Wh | **76.2%** | 129.2 g | **109.1 Wh/kg** | Li-Po Pouch |
| **21.** | **AlzaPower Vision 10k (100W)** | 36.0 Wh | 33.15 Wh | **92.1%** | 345.8 g | **95.9 Wh/kg** | Li-Ion + display |
| 🛑 **22.** | **TRONIC PD/QC (Lidl 10k)** | 37.0 Wh | 18.20 Wh | **49.2%** | 219.8 g | **82.8 Wh/kg** | Low-grade Li-Po |
