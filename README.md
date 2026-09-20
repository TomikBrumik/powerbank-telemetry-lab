Hey everyone! 👋

I’ve spent the past few weeks running standardized continuous discharge tests on **30 different powerbank models** (from 5,000 mAh ultra-slims up to massive 50,000 mAh bricks) using a calibrated **ATORCH DL24P** electronic programmable DC load with dynamic monitoring of voltage, current, internal impedance, and converter temperatures.

The goal? To quantify real usable Wh efficiency, actual gravimetric energy density (Wh/kg), voltage stability, and BMS/OCP trip thresholds under sustained loads.

*Note on Volumetric Density (Wh/liter): A few of you asked for Wh/L. While I track gravimetric density (Wh/kg) precisely on a digital scale, calculating exact Wh/L is tricky due to curved chassis designs and varying case thicknesses. However, high-density Li-Po pouches (like INIU) push well past 400 Wh/L. I'll be adding caliper measurements to the database soon to track exact volumetric density as well!*

***

### 📊 Key Findings & Benchmarks

* 🥇 **The Ultimate King of Density & Efficiency** – The **INIU 45W (20k)** holds the absolute lab record with **93.7% efficiency** (69.36 Wh usable) and an unmatched **206.9 Wh/kg**. 
* 🎀 **The Pocket Rocket** – The new **INIU Pocket 10k (P50)** just shocked the lab. Pushing **84.9% efficiency** out of a tiny 162g body, it claimed the #2 spot overall in energy density at **188.6 Wh/kg** thanks to a true 2S high-voltage architecture (7.2V / 36Wh).
* 🔋 **The 50k Monolith** – The **ChoeTech Digital 22.5W (50k)** ran for an exhausting 16h 42m on the testbench. It delivered **166.75 Wh**, hitting an incredible **90.1% efficiency** and proving that massive capacity doesn't have to mean massive conversion losses.
* ⚡ **AlzaPower Vision Series** – A true mixed bag. The **Vision 10k 100W** is a beast with **91.8% efficiency** (using 21700 cells), but the smaller 30W version drops to a mediocre 79.1%. Meanwhile, the **Vision 20k 100W** showed significant variance between units (one hit 60.6 Wh, a degraded one only 50.0 Wh).
* ⚠️ **Marketing Deception Exposed** – The modern-looking **AlzaPower Garnet 20k** proved to be a major disappointment. It burns through energy as pure heat (**73.9% efficiency**) and abruptly shuts down from 15% directly to 0%. Classic case of form over function.
* 🛑 **Critical Engineering Failure** – **TRONIC 10k (Lidl)** converted 18.8 Wh into pure waste heat (**49.2% efficiency**), cuts off below 2.5 W, has high self-discharge, and uses a fake charge gauge.

***

### 📋 Top Units Telemetry & Tier Summary

| Tier | Model | Rated Wh | Measured Wh | Efficiency | Weight | Wh/kg | Notes & Telemetry |
|:---|:---|:---:|:---:|:---:|:---:|:---:|:---|
| 🥇 **S** | **INIU 45W** (20k) | 74.0 | 69.36 | **93.7%** | 335.2g | **206.9** | Absolute lab record; minimal internal losses; high-density Li-Po. |
| 🥇 **S** | **AlzaPower Vision 100W** (10k) | 36.0 | 33.04 | **91.8%** | 343.6g | **96.2** | Excellent voltage stability; robust body with TFT display. |
| 🥇 **S** | **ChoeTech Digital 22.5W** (50k) | 185.0 | 166.75 | **90.1%** | 955.3g | **174.6** | 16h 42m runtime, massive capacity with top-tier efficiency. |
| 🥇 **S** | **INIU Pocket 10k** (P50) | 36.0 | 30.56 | **84.9%** | 162.0g | **188.6** | Exceptional gravimetric density, 2S architecture supporting 45W. |
| 🥇 **S** | **WG 20+** (20k) | 74.0 | 62.74 | **84.8%** | 421.0g | **149.0** | New king of 20k category. Highly efficient internal hardware. |
| 🥇 **S** | **AlzaPower Parade 22.5W** (20k) | 74.0 | 62.27 | **84.1%** | 415.0g | **150.0** | Re-tested (30cm USB-C). Exceptional DC-DC conversion. |
| 🥈 **A** | **PanzerGlass Empower Qi2** (10k) | 38.5 | 31.80 | **82.6%** | 195.4g | **162.7** | High efficiency and premium density for a wireless powerbank. |
| 🥈 **A** | **AlzaPower WorkMate 100W** (20k) | 74.0 | 59.99 | **81.1%** | 432.8g | **138.6** | Solid and reliable 100W performance. |
| 🥉 **B** | **Vention Mini 35W w/ Cable** (10k) | 38.5 | 29.15 | **75.7%** | 176.5g | **165.2** | Compact form factor but suffers from standard conversion losses. |
| 🥉 **B** | **AlzaPower Parade Gen2** (20k) | 75.0 | 53.86 | **71.8%** | 409.5g | **131.5** | Lower efficiency compared to the older generation Parade. |
| 🛑 **F** | **TRONIC PD/QC (Lidl)** (10k) | 37.0 | 18.20 | **49.2%** | 219.8g | **82.8** | 18.8Wh wasted as heat; fake charge gauge; massive self-discharge. |

***

### 🌐 Live Dashboard & Open-Source Database

* 📊 **Live Interactive Dashboard:** https://tomikbrumik.github.io/powerbank-telemetry-lab/
* 📁 **GitHub Repository & CSV:** https://github.com/TomikBrumik/powerbank-telemetry-lab/
