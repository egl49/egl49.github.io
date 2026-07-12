---
title: "Numerical Relativity & Compact Objects"
layout: page
permalink: /research/simulating-extreme-spacetimes/
mathjax: true
---

I am working towards my senior thesis in this role, where I implement modified Tolman–Oppenheimer–Volkoff Equations in Python to numerically solve theoretical neutron stars with different equations of state (EOS), and perform error analysis to determine the validity of simulated solutions. The form of the TOV equations I am using are based on the ones defined by <a href="https://doi.org/10.48550/arXiv.gr-qc/9802072" target="_blank">Lindblom, Lee (1998)</a>, and  <a href="https://spectre-code.org/classRelativisticEuler_1_1Solutions_1_1TovSolution.html#details" target="_blank">SpECTRE’s TOV solver code</a>. The coupled ODE’s are as follows: 

$$\frac{du}{dH} = -\frac{2u(1-2v)}{4\pi u p(h) + v}$$

$$\frac{dv}{dH} = -(1-2v)\frac{4\pi u e(h) - v}{4\pi u p(h) + v}$$

And the EOS that I work most frequently with is the polytropic EOS $p = K\rho^\Gamma$


 Currently, my project is to improve the simulated solutions of the TOV equations by performing an expansion around the singular point at the start of integration. I am working to implement this expansion completely analytically so that it can be generalizable to all equations of state. I have performed an integration for the first four orders of expansion and have performed an error comparison for each expansion order to determine the radius about the stellar center for which the expansion is valid. The error comparison looks like: 

$$(h_c-h) \leq \frac{|u_1|}{|2u_2|} 10^{-15}$$

And is generalizable to higher orders. This allows me to determine when the numerical error becomes smaller than machine precision. The final expansion terms that I have found are as follows:
$$\begin{align}
&\begin{aligned}
\frac{du}{dH} =& -\frac{3}{2 \pi \left(e_{c} + 3 p_{c}\right)}\\
&-2\frac{15(3p_c-e_c) - 9e_1}{20\pi ( e_c + 3p_c)^2}(H_c-H) \\
&-3[\frac{3p_c-5e_c}{4\pi (e_c+3p_c)^2}
-\frac{3e_2}{14\pi (e_c+3p_c)^2}
+\frac{3e_1(48e_1-95e_c-765p_c)}
{700\pi (e_c+3p_c)^3}](H_c-H)^2
\end{aligned}
\\
&\begin{aligned}
\frac{dv}{dH} =& -\frac{2 e_{c}}{e_{c} + 3 p_{c}}\\
&-2\frac{5e_c(3p_c-e_c) + 3(e_c + 6p_c)e_1}{5(e_c+3p_c)^2}(H_c-H) \\
&-3[
 \frac{e_c(3p_c-5e_c)}
{3(e_c+3p_c)^2}
+\frac{2(2e_c+9p_c)e_2}
{7(e_c+3p_c)^2}
\\
&-\frac{
5(46e_c^2+153e_cp_c-243p_c^2)e_1
+3(11e_c+81p_c)e_1^2
}
{175(e_c+3p_c)^3}](H_c-H)^2
\end{aligned}
\end{align}$$


I am also investigating the tidal deformability factor of simulated neutron stars with different equations of state and whether future gravitational wave detectors will have a high enough resolution to detect any differences in neutron star inspirals that may indicate what equations of state are most accurate.


## Appendix: Fluid Dynamics & Equation of State Framework

### 1. Variables
* **Mass Density ($\rho$)**
* **Pressure ($p$)**
* **Specific Internal Energy Density ($\epsilon$)**
* **Total Energy Density ($e$):** $$e = \rho(1 + \epsilon)$$
* **Relativistic Enthalpy ($h$):** $$h = \frac{e + p}{\rho} = 1 + \epsilon + \frac{p}{\rho}$$
* **Logarithmic Enthalpy ($H$):** $$H = \ln(h)$$

---

### 2. Polytropic Relations
Using adiabatic index $\Gamma$ and coefficient $K$:

$$\epsilon = \frac{K \rho^{\Gamma-1}}{\Gamma - 1} = \frac{p}{(\Gamma - 1)\rho}$$

#### Total Energy Density
$$e = \rho \left(1 + \frac{K\rho^{\Gamma-1}}{\Gamma - 1}\right)$$

#### Specific Enthalpy
$$h = 1 + \frac{K\rho^{\Gamma-1}}{\Gamma - 1} + K\rho^{\Gamma-1} = 1 + \frac{\Gamma K \rho^{\Gamma-1}}{\Gamma - 1}$$

#### Density Inversion
$$\rho = \left[ \frac{\Gamma - 1}{\Gamma K} (h - 1) \right]^{\frac{1}{\Gamma - 1}}$$

---

### 3. Scaling Approximations
Given the structural parameters defined as $u := r^2$ and $v := \frac{m}{r}$, the volumetric mass-energy scaling profile reduces to:

$$\begin{aligned}
v &\approx \frac{4}{3}\pi u e \\[1ex]
\frac{m}{r} &\approx \frac{4}{3}\pi r^2 e
\end{aligned}$$

<div class="custom-gallery-container" style="margin: 30px 0; overflow: hidden; width: 100%;">
  <div class="custom-gallery-scroll" style="display: flex; gap: 16px; overflow-x: auto; scroll-snap-type: x mandatory; padding-bottom: 12px; -webkit-overflow-scrolling: touch;">
    
    <div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
      <div style="width: 100%; height: 200px; overflow: hidden;">
        <img src="{{ site.baseurl }}/assets/img/your-image-1.jpg" alt="Description" style="width: 100%; height: 100%; object-fit: cover;">
      </div>
      <div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
        Caption text describing your research setup, event timeline, or group metrics here.
      </div>
    </div>

    <div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
      <div style="width: 100%; height: 200px; overflow: hidden;">
        <img src="{{ site.baseurl }}/assets/img/your-image-2.jpg" alt="Description" style="width: 100%; height: 100%; object-fit: cover;">
      </div>
      <div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
        Caption text detailing simulation code diagnostics or performance data.
      </div>
    </div>

  </div>
</div>

<style>
  .custom-gallery-scroll::-webkit-scrollbar {
    height: 6px;
  }
  .custom-gallery-scroll::-webkit-scrollbar-track {
    background: transparent;
  }
  .custom-gallery-scroll::-webkit-scrollbar-thumb {
    background: var(--global-divider-color, rgba(255, 255, 255, 0.15));
    border-radius: 10px;
  }
  .custom-gallery-scroll::-webkit-scrollbar-thumb:hover {
    background: #733BEB;
  }
</style>


<!-- Back Button Link -->
<a href="{{ site.url }}{{ site.baseurl }}/research/" style="display: inline-block; background-color: rgba(115, 59, 235, 0.1); color: #733BEB; border: 1px solid #733BEB; padding: 6px 16px; border-radius: 20px; text-decoration: none; font-size: 0.85em; font-weight: 500; margin-bottom: 30px; transition: background 0.2s;" onmouseover="this.style.backgroundColor='rgba(115, 59, 235, 0.2)'" onmouseout="this.style.backgroundColor='rgba(115, 59, 235, 0.1)'">
  ← Back to Research
</a>
