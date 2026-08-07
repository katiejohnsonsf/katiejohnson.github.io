---
layout: post
title: "Ecosystem Mapping: Classifying Endangered Plant Communities to Quantify the Ecological Cost of Data Centers"
subtitle: "Independent Ecological Data Science Research"
date: 2026-08-06
tags: ecology, remote-sensing, gis
image: /images/projects/ecosystem-mapping-rarity-heatmap.png
thumbnail: /images/projects/ecosystem-mapping-rarity-heatmap.png
description: "Ecosystem classification at the association level—the most precise and ecologically meaningful scale—is often costly, time-consuming, and incomplete, which means conservation resources may be misallocated and protective measures can lag behind ecological changes. This has become urgent as data center expansion creates substantial, localized demand for water and land, often diverted from ecosystems that depend on it. This project evaluates whether Earth Observation data, combined with California's vegetation datasets, can be used to train models that map ecosystems at the association level, producing a baseline for comparing infrastructure siting decisions against ecological risk."
---

<img src="/images/projects/ecosystem-mapping-rarity-heatmap.png" alt="California Ecosystem Surveys: rarest vegetation association per 1000m grid cell, based on 19,368 classified surveys across 8,280 cells and 10,029 distinct associations, showing statewide occurrences of the rarest association in each cell" style="max-width:100%;display:block;margin:0 0 1.5rem;" />

*This project builds upon my experience in the Ecosystems of California course at Mills College in 2008, where I studied under desert ecologist Bruce Pavlic. Since that time, I have tracked the expansion of the dataset as field crews have surveyed plant communities throughout California.*

---

### Problem

Effective environmental policy requires detailed knowledge of what needs protection. However, ecosystem classification at the association level—the most precise and ecologically meaningful scale—is often costly, time-consuming, and incomplete. In the absence of reliable data identifying which plant communities are rare or declining, conservation resources may be misallocated, and protective measures can lag significantly behind ecological changes.

The central question is which ecosystems are endangered within a given state, and how they can be identified rapidly enough to inform protection before siting decisions occur.

This issue has become increasingly urgent as the expansion of data centers creates substantial, localized demand for water and land. Much of this water is diverted from ecosystems that rely on it. A single large facility may consume millions of gallons daily for cooling, depleting watersheds and stressing plant communities that would be recognized as rare with association-level data. Without a baseline indicating what is endangered and where, these ecological costs remain unaccounted for in data center siting decisions.

Improved information sharing among agencies, targeted conservation funding, and informed infrastructure siting are essential to support future environmental health and biodiversity. The key challenge is that scarcity becomes apparent only at the association scale, yet current methods are neither fast nor affordable enough to keep pace.

---

### Solution

I have designed this project as a proof-of-concept to investigate geometric data science and temporal remote sensing methods. Rather than presenting a finalized pipeline, my aim is to initiate a dialogue regarding the potential of these approaches.

This work evaluates whether Earth Observation data, combined with California's vegetation datasets, can be used to train models that map ecosystems at the association level—the scale at which endangerment becomes apparent. Addressing this question will determine whether the model can identify endangered ecosystems within a state and to what extent, thereby providing a baseline for comparing siting decisions against ecological risk.

Data on endangered ecosystems transforms diffuse ecological costs into quantifiable metrics: identifying which associations are located in stressed watersheds, which are declining as water withdrawal increases, and which should be considered in siting decisions.

The exploratory data analysis revealed the complexity of fine-grained classification across heterogeneous landscapes, which constitutes a significant contribution of this project. The initial pipeline is publicly available and designed for adaptation by others.

---

### Impact

A reproducible pipeline would provide agencies, conservation organizations, and land managers with a faster and more cost-effective means to identify priority areas for protection. It would also enable stakeholders to hold new infrastructure projects accountable for their environmental impact by supporting decisions with empirical data rather than intuition.

Integrating an endangered-ecosystem baseline with data center water-use information would allow regulators to assess, prior to facility approval, which watersheds are at risk and which rare communities may be affected by water diversion. This approach shifts the ecological cost of computing from an unmeasured externality to documented evidence within the permitting process.

The project aims to demonstrate how data on vegetative communities can inform decision-making systems, ensuring that limited protection and water resources are legally recognized and safeguarded.

Achieving meaningful impact will require collaboration with experts in ecology, hydrology, and conservation policy to validate results and assess how the pipeline can support local permitting officials and community stakeholders. Ultimately, classification efforts translate into conservation only when those with practical knowledge and policy authority participate in shaping outcomes.

---

### Stack & Methods

Python, Jupyter, geospatial and GIS data (ESRI geodatabase), vegetation classification data (CDFW).

Project repository available on [GitHub](https://github.com/katiejohnsonsf/ecosystem-mapping).
