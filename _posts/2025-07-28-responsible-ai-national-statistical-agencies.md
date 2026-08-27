---
layout: post
title: "Responsible AI in National Statistical Agencies"
subtitle: "Challenges in applying responsible AI principles in daily practice and what practitioners require to address these gaps."
collab: "U.S. Census Bureau Emerging Technology (xD) Fellowship"
date: 2025-07-28
tags: responsible-ai, government, policy
image: /images/projects/responsible-ai-data-lifecycle.png
thumbnail: /images/projects/responsible-ai-data-lifecycle.png
description: "Responsible AI is guided by principles in policy documents, NIST frameworks, and Executive Orders, but a persistent gap separates those principles from daily practice—visible in decisions like disclosure avoidance under deadline pressure, imputation choices for small datasets, and feature engineering that doesn't fully account for bias. This project conducted qualitative research with practitioners at eight federal statistical agencies, tracing where responsible AI principles break down at each stage of the data lifecycle—from raw data through deployment—and translating those findings into practitioner-focused recommendations: a policy navigator, shared evaluation rubrics with bias thresholds, community and domain-expert review, tiered model governance, and post-deployment feedback loops."
---

**U.S. Census Bureau Emerging Technology (xD) Fellowship**

---

### Problem

<img src="/images/projects/responsible-ai-principles-practice-gap.png" alt="Where the principles stop: transparency, accountability, fairness, explainability, respect for persons, and beneficence as stated in policy, mapped against what practitioners actually decide at the desk—which regulation applies, who owns the decision, impute/drop/suppress, why the board said no, which features and for whom, and who hears about it afterward" style="max-width:100%;display:block;margin:1.5rem auto;" />

Responsible AI is guided by principles articulated in policy documents, NIST frameworks, and Executive Orders. But a significant gap persists between these principles and their implementation.

That gap shows up in routine decisions—disclosure avoidance under tight deadlines, choosing an imputation method for a small dataset, feature engineering choices made without adequately weighing bias for affected populations. Harm can be introduced at any stage of the data lifecycle, through organizational structures such as agencies, review boards, and compliance regimes, and through cultural factors embedded in the data itself, including sensitivity, representation, and accountability for technical defaults.

This is best understood from the bottom up. Even practitioners familiar with the frameworks may not fully grasp the real challenges encountered in practice—a Census economist balancing privacy against a deadline, a Treasury staff member navigating conflicting regulations.

My central question: at which points in the data lifecycle do responsible AI principles break down in practice, and why?

---

### Solution

<img src="/images/projects/responsible-ai-what-practitioners-need.png" alt="What practitioners need: a table mapping each data lifecycle stage—raw data, processing, ordering, modeling, deployment—to where responsible AI breaks down and what is missing, from a policy navigator practitioners can query to post-deployment feedback loops" style="max-width:100%;display:block;margin:1.5rem auto;" />

I conducted qualitative research with practitioners at eight federal statistical agencies, treating their experiences as the primary source of insight rather than proposing a predetermined solution.

The inquiry followed the data lifecycle: producing raw data, processing, ordering to represent the world, building models, and deploying outputs. At each stage, I compared practitioners' experiences against federal responsible AI principles—transparency, accountability, fairness, explainability, respect for persons, and beneficence—not as a compliance exercise, but to identify where intent and infrastructure diverge.

The findings were specific to each stage. At the raw data stage, practitioners may be uncertain which regulation applies to a sensitivity decision, and accountability can be distributed across multiple roles, requiring deliberate stakeholder facilitation. At the ordering stage, technical choices carry distributive-justice implications—the imputation method chosen for a small jurisdiction's poverty estimate directly affects what that jurisdiction is allocated. At the model stage, governance boards may decide on criteria that aren't transparent to the practitioners building the models.

For each observation, I developed concrete, practitioner-focused recommendations: a policy navigator, shared evaluation rubrics with required bias thresholds, community and domain-expert review at the ordering stage, tiered model governance for transparency, and post-deployment feedback loops. These recommendations are designed to be adaptable across agencies.

---

### Impact

This synthesis shows that existing frameworks often overlook a basic fact: practitioners are committed to responsible AI, but lack the tools, explicit policies, and organizational support to implement it consistently. Recognizing this as an issue rooted in organizational culture and tooling shifts where solutions should focus.

The immediate users of these recommendations are agency practitioners, review boards, and policy leads who determine future investments. Ultimately, the beneficiaries are the populations affected by these decisions—small jurisdictions shaped by imputation choices, subgroups affected by bias evaluations.

The central argument is that closing the gap between principles and practice requires investment in practitioner-oriented tools, not additional governing frameworks that are hard to implement without ongoing, practitioner-specific organizational support. Accountability infrastructure should be built from the lived experience of those inside the system, with affected communities actively involved in designing the tools—not only in reviewing outcomes.

---

### Stack & Methods

Qualitative research · semi-structured practitioner interviews across eight federal statistical agencies · data lifecycle framework · federal responsible AI principles (transparency, accountability, fairness, explainability, respect for persons, beneficence) · NIST AI frameworks · policy analysis · U.S. Census Bureau Emerging Technology (xD) Fellowship.
