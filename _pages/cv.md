---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
custom_css:
  - cv.css
redirect_from:
  - /resume
---

{% include base_path %}

<p class="cv-download">
  <a href="{{ '/files/cv.pdf' | absolute_url }}?v={{ site.time | date: '%s' }}" class="btn btn--primary">Download CV (PDF)</a>
</p>

<embed src="{{ '/files/cv.pdf' | absolute_url }}?v={{ site.time | date: '%s' }}" class="cv-embed" type="application/pdf">
