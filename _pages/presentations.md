---
layout: page
permalink: /presentations/
title: presentations
description: talks and posters in reversed chronological order
nav: true
nav_order: 3
---

<!-- _pages/presentations.md -->
<!-- entries come from _data/presentations.yml -->

<div class="publications">
  <ol class="bibliography">
    {% for item in site.data.presentations %}
      <li>
        <div class="row">
          <div class="col col-sm-2 abbr">
            <abbr class="badge rounded w-100">{{ item.type }}</abbr>
            {% if item.preview %}
              <img class="preview img-fluid z-depth-1 rounded" src="{{ item.preview | relative_url }}" alt="{{ item.title }}">
            {% endif %}
          </div>
          <div class="col-sm-8">
            <div class="title">{{ item.title }}</div>
            <div class="author">{{ item.authors | replace: 'Kaylee Vo', '<em>Kaylee Vo</em>' }}</div>
            <div class="periodical"><em>{{ item.venue }}</em>, {{ item.location }}. {{ item.date }}</div>
            <div class="links">
              {% if item.paper %}<a href="{{ item.paper }}" class="btn btn-sm z-depth-0" role="button">Paper</a>{% endif %}
              {% if item.poster %}<a href="{{ item.poster }}" class="btn btn-sm z-depth-0" role="button">Poster</a>{% endif %}
              {% if item.slides %}<a href="{{ item.slides }}" class="btn btn-sm z-depth-0" role="button">Slides</a>{% endif %}
              {% if item.source %}<a href="{{ item.source }}" class="btn btn-sm z-depth-0" role="button">Source</a>{% endif %}
            </div>
          </div>
        </div>
      </li>
    {% endfor %}
  </ol>
</div>
