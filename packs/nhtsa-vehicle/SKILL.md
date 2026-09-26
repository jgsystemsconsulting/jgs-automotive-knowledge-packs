---
name: nhtsa-vehicle
description: "Reconstructed reference notes on US NHTSA vehicle guidance, built from three public-domain sources (Cybersecurity Best Practices for the Safety of Modern Vehicles, Updated 2022 final, 87 FR 55459, docket NHTSA-2020-0087; Automated Driving Systems 2.0: A Vision for Safety, DOT HS 812 442, September 2017; 49 CFR Part 571 FMVSS selections, GovInfo annual edition 2024; pinned 2026-09-25). Use for vehicle cybersecurity programme questions (the 45 general [G.x] and 25 technical [T.x] best practices: leadership priority, the risk-based development process, hardware and software asset inventory, cybersecurity testing and monitoring, Auto-ISAC information sharing, vulnerability reporting, incident response, self-audit, education, aftermarket and user-owned devices, serviceability, and technical controls from debug access to over-the-air updates), automated driving system questions (SAE levels of driving automation as adopted in ADS 2.0, the 12 priority safety design elements, the Voluntary Safety Self-Assessment, Federal and State regulatory roles, best practices for legislatures and state highway safety officials), and the FMVSS landscape (Part 571 Subpart A framework, self-certification, and the selected standards 101, 105/135, 111, 124, 126/136, 138, 141). SCOPE LIMITS: US NHTSA and Federal Register sources only; no ISO 26262, ISO 21448 (SOTIF), ISO/SAE 21434, SAE J3016, UL 4600, or IEC 61508 text, which are cited by name only (see the automotive-signpost and functional-safety-signpost packs); UNECE R155/R156 are free downloads but (c) UNECE and are likewise citation-only; functional-safety coverage is orientation depth only; FMVSS coverage is a selected landscape, not the full standard set; guidance is not regulation; reflects the pinned source dates, not later agency actions; synthesized reference notes, not legal advice and not a substitute for the source documents. LICENCE: Public Domain (US Government work, 17 U.S.C. 105)."
---

<!-- argument-hint: [cybersecurity practice, ADS question, FMVSS standard number, or chapter number] -->

# NHTSA Vehicle Cybersecurity, ADS, and FMVSS Guidance
**Source**: U.S. National Highway Traffic Safety Administration (NHTSA), 3-source reference set: Cybersecurity Best Practices for the Safety of Modern Vehicles (Updated 2022 final; 87 FR 55459, docket NHTSA-2020-0087), Automated Driving Systems 2.0: A Vision for Safety (DOT HS 812 442, September 2017), and 49 CFR Part 571 FMVSS selections (GovInfo annual edition 2024); pinned 2026-09-25 | **Licence**: Public Domain (US Government work, 17 U.S.C. 105) | **Chapters**: 8

## When to use

**Prerequisites:** none, plain Markdown; no MCP server, API key, or licence tier needed at runtime.

Use this skill for questions about how US federal guidance and regulation shape vehicle electronics and software: what NHTSA expects of a vehicle cybersecurity programme, from leadership priority and the risk-based development process through information sharing, vulnerability reporting, incident response, and the technical controls; what ADS 2.0 recommends for automated driving systems, including the safety design elements and the voluntary safety self-assessment; how the FMVSS regime is organised and what the selected Part 571 standards demand; and where functional-safety standards (IEC 61508, ISO 26262) fit at orientation depth. The pack answers with NHTSA's own frameworks, cited by chapter and source row.

## How to Use This Skill

- **Without arguments**: read the Core Frameworks below for the three-source map, the general and technical cybersecurity practices, the ADS 2.0 guidance structure, and the FMVSS landscape.
- **With a topic**: use the Topic Index to find the chapter, then ask directly (e.g. "what does NHTSA say about over-the-air updates", "which safety design element covers fallback", "what does FMVSS 141 require").
- **With a chapter**: ch01 orientation (which document answers which question); ch02-ch04 cybersecurity best practices (S1); ch05-ch06 ADS 2.0 (S2); ch07 FMVSS landscape (S3); ch08 functional-safety orientation.

Supporting files: `glossary.md`, `cheatsheet.md`.

## Core Frameworks & Mental Models

### Guidance versus regulation: which NHTSA document answers what
The pack rests on three documents with two different legal characters. **S1 and S2 are voluntary guidance**: they express what NHTSA recommends and do not bind the public. S1 (the 2022 final cybersecurity best practices, noticed at 87 FR 55459 under docket NHTSA-2020-0087) addresses the industry's vehicle cybersecurity processes and controls; S2 (ADS 2.0, DOT HS 812 442, September 2017) addresses the safe testing and deployment of automated driving systems. **S3 is regulation**: the Federal Motor Vehicle Safety Standards in 49 CFR Part 571 are legally binding through the manufacturer self-certification duty, and NHTSA enforces defects and noncompliance against them. The mental model for reading any question: first decide whether it is about what NHTSA recommends (guidance, chapters 02 to 06) or about what the rulebook requires (FMVSS, chapter 07). Guidance can become de facto practice through procurement, liability, and state adoption, but citing it as "required" is a category error this pack keeps visible.

### General best practices: leadership and the risk-based development process ([G.x], S1)
S1 enumerates its recommendations so they can be tracked and audited: **45 general best practices printed under 44 distinct labels** (the source has no standalone [G.1] and reuses [G.18] for two different practices) and 25 technical best practices numbered [T.1] to [T.25]. The general block opens with organizational commitment: leadership priority on product cybersecurity, a vehicle development process with explicit cybersecurity considerations, and a risk assessment step that drives design decisions. It then runs the asset side: maintain inventories of vehicle hardware and software, track sufficient detail on software components (the software bill of materials habit), and evaluate commercial off-the-shelf and open-source components before use. Assurance follows: product cybersecurity testing including penetration testing at the vehicle level, qualified testers independent of development, and vulnerability analysis for known weaknesses. Layered protection covers sensor vulnerabilities and safety-critical systems first: any unreasonable risk is removed or mitigated, and residual functionality sits behind layers of protection. The mental model: [G.x] practices are the management system; they set up everything the [T.x] practices enforce.

### Operating the programme: sharing, reporting, response, audit (S1)
Four process chapters turn the development-time practices into a running capability. **Information sharing** works through the Automotive Information Sharing and Analysis Center (Auto-ISAC): members collect intelligence on potential attacks and contribute to the sector's shared picture. **Vulnerability reporting** means a published, coordinated disclosure path: an accessible reporting channel, acknowledgment and triage of reports, and remediation tracked to closure. **Incident response** is an organizational process with roles, escalation, and the ability to mitigate safety risks to occupants and other road users, exercised before it is needed. **Self-auditing** closes the loop: organizations should assess their own conformance to these practices and feed results back into the process. Around these sit education (workforce and consumer), aftermarket and user-owned devices (both vehicle manufacturers and aftermarket device manufacturers have obligations), and serviceability (repair and maintenance must not degrade cybersecurity). The mental model: the programme is a lifecycle, not a launch gate; post-production operation carries its own named duties.

### Technical controls: the [T.x] practices (S1)
The 25 technical best practices attach controls to specific attack surfaces, and each maps to a section of the source. Debug and developer access in production devices must be locked down. Cryptographic protections cover keys, algorithms, and their lifecycle management. Vehicle diagnostic functionality and diagnostic tools both need protection, because diagnostics are a designed-in backdoor if left open. Vehicle internal communications (the in-vehicle networks carrying safety-critical messages) need segmentation, gateway controls, and protection against message injection and spoofing. Event logging should capture security-relevant events to support detection and forensics. Wireless paths into vehicles (remote services, key fobs, tire pressure sensors, in-vehicle Wi-Fi and cellular) each get surface-specific hardening. Finally, software updates and modifications, including **over-the-air (OTA) updates**, need process controls: authenticity and integrity verification, rollback safety, and update management consistent with the organizational programme. The mental model: [T.x] is a checklist over the vehicle's physical and network surfaces; a control gap maps to a named practice, which makes review auditable.

### ADS 2.0: levels, safety design elements, and the VSSA (S2)
ADS 2.0 is organized as two sections. **Section 1, Voluntary Guidance**, adopts SAE International's levels of driving automation (naming the SAE taxonomy rather than writing its own) and centers on **12 priority safety design elements**: system safety; operational design domain (ODD); object and event detection and response (OEDR); fallback (minimal risk condition); validation methods; human machine interface; vehicle cybersecurity; crashworthiness; post-crash ADS behavior; data recording; consumer education and training; and federal, state, and local laws. Three habits recur across the elements: a documented process for each element, design and validation against the assessed risks within the declared ODD, and the ability to detect malfunction or ODD exit and fall back to a minimal risk condition, with higher-automation vehicles able to do so without driver intervention. **Section 2** covers Federal and State regulatory roles and best practices for legislatures and state highway safety officials (licensing, registration and titling, test applications, training public safety officials). The **Voluntary Safety Self-Assessment (VSSA)** is the accountability instrument: entities are encouraged, not required, to publish a public statement of how they address the elements. The mental model: the elements are a design checklist and the VSSA is its public receipt.

### FMVSS and Part 571: the self-certification landscape (S3)
Part 571 is the code of FMVSS, organized with **Subpart A (General)** carrying scope, definitions, applicability, and incorporation-by-reference machinery, and **Subpart B (Safety Standards)** carrying the numbered standards. Manufacturers certify each vehicle to applicable standards at sale; the chapters treat the selected set as named obligations with engineering intent rather than as a republication of rule text: 101 (controls and displays), 105 and 135 (hydraulic and electric, and light vehicle, brake systems), 111 (rear visibility), 124 (accelerator control systems), 126 and 136 (electronic stability control systems, light and heavy vehicle), 138 (tire pressure monitoring systems), and 141 (minimum sound requirements for hybrid and electric vehicles). The selection favors electronics-and-software-relevant standards, which is where guidance (S1, S2) and regulation meet. The mental model: FMVSS define the floor the vehicle must certify to; guidance describes how to build the electronics that increasingly deliver it.

### Functional-safety orientation: the bridge to IEC 61508 and ISO 26262 (ch08)
Both NHTSA documents lean on the functional-safety tradition without reproducing it: S1's 2022 update explicitly considers ISO/SAE 21434 for corporate processes, and S2's system-safety element points at the functional-safety process standard for road vehicles. Chapter 08 holds the orientation layer only: the concepts (hazard analysis and risk classification, safety lifecycle, safety integrity levels and their automotive derivation, and the SOTIF concern of hazards without component faults) are explained at citation depth so the guidance's references are readable. The standards themselves, ISO 26262, IEC 61508, ISO 21448 (SOTIF), ISO/SAE 21434, UL 4600, SAE J3016, and Automotive SPICE, are cited by name only; the automotive-signpost and functional-safety-signpost packs carry the pointer tables. The mental model: this pack tells you what NHTSA says about safety; the signposts tell you where the underlying standards live.

---

## Chapter Index

| Ch | File | Sources (pages) | Coverage | Cluster |
|----|------|-----------------|----------|---------|
| 01 | [ch01-nhtsa-document-map](chapters/ch01-nhtsa-document-map.md) | orientation (authored without a source slice) | Which document answers which question; the FMVSS/Part 571 landscape; where cyber and ADS guidance fit; signpost routing | Regulatory & FMVSS |
| 02 | [ch02-cyber-process-and-leadership](chapters/ch02-cyber-process-and-leadership.md) | S1 secs 1-4.2 (pp 5-11; 7 pp) | Purpose, scope, background; leadership priority on product cybersecurity; the development process with cybersecurity risk assessment, asset inventory, and testing [G.x] | Cybersecurity & ADS |
| 03 | [ch03-cyber-ops-sharing-incident-audit](chapters/ch03-cyber-ops-sharing-incident-audit.md) | S1 secs 4.3-7 (pp 12-16; 5 pp) | Information sharing (Auto-ISAC), vulnerability reporting, incident response, self-auditing, education, aftermarket and user-owned devices, serviceability | Cybersecurity & ADS |
| 04 | [ch04-cyber-technical-controls](chapters/ch04-cyber-technical-controls.md) | S1 sec 8 (pp 17-21; 5 pp) | Technical practices [T.1]-[T.25]: debug access, cryptography, diagnostics, internal communications, event logs, wireless paths, software and OTA updates | Cybersecurity & ADS |
| 05 | [ch05-ads-taxonomy-and-safety-elements](chapters/ch05-ads-taxonomy-and-safety-elements.md) | S2 sec 1 (pp 7-22; 16 pp) | SAE levels of driving automation as adopted; the 12 priority safety design elements; Voluntary Safety Self-Assessment | Cybersecurity & ADS |
| 06 | [ch06-ads-state-roles-and-best-practices](chapters/ch06-ads-state-roles-and-best-practices.md) | S2 sec 2 (pp 24-30; 7 pp) | Federal and State regulatory roles; best practices for legislatures and for state highway safety officials | Cybersecurity & ADS |
| 07 | [ch07-fmvss-part571-landscape](chapters/ch07-fmvss-part571-landscape.md) | S3 Subpart A (pp 3-15) + selected standards | Part 571 framework and self-certification; selected standards 101, 105/135, 111, 124, 126/136, 138, 141 as obligations | Regulatory & FMVSS |
| 08 | [ch08-functional-safety-orientation](chapters/ch08-functional-safety-orientation.md) | orientation (IEC 61508 / ISO 26262 concepts at citation depth; no source slice) | Functional-safety vocabulary and concepts behind the guidance's references; routes to both signpost packs | Functional Safety Orientation |

## Topic Index

- ADS 2.0 guidance structure and scope → ch01, ch05
- Aftermarket and user-owned devices → ch03
- Auto-ISAC and information sharing → ch03
- Automotive SPICE → ch08
- Brake standards (FMVSS 105, 135) → ch07
- Controls and displays (FMVSS 101) → ch07
- Cryptographic protections and key management → ch04
- Data recording (ADS element) → ch05
- Debug/developer access in production devices → ch04
- Diagnostics functionality and diagnostic tools → ch04
- Education (workforce and consumer) → ch03, ch05
- Event logs and forensics → ch04
- Fallback and minimal risk condition → ch05
- FMVSS self-certification duty → ch01, ch07
- Functional safety (IEC 61508, ISO 26262) orientation → ch08
- Hazard analysis and risk classification concepts → ch08
- Human machine interface (ADS element) → ch05
- Incident response process → ch03
- Internal communications (in-vehicle networks) → ch04
- ISO/SAE 21434 (cybersecurity engineering) → ch02, ch08
- Minimum sound requirements (FMVSS 141) → ch07
- Operational design domain (ODD) → ch05
- Over-the-air (OTA) updates → ch04
- Part 571 structure (Subpart A, Subpart B) → ch01, ch07
- Post-crash ADS behavior → ch05
- Rear visibility (FMVSS 111) → ch07
- Risk assessment in the development process → ch02
- SAE levels of driving automation → ch05
- Self-auditing → ch03
- Sensor vulnerabilities → ch02
- Serviceability → ch03
- SOTIF (ISO 21448) → ch08
- System safety (ADS element) → ch05
- Tire pressure monitoring (FMVSS 138) → ch07
- UL 4600 → ch08
- Validation methods (ADS element) → ch05
- Vehicle cybersecurity (ADS element) → ch05
- Vulnerability reporting and coordinated disclosure → ch03
- Wireless attack surfaces → ch04

## Supporting Files

- `glossary.md`: key terms (ADS, Auto-ISAC, FMVSS, MRC, ODD, OEDR, OTA, SOTIF, VSSA) with chapter references.
- `cheatsheet.md`: decision rules (which document governs, which chapter, which practice block applies, when to route to a signpost).

## Scope & Limits

- **NHTSA sources only.** This pack restates US federal material: the 2022 final cybersecurity best practices (S1), ADS 2.0 (S2), and the selected FMVSS (S3). Other agencies' vehicle rules (EPA, NHTSA's rulemaking docket detail beyond the cited notice) and state law are outside it.
- **Standards are citation-only.** ISO 26262, ISO 21448 (SOTIF), ISO/SAE 21434, SAE J3016, UL 4600, IEC 61508, and Automotive SPICE are copyrighted or no-derivatives; no text, table, or clause wording from any of them appears here. UNECE R155/R156 are free to download but (c) UNECE, so they are likewise citation-only. For designations, editions, and free or purchase paths, use the automotive-signpost and functional-safety-signpost packs.
- **Functional safety is orientation depth only.** Chapter 08 explains the concepts behind the guidance's references; it does not substitute for the standards or for an actual safety case.
- **FMVSS is a selection, not the code.** Chapter 07 covers the Part 571 framework and the selected standards named in the chapter index. The remaining standards, and compliance engineering against any of them, are out of scope; consult the current CFR text.
- **Guidance is not regulation.** S1 and S2 are voluntary guidance; they do not bind manufacturers. The FMVSS self-certification duty is the binding layer. Nothing in this pack is legal advice or a substitute for the source documents or counsel.
- **Dates are pinned.** The source set was pinned 2026-09-25 (S1 final September 2022; S2 September 2017; S3 the 2024 annual edition). Later agency actions, new guidance, or FMVSS amendments are out of scope; check the current sources before relying on any single requirement.
