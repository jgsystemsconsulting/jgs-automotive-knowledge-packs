# Chapter 5: ADS Taxonomy and Safety Elements

Sources: S2 Automated Driving Systems 2.0: A Vision for Safety (DOT HS 812 442, September 2017), Section 1: Voluntary Guidance (Overview, Scope and Purpose, NHTSA enforcement authority note, SAE automation levels as adopted, 12 ADS safety design elements, Voluntary Safety Self-Assessment), body pp. 7-22 of `sources/text/S2.txt` (printed document pp. 1-16). Cover, intro, executive summary, and ToC pp. 1-6 excluded per pin. Section 2 (Federal/State roles) is ch06. SAE J3016 and ISO functional-safety process standards appear as name citations only; UNECE R155/R156 are not in this source slice (citation-only if named elsewhere).

## Core Idea

ADS 2.0 Section 1 is voluntary guidance, not a regulation and not an approval regime. NHTSA wrote it to help entities that design, supply, test, sell, operate, or deploy Automated Driving Systems (ADSs) analyze safety before public-road use. The document updates the September 2016 Federal Automated Vehicles Policy and remains the Agency's operating guidance for ADSs in this pinned edition. It focuses on SAE Automation Levels 3 through 5: systems that can take the driving task for a period of time, including designs with no human driver expected to perform driving-related tasks while the ADS is engaged.

The spine of Section 1 is twelve priority safety design elements drawn from TRB, university, and NHTSA research. For each element, entities are encouraged to document a process for assessment, testing, and validation, and to record how industry standards, company policy, or other methods address the risks inside the declared operating envelope. No single pass/fail metric is prescribed; entities may innovate on method so long as safety risk is addressed. The Voluntary Safety Self-Assessment (VSSA) is the public receipt for that work: encouraged, not required, not subject to Federal approval, and not a gate that must delay testing or deployment.

NHTSA's defect, recall, and enforcement authority still reaches motor vehicles and motor vehicle equipment that include ADSs. Interstate CMV driver and carrier operations sit with FMCSA and are out of this Guidance's scope unless a separate FMCSA waiver or exemption path applies. Taxonomy consistency comes from adopting SAE International's levels of automation and related terms rather than inventing a parallel ladder.

## Frameworks Introduced

- **Voluntary Guidance for ADSs (Section 1 Overview / Scope and Purpose).** Non-binding recommendations for design, development, testing, and deployment on US public roadways. Applies to traditional manufacturers and to other entities that outfit, operate, or offer services with ADS technology, across vehicle classes under NHTSA jurisdiction (low-speed through heavy CMVs as equipment). Recommendations cover original ADS equipment and replacement equipment or software updates.
- **SAE automation levels as adopted (Levels graphic and taxonomy note).** NHTSA adopts SAE International's levels rather than writing a separate scale. The Guidance targets Levels 3-5 (Conditional, High, Full Automation). Level determination is the entity's responsibility against SAE's published definitions. Levels 0-2 remain driver-performed or driver-supervised assistance context in the adopted chart, outside the ADS focus of this section.
- **Twelve priority safety design elements (elements 1-12).** The Agency's consensus checklist of salient design aspects. Source order, retained here: (1) System Safety; (2) Operational Design Domain; (3) Object and Event Detection and Response; (4) Fallback (Minimal Risk Condition); (5) Validation Methods; (6) Human Machine Interface; (7) Vehicle Cybersecurity; (8) Crashworthiness; (9) Post-Crash ADS Behavior; (10) Data Recording; (11) Consumer Education and Training; (12) Federal, State, and Local Laws.
- **Documented process habit across elements.** For each element, entities are encouraged to define how they assess, test, and validate the related functions, and to keep design choices, analyses, tests, and data traceable.
- **Operational Design Domain (ODD) as the capability boundary (element 2).** Document where and when each ADS or feature is intended to function (roadway types, geography, speed range, environment, other constraints). Safe operation is expected inside the ODD; exit or dynamic loss of ODD should drive transition toward a minimal risk condition.
- **Object and Event Detection and Response (OEDR) (element 3).** While engaged inside its ODD, the ADS performs detection of driving-task-relevant circumstances and the appropriate response. Covers other road users and objects, foreseeable unusual conditions (emergency vehicles, work zones, manual traffic control), normal-driving behavioral competencies, and crash-avoidance performance against applicable pre-crash scenario classes tied to the ODD.
- **Fallback / minimal risk condition (MRC) (element 4).** Detect malfunction, degradation, or ODD exit; notify a human driver when handback is the path, or achieve MRC without driver intervention at higher automation when no driver is available. MRC varies by failure (often a controlled stop outside an active lane when feasible). Design for inattentive or impaired humans despite contrary rules.
- **Validation methods (element 5).** Entity-defined mix of simulation, test track, and on-road testing sized to the ADS approach. Demonstrate normal behavioral competencies, crash avoidance, and fallback strategies relevant to the ODD. Prefer adequate simulation and track work before on-road testing; first-party or independent third-party testing both fit. Continue work with NHTSA and standards bodies on tests and facility criteria.
- **Human Machine Interface (element 6).** Design and validate HMI for drivers, operators, occupants, and external actors (other vehicles, motorcyclists, bicyclists, pedestrians). At minimum, indicate proper function, ADS engagement, unavailability, malfunction, and requests to take control. Consider driver-engagement monitoring where a human may be asked to resume. Support accessibility when driver controls are absent; support remote dispatcher status when the vehicle may be unoccupied.
- **Vehicle cybersecurity as an ADS element (element 7).** Systems-engineering product development with ongoing safety risk assessment that includes cyber threats; incorporate established vehicle cyber-physical best practices (NIST, NHTSA, SAE International, Auto-ISAC, and peer industry groups named as sources of voluntary practice). Document cyber design choices under version control; share incidents and vulnerabilities with Auto-ISAC promptly; maintain incident response plans and coordinated vulnerability disclosure policy. Detailed [G.x] and [T.x] controls live in ch02-ch04 (S1); this element is the ADS 2.0 cross-link.
- **Crashworthiness for mixed fleets (element 8).** Occupant protection must hold its intended performance whether the ADS or a human is driving. Consider using ADS sensing to improve protection across occupant sizes and alternative seating or interior layouts. Unoccupied ADS vehicles still need geometric and energy-absorption compatibility with the existing fleet and with vulnerable road users.
- **Post-crash ADS behavior (element 9).** After a crash, return the ADS to a safe state (examples named in source: fuel shutoff, remove motive power, move off the roadway when feasible, disengage electrical power). Share relevant data with operations or notification centers when those links exist. Keep repair and return-to-service documentation that identifies equipment and processes needed before the ADS is fielded again.
- **Data recording for learning and reconstruction (element 10).** Documented process to collect malfunction, degradation, and failure data usable for crash cause analysis during testing and use. For fatal/injury crashes and tow-away or immobilization damage, collect data that supports reconstruction, including ADS status and whether the ADS or human was in control before, during, and after the event. Preserve retrieval capability consistent with event data recorder practice and applicable privacy rules; retain technical and legal ability to share with authorities for reconstruction. Work toward uniform elements with SAE International; no standard ADS crash data element set existed at publication.
- **Consumer education and training (element 11).** Maintain programs for employees, dealers, distributors, and consumers covering functional intent, limits, engagement methods, HMI, fallback scenarios, ODD parameters, and in-service behavior changes. State clearly what the ADS can and cannot do. Ensure marketing and sales staff can train the chain. Prefer on-road or on-track experience before consumer release where practical; evaluate program effectiveness and update from feedback.
- **Federal, State, and local laws in design (element 12).** Document how the ADS accounts for applicable law inside its ODD while in automated mode. Testing may rely on a test driver or other mechanism for compliance management. Design for foreseeable safety-critical situations where temporary departure from a nominal rule (example pattern in source: crossing double lines to pass a disabled vehicle) is the safe path; keep independent assessment of those scenarios. Plan processes to adapt the ADS when laws change.
- **Voluntary Safety Self-Assessment (VSSA).** Optional public demonstration that the entity considered the safety elements (or marked an element not applicable), without dumping proprietary detail or every engineering action. May follow NHTSA's illustrative template or vary when information is limited. Must not contain confidential business information if published. Not submitted for approval; not compulsory; not a delay requirement.

## Key Concepts

- **Guidance is voluntary.** Section 1 creates no compliance obligation and no enforcement mechanism of its own; defect authority under existing law is separate.
- **Entity set is broad.** "Entities" includes manufacturers, suppliers, modifiers, fleet and transit operators, driverless service providers, and others offering ADS services.
- **Levels 3-5 are the ADS focus.** Lower automation remains relevant context on the SAE chart but is not the primary subject of the twelve elements.
- **ODD bounds claims.** An ADS is evaluated against the domain it declares, not against unbounded "drives anywhere" rhetoric.
- **OEDR is the ADS's job while engaged.** Detection and response load shifts to the system inside the ODD for the Guidance's ADS definition.
- **MRC is the safety net.** Malfunction, degradation, and ODD exit are expected design cases, not only rare faults.
- **Validation is multi-modal.** Simulation, track, and road each cover different risk; entities size the mix to their approach.
- **HMI is multi-audience.** Internal handback cues and external communication both matter; unoccupied and accessible designs are in scope.
- **Cyber is an ADS safety element.** ADS 2.0 points at the same industry sharing and systems-engineering posture developed further in S1 (ch02-ch04).
- **Crashworthiness does not retire with automation.** Mixed fleets and unoccupied vehicles keep compatibility and occupant protection live.
- **Data enables industry learning.** One crash reconstructed well can prevent repeats across other ADSs.
- **Education fights misuse.** Explicit capability and limitation teaching is part of the safety case, not marketing garnish.
- **Law is a design input.** Traffic law inside the ODD, including hard edge cases, belongs in the documented process.
- **VSSA is transparency, not type approval.** Publishing how elements were considered builds trust; withholding CBI is expected; Federal sign-off is not part of the instrument.

## Mental Models

- **Checklist plus envelope.** The twelve elements are the checklist; the ODD is the envelope that sizes every other element.
- **Process over single test number.** ADS 2.0 asks for a documented, traceable method per element because no universal metric existed at publication.
- **Handback versus self-MRC.** Level 3 paths often transfer to a receptive fallback-ready user; higher automation must reach MRC without that user.
- **OEDR splits normal and crash.** Behavioral competency (lane, law, etiquette) and pre-crash scenario handling are both required design threads.
- **Public receipt, private method.** VSSA shows consideration of elements; detailed trade secrets stay inside the company process.
- **Taxonomy borrowed, not rewritten.** SAE levels are adopted for shared language with industry and States; do not invent parallel level names in this pack.
- **Guidance beside regulation.** Section 1 recommends; FMVSS (ch07) and defect law still bind. Confusing the two is a category error.

## Anti-patterns

- **Treating ADS 2.0 as a binding standard or type-approval file.** It is voluntary guidance; VSSA is not Federal approval.
- **Declaring Level 4/5 marketing while designing only Level 2 driver supervision.** Level claims must track SAE definitions the entity itself applies.
- **Unbounded ODD language ("handles all roads") with no documented limits or ODD-exit MRC path.** Element 2 expects defined boundaries and transition behavior.
- **OEDR that tracks lane paint but ignores work zones, emergency vehicles, or manual traffic direction.** Foreseeable unusual conditions are in the element text.
- **Fallback that assumes a perfectly attentive human.** Element 4 explicitly designs for inattention, impairment, and non-receptive users.
- **On-road testing as the first serious validation step.** Element 5 pushes simulation and track consideration before public-road exposure.
- **HMI that only shows "Auto On" with no malfunction, unavailability, or handback request cues.** The minimum indicator set is explicit.
- **Cyber treated as an IT afterthought outside the ADS safety case.** Element 7 puts systems-engineering risk assessment, Auto-ISAC reporting, and disclosure policy inside the ADS element list.
- **Occupant protection assumed irrelevant because "the ADS will not crash."** Element 8 requires performance when another vehicle strikes the ADS vehicle, human- or ADS-driven.
- **No post-crash safe state or return-to-service criteria.** Element 9 expects immediate safe-state methods and repair documentation.
- **No recoverable record of who or what was in control around a crash.** Element 10 makes control status and reconstruction data first-class.
- **Sales narratives that overstate capability relative to training content.** Element 11 wants explicit can/cannot teaching and trained dealer/sales staff.
- **Design that cannot handle lawful edge maneuvers or cannot be updated when statutes change.** Element 12 expects both.

## Key Takeaways

1. ADS 2.0 Section 1 is voluntary NHTSA guidance for ADS design, testing, and deployment; it is not itself a regulation or approval process.
2. Scope centers on SAE Levels 3-5 as adopted from SAE International; entities classify their own systems against SAE definitions.
3. The twelve safety design elements in source order are System Safety; Operational Design Domain; Object and Event Detection and Response; Fallback (Minimal Risk Condition); Validation Methods; Human Machine Interface; Vehicle Cybersecurity; Crashworthiness; Post-Crash ADS Behavior; Data Recording; Consumer Education and Training; and Federal, State, and Local Laws.
4. Recurring habits across elements: document the process, validate inside the declared ODD, and provide malfunction/ODD-exit paths toward a minimal risk condition (without driver intervention when no driver is available).
5. OEDR while engaged covers other road users, foreseeable unusual roadway conditions, normal behavioral competencies, and ODD-relevant crash-avoidance scenarios.
6. Validation should combine simulation, track, and on-road methods sized to the ADS, with serious non-public testing considered before on-road work.
7. HMI minimum cues cover function, engagement, unavailability, malfunction, and control-transfer requests; unoccupied and accessible designs remain in scope.
8. Vehicle cybersecurity in ADS 2.0 aligns with systems engineering, industry best-practice sources, Auto-ISAC sharing, incident response, and coordinated disclosure; detailed controls are in S1 (ch02-ch04).
9. Crashworthiness, post-crash safe state, and reconstruction-grade data recording keep mixed-fleet and learning-system duties alive after automation is added.
10. The VSSA is an encouraged public acknowledgment that each applicable element was considered (or marked not applicable); it is optional, not approved by NHTSA, and must not publish CBI.

## Connects To

- **ch01** - which NHTSA document answers which question; guidance versus FMVSS duty.
- **ch02-ch04** - S1 cybersecurity process and technical controls that implement ADS element 7 in depth.
- **ch06** - Section 2 Federal/State role split, legislature practices, and state highway safety official framework.
- **ch07** - FMVSS self-certification landscape that remains binding beside this voluntary ADS checklist.
- **ch08** - functional-safety orientation when System Safety points at road-vehicle functional-safety process standards (ISO 26262 and related names at citation depth only).
- **automotive-signpost** - SAE J3016 and other paywalled or citation-only designations named for taxonomy and practice.
- **functional-safety-signpost** - IEC 61508 / ISO 26262 pointer routing when system-safety process standards are named.
