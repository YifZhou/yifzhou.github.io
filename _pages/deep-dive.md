---
layout: single
title: "Deep Dive"
permalink: /deep-dive/
description: "The questions, observations, and results behind recent papers from Yifan Zhou's research group."
author_profile: false
hide_page_title: true
share: false
comments: false
---

{% include base_path %}

<div class="editorial-page deep-dive-index">
  <header class="page-intro">
    <p class="eyebrow">Our research in detail</p>
    <h1>Deep Dive</h1>
    <p class="lead">The questions behind our recent papers, how we approached them, and what we learned.</p>
  </header>
  <div class="story-list">
    {% assign stories = site.deep_dives | sort: "paper_order" | reverse %}
    {% for story in stories %}
    <article class="story-card">
      <div class="story-card__image">
        <img src="{{ base_path }}/images/{{ story.social_image }}" width="{{ story.figure_width }}" height="{{ story.figure_height }}" alt="{{ story.figure_alt | escape }}" loading="lazy">
      </div>
      <div class="story-card__body">
        <p class="card-kicker">{{ story.topic }}</p>
        <h2><a href="{{ base_path }}{{ story.url }}">{{ story.title }}</a></h2>
        <p>{{ story.description }}</p>
        <p class="article-meta">{{ story.paper_authors }} · {{ story.paper_period }} · {{ story.paper_status }}</p>
        <a class="card-link" href="{{ base_path }}{{ story.url }}">Read the article<span class="visually-hidden">: {{ story.title }}</span></a>
      </div>
    </article>
    {% endfor %}
  </div>
</div>
