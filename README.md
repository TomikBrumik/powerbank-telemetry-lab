# 🔋 Powerbank Telemetry & Efficiency Benchmark Lab

A publicly accessible, standardized telemetry database and engineering benchmark for portable powerbanks. All units undergo controlled constant-current/constant-power discharge tests to expose real usable energy, DC-DC converter efficiency, thermal behavior, and BMS limits.

---

## 🔬 Testing Methodology & Equipment

* **Hardware Testbench:** ATORCH DL24P Programmable Electronic DC Load.
* **Continuous Monitoring:** Real-time logging of terminal voltage, line current, DCIR (internal resistance), and thermal dissipation.
* **Electrical Efficiency Metric:**

$$\text{Efficiency } (\%) = \left( \frac{\text{Measured Output Energy (Wh)}}{\text{Rated Battery Pack Energy (Wh)}} \right) \times 100$$


* **Gravimetric Energy Density:**

$$\text{Energy Density } (\text{Wh/kg}) = \frac{\text{Measured Output Energy (Wh)}}{\text{Total Unit Weight (kg)}}$$



---

## 🏆 Tier List Classification

### 🥇 S-Tier: Engineering Excellence (Sync Buck-Boost & Premium Chemistry)

* **INIU 45W Power Bank for iPhone (20,000 mAh / 74 Wh)** 👑
**Measured:** 69.36 Wh (14,291 mAh) | **Efficiency:** **93.7%** *(All-time lab record)* | **Weight:** 335.2 g | **Density:** **206.9 Wh/kg**
*Ultra-compact high-density Li-Po architecture; exceptionally efficient synchronous DC-DC converter with negligible internal resistance.*
* **AlzaPower Vision 10k PD 100W (10,000 mAh / 36 Wh)** 💡
**Measured:** 32.94 Wh (6,593 mAh) | **Efficiency:** **91.5%** *(Avg of 2 units)* | **Weight:** 345.8 g
*Uncompromised rail stability throughout discharge; solid aluminum-polycarbonate chassis with integrated TFT display and flashlight.*
* **CUKTECH 20k 45W (20,000 mAh / 74 Wh)** 🏆
**Measured:** 64.09 Wh (12,822 mAh) | **Efficiency:** **86.6%** | **Weight:** 496.9 g
*Synchronous buck-boost topology (ZMI/Xiaomi lineage); minimal voltage ripple, precise microprocessor line telemetry, hard cutoff only at critical thresholds.*
* **UGreen 145W 25k (25,000 mAh / 90 Wh - 90597A)** 👑
**Measured:** 75.23 Wh | **Sustained Load:** 100W (92.59W real @ 18.5V / 5.0A) | **Efficiency:** **83.6%** | **Peak Temp:** 35.3°C
*Industrial 5× 21700 cylindrical cells with ultra-low DCIR; firm 5.2A OCP limit; full PD 3.0 / PPS compatibility.*
* **Vention 165W TFT 20k (20,000 mAh / 74 Wh)** 📺
**Measured:** 61.62 Wh (11,958 mAh) | **Efficiency:** **83.3%** | **Weight:** 439.7 g
*Independent DC-DC rail design eliminates port handshake resets; dedicated telemetry chip feeds real-time color TFT panel.*
* **AlzaPower Metal 40k (40,000 mAh / 148 Wh)** 🏗️
**Measured:** 119.69 Wh | **Efficiency:** **80.9%** | **Weight:** 790.9 g
*Heavy extruded aluminum chassis serves as a full-contact heatsink for MOSFETs and power inductors; zero thermal throttling across >12h run.*
* **O2 Spark 35W with Built-in Cable (10,000 mAh / 36 Wh)** ⚡
**Measured:** 28.97 Wh | **Efficiency:** **80.5%** | **Weight:** 173.9 g | **Density:** **166.6 Wh/kg**
*2S cell architecture (2× 21700, 7.2V / 5,000mAh) halves input stage current to drastically reduce $I^2R$ resistive thermal losses.*

---

### 🥈 A-Tier: Reliable Workhorses & Solid DC-DC Regulation

* **O2 Power Bank 10k 20W PD 3.0/QC (10,000 mAh / 37 Wh)** — **30.48 Wh (82.4%)** | **148.7 Wh/kg** | *Low-resistance integrated flex cables; clean analog OCP cutting at 2.4A on 9V rail.*
* **WG 10k QC3.0/PD/SM (10,000 mAh / 37 Wh)** — **30.10 Wh (81.4%)** | **136.8 Wh/kg** | *Firm rail regulation without transient voltage spikes during dynamic load switching.*
* **AlzaPower Parade 22.5W (20,000 mAh / 74 Wh)** — **59.46 Wh (80.4%)** | **144.7 Wh/kg** | *Standard Li-Po pouch workhorse; uninterrupted 22.5W delivery with moderate thermal headroom.*
* **WG 20+ (20,000 mAh / 74 Wh)** — **56.74 Wh (76.7%)** | **134.8 Wh/kg** | *Conservative analog over-current protection (+15% trip) designed for extended pouch cell longevity.*
* **AlzaPower Garnet 20k 22.5W White (20,000 mAh / 74 Wh)** — **55.98 Wh (75.6%)** | **134.0 Wh/kg** | *Proven Li-Po pouch module with oval LED digital readout; consistent 22.5W PD/QC output.*

---

### 🥉 B-Tier: Compact Wireless, High-Capacity & Specialized Peripherals

* **AlzaPower Qi2 Ultra Slim (5,000 mAh / 18.5 Wh)** — **14.36 Wh (77.6%)** | **114.7 Wh/kg** | *Full Qi2 15W MPP magnetic profile with closed-loop coil thermal monitoring.*
* **Vention with Cables – Yellow (5,000 mAh / 18.5 Wh)** — **14.10 Wh (76.2%)** | **109.1 Wh/kg** | *Minor voltage sag under sustained current draws exceeding 2.0A on 5V rail.*
* **AlzaPower Parade Gen2 27k PD 100W (27,000 mAh / 99.9 Wh)** — **73.34 Wh (73.4%)** | **137.6 Wh/kg** | *Heavy-duty 100W buck-boost converter; increased conversion heat under load pulls efficiency to 73.4%.*
* **Pink Qi2 / MagSafe (5,000 mAh / 18.5 Wh)** — **13.56 Wh (73.3%)** | **107.3 Wh/kg** | *Standard 15W Qi2 / 18W PD; aggressive thermal foldback triggered by magnetic ring hotspot.*
* **Samsung 20,000mAh 25W PD EB-P5300 (20,000 mAh / 74 Wh)** — **53.98 Wh (73.0%)** | **134.8 Wh/kg** | *Dual USB-C + USB-A configuration; solid construction delivering 11,694 mAh over 5h 50m runtime.*
* **Samsung Wireless EB-U1200CS (10,000 mAh / 37 Wh)** — **26.85 Wh (72.6%)** | **114.9 Wh/kg** | *Legacy AFC protocol drops to 2.4W on non-Samsung sinks; elevated standby parasitic drain.*
* **ROMOSS 65W Fast Charge (27,000 mAh / 99.9 Wh)** — **69.62 Wh (69.7%)** | **102.8 Wh/kg** | *Sustained 65W PD capability offset by higher step-up losses and significant mass.*
* **UGreen Qi2 – Black (10,000 mAh / 37 Wh)** — **25.50 Wh (68.9%)** | **119.9 Wh/kg** | *High baseline losses in Qi2 wireless bridge circuit; USB-C port hard-capped at 3.1A (5V).*

---

### 🛑 F-Tier: Critical Hardware & Firmware Flaws

* **TRONIC PD/QC (Lidl - 10,000 mAh / 37 Wh)** 🗑️
**Measured:** 18.20 Wh (3,663 mAh) | **Efficiency:** **49.2%** 🔴 *(18.8 Wh lost entirely to waste heat)*
* **Lying State-of-Charge Gauge:** Displays 4 solid LEDs while continuing to draw 6W in an infinite CV charge stage.
* **Defective Minimum-Load Detection:** Abruptly cuts output below 2.5W loads (500mA @ 5V).
* **Severe Parasitic Discharge:** High quiescent drain fully depletes the cells within weeks of storage.



---

## 📊 Comprehensive Energy Density & Telemetry Ranking

| Rank | Model | Rated Wh | Measured Wh | Efficiency | Weight | Energy Density | Cell Architecture |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 🥇 **1.** | **INIU 45W for iPhone (20k)** | 74.0 Wh | 69.36 Wh | **93.7%** | 335.2 g | **206.9 Wh/kg** | High-Density Li-Po |
| 🥈 **2.** | **O2 Spark 35W (10k)** | 36.0 Wh | 28.97 Wh | **80.5%** | 173.9 g | **166.6 Wh/kg** | Li-Ion (2× 21700) |
| 🥉 **3.** | **UGreen 145W (25k - 90597A)** | 90.0 Wh | 75.23 Wh | **83.6%** | 493.5 g | **152.4 Wh/kg** | Li-Ion (5× 21700) |
| **4.** | **AlzaPower Metal 40k** | 148.0 Wh | 119.69 Wh | **80.9%** | 790.9 g | **151.3 Wh/kg** | Li-Po / Li-Ion |
| **5.** | **O2 Built-in Cables 20W (10k)** | 37.0 Wh | 30.48 Wh | **82.4%** | 205.0 g | **148.7 Wh/kg** | Li-Po Pouch |
| **6.** | **AlzaPower Parade 22.5W (20k)** | 74.0 Wh | 59.46 Wh | **80.4%** | 410.9 g | **144.7 Wh/kg** | Li-Po Pouch |
| **7.** | **Vention 165W TFT (20k)** | 74.0 Wh | 61.62 Wh | **83.3%** | 439.7 g | **140.1 Wh/kg** | Li-Ion (21700) |
| **8.** | **AlzaPower Parade Gen2 27k (100W)** | 99.9 Wh | 73.34 Wh | **73.4%** | 532.8 g | **137.6 Wh/kg** | Li-Po Pouch |
| **9.** | **WG 10k QC3.0/PD/SM** | 37.0 Wh | 30.10 Wh | **81.4%** | 220.0 g | **136.8 Wh/kg** | Li-Po Pouch |
| **10.** | **WG 20+ (20k)** | 74.0 Wh | 56.74 Wh | **76.7%** | 421.0 g | **134.8 Wh/kg** | Li-Po Pouch |
| **11.** | **Samsung 20k 25W (EB-P5300)** | 74.0 Wh | 53.98 Wh | **73.0%** | 400.4 g | **134.8 Wh/kg** | Li-Po Pouch |
| **12.** | **AlzaPower Garnet 20k (White)** | 74.0 Wh | 55.98 Wh | **75.6%** | 417.7 g | **134.0 Wh/kg** | Li-Po Pouch |
| **13.** | **CUKTECH 45W (20k)** | 74.0 Wh | 64.09 Wh | **86.6%** | 496.9 g | **129.0 Wh/kg** | Li-Ion |
| **14.** | **UGreen Qi2 – Black (10k)** | 37.0 Wh | 25.50 Wh | **68.9%** | 212.8 g | **119.9 Wh/kg** | Li-Po + Qi2 coil |
| **15.** | **Samsung Wireless EB-U1200CS (10k)** | 37.0 Wh | 26.85 Wh | **72.6%** | 233.6 g | **114.9 Wh/kg** | Li-Po + Qi coil |
| **16.** | **AlzaPower Qi2 Ultra Slim (5k)** | 18.5 Wh | 14.36 Wh | **77.6%** | 125.2 g | **114.7 Wh/kg** | Ultra-slim Li-Po |
| **17.** | **Vention Cables – Yellow (5k)** | 18.5 Wh | 14.10 Wh | **76.2%** | 129.2 g | **109.1 Wh/kg** | Li-Po Pouch |
| **18.** | **Pink Qi2 / MagSafe (5k)** | 18.5 Wh | 13.56 Wh | **73.3%** | 126.4 g | **107.3 Wh/kg** | Li-Po + Qi2 coil |
| **19.** | **ROMOSS 65W (27k)** | 99.9 Wh | 69.62 Wh | **69.7%** | 677.5 g | **102.8 Wh/kg** | Li-Po Pouch |
| **20.** | **AlzaPower Vision 10k (100W)** | 36.0 Wh | 32.94 Wh | **91.5%** | 345.8 g | **95.3 Wh/kg** | Li-Ion + display |
| 🛑 **21.** | **TRONIC PD/QC (Lidl 10k)** | 37.0 Wh | 18.20 Wh | **49.2%** | 219.8 g | **82.8 Wh/kg** | Low-grade Li-Po |

---

## 📥 Raw Data Access

Download the complete machine-readable dataset:

👉 [`powerbank_telemetry_database.csv`](https://www.google.com/search?q=powerbank_telemetry_database.csv)
