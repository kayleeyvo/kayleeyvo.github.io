---
layout: page
permalink: /teaching/
title: teaching
description: courses I have taught in reversed chronological order
nav: true
nav_order: 4
---

<!-- _pages/teaching.md -->
<!-- entries come from _data/teaching.yml -->

<div class="publications">
  <ol class="bibliography">
    {% for item in site.data.teaching %}
      <li>
        <div class="row">
          <div class="col col-sm-2 abbr">
            <abbr class="badge rounded w-100">{{ item.course }}</abbr>
          </div>
          <div class="col-sm-8">
            <div class="title">{{ item.title }}</div>
            <div class="author"><em>{{ item.role }}</em>, with {{ item.instructor }}</div>
            <div class="periodical">{{ item.school }}. {{ item.term }}</div>
            {% if item.description %}<div class="periodical">{{ item.description }}</div>{% endif %}
            <div class="links">
              {% if item.course_page %}<a href="{{ item.course_page }}" class="btn btn-sm z-depth-0" role="button">Current Offering</a>{% endif %}
              {% if item.code %}<a href="{{ item.code }}" class="btn btn-sm z-depth-0" role="button">Code</a>{% endif %}
            </div>
          </div>
        </div>
      </li>
    {% endfor %}
  </ol>
</div>
