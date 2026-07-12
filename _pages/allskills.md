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
    
    <details id="{{ skill | slugify }}" class="skill-details-wrapper" style="border: 1px solid var(--global-border-color, #e1e1e1); border-radius: 8px; margin-bottom: 12px; padding: 0; overflow: hidden; transition: border-color 0.2s ease;">
      
      <summary style="padding: 16px 20px; font-size: 1.1em; font-weight: 600; color: inherit; cursor: pointer; display: flex; justify-content: space-between; align-items: center; list-style: none; outline: none; user-select: none;">
        <span style="display: inline-flex; align-items: center; gap: 8px;">
          <span style="color: #733BEB; font-size: 0.8em; transform: rotate(0deg); transition: transform 0.2s ease;">▶</span>
          {{ skill }}
        </span>
        <span class="skill-count-badge" style="font-size: 0.85em; padding: 2px 10px; border-radius: 12px; font-weight: 500;">
          {{ count }} {% if count == 1 %}role{% else %}roles{% endif %}
        </span>
      </summary>

      <div class="skill-dropdown-body" style="padding: 0 20px 20px 20px; border-top: 1px solid var(--global-border-color, #f0f0f0); display: grid; gap: 10px;">
        <p style="font-size: 0.85em; opacity: 0.8; margin-top: 15px; margin-bottom: 5px;">Demonstrated in the following positions:</p>
        
        {% for exp in site.data.experiences %}
          {% if exp.skills contains skill %}
            <div class="skill-position-row" style="border: 1px solid var(--global-border-color, #e5e5e5); border-radius: 6px; padding: 12px 16px; display: flex; justify-content: space-between; align-items: center;">
              <div style="display: flex; align-items: center; gap: 10px; flex-wrap: wrap;">
                <span style="font-size: 0.95em;">
                  <strong style="color: inherit;">{{ exp.title }}</strong>
                  {% if exp.organization and exp.organization != "" %}
                    <span style="opacity: 0.7; font-weight: 400;"> — {{ exp.organization }}</span>
                  {% endif %}
                </span>
                <span class="skill-type-tag" style="font-size: 0.75em; padding: 2px 6px; border-radius: 4px; text-transform: uppercase; font-weight: 600;">{{ exp.type }}</span>
              </div>
              
              {% if exp.type == "miscellaneous" %}
                <span style="opacity: 0.5; font-size: 0.85em; font-style: italic;">General Stack</span>
              {% else %}
                <a href="{{ site.url }}{{ site.baseurl }}/{{ exp.type }}/#{{ exp.id }}" style="color: #733BEB; text-decoration: none; font-size: 0.85em; font-weight: 600; white-space: nowrap;">View Card →</a>
              {% endif %}
            </div>
          {% endif %}
        {% endfor %}
      </div>

    </details>
  {% endfor %}

</div>

<style>
  details summary::-webkit-details-marker {
    display: none;
  }
  details[open] summary span span {
    transform: rotate(90deg) !important;
  }
  
  /* Light theme baseline defaults */
  .skill-details-wrapper { background: #fff; }
  .skill-count-badge { background: #f5f5f5; color: #888; }
  .skill-dropdown-body { background: #fafafa; }
  .skill-position-row { background: #fff; box-shadow: 0 1px 3px rgba(0,0,0,0.02); }
  .skill-type-tag { background: #eee; color: #555; }
  details:hover { border-color: #c9bcf2; }

  /* Dark theme overrides using your framework attributes */
  html[data-theme='dark'] .skill-details-wrapper { background: #1e1e1f; }
  html[data-theme='dark'] .skill-count-badge { background: #2e2e30; color: #bbb; }
  html[data-theme='dark'] .skill-dropdown-body { background: #171718; }
  html[data-theme='dark'] .skill-position-row { background: #222224; }
  html[data-theme='dark'] .skill-type-tag { background: #333; color: #ccc; }
  html[data-theme='dark'] details:hover { border-color: #733BEB; }
</style>

{::options parse_block_html="true" /}
