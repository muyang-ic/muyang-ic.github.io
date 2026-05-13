---
layout: single
mathjax: true
title: "Compact Ultra-Broadband Impedance Matching Network"
excerpt: "Design and EM simulation of a 3-section Chebyshev transformer achieving 93.6% fractional bandwidth at 2 GHz, miniaturized to a 25.8 × 27.1 mm² footprint."
categories: 
  - Project
tags: 
  - ECE
  - Microwave
  - Hardware
header:
  teaser: /assets/portfolio_images/3_sec_curved_layout.png
  overlay_image: /assets/portfolio_images/comparison.png
  overlay_filter: 0.6
---
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
  
/* 2. 独立控制：大标题 (对应 Markdown 里的 ##) */
  .page__content h2 {
    font-size: 1.3em !important;       /* 大标题字号 */
    margin-top: 0.25em !important;      /* 距离上文的留白（建议大一点，拉开章节差距） */
    margin-bottom: 0.1em !important;   /* 距离下文的留白（紧凑一点，压住正文） */
    /*border-bottom: 1px solid #eee !important; /* 可选：加一条极浅的底线增加专业感 */
    /*padding-bottom: 0.3em !important;*/
  }

  /* 3. 独立控制：小标题 (对应 Markdown 里的 ###) */
  .page__content h3 {
    font-size: 1.0em !important;       /* 小标题字号 */
    margin-top: 0.2em !important;      /* 距离上文的留白（比大标题略小） */
    margin-bottom: 0.02em !important;   /* 距离下文的留白 */
  }
</style>

## I. Project Overview
This project focuses on the design and optimization of a multi-section microstrip impedance matching network. The objective was to match a 200 $\Omega$ lumped resistor load to a 50 $\Omega$ source at a center frequency of 2 GHz. 

To maximize bandwidth while satisfying strict fabrication constraints, a modified **3-section Chebyshev transformer** was synthesized. Through iterative schematic tuning and layout optimization, the final Momentum electromagnetic (EM) simulation achieved a **93.6% fractional bandwidth** with a highly compact footprint of **25.8 × 27.1 mm²**, significantly exceeding all initial design specifications.

---

## II. Rationale Behind Design Choices

### A. Topology Selection
To achieve a broadband response well beyond the minimum 40% requirement, a multi-section transformer was chosen over narrow-band stub matching. A Chebyshev polynomial response was targeted for its optimal equal-ripple passband behavior. Although an $N=2$ design would satisfy the minimum criteria, an $N=3$ architecture was pursued to push the theoretical limits of maximum achievable bandwidth.

### B. Navigating Fabrication Constraints
According to standard Chebyshev tables (for $\Gamma_m = 0.05$ and an impedance ratio of 4), the required impedance closest to the load must be $Z_3 = 157.95\ \Omega$. However, ADS LineCalc indicated that such a line on the specified Rogers RT/duroid 5880 substrate would have a width of only $0.37\text{ mm}$, directly violating the strict fabrication rule of minimum width $\ge 0.5\text{ mm}$.

To resolve this, the maximum allowable impedance satisfying $W \ge 0.5\text{ mm}$ was calculated to be $145\ \Omega$. To maintain a symmetric reflection profile, the center section impedance was geometrically averaged:
$$Z_2 = \sqrt{Z_0 Z_L} = \sqrt{50 \times 200} = 100\ \Omega$$

By leveraging the theory of small reflections for symmetric networks ($\gamma_0 = \gamma_3$ and $\gamma_1 = \gamma_2$), the modified characteristic impedances were derived:
$$\gamma_2 = \frac{Z_3 - Z_2}{Z_3 + Z_2} = \frac{145 - 100}{145 + 100} \approx 0.1837$$
$$\gamma_1 = \frac{Z_2 - Z_1}{Z_2 + Z_1} \implies Z_1 = Z_2 \frac{1 - \gamma_1}{1 + \gamma_1} \approx 68.97\ \Omega$$

Based on these adjusted impedances, the theoretical initial dimensions synthesized at 2 GHz are:
* **$Z_1 = 68.97\ \Omega$:** $W_1 = 2.87\text{ mm}$, $L_1 = 27.72\text{ mm}$
* **$Z_2 = 100\ \Omega$:** $W_2 = 1.38\text{ mm}$, $L_2 = 28.25\text{ mm}$
* **$Z_3 = 145\ \Omega$:** $W_3 = 0.504\text{ mm}$, $L_3 = 28.73\text{ mm}$

---

## III. Schematic Design and Miniaturization

### A. Straight Transformer Tuning
The calculated dimensions were initially implemented using straight microstrip lines (`MLIN`). Due to our analytical modifications, the initial $S_{11}$ curve slightly deviated from the $-20\text{ dB}$ limit at the ripple peaks. The ADS Tuning tool was utilized to fine-tune section dimensions, re-centering the optimal matching response at 2 GHz.

<figure>
  <img src="/assets/portfolio_images/3_sec_after_tuning.png" alt="Straight Transformer Schematic" loading="lazy" decoding="async">
  <figcaption>Schematic of the 3-section transformer after initial tuning.</figcaption>
</figure>

### B. Meandered Architecture
A linear connection of the three sections results in a total length exceeding 84 mm. To satisfy the strict $28 \times 28\text{ mm}^2$ spatial constraint, the network was aggressively meandered using `MCURVE` elements. The electrical length of each stage was conserved by subtracting curve physical lengths from adjacent straight segments. The structure was carefully routed to minimize unwanted parallel trace coupling, followed by subsequent tuning to absorb bend-induced parasitic reactances.

<figure>
  <img src="/assets/portfolio_images/3_sec_curved_after_tuning.png" alt="Curved Transformer Schematic" loading="lazy" decoding="async">
  <figcaption>Schematic of the miniaturized meandered 3-section transformer.</figcaption>
</figure>

---

## IV. EM Layout Implementation

For the physical layout, mounting pads for the 0805 resistor were designed with dimensions $W = 0.7\text{ mm}$ and $L = 1.3\text{ mm}$, separated by a $1.7\text{ mm}$ gap. A $0.4\text{ mm}$ diameter via was added to ground the load. The substrate stackup configured for the Momentum simulation, explicitly defining the Rogers 5880 dielectric layer and the via hole, is depicted below.

<figure>
  <img src="/assets/portfolio_images/substrate.png" alt="Momentum Substrate Stackup" loading="lazy" decoding="async">
  <figcaption>Momentum substrate stackup defining the dielectric layer and grounding via.</figcaption>
</figure>

A rigorous iterative co-simulation approach was employed: we discovered frequency shifts and performance degradation in the initial layout results. We determined the cause to be unwanted electromagnetic coupling between the closely meandered transmission line segments and parasitics from the physical pads and grounding via. To correct this, we modified the schematic parameters to pre-compensate for the parasitic reactances and maximized spatial separation within the footprint, and finally re-simulated the layout. This process was repeated until the EM-simulated $S_{11}$ fully complied with the wideband specification.

<figure>
  <img src="/assets/portfolio_images/3_sec_curved_layout.png" alt="Final EM Layout" loading="lazy" decoding="async">
  <figcaption>Final meandered layout of the matching network ($25.8 \times 27.1\text{ mm}^2$).</figcaption>
</figure>

<figure>
  <img src="/assets/portfolio_images/em_layout.png" alt="3D Momentum Layout" loading="lazy" decoding="async">
  <figcaption>3D view of the matching network layout in Momentum.</figcaption>
</figure>

---

## V. Simulation Results and Discussion

### A. EM vs. Schematic Comparison
The overlaid $S_{11}$ results demonstrate excellent agreement between the final schematic and Momentum EM simulations. The layout parasitics introduce only slight variations in null depth and position. 
* Center Frequency Return Loss: $-25.5\text{ dB}$ at $2\text{ GHz}$
* $20\text{ dB}$ Bandwidth: $1.058\text{ GHz}$ to $2.931\text{ GHz}$
* Fractional Bandwidth: $93.6\%$

<figure>
  <img src="/assets/portfolio_images/comparison.png" alt="S11 Comparison Chart" loading="lazy" decoding="async">
  <figcaption>Comparison of $S_{11}$ between schematic and Momentum EM simulation.</figcaption>
</figure>

### B. Calculation of Expected Loss
The expected power loss of the passive matching network is evaluated using the principle of energy conservation, defined as:
$$\text{Loss} = 1 - |S_{11}|^2 - |S_{21}|^2$$

For the schematic simulation, the evaluated power dissipation at the 2 GHz center frequency is approximately 0.012, translating to a power loss of 1.2%.

<figure>
  <img src="/assets/portfolio_images/schematic_loss_2.png" alt="Schematic Simulation Loss" loading="lazy" decoding="async">
  <figcaption>Simulated total power loss ratio evaluated using S-parameter magnitudes (Schematic).</figcaption>
</figure>

For the Momentum simulation, the loss at 2 GHz is approximately 0.023 (or 2.3%). The slightly higher loss in the Momentum simulation accurately reflects the additional ohmic losses, skin effects, and dielectric dissipation introduced by the physical copper traces and the Rogers 5880 substrate, which are not fully captured by ideal schematic models. Nevertheless, an overall transmission efficiency of 97.7% confirms the excellent low-loss characteristics of the final layout.

<figure>
  <img src="/assets/portfolio_images/momentum_loss_2.png" alt="Momentum Simulation Loss" loading="lazy" decoding="async">
  <figcaption>Simulated total power loss ratio evaluated using S-parameter magnitudes (Momentum).</figcaption>
</figure>

---

## VI. Conclusion
A highly compact, 3-section Chebyshev matching network was successfully designed and validated. By mathematically reconstructing the impedance profile to respect the 0.5 mm fabrication limit and utilizing meandering techniques for miniaturization, the final Momentum layout achieved an exceptional 93.6% fractional bandwidth within a $25.8 \times 27.1\text{ mm}^2$ footprint. All performance metrics met or exceeded the project specifications.

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