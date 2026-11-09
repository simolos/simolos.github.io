---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

# Education

August 2023 - Present <br>
**École polytechnique fédérale de Lausanne (Switzerland)** <br>
PhD candidate in Neuroscience

<br>

March 2020 - July 2023 <br>
**Polytechnic University of Turin (Italy)** <br>
Master degree: Biomedical Engineering - Biomedical Instrumentation

- Biomedical signal and image processing, neuroengineering, artificial intelligence - Machine Learning and Deep Learning
- Biomedical devices, electrical measurements
- 3D digitalization and modelling systems

***Master thesis project***
Hosted by the Laboratory for Soft Bioelectronic Interfaces (LSBI) at EPFL, supervised by Prof. Stéphanie Lacour.
My project aimed at characterizing and modulating spreading depolarizations (SDs), propagating waves of brain tissue depolarization, triggered by the accumulation of intracellular potassium. SDs occurring after traumatic brain injury (TBI) have been shown to be responsible for worse neurological outcomes.

- Design of experimental protocols
- In-vivo work - SDs induced by KCl application in rats
- Intracortical recordings and closed-loop electrical stimulation using soft neural interfaces
- Data analysis

<br>

Sept 2016 - March 2020 <br>
**Polytechnic University of Turin** <br>
Bachelor's degree: Biomedical Engineering


# Publications

<ul>
{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}
</ul>