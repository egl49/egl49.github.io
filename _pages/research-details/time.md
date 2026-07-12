---
title: "Observational Cosmology Calibration and Instrumentation"
layout: page
permalink: /research/tomographic-ionized-carbon-intensity-mapping-experiment/
mathjax: true
---
The Tomographic Ionized Carbon Intensity Mapping Experiment (TIME)  works to deepen our understanding of the Epoch of Reionization, the era the Universe entered about a billion years after the Big Bang. To study this period, TIME uses a large instrument that can cool arrays of small, superconducting photon detectors to 250 mK. These detectors then observe CII emission at a wavelength of 157.7 micrometers. More information about the design, fabrication, and deployment of TIME can be found in<a href="https://thesis.caltech.edu/13683/” target="_blank">Jon Hunacek’s 2020 Dissertation</a>.

The detectors must be heated to a characteristic temperature, 450-700 mK, which differs for each due to manufacturing inconsistencies. Since the cryostat’s lowest level reaches 250 mK, all columns of the detectors are placed on a parallel circuit, with each detector within a column in series, and the current passed through the circuit is proportional to the power across each detector, and therefore the heat that will raise the temperature of the detector to the transition. Due to this setup, each column of detectors must receive the same current, even if the optimal transition temperature of each detector varies wildly. I wrote calibration code using Python to determine the optimal current level for each column on the detector arrays, that being the current level that would allow for the most detectors to function properly. I specifically used a kernel density estimation and a chi-square reduction to find the optimal current, then applied this current to the arrays during cooldown testing. 

I also worked on the instrument itself, creating a mount for a mirror that reflects the incident light into the spectrometers. I examined the distribution board that fed the current to each detector array to find broken connections and repair them. I used a crane to assemble and disassemble the instrument, and ran multiple test cooldowns to see the functionality of the instrument at its working temperature. 

Lastly, I improved the control code for an IR array that got mounted on a control module that could move in the x-y plane with a motor stepper. This IR source needed to be automated to change polarizations, change frequencies from a function generator, and move to new coordinates over the course of several hours to generate test data between yearly observatory runs. I utilized serial port programming to combine several different control scripts into one master script. 


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
<div id="img1-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/detectors.jpeg" alt="TES Bolometer Arrays">
<a href="#_" class="lightbox-close-btn">&times;</a>
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
<div id="img2-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/inside_cryo.jpeg" alt="Inside cryo">
<a href="#_" class="lightbox-close-btn">&times;</a>
</div>
</div>


<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img3-lightbox"><img src="{{ site.baseurl }}/images/research/ir_array.jpeg" alt="IR array" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
IR source array. 
</div>
</div>
<div id="img3-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/ir_array.jpeg" alt="IR array">
<a href="#_" class="lightbox-close-btn">&times;</a>
</div>
</div>

<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img4-lightbox"><img src="{{ site.baseurl }}/images/research/transition_plot.jpg" alt="transition plot" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
A transition plot for an individual detector. The section of negative slope is the interval on which the bias current should sit to allow for the detector to function normally. 
</div>
</div>
<div id="img4-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/transition_plot.jpg" alt="transition plot">
<a href="#_" class="lightbox-close-btn">&times;</a>
</div>
</div>

<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img5-lightbox"><img src="{{ site.baseurl }}/images/research/bias_finder_plot.png" alt="bias finder plot" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
A bias-finder plot, which shows all detector curves on a given column, and the optimal bias current overlapping as a dotted line. 
</div>
</div>
<div id="img5-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/bias_finder_plot.png" alt="bias finder plot">
<a href="#_" class="lightbox-close-btn">&times;</a>
</div>
</div>

<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img6-lightbox"><img src="{{ site.baseurl }}/images/research/kde_plot.png" alt="kde plot" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
A combination plot that features a rug plot with optimal transitions for all individual detectors on a column, overlayed with a kernel density estimation that denotes the bias current with the highest overlap. The peak of this KDE distribution is the bias current that is passed along that specific detector column.
</div>
</div>
<div id="img6-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/kde_plot.png" alt="kde plot">
<a href="#_" class="lightbox-close-btn">&times;</a>
</div>
</div>

<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img7-lightbox"><img src="{{ site.baseurl }}/images/research/circuit_diagram2.png" alt="column circuit diagram" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
A circuit diagram detailing the wiring setup for each column of the detector arrays.
</div>
</div>
<div id="img7-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/circuit_diagram2.png" alt="column circuit diagram">
<a href="#_" class="lightbox-close-btn">&times;</a>
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

.lightbox-overlay {
display: none;
position: fixed;
z-index: 9999;
top: 0;
left: 0;
width: 100vw;
height: 100vh;
background: var(--global-bg-color, #fff);
filter: drop-shadow(0 0 10px rgba(0,0,0,0.5));
align-items: center;
justify-content: center;
}
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
