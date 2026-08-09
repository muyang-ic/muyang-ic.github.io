---
layout: single
title: "Design of a CMOS Two-Stage Miller Compensated OTA"
excerpt: "A comprehensive design and verification of a two-stage Miller compensated OTA using the TSMC 180nm process, leveraging the gm/ID methodology."
categories: 
  - Project
tags: 
  - Analog IC
mathjax: true
---

<style>
  /* 1. 调节文章正文、列表和数学公式的字号与间距 */
  .page__content p, 
  .page__content li, 
  .MathJax {
    font-size: 0.9em !important; 
    line-height: 1.5 !important;  
    margin-bottom: 0.5em !important; 
  }

  /* 2. 强制表格整体居中 */
  .page__content table {
    margin-left: auto !important;
    margin-right: auto !important;
  }

  /* 3. 极大缩小图片容器下方的留白 */
  .page__content figure {
    margin-bottom: 0.2em !important; /* 💡 如果觉得还是大，可以改成 0em */
  }
</style>

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

<!-- 💡 强制加载后置 MathJax 渲染引擎，并识别单 $ 符号 -->
<script>
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$', '$$'], ['\\[', '\\]']],
      processEscapes: true
    }
  };
</script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>