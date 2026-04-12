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
  MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$', '$$'], ['\\[', '\\]']],
      processEscapes: true
    }
  };
</script>
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
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
  
  /* 2. 控制大标题 (##) 和小标题 (###) 周围的间距 */
  .page__content h2,
  .page__content h3 {
    /* 💡 控制标题距离上一段的空白（默认非常大） */
    margin-top: 0.8em !important;    
    /* 💡 控制标题距离下一段的空白 */
    margin-bottom: 0.3em !important; 
  }
</style>

## I. Project Overview
This project focuses on the design and optimization of a multi-section microstrip impedance matching network. The objective was to match a 200 $\Omega$ lumped resistor load to a 50 $\Omega$ source at a center frequency of 2 GHz. 

To maximize bandwidth while satisfying strict fabrication constraints, a modified 3-section Chebyshev transformer was synthesized. Through iterative schematic tuning and layout optimization, the final Momentum electromagnetic (EM) simulation achieved a 93.6% fractional bandwidth with a highly compact footprint of 25.8 × 27.1 mm², significantly exceeding all initial design specifications.

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
* $Z_1 = 68.97\ \Omega$: $W_1 = 2.87\text{ mm}$, $L_1 = 27.72\text{ mm}$
* $Z_2 = 100\ \Omega$: $W_2 = 1.38\text{ mm}$, $L_2 = 28.25\text{ mm}$
* $Z_3 = 145\ \Omega$: $W_3 = 0.504\text{ mm}$, $L_3 = 28.73\text{ mm}$

---

## III. Schematic Design and Miniaturization
### A. Straight Transformer Tuning
The calculated dimensions were initially implemented using straight microstrip lines (`MLIN`). Due to our analytical modifications, the initial $S_{11}$ curve slightly deviated from the $-20\text{ dB}$ limit at the ripple peaks. The ADS Tuning tool was utilized to fine-tune section dimensions, re-centering the optimal matching response at 2 GHz.

<figure>
  <img src="/assets/portfolio_images/3_sec_after_tuning.png" alt="Straight Transformer Schematic">
  <figcaption>Schematic of the 3-section transformer after initial tuning.</figcaption>
</figure>

### B. Meandered Architecture
A linear connection of the three sections results in a total length exceeding 84 mm. To satisfy the strict $28 \times 28\text{ mm}^2$ spatial constraint, the network was aggressively meandered using `MCURVE` elements. The electrical length of each stage was conserved by subtracting curve physical lengths from adjacent straight segments. The structure was carefully routed to minimize unwanted parallel trace coupling, followed by subsequent tuning to absorb bend-induced parasitic reactances.

<figure>
  <img src="/assets/portfolio_images/3_sec_curved_after_tuning.png" alt="Curved Transformer Schematic">
  <figcaption>Schematic of the miniaturized meandered 3-section transformer.</figcaption>
</figure>

---

## IV. EM Simulation and Layout Optimization

An iterative EM-Schematic simulation approach was crucial. Initial Momentum simulations revealed severe frequency shifts and performance degradation primarily caused by electromagnetic coupling between closely meandered segments. 

To mitigate this, the physical layout was meticulously optimized within the boundary constraint to maximize spatial separation between traces. Concurrently, schematic parameters were iteratively tuned based on Momentum feedback to pre-compensate for residual coupling and unmodeled pad/via parasitics. 

<figure>
  <img src="/assets/portfolio_images/3_sec_curved_layout.png" alt="Final EM Layout">
  <figcaption>Final Momentum layout of the matching network ($25.8 \times 27.1\text{ mm}^2$).</figcaption>
</figure>

---

## V. Results and Performance
### A. EM vs. Schematic Comparison
The overlaid $S_{11}$ results demonstrate excellent agreement between the final schematic and Momentum EM simulations. The layout parasitics introduce only slight variations in null depth and position. 
* Center Frequency Return Loss: $-25.5\text{ dB}$ at $2\text{ GHz}$
* $20\text{ dB}$ Bandwidth: $1.058\text{ GHz}$ to $2.931\text{ GHz}$
* Fractional Bandwidth: $93.6\%$

<figure>
  <img src="/assets/portfolio_images/comparison.png" alt="S11 Comparison Chart">
  <figcaption>Comparison of $S_{11}$ between schematic and Momentum EM simulation.</figcaption>
</figure>

### B. Expected Power Loss
ADS power loss simulations verified the low-loss characteristics of the design. The total power loss ratio at the center frequency is approximately 0.003, translating to a 99.7% transmission efficiency.

<figure>
  <img src="/assets/portfolio_images/Power_loss.png" alt="Power Loss Graph">
  <figcaption>Expected total loss of the matching network across the frequency band.</figcaption>
</figure>

---

## VI. Conclusion
A highly compact, 3-section Chebyshev matching network was successfully designed, simulated, and validated. By mathematically reconstructing the impedance profile to navigate fabrication limits and utilizing advanced meandering techniques, the final Momentum layout achieved an exceptional 93.6% fractional bandwidth within a minimal footprint. All performance metrics comfortably exceeded project specifications.