---
name: functional-safety-signpost
kind: signpost
description: "Signpost (not a knowledge pack) for the functional safety standards landscape: IEC 61508:2010 (ed 2.0, parts 1-7) for E/E/PE safety-related systems; ISO 26262:2018 as its road-vehicle derivation; ISO 21448:2022 on the safety of the intended functionality (SOTIF); and UL 4600 Ed 3 for autonomous products. Contains no source content: each row carries only the designation, title, edition, owner, redistributability status, and the owner's URL. Use when you need to identify, cite, or locate a functional safety standard; every row is paywalled, so each points to the owner's page, and the free paths section routes to nhtsa-vehicle in this repo and to fleet sibling packs by name."
---

# Functional Safety Standards: Signpost (pointers only)

**This is a signpost, not a knowledge pack.** It carries **no standards-body content**:
no reproduced clauses, no normative text, no synthesised summaries of the standards.
Every document in this lineage (IEC 61508, ISO 26262, ISO 21448, UL 4600) is paywalled
with no redistribution grant, Excluded under this repo's `docs/SOURCE-VETTING.md`, so
none can be reconstituted into a redistributable pack. What this skill does: tell you
which document you want, what it is for, who owns it, and where to buy the authentic one.

## When to use

You are developing or reviewing a safety-related system and need to identify or cite
the governing document: which standard is the generic functional safety baseline, which
text adapts it to road vehicles, which one addresses hazard behaviour without faults
(SOTIF), and which standard evaluates an autonomous product end to end. Each row routes
you to the owner; the free-paths section points at what this fleet ships alongside.

**Prerequisites:** none, plain Markdown.

## How to use

Find your document below. The **Status** column says whether it can be packaged:

- **Excluded**: paywalled, no redistribution grant; buy from the owner. *Cannot* be packaged here.

All four rows are Excluded; the URL column is the owner's authoritative catalogue page,
not a download. Editions were confirmed from the IEC, ISO, and UL catalogue pages; do
not quote a publication date that a row does not carry.

## Generic baseline

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| IEC 61508 (parts 1-7) | Functional Safety of Electrical/Electronic/Programmable Electronic Safety-related Systems. The generic baseline: safety lifecycle, SIL determination, and the hardware and software requirements that sector standards derive from. | Ed 2.0, 2010 | IEC | Excluded: paywalled, no redistribution grant; buy from the owner | https://webstore.iec.ch/en/publication/5515 |

## Automotive derivation

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| ISO 26262 series (parts 1-12) | Road Vehicles - Functional Safety. The automotive adaptation of IEC 61508: replaces SIL with ASIL, adds the item definition, and tailors the lifecycle to road-vehicle E/E systems including software. | 2018 (second edition) | ISO | Excluded: paywalled, no redistribution grant; buy from the owner | https://www.iso.org/standard/68383.html |

## Safety of the intended functionality

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| ISO 21448 | Road Vehicles - Safety of the Intended Functionality (SOTIF). Addresses harm caused by functional insufficiency of the intended function, for example perception or algorithmic limits of a driving automation system, in the absence of a fault; the companion to ISO 26262. | 2022 (first edition), published 2022-06 | ISO | Excluded: paywalled, no redistribution grant; buy from the owner | https://www.iso.org/standard/77490.html |

## Autonomous products

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| UL 4600 | Standard for Evaluation of Autonomous Products. Safety case approach for autonomous vehicles and machines operating without human intervention, covering scenarios the ISO lineage leaves open (it assumes no human driver and no infrastructure safety net). | Ed 3, published 2023-03-17 | UL Standards & Engagement | Excluded: paywalled, no redistribution grant; buy from the owner | https://www.shopulstandards.com/ProductDetail.aspx?productId=UL4600 |

## Free paths in this repo and fleet

- **pack: nhtsa-vehicle** (this repo). The free regulator side of the automotive
  landscape: NHTSA Cybersecurity Best Practices (Updated 2022), Automated Driving
  Systems 2.0, and 49 CFR Part 571 FMVSS selections as reconstructed reference notes.
- Fleet sibling repos are named, not linked, per the fleet link policy:
  **jgs-se-knowledge-packs** carries the SE fleet's system safety signpost covering
  MIL-STD-882 and adjacent military standards; **jgs-med-device-knowledge-packs**
  carries the medical-device signpost with FDA cybersecurity guidance (CSA) coverage.
  Both flank this lineage for cross-sector work; neither repackages it.

---
*Signpost content © JG Systems Consulting Ltd. (MIT). Standard designations and titles
are named for reference only; "IEC", "ISO", "UL", and document numbers are the
property of their respective owners. Named for identification, not endorsement.*
