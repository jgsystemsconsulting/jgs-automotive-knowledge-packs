# Cheatsheet: nhtsa-vehicle

Decision rules for US vehicle cybersecurity, ADS, and FMVSS questions. Each rule names the chapter that owns the detail; the paywalled and citation-only industry standards live behind the automotive-signpost and functional-safety-signpost packs.

## Which document governs my question? → ch01

- Vehicle cybersecurity programme or technical controls: S1, voluntary guidance. (ch01, ch02-ch04)
- ADS taxonomy, safety design elements, VSSA, Federal/State roles: S2, voluntary guidance. (ch01, ch05, ch06)
- What the vehicle must comply with at sale: S3, Part 571 FMVSS, binding through self-certification. (ch01, ch07)
- Sort legal character first: procurement pressure, liability practice, or state adoption never converts S1/S2 into an FMVSS. (ch01)
- A functional-safety name in a footnote is orientation only; decode it in ch08, then leave the pack. (ch01, ch08)

## Which chapter owns the cybersecurity question? → ch02-ch04

- Programme shape (leadership priority, risk assessment, inventory, testing, monitoring, documentation): ch02, practices [G.2]-[G.24].
- Post-production operations (Auto-ISAC sharing, vulnerability reporting, incident response, self-audit, education, aftermarket devices, serviceability): ch03, practices [G.25]-[G.45].
- Vehicle-side technical controls (debug access, cryptography, diagnostics, internal communications, event logs, wireless paths, updates and OTA): ch04, practices [T.1]-[T.25].
- Process before controls: reading ch04 alone misses who owns and maintains the controls. (ch02, ch04)
- Label quirk when citing: 45 general practices under 44 printed labels; no standalone [G.1], and [G.18] names two different practices. (ch02)

## Which chapter owns the ADS question? → ch05-ch06

- SAE levels as adopted, the twelve safety design elements, ODD/OEDR/MRC, validation, VSSA: ch05.
- Who regulates what, legislature best practices, and the state highway safety official framework: ch06.
- The VSSA is transparency, not type approval; NHTSA defect, recall, and enforcement authority still reaches ADS-equipped vehicles. (ch05)
- States should not codify the Voluntary Guidance into statute as design law. (ch06)
- Cybersecurity as ADS element 7 points back at ch02-ch04 for the detailed practices. (ch05)

## FMVSS or Part 571 question? → ch07

- Self-certification duty: the manufacturer certifies each applicable standard at sale; NHTSA enforces after the fact. (ch07)
- Four-part cite for any standard: number and title, one-line purpose, application paragraph (vehicle category and GVWR), electronics/software hook. (ch07)
- The selected set is 101; 105/135; 111; 124; 126/136; 138; 141. FMVSS 127 (AEB) is out of the pack pin. (ch01, ch07)
- Light/heavy twins: 105/135 brakes and 126/136 ESC; check the application paragraph before borrowing either story. (ch07)
- Landscape, not reprint: engineer and certify against the current CFR and its IBR documents. (ch07)

## Functional-safety term in the footnotes? → ch08

- Orientation depth only: concepts (functional safety, ASIL, safety lifecycle, SOTIF) with zero clause or table text. (ch08)
- Fault-based harm story → functional safety territory (IEC 61508 / ISO 26262 names). Insufficiency without a fault → SOTIF territory (ISO 21448 name). (ch08)
- ASIL is not an FMVSS grade and not an SAE automation level; never rank one with the other. (ch08)
- Meeting S1 practices or publishing a VSSA is not an ISO 26262 or IEC 61508 conformance claim. (ch08)

## Paywalled or citation-only standard? → the signpost packs

- automotive-signpost: ISO 26262:2018 series, ISO/SAE 21434:2021, Automotive SPICE 4.0, SAE J3016_202104, UNECE R155/R156 (free download, (c) UNECE, citation-only), and a SOTIF cross-ref row. (ch01, ch08)
- functional-safety-signpost: IEC 61508:2010, ISO 26262, ISO 21448 (SOTIF), UL 4600. (ch01, ch08)
- No standard text lives in this pack; the signposts carry designations, editions, and obtain paths. (ch01)

## Quick anchors

| Need | Answer | Chapter |
|------|--------|---------|
| Which document governs? | S1 cyber guidance, S2 ADS guidance, S3 Part 571 regulation; sort legal character first | ch01 |
| Cybersecurity programme shape | [G.2]-[G.24]: leadership, risk, inventory, testing, monitoring | ch02 |
| Post-production cyber duties | Auto-ISAC, reporting, response, audit, education, aftermarket, serviceability | ch03 |
| Technical controls | [T.1]-[T.25]: debug, crypto, diagnostics, networks, logs, wireless, updates/OTA | ch04 |
| Twelve ADS elements | System safety through Federal, State, and Local Laws, in source order | ch05 |
| ADS fallback rule | Detect malfunction or ODD exit, reach MRC; handback only if a receptive driver exists | ch05 |
| State versus federal | NHTSA: vehicle and equipment; States: driver, registration, insurance, liability | ch06 |
| Self-certification | Manufacturer certifies each applicable FMVSS at sale; no pre-approval | ch07 |
| ASIL question | Integrity label inside ISO 26262; orientation only here | ch08 |
| SOTIF question | Insufficiency without a fault; ISO 21448 by name | ch08 |
| Paywalled standard | Designations and purchase points, no text | both signposts |

## Tells & smells

| Smell | Likely gap | Chapter |
|-------|------------|---------|
| S1 or S2 cited as certification evidence | Guidance is not the standard | ch01, ch07 |
| FMVSS number quoted without its application paragraph | Vehicle category and GVWR decide scope | ch07 |
| ch04 controls with no ch02-ch03 programme behind them | Controls need an owner and a lifecycle | ch02-ch04 |
| [G.18] treated as one practice | The label is reused for two practices | ch02 |
| "Handles all roads" ODD language | Element 2 wants documented bounds and an ODD-exit MRC path | ch05 |
| VSSA sent to NHTSA for approval | The VSSA is voluntary and never approved | ch05 |
| State statute copying the twelve elements as design law | Section 2 preface discourages codification | ch06 |
| Level 4 claim mapped to ASIL D | Automation level and integrity level answer different questions | ch08 |
| ISO 26262 clause text in the notes | Citation-only; route to the signposts | ch01, ch08 |

## What this pack is not

- Not regulation: S1 and S2 are voluntary guidance; only Part 571 binds, through self-certification. (ch01)
- Not the standards: no ISO 26262, IEC 61508, ISO 21448, ISO/SAE 21434, SAE J3016, UL 4600, Automotive SPICE, or UNECE text; the signpost packs carry designations and obtain paths. (ch01, ch08)
- Not the whole of Part 571: a pinned electronics-relevant selection; FMVSS 127 and the remaining standards stay outside. (ch07)
- Not legal advice and not current-policy insurance: the source set is pinned 2026-09-25; check the current sources before relying on any single requirement. (ch01)
