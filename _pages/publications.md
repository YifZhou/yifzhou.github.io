---
layout: single
title: "Publications"
permalink: /publications/
excerpt: "Selected recent results from the group."
description: "Recent group-led papers and 2026 collaborations by Yifan Zhou, including β Pictoris b's rotation, MIRI planet searches, and brown-dwarf variability."
author_profile: false
hide_page_title: true
share: false
comments: false
---

{% include base_path %}

<div class="editorial-page publications-page">
  <header class="page-intro">
    <p class="eyebrow">Selected recent results</p>
    <h1>Publications</h1>
    <p class="lead">Recent papers on planet formation and planetary atmospheres, including our 2026 results. <a href="{{ base_path }}/deep-dive/">Deep Dive</a> explains the group-led studies; the list below also includes recent collaborations.</p>
    <p class="article-links"><a href="#group-papers">Group-led papers</a><a href="#collaborations">Recent collaborations</a><a href="#full-publication-list">Full ADS record</a></p>
  </header>

  <section class="publications-list" aria-labelledby="group-papers">
    <h2 id="group-papers">Group-led papers</h2>
    {% assign group_papers = site.deep_dives | sort: "paper_order" | reverse %}
    {% for paper in group_papers %}
    <article class="publication-item">
      <div class="publication-item__number" aria-hidden="true">{% if forloop.index < 10 %}0{% endif %}{{ forloop.index }}</div>
      <div>
        <h3><a href="https://ui.adsabs.harvard.edu/abs/{{ paper.bibcode }}/abstract">{{ paper.paper_title | escape }}</a></h3>
        <p>{{ paper.paper_authors }} · {{ paper.paper_period }} · {{ paper.paper_journal }}</p>
        <p class="article-links"><span>{{ paper.paper_status }}</span><a href="{{ base_path }}{{ paper.url }}">Read the Deep Dive<span class="visually-hidden">: {{ paper.title }}</span></a></p>
      </div>
    </article>
    {% endfor %}
  </section>

  <section class="publications-list" aria-labelledby="collaborations">
    <h2 id="collaborations">Recent collaborations</h2>
    {% assign collaborations = site.data.recent_collaborations | sort: "order" | reverse %}
    {% for paper in collaborations %}
    <article class="publication-item">
      <div class="publication-item__number" aria-hidden="true">{% if forloop.index < 10 %}0{% endif %}{{ forloop.index }}</div>
      <div>
        <h3><a href="https://ui.adsabs.harvard.edu/abs/{{ paper.bibcode | escape }}/abstract">{{ paper.title | escape }}</a></h3>
        <p>{{ paper.authors }} · {{ paper.period }} · {{ paper.journal | escape }}</p>
        <p>{{ paper.status }}</p>
      </div>
    </article>
    {% endfor %}
  </section>

  <section class="split-band" aria-labelledby="full-publication-list">
    <div>
      <p class="eyebrow">Complete record</p>
      <h2 id="full-publication-list">Find the full publication list in NASA ADS.</h2>
      <p>The ADS record is the authoritative place to browse the complete, current bibliography.</p>
      <div class="button-row">
        <a class="site-button" href="https://ui.adsabs.harvard.edu/#search/p_=0&amp;q=orcid%3A0000-0003-2969-6040&amp;sort=date%20desc%2C%20bibcode%20desc">Open full ADS list</a>
      </div>
    </div>
  </section>
</div>
