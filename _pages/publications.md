---
title: "KLY Group - Publications"
layout: gridlay
excerpt: "KLY Group -- Publications."
permalink: /publications/
---

# Publications

For publications prior to 2019, see [Google Scholar](https://scholar.google.com/citations?hl=en&user=2nC9a2cAAAAJ&view_op=list_works&sortby=pubdate).

Jump to [journals](#journals), [conferences](#conferences).

{% assign publication_types = "journal,conference" | split: "," %}
{% for publication_type in publication_types %}
## {% if publication_type == "journal" %}Journals{% else %}Conferences{% endif %}

{% assign publications = site.data.publist | where: "type", publication_type | sort: "year" | reverse %}
{% assign publications_by_year = publications | group_by: "year" %}
{% for year in publications_by_year %}
<p>{{ year.name }}</p>
<ol>
{% for publication in year.items %}
<li>{{ publication.citation }}</li>
{% endfor %}
</ol>
{% endfor %}
{% endfor %}
