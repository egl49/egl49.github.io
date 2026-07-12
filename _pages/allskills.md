---
title: "Skills & Competencies"
layout: page
permalink: /allskills/
---
---

{::options parse_block_html="false" /}

{% assign all_skills = "" | split: "," %}
{% for exp in site.data.experiences %}
  {% for skill in exp.skills %}
    {% assign all_skills = all_skills | push: skill %}
  {% endfor %}
{% endfor %}
{% assign unique_skills = all_skills | uniq %}

{% assign skill_counts = "" | split: "," %}
{% for skill in unique_skills %}
  {% assign count = 0 %}
  {% for s in all_skills %}
    {% if s == skill %}{% assign count = count | plus: 1 %}{% endif %}
  {% endfor %}
  {% if count < 10 %}{% assign prefix = "0" | append: count %}{% else %}{% assign prefix = count %}{% endif %}
  {% assign entry = prefix | append: "::" | append: skill %}
  {% assign skill_counts = skill_counts | push: entry %}
{% endfor %}

{% assign sorted_skills = skill_counts | sort | reverse %}

<div class="skills-accordion-container" style="margin-top: 30px;">
  
  {% for entry in sorted_skills %}
    {% assign parts = entry | split: "::" %}
    {% assign count = parts[0] | plus: 0 %}
    {% assign skill = parts[1] %}
    
    <!-- Using section-card to cleanly match your site's native container structure -->
    <div class="section-card" style="margin-bottom: 20px; padding: 0; overflow: hidden;">
      <details id="{{ skill | slugify }}" class="skill-details-wrapper" style="background: transparent; color: var(--global-text-color);">
        
        <summary class="skill-summary-header" style="padding: 18px 24px; font-size: 1.1em; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; list-style: none; outline: none; user-select: none;">
          <span style="display: inline-flex; align-items: center; gap: 10px;">
            <span style="color: #733BEB; font-size: 0.8em; transform: rotate(0deg); transition: transform 0.2s ease;">▶</span>
            {{ skill }}
          </span>
          <span class="skill-count-badge" style="font-size: 0.85em; padding: 4px 12px; border-radius: 20px; font-weight: 500; background-color: var(--global-divider-color, rgba(255,255,255,0.05)); color: var(--text-secondary, inherit);">
            {{ count }} {% if count == 1 %}role{% else %}roles{% endif %}
          </span>
        </summary>

        <div class="skill-dropdown-body" style="padding: 20px 24px 24px 24px; border-top: 1px solid var(--global-border-color); display: grid; gap: 12px; background-color: rgba(0, 0, 0, 0.15);">
          <p style="font-size: 0.85em; margin: 0 0 5px 0; color: var(--text-secondary, inherit); opacity: 0.8;">Demonstrated in the following positions:</p>
          
          {% for exp in site.data.experiences %}
            {% if exp.skills contains skill %}
              <!-- Nested row utilizing the theme border config -->
              <div class="skill-position-row" style="border: 1px solid var(--global-border-color); border-radius: 8px; padding: 14px 18px; display: flex; justify-content: space-between; align-items: center; background-color: rgba(255, 255, 255, 0.02);">
                <div style="display: flex; align-items: center; gap: 10px; flex-wrap: wrap;">
                  <span style="font-size: 0.95em;">
                    <strong style="color: var(--global-text-color);">{{ exp.title }}</strong>
                    {% if exp.organization and exp.organization != "" %}
                      <span style="opacity: 0.8; font-weight: 400;"> — {{ exp.organization }}</span>
                    {% endif %}
                  </span>
                  <span class="skill-type-tag" style="font-size: 0.75em; padding: 2px 8px; border-radius: 4px; text-transform: uppercase; font-weight: 600; background-color: var(--global-divider-color, rgba(255,255,255,0.08)); color: var(--global-text-color);">{{ exp.type }}</span>
                </div>
                
                {% if exp.type == "miscellaneous" %}
                  <span style="opacity: 0.6; font-size: 0.85em; font-style: italic;">General Stack</span>
                {% else %}
                  <a href="{{ site.url }}{{ site.baseurl }}/{{ exp.type }}/#{{ exp.id }}" style="color: #733BEB; text-decoration: none; font-size: 0.85em; font-weight: 600; white-space: nowrap;">View Card →</a>
                {% endif %}
              </div>
            {% endif %}
          {% endfor %}
        </div>

      </details>
    </div>
  {% endfor %}

</div>

<style>
  details summary::-webkit-details-marker { display: none; }
  details[open] summary span span { transform: rotate(90deg) !important; }
  .section-card:hover { border-color: #733BEB !important; }
</style>

{::options parse_block_html="true" /}
