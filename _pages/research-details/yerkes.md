---
title: "Observational/Historical Astronomy of Nebular Growth"
layout: page
permalink: /research/yerkes-observatory/
---

During the summer of 2025, I conducted a growth study of the Dumbbell Nebula (M27) that used observations from a time span of 119 years. A planetary nebula (PN) is a stage in the stellar life-cycle where an ordinary-mass star sheds its outer atmospheric layers as it leaves the main sequence. This reveals a condensed core, or a white dwarf (WD). PNs are only visible on the order of 10,000 years, which is much shorter than other stages of the stellar life-cycle for ordinary-mass stars. This shorter lifespan makes it much more plausible to observe visible changes that have occurred since astronomical imaging became possible. 

I conducted several observing runs over the course of the summer to capture a modern-day photo of M27, and I used the Yerkes 41” Reflector (Y41) and its CMOS camera to take exposures with empty, g’, i’, r’, H-alpha, and OIII filters. I used the pinpoint astrometry feature in MaximDL to insert World Coordinate System (WCS) information into the FITS (Flexible Image Transport System) header of each FITS file. This allowed me to have RA and Dec coordinates for every pixel in each image, and combine exposures over top of each-other to improve my signal-to-noise ratio. I stacked all my exposures using AstroImageJ, used the empty-filter exposures as my 2025 data point, and used the other filters to create a color image. 

I found over 20 different M27 plates in the Yerkes plate vault from different telescopes, and digitized all of them to allow for WCS information to be added to each file with astrometry.net. The plates used for this study are:
R-555: 90 min exposure taken by Jordan in 1906 on the Yerkes 24"
60PN-46: 60 min exposure taken by Ross in 1931 on the Mt. Wilson 60"
Y41-311: 60 min exposure taken by Cudworth in 1975 on the Yerkes 41"
Y41-749: unknown exposure time taken by Ulowetz on the Yerkes 41"

Other plates of M27 were removed due to tracking issues, emulsion deterioration, and saturation levels.

Due to the differing telescope sizes among the plates and modern observations, I cropped and aligned all my images to 13x13 arcmins around the central WD, using Caltech’s Montage for north alignment and Astropy’s Cutout2D to cut out the proper size. Then I rotated the image to have the narrowest axis of the nebula pointing vertically, and isolated the centermost rows of the rotated image. Then, I used an edge-detection method from OpenCV to convert each image into an outline, and found the outermost edge. This allowed me to find the radius of the nebula in pixels and convert it to arcsecs.

I also plotted flux curves across the nebula, then overlaid the cutoffs I found with OpenCV onto the flux curves. I could then plot the growth trends of the nebula, and I found a growth rate of 2.162 arcsec/century for the upper lobe, and 1.515 arcsec/century for the lower lobe (during the 1931 era). The 1906 data point was removed due to resolution issues that made it difficult to find the true cutoff, and the fact that the metadata of the plate did not detail the emulsion that was used for the exposure, which introduced another variable that may have affected the visual radius. 

The growth rates for both lobes were consistent with published values for M27, of about 2.0 arcsec/century. For even more detail, please refer to my AAS iPoster on my publications tab. 

<div class="custom-gallery-container" style="margin: 30px 0; overflow: hidden; width: 100%;">
<div class="custom-gallery-scroll" style="display: flex; gap: 16px; overflow-x: auto; scroll-snap-type: x mandatory; padding-bottom: 12px; -webkit-overflow-scrolling: touch;">

<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden; transition: border-color 0.2s ease, transform 0.2s ease;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img1-lightbox"><img src="{{ site.baseurl }}/images/research/color_dumbbell.jpeg" alt="Dumbbell False Color Image" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
False color image of the Dumbbell Nebula (M27), taken on the Yerkes 41" Reflector in 2025. 
</div>
</div>
<div id="img1-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/color_dumbbell.jpeg" alt="Dumbbell False Color Image">
<a href="#_" class="lightbox-close-btn">&times;</a>
</div>
</div>


<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden; transition: border-color 0.2s ease, transform 0.2s ease;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img2-lightbox"><img src="{{ site.baseurl }}/images/research/distance_from_white_dwarf.jpeg" alt="growth plot" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
Distance from white dwarf as a function of year. Separate lin regressions were made for 1906-1931 and 1931-2025 due to the inconsistencies in the 1906 plate discussed earlier. 
</div>
</div>
<div id="img2-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/distance_from_white_dwarf.jpeg" alt="growth plot">
<a href="#_" class="lightbox-close-btn">&times;</a>
</div>
</div>


<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden; transition: border-color 0.2s ease, transform 0.2s ease;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img3-lightbox"><img src="{{ site.baseurl }}/images/research/dumbbell_plate.jpeg" alt="dumbbell plate" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
An M27 plate from the Yerkes collection.
</div>
</div>
<div id="img3-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/dumbbell_plate.jpeg" alt="dumbbell plate">
<a href="#_" class="lightbox-close-btn">&times;</a>
</div>
</div>

<div class="gallery-item" style="flex: 0 0 300px; scroll-snap-align: start; display: flex; flex-direction: column; background-color: var(--global-card-bg, rgba(255, 255, 255, 0.02)); border: 1px solid var(--global-border-color, rgba(255,255,255,0.1)); border-radius: 8px; overflow: hidden; transition: border-color 0.2s ease, transform 0.2s ease;">
<div style="width: 100%; height: 200px; overflow: hidden;">
<a href="#img4-lightbox"><img src="{{ site.baseurl }}/images/research/yerkes_in_dome.jpg" alt="y41 dome" style="width: 100%; height: 100%; object-fit: cover; cursor: pointer;"></a>
</div>
<div class="gallery-caption" style="padding: 12px; font-size: 0.85em; color: var(--global-text-color); line-height: 1.4; border-top: 1px solid var(--global-border-color, rgba(255,255,255,0.1));">
Me inside the Y41 dome!
</div>
</div>
<div id="img4-lightbox" class="lightbox-overlay">
<a href="#_" class="lightbox-close-bg"></a>
<div class="lightbox-content">
<img src="{{ site.baseurl }}/images/research/yerkes_in_dome.jpg" alt="y41 dome">
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

.gallery-item:hover {
border-color: #733BEB !important;
transform: translateY(-2px);
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



<!-- Back Button Link -->
<a href="{{ site.url }}{{ site.baseurl }}/research/" style="display: inline-block; background-color: rgba(115, 59, 235, 0.1); color: #733BEB; border: 1px solid #733BEB; padding: 6px 16px; border-radius: 20px; text-decoration: none; font-size: 0.85em; font-weight: 500; margin-bottom: 30px; transition: background 0.2s;" onmouseover="this.style.backgroundColor='rgba(115, 59, 235, 0.2)'" onmouseout="this.style.backgroundColor='rgba(115, 59, 235, 0.1)'">
  ← Back to Research
</a>
