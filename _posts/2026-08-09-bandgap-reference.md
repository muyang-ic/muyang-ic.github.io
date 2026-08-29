---
title: "Design of a CMOS Bandgap Reference (BGR)"
description: "A comprehensive design and optimization of a CMOS bandgap reference using the TSMC 180 nm process, featuring a folded-cascode op-amp and global temperature compensation."
categories: [Projects]
tags: [Analog IC, Bandgap Reference, CMOS]
permalink: /project/bandgap-reference/
math: true
image:
  path: /assets/portfolio_images/bg_final_sch.png
  alt: CMOS bandgap reference schematic
---

**[Read / Download the Full Project Report (PDF)](/assets/pdfs/CMOS_BGR_1.0.pdf)**

This project focuses on the design and optimization of a Bandgap Reference (BGR) based on the TSMC 180nm process.

The schematic of the circuit is presented below:

<figure>
  <img src="/assets/portfolio_images/bg_final_sch.png" alt="BGR Schematic" loading="lazy" decoding="async">
</figure>

Under nominal operating conditions (1.8V, 27°C, TT process corner), the circuit achieves the following performance metrics:

| Parameter | Simulated Value |
| :--- | :--- |
| Tempco (TC) | 635.6 µV |
| PSRR @ DC | -94.5 dB |
| PSRR @ 100kHz | -58.3 dB |
| Phase Margin (PM) | 58.8° |
| RMS Noise | 49.4 µV |
| DC Current | 229 µA |

For more details, please refer to the complete project report below:

**[Read / Download the Full Project Report (PDF)](/assets/pdfs/CMOS_BGR_1.0.pdf)**
