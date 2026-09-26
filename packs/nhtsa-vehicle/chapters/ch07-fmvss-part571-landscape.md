# Chapter 7: FMVSS Part 571 Landscape

Sources: S3 49 CFR Part 571 Federal Motor Vehicle Safety Standards (GovInfo annual edition 2024, 49 CFR Ch. V (10-1-24 Edition)), Subpart A General (structure, definitions, incorporation by reference, applicability, effective date, separability, seating designation) and selected Subpart B standards: Standard No. 101; 105; 111; 124; 126; 135; 136; 138; 141. Page landmarks in `sources/text/S3.txt`: Subpart A roughly pp. 3-15; selected standards at body starts near pp. 16 (101), 31 (105), 228 (111), 334 (124), 340 (126), 378 (135), 398 (136), 406 (138), 418 (141). Full standard bodies are not reproduced; this chapter is an obligations landscape. FMVSS 127 (automatic emergency braking) stays out per pack pin. Part 570 lead-in and bare ToC plates excluded. No CFR section text dump; short named references only.

## Core Idea

Part 571 is regulation, not guidance. It is the code of Federal Motor Vehicle Safety Standards (FMVSS) that manufacturers must certify to before selling new motor vehicles and covered equipment. Subpart A carries the general machinery: scope of the part, definitions used across standards, how matter is incorporated by reference, which vehicles a standard reaches, effective dates, separability, and seating-position designation rules. Subpart B carries the numbered standards themselves.

US practice is manufacturer self-certification, not pre-market type approval by NHTSA for each design. The manufacturer determines that the vehicle meets each applicable standard and certifies accordingly; NHTSA enforces through compliance testing, defects investigation, and recall authority. S1 and S2 (ch02-ch06) recommend processes and ADS design elements; they do not replace this floor. This chapter maps the Part 571 framework and a selected set of electronics- and software-relevant standards. It is not a substitute for the current CFR text or for compliance engineering against any standard.

## Frameworks Introduced

- **Part 571 two-subpart layout.** Subpart A (General) hosts cross-cutting rules (among them definitions at 571.3, explanation of usage at 571.4, matter incorporated by reference at 571.5, applicability at 571.7, effective date at 571.8, separability at 571.9, designation of seating positions at 571.10). Subpart B (Federal Motor Vehicle Safety Standards) hosts Standard No. NNN entries under 571.NNN.
- **Self-certification duty.** Each applicable Subpart B standard is a performance (and sometimes equipment) obligation the manufacturer must meet and certify at sale. Failure modes are noncompliance and safety-related defect processes under NHTSA authority, not a ch05-style voluntary self-assessment.
- **Incorporation by reference (IBR).** Subpart A lists external test methods, drawings, and industry publications that standards call into (SAE recommended practices, ASTM methods, and similar). Compliance engineering follows those incorporated editions as the standard states; this pack does not reproduce IBR texts.
- **Applicability is per-standard.** Vehicle categories (passenger car, multipurpose passenger vehicle, truck, bus, motorcycle, low-speed vehicle, heavy vehicle classes, and others defined in Subpart A) and GVWR cutoffs decide which standards bite. Always read the standard's own application paragraph.
- **Standard No. 101; Controls and displays.** Performance requirements for location, identification, color, and illumination of controls, telltales, and indicators. Purpose: accessibility, visibility, and recognition so drivers can select the right control. Applies to passenger cars, multipurpose passenger vehicles, trucks, and buses. Electronics relevance: telltale and indicator behavior for malfunctions, TPMS lamps, ESC lamps, and ADS HMI still sit on top of a regulated display vocabulary.
- **Standard No. 105; Hydraulic and electric brake systems.** Requirements for hydraulic and electric service brake systems and associated parking brakes. Purpose: safe braking under normal and emergency conditions. Application centers on multipurpose passenger vehicles, trucks, and buses above the standard's GVWR threshold equipped with hydraulic or electric brakes (light vehicles are largely under 135). Electronics relevance: brake power units, antilock modulators, and electric vehicle braking definitions appear in the standard's vocabulary.
- **Standard No. 135; Light vehicle brake systems.** Requirements for service brake and associated parking brake systems on light vehicles. Purpose: safe braking under normal and emergency driving conditions. Applies to passenger cars (from the standard's dated threshold) and to multipurpose passenger vehicles, trucks, and buses at or below the standard's GVWR cutoff. Pair with 105 as the light/heavy hydraulic-electric brake split in this selection.
- **Standard No. 111; Rear visibility.** Requirements for rear visibility devices and systems. Purpose: reduce deaths and injuries when the driver lacks a clear, reasonably unobstructed view to the rear. Applies across passenger cars, multipurpose passenger vehicles, trucks, buses, school buses, motorcycles, and low-speed vehicles. Electronics relevance: rear visibility systems and rearview images (camera-based indirect vision) are regulated functions, not only mirrors.
- **Standard No. 124; Accelerator control systems.** Requirements that throttle returns to idle when the driver removes actuating force, and upon severance or disconnection in the accelerator control system. Purpose: reduce deaths and injuries from engine overspeed caused by accelerator control malfunctions. Applies to passenger cars, multipurpose passenger vehicles, trucks, and buses. Electronics relevance: electronic throttle control still owes the idle-return performance the standard states.
- **Standard No. 126; Electronic stability control systems for light vehicles.** Performance and equipment requirements for ESC on light vehicles. Purpose: reduce deaths and injuries from loss of directional control, including rollover-related crashes. Applies to passenger cars, multipurpose passenger vehicles, trucks, and buses at or below 4,536 kg (10,000 lb) GVWR per the standard's phase-in. Electronics relevance: computer-controlled yaw and brake torque modulation with required malfunction indication.
- **Standard No. 136; Electronic stability control systems for heavy vehicles.** Performance and equipment requirements for ESC on heavy vehicles. Purpose: reduce crashes from rollover or directional loss-of-control. Applies to the heavy vehicle set the standard lists (truck tractors and buses in the stated classes and exclusions). Electronics relevance: closed-loop ESC that can apply individual wheel brake torques for yaw and rollover stability on heavy platforms.
- **Standard No. 138; Tire pressure monitoring systems.** Performance requirements for TPMS that warn drivers of significant under-inflation and related safety problems. Applies to passenger cars, multipurpose passenger vehicles, trucks, and buses at or below 4,536 kg (10,000 lb) GVWR, with the dual-wheel axle exclusion and phase-in the standard states. Electronics relevance: low-pressure and TPMS-malfunction telltales (identified in coordination with Standard No. 101), detection timing, and continuity of warning while the condition lasts.
- **Standard No. 141; Minimum Sound Requirements for Hybrid and Electric Vehicles.** Performance requirements for pedestrian alert sounds. Purpose: reduce injuries from electric and hybrid vehicle crashes with pedestrians by providing sound level and sound characteristics that aid detection. Applies to electric (and hybrid, per the standard's application detail) light vehicles in the categories and GVWR band the standard states. Electronics relevance: software-defined alert sound generation is a regulated safety function for quiet powertrains.
- **Selection rule for this pack.** Standards above were pinned for electronics, software, sensing, and control relevance beside S1/S2. Other FMVSS (occupant crash protection, lighting, school bus body standards, and the rest of Subpart B) remain in force but outside this landscape chapter. FMVSS 127 is intentionally omitted per pack scope.

## Key Concepts

- **Regulation versus guidance.** Part 571 obligations are legally binding through certification and enforcement. ADS 2.0 and the cybersecurity best practices are not.
- **Subpart A is the dictionary and switchgear.** Definitions, IBR, applicability, and dates determine how every Subpart B standard is read.
- **Self-certification is the US default.** Manufacturers certify; NHTSA spot-checks and enforces. There is no VSSA-style optional public narrative that substitutes for certification.
- **Application paragraphs control scope.** Quoting a standard number without its vehicle-category and GVWR limits is incomplete.
- **Telltale language is shared infrastructure.** Standard No. 101 is how many other systems label malfunction and status lamps that drivers must recognize.
- **Brake standards split by class.** 135 covers light vehicles; 105 covers heavier hydraulic/electric applications in this selection; both aim at normal and emergency braking performance.
- **ESC is mandatory equipment with performance tests.** 126 (light) and 136 (heavy) are not advisory driver-aid descriptions; they are FMVSS equipment and performance standards.
- **Camera rear vision is regulated.** Standard No. 111 reaches rear visibility systems, not only unit mirrors.
- **Throttle fail-safe is regulated.** Standard No. 124 cares about idle return on release and on control-system severance, including electronic implementations.
- **TPMS is a timed warning duty.** Standard No. 138 sets detection and telltale behavior for under-inflation and for TPMS malfunction.
- **Quiet vehicles must still be detectable.** Standard No. 141 puts minimum pedestrian alert sound performance on hybrid and electric vehicles in scope.
- **Landscape, not reprint.** Engineers still open the current CFR (and IBR documents) for test procedures, tables, and phase-ins.

## Mental Models

- **Floor versus playbook.** FMVSS is the floor the vehicle must certify to; S1/S2 playbooks describe how organizations build electronics and ADS functions that increasingly deliver or sit beside that floor.
- **Number, title, purpose, application.** The safe four-part cite for any standard in this pack: number and title, one-line purpose, who it applies to, electronics/software hook. No section-text paste.
- **Telltale chain.** Sensors and control software detect a condition; Standard No. 101 governs how the driver-facing lamp or indicator must present; system-specific standards (126, 138, others) define when that lamp must come on.
- **Light versus heavy twins.** Brakes (135/105) and ESC (126/136) show the recurring pattern: same safety idea, different vehicle class standards.
- **Software does not escape performance standards.** Electronic throttle, ESC controllers, camera rear vision, TPMS logic, and EV alert sound synthesizers still owe the named FMVSS outcomes.

## Anti-patterns

- **Citing S1 or S2 as if they satisfied a Part 571 certification duty.** Guidance is not the standard.
- **Republishing CFR paragraphs into internal "knowledge" docs and treating them as maintained law.** This pack deliberately stays at landscape depth; the CFR moves by amendment.
- **Applying a light-vehicle standard's story to a heavy vehicle (or the reverse) without checking application and GVWR.** 105/135 and 126/136 exist as pairs for a reason.
- **Assuming mirrors alone discharge Standard No. 111 when the vehicle relies on a rear visibility system.** The standard reaches devices and systems, including camera image paths.
- **Electronic throttle designs that have no defined idle-return behavior on signal loss.** Standard No. 124's severance case remains live.
- **ESC present as a market feature but without required malfunction telltale behavior.** 126 and 136 couple equipment definitions to telltale and performance duties.
- **TPMS that warns eventually, outside the standard's timing and telltale rules.** Standard No. 138 is explicit on detection windows and malfunction indication.
- **Silent EVs in scope for Standard No. 141 without a compliant pedestrian alert sound.** Minimum sound is a safety standard, not a brand choice.
- **Treating FMVSS 127 as in-scope for this pack.** Automatic emergency braking is out of the pinned selection.
- **Ignoring Subpart A definitions when reading a Subpart B test condition.** Shared terms (vehicle categories, seating, IBR editions) live in A.

## Key Takeaways

1. 49 CFR Part 571 is binding FMVSS regulation organized as Subpart A (general) plus Subpart B (numbered standards).
2. Manufacturers self-certify applicable standards at sale; NHTSA enforces noncompliance and safety-related defects.
3. Subpart A supplies definitions, incorporation by reference, applicability, effective dates, separability, and seating designation used across standards.
4. This pack's selected Subpart B set is Standard No. 101 (Controls and displays); 105 (Hydraulic and electric brake systems); 135 (Light vehicle brake systems); 111 (Rear visibility); 124 (Accelerator control systems); 126 (Electronic stability control systems for light vehicles); 136 (Electronic stability control systems for heavy vehicles); 138 (Tire pressure monitoring systems); and 141 (Minimum Sound Requirements for Hybrid and Electric Vehicles).
5. 101 is the shared controls/telltales/indicators vocabulary many electronic warning functions must fit.
6. 105/135 split brake performance obligations across heavier and lighter vehicle classes; both target normal and emergency braking safety.
7. 126/136 require ESC equipment and performance for light and heavy classes respectively, including directional-control and rollover-related aims.
8. 111 regulates rear visibility devices and systems (including camera-based rearview image paths); 124 regulates throttle idle-return on release and on control-path failure.
9. 138 mandates TPMS under-inflation and malfunction driver warnings on in-scope light vehicles; 141 mandates pedestrian alert sound performance for in-scope hybrid and electric vehicles.
10. Use this chapter to navigate obligations; use the current CFR and its IBR documents to engineer and certify. S1/S2 guidance (ch02-ch06) does not replace any FMVSS duty.

## Connects To

- **ch01** - orientation map of which NHTSA document is guidance versus which is Part 571 regulation.
- **ch05-ch06** - ADS 2.0 voluntary elements and State roles that sit beside, not instead of, FMVSS certification.
- **ch02-ch04** - cybersecurity practices for the electronic systems that implement many of these regulated functions.
- **ch08** - functional-safety orientation when hazard analysis language appears next to regulated electronic control systems (ISO 26262 and IEC 61508 name-only).
- **automotive-signpost** / **functional-safety-signpost** - pointers for citation-only standards named alongside this regulatory landscape.
