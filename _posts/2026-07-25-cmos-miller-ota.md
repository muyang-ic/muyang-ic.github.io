---
layout: single
title: "Design of a CMOS Two-Stage Miller Compensated OTA"
excerpt: "A comprehensive design and verification of a two-stage Miller compensated OTA using the TSMC 180nm process, leveraging the gm/ID methodology."
mathjax: true
categories: 
  - Project
tags: 
  - ECE
  - Analog IC
  - CMOS
  - Hardware
---

<style>
  /* 继承之前调校好的完美工程排版 */
  .page__content p, 
  .page__content li, 
  .MathJax {
    font-size: 1.15em !important; 
    line-height: 1.8 !important;  
    margin-bottom: 0.8em !important; 
  }
  .page__content h2 {
    font-size: 1.6em !important;       
    margin-top: 1.5em !important;      
    margin-bottom: 0.6em !important;   
    border-bottom: 1px solid #eee !important; 
    padding-bottom: 0.3em !important;
  }
  .page__content h3 {
    font-size: 1.3em !important;       
    margin-top: 1.2em !important;      
    margin-bottom: 0.4em !important;   
  }
</style>

## 📌 Project Overview

This project focuses on the design and optimization of a CMOS two-stage Miller compensated operational transconductance amplifier (OTA) based on the TSMC 180nm process[cite: 1]. 

The primary objective was to maximize the Unity-Gain Bandwidth (GBW) while strictly satisfying a robust set of constraints operating on a 1.8V supply[cite: 1]. By leveraging the $g_m/I_D$ design methodology to meticulously size the physical transistors, the final core performance achieved an open-loop DC gain of 87 dB, a Phase Margin of 66.4°, and a GBW of 61 MHz[cite: 1]. To ensure exceptional reliability, the design was fully verified across a comprehensive 27-corner PVT (Process, Voltage, Temperature) sweep[cite: 1].

## 📄 Full Project Report

For a deep dive into the theoretical calculations, $g_m/I_D$ curve extractions, transient simulations, and schematic details, please refer to the complete engineering log below:

🔗 **[Read / Download the Full Project Report (PDF)](/assets/pdfs/CMOS_Two-Stage_Miller_OTA.pdf)**

<!-- 💡 强制加载后置 MathJax 渲染引擎，极速打开网页 -->
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