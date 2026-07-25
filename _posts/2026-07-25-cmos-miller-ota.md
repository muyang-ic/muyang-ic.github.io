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
  /* 1. 调节文章正文、列表和数学公式的字号与间距 */
  .page__content p, 
  .page__content li, 
  .MathJax {
    font-size: 0.9em !important; 
    line-height: 1.6 !important;  
    /* 💡 下面这行就是控制段落间距的绝杀！数值越小，段落靠得越紧 */
    margin-bottom: 0.6em !important; 
  }
</style>

This project focuses on the design and optimization of a CMOS two-stage Miller compensated operational transconductance amplifier (OTA) based on the TSMC 180nm process. 

The final core performance achieved an open-loop DC gain of 87 dB, a Phase Margin of 66.4°, and a GBW of 61 MHz. 

For more details, please refer to the complete project report below:

**[Read / Download the Full Project Report (PDF)](/assets/pdfs/CMOS_Two-Stage_Miller_OTA.pdf)**

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