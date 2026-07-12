---
layout: gridlay
title: "Publications"
permalink: /publications/
---

## Senior Thesis Proposal

**Title:** *Examining Tidal Deformability of Neutron Stars by Simulating Inspiral Degeneracy of Differing Internal Structures*

**Advisor:** Prof. Nils Deppe

I am looking to use the SpECTRE code base to compare simulated solutions of neutron stars that exhibit a degenerate tidal deformability factor, but different internal equations of state. I hope to explore this question of how internal microphysics can influence the observable macrophysics of a binary neutron star system to determine whether there are any observable differences that would be visible at the resolution of future gravitational wave observatories currently planned.

---

## Conference & Seminar Presentations

*Selected oral talks and poster presentations given at symposia and national meetings.*

{% bibliography %}

<style>
  /* Fix layout card wrappers for bibliography items */
  .bibliography li {
    background-color: var(--global-card-bg, #1e1e1e) !important;
    border: 1px solid var(--global-border-color, rgba(255, 255, 255, 0.1)) !important;
    padding: 24px !important;
    border-radius: 8px !important;
    margin-bottom: 20px !important;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: all 0.2s ease-in-out;
  }

  /* Target text tokens strictly to ensure clear readability against the theme background */
  .bibliography li,
  .bibliography li .title,
  .bibliography li .author,
  .bibliography li .periodical,
  .bibliography li span:not(.badge) {
    color: var(--global-text-color, #f5f5f5) !important;
  }

  /* Keep core structural labels distinct */
  .bibliography li abbr {
    color: var(--global-theme-color, #733BEB) !important;
    font-weight: bold;
  }

  /* Retain correct contrast configurations for your custom purple buttons and badges */
  .bibliography li a.btn,
  .bibliography li .btn,
  .bibliography li span.badge {
    color: #ffffff !important;
  }
</style>
