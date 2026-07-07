---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About Me

I am pursuing a B.A. in Physics in the College of Arts and Sciences at Cornell University, and am looking to start a PhD in Astrophysics after I graduate in May 2027. 

I currently conduct numerical relativity research under the mentorship of Prof. Nils Deppe, as a part of the Simulating eXtreme Spacetimes (SXS) Collaboration. I also have experience with historical observational astronomy through my Summer 2025 internship at Yerkes Observatory, where I worked with Dr. Amanda Bauer to conduct a longitudinal growth study of the Dumbbell Nebula. In the summer of 2024, I was granted a Nexus Scholars research position to work with Prof. Abigail Crites on instrumentation for TIME, an observational cosmology experiment. 

While I am not in class or at the lab, you can find me with the Cornell Society of Physics Students as their President, or singing with Hearsay A Cappella as their Assistant Music Director and Choreography Chair.

<div class="section-card">
<div class="pi-card">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ site.photo }}" class="pi-photo" alt="{{ site.name }}" loading="lazy">
<div>
<h3 class="pi-name">{{ site.name }}</h3>
<p style="font-style: italic; color: var(--text-secondary);">{{ site.title }}, {{ site.institution }}</p>
<div class="pi-links">
{% if site.email %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email"><i class="fa-solid fa-envelope"></i></a>{% endif %}
{% if site.links.cv and site.links.cv != "" %}<a href="{{ site.url }}{{ site.baseurl }}/{{ site.links.cv }}" class="icon-link" title="CV"><i class="ai ai-cv"></i></a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
</div>
</div>
</div>
</div>

{% if site.data.awards %}
<div class="section-card">
<h3>Recent Awards & Fellowships</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
{% endif %}
