# PentoGraf-Pentagon-1024k

## Pentagon ZX Spectrum clone on SRAM with TurboSound and NemoBus in Leningrad-2 (Aurora) form-factor.

> [English](README.en.md) | [Русский](README.md)

# 🛠 PentoGraf (Pentagon Clone by Alex-2-Graf)

After the successful launch of Leningrad-2-48k and Leningrad-2-128k-SRAM, the question arose about playing demos. 
We all know that the majority of demosceners write their demos specifically for the Pentagon clone.

## 📜 History

**Pentagon** is the most popular and iconic Soviet clone of the ZX Spectrum, developed in Moscow around 1989–1990. Unlike the original British computer, the Pentagon featured unique screen timings (320 lines per frame instead of 312, and 71,680 T-cycles per INT instead of 69,888).

These "incorrect" timings gave the CPU more time to execute code during the interrupt. This made the Pentagon a worldwide benchmark for creating highly complex graphical and musical demos (Demoscene). Even today, 99% of all graphical effects and multicolor routines in the post-Soviet space are written strictly for the Pentagon architecture.

Many suggested simply modifying the timings of the Aurora board to match the Pentagon. However, in that case, it wouldn't be a Leningrad-2 anymore, nor would it be a proper Pentagon.

A different approach was chosen.

**PentoGraf** is an author's modification of the iconic Pentagon ZX Spectrum clone. This project is a direct continuation of the **Aurora** board (Leningrad-2 128k SRAM) and brings the legendary demoscene architecture into the compact form-factor and dimensions of the "Leningrad".

**PentoGraf** is a tribute to the legend, built on reliable static RAM (SRAM) and packed into the ergonomic size of the "Leningrad" board.

## 💾 Key Features

* **Compatibility:** Full match of dimensions, mounting holes, and connectors with the "Aurora" board (Leningrad-2). Fits the same cases and is compatible with original keyboards.
* **Component Base:** 100% classic discrete logic ("rassypukha") of K1533/K555 series (74HC/HCT) without using CPLD/FPGA.
* **Memory:** 1024 KB of static RAM (SRAM) onboard, eliminating issues related to complex and unreliable dynamic RAM (RU5/RU7).
* **Sound:** Integrated dual-chip TurboSound system (two AY-3-8910/YM2149F chips).
* **Modernization:** The bulky classic floppy disk controller (FDD) has been completely removed.
* **Expansion:** Equipped with a single NemoBus system slot for connecting modern peripherals (DivMMC, BDI, PiCard, ZXKM, GeneralSound, ZX-Multisound, etc.).
* **RISER:** Further expansion up to 4 devices is possible using a Riser board.

---

## As a result, the following files were created:
* [PentoGraf iBOM 1.01](Export/PentoGraf_1.01.html)
* [Schematics](Export/PentoGraf_1.01.pdf)
* [Gerber Files](Gerber/PentoGraf_1.01_gerber.zip)

### T-connector (Riser) series:
* [Riser iBOM](Export/Rizer.html)
* [Schematics](Export/Rizer.pdf)
* [RIZER x4](Gerber/RIZER_x4_Nemobus_Pent_gerber.zip)
* [RIZER x3](Gerber/RIZER_x3_Nemobus_Pent_gerber.zip)
* [RIZER x2](Gerber/RIZER_x2_Nemobus_Pent_gerber.zip)
* [RIZER x1](Gerber/RIZER_x1_Nemobus_Pent_gerber.zip)

## 📌 Additional Notes
* Memory can be used in **SOP packages** via an adapter [Gerber](Gerber/SRAM-PentoGraf_Gerber.zip)  .
* As mentioned above, you can use the **keyboard from the Aurora board**.

---

## 🛠 Assembly and Troubleshooting

Generally, assembly and tuning do not cause any major issues. However, let's clarify the purpose of the jumpers:

* **JP1, JP2, and JP3:** These must be shorted/closed if you are installing a **VGA connector**. If you are installing an **HDMI output**, leave them open. 
  * *Note:* When installing HDMI, all resistors **R24-R31** must be replaced with **270 Ohm** values.
* **J9:** This jumper is required to cut power from the **RP2040-Zero** during firmware flashing.
* **J18:** This jumper is required when using the **W27C512 ROM**.

### 💾 ROM / Firmware
* ROM files for the project can be found [here](ROM).

### 📺 VGA Output
* Firmware and configuration settings for the RP2040-Zero can be found [here](VGA).

---

## ⚖ License

This project is Open Source Hardware. Graphic materials, schematics, and PCB layouts are distributed under the **CERN OHL v2 Weak Reciprocal** license (CERN-OHL-W-2.0).

You are free to redistribute, modify, and manufacture this device, provided that the authorship of **Alex-2-Graf** is preserved and any modified source files of the board are published under the same open-source license.
