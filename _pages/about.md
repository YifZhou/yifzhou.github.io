---
layout: splash
title: "Yifan Zhou | Exoplanets, Planet Formation, and Atmospheres"
permalink: /
excerpt: "How planets form and how their atmospheres change."
description: "Yifan Zhou is an astronomer at the University of Virginia studying how planets form and how their atmospheres change."
author_profile: false
sitemap: true
---

{% include base_path %}

  <section class="home-hero" aria-labelledby="home-hero-title">
    <div class="home-hero__inner">
      <div class="home-hero__copy">
        <p class="eyebrow">Observational astronomy at UVA</p>
        <h1 id="home-hero-title">How planets form and change.</h1>
        <p class="home-hero__lead">I am an astronomer at the University of Virginia. My group uses Hubble, JWST, and ground-based telescopes to study how planets grow and how clouds, chemistry, and heat shape their atmospheres.</p>
        <div class="button-row">
          <a class="site-button" href="{{ base_path }}/research/">Explore the research</a>
          <a class="site-button site-button--light" href="{{ base_path }}/group/#prospective-students">For prospective students</a>
        </div>
      </div>
      <div class="home-hero__media">
        <img src="{{ base_path }}/images/home-hero.png" width="1536" height="1024" alt="Artist's concept of a young planet collecting gas, a brown dwarf with a hot dayside and cool nightside, and a space telescope observing a distant planet">
      </div>
    </div>
    <p class="hero-caption">Artist's concept of a growing planet, an irradiated brown dwarf, and JWST observations of a distant planet.</p>
  </section>

<div class="home-page">
  <section class="site-content" aria-labelledby="research-at-a-glance">
    <div class="section-heading">
      <h2 id="research-at-a-glance">Research at a glance</h2>
      <p>We observe planets and brown dwarfs over time to measure changes in their accretion, brightness, and spectra.</p>
    </div>
    <div class="research-grid">
      <article class="research-card">
        <img class="research-card__image" src="{{ base_path }}/images/accretion_art.jpg" width="985" height="554" alt="Artist's concept of a young planet accreting material from a surrounding disk">
        <div class="research-card__body">
          <p class="card-kicker">Planet formation</p>
          <h3>How young planets grow</h3>
          <p>We measure the light released as gas falls onto young planets. Repeated observations reveal how this process changes.</p>
          <a class="card-link" href="{{ base_path }}/research/accretion/">Read about accretion</a>
        </div>
      </article>
      <article class="research-card">
        <img class="research-card__image research-card__image--figure" src="{{ base_path }}/images/ztf0038-phase-curve.png" width="1231" height="689" alt="ZTF0038B's measured phase curve and the day-night viewing geometry from Broski-Laing et al. (2026)">
        <div class="research-card__body">
          <p class="card-kicker">Irradiated worlds</p>
          <h3>Irradiated brown dwarfs</h3>
          <p>We follow brown dwarfs around white dwarfs to measure how external heating changes their day- and nightside atmospheres.</p>
          <a class="card-link" href="{{ base_path }}/research/irradiated-worlds/">Read about irradiated worlds</a>
        </div>
      </article>
      <article class="research-card">
        <img class="research-card__image" src="{{ base_path }}/images/2M1207b_JWST.png" width="1024" height="768" alt="Illustration of time-resolved JWST observations of a directly imaged planet">
        <div class="research-card__body">
          <p class="card-kicker">JWST observations</p>
          <h3>Changing planetary atmospheres</h3>
          <p>We measure planetary rotation and atmospheric variability, including the nine-hour rotation of β Pictoris b.</p>
          <a class="card-link" href="{{ base_path }}/research/time-domain-imaging/">Read about the methods</a>
        </div>
      </article>
    </div>
  </section>

  <section class="split-band" aria-labelledby="student-inquiry">
    <div>
      <p class="eyebrow">Prospective students</p>
      <h2 id="student-inquiry">Interested in working with us?</h2>
      <p>I welcome inquiries from students interested in planet formation, planetary atmospheres, or astronomical observations. Please tell me about your interests, background, and when you hope to begin.</p>
      <div class="button-row">
        <a class="site-button" href="mailto:{{ site.author.email }}">Send an inquiry</a>
        <a class="site-button site-button--light" href="{{ base_path }}/group/#prospective-students">How to prepare</a>
      </div>
    </div>
    <div class="split-band__aside">
      <p>Our projects involve images, spectra, physical models, and scientific computing. The research pages and Deep Dive articles offer a starting point for learning about our work.</p>
    </div>
  </section>

  <section class="site-content" aria-labelledby="teaching-preview">
    <div class="section-heading">
      <h2 id="teaching-preview">Teaching and mentoring</h2>
      <p>I teach students how we use observations and physical models to understand planets, stars, and galaxies.</p>
    </div>
    <div class="teaching-grid">
      <article class="teaching-card">
        <p class="card-kicker">ASTR 1250</p>
        <h3>Alien Worlds</h3>
        <p>Planets beyond the Solar System: how we find them and what we know about their properties.</p>
      </article>
      <article class="teaching-card">
        <p class="card-kicker">ASTR 5110</p>
        <h3>Astronomical Techniques</h3>
        <p>How astronomical instruments work, how we reduce their data, and how we interpret the measurements.</p>
      </article>
      <article class="teaching-card">
        <p class="card-kicker">Mentoring</p>
        <h3>Learn by doing</h3>
        <p>Students develop independent questions while working with images, spectra, time series, and models.</p>
      </article>
    </div>
    <p class="button-row"><a class="card-link" href="{{ base_path }}/teaching/">See teaching overview</a></p>
  </section>

  <section class="site-content" aria-labelledby="recent-results">
    <div class="section-heading">
      <h2 id="recent-results">Selected recent results</h2>
      <p>Read the science behind three recent papers from our group.</p>
    </div>
    <div class="results-grid">
      {% assign recent_stories = site.deep_dives | sort: "paper_order" | reverse %}
      {% for story in recent_stories limit:3 %}
      <article class="result-card">
        <p class="card-kicker">{{ story.paper_year }} · {{ story.paper_authors }}</p>
        <h3>{{ story.title }}</h3>
        <p class="result-card__source"><a href="{{ base_path }}{{ story.url }}">Read the Deep Dive<span class="visually-hidden">: {{ story.title }}</span></a></p>
      </article>
      {% endfor %}
    </div>
    <p class="button-row"><a class="card-link" href="{{ base_path }}/deep-dive/">All Deep Dive articles</a><a class="card-link" href="{{ base_path }}/news/">Group news</a></p>
  </section>
</div>
