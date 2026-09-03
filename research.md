---
layout: default
title: Research & Publications
permalink: /research/
---

<h1 class="post-title">Research &amp; Publications</h1>

### Research

<div class="work-list research-work-list">
{% assign research_titles = "Informed Seattle: Collective Sensemaking Infrastructure with AI Supported Legislative Plain Text Summaries|Remote Sensing–ML Approach for Household Wealth Index Estimation" | split: "|" %}
{% for post in site.posts %}
  {% if research_titles contains post.title %}
  <div class="work-entry">
    <div class="work-left">
      <span class="work-date">{{ post.date | date: "%d %b %Y" }}</span>
      {% if post.thumbnail or post.image %}
      <div class="work-image">
        <img src="{{ post.thumbnail | default: post.image }}" alt="{{ post.title }}" />
      </div>
      {% endif %}
    </div>
    <div class="work-content">
      <h2 class="work-title">
        <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      </h2>
      {% if post.subtitle %}<p class="work-subtitle">{{ post.subtitle }}</p>{% endif %}
      {% if post.collab %}<p class="work-collab">{{ post.collab }}</p>{% endif %}
      <div class="work-desc-wrap">
        <p class="work-description">{{ post.description | default: post.content | strip_html | truncatewords: 110 }}</p>
      </div>
      <a href="{{ site.baseurl }}{{ post.url }}" class="work-more">More &rarr;</a>
    </div>
  </div>
  {% endif %}
{% endfor %}
</div>

### Publications

<ul class="publications-list">
  <li class="publication-entry">
    <p class="publication-authors">Atul Rawal, <strong>Katie Johnson</strong>, Curtis Mitchell, Michael Walton, Diamond Nwankwo.</p>
    <p class="publication-title">"Responsible Artificial Intelligence (RAI) in US Federal Government: Principles, Policies, and Practices."</p>
    <p class="publication-venue">Presented in Workshop: Regulatable ML: Towards Bridging the Gaps between Machine Learning Research and Regulations. NeurIPS, Vancouver, Canada, December 2024.</p>
  </li>
</ul>
