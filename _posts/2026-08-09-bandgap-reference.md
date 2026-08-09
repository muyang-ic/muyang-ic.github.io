---
layout: single
title: "Design of a CMOS Bandgap Reference (BGR)"
excerpt: "A comprehensive design and optimization of a CMOS Bandgap Reference using the TSMC 180nm process, featuring a folded-cascode op-amp and global temperature compensation."
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
    width: max-content !important; /* 💡 绝杀：解除主题默认的 100% 宽度限制，让表格收缩到内容的真实宽度 */
    margin-left: auto !important;
    margin-right: auto !important;
  }

  /* 3. 极大缩小图片容器下方的留白 */
  .page__content figure {
    margin-top: 0.1em !important; /* 💡 如果觉得还是大，可以改成 0em */
    margin-bottom: 0.2em !important; /* 💡 如果觉得还是大，可以改成 0em */
  }
</style>

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