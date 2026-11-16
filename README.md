# ⚡ Powerbank Telemetry & Efficiency Benchmark Lab

A publicly accessible, standardized telemetry database and rigorous engineering benchmark for portable power banks. All units undergo controlled continuous discharge and recharge cycles to expose real usable energy, DC-DC converter topology, multi-port voltage sag, thermal throttling, and cell architecture.

**Total Units Tested:** 🔬 46 individual runs/units across **34 models** (from 5,000 mAh EDC units to massive 50,000 mAh field packs).

---

## ⚡ Input Charging vs. Output Efficiency (Wall-to-Load Benchmark)

| Model | Labeled Pack | Input (Wall) | Output (Load) | Total Loss | Pack Discharge Eff. | Wall-to-Load Cycle Eff. | Circuitry & Diagnostic Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **UGREEN Nexode 200W 25000mAh** 🆕 | 90.00 Wh | 99.00 Wh | 72.29 Wh | -26.71 Wh | **80.32%** | **73.02%** | Full cycle: 9.07V in (10,939 mAh) → 15,133 mAh @ 5V/2A out; 5S 21700 cell pack |
| **INIU P771 Qi2.2 25W 10000mAh** 🏆 | 36.00 Wh | 38.00 Wh | 31.94 Wh | -6.06 Wh | **88.72%** | **84.05%** | 🏆 **Lab World Record:** Highest round-trip cycle efficiency ever recorded. Qi2.2 25W magnetic + 45W wired PD/PPS. Temp°Guard 3.0 active cooling. |
| **AlzaPower Parade Gen2 22.5W 10000mAh** 🆕 | 37.00 Wh | 43.48 Wh | 32.43 Wh | -11.05 Wh | **87.64%** | **74.58%** | Full cycle verified: 9V in (4,781 mAh) → 6,471 mAh out; 2× USB-C, 1× USB-A; full Low-Power Mode; 5V drop under multi-port. |
| **AlzaPower Parade Gen2 100W 27000mAh (Run 2)** | 99.90 Wh | 111.88 Wh | 82.35 Wh | -29.53 Wh | **82.43%** | **73.60%** | Peak discharge pass; 16,232 mAh @ 5V/2A; reached clean 00% cut |
| **AlzaPower Parade Gen2 100W 27000mAh (Run 1)** | 99.90 Wh | 111.88 Wh | 81.07 Wh | -30.81 Wh | **81.15%** | **72.46%** | High thermal dissipation during 65W input replenishment stage |
| **Samsung 45W EB-P4520 20000mAh (Unit 2)** | 74.00 Wh | 76.00 Wh | 60.39 Wh | -15.61 Wh | **81.61%** | **79.46%** | Second production sample; complete wall-to-load cycle verified; slow 25W input cap. |
| **Samsung 45W EB-P4520 20000mAh (Unit 1)** | 74.00 Wh | **TBD** | 64.01 Wh | **-** | **86.50%** | **TBD** | Baseline reference run; pack discharge verified; input recharge pending |
| **Vention Mini 35W w/ Cable 10000mAh** 💀 | 38.50 Wh | 35.00 Wh | 26.59 Wh | -8.41 Wh | **69.07%** | **75.98%** | **F-Tier Failure:** 20W input absorbed only 35Wh; 3x thermal shutdowns (OTP) under 24W load |

---

## 🔬 Hardware Revision & 45W Stress-Test Deep-Dive: INIU `P52L / P51L` (2S 7.4V) vs. `P51L-E2` (1S 3.7V)

Controlled continuous **45W (`15V / 3.000A` via ATORCH DL24P)** stress tests across two retail hardware revisions of INIU's 45W 20,000 mAh integrated-cable platform exposed major internal cell architecture and firmware differences (cross-verified with `r/ChargingSheet`, `r/UsbCHardware`, and official INIU documentation):

### 1. Revision & Protocol Comparison Matrix

| Parameter / Feature | White INIU `P51L-E2` (`SN:000125`) | Black INIU `P51L / P52L` (`SN:000025`) | Reddit (`r/ChargingSheet`) & Official INIU Verification |
| :--- | :--- | :--- | :--- |
| **Cell Architecture & Rated Pack** | **1S Parallel** (`3.7V` / `20,000 mAh` / `74 Wh`) | **2S Series** (`7.4V` / `10,000 mAh` / `74 Wh`, cells `2INP12/62/80`) | `P51L-E2` was upgraded/rebranded into `P51L` / `P52L`; `74 Wh` nominal, `11.45 × 7.25 × 2.92 cm`, `326–335.2 g` |
| **Cell Current Draw at 45W** | High (**~14–16 A** on 3.7V bus) | Halved (**~6–7 A** on 7.4V bus) | 1S topology doubles boost converter input current, increasing $I^2R$ copper/MOSFET heating |
| **PPS / Samsung SFC 2.0 (45W)** | **YES (`3.3–11V / 4.5A`)** on **BOTH** port C1 & smooth white cable | **YES (`3.3–11V / 4.5A`)** on **BOTH** port C1 & braided black cable | Full `5A PPS` (`45W SFC 2.0`) on both C1 and attached cable + `UFCS` up to `49W` |
| **Fixed USB-PD Profiles & Input** | `5V/3A, 9V/3A, 12V/3A, 15V/3A` (**No 20V PDO**) • `27W` max input | `5V/3A, 9V/3A, 12V/3A, 15V/3A` (**No 20V PDO**) • `27W` max input | No `20V` PDO on any 45W `P51L/P52L` revision; input capped at `27W` (`9V/3A` or `15V/1.8A`) |
| **Multi-Port Power Sharing** | **`5V / 3A` (`15W Max` shared)** | **`5V / 3A` (`15W Max` shared)** | Vendor label: `Total(OUT1+OUT2+OUT3): 15W(MAX)` (drops PD/PPS to shared `5V` bus) |
| **Passthrough & UPS Support** | **Passthrough: YES (`5V` only, no SFC)** • **UPS: NO** | **Passthrough: YES (`5V` only, no SFC)** • **UPS: NO** | Simultaneous charge/discharge drops fast charging to `5V`; unplugging AC causes brief output dropout (not UPS) |
| **Low-Power Mode (LPM)** | **YES (Auto)** – INIU Auto Trickle Mode (`5V`) | **YES (Auto)** – INIU Auto Trickle Mode (`15V→5V` after 30s `<40 mA`) | Official *Automatically-Adapted Trickle-Charging Mode* (`5V` trickle for earbuds/watches; unloaded `15V` sleeps to `5V` after 30s) |
| **Continuous 45W (`15V/3A`) Stress** | Sustained **34 min** continuous until converter OTP (`44.3–48.3 °C`); **60.56 Wh (`81.84%`)** in `01:22:16` | **Fixed 5–8 min FW 45W throttling timer** drops `15V` PDO regardless of cable or `2.9A` vs `3.0A` load | `r/ChargingSheet`: `P51L-E2` sustains 45W 20–34 min before OTP; newer INIU FW uses a fixed 5–8 min 45W timer |

### 2. Complete 45W Stress Discharge Log – White INIU `P51L-E2` (1S / 3.7V, `SN:000125`)

| Segment / Milestone | Substrate & DL24P Setup | Voltage / Current | Power / Load Res | Cumulative `Ene` | Segment `Ene` | Cumulative `Cap` | IR Display Temp / `MOS` | SoC `%` & Termination Cause |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **Seg 1 Start (`00:00:36`)** | Cork pad, 30cm Asus C1, `CC`, `3.000A`, `<10.0V` | `14.803 V` / `3.000 A` | `44.40 W` / `4.93 Ω` | `0.41412 Wh` | — | `28 mAh` | `MOS 37.5 °C` (`BAT 81 mΩ`) | `100%` – Clean 15V start |
| **Seg 1 (~15 min)** | Cork pad, `3.000A` | `14.774 V` / `3.000 A` | `44.32 W` / `4.92 Ω` | `11.2518 Wh` | `+10.8377 Wh` | — | **IR `34.2 °C`** | `79%` – Only `-29 mV` sag |
| **Seg 1 (~30 min)** | Cork pad, `3.000A` | `14.769 V` / `3.000 A` | `44.30 W` / `4.92 Ω` | `22.7856 Wh` | `+11.5338 Wh` | — | **IR `42.3 °C`** | `57%` – Converter heat buildup |
| **Seg 1 Stop (`00:34:xx`)** | Cork pad, `3.000A` | Cutoff (`0 V`) | — | **`25.6213 Wh`** | `+25.6213 Wh` | `1,734 mAh` | **IR `44.3 °C`** | **1st Converter OTP Cutoff** (hard 0V cut) |
| **Seg 2 Start → Mid** | **Bare cool tile**, `3.000A`, `<3.5V` | `14.730 V` / `3.000 A` | `44.19 W` / `4.91 Ω` | `37.4941 Wh` | `+11.8728 Wh` | — | `28.0 °C` → **`44.1 °C`** | `51%` start → `26%` under load |
| **Seg 2 Stop (`01:00:35`)** | Bare tile (`~26m 35s` segment) | Cutoff (`0 V`) | — | **`44.5760 Wh`** | `+18.9547 Wh` | `3,021 mAh` | **IR `48.3 °C`** | **2nd Converter OTP Cutoff** (top-mounted PCB heat) |
| **Seg 3 (`01:14:34`)** | Bare tile (`13m 59s` segment) | Cutoff (`0 V`) | — | **`54.9964 Wh`** | `+10.4204 Wh` | `3,728 mAh` | **IR `45.6 °C`** | `16%` → **`6%`** (BMS UVP under ~15–16A cell load) |
| **Seg 4 (`01:22:16`)** | Paper tissue on tile (`7m 42s` segment) | Cutoff (`0 V`) | — | **`60.5592 Wh`** | `+5.5628 Wh` | **`4,105 mAh`** | `30.0 °C` → **`44.8 °C`** | **`0%` Final Empty** (`6%→5%→4%` sag jump; **`81.84%`** of 74Wh) |

### 3. Diagnostic Run Log – Black INIU `P51L / P52L` (2S / 7.4V, `SN:000025`, Paper Tissue Substrate)

| Run / Test | Harness & Current Setting | Telemetry (`Vol`, `Pwr`, `Res`) | Runtime (Cumulative) | `Ene` (Cumulative) | `Cap` (Cumulative) | SoC & Diagnostic Outcome |
| :--- | :--- | :---: | :---: | :---: | :---: | :--- |
| **Cable Resistance Test** | Integrated braided vs. external USB-C (`3.000A`) | `14.705V / 44.13W` vs. `14.678V / 44.03W` | `00:29` / `00:45` | — | — | Only `27 mV` (`9 mΩ`) difference – braided cable is healthy |
| **Run 1 (`3.0000A`)** | Port C1, 30cm Asus cable, `<3.5V` | Avg `43.93 W` (`~14.64 V`) | `00:05:54` | `4.31932 Wh` | `292 mAh` | 15V PDO dropped by FW timer → trigger flashes → `<3.5V` stop |
| **Run 2 (`3.0000A`)** | Port C1, 30cm Asus cable, `<3.5V` | — | `+00:05:00` (`00:10:54`) | `7.97569 Wh` | `540 mAh` | **`87%`** – Hard 0V output cut (trigger LED off) |
| **Run 3 (`3.0000A`)** | Port C1, **Asus flipped 180°** (2nd `CC` pin) | — | `+00:10:04` (`00:20:58`) | `15.2954 Wh` | `1,032 mAh` | **`~75–76%`** – Hard 0V output cut after 10 min |
| **Run 4 (`2.9000A`)** | **Integrated braided cable** (`~42.7 W`) | — | `+00:04:32` (`00:25:30`) | **`18.5240 Wh`** | **`1,249 mAh`** | **`70%`** – 15V PDO dropped again (confirms fixed FW timer) |

### 4. Documented Electronic & Firmware Edge Cases

- **PD Controller 5V Fallback Lockout:** Repeated load cutoffs (on DL24P) or reaching 0% UVP locks INIU's bidirectional USB-C PD controller into a `5V`-only safety fallback state (disabling PPS / SFC 2.0). Briefly connecting the power bank to an AC wall charger resets the internal PD electronic fuse and immediately restores full `45W SFC 2.0`.
- **DL24P Residual Capacitor Handshake Lock:** Residual charge in DL24P input capacitors tricks INIU's bidirectional `IN/OUT` port into detecting an external charger, locking output to `5V`. Always discharge the unloaded DL24P (`ON` for 2s → `OFF`, `Vol: 00.000 V`) and leave the power bank unplugged for ~30s before reconnecting.
- **30-Second Idle `15V → 5V` Transition:** Because the bare PD trigger draws only ~10–15 mA (below INIU's ~40–60 mA high-voltage load threshold), leaving the load in `OFF` for >30 seconds causes the power bank to step down its `15V` boost rail to its `5V` Automatically-Adapted Trickle-Charging rail while keeping its display and trigger LED lit.

---

## 🛡️ Dedicated 21700 Cylindrical Cell Index (Zero Swelling Risk)

Steel cylindrical 21700 cells eliminate pouch pillowing, handle high continuous C-rates, and feature mechanical CID pressure relief valves.

| Model | Cell Configuration | Max Output | Multi-Port Topology | 5A PPS | Low-Power Mode (LPM) | Input Throttling | Telemetry Display |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **UGREEN Nexode 200W 25000mAh** | 5S1P (5x 21700) | 200W (140W EPR) | ✅ Independent (100W+100W) | ✅ YES | 🟢 Dedicated | None (65W clean) | 📊 Color TFT Wattmeter |
| **UGREEN 145W 25000mAh** | 5S1P (5x 21700) | 145W (100W C1) | ✅ Independent (100W+45W) | ✅ YES | 🟢 Dedicated | None (65W clean) | 🔢 Digital % |
| **AlzaPower WorkMate 100W 20000mAh** | 4S1P (4x 21700) | 100W | ✅ Independent (No 5V drop) | ❌ NO (Locked to 3A) | 🟢 Dedicated | None (65W clean) | 🔢 Digital (V/W) |
| **AlzaPower Vision 100W 20000mAh** | 4S1P (4x 21700) | 130W (100W C + 30W A) | ⚠️ C+A OK (130W) / C1+C2 5V drop | ✅ YES | 🟢 Dedicated | None (100W clean) | 📊 Color TFT Wattmeter |
| **AlzaPower Vision 100W 10000mAh** | 2S1P (2x 21700) | 130W (100W C + 30W A) | ⚠️ C+A OK (130W) / C1+C2 5V drop | ✅ YES | 🟢 Dedicated | None (100W clean) | 📊 Color TFT Wattmeter |
| **Vention 165W TFT 20000mAh** | 4S1P (4x 21700) | 165W (100W C1) | ✅ Independent (100W+65W) | ✅ YES | ❌ None | None (65W clean) | 📊 Color TFT Wattmeter |
| **O2 Spark 35W 10000mAh** | 2S1P (2x 21700) | 35W (40W Peak) | ❌ 5V Drop (Shared) | ❌ NO (Max 3A) | ❌ None | None (20W clean) | 🔢 Digital % |
| **AlzaPower Vision 30W 10000mAh** | 2S1P (2x 21700) | 30W | ❌ 5V Drop (Shared 15W) | ❌ NO | ❌ None | ⚠️ **Severe (15–22W)** | 📊 Color TFT Wattmeter |

---

## 🏆 Full 7-Tier Classification & Standards (r/UsbCHardware Aligned)

### ⚡ S-Tier: Absolute Technological Elite
*Steel cylindrical 21700 cells with zero swelling risk, true independent multi-port rails, or breakthrough world efficiency records.*
- **UGREEN Nexode 200W 25000mAh** — **72.29 Wh (80.32%)** | **127.95 Wh/kg** | *Heavyweight Champion:* Steel cylindrical 5S 21700 cells (zero swelling risk), dual independent buck-boost converters (100W+100W simultaneous without reset or 5V drop), 140W EPR 28V/5A profile, full 5A PPS, color TFT live wattmeter (V/A/W), 65W passthrough recharge, dedicated Low-Power Mode (3s hold, 3.5h auto-off). Ports: 2× USB-C, 1× USB-A.
- **UGREEN 145W 25000mAh** — **74.49 Wh (82.77%)** | **150.94 Wh/kg** | *Laptop Gold Standard:* Heavy-duty 21700 cells, independent 100W + 45W split, 65W fast input with passthrough and zero throttling, full 5A PPS, dedicated Low-Power Mode (3s hold, 3.5h timer). Ports: 2× USB-C, 1× USB-A.
- **INIU P771 Qi2.2 25W 10000mAh** — **31.94 Wh (88.72%)** | **148.56 Wh/kg** | 🏆 **World Lab Record Holder:** Unmatched **84.05%** round-trip Wall-to-Load cycle efficiency. Certified Qi2.2 25W magnetic wireless charging, 45W wired USB-C output with 5A PPS, integrated 60W GoCord lanyard cable, Temp°Guard 3.0 thermal regulation, and INIU Automatically-Adapted Trickle-Charging Mode. Ports: 1× USB-C + Qi2 magnetic pad.
- **INIU P52L / P51L / P51L-E2 45W 20000mAh** — **70.30 Wh (95.00%)** | **209.72 Wh/kg** | 🏆 **Discharge Efficiency Record Holder:** Average efficiency 95.00% @ 10W baseline (Unit 2 reached **96.27%** discharge efficiency), extreme gravimetric density of 209.72 Wh/kg, full 5A PPS (3.3–11V/4.5A, Samsung SFC 2.0) on BOTH port C1 & built-in cable + UFCS 49W, no 20V PDO (max 15V/3A), 27W input, 5V/3A (15W) multi-port drop, 5V-only passthrough (no UPS), and INIU Auto Trickle Mode. Under continuous 45W (15V/3A) DL24P stress: White `P51L-E2` (1S 3.7V, `SN:000125`) sustained 34 min before converter OTP (`44.3–48.3 °C`, delivering `60.56 Wh` / `81.84%`), while Black `P51L` (2S 7.4V, `SN:000025`, `2INP12/62/80`) enforces a fixed 5–8 min FW 45W throttling timer dropping 15V PDO (`18.52 Wh` to 70% SoC). Ports: 1× USB-C, 1× USB-A, 1× attached USB-C cable.

### 🔋 A-Tier: Top Work and Daily Models
*High continuous output, cylindrical cells or advanced 2S packs, excellent regulation.*
- **AlzaPower Vision 100W 20000mAh** — **60.62 Wh (84.19%)** | **126.85 Wh/kg** | *4x 21700 cylindrical cells (zero swelling risk), combined output up to 130W (100W C + 30W A, 100W in/out), full 5A PPS, color TFT live wattmeter (V, A, W, time), dedicated Low-Power Mode. C+A works without 5V drop; drops to 5V only when C1+C2 are shared. Ports: 2× USB-C, 1× USB-A.*
- **AlzaPower Vision 100W 10000mAh** — **32.82 Wh (91.17%)** | **95.52 Wh/kg** | *2x 21700 cylindrical cells, exceptional 91.17% discharge efficiency, combined output up to 130W (100W C + 30W A), full 5A PPS, color TFT live wattmeter, dedicated Low-Power Mode. C+A works without 5V drop; drops to 5V only when C1+C2 are shared. Ports: 2× USB-C, 1× USB-A.*
- **Vention 165W TFT 20000mAh** — **61.62 Wh (83.27%)** | **140.14 Wh/kg** | *21700 cells, paper split 100W + 65W, color TFT display, high power ceiling. Lacks Low-Power Mode. Ports: 2× USB-C, 1× USB-A.*
- **CUKTECH PB200N 55W 20000mAh** — **64.09 Wh (86.61%)** | **128.98 Wh/kg** | *2S Li-Po block (7.4V), fixed PDO up to 20V/2.75A + full 5A PPS (5–11V/5A, up to 55W Xiaomi Turbo), 40W fast input, independent multi-port split without 5V drop (33W+15W / 45W+10W), dedicated 2-hour Low-Power Mode (double-click), integrated lanyard cable. Ports: 1× USB-C, 1× USB-A, 1× attached USB-C lanyard.*
- **AlzaPower WorkMate 100W 20000mAh** — **59.99 Wh (83.32%)** | **138.61 Wh/kg** | *4x 21700 cylindrical cells (72 Wh pack). Independent multi-port rail (zero 5V drop!), telemetry digital display showing live Volts and Watts, dedicated Low-Power Mode. Demoted from top tiers due to lack of 5A PPS (locked to 3A). Ports: 2× USB-C, 1× USB-A.*
- **Samsung 45W EB-P4520 20000mAh** — **62.20 Wh (84.05%)** | **155.34 Wh/kg** | *Symmetrical 22W + 22W split on 2 ports, but collapses to 10W (5V drop) on all 3 ports. PDO 5V/9V/15V@3A + 20V/2.25A (no 12V PDO) + dual PPS (3.3–11V/4.5A SFC 2.0 & 3.3–16V/3A). Slow 25W input (~3.5h), 5V-only passthrough. Soft pouch cells, lacks dedicated Low-Power Mode. Ports: 3× USB-C.*
- **INIU Pocket P50 45W 10000mAh** — **30.56 Wh (84.89%)** | **188.64 Wh/kg** | *Pocket EDC (162 g, 188.64 Wh/kg) with 45W output, 5A PPS (11V/4.5A SFC 2.0), no 20V PDO (max 15V/3A), 5V/3A multi-port drop, and INIU Automatically-Adapted Trickle-Charging Mode (5V). Ports: 1× USB-C, 1× USB-A.*

### 💎 B-Tier: Solid Daily Drivers with Minor Compromises
- **O2 Spark 35W 10000mAh** — **28.97 Wh (80.47%)** | **166.59 Wh/kg** | *Heavy-duty 2x 21700 cylindrical cells with up to 40W peak headroom. 1x USB-C port + 1x built-in USB-C cable (no USB-A). Digital segment display showing percentage. Fast 20W input. Drops to 5V when both are used. Lacks 5A PPS and Low-Power Mode. Ports: 1× USB-C, 1× Built-in USB-C Cable.*
- **AlzaPower Parade Gen2 100W 27000mAh** — **81.16 Wh (81.21%)** | **152.31 Wh/kg** | *Huge 99.9 Wh pack, 100W in/out, dedicated Low-Power Mode, but soft pouch cell, 5V multi-port drop, and voltage instability below 45% SoC. Ports: 2× USB-C, 2× USB-A.*
- **AlzaPower Metal 100W 40000mAh** — **119.69 Wh (80.87%)** | **151.33 Wh/kg** | *100W output and durable metal body, but suffers from poor multi-port power sharing and lacks Low-Power Mode. Ports: 1× USB-C, 2× USB-A, 1× Micro-USB.*
- **Samsung 25W PD 10000mAh** — **30.00 Wh (81.08%)** | **135.14 Wh/kg** | *Reliable foundation with 9W+9W split and 25W input. Soft pouch. Ports: 2× USB-C.*
- **PanzerGlass Empower Qi2 10000mAh** — **31.80 Wh (82.60%)** | **162.74 Wh/kg** | *Honest Qi2 wireless with 82.6% efficiency. Soft pouch. Ports: 1× USB-C + Qi2 Magnetic.*
- **O2 Built-in Cable 10000mAh** — **30.48 Wh (82.38%)** | **148.68 Wh/kg** | *Practical city bank with 82.38% efficiency. Soft pouch. Ports: 1× USB-C, 1× USB-A, 1× attached USB-C cable.*

### 🔹 C-Tier: Capacity Workhorses & Older Foundations
- **AlzaPower Parade Gen2 22.5W 10000mAh** 🆕 — **32.43 Wh (87.64%)** | **142.59 Wh/kg** (227.4 g) | *Full cycle: 43.48 Wh in (4,781 mAh @ 9V) → 32.43 Wh out (6,471 mAh), achieving 74.58% round-trip Wall-to-Load efficiency. Solid 87.64% discharge efficiency and dedicated Low-Power Mode, but limited to 20W PD / 22.5W max, 18W recharge, and 5V multi-port drop. Ports: 2× USB-C, 1× USB-A.*
- **ChoeTech Digital 22.5W 50000mAh** — **166.75 Wh (90.14%)** | **174.55 Wh/kg** | *Massive 50,000 mAh parallel block with high low-current efficiency, but capped at 22.5W and sags above 15W. Ports: 1× USB-C, 2× USB-A.*
- **ROMOSS 65W Fast Charge 27000mAh** — **75.44 Wh (75.52%)** | **111.35 Wh/kg** | *Large body, honest 65W output, average 75.52% efficiency. Ports: 1× USB-C, 2× USB-A, 1× Micro-USB.*
- **WG QC/PD 20W 10000mAh** — **30.10 Wh (81.35%)** | **136.82 Wh/kg** | *Standard 20W baseline pouch bank. Ports: 1× USB-C, 2× USB-A.*
- **AlzaPower Vision 30W 10000mAh** — **28.46 Wh (79.06%)** | **119.73 Wh/kg** | *Has 2x 21700 cells and Color TFT display with alarm/timer, but suffers a triple flaw: 5V multi-port drop (shared 15W), severe thermal throttling during recharge (drops to 15–22W), and NO Low-Power Mode. Ports: 2× USB-C, 1× USB-A.*
- **Samsung Wireless 10000mAh** — **29.79 Wh (80.51%)** | **124.13 Wh/kg** | *Older slow wireless bank. Ports: 1× USB-C, 1× USB-A + Wireless Pad.*

### 📉 D-Tier: Outdated Concepts & Severe Constraints
- **AlzaPower Parade Gen1 22.5W 20000mAh** — **62.27 Wh (84.15%)** | **151.55 Wh/kg** (410.9 g) | *Tested run 06:10:18 (12,343 mAh out). Good efficiency, but obsolete: capped at 22.5W (20W on C), slow 18W recharge, 5V multi-port drop. Ports: 2× USB-C, 1× USB-A, 1× Micro-USB.*
- **AlzaPower Parade Gen2 22.5W 20000mAh** — **53.86 Wh (71.81%)** | **131.53 Wh/kg** (409.5 g) | *Has dedicated Low-Power Mode, but crippled by 71.81% efficiency, prehistoric 18W input, and 5V multi-port drop. Ports: 2× USB-C, 1× USB-A.*
- **ChoeTech PD20W 5000mAh** — **13.93 Wh (75.28%)** | **137.78 Wh/kg** (101.10 g) | *Compact body plug (101.1g), but only recharges via slow 5V USB-A adapters; completely refuses handshake on USB-C PD chargers. NO Low-Power Mode. Ports: 1× USB-C Plug, 1× USB-C Port.*
- **WG 20+ 20000mAh** — **62.74 Wh (84.78%)** | **148.98 Wh/kg** | *Outdated 20W concept with slow 18W input from wall and 5V drop. Ports: 1× USB-C, 2× USB-A, 1× Micro-USB.*
- **Vention 5000mAh** — **14.10 Wh (76.22%)** | **109.13 Wh/kg** | *Basic model without cables, average efficiency. Ports: 1× USB-C, 1× USB-A.*
- **Vention Magnetic Wireless 20W 5000mAh** — **15.71 Wh (84.92%)** | **124.29 Wh/kg** | *Older heating 7.5W wireless coil. Ports: 1× USB-C + Wireless Pad.*
- **AlzaPower Qi2 Slim 5000mAh** — **15.30 Wh (82.70%)** | **122.20 Wh/kg** | *Extremely thin, limited 5V/3A sharing. Ports: 1× USB-C + Qi2 Magnetic.*

### ⚠️ E-Tier: Heat Generators & Prehistoric Inputs
- **AlzaPower Garnet 20000mAh** — **54.72 Wh (73.95%)** | **131.86 Wh/kg** | *Soft pouch cell, prehistoric 18W input, 5V multi-port drop, NO Low-Power Mode. Ports: 1× USB-C, 2× USB-A, 1× Micro-USB.*
- **UGREEN Qi2 Magnetic 10000mAh** — **25.34 Wh (68.49%)** | **119.08 Wh/kg** | *Poor thermal design of coil and converter with 68.49% efficiency. Ports: 1× USB-C, 1× USB-A + Qi2 Pad.*

### 💀 F-Tier: Disqualified / Hardware Failures
- **Vention Mini 35W w/ Cable 10000mAh** 💀 — **0.0 pts (Disqualified)** | **26.59 Wh @ 9V (69.07%) / 29.15 Wh @ 5V (75.71%)** | *Immediate 0.355V voltage sag, collapsed to 69.07% efficiency, and triggered 3 consecutive Over-Temperature Protection (OTP) shutdowns flashing error 188 under a modest 24W load. Ports: 1× USB-C, 1× USB-C Cable.*
- **TRONIC PD/QC 10000mAh** 💀 — **21.6 pts (Disqualified)** | **18.20 Wh (49.19%)** | **82.80 Wh/kg** | *Catastrophic 49.19% efficiency, voltage collapses below 4.5V under a basic 2A load. Low-grade dangerous e-waste. Ports: 1× USB-C, 1× USB-A.*

---

### 🌐 Open Source Database & Interactive Dashboard

- 📊 **Live Interactive Dashboard:** [tomikbrumik.github.io/powerbank-telemetry-lab/](https://tomikbrumik.github.io/powerbank-telemetry-lab/)
- 💻 **GitHub Repository (Raw Datasets & Schematics):** [github.com/TomikBrumik/powerbank-telemetry-lab](https://github.com/TomikBrumik/powerbank-telemetry-lab/)
