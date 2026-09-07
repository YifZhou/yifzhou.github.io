---
layout: single
title: "News"
permalink: /news/
description: "Media coverage, research highlights, student awards, and recent papers from Yifan Zhou's astronomy group at the University of Virginia."
author_profile: false
hide_page_title: true
share: false
comments: false
---

{% include base_path %}

<div class="editorial-page news-page">
  <header class="page-intro">
    <p class="eyebrow">From the group</p>
    <h1>News</h1>
    <p class="lead">Media coverage, research highlights, and updates from our group.</p>
    <nav class="article-links" aria-label="On this news page"><a href="#media-coverage">In the news</a><a href="#group-updates">Papers from the group</a></nav>
  </header>
  <section class="news-section" aria-labelledby="media-coverage">
    <h2 id="media-coverage">In the news</h2>
    <p>Coverage and announcements from universities, observatories, journals, and scientific societies. Dates below refer to the reports.</p>
    <div class="news-list">
      {% assign coverage = site.data.media_coverage | sort: "date" | reverse %}
      {% for item in coverage %}
        {% include news-item.html item=item %}
      {% endfor %}
    </div>
  </section>
  <section class="news-section" aria-labelledby="group-updates">
    <h2 id="group-updates">Papers from the group</h2>
    <p>Short summaries of our recent papers, with longer explanations in Deep Dive. Preprints are labeled separately from refereed publications.</p>
    <div class="news-list">
      {% assign news_items = site.data.news | sort: "date" | reverse %}
      {% for item in news_items %}
        {% include news-item.html item=item %}
      {% endfor %}
    </div>
  </section>
</div>
