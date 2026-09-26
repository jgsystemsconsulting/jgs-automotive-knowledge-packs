# Capability to Knowledge-Pack Map

Working artifact mapping sector technical capabilities to the pack chapters that provide
reference depth for each capability. Empty-tree template seed: no content packs yet.

Rules of construction:
- Every chapter in every pack under `packs/<slug>/chapters/` is assigned to exactly one capability cluster (best fit).
- Signpost packs contain no chapters and are not mapped.
- Machine-readable version: `docs/capability-pack-map.json`.
- Machine-readable classification rules: `docs/classification-rules.json`.
- Changelog (v0.1.0): empty-tree template seed.

## Summary

| Cluster | Entries |
|---|---|
| 1. Cybersecurity & ADS | 5 |
| 2. Regulatory & FMVSS | 4 |
| 3. Functional Safety Orientation | 1 |
| **Total** | **10** |

## 1. Cybersecurity & ADS

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| nhtsa-vehicle | ch02-cyber-process-and-leadership.md | S1 leadership priority and risk-based cybersecurity development process (general practices through 4.2) |
| nhtsa-vehicle | ch03-cyber-ops-sharing-incident-audit.md | S1 post-production ops: Auto-ISAC sharing, vulnerability reporting, incident response, self-audit, education, serviceability |
| nhtsa-vehicle | ch04-cyber-technical-controls.md | S1 technical vehicle controls [T.1]-[T.25]: debug access, crypto, diagnostics, logs, wireless, OTA updates |
| nhtsa-vehicle | ch05-ads-taxonomy-and-safety-elements.md | ADS 2.0 Section 1: SAE levels as adopted, 12 safety design elements, Voluntary Safety Self-Assessment |
| nhtsa-vehicle | ch06-ads-state-roles-and-best-practices.md | ADS 2.0 Section 2: Federal and State roles, legislature and state highway safety official best practices |

## 2. Regulatory & FMVSS

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| nhtsa-vehicle | ch01-nhtsa-document-map.md | Which NHTSA document answers which vehicle cyber, ADS, or FMVSS question; guidance versus regulation sort |
| nhtsa-vehicle | ch07-fmvss-part571-landscape.md | 49 CFR Part 571 Subpart A framework and selected FMVSS obligations landscape (101, 105/135, 111, 124, 126/136, 138, 141) |
| nhtsa-vehicle | glossary.md (support file) | Shared NHTSA vehicle cyber, ADS, and FMVSS terms used across the pack |
| nhtsa-vehicle | cheatsheet.md (support file) | Cross-chapter decision checklists for cyber, ADS, and FMVSS consult questions |

## 3. Functional Safety Orientation

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| nhtsa-vehicle | ch08-functional-safety-orientation.md | Functional-safety concepts at orientation depth only; paywalled standards route to the signpost packs |
