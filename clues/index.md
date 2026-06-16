---
layout: page
title: "Unlocked Clues"
permalink: /clues/
---

Every station you've reached so far. Tap one to read its ticket.

{% assign clues = site.pages | where: "layout", "clue" | sort: "clue_number" %}
<ul class="clue-list">
{% for c in clues %}
  <li><a href="{{ c.url | relative_url }}">Clue No. {{ c.clue_number }} — {{ c.title }}</a></li>
{% endfor %}
</ul>

<style>
.clue-list{ list-style:none; padding:0; }
.clue-list li{ margin:.4rem 0; font-family:"Cinzel",serif; font-size:1.05rem; }
.clue-list a{ text-decoration:none; }
.clue-list li::before{ content:"❧ "; color:var(--pumpkin); }
</style>
