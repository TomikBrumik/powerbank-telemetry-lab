# 🔋 Powerbank Telemetry & Efficiency Benchmark Lab

[![Dataset: CSV](https://img.shields.io/badge/Dataset-CSV-green.svg)](powerbank_telemetry_database.csv)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Testbench: ATORCH DL24P](https://img.shields.io/badge/Testbench-ATORCH%20DL24P-orange.svg)](#)

A publicly accessible, standardized telemetry database and engineering benchmark for portable powerbanks. All units undergo controlled constant-current/constant-power discharge tests to expose real usable energy, DC-DC converter efficiency, thermal behavior, and BMS limits.

---

## 🔬 Testing Methodology & Cabling Standards

* **Hardware Testbench:** ATORCH DL24P Programmable Electronic DC Load.
* **Continuous Monitoring:** Real-time logging of terminal voltage, line current, DCIR (internal resistance), and thermal dissipation.
* **Discharge Profile:** Constant Current (`CC` @ 2.000 A / 5.0 V baseline nominal).

### 🔌 Harness & Cabling Evolution:
1. **Integrated Built-in Cables:** Tested directly using the factory-attached cable (zero extraneous connection losses).
2. **USB-A Port Models:** Tested via low-resistance **30cm INIU USB-A** connection.
3. **Legacy USB-C Baseline (1m Vention):** Initial pure USB-C tests used a **1m Vention 5Gbps USB-C** cable with `< 4.5V` cut-off. High trace resistance caused line drops (~0.45V sag) leading to premature DL24P trigger stops.
4. **New Standardized Method (30cm ADOL USB-C to C):** All pure USB-C powerbanks are being transitioned to a calibrated **30cm ADOL USB-C to C** cable with a lowered cut-off threshold of `< 3.8V` to capture true cell exhaustion.
   * *First Completed Re-Test:* **Samsung 20,000mAh 45W (EB-P4520)** completed on the new method, gaining +10.03 Wh (efficiency improved from 73.0% to **86.5%**, placing it into S-Tier). Remaining USB-C units are being actively re-benchmarked.

* **Electrical Efficiency Metric:**
  $$\text{Efficiency } (\%) = \left( \frac{\text{Measured Output Energy (Wh)}}{\text{Rated Battery Pack Energy (Wh)}} \right) \times 100$$
* **Gravimetric Energy Density:**
  $$\text{Energy Density } (\text{Wh/kg}) = \frac{\text{Measured Output Energy (Wh)}}{\text{Total Unit Weight (kg)}}$$

---

## 🏆 Tier List Classification

### 🥇 S-Tier: Engineering Excellence (Sync Buck-Boost & Premium Chemistry)

* **INIU 45W Power Bank for iPhone (20,000 mAh / 74 Wh)** 👑  
  **Measured:** 69.36 Wh (14,291 mAh) | **Efficiency:** **93.7%** *(All-time lab record)* | **Weight:** 335.2 g | **Density:** **206.9 Wh/kg**  
  *Built-in cable; ultra-compact high-density Li-Po architecture; exceptionally efficient synchronous DC-DC converter.*
* **AlzaPower Vision 10k PD 100W (10,000 mAh / 36 Wh)** 💡  
  **Measured:** 32.94 Wh (6,593 mAh) | **Efficiency:** **91.5%** *(Avg of 2 units)* | **Weight:** 345.8 g  
  *Tested via 30cm INIU USB-A; uncompromised rail stability throughout discharge; solid aluminum-polycarbonate chassis with TFT display.*
* **CUKTECH 20k 45W (20,000 mAh / 74 Wh)** 🏆  
  **Measured:** 64.09 Wh (12,822 mAh) | **Efficiency:** **86.6%** | **Weight:** 496.9 g  
  *Built-in cable; synchronous buck-boost topology (ZMI/Xiaomi lineage); minimal voltage ripple, precise microprocessor line telemetry.*
* **Samsung 20,000mAh 45W PD SFC 2.0 (EB-P4520) (20,000 mAh / 74 Wh)** ⚡  
  **Measured:** 64.01 Wh (12,793 mAh) | **Efficiency:** **86.5%** | **Weight:** 400.4 g | **Density:** **159.9 Wh/kg**  
  *Re-tested with NEW 30cm ADOL USB-C method (<3.8V cut-off); triple USB-C 45W PPS architecture; delivered 12,793 mAh across 6h 23m.*
* **UGreen 145W 25k (25,000 mAh / 90 Wh - 90597A)** 👑  
  **Measured:** 75.23 Wh | **Sustained Load:** 100W (92.59W real @ 18.5V / 5.0A) | **Efficiency:** **83.6%** | **Peak Temp:** 35.3°C  
  *Tested via 30cm INIU USB-A; industrial 5× 21700 cylindrical cells with ultra-low DCIR; firm 5.2A OCP limit.*
* **Vention 165W TFT 20k (20,000 mAh / 74 Wh)** 📺  
  **Measured:** 61.62 Wh (11,958 mAh) | **Efficiency:** **83.3%** | **Weight:** 439.7 g  
  *Tested via 30cm INIU USB-A; independent DC-DC rail design eliminates port handshake resets; dedicated telemetry chip feeds color TFT panel.*
* **AlzaPower Metal 40k (40,000 mAh / 148 Wh)** 🏗️  
  **Measured:** 119.69 Wh | **Efficiency:** **80.9%** | **Weight:** 790.9 g  
  *Tested via 30cm INIU USB-A; heavy extruded aluminum chassis serves as a full heatsink; zero thermal throttling across >12h run.*
* **O2 Spark 35W with Built-in Cable (10,000 mAh / 36 Wh)** ⚡  
  **Measured:** 28.97 Wh | **Efficiency:** **80.5%** | **Weight:** 173.9 g | **Density:** **166.6 Wh/kg**  
  *Built-in cable; 2S cell architecture (2× 21700, 7.2V / 5k mAh) halves input stage current to drastically reduce $I^2R$ resistive losses.*

---

### 🥈 A-Tier: Reliable Workhorses & Solid DC-DC Regulation

* **O2 Power Bank 10k 20W PD 3.0/QC (10,000 mAh / 37 Wh)** — **30.48 Wh (82.4%)** | **148.7 Wh/kg** | *Built-in flex cables; clean analog OCP cutting at 2.4A on 9V rail.*
* **WG 10k QC3.0/PD/SM (10,000 mAh / 37 Wh)** — **30.10 Wh (81.4%)** | **136.8 Wh/kg** | *Tested via 30cm INIU USB-A; firm rail regulation without transient voltage spikes.*
* **Samsung 10,000mAh 25W PD Beige (10,000 mAh / 37 Wh)** — **30.00 Wh (81.1%)** | **135.1 Wh/kg** | *Tested via 1m Vention (Stop 4.0V); high-efficiency 25W PPS/PD converter; 6,551 mAh in 3h 16m.*
* **AlzaPower Parade 22.5W (20,000 mAh / 74 Wh)** — **59.46 Wh (80.4%)** | **144.7 Wh/kg** | *Tested via 30cm INIU USB-A; standard Li-Po pouch workhorse; uninterrupted 22.5W delivery.*
* **WG 20+ (20,000 mAh / 74 Wh)** — **56.74 Wh (76.7%)** | **134.8 Wh/kg** | *Tested via 30cm INIU USB-A; conservative analog OCP (+15% trip) protecting pouch cells.*
* **AlzaPower Garnet 20k 22.5W White (20,000 mAh / 74 Wh)** — **55.98 Wh (75.6%)** | **134.0 Wh/kg** | *Tested via 30cm INIU USB-A; proven Li-Po pouch module with oval LED digital readout.*

---

### 🥉 B-Tier: Compact Wireless, High-Capacity & Specialized Peripherals

* **AlzaPower Qi2 Ultra Slim (5,000 mAh / 18.5 Wh)** — **14.36 Wh (77.6%)** | **114.7 Wh/kg** | *1m Vention USB-C; full Qi2 15W MPP profile with active coil thermal monitoring. (ADOL re-test queued)*
* **Vention with Cables – Yellow (5,000 mAh / 18.5 Wh)** — **14.10 Wh (76.2%)** | **109.1 Wh/kg** | *Built-in cable; minor voltage sag under sustained current draws exceeding 2.0A on 5V rail.*
* **AlzaPower Parade Gen2 27k PD 100W (27,000 mAh / 99.9 Wh)** — **73.34 Wh (73.4%)** | **137.6 Wh/kg** | *Tested via 30cm INIU USB-A; heavy-duty 100W buck-boost converter; increased conversion heat under load.*
* **Pink Qi2 / MagSafe (5,000 mAh / 18.5 Wh)** — **13.56 Wh (73.3%)** | **107.3 Wh/kg** | *1m Vention USB-C; standard 15W Qi2 / 18W PD; early thermal foldback on magnetic ring. (ADOL re-test queued)*
* **Samsung Wireless EB-U1200CS (10,000 mAh / 37 Wh)** — **26.85 Wh (72.6%)** | **114.9 Wh/kg** | *1m Vention USB-C; legacy AFC protocol drops to 2.4W; elevated standby parasitic drain. (ADOL re-test queued)*
* **ROMOSS 65W Fast Charge (27,000 mAh / 99.9 Wh)** — **69.62 Wh (69.7%)** | **102.8 Wh/kg** | *Tested via 30cm INIU USB-A; sustained 65W PD capability offset by higher step-up losses.*
* **UGreen Qi2 – Black (10,000 mAh / 37 Wh)** — **25.50 Wh (68.9%)** | **119.9 Wh/kg** | *1m Vention USB-C; high baseline losses in Qi2 wireless bridge circuit; USB-C capped at 3.1A. (ADOL re-test queued)*

---

### 🛑 F-Tier: Critical Hardware & Firmware Flaws

* **TRONIC PD/QC (Lidl - 10,000 mAh / 37 Wh)** 🗑️  
  **Measured:** 18.20 Wh (3,663 mAh) | **Efficiency:** **49.2%** 🔴 *(18.8 Wh lost entirely to waste heat)*
  * **Lying SoC Gauge:** Displays 4 solid LEDs while continuing to draw 6W in infinite CV charge stage.
  * **Defective Minimum-Load Detection:** Abruptly cuts output below 2.5W loads (500mA @ 5V).
  * **Severe Parasitic Discharge:** Quiescent drain fully depletes cells within weeks of storage.

---

## 📊 Comprehensive Energy Density & Telemetry Ranking

| Rank | Model | Rated Wh | Measured Wh | Efficiency | Weight | Energy Density | Cabling Standard |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| 🥇 **1.** | **INIU 45W for iPhone (20k)** | 74.0 Wh | 69.36 Wh | **93.7%** | 335.2 g | **206.9 Wh/kg** | Built-in USB-C Cable |
| 🥈 **2.** | **O2 Spark 35W (10k)** | 36.0 Wh | 28.97 Wh | **80.5%** | 173.9 g | **166.6 Wh/kg** | Built-in USB-C Cable |
| 🥉 **3.** | **Samsung 20,000mAh 45W (EB-P4520)** | 74.0 Wh | 64.01 Wh | **86.5%** | 400.4 g | **159.9 Wh/kg** | **30cm ADOL USB-C (New Method)** |
| **4.** | **UGreen 145W (25k - 90597A)** | 90.0 Wh | 75.23 Wh | **83.6%** | 493.5 g | **152.4 Wh/kg** | 30cm INIU USB-A |
| **5.** | **AlzaPower Metal 40k** | 148.0 Wh | 119.69 Wh | **80.9%** | 790.9 g | **151.3 Wh/kg** | 30cm INIU USB-A |
| **6.** | **O2 Built-in Cables 20W (10k)** | 37.0 Wh | 30.48 Wh | **82.4%** | 205.0 g | **148.7 Wh/kg** | Built-in Flex Cables |
| **7.** | **AlzaPower Parade 22.5W (20k)** | 74.0 Wh | 59.46 Wh | **80.4%** | 410.9 g | **144.7 Wh/kg** | 30cm INIU USB-A |
| **8.** | **Vention 165W TFT (20k)** | 74.0 Wh | 61.62 Wh | **83.3%** | 439.7 g | **140.1 Wh/kg** | 30cm INIU USB-A |
| **9.** | **AlzaPower Parade Gen2 27k (100W)** | 99.9 Wh | 73.34 Wh | **73.4%** | 532.8 g | **137.6 Wh/kg** | 30cm INIU USB-A |
| **10.** | **WG 10k QC3.0/PD/SM** | 37.0 Wh | 30.10 Wh | **81.4%** | 220.0 g | **136.8 Wh/kg** | 30cm INIU USB-A |
| **11.** | **Samsung 10k 25W PD (Beige)** | 37.0 Wh | 30.00 Wh | **81.1%** | 222.0 g | **135.1 Wh/kg** | 1m Vention USB-C (Stop 4.0V) |
| **12.** | **WG 20+ (20k)** | 74.0 Wh | 56.74 Wh | **76.7%** | 421.0 g | **134.8 Wh/kg** | 30cm INIU USB-A |
| **13.** | **AlzaPower Garnet 20k (White)** | 74.0 Wh | 55.98 Wh | **75.6%** | 417.7 g | **134.0 Wh/kg** | 30cm INIU USB-A |
| **14.** | **CUKTECH 45W (20k)** | 74.0 Wh | 64.09 Wh | **86.6%** | 496.9 g | **129.0 Wh/kg** | Built-in USB-C Cable |
| **15.** | **UGreen Qi2 – Black (10k)** | 37.0 Wh | 25.50 Wh | **68.9%** | 212.8 g | **119.9 Wh/kg** | 1m Vention USB-C *(Queued for ADOL)* |
| **16.** | **Samsung Wireless EB-U1200CS (10k)** | 37.0 Wh | 26.85 Wh | **72.6%** | 233.6 g | **114.9 Wh/kg** | 1m Vention USB-C *(Queued for ADOL)* |
| **17.** | **AlzaPower Qi2 Ultra Slim (5k)** | 18.5 Wh | 14.36 Wh | **77.6%** | 125.2 g | **114.7 Wh/kg** | 1m Vention USB-C *(Queued for ADOL)* |
| **18.** | **Vention Cables – Yellow (5k)** | 18.5 Wh | 14.10 Wh | **76.2%** | 129.2 g | **109.1 Wh/kg** | Built-in Flex Cables |
| **19.** | **Pink Qi2 / MagSafe (5k)** | 18.5 Wh | 13.56 Wh | **73.3%** | 126.4 g | **107.3 Wh/kg** | 1m Vention USB-C *(Queued for ADOL)* |
| **20.** | **ROMOSS 65W (27k)** | 99.9 Wh | 69.62 Wh | **69.7%** | 677.5 g | **102.8 Wh/kg** | 30cm INIU USB-A |
| **21.** | **AlzaPower Vision 10k (100W)** | 36.0 Wh | 32.94 Wh | **91.5%** | 345.8 g | **95.3 Wh/kg** | 30cm INIU USB-A |
| 🛑 **22.** | **TRONIC PD/QC (Lidl 10k)** | 37.0 Wh | 18.20 Wh | **49.2%** | 219.8 g | **82.8 Wh/kg** | 1m Vention USB-C |

---

## 📥 Raw Data Access

Download the complete machine-readable dataset:  
👉 [`powerbank_telemetry_database.csv`](powerbank_telemetry_database.csv)
