---
layout: page
title: Home
id: home
permalink: /
---

# Welcome!

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  This is the guide of this Blog <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration.
</p>

Digital Garden Template from [Github here](https://github.com/maximevaillancourt/digital-garden-jekyll-template).

If interested, [step-by-step guide](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).
<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 10 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
