---
layout: single
title: "Research"
permalink: /research/
excerpt: "Planet formation, irradiated brown dwarfs, and changing planetary atmospheres."
description: "Yifan Zhou's research on planet growth, irradiated atmospheres, planetary rotation, and direct imaging, with recent results on β Pictoris b, MIRI planet searches, and brown dwarfs."
author_profile: false
hide_page_title: true
share: false
comments: false
---

{% include base_path %}

<div class="editorial-page research-overview">
  <header class="page-intro">
    <p class="eyebrow">Research themes</p>
    <h1>Planet formation and atmospheres</h1>
    <p class="lead">My group studies how planets grow, how they rotate, and how their atmospheres change. We use Hubble, JWST, and ground-based telescopes to measure accretion, compare day- and nightside spectra, and separate faint planets from their host stars.</p>
    <nav class="article-links" aria-label="On this research page"><a href="#research-themes">Research themes</a><a href="#recent-research">Recent results</a><a href="#research-students">Student projects</a></nav>
  </header>

  <section class="site-content" aria-labelledby="research-themes">
    <div class="section-heading">
      <h2 id="research-themes">Our research</h2>
      <p>Three connected questions guide our observations and the methods we develop.</p>
    </div>
    <div class="research-grid">
      <article class="research-card">
        <img class="research-card__image research-card__image--figure" src="{{ base_path }}/images/pds70-halpha.png" width="2024" height="933" alt="Hubble hydrogen-alpha images of PDS 70 in 2020 and 2024, with the growing planet c detected in 2024">
        <div class="research-card__body">
          <p class="card-kicker">01 · Formation</p>
          <h3>How young planets grow</h3>
          <p>Is gas accretion steady or variable? We measure the light released as gas falls onto young planets. PDS 70 c's changing hydrogen emission shows why repeated observations matter.</p>
          <a class="card-link" href="{{ base_path }}/research/accretion/">Explore the formation work</a>
        </div>
      </article>
      <article class="research-card">
        <img class="research-card__image research-card__image--figure" src="{{ base_path }}/images/ztf0038-phase-curve.png" width="1231" height="689" alt="ZTF0038B's measured phase curve and the day-night viewing geometry from Broski-Laing et al. (2026)">
        <div class="research-card__body">
          <p class="card-kicker">02 · Atmospheres</p>
          <h3>Irradiated brown dwarfs</h3>
          <p>How much heat moves from day to night? Daphne Broski-Laing's JWST study of ZTF0038B measures inefficient heat transport and a nightside carbon dioxide feature that remains difficult to explain.</p>
          <a class="card-link" href="{{ base_path }}/research/irradiated-worlds/">Explore irradiated worlds</a>
        </div>
      </article>
      <article class="research-card">
        <img class="research-card__image research-card__image--figure" src="{{ base_path }}/images/betapic-light-curves.png" width="1960" height="683" alt="β Pictoris b's light curves in two JWST infrared bands show a repeating rotation signal">
        <div class="research-card__body">
          <p class="card-kicker">03 · Imaging and variability</p>
          <h3>Finding planets and measuring their changes</h3>
          <p>What can repeated images and spectra reveal? Our recent work measures β Pictoris b's rotation, searches MIRI images for outer planets, and tests cloud models with changing brown-dwarf spectra.</p>
          <a class="card-link" href="{{ base_path }}/research/time-domain-imaging/">Explore imaging and variability</a>
        </div>
      </article>
    </div>
  </section>

  <section class="site-content" aria-labelledby="recent-research">
    <div class="section-heading">
      <h2 id="recent-research">Recent results</h2>
      <p>What we measured, what it tells us, and the questions that remain. Each article links to the research paper and its original figures.</p>
    </div>
    <div class="results-grid">
      {% assign research_stories = site.deep_dives | sort: "paper_order" | reverse %}
      {% for story in research_stories %}
      <article class="result-card">
        <p class="card-kicker">{{ story.paper_authors }} · {{ story.paper_period }}</p>
        <h3>{{ story.title }}</h3>
        <p>{{ story.research_summary | default: story.description }}</p>
        <p class="article-meta">{{ story.paper_status }}</p>
        <a class="card-link" href="{{ base_path }}{{ story.url }}">Read the Deep Dive<span class="visually-hidden">: {{ story.title }}</span></a>
      </article>
      {% endfor %}
    </div>
    <p class="button-row"><a class="card-link" href="{{ base_path }}/publications/">Publications and recent collaborations</a><a class="card-link" href="{{ base_path }}/news/#media-coverage">Research in the news</a></p>
  </section>

  <section class="split-band" aria-labelledby="research-approach">
    <div>
      <p class="eyebrow">Our approach</p>
      <h2 id="research-approach">What can variability tell us?</h2>
      <p>Changes in brightness and spectra constrain processes that a single observation cannot measure. We compare these changes with models of accretion, clouds, chemistry, and heat transport.</p>
    </div>
    <div class="split-band__aside">
      <p><a href="{{ base_path }}/deep-dive/">Deep Dive</a> explains the observations and results behind our recent papers.</p>
    </div>
  </section>

  <section class="site-content" aria-labelledby="research-students">
    <div class="section-heading">
      <h2 id="research-students">Student projects</h2>
      <p>Students measure brightness changes, extract spectra, test how well faint sources can be recovered, and compare observations with physical models. Yihan's MIRI search and Maddie's Hubble study are recent examples.</p>
    </div>
    <p>I welcome inquiries from students interested in these questions. Visit the <a href="{{ base_path }}/group/#prospective-students">prospective-student section</a> for preparation and how to get in touch.</p>
  </section>
</div>
