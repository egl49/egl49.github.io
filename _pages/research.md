---
title: "Research"
layout: gridlay
sitemap: false
permalink: /research/
---

## Research
![Uploading image.png…]()


{::options parse_block_html="false" /}
<div class="research-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 24px; margin-top: 20px;">
  {% for exp in site.data.experiences %}
    {% if exp.type == "research" %}
      
      <div id="{{ exp.id }}" class="research-card" style="background: #fff; border: 1px solid #e1e1e1; border-radius: 12px; overflow: hidden; display: flex; flex-direction: column; box-shadow: 0 4px 12px rgba(0,0,0,0.01); transition: transform 0.2s ease, box-shadow 0.2s ease;">
        
        {% if exp.image and exp.image != "" %}
          <div class="card-image-wrapper" style="width: 100%; height: 180px; overflow: hidden; border-bottom: 1px solid #e1e1e1;">
            <img src="{{ site.url }}{{ site.baseurl }}/assets/img/{{ exp.image }}" alt="{{ exp.title }}" style="width: 100%; height: 100%; object-fit: cover;">
          </div>
        {% endif %}

        <div class="research-body" style="padding: 24px; flex: 1; display: flex; flex-direction: column; justify-content: space-between;">
          <div>
            <h4 class="research-title" style="margin-top: 0; margin-bottom: 8px; font-size: 1.25em; font-weight: 700; line-height: 1.4; color: #111;">
              {{ exp.title }}
            </h4>
            
            <p style="margin: 0 0 14px 0; font-size: 0.85em; color: #666; line-height: 1.6;">
              {% if exp.organization and exp.organization != "" %}<strong>Org:</strong> {{ exp.organization }}<br>{% endif %}
              {% if exp.advisor and exp.advisor != "" %}<strong>Advisor:</strong> {{ exp.advisor }}<br>{% endif %}
              {% if exp.term and exp.term != "" %}<strong>Term:</strong> {{ exp.term }}{% endif %}
            </p>

            <p class="research-desc" style="font-size: 0.95em; color: #444; line-height: 1.6; margin-bottom: 20px;">
              {{ exp.description }}
            </p>
          </div>

          <div class="skill-badges" style="margin-top: auto; padding-top: 10px;">
            {% for skill in exp.skills %}
              <span style="display: inline-block; background: rgba(115, 59, 235, 0.06); color: #733BEB; font-size: 0.75em; padding: 4px 10px; border-radius: 12px; margin-right: 6px; margin-bottom: 6px; font-weight: 600; letter-spacing: 0.2px;">
                {{ skill }}
              </span>
            {% endfor %}
          </div>

        </div>
      </div>

    {% endif %}
  {% endfor %}
</div>

<div class="research-grid">

  <!-- 1. NEUTRON STARS CARD -->
  <a href="{{ site.url }}{{ site.baseurl }}/research/simulating-extreme-spacetimes/" style="text-decoration: none; color: inherit; display: block; margin-bottom: 20px;">
    <div class="research-card" style="cursor: pointer; display: flex; transition: transform 0.2s ease-in-out; background: #fff; border: 1px solid #e1e1e1; border-radius: 8px; padding: 15px;" onmouseover="this.style.transform='scale(1.01)'" onmouseout="this.style.transform='scale(1)'">
      <img src="{{ site.url }}{{ site.baseurl }}/images/research/neutron-stars.svg" class="research-thumb" alt="Neutron star simulation" style="width: 100px; height: 100px; object-fit: cover; margin-right: 20px;">
      <div class="research-body" style="flex: 1;">
        <h4 class="research-title" style="margin-top: 0; margin-bottom: 4px;">Numerical Relativity & Compact Objects</h4>
        <div class="research-subtitles" style="font-size: 0.82em; color: #666; margin-bottom: 8px; line-height: 1.4;">
          <strong>Organization:</strong> Simulating eXtreme Spacetimes <br>
          <strong>Advisor:</strong> Prof. Nils Deppe <br>
          <strong>Term:</strong> Aug 2025 – Present
        </div>
        <p class="research-desc" style="margin-top: 0;">Investigating the tidal deformability of neutron stars using numerical relativity tools... </p>
        <div style="display: block; margin-top: 8px; color: #733BEB; font-weight: bold; font-size: 0.9em;">Read more →</div>
      </div>
    </div>
  </a>

  <!-- 2. DUMBBELL NEBULA CARD -->
  <a href="{{ site.url }}{{ site.baseurl }}/research/yerkes-observatory/" style="text-decoration: none; color: inherit; display: block; margin-bottom: 20px;">
    <div class="research-card" style="cursor: pointer; display: flex; transition: transform 0.2s ease-in-out; background: #fff; border: 1px solid #e1e1e1; border-radius: 8px; padding: 15px;" onmouseover="this.style.transform='scale(1.01)'" onmouseout="this.style.transform='scale(1)'">
      <img src="{{ site.url }}{{ site.baseurl }}/images/research/nebula.svg" class="research-thumb" alt="Dumbbell Nebula M27" style="width: 100px; height: 100px; object-fit: cover; margin-right: 20px;">
      <div class="research-body" style="flex: 1;">
        <h4 class="research-title" style="margin-top: 0; margin-bottom: 4px;">Observational Astronomy & Nebular Evolution</h4>
        <div class="research-subtitles" style="font-size: 0.82em; color: #666; margin-bottom: 8px; line-height: 1.4;">
          <strong>Organization:</strong> Yerkes Observatory <br>
          <strong>Advisor:</strong> Dr. Amanda Bauer <br>
          <strong>Term:</strong> May 2025 – Aug 2025
        </div>
        <p class="research-desc" style="margin-top: 0;">Analyzing long-baseline evolutionary characteristics of planetary nebulae...</p>
        <div style="display: block; margin-top: 8px; color: #733BEB; font-weight: bold; font-size: 0.9em;">Read more →</div>
      </div>
    </div>
  </a>

  <!-- 3. TIME INSTRUMENT CARD -->
  <a href="{{ site.url }}{{ site.baseurl }}/research/tomographic-ionized-carbon-intensity-mapping-experiment/" style="text-decoration: none; color: inherit; display: block; margin-bottom: 20px;">
    <div class="research-card" style="cursor: pointer; display: flex; transition: transform 0.2s ease-in-out; background: #fff; border: 1px solid #e1e1e1; border-radius: 8px; padding: 15px;" onmouseover="this.style.transform='scale(1.01)'" onmouseout="this.style.transform='scale(1)'">
      <img src="{{ site.url }}{{ site.baseurl }}/images/research/instrumentation.svg" class="research-thumb" alt="TIME Instrument detector" style="width: 100px; height: 100px; object-fit: cover; margin-right: 20px;">
      <div class="research-body" style="flex: 1;">
        <h4 class="research-title" style="margin-top: 0; margin-bottom: 4px;">Astronomical Instrumentation</h4>
        <div class="research-subtitles" style="font-size: 0.82em; color: #666; margin-bottom: 8px; line-height: 1.4;">
          <strong>Institution:</strong> Tomographic Ionized Carbon Intensity Mapping Experiment (TIME) <br>
          <strong>Advisor:</strong> Prof. Abigail Crites <br>
          <strong>Term:</strong> Jan 2024 – May 2025
        </div>
        <p class="research-desc" style="margin-top: 0;">Developing and optimizing experimental submillimeter spectrometers... </p>
        <div style="display: block; margin-top: 8px; color: #733BEB; font-weight: bold; font-size: 0.9em;">Read more →</div>
      </div>
    </div>
  </a>

</div>

{::options parse_block_html="true" /}
