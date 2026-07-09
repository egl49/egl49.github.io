---
title: "Skills & Competencies"
layout: page
permalink: /skills/
---

## Skills & Competencies

---

{::options parse_block_html="false" /}

<!-- Optional update for top of _pages/skills.md to maintain the ranking layout -->
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
endfor %}

{% assign sorted_skills = skill_counts | sort | reverse %}

<div class="skills-timeline" style="margin-top: 30px;">
  {% for entry in sorted_skills %}
    {% assign parts = entry | split: "::" %}
    {% assign count = parts[0] | plus: 0 %}
    {% assign skill = parts[1] %}
    
    <div id="{{ skill | slugify }}" style="margin-bottom: 40px; border-left: 3px solid #733BEB; padding-left: 20px;">
       <!-- Rest of your original timeline code layout stays exactly the same -->
       
      <h3 style="margin-top: 0; color: #333; font-weight: 700;">{{ skill }}</h3>
      <p style="font-size: 0.9em; color: #666; margin-bottom: 15px;">Referenced in the following roles:</p>
      
      <div style="display: grid; gap: 10px;">
        {% for exp in site.data.experiences %}
          {% if exp.skills contains skill %}
            <div style="background: #f9f9f9; border: 1px solid #e1e1e1; border-radius: 6px; padding: 12px 18px; display: flex; justify-content: space-between; align-items: center;">
              <div>
                <strong style="color: #111;">{{ exp.title }}</strong>
                <span style="font-size: 0.8em; margin-left: 10px; padding: 2px 6px; background: #eee; border-radius: 4px; text-transform: uppercase; color: #555;">{{ exp.type }}</span>
              </div>
              <a href="{{ site.url }}{{ site.baseurl }}/{{ exp.type }}/#{{ exp.id }}" style="color: #733BEB; text-decoration: none; font-size: 0.9em; font-weight: 500;">View Card →</a>
            </div>
          {% endif %}
        {% endfor %}
      </div>

    </div>
  {% endfor %}

</div>

{::options parse_block_html="true" /}
