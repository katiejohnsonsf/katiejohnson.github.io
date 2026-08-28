---
layout: post
title: "Counting the Uncounted: Privacy-Preserving Linkage for Public Health"
subtitle: "U.S. Census Bureau Emerging Technology (xD) Fellowship / eHealth and Northwestern University CAPriCORN network"
date: 2025-11-26
tags: privacy, public-health, government
image: /images/projects/counting-uncounted-who-the-ssn-drops.png
thumbnail: /images/projects/counting-uncounted-who-the-ssn-drops.png
description: "Public health research depends on linking people across datasets—connecting someone's record to their Census responses to see how neighborhood conditions shape chronic disease—but the infrastructure to do this safely doesn't exist at scale, and the identifiers most linkage methods rely on are least available for the unhoused, low-income, and undocumented people the research is meant to serve. This project piloted VaultDB, a secure multiparty computation tool that lets the Census Bureau and Northwestern's ORION network compute across ACS and EHR data without either side exposing its records, and recommended moving from probabilistic matching with human review to a deterministic or hybrid method that avoids disclosing patient identity. The technical path proved tractable; the harder finding was that governance—an honest broker defensible under both Title 13 and HIPAA, a privacy review of externally-assigned identifiers, and community health advocates at the table—is the real unfinished work."
---

**U.S. Census Bureau Emerging Technology (xD) Fellowship / eHealth and Northwestern University CAPriCORN network**

---

### Problem

<img src="/images/projects/counting-uncounted-who-the-ssn-drops.png" alt="The identifier decides who counts: two record cards showing name, date of birth, address, and SSN fields. Record A is linked to Census responses; Record B has its SSN dropped before analysis. Captioned: people without an SSN in their record are disproportionately unhoused, low-income, or undocumented, and a linkage built on SSN repeats the erasure the research is meant to correct." style="max-width:100%;display:block;margin:1.5rem auto;" />

Public health research depends on linking people across datasets, connecting someone's record to their Census responses to see how neighborhood conditions shape chronic disease. This could surface insights about populations long underrepresented in health research, but the infrastructure to do it safely does not exist at scale.

The two organizational systems involved set hard constraints: Census data is protected under Title 13, health records under HIPAA, and the Bureau's matching outputs are possible links needing human review, creating unacceptable exposure of patient identity.

The cultural system encoded in the health data revealed the problem: people most likely to lack an SSN in their record are the unhoused, low-income, and undocumented. A linkage built on identifiers available to the well-documented would reproduce the erasure the research tries to correct. The lever is to establish that a person in one dataset is the same as in another without relying on SSNs, which biased record linkage accuracy against sensitive populations.

---

### Solution

<img src="/images/projects/counting-uncounted-compute-not-share.png" alt="Compute across both, move neither: U.S. Census Bureau ACS responses and Northwestern ORION electronic health records each stay in place, connecting only through VaultDB's secure multiparty computation, where neither side sees the other, answering which neighborhoods pair social conditions with high chronic disease." style="max-width:100%;display:block;margin:1.5rem auto;" />

<img src="/images/projects/counting-uncounted-matching-method.png" alt="No human review, no exposure: the current method — candidate pairs, scored possible links, human review — ends in patient identity exposed. The recommended method — exact identifier rules, deterministic or hybrid match, honest broker — ends in a linked cohort with no record read, flagged as still open: which honest broker can defend this under both Title 13 and HIPAA." style="max-width:100%;display:block;margin:1.5rem auto;" />

I began by mapping what the lever touched and what a good ending looked like for Bureau and health researcher stakeholders before designing anything.

This mapping informed the record linkage design for pilot testing VaultDB using existing Bureau and University infrastructure. This Secure Multiparty Computation tool lets institutions compute across each other's data without exposing it, enabling linkage between Census ACS data and EHRs held by Northwestern's ORION network.

After evaluating honest-broker tools (Linkja, Datavant) and a possible Phase 2 pathway, my core recommendation was to move from a probabilistic linkage method to one without human review to avoid disclosure of health record data. A deterministic matching method or a hybrid of deterministic and probabilistic methods, paired with the right honest broker, is fairer by design for populations less likely to have SSNs.

---

### Impact

<img src="/images/projects/counting-uncounted-governance-is-the-work.png" alt="Governance was the real work: a two-column checklist. Technical path, tractable — stakeholder mapping, secure computation layer selected, linkage design, and matching method recommended, all complete. Governance path, open — an honest broker defensible under both statutes, formal privacy review of externally-assigned PIKs, data standardization across the two organizations, and community health advocates at the table, none complete. Captioned: shipping a tool is not the same as shipping a safe one." style="max-width:100%;display:block;margin:1.5rem auto;" />

This pipeline would let researchers query across Census and EHR data which neighborhoods pair social determinants of health with high chronic disease, without either institution sharing its data, defensible under Title 13 and HIPAA. It ultimately serves patients who stay invisible in cross-institutional research because the infrastructure to include them safely does not yet exist.

My biggest takeaway was respect for governance as the real work: the technical path proved tractable, but I finished without a Phase 2 honest-broker solution I could confidently defend. Naming that gap was an important insight. The review layer that once seemed like friction is what makes public data trustworthy, and shipping a tool is not the same as shipping a safe one for vulnerable people between these two complex organizations.

The next phase needs a formal privacy review of externally-assigned PIKs, data-standardization coordination between Census and clinical partners, and community health advocates at the table to help frame test queries using the pilot pipeline.

<img src="/images/projects/counting-uncounted-phase-two-needs.png" alt="What the next phase needs: three cards — privacy review, a formal review of externally-assigned PIKs before any linkage runs; standardization, coordinated between the Bureau and the clinical partners holding records; and community voice, community health advocates at the table framing the test queries themselves. Captioned: none of the three is a technical task, and the pipeline is not defensible without all of them." style="max-width:100%;display:block;margin:1.5rem auto;" />

---

### Stack & Methods

VaultDB (Secure Multiparty Computation) · privacy-preserving record linkage · honest-broker evaluation (Linkja, Datavant) · deterministic and hybrid matching methods · Census ACS data · Northwestern ORION electronic health records · Title 13 / HIPAA compliance · U.S. Census Bureau Emerging Technology (xD) Fellowship · eHealth and Northwestern University CAPriCORN network.
