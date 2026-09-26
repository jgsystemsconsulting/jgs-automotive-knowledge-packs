---
name: automotive-signpost
kind: signpost
description: "Signpost (not a knowledge pack) for the automotive software standards landscape: ISO 26262:2018 road-vehicle functional safety; ISO/SAE 21434:2021 cybersecurity engineering; Automotive SPICE PRA/PAM 4.0; SAE J3016_202104 driving-automation taxonomy; UNECE Regulations 155 (CSMS) and 156 (SUMS); and the SOTIF cross-reference into functional-safety-signpost. Contains no source content: each row carries only the designation, title, edition, owner, redistributability status, and the owner's URL. Use when you need to identify, cite, or locate an automotive standard; paywalled rows point to the owner, free rows point to the publisher text or the in-repo nhtsa-vehicle pack."
---

# Automotive Software and Cybersecurity Standards: Signpost (pointers only)

**This is a signpost, not a knowledge pack.** It carries **no standards-body content**:
no reproduced clauses, no normative text, no synthesised summaries of the standards.
ISO 26262, ISO/SAE 21434, and SAE J3016 are paywalled with no redistribution grant
(Excluded under this repo's `docs/SOURCE-VETTING.md`); UNECE R155/R156 and Automotive
SPICE are free to download but remain (c) their publishers with citation-only or
no-derivatives terms, so they cannot be reconstituted into a redistributable pack
either. What this skill does: tell you which document you want, what it is for, who
owns it, whether a free copy exists, and where to get the authentic one.

## When to use

You are developing or reviewing automotive software and need to identify or cite the
governing document: which standard covers item-level functional safety, which ISO/SAE
text defines the cybersecurity engineering process, which UN regulation makes a CSMS
or SUMS mandatory for type approval, which SAE document fixes the J3016 autonomy
levels. Paywalled rows route you to the owner; free rows route you to the publisher
download or, where this repo ships one, to the installable pack.

**Prerequisites:** none, plain Markdown.

## How to use

Find your document below. The **Status** column says whether it can be packaged:

- **Excluded**: paywalled, no redistribution grant; buy from the owner. *Cannot* be packaged here.
- **Open**: free to obtain from the owner, but the copyright terms (citation only, or
  no derivatives) bar repackaging, so download from the URL given.
- **Cross-ref**: the full row lives in a sibling signpost pack in this repo.

Editions and dates were confirmed from the publisher catalogue pages and the UNECE
document register listed in the rows. Do not quote a publication date that a row does
not carry.

## Functional safety

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| ISO 26262 series (parts 1-12) | Road Vehicles - Functional Safety. Adaptation of the IEC 61508 model to road vehicles: item definition, ASIL classification, and the safety lifecycle for E/E systems including software. The functional-safety reference most automotive programmes are judged against. | 2018 (second edition) | ISO | Excluded: paywalled, no redistribution grant; buy from the owner | https://www.iso.org/standard/68383.html |

## Cybersecurity engineering

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| ISO/SAE 21434 | Road Vehicles - Cybersecurity Engineering. Cybersecurity risk management across the vehicle lifecycle: concept, product development, validation, production, and incident response. The engineering-process counterpart to UNECE R155 below. | 2021-08 | ISO; SAE International | Excluded: paywalled, no redistribution grant; buy from the owner | https://www.iso.org/standard/70918.html |

## UN type-approval regulation

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| UN R155 | Cyber Security and Cyber Security Management System. Uniform provisions for vehicle type approval with respect to cybersecurity and the CSMS (document E/ECE/TRANS/505/Rev.3/Add.154). | In force 2021-01-22 | UNECE | Open, free download (c) UNECE; citation only, not packaged here | https://unece.org/transport/documents/2021/03/standards/un-regulation-no-155-cyber-security-and-cyber-security |
| UN R156 | Software Update and Software Updates Management System. Uniform provisions for type approval with respect to software updates and the SUMS, including the RXSWIN software identification scheme. | In force 2021-01-22 | UNECE | Open, free download (c) UNECE; citation only, not packaged here | https://unece.org/transport/documents/2021/03/standards/un-regulation-no-156-software-update-and-software-updates-management-system |

## Process assessment

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| Automotive SPICE PRA/PAM 4.0 | Automotive Software Process Improvement and Capability dEtermination, Process Reference Model and Process Assessment Model. Process capability assessment for automotive software development, used in supplier audits and tenders. | 4.0, published 2023-11-29 | VDA QMC | Open, free download (c) VDA QMC; no derivatives, not packaged here | https://vda-qmc.de/wp-content/uploads/2023/12/Automotive-SPICE-PAM-v40.pdf |

## Driving automation taxonomy

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| SAE J3016_202104 | Taxonomy and Definitions for Terms Related to Driving Automation Systems. The standard level taxonomy (Levels 0-5) and the operational design domain vocabulary that ADS regulation and guidance, including the NHTSA documents this repo packages, build on. | J3016_202104, published 2021-04-30 | SAE International | Excluded: paywalled, no redistribution grant; buy from the owner | https://www.sae.org/standards/content/j3016_202104/ |

## Safety of the intended functionality (SOTIF)

| Designation | Title | Edition | Owner | Status | URL |
|-------------|-------|---------|-------|--------|-----|
| ISO 21448 | Road Vehicles - Safety of the Intended Functionality. Covers harm from functional insufficiency of the intended function (for example perception limits of an ADS) rather than system faults; the companion to ISO 26262. | 2022-06 | ISO | Cross-ref: full row in pack functional-safety-signpost | https://www.iso.org/standard/77490.html |

## Free paths in this repo and fleet

- **pack: nhtsa-vehicle** (this repo). The free regulator side of this landscape:
  NHTSA Cybersecurity Best Practices for the Safety of Modern Vehicles (Updated 2022),
  Automated Driving Systems 2.0: A Vision for Safety, and 49 CFR Part 571 FMVSS
  selections, packaged as reconstructed reference notes. The ISO/SAE rows above route
  the paywalled lookups; nhtsa-vehicle carries the regulator text.
- **pack: functional-safety-signpost** (this repo). The functional-safety lineage
  (IEC 61508, ISO 26262, ISO 21448, UL 4600) with its own free-path pointers.
- Fleet sibling repos are named, not linked, per the fleet link policy: automotive
  content lives only in this repo today; the SE fleet repo (jgs-se-knowledge-packs)
  and the med-device repo (jgs-med-device-knowledge-packs) hold the adjacent
  system-safety and medical-device signposts.

---
*Signpost content © JG Systems Consulting Ltd. (MIT). Standard designations and titles
are named for reference only; "ISO", "SAE", "VDA QMC", "UNECE", and document numbers are the
property of their respective owners. Named for identification, not endorsement.*
