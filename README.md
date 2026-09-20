# 🔋 Powerbank Telemetry & Efficiency Benchmark Lab

[![Dataset: CSV](https://img.shields.io/badge/Dataset-CSV-green.svg)](powerbank_telemetry_database.csv)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Testbench: ATORCH DL24P](https://img.shields.io/badge/Testbench-ATORCH%20DL24P-orange.svg)](#)

A publicly accessible, standardized telemetry database and engineering benchmark for portable powerbanks. All units undergo controlled constant-current/constant-power discharge tests to expose real usable energy, DC-DC converter efficiency, thermal behavior, and BMS limits.

*Note on Volumetric Density (Wh/liter): Gravimetric density (Wh/kg) is tracked precisely via digital scale. Volumetric density (Wh/L) is currently being estimated and will be added via caliper measurements soon!*

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
* **AlzaPower Vision 100W (10,000 mAh / 36 Wh)** 💡  
  **Measured:** 33.04 Wh | **Efficiency:** **91.8%** *(Avg of 2 units)* | **Weight:** 343.6 g | **Density:** **96.2 Wh/kg**  
  *Uncompromised rail stability throughout discharge; solid aluminum-polycarbonate chassis with integrated TFT display and flashlight.*
* **ChoeTech Digital 22.5W (50,000 mAh / 185 Wh)** 🔋  
  **Measured:** 166.75 Wh | **Efficiency:** **90.1%** | **Weight:** 955.3 g | **Density:** **174.6 Wh/kg**  
  *16h runtime, massive capacity.*
* **CUKTECH 45W (20,000 mAh / 74 Wh)** 🏆  
  **Measured:** 64.09 Wh | **Efficiency:** **86.6%** | **Weight:** 496.9 g | **Density:** **129.0 Wh/kg**  
  *Synchronous buck-boost topology; minimal voltage ripple, precise microprocessor line telemetry.*
* **Samsung 20,000mAh 45W PD SFC 2.0 (EB-P4520) (20,000 mAh / 74 Wh)** ⚡  
  **Measured:** 64.01 Wh | **Efficiency:** **86.5%** | **Weight:** 400.4 g | **Density:** **159.9 Wh/kg**  
  *Re-tested (USB-C 30cm, <3.8V stop), 3x USB-C 45W SFC 2.0.*
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
* **WG 10k QC/PD** — **30.10 Wh (81.4%)** | **136.8 Wh/kg** | *Clean rail regulation without transient spikes.*
* **Samsung 10k 25W PD (Beige)** — **30.00 Wh (81.1%)** | **135.1 Wh/kg** | *High-efficiency 25W PPS/PD converter.*
* **AlzaPower WorkMate 100W (20k)** — **59.99 Wh (81.1%)** | **138.6 Wh/kg** | *Solid 100W performance.*
* **AlzaPower Metal (40k)** — **119.69 Wh (80.9%)** | **151.3 Wh/kg** | *Massive aluminum chassis, zero thermal sag.*
* **AlzaPower Parade Gen2 100W (27k)** — **80.47 Wh (80.6%)** | **151.0 Wh/kg** | *Robust 100W chassis.*
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

---

## 📊 Comprehensive Energy Density Ranking

| Rank | Tier | Model | Rated Wh | Measured Wh | Efficiency | Weight | Energy Density |
| :---: | :---: | :--- | :---: | :---: | :---: | :---: | :---: |
| 🥇 1. | S | INIU 45W w/ Built-in Cable (20k) | 74.0 Wh | 69.36 Wh | **93.7%** | 335.2 g | **206.9 Wh/kg** |
| 🥈 2. | S | INIU Pocket 10k (P50) | 36.0 Wh | 30.56 Wh | **84.9%** | 162.0 g | **188.6 Wh/kg** |
| 🥉 3. | S | ChoeTech Digital 22.5W (50k) | 185.0 Wh | 166.75 Wh | **90.1%** | 955.3 g | **174.6 Wh/kg** |
| 4. | A | O2 Spark 35W (10k) | 36.0 Wh | 28.97 Wh | **80.5%** | 173.9 g | **166.6 Wh/kg** |
| 5. | B | Vention Mini 35W w/ Cable (10k) | 38.5 Wh | 29.15 Wh | **75.7%** | 176.5 g | **165.2 Wh/kg** |
| 6. | A | PanzerGlass Empower Qi2 (10k) | 38.5 Wh | 31.80 Wh | **82.6%** | 195.4 g | **162.7 Wh/kg** |
| 7. | S | Samsung 20k 45W (EB-P4520) | 74.0 Wh | 64.01 Wh | **86.5%** | 400.4 g | **159.9 Wh/kg** |
| 8. | A | AlzaPower Metal 40k | 148.0 Wh | 119.69 Wh | **80.9%** | 790.9 g | **151.3 Wh/kg** |
| 9. | A | AlzaPower Parade Gen2 100W (27k) | 99.9 Wh | 80.47 Wh | **80.6%** | 532.8 g | **151.0 Wh/kg** |
| 10. | A | UGreen 145W (25k) | 90.0 Wh | 74.49 Wh | **82.8%** | 493.5 g | **150.9 Wh/kg** |
| 11. | S | AlzaPower Parade 22.5W (20k) | 74.0 Wh | 62.27 Wh | **84.1%** | 415.0 g | **150.0 Wh/kg** |
| 12. | S | WG 20+ (20k) | 74.0 Wh | 62.74 Wh | **84.8%** | 421.0 g | **149.0 Wh/kg** |
| 13. | A | O2 Built-in Cable 10k | 37.0 Wh | 30.48 Wh | **82.4%** | 205.0 g | **148.7 Wh/kg** |
| 14. | S | Vention 165W TFT (20k) | 74.0 Wh | 61.62 Wh | **83.3%** | 439.7 g | **140.1 Wh/kg** |
| 15. | A | AlzaPower WorkMate 100W (20k) | 74.0 Wh | 59.99 Wh | **81.1%** | 432.8 g | **138.6 Wh/kg** |
| 16. | A | WG 10k QC/PD | 37.0 Wh | 30.10 Wh | **81.4%** | 220.0 g | **136.8 Wh/kg** |
| 17. | A | Samsung 10k 25W PD (Beige) | 37.0 Wh | 30.00 Wh | **81.1%** | 222.0 g | **135.1 Wh/kg** |
| 18. | B | AlzaPower Garnet 20k (White) | 74.0 Wh | 54.72 Wh | **73.9%** | 415.0 g | **131.9 Wh/kg** |
| 19. | B | AlzaPower Parade Gen2 22.5W (20k) | 75.0 Wh | 53.86 Wh | **71.8%** | 409.5 g | **131.5 Wh/kg** |
| 20. | S | CUKTECH 45W (20k) | 74.0 Wh | 64.09 Wh | **86.6%** | 496.9 g | **129.0 Wh/kg** |
| 21. | S | AlzaPower Vision 100W (20k) | 72.0 Wh | 60.62 Wh | **84.2%** | 477.9 g | **126.8 Wh/kg** |
| 22. | S | Vention Magnetic Pink (5k) | 18.5 Wh | 15.71 Wh | **84.9%** | 126.4 g | **124.3 Wh/kg** |
| 23. | A | Samsung 10k Wireless | 37.0 Wh | 29.79 Wh | **80.5%** | 240.0 g | **124.1 Wh/kg** |
| 24. | A | AlzaPower Qi2 Slim (5k) | 18.5 Wh | 15.30 Wh | **82.7%** | 125.2 g | **122.2 Wh/kg** |
| 25. | A | AlzaPower Vision 10k (30W) | 36.0 Wh | 28.46 Wh | **79.1%** | 237.7 g | **119.7 Wh/kg** |
| 26. | B | UGreen Qi2 Black (10k) | 37.0 Wh | 25.34 Wh | **68.5%** | 212.8 g | **119.1 Wh/kg** |
| 27. | B | ROMOSS 65W Fast Charge (27k) | 99.9 Wh | 75.44 Wh | **75.5%** | 677.5 g | **111.4 Wh/kg** |
| 28. | B | Vention Cables Yellow (5k) | 18.5 Wh | 14.10 Wh | **76.2%** | 129.2 g | **109.1 Wh/kg** |
| 29. | S | AlzaPower Vision 100W (10k) | 36.0 Wh | 33.04 Wh | **91.8%** | 343.6 g | **96.2 Wh/kg** |
| 30. | F | TRONIC 10k (Lidl) | 37.0 Wh | 18.20 Wh | **49.2%** | 219.8 g | **82.8 Wh/kg** |
