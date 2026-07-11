---
title: "Teaching"
layout: gridlay
sitemap: false
permalink: /teaching/
---

## Teaching

{::options parse_block_html="false" /}

<div class="research-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: 24px; margin-top: 20px;">
  {% for exp in site.data.experiences %}
    {% if exp.type == "teaching" %}
      
      <a href="{{ site.url }}{{ site.baseurl }}/teaching/{% if exp.id == 'peer-mentor' %}mentorship{% else %}{{ exp.id }}{% endif %}/" id="{{ exp.id }}" style="text-decoration: none; color: inherit; display: flex; flex-direction: column;">
        
        <div class="research-card" style="cursor: pointer; background: #fff; border: 1px solid #e1e1e1; border-radius: 12px; overflow: hidden; display: flex; flex-direction: column; height: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.01); transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;" onmouseover="this.style.transform='scale(1.015)'; this.style.boxShadow='0 6px 16px rgba(0,0,0,0.04)';" onmouseout="this.style.transform='scale(1)'; this.style.boxShadow='0 4px 12px rgba(0,0,0,0.01)';">
          
          {% if exp.image and exp.image != "" %}
            <div class="card-image-wrapper" style="width: 100%; height: 160px; overflow: hidden; border-bottom: 1px solid #e1e1e1; background: #fafafa;">
              <img src="{{ site.url }}{{ site.baseurl }}/images/teaching/{{ exp.image }}" alt="{{ exp.title }}" style="width: 100%; height: 100%; object-fit: cover;">
            </div>
          {% endif %}

          <div class="research-body" style="padding: 24px; flex: 1; display: flex; flex-direction: column; justify-content: space-between;">
            <div>
              <h4 class="research-title" style="margin-top: 0; margin-bottom: 8px; font-size: 1.2em; font-weight: 700; line-height: 1.4; color: #111;">
                {{ exp.title }}
              </h4>
              
              <div class="research-subtitles" style="font-size: 0.85em; color: #666; margin-bottom: 12px; line-height: 1.5;">
                {% if exp.organization and exp.organization != "" %}<strong>Institution:</strong> {{ exp.organization }}<br>{% endif %}
                {% if exp.supervisor and exp.supervisor != "" %}<strong>Supervisor:</strong> {{ exp.supervisor }}<br>{% endif %}
                {% if exp.term and exp.term != "" %}<strong>Term:</strong> {{ exp.term }}{% endif %}
              </div>

              <p class="research-desc" style="font-size: 0.92em; color: #444; line-height: 1.6; margin-top: 0; margin-bottom: 16px;">
                {{ exp.description }}
              </p>
            </div>

            {% if exp.skills and exp.skills.size > 0 %}
              <div style="margin-top: auto; padding-top: 12px; border-top: 1px solid #f5f5f5;">
                <details style="width: 100%;" onclick="event.stopPropagation();">
                  <summary style="font-size: 0.82em; color: #733BEB; font-weight: 600; cursor: pointer; display: flex; align-items: center; gap: 4px; outline: none; user-select: none;">
                    <span>View Technical Stack</span>
                  </summary>
                  <div class="skill-badges" style="margin-top: 10px; display: flex; flex-wrap: wrap; gap: 6px;">
                    {% for skill in exp.skills %}
                      <span style="display: inline-block; background: rgba(115, 59, 235, 0.06); color: #733BEB; font-size: 0.75em; padding: 4px 10px; border-radius: 12px; font-weight: 600; letter-spacing: 0.2px; white-space: nowrap;">
                        {{ skill }}
                      </span>
                    {% endfor %}
                  </div>
                </details>
              </div>
            {% endif %}

            <div style="display: block; margin-top: 14px; color: #733BEB; font-weight: bold; font-size: 0.9em; text-decoration: none;">Read more →</div>

          </div>
        </div>

      </a>

    {% endif %}
  {% endfor %}
</div>

<style>
  details summary::-webkit-details-marker { display: none; }
  details summary { list-style: none; }
</style>

{::options parse_block_html="true" /}---
title: "Teaching"
layout: gridlay
sitemap: false
permalink: /teaching/
---

## Teaching

{::options parse_block_html="false" /}

<div class="research-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: 24px; margin-top: 20px;">
  {% for exp in site.data.experiences %}
    {% if exp.type == "teaching" %}
      
      <a href="{{ site.url }}{{ site.baseurl }}/teaching/{% if exp.id == 'peer-mentor' %}mentorship{% else %}{{ exp.id }}{% endif %}/" id="{{ exp.id }}" style="text-decoration: none; color: inherit; display: flex; flex-direction: column;">
        
        <div class="research-card" style="cursor: pointer; background: #fff; border: 1px solid #e1e1e1; border-radius: 12px; overflow: hidden; display: flex; flex-direction: column; height: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.01); transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;" onmouseover="this.style.transform='scale(1.015)'; this.style.boxShadow='0 6px 16px rgba(0,0,0,0.04)';" onmouseout="this.style.transform='scale(1)'; this.style.boxShadow='0 4px 12px rgba(0,0,0,0.01)';">
          
          {% if exp.image and exp.image != "" %}
            <div class="card-image-wrapper" style="width: 100%; height: 160px; overflow: hidden; border-bottom: 1px solid #e1e1e1; background: #fafafa;">
              <img src="{{ site.url }}{{ site.baseurl }}/images/teaching/{{ exp.image }}" alt="{{ exp.title }}" style="width: 100%; height: 100%; object-fit: cover;">
            </div>
          {% endif %}

          <div class="research-body" style="padding: 24px; flex: 1; display: flex; flex-direction: column; justify-content: space-between;">
            <div>
              <h4 class="research-title" style="margin-top: 0; margin-bottom: 8px; font-size: 1.2em; font-weight: 700; line-height: 1.4; color: #111;">
                {{ exp.title }}
              </h4>
              
              <div class="research-subtitles" style="font-size: 0.85em; color: #666; margin-bottom: 12px; line-height: 1.5;">
                {% if exp.organization and exp.organization != "" %}<strong>Institution:</strong> {{ exp.organization }}<br>{% endif %}
                {% if exp.supervisor and exp.supervisor != "" %}<strong>Supervisor:</strong> {{ exp.supervisor }}<br>{% endif %}
                {% if exp.term and exp.term != "" %}<strong>Term:</strong> {{ exp.term }}{% endif %}
              </div>

              <p class="research-desc" style="font-size: 0.92em; color: #444; line-height: 1.6; margin-top: 0; margin-bottom: 16px;">
                {{ exp.description }}
              </p>
            </div>

            {% if exp.skills and exp.skills.size > 0 %}
              <div style="margin-top: auto; padding-top: 12px; border-top: 1px solid #f5f5f5;">
                <details style="width: 100%;" onclick="event.stopPropagation();">
                  <summary style="font-size: 0.82em; color: #733BEB; font-weight: 600; cursor: pointer; display: flex; align-items: center; gap: 4px; outline: none; user-select: none;">
                    <span>View Technical Stack</span>
                  </summary>
                  <div class="skill-badges" style="margin-top: 10px; display: flex; flex-wrap: wrap; gap: 6px;">
                    {% for skill in exp.skills %}
                      <span style="display: inline-block; background: rgba(115, 59, 235, 0.06); color: #733BEB; font-size: 0.75em; padding: 4px 10px; border-radius: 12px; font-weight: 600; letter-spacing: 0.2px; white-space: nowrap;">
                        {{ skill }}
                      </span>
                    {% endfor %}
                  </div>
                </details>
              </div>
            {% endif %}

            <div style="display: block; margin-top: 14px; color: #733BEB; font-weight: bold; font-size: 0.9em; text-decoration: none;">Read more →</div>

          </div>
        </div>

      </a>

    {% endif %}
  {% endfor %}
</div>

<style>
  details summary::-webkit-details-marker { display: none; }
  details summary { list-style: none; }
</style>

{::options parse_block_html="true" /}---
title: "Teaching"
layout: gridlay
sitemap: false
permalink: /teaching/
---

## Teaching

{::options parse_block_html="false" /}

<div class="research-grid">

  <!-- 1. ULA ROLE (CLICKABLE) -->
  <a href="{{ site.url }}{{ site.baseurl }}/teaching/ula/" style="text-decoration: none; color: inherit; display: block; margin-bottom: 20px;">
    <div class="research-card" style="cursor: pointer; display: flex; transition: transform 0.2s ease-in-out; background: #fff; border: 1px solid #e1e1e1; border-radius: 8px; padding: 15px;" onmouseover="this.style.transform='scale(1.01)'" onmouseout="this.style.transform='scale(1)'">
      <img src="{{ site.url }}{{ site.baseurl }}/images/teaching/physics.svg" class="research-thumb" alt="Physics classroom icon" style="width: 100px; height: 100px; object-fit: cover; margin-right: 20px;">
      <div class="research-body" style="flex: 1;">
        <h4 class="research-title" style="margin-top: 0; margin-bottom: 4px;">Physics Undergraduate Learning Assistant (ULA)</h4>
        <div class="research-subtitles" style="font-size: 0.82em; color: #666; margin-bottom: 8px; line-height: 1.4;">
          <strong>Institution:</strong> Cornell University <br>
          <strong>Supervisor:</strong> Physics Department Faculty <br>
          <strong>Term:</strong> Academic Year Role
        </div>
        <p class="research-desc" style="margin-top: 0; margin-bottom: 0;">
          Facilitated student learning and collaborative problem-solving in undergraduate physics courses at Cornell. Led active-learning recitations, held office hours to clarify core conceptual frameworks, and supported peers in mastering foundational mathematical and physical tools.
        </p>
        <div style="display: block; margin-top: 8px; color: #733BEB; font-weight: bold; font-size: 0.9em;">Read more →</div>
      </div>
    </div>
  </a>

  <!-- 2. MENTORSHIP ROLE (CLICKABLE) -->
  <a href="{{ site.url }}{{ site.baseurl }}/teaching/mentorship/" style="text-decoration: none; color: inherit; display: block; margin-bottom: 20px;">
    <div class="research-card" style="cursor: pointer; display: flex; transition: transform 0.2s ease-in-out; background: #fff; border: 1px solid #e1e1e1; border-radius: 8px; padding: 15px;" onmouseover="this.style.transform='scale(1.01)'" onmouseout="this.style.transform='scale(1)'">
      <img src="{{ site.url }}{{ site.baseurl }}/images/teaching/peer-led.svg" class="research-thumb" alt="Mentorship icon" style="width: 100px; height: 100px; object-fit: cover; margin-right: 20px;">
      <div class="research-body" style="flex: 1;">
        <h4 class="research-title" style="margin-top: 0; margin-bottom: 4px;">Peer Mentorship & Academic Support</h4>
        <div class="research-subtitles" style="font-size: 0.82em; color: #666; margin-bottom: 8px; line-height: 1.4;">
          <strong>Institution:</strong> Cornell University <br>
          <strong>Supervisor:</strong> Society of Physics Students <br>
          <strong>Term:</strong> Continuous
        </div>
        <p class="research-desc" style="margin-top: 0; margin-bottom: 0;">
          Provided guidance on course selection, lab workflows, and technical skill development (such as Python and LaTeX) for underclassmen in the department, helping foster an inclusive and accessible environment for incoming physics and astronomy students.
        </p>
        <div style="display: block; margin-top: 8px; color: #733BEB; font-weight: bold; font-size: 0.9em;">Read more →</div>
      </div>
    </div>
  </a>

</div>

{::options parse_block_html="true" /}
