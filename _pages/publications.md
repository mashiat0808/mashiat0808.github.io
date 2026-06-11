---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% if author.googlescholar %}
  <p class="publication-intro">Find my articles on <a href="{{ author.googlescholar }}" class="btn btn--info" target="_blank" rel="noopener">Google Scholar <i class="fas fa-graduation-cap"></i></a></p>
{% endif %}

<h2 class="publication-status-label publication-status-label--accepted">Accepted</h2>

{% assign accepted_pubs = site.publications | where: "status", "accepted" | sort: "date" | reverse %}
{% for post in accepted_pubs %}
  {% include archive-single.html %}
{% endfor %}

<h2 class="publication-status-label publication-status-label--published">Published</h2>

{% assign published_pubs = site.publications | where: "status", "published" | sort: "date" | reverse %}
{% for post in published_pubs %}
  {% include archive-single.html %}
{% endfor %}

<h2 class="publication-status-label publication-status-label--under-review">Under Review</h2>

{% assign review_pubs = site.publications | where: "status", "under-review" | sort: "date" | reverse %}
{% for post in review_pubs %}
  {% include archive-single.html %}
{% endfor %}
