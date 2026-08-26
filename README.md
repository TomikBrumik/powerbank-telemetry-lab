# 🔋 Powerbank Telemetry & Efficiency Benchmark Lab

[![Dataset](https://img.shields.io/badge/Dataset-CSV-green.svg)](./powerbank_telemetry_database.csv)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Testbench](https://img.shields.io/badge/Testbench-ATORCH%20DL24P-orange.svg)]()

A publicly accessible, standardized telemetry database and engineering benchmark for portable powerbanks. All units undergo controlled constant-current/constant-power discharge tests to expose real usable energy, DC-DC converter efficiency, thermal behavior, and BMS limits.

---

## 🔬 Testing Methodology & Equipment

* **Hardware Testbench:** ATORCH DL24P Programmable Electronic DC Load.
* **Continuous Monitoring:** Real-time logging of terminal voltage, line current, DCIR (internal resistance), and thermal dissipation.
* **Electrical Efficiency Metric:**
  $$\text{Efficiency (\%)} = \left( \frac{\text{Measured Output Energy (Wh)}}{\text{Rated Battery Pack Energy (Wh)}} \right) \times 100$$
* **Gravimetric Energy Density:**
  $$\text{Energy Density (Wh/kg)} = \frac{\text{Measured Output Energy (Wh)}}{\text{Total Unit Weight (kg)}}$$

---

## 🏆 Tier List Classification

### 🥇 S-Tier: Engineering Excellence (Sync Buck-Boost & Premium Chemistry)
* **CUKTECH 45W (20,000 mAh / 74 Wh)** 🏆
  * **Measured:** `64.09 Wh` (12,822 mAh) | **Efficiency:** `86.6%` *(All-time lab record)*
  * Synchronous buck-boost converter (ZMI/Xiaomi pedigree); ultra-low voltage ripple and stellar passive cooling.
* **UGreen 145W (25,000 mAh / 90 Wh)** 👑
  * **Measured:** `75.23 Wh` | **Sustained Load:** `100W` (92.59W real @ 18.5V / 5.0A)
  * **Efficiency:** `83.6%` | **Peak Converter Temp:** `35.3°C`
  * Industrial 21700 cells with low DCIR; strict 5.2A OCP trip limit.
* **Vention 165W TFT (20,000 mAh / 74 Wh)** 📺
  * **Measured:** `61.62 Wh` (11,958 mAh) | **Efficiency:** `83.3%`
  * Independent DC-DC lines eliminate port resetting; integrated dedicated IC drives color TFT telemetry.
* **AlzaPower Metal 40k (40,000 mAh / 148 Wh)** 🏗️
  * **Measured:** `119.69 Wh` | **Efficiency:** `80.9%`
  * Heavy solid aluminum chassis acts as an integrated heatsink; zero thermal throttling over a >12-hour continuous run.
* **O2 Spark 35W (10,000 mAh / 37 Wh)** ⚡
  * **Measured:** `28.97 Wh` | **Efficiency:** `78.3%` | **Weight:** `173.9g`
  * **Energy Density:** `166.6 Wh/kg` *(Highest in the benchmark)*
  * 2S cell architecture (2× 21700) cuts input current to reduce $I^2R$ resistive heating losses.

---

### 🥈 A-Tier: Reliable Workhorses & Solid DC-DC Regulation
* **O2 with Built-in Cables (10,000 mAh / 37 Wh)** — `30.48 Wh` (**82.4%**) | 148.7 Wh/kg | Low-resistance flex cables, analog 2.4A OCP on 9V rail.
* **WG 10k QC3.0/PD (10,000 mAh / 37 Wh)** — `30.10 Wh` (**81.4%**) | 136.8 Wh/kg | Rock-solid rail stability without transient voltage spikes.
* **AlzaPower Parade 22.5W (20,000 mAh / 74 Wh)** — `59.46 Wh` (**80.4%**) | 144.7 Wh/kg | Li-Po pouch architecture, steady 22.5W output.
* **WG 20+ (20,000 mAh / 74 Wh)** — `56.74 Wh` (**76.7%**) | 134.8 Wh/kg | Conservative analog OCP (+15% trip) protecting cell cycle life.

---

### 🥉 B-Tier: Compact Wireless & Specialized Peripherals
* **AlzaPower Qi2 Ultra Slim (5,000 mAh / 18.5 Wh)** — `14.36 Wh` (**77.6%**) | 114.7 Wh/kg | Full Qi2 15W MPP magnetic profile, active coil thermal control.
* **Vention with Cables - Yellow (5,000 mAh / 18.5 Wh)** — `14.10 Wh` (**76.2%**) | 109.1 Wh/kg | Slight voltage sag under loads >2.0A on 5V rail.
* **Pink Qi2 / MagSafe (5,000 mAh / 18.5 Wh)** — `13.56 Wh` (**73.3%**) | 107.3 Wh/kg | Standard 15W wireless / 18W USB-C; early thermal throttle on magnetic ring.
* **Samsung Wireless EB-U1200CS (10,000 mAh / 37 Wh)** — `26.85 Wh` (**72.6%**) | 114.9 Wh/kg | Legacy AFC drops to 2.4W on standard devices; higher standby quiescent drain.
* **UGreen Qi2 Black (10,000 mAh / 37 Wh)** — `25.50 Wh` (**68.9%**) | 119.9 Wh/kg | Wireless coil dissipation drops efficiency <70%; USB-C capped at 3.1A (5V).

---

### 🛑 F-Tier: Critical Hardware & Firmware Flaws
* **TRONIC PD/QC (Lidl 10,000 mAh / 37 Wh)** 🗑️
  * **Measured:** `18.20 Wh` (3,663 mAh) | **Efficiency:** **49.2%** 🔴 *(18.8 Wh lost entirely to waste heat)*
  * **Broken CV Gauge:** Displays 4 solid LEDs while still consuming 6W in an endless CV phase.
  * **Faulty Low-Load Cutoff:** Shuts down unexpectedly below 2.5W loads (500mA @ 5V).
  * **Parasitic Self-Discharge:** High parasitic circuit drain drains cells within weeks of sitting idle.

---

## 📊 Comprehensive Energy Density & Telemetry Ranking

| Rank | Model | Rated Wh | Measured Wh | Efficiency | Weight | Energy Density | Cell Architecture |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| 🥇 1. | **O2 Spark 35W** | 37.0 Wh | 28.97 Wh | 78.3% | 173.9 g | **166.6 Wh/kg** | Li-Ion (2× 21700) |
| 🥈 2. | **UGreen 145W** | 90.0 Wh | 75.23 Wh | 83.6% | 493.5 g | **152.4 Wh/kg** | Li-Ion (21700) |
| 🥉 3. | **AlzaPower Metal 40k** | 148.0 Wh | 119.69 Wh | 80.9% | 790.9 g | **151.3 Wh/kg** | Li-Po / Li-Ion |
| 4. | **O2 Built-in Cables** | 37.0 Wh | 30.48 Wh | 82.4% | 205.0 g | **148.7 Wh/kg** | Li-Po Pouch |
| 5. | **AlzaPower Parade 22.5W** | 74.0 Wh | 59.46 Wh | 80.4% | 410.9 g | **144.7 Wh/kg** | Li-Po Pouch |
| 6. | **Vention 165W TFT** | 74.0 Wh | 61.62 Wh | 83.3% | 439.7 g | **140.1 Wh/kg** | Li-Ion (21700) |
| 7. | **WG 10k QC3.0/PD/SM** | 37.0 Wh | 30.10 Wh | 81.4% | 220.0 g | **136.8 Wh/kg** | Li-Po Pouch |
| 8. | **WG 20+** | 74.0 Wh | 56.74 Wh | 76.7% | 421.0 g | **134.8 Wh/kg** | Li-Po Pouch |
| 9. | **CUKTECH 45W** | 74.0 Wh | 64.09 Wh | 86.6% | 496.9 g | **129.0 Wh/kg** | Li-Ion |
| 10. | **UGreen Qi2 Black** | 37.0 Wh | 25.50 Wh | 68.9% | 212.8 g | **119.9 Wh/kg** | Li-Po + Qi2 coil |
| 11. | **Samsung EB-U1200CS** | 37.0 Wh | 26.85 Wh | 72.6% | 233.6 g | **114.9 Wh/kg** | Li-Po + Qi coil |
| 12. | **AlzaPower Qi2 Ultra Slim** | 18.5 Wh | 14.36 Wh | 77.6% | 125.2 g | **114.7 Wh/kg** | Ultra-slim Li-Po |
| 13. | **Vention Cables Yellow** | 18.5 Wh | 14.10 Wh | 76.2% | 129.2 g | **109.1 Wh/kg** | Li-Po Pouch |
| 14. | **Pink Qi2 / MagSafe** | 18.5 Wh | 13.56 Wh | 73.3% | 126.4 g | **107.3 Wh/kg** | Li-Po + Qi2 coil |
| 🛑 15. | **TRONIC PD/QC (Lidl)** | 37.0 Wh | 18.20 Wh | 49.2% | 219.8 g | **82.8 Wh/kg** | Low-grade Li-Po |

---

## 📥 Raw Data Access
Download the raw machine-readable dataset: [`powerbank_telemetry_database.csv`](./powerbank_telemetry_database.csv)
