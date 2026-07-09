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
    
    <!-- The details tag serves as the dropdown wrapper -->
    <details id="{{ skill | slugify }}" style="background: #fff; border: 1px solid #e1e1e1; border-radius: 8px; margin-bottom: 12px; padding: 0; overflow: hidden; box-shadow: 0 2px 5px rgba(0,0,0,0.01); transition: border-color 0.2s ease;">
      
      <!-- The summary tag is the visible header you click on -->
      <summary style="padding: 16px 20px; font-size: 1.1em; font-weight: 600; color: #333; cursor: pointer; display: flex; justify-content: space-between; align-items: center; list-style: none; outline: none; user-select: none;">
        <span style="display: inline-flex; align-items: center; gap: 8px;">
          <span style="color: #733BEB; font-size: 0.8em; transform: rotate(0deg); transition: transform 0.2s ease;">▶</span>
          {{ skill }}
        </span>
        <span style="font-size: 0.85em; color: #888; background: #f5f5f5; padding: 2px 10px; border-radius: 12px; font-weight: 500;">
          {{ count }} {% if count == 1 %}role{% else %}roles{% endif %}
        </span>
      </summary>

      <!-- The hidden dropdown content containing the matched cards -->
      <div style="padding: 0 20px 20px 20px; background: #fafafa; border-top: 1px solid #f0f0f0; display: grid; gap: 10px;">
        <p style="font-size: 0.85em; color: #666; margin-top: 15px; margin-bottom: 5px;">Demonstrated in the following positions:</p>
        
        {% for exp in site.data.experiences %}
          {% if exp.skills contains skill %}
            <div style="background: #fff; border: 1px solid #e5e5e5; border-radius: 6px; padding: 12px 16px; display: flex; justify-content: space-between; align-items: center; box-shadow: 0 1px 3px rgba(0,0,0,0.02);">
              <div>
                <strong style="color: #111; font-size: 0.95em;">{{ exp.title }}</strong>
                <span style="font-size: 0.75em; margin-left: 10px; padding: 2px 6px; background: #eee; border-radius: 4px; text-transform: uppercase; color: #555; font-weight: 600;">{{ exp.type }}</span>
              </div>
              <a href="{{ site.url }}{{ site.baseurl }}/{{ exp.type }}/#{{ exp.id }}" style="color: #733BEB; text-decoration: none; font-size: 0.85em; font-weight: 600; white-space: nowrap;">View Card →</a>
            </div>
          {% endif %}
        {% endfor %}
      </div>

    </details>
  {% endfor %}

</div>

<!-- Small inline CSS snippet to hide default browser dropdown arrows and handle smooth rotations -->
<style>
  details summary::-webkit-details-marker {
    display: none;
  }
  details[open] summary span span {
    transform: rotate(90deg) !important;
  }
  details:hover {
    border-color: #c9bcf2;
  }
</style>

{::options parse_block_html="true" /}
