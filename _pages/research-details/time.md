---
title: "Observational Cosmology Calibration and Instrumentation"
layout: page
permalink: /research/tomographic-ionized-carbon-intensity-mapping-experiment/
mathjax: true
---



<div class="custom-gallery-container" style="margin: 30px 0; overflow: hidden; width: 100%;">
<div class="custom-gallery-scroll" style="display: flex; gap: 16px; overflow-x: auto; scroll-snap-type: x mandatory; padding-bottom: 12px; -webkit-overflow-scrolling: touch;">
<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img1-lightbox"><img src="{{ site.baseurl }}/images/research/detectors.jpeg" alt="TES Bolometer Arrays" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
TES Bolometer Arrays.
</div>
</div>
<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img2-lightbox"><img src="{{ site.baseurl }}/images/research/inside_cryo.jpeg" alt="Inside cryo" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
Wiring inside of the cryostat.
</div>
</div>
<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img2-lightbox"><img src="{{ site.baseurl }}/images/research/ir_array.jpeg" alt="IR array" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
IR source array. 
</div>
</div>
</div>
</div>

<div id="img1-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/u_expansion_order.jpeg" alt="Comparison of u expansion orders to legacy solver">
<a href="#_" class="lightbox-close-btn">&times;</a>
</div>
</div>

<div id="img2-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/u_residuals.jpeg" alt="Residual u plot">
<a href="#_" class="lightbox-close-btn">&times;</a>
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

/* Light/Dark mode responsive lightbox overlay */
.lightbox-overlay {
  display: none;
  position: fixed;
  z-index: 9999;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  /* Uses theme bg with high opacity so text/header behind it gets cleanly masked */
  background: var(--global-bg-color, #fff);
  filter: drop-shadow(0 0 10px rgba(0,0,0,0.5));
  align-items: center;
  justify-content: center;
}
/* Fallback treatment via CSS translucent masking if your theme variable has transparency */
@defaults {
  .lightbox-overlay {
    background: rgba(var(--global-bg-color-rgb, 0, 0, 0), 0.95);
  }
}

.lightbox-overlay:target {
  display: flex;
}
.lightbox-close-bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  cursor: default;
}
.lightbox-content {
  position: relative;
  max-width: 90%;
  max-height: 90%;
  box-shadow: 0 10px 40px rgba(0,0,0,0.3);
  border-radius: 6px;
  overflow: hidden;
  display: flex;
  background: var(--global-card-bg, rgba(0,0,0,0.05));
}
.lightbox-content img {
  max-width: 100%;
  max-height: 85vh;
  object-fit: contain;
  margin: auto;
}
.lightbox-close-btn {
  position: absolute;
  top: 15px;
  right: 20px;
  /* Close symbol matches your theme text color instead of forcing white */
  color: var(--global-text-color, #000);
  font-size: 35px;
  text-decoration: none;
  font-weight: 300;
  line-height: 1;
  transition: transform 0.2s, color 0.2s;
}
.lightbox-close-btn:hover {
  color: #733BEB;
  transform: scale(1.1);
}
</style>

<a href="{{ site.url }}{{ site.baseurl }}/research/" style="display: inline-block; background-color: rgba(115, 59, 235, 0.1); color: #733BEB; border: 1px solid #733BEB; padding: 6px 16px; border-radius: 20px; text-decoration: none; font-size: 0.85em; font-weight: 500; margin-bottom: 30px; transition: background 0.2s;" onmouseover="this.style.backgroundColor='rgba(115, 59, 235, 0.2)'" onmouseout="this.style.backgroundColor='rgba(115, 59, 235, 0.1)'">
← Back to Research
</a>
