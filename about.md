---
layout: about
title: About
permalink: /
---

### How I Approach the Work

I love to build proof of concepts and prototypes with code to facilitate conversation but hold them lightly. I want to understand: what lever does this touch? Who are the stakeholders? What does a good ending look like? This is systems thinking applied before design.

I lead with learning. I don't assume I know everything, and I ask collaborators to help shape what gets built. I frame my technological contributions of data, AI, and UX as tools in service of a vision others help define, rather than imposing solutions.

I care about facilitation as a discipline equal to engineering. Data isn't just a pipeline output—when combined with human-centered facilitation, its design can enable conversation, connect stories, and create feedback loops between stakeholders. Facilitation is a design value, and the relevance of technical work relies on it.

I'm drawn to work that is legible at scale but meaningful at the individual level. I'm passionate about the tools and capabilities of technology to understand population-level patterns whilst simultaneously holding space for the reality of plurality outside of the data. Every person and moment in time is unique and is a strength of what it means to be human. I believe good systems design can support and use this as a means for constant improvement.

---

### What is my relationship to impact?

Impact is the organizing purpose of my work. Over time I've moved from identifying primarily as a data scientist to seeing myself as someone who catalyzes how problems and solutions are understood—for vulnerable populations, communities, and the ecosystems we all depend on. I care less about the technical skillset itself than about where and how it's applied.

I'm drawn to work with impact designed in from the start instead of only being measured after the fact: programs built with measurement and human-centered design from the beginning, so they actually change the lives of the people they're meant to serve. At its core, this work is about shifting power, transparency, and systems toward meeting people where they are and serving real human needs.

---

### How I Collaborate

I work best when there's genuine co-creation. I bring a draft and invite others to reshape it. I'm energized by thought leadership that operates from multiple angles at once, and I'm drawn to people who can contribute expertise I don't have: policy, demography, and community organizing.

I notice when I'm doing the "bridging" work — translating between people, domains, or emotional registers. I'm learning to make this more of a conscious choice rather than a reflex.

---

{% assign recent = site.posts.first %}{% if recent %}
<div class="about-recent">
<h3>Recent Projects</h3>
<div class="about-recent-card">
<div class="about-recent-left">
<span class="about-recent-date">{{ recent.date | date: "%d %b %Y" }}</span>
{% if recent.thumbnail or recent.image %}<img src="{{ recent.thumbnail | default: recent.image }}" alt="{{ recent.title }}" class="about-recent-thumb" />{% endif %}
</div>
<div class="about-recent-right">
<h4 class="about-recent-title"><a href="{{ site.baseurl }}{{ recent.url }}">{{ recent.title }}</a></h4>
{% if recent.subtitle %}<p class="about-recent-sub">{{ recent.subtitle }}</p>{% endif %}
{% if recent.collab %}<p class="about-recent-collab">{{ recent.collab }}</p>{% endif %}
<p class="about-recent-desc">{{ recent.description | default: recent.excerpt | strip_html | truncatewords: 35 }}</p>
</div>
</div>
<a href="{{ site.baseurl }}/work/" class="about-work-btn">View Projects</a>
</div>
{% endif %}

---

### Get in Touch

- GitHub: [katiejohnsonsf](https://github.com/katiejohnsonsf)
- Email: [thisiskatiejohnson@proton.me](mailto:thisiskatiejohnson@proton.me)
