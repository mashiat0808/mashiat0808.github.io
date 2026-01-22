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

## Accepted

{% assign accepted_pubs = site.publications | where: "status", "accepted" | sort: "date" | reverse %}
{% for post in accepted_pubs %}
  {% include archive-single.html %}
{% endfor %}

## Published

{% assign published_pubs = site.publications | where: "status", "published" | sort: "date" | reverse %}
{% for post in published_pubs %}
  {% include archive-single.html %}
{% endfor %}

## Under Review

{% assign review_pubs = site.publications | where: "status", "under-review" | sort: "date" | reverse %}
{% for post in review_pubs %}
  {% include archive-single.html %}
{% endfor %}
