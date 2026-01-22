---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<span style="display: inline-block; padding: 0.25em 0.75em; margin: 1em 0 0.5em 0; background-color: #4CAF50; color: white; border-radius: 3px; font-size: 0.85em; font-weight: 600; text-transform: uppercase;">Accepted</span>

{% assign accepted_pubs = site.publications | where: "status", "accepted" | sort: "date" | reverse %}
{% for post in accepted_pubs %}
  {% include archive-single.html %}
{% endfor %}

<span style="display: inline-block; padding: 0.25em 0.75em; margin: 1.5em 0 0.5em 0; background-color: #2196F3; color: white; border-radius: 3px; font-size: 0.85em; font-weight: 600; text-transform: uppercase;">Published</span>

{% assign published_pubs = site.publications | where: "status", "published" | sort: "date" | reverse %}
{% for post in published_pubs %}
  {% include archive-single.html %}
{% endfor %}

<span style="display: inline-block; padding: 0.25em 0.75em; margin: 1.5em 0 0.5em 0; background-color: #FF9800; color: white; border-radius: 3px; font-size: 0.85em; font-weight: 600; text-transform: uppercase;">Under Review</span>

{% assign review_pubs = site.publications | where: "status", "under-review" | sort: "date" | reverse %}
{% for post in review_pubs %}
  {% include archive-single.html %}
{% endfor %}
