---
layout: post
title: "Recurve Market Access Reporting"
subtitle: "Data product for CPUC oversight of $150M in clean-energy program funding"
date: 2022-10-10
tags: energy, government, data-engineering
image: /images/projects/recurve-duck-curve-peak-reduction.png
thumbnail: /images/projects/recurve-duck-curve-peak-reduction.png
description: "The California Public Utilities Commission oversees $150 million in Market Access program funding meant to accelerate the shift to a clean-energy economy through utility-run, demand-side programs—but funding was allocated using estimated savings rather than verified results, risking both ratepayer accountability and the low-income and hard-to-reach households the programs were meant to serve. This project built a configurable Market Access reporting pipeline that measures outcomes directly from meter data, developed through weekly collaboration with business stakeholders as CPUC requirements evolved. A dbt/LaTeX/Looker abstraction layer made the pipeline portable across utility clients with different datasets, cutting new-client deployment effort 30x, while anonymized building attribute data let energy efficiency companies evaluate performance across jurisdictions without exposing personal information."
---

![Reducing the 7–9pm peak — flattening the duck curve](/images/projects/recurve-duck-curve-peak-reduction.png)

**Data product for CPUC oversight of $150M in clean-energy program funding**

---

### Problem

The public needed accountability for clean-energy funding but relied on measurements that, at the time, did not exist at the necessary level of detail.

The California Public Utilities Commission oversees $150 million in funding for its Market Access program—money intended to promote the shift to a clean energy economy through demand-side programs operated by the utilities. To qualify for that funding, though, programs must show actual results, and the tools available for this purpose were based on estimated savings rather than real meter data.

The reporting problem wasn't merely technical. The CPUC set out requirements and revised them across several rounds; data definitions needed to stay consistent across utility clients with very different datasets; and there was a risk that forecasted values would be read as actual, measured performance when projects hadn't yet gone online. Getting this wrong meant either misdirecting ratepayer funds or letting the programs that most effectively serve customers—including those reaching low-income and hard-to-reach households—fail to get credit for what they delivered.

The difficulty was building a measurement system trustworthy enough to allocate public funds.

---

### Solution

I led the development of a configurable reporting pipeline that measures outcomes from meter data and scales across utilities.

The project produced a Market Access reporting product for the whole organization, with scope shaped through weekly collaboration with business stakeholders and subject matter experts so that data definitions could evolve step by step as CPUC's requirements changed—treating changing requirements as a normal part of the design process rather than a disruption to it.

The technical work made the pipeline both accurate and portable:

- CPUC-aligned metrics, written in SQL and modeled in Looker, were designed so a single pipeline could serve any client, letting Market Access programs scale.
- A configuration layer abstracting dbt, LaTeX, and Looker made the pipeline adaptable to different utility datasets, cutting new-client deployment effort 30x.

Privacy was also a central concern when modeling data to improve energy efficiency. I led conversations with internal and external stakeholders about protecting small and medium-sized enterprises by anonymizing building attribute data. This allowed energy efficiency companies to evaluate performance across different jurisdictions while keeping personal information safe.

---

### Impact

A system for measuring actual outcomes for the people being served, so public funds match public value delivered.

- **Public accountability** for $150M in Market Access funding, with outcomes measured from actual meter data rather than estimated.
- **Scalable oversight** across California utilities, so accurate reporting doesn't have to be rebuilt from scratch for each client.
- **Customer privacy** protected, so the need for transparency doesn't risk disclosure that could harm building occupants.

The key impact is a commitment to using taxpayer money in a way that holds clean-energy programs answerable to both the public that funds them and the customers they serve.

---

### Stack & Methods

SQL (BigQuery) · Looker · dbt · LaTeX · Python (pandas) · BigQuery ML · Google Cloud Storage · Guru (documentation) · stakeholder facilitation and project scoping · CPUC Market Access reporting requirements.
