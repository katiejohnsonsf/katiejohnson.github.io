---
layout: post
title: "Responsible Feature Engineering: Advancing Fairness from Post-Hoc Audit to a Design Discipline"
subtitle: "U.S. Census Bureau Emerging Technology (xD) Fellowship"
collab: "With Atul Rawal"
date: 2025-02-27
tags: fairness, machine-learning, responsible-ai
image: /images/projects/responsible-feature-engineering-intervention-point.png
thumbnail: /images/projects/responsible-feature-engineering-intervention-point.png
description: "Most AI fairness interventions occur after model development, through output audits that address harms only after they've affected people—but by the time a model generates predictions, the decisions about data inclusion and feature selection that embedded the bias have already been finalized. This project, with Atul Rawal, developed Responsible Feature Engineering (RFE), a model-agnostic framework that evaluates whether a feature's influence varies across the demographic groups a model affects, surfacing proxy variables like latitude and longitude (which stand in for race via residential segregation) before they reach training. RFE doesn't automate the resulting judgment call—it makes an implicit, often invisible decision explicit and puts it in front of domain experts and affected communities."
---

<img src="/images/projects/responsible-feature-engineering-intervention-point.png" alt="Move the intervention earlier: a machine learning lifecycle timeline from data collection through feature engineering, model training, evaluation, deployment, and post-hoc audit. Feature engineering is marked as where to intervene instead, since bias is already embedded across the span up to where fairness is usually checked, at post-hoc audit." style="max-width:100%;display:block;margin:0 0 1.5rem;" />

**U.S. Census Bureau Emerging Technology (xD) Fellowship**

*With Atul Rawal*

---

### Problem

<img src="/images/projects/responsible-feature-engineering-proxy-feature.png" alt="Latitude is a proxy for race: applicant income, loan amount, latitude, and longitude given to a credit model. Latitude and longitude connect to the model's racially disparate credit decisions via residential segregation, even though race itself was excluded by design and never a column." style="max-width:100%;display:block;margin:1.5rem auto;" />

Most AI fairness interventions occur after model development, typically through output audits that address harms only after they've affected people. This overlooks an earlier and more effective intervention point. By the time a model generates predictions, the decisions about data inclusion and feature selection have already been finalized—bias introduced during feature engineering is embedded before any assessment of disparate impact or model evaluation begins.

The more effective intervention happens earlier: feature engineering is the stage where data scientists can assess whether a feature behaves differently across the populations a model affects. Remediation at this stage is significantly more cost-effective than post-deployment fixes.

My focus sits at the intersection of the organizational system—the machine learning lifecycle and an organization's governance practices—and the cultural system, where bias gets encoded as a seemingly neutral technical property with real consequences. The gap is that practitioners lack a standardized method to evaluate feature fairness at the point of selection.

---

### Solution

<img src="/images/projects/responsible-feature-engineering-influence-test.png" alt="Test the feature, not just the output: two bar charts of feature influence by population group A through E. One shows influence spread evenly across groups, labeled 'represents the population evenly, use it.' The other shows influence concentrated in group C, flagged for review before training, labeled 'one group carries the feature, review it before training.'" style="max-width:100%;display:block;margin:1.5rem auto;" />

In addition to post-hoc audits, I shifted the intervention to the earliest stages of the data lifecycle, before model development. Together with Atul Rawal, I developed a framework and paper introducing Responsible Feature Engineering (RFE) as a formalized practice within the machine learning lifecycle.

The central method evaluates how a feature's influence varies across the demographic groups a model affects. Consistent behavior across groups indicates fair representation; disproportionate influence for a specific subgroup signals the need for further investigation before using the feature in training.

The canonical example: latitude and longitude may appear neutral, but because of racially segregated residential patterns in the United States, these variables act as proxies for race. Models trained on location data in housing or credit contexts can produce racially biased predictions without ever explicitly encoding race. RFE exposes issues like this before they cause harm.

The framework is intentionally model-agnostic, built to be adopted as a standard practice rather than a niche technique. RFE also provides guidelines for when disparities should prompt review by domain experts or community governance, rather than relying solely on automated adjustments—keeping a human in the loop.

---

### Impact

Practitioners in regulated sectors—housing, credit, healthcare, employment—get a concrete intervention point before fairness issues are amplified during model training and deployment. That matters most in civic contexts, where models affect populations with limited avenues for recourse or transparency into how decisions were made.

This methodology argues for both a cultural and a technical shift: repositioning fairness practice from a post-hoc compliance measure to a foundational part of data design, shaping model development from the outset. Bringing impact considerations in early means measurement and testing get built in proactively, rather than bolted on.

A reviewer, Severen, raised a critical question: had we quantified the risk of underfitting when removing features for fairness? That question names the real tension—excluding a biased but predictive feature has a cost. RFE doesn't resolve that dilemma, but it puts the issue in front of practitioners and makes an implicit decision explicit. Right now, that decision is often made by default and stays invisible to the people building and reviewing the model. RFE is a tool for surfacing the decision, not automating it—the judgment stays with humans, ideally including the communities the model affects.

For RFE to become standard practice, it needs pipeline tooling at the feature selection stage, evaluation studies using real-world regulated-domain datasets, and partnerships with domain experts and communities who can identify latent variables that engineers may overlook on their own.

---

### Stack & Methods

Feature influence testing across demographic groups · model-agnostic fairness framework · proxy variable analysis · U.S. Census Bureau Emerging Technology (xD) Fellowship · co-authored with Atul Rawal.
