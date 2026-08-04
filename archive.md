---
layout: default
title: Talk Archive
meta-description: "RAIN Seminar Talk Archive"
---

# RAIN Seminar Talk Archive

View the [upcoming RAIN seminar talks](/).

{% for category in site.data.archive %}
<h2 id="{{ category.type | slugify }}">{{ category.type }}</h2>
{% include talk-list.html members=category.members %}
{% endfor %}

Browse the [pre-2020 RAIN talk archive](https://docs.google.com/document/d/1zcB4p_KLtC8FaKImf0VXysRf_edFAE9jBCluuVvU7Cg/edit?usp=sharing) for earlier talks and abstracts.
