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
    <p class="article-links"><a href="#group-papers">Group-led papers</a><a href="#collaborations">Recent collaborations</a><a href="#white-papers">White papers</a><a href="#full-publication-list">Full publication list</a></p>
  </header>

  <section class="publications-list" aria-labelledby="group-papers">
    <h2 id="group-papers">Group-led papers</h2>
    {% for paper in site.data.group_preprints %}
    <article class="publication-item">
      <div class="publication-item__number" aria-hidden="true">{% if forloop.index < 10 %}0{% endif %}{{ forloop.index }}</div>
      <div>
        <h3><a href="https://ui.adsabs.harvard.edu/abs/{{ paper.bibcode }}/abstract">{{ paper.title | escape }}</a></h3>
        <p>{{ paper.authors }} · {{ paper.period }} · {{ paper.status }}</p>
      </div>
    </article>
    {% endfor %}
    {% assign group_papers = site.deep_dives | sort: "paper_order" | reverse %}
    {% for paper in group_papers %}
    <article class="publication-item">
      <div class="publication-item__number" aria-hidden="true">{% assign paper_number = forloop.index | plus: site.data.group_preprints.size %}{% if paper_number < 10 %}0{% endif %}{{ paper_number }}</div>
      <div>
        <h3><a href="{% if paper.publication_url %}{{ paper.publication_url | escape }}{% else %}https://ui.adsabs.harvard.edu/abs/{{ paper.bibcode }}/abstract{% endif %}">{{ paper.paper_title | escape }}</a></h3>
        <p>{{ paper.paper_authors }} · {{ paper.paper_period }} · {{ paper.paper_journal }}{% if paper.paper_citation %}, {{ paper.paper_citation }}{% endif %}</p>
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
        <h3>{% if paper.publication_url %}<a href="{{ paper.publication_url | escape }}">{{ paper.title | escape }}</a>{% elsif paper.bibcode %}<a href="https://ui.adsabs.harvard.edu/abs/{{ paper.bibcode | escape }}/abstract">{{ paper.title | escape }}</a>{% else %}{{ paper.title | escape }}{% endif %}</h3>
        <p>{{ paper.authors }} · {{ paper.period }} · {{ paper.journal | escape }}</p>
        <p>{{ paper.status }}</p>
      </div>
    </article>
    {% endfor %}
  </section>

  <section class="publications-list" aria-labelledby="white-papers">
    <h2 id="white-papers">White papers</h2>
    {% for paper in site.data.white_papers %}
    <article class="publication-item">
      <div class="publication-item__number" aria-hidden="true">{% if forloop.index < 10 %}0{% endif %}{{ forloop.index }}</div>
      <div>
        <h3><a href="https://ui.adsabs.harvard.edu/abs/{{ paper.bibcode | escape }}/abstract">{{ paper.title | escape }}</a></h3>
        <p>{{ paper.authors }} · {{ paper.period }} · {{ paper.status }}</p>
      </div>
    </article>
    {% endfor %}
  </section>

  <section class="split-band" aria-labelledby="full-publication-list">
    <div>
      <p class="eyebrow">Complete record</p>
      <h2 id="full-publication-list">Browse the full publication list.</h2>
      <p>As of October 30, 2026, the CV lists {{ site.data.publication_links.published }} published papers and {{ site.data.publication_links.accepted }} accepted manuscripts. The published papers include {{ site.data.publication_links.first_author }} first-author and {{ site.data.publication_links.mentee_led }} mentee-led papers. Preprints, submissions, and white papers are listed separately. The curated ADS search covers all {{ site.data.publication_links.indexed }} indexed CV records.</p>
      <div class="button-row">
        <a class="site-button" href="{{ site.data.publication_links.ads | escape }}">Browse publications in ADS</a>
        <a class="site-button" href="{{ site.data.publication_links.library | escape }}">My ADS library</a>
        <a class="site-button" href="{{ base_path }}/files/cv.pdf">Download the complete CV</a>
      </div>
    </div>
  </section>
</div>
