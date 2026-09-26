# Chapter 1: NHTSA Document Map

Sources: pack orientation across the three pinned public-domain sources (no body slice of its own). S1 Cybersecurity Best Practices for the Safety of Modern Vehicles, Updated 2022 final (87 FR 55459; docket NHTSA-2020-0087); S2 Automated Driving Systems 2.0: A Vision for Safety (DOT HS 812 442, September 2017); S3 49 CFR Part 571 Federal Motor Vehicle Safety Standards selections (GovInfo annual edition 2024). Chapter detail lives in ch02-ch07; paywalled and citation-only standards route through automotive-signpost and functional-safety-signpost. Reconstructed reference notes, not legal advice and not a substitute for the source documents.

## Core Idea

This pack answers vehicle electronics and software questions from three NHTSA-side documents with two different legal characters. S1 and S2 are voluntary guidance: they state what the agency recommends and do not bind the public by force of law. S3 is regulation: the Federal Motor Vehicle Safety Standards in 49 CFR Part 571 are the floor manufacturers must certify to before sale, enforced through compliance testing, defects investigation, and recall authority. The first sorting question for any consult is therefore guidance versus regulation, not "what does NHTSA say" as a single voice.

The chapter map is fixed. Cybersecurity programme and vehicle technical controls live in ch02-ch04 (S1). Automated Driving Systems taxonomy, twelve safety design elements, the Voluntary Safety Self-Assessment, and Federal/State role guidance live in ch05-ch06 (S2). The Part 571 framework and the selected FMVSS obligations live in ch07 (S3). Functional-safety vocabulary that the guidance names but does not reproduce lives at orientation depth in ch08, then exits to the two signpost packs. This chapter is the routing board; later chapters carry the reconstructed substance.

## Frameworks Introduced

- **Three-source stack.** S1 = vehicle cybersecurity best practices (Updated 2022 final). S2 = ADS 2.0 voluntary guidance (September 2017). S3 = 49 CFR Part 571 FMVSS selections (GovInfo 2024 annual edition in this pin). All three are US government public-domain material reconstructed here as reference notes.
- **Guidance versus regulation.** S1 and S2 recommend. Part 571 binds through manufacturer self-certification. Procurement pressure, liability practice, and state adoption can make guidance feel mandatory; that still does not convert it into an FMVSS.
- **S1 shape: [G.x] then [T.x].** Forty-five general best practices cover leadership, development process, risk, inventory, testing, monitoring, sharing, incident response, audit, education, aftermarket, and serviceability. Twenty-five technical best practices cover debug access, cryptography, diagnostics, internal communications, logs, wireless paths, and software/OTA updates. ch02-ch03 own the general block; ch04 owns the technical block.
- **S2 shape: Section 1 elements, Section 2 roles.** Section 1 adopts SAE automation levels by name, lists twelve priority safety design elements, and encourages a Voluntary Safety Self-Assessment. Section 2 clarifies Federal versus State roles and offers best-practice components for legislatures and state highway safety officials. ch05 owns Section 1; ch06 owns Section 2.
- **S3 shape: Subpart A plus selected Subpart B.** Subpart A is the general machinery (definitions, incorporation by reference, applicability, dates). Subpart B holds numbered standards. This pack's selected set is Standard Nos. 101, 105/135, 111, 124, 126/136, 138, and 141. Full standard bodies are not dumped; ch07 is an obligations landscape. FMVSS 127 stays out per pack pin.
- **Signpost exit ramps.** ISO 26262, ISO 21448 (SOTIF), ISO/SAE 21434, SAE J3016, UL 4600, IEC 61508, Automotive SPICE, and UNECE R155/R156 appear in this pack as name citations only. Designation, edition, owner, and obtain path live in automotive-signpost and functional-safety-signpost. ch08 holds concept orientation so those names are readable beside the NHTSA text.

## Key Concepts

### Which document answers which question

| Question | Go to | Pack chapter |
|---|---|---|
| How should a vehicle cybersecurity programme be led and built (risk, inventory, testing, monitoring)? | S1 secs 1-4.2 | ch02 |
| How should the programme operate after design (Auto-ISAC sharing, vulnerability reporting, incident response, self-audit, education, aftermarket, serviceability)? | S1 secs 4.3-7 | ch03 |
| What technical controls attach to debug ports, crypto, diagnostics, in-vehicle networks, logs, wireless paths, and OTA updates? | S1 sec 8 | ch04 |
| What ADS taxonomy and twelve safety design elements does NHTSA recommend, and what is a VSSA? | S2 Section 1 | ch05 |
| How do Federal and State roles split for ADS, and what best practices target legislatures and SHSOs? | S2 Section 2 | ch06 |
| What is Part 571, how does self-certification work, and what do the selected FMVSS require at landscape depth? | S3 Part 571 selections | ch07 |
| What do "functional safety," ASIL, safety lifecycle, and SOTIF mean when guidance names them? | orientation only | ch08 |
| Where do I buy or locate ISO 26262, ISO/SAE 21434, Automotive SPICE, SAE J3016, UNECE R155/R156? | automotive-signpost | signpost pack |
| Where do I buy or locate IEC 61508, ISO 26262, ISO 21448, UL 4600? | functional-safety-signpost | signpost pack |

### S1 in one page

- Title: Cybersecurity Best Practices for the Safety of Modern Vehicles, Updated 2022 final.
- Legal character: voluntary, non-binding guidance (noticed at 87 FR 55459; docket NHTSA-2020-0087).
- Scope: motor vehicles and motor vehicle equipment, including software; designers, suppliers, manufacturers, modifiers, and alterers.
- Spine: layered, compromise-assumed cybersecurity; NIST CSF as scaffold; [G.x] management system; [T.x] vehicle-side controls.
- Not in S1: FMVSS certification text, ADS twelve-element checklist detail (that is S2), paywalled ISO/SAE standard bodies.

### S2 in one page

- Title: Automated Driving Systems 2.0: A Vision for Safety (DOT HS 812 442, September 2017).
- Legal character: voluntary guidance; VSSA encouraged, not required, not an approval gate.
- Focus: SAE Levels 3-5 as adopted by name; twelve priority safety design elements; Federal/State role clarification.
- Standing NHTSA defect, recall, and enforcement authority still reaches motor vehicles and equipment that include ADSs.
- Not in S2: a substitute FMVSS set for ADS performance, UNECE R155/R156 text, or ISO 26262 clause text.

### S3 in one page

- Title: 49 CFR Part 571, Federal Motor Vehicle Safety Standards (selected).
- Legal character: binding regulation via manufacturer self-certification and NHTSA enforcement.
- Layout: Subpart A general rules; Subpart B numbered standards.
- This pack's selection (electronics and software relevance): 101, 105/135, 111, 124, 126/136, 138, 141.
- Not in this pack: full Part 571 dump, FMVSS 127 (AEB), or incorporation-by-reference document bodies.

### What this pack deliberately does not contain

- No ISO 26262, ISO 21448, ISO/SAE 21434, SAE J3016, UL 4600, IEC 61508, or Automotive SPICE standard text. Name citations only; signposts carry obtain paths.
- No UNECE R155/R156 body text. Free to download from the owner but (c) UNECE; citation-only rows in automotive-signpost.
- No full CFR republication. ch07 is a landscape of obligations, not a maintained law library.
- No legal advice. Guidance recommendations are not freestanding law; cited regulations bind as written in the current CFR.

## Mental Models

- **Sort legal character first.** Ask whether the question is about what NHTSA recommends (S1/S2) or what Part 571 requires (S3) before opening a chapter.
- **Process before controls for cyber.** [G.x] builds the programme; [T.x] hardens surfaces. Reading ch04 alone without ch02-ch03 misses ownership and lifecycle duties.
- **Elements before roles for ADS.** ch05 is the design checklist and VSSA; ch06 is who regulates whom once vehicles move on public roads.
- **Floor versus playbook.** FMVSS is the certification floor; S1/S2 are playbooks for electronics, cyber, and ADS functions that increasingly deliver or sit beside that floor.
- **Name is not text.** When a sentence needs ISO 26262, IEC 61508, SOTIF, UL 4600, or J3016 substance, leave this pack: ch08 orients the vocabulary, signposts point at the owner.
- **Orientation chapter, not the deep dive.** Use the routing table above; do not treat this chapter as a substitute for ch02-ch08.

## Anti-patterns

- **Citing S1 or S2 as if they satisfied a Part 571 certification duty.** Guidance is not the standard.
- **Citing an FMVSS number as if it answered a cybersecurity programme design question.** Programme shape is S1; the standard is a performance or equipment obligation.
- **Treating the VSSA as a Federal approval or as a substitute for self-certification.** It is voluntary public narrative under S2.
- **Codifying ADS 2.0 Section 1 into state statute as a design law.** S2 Section 2 explicitly discourages that collision path (detail in ch06).
- **Pasting paywalled standard clauses into internal "NHTSA pack" notes.** This pack carries none; use the signposts and buy or license the standard.
- **Assuming the selected FMVSS list is the whole of Part 571.** It is a pinned electronics-relevant landscape; other standards remain in force.
- **Skipping ch01 and searching randomly.** Wrong document is the most expensive first mistake in this domain.

## Key Takeaways

1. Three sources, two legal characters: S1 and S2 are voluntary NHTSA guidance; S3 (Part 571) is binding FMVSS regulation via self-certification.
2. Cybersecurity questions route to ch02-ch04 (S1 [G.x] and [T.x]); ADS questions route to ch05-ch06 (S2 Sections 1-2); FMVSS landscape questions route to ch07 (S3).
3. S1 is the 2022 final cybersecurity best practices (87 FR 55459, docket NHTSA-2020-0087); S2 is ADS 2.0 (DOT HS 812 442, September 2017); S3 is Part 571 selections from the pinned GovInfo annual edition.
4. Self-certification to applicable FMVSS is the US manufacturer duty at sale; S1/S2 do not replace it.
5. Functional-safety and related industry standards are citation-only here; ch08 orients concepts; automotive-signpost and functional-safety-signpost carry designation rows and free-path pointers.
6. UNECE R155/R156 and Automotive SPICE are likewise citation-only (copyright or no-derivatives constraints), even when a free download exists at the owner.
7. This chapter is the map. Open the chapter that owns the source slice before drafting programme language, design-element responses, or compliance matrices.

## Connects To

- **ch02-ch04** - S1 cybersecurity process, operations, and technical controls.
- **ch05-ch06** - S2 ADS safety elements, VSSA, and Federal/State role guidance.
- **ch07** - S3 Part 571 framework and selected FMVSS obligations.
- **ch08** - functional-safety orientation (IEC 61508 / ISO 26262 concepts at citation depth) and signpost routing.
- **automotive-signpost** - ISO 26262, ISO/SAE 21434, Automotive SPICE, SAE J3016, UNECE R155/R156, and SOTIF cross-ref rows.
- **functional-safety-signpost** - IEC 61508, ISO 26262, ISO 21448 (SOTIF), UL 4600 rows and fleet free-path names.
- **glossary.md / cheatsheet.md** - terms and decision rules once Task 9 lands.
