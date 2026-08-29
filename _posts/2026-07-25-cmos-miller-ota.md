---
title: "Design of a CMOS Two-Stage Miller Compensated OTA"
description: "A comprehensive design and verification of a two-stage Miller compensated OTA using the TSMC 180 nm process, leveraging the gm/ID methodology."
categories: [Projects]
tags: [Analog IC, OTA, CMOS]
permalink: /project/cmos-miller-ota/
math: true
---

**[Read / Download the Full Project Report (PDF)](/assets/pdfs/CMOS_Two-Stage_Miller_OTA_4.0.pdf)**

This project focuses on the design and optimization of a CMOS two-stage Miller compensated OTA based on the TSMC 180nm process.

The schematic of the circuit is presented below:

<figure>
  <img src="/assets/portfolio_images/opamp_final_sch.png" alt="OTA Schematic" loading="lazy" decoding="async">
</figure>

Under typical operating conditions ($V_{DD}$ = 1.8 V, 27°C, tt process corner), the circuit achieves the following performance metrics:

| Parameter | Simulated Value |
| :--- | :--- |
| Input Common-Mode ($V_{in,cm}$) | 0.9 V |
| Output Swing | 0.14 V ~ 1.65 V |
| Power Consumption | 1.33 mW |
| Open-Loop DC Gain ($A_{v0}$) | 87.1 dB |
| Unity-Gain Bandwidth (GBW) | 57.6 MHz |
| Phase Margin (PM) | 66.1° |
| Slew Rate (SR+, SR-) | +31 V/$\mu$s, -72 V/$\mu$s |
| CMRR | 87.9 dB |
| PSRR- | 92.8 dB |
| Equivalent Input Noise (@ 1kHz) | 42.7 nV/$\sqrt{\text{Hz}}$ |

For more details, please refer to the complete project report below:

**[Read / Download the Full Project Report (PDF)](/assets/pdfs/CMOS_Two-Stage_Miller_OTA_4.0.pdf)**
