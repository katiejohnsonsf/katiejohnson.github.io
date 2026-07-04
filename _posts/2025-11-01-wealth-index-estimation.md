---
layout: post
title: "Remote Sensing–ML Approach for Household Wealth Index Estimation"
subtitle: "U.S. Census Bureau — xD / SEHSD / AI and Global Development Lab"
date: 2025-11-01
tags: machine-learning, remote-sensing, census
image: /images/projects/wealth-index-estimation.png
thumbnail: /images/projects/wealth-index-thumbnail.png
---

![Median Household Income by Block Group and Dasymetric Downscaled Median HH Income, Rhode Island](/images/projects/wealth-index-estimation.png)

**U.S. Census Bureau — xD / SEHSD / AI and Global Development Lab**

---

### The Problem

The Census Bureau's mission is to serve as the nation's leading provider of quality data about its people and economy — but existing tools for understanding economic wellbeing at fine spatial resolution are constrained by fundamental survey design limits. Traditional small area estimation methods become statistically unreliable below the block group level, carry high compliance overhead, and can take years to reflect ground conditions.

Existing wealth measures capture only part of the picture. The Urban Institute's True Cost of Economic Security (TCES) — which compares a family's total costs (housing, health care, food, transportation, child care, savings, student debt, taxes, and other costs) against total resources — reveals that even families with meaningful incomes may not achieve genuine economic security when the full cost of living is accounted for. This cost-resource gap varies dramatically by geography, but current data tools cannot resolve it below the county or state level. The result: economic development interventions are targeted with a blunt instrument when a scalpel is needed.

The map produced in this project makes the problem legible at a finer grain. Rhode Island's 2023 ACS 5-year block group income data — one of the primary ground truth inputs — reveals stark spatial inequality even within a small state: dense urban cores (Providence and surrounding areas) show median household incomes concentrated below $100K and in some blocks below $50K, while suburban and coastal areas reach $150K–$250K. These differences matter enormously for families trying to meet basic costs, yet they are invisible to policy tools operating at the county level.

The core observation motivating this project: from Earth's orbit, it's possible to observe economic development directly — through construction and maintenance of housing, farmland, roads, and infrastructure. A temporally aware model tracking this development over time can estimate not just current wealth levels but trajectories of change — something surveys fundamentally cannot do between collection cycles.

---

### The Approach

This project developed a geo-temporal EO-ML pipeline to predict average material wealth at the 1km grid level, designed to support tagging of social and economic policies at the neighborhood level. The wealth index is framed as a gap measure — absolute income minus relative cost of living (using TCES or Self-Sufficiency Standard as the relative cost denominator) — making outputs meaningful across different regional contexts. The work proceeded through two complete phases, with GEE satellite image ingestion as the planned next step.

- **Phase 1 — Survey data preparation and visualization (R)**
- **Phase 2 — Survey data formatting for model input (Python)**
- **Phase 3 — Satellite image export (configured, next step)**

Disclosure risk was addressed throughout using xD pre-mortem frameworks.

---

### What It Makes Possible

The Rhode Island block group map produced in this work is itself a demonstration of the problem: meaningful income inequality is visible at the neighborhood level, but existing federal data products can't track how it changes over time or predict where it's heading. A completed version of this pipeline would produce historical, present, and projected wealth index estimates at 1km resolution — enabling:

- Program targeting by NGOs and governments
- Public infrastructure planning
- Disaster preparedness
- Causal analysis of policy treatment effects on wealth trajectories
- Health and workforce development planning

The TCES framework provides a particularly powerful lens for interpreting outputs: a neighborhood where incomes appear adequate at the county level may still show a persistent cost-resource gap when housing, child care, student debt, and savings needs are fully accounted for. This project was designed to make that gap visible at the spatial resolution where interventions can actually be made.

---

### What I Learned / What's Next

Implementation reached a meaningful and reproducible milestone: a complete data preparation pipeline producing model-ready input data across three survey vintages, a validated block group income visualization, and a configured GEE exporter ready to run. The work that remains — satellite export, model training, and validation against held-out Rhode Island data — is well-scoped and picks up from clear documentation.

The broader open questions are institutional: at what confidence interval does this approach become appropriate for official federal statistics, and which downstream applications are ready to use outputs at the current validation level?

---

### Stack & Methods

**Languages & Libraries:** R (tidycensus, terra, sf, exactextractr, sfarrow, ggplot2, dplyr), Python (pandas, numpy, ee, configparser, multiprocessing)

**Data & Infrastructure:** Google Earth Engine (Landsat 5/7/8, high-volume endpoint), LandSCAN Global population raster, ACS PUMS 5-year estimates (B19013)

**Methods:** Dasymetric downscaling, TCES/Self-Sufficiency Standard wealth gap framing, LSTM/ResNet-18 architecture (Daoud/Adel-Petterson), Pearson's r² evaluation, xD/Data & Society disclosure pre-mortem

**Scope:** Rhode Island PoC — 11,926 grid cells, 2013/2018/2023 vintages
