---
title: "Leadership & Outreach"
layout: gridlay
sitemap: false
permalink: /leadership/
---

## Leadership & Outreach

{::options parse_block_html="false" /}

<h3 style="margin-top: 30px; margin-bottom: 20px;">Current Roles</h3>

<div class="research-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: 24px; margin-top: 20px;">
  {% for exp in site.data.experiences %}
    {% if exp.type == "leadership" and exp.current == true %}
      
      {% if exp.has_page == true %}
        <a href="{{ site.url }}{{ site.baseurl }}/leadership/{% if exp.id == 'hearsay-acappella-choreo' %}choreo{% elsif exp.id == 'hearsay-acappella-amd' %}amd{% elsif exp.id == 'hearsay-acappella-alumni' %}alumni-chair{% elsif exp.id == 'alumni-interviewer' %}api-interviewer{% else %}{{ exp.id }}{% endif %}/" id="{{ exp.id }}" style="text-decoration: none; color: inherit; display: flex; flex-direction: column;">
      {% else %}
        <div id="{{ exp.id }}" style="display: flex; flex-direction: column;">
      {% endif %}
        
        <div class="section-card" style="{% if exp.has_page == true %}cursor: pointer;{% else %}cursor: default;{% endif %} overflow: hidden; display: flex; flex-direction: column; height: 100%; padding: 0; box-shadow: none; transition: transform 0.2s ease-in-out;" {% if exp.has_page == true %}onmouseover="this.style.transform='scale(1.015)';" onmouseout="this.style.transform='scale(1)';" {% endif %}>
          
          {% if exp.image and exp.image != "" %}
            <div class="card-image-wrapper" style="width: 100%; height: 160px; overflow: hidden; border-bottom: 1px solid var(--global-border-color); background: rgba(0,0,0,0.05);">
              <img src="{{ site.url }}{{ site.baseurl }}/images/leadership/{{ exp.image }}" alt="{{ exp.title }}" style="width: 100%; height: 100%; object-fit: cover;">
            </div>
          {% endif %}

          <div class="research-body" style="padding: 24px; flex: 1; display: flex; flex-direction: column; justify-content: space-between;">
            <div>
              <h4 class="research-title" style="margin-top: 0; margin-bottom: 8px; font-size: 1.2em; font-weight: 700; line-height: 1.4; color: var(--global-text-color);">
                {{ exp.title }}
              </h4>
              
              <div class="research-subtitles" style="font-size: 0.85em; color: var(--text-secondary, inherit); opacity: 0.8; margin-bottom: 12px; line-height: 1.5;">
                {% if exp.organization and exp.organization != "" %}<strong>Organization:</strong> {{ exp.organization }}<br>{% endif %}
                {% if exp.term and exp.term != "" %}<strong>Term:</strong> {{ exp.term }}{% endif %}
              </div>

              <p class="research-desc" style="font-size: 0.92em; color: var(--global-text-color); opacity: 0.9; line-height: 1.6; margin-top: 0; margin-bottom: 16px;">
                {{ exp.description }}
              </p>
            </div>

            {% if exp.skills and exp.skills.size > 0 %}
              <div style="margin-top: auto; padding-top: 12px; border-top: 1px solid var(--global-border-color);">
                <details style="width: 100%;" onclick="event.stopPropagation();">
                  <summary style="font-size: 0.82em; color: #733BEB; font-weight: 600; cursor: pointer; display: flex; align-items: center; gap: 4px; outline: none; user-select: none;">
                    <span>View Technical Stack</span>
                  </summary>
                  <div class="skill-badges" style="margin-top: 10px; display: flex; flex-wrap: wrap; gap: 6px;">
                    {% for skill in exp.skills %}
                      <span style="display: inline-block; background: var(--global-divider-color, rgba(115, 59, 235, 0.15)); color: #733BEB; font-size: 0.75em; padding: 4px 10px; border-radius: 12px; font-weight: 600; letter-spacing: 0.2px; white-space: nowrap;">
                        {{ skill }}
                      </span>
                    {% endfor %}
                  </div>
                </details>
              </div>
            {% endif %}

            {% if exp.has_page == true %}
              <div style="display: block; margin-top: 14px; color: #733BEB; font-weight: bold; font-size: 0.9em; text-decoration: none;">Read more →</div>
            {% endif %}

          </div>
        </div>

      {% if exp.has_page == true %}
        </a>
      {% else %}
        </div>
      {% endif %}

    {% endif %}
  {% endfor %}
</div>

<h3 style="margin-top: 50px; margin-bottom: 20px;">Previous Experience</h3>

<div class="research-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: 24px; margin-top: 20px;">
  {% for exp in site.data.experiences %}
    {% if exp.type == "leadership" and exp.current == false %}
      
      {% if exp.has_page == true %}
        <a href="{{ site.url }}{{ site.baseurl }}/leadership/{% if exp.id == 'hearsay-acappella-social' %}social-chair{% else %}{{ exp.id }}{% endif %}/" id="{{ exp.id }}" style="text-decoration: none; color: inherit; display: flex; flex-direction: column;">
      {% else %}
        <div id="{{ exp.id }}" style="display: flex; flex-direction: column;">
      {% endif %}
        
        <div class="section-card" style="{% if exp.has_page == true %}cursor: pointer;{% else %}cursor: default;{% endif %} border-style: dashed !important; border-color: #733BEB !important; border-width: 2px !important; overflow: hidden; display: flex; flex-direction: column; height: 100%; padding: 0; box-shadow: none; transition: transform 0.2s ease-in-out;" {% if exp.has_page == true %}onmouseover="this.style.transform='scale(1.015)';" onmouseout="this.style.transform='scale(1)';" {% endif %}>
          
          {% if exp.image and exp.image != "" %}
            <div class="card-image-wrapper" style="width: 100%; height: 160px; overflow: hidden; border-bottom: 2px dashed #733BEB; background: rgba(0,0,0,0.05);">
              <img src="{{ site.url }}{{ site.baseurl }}/images/leadership/{{ exp.image }}" alt="{{ exp.title }}" style="width: 100%; height: 100%; object-fit: cover;">
            </div>
          {% endif %}

          <div class="research-body" style="padding: 24px; flex: 1; display: flex; flex-direction: column; justify-content: space-between;">
            <div>
              <h4 class="research-title" style="margin-top: 0; margin-bottom: 8px; font-size: 1.2em; font-weight: 700; line-height: 1.4; color: var(--global-text-color);">
                {{ exp.title }}
              </h4>
              
              <div class="research-subtitles" style="font-size: 0.85em; color: var(--text-secondary, inherit); opacity: 0.8; margin-bottom: 12px; line-height: 1.5;">
                {% if exp.organization and exp.organization != "" %}<strong>Organization:</strong> {{ exp.organization }}<br>{% endif %}
                {% if exp.term and exp.term != "" %}<strong>Term:</strong> {{ exp.term }}{% endif %}
              </div>

              <p class="research-desc" style="font-size: 0.92em; color: var(--global-text-color); opacity: 0.9; line-height: 1.6; margin-top: 0; margin-bottom: 16px;">
                {{ exp.description }}
              </p>
            </div>

            {% if exp.skills and exp.skills.size > 0 %}
              <div style="margin-top: auto; padding-top: 12px; border-top: 2px dashed #733BEB;">
                <details style="width: 100%;" onclick="event.stopPropagation();">
                  <summary style="font-size: 0.82em; color: #733BEB; font-weight: 600; cursor: pointer; display: flex; align-items: center; gap: 4px; outline: none; user-select: none;">
                    <span>View Technical Stack</span>
                  </summary>
                  <div class="skill-badges" style="margin-top: 10px; display: flex; flex-wrap: wrap; gap: 6px;">
                    {% for skill in exp.skills %}
                      <span style="display: inline-block; background: var(--global-divider-color, rgba(115, 59, 235, 0.15)); color: #733BEB; font-size: 0.75em; padding: 4px 10px; border-radius: 12px; font-weight: 600; letter-spacing: 0.2px; white-space: nowrap;">
                        {{ skill }}
                      </span>
                    {% endfor %}
                  </div>
                </details>
              </div>
            {% endif %}

            {% if exp.has_page == true %}
              <div style="display: block; margin-top: 14px; color: #733BEB; font-weight: bold; font-size: 0.9em; text-decoration: none;">Read more →</div>
            {% endif %}

          </div>
        </div>

      {% if exp.has_page == true %}
        </a>
      {% else %}
        </div>
      {% endif %}

    {% endif %}
  {% endfor %}
</div>

<style>
  details summary::-webkit-details-marker { display: none; }
  details summary { list-style: none; }
  .section-card:hover { border-color: #733BEB !important; }
</style>

{::options parse_block_html="true" /}
