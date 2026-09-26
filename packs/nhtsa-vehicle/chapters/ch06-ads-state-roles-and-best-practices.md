# Chapter 6: ADS State Roles and Best Practices

Sources: S2 Automated Driving Systems 2.0: A Vision for Safety (DOT HS 812 442, September 2017), Section 2: Technical Assistance to States (Federal and State roles preface, Best Practices for Legislatures, Best Practices for State Highway Safety Officials), body pp. 24-30 of `sources/text/S2.txt` (printed document pp. 18-24). Conclusion, endnotes, and back matter excluded per pin. Section 1 safety elements and VSSA are ch05. UNECE R155/R156 are not part of this US federal guidance slice (citation-only if encountered elsewhere).

## Core Idea

Section 2 is NHTSA technical assistance to States, not a second copy of the twelve safety design elements. Vehicles on public roads sit under both Federal and State jurisdiction. As States began proposing ADS statutes, public comments showed divergent approaches and asked for a more national testing and deployment frame. Section 2 answers by clarifying who regulates what, then offering best-practice components for legislatures and a framework for state highway safety officials.

The standing division of labor stays largely unchanged for ADSs. NHTSA regulates motor vehicles and motor vehicle equipment (FMVSS, compliance enforcement, defect recall, public safety communication). States regulate the human driver and most other aspects of operation (licensing, registration, traffic law, optional safety inspection, insurance and liability rules). DOT also points at FHWA infrastructure roles and FMCSA roles for interstate carriers and commercial drivers. The Agency's consistent request: States should not codify the Voluntary Guidance into state statute as a legal design requirement, and should leave safety design and performance regulation of ADS technology to DOT/NHTSA so Federal and State rules do not collide and block deployment.

Consistency across States is the practical goal, not identical text in every code. Enough alignment to support innovation and safe integration matters more than uniform statutes. States should also keep infrastructure and traffic-control device quality aligned with the Manual on Uniform Traffic Control Devices (MUTCD) and work with FHWA and AASHTO as machine vision raises the cost of "low priority" markings and signs that human drivers could forgive.

## Frameworks Introduced

- **Do not codify the Voluntary Guidance as state design law (Federal/State roles preface).** NHTSA strongly encourages States not to write Section 1 into statutes as a requirement for development, testing, or deployment phases. Leaving safety design and performance to NHTSA avoids conflicting rules.
- **Federal versus State regulatory roles (roles table).** NHTSA: set FMVSS for new vehicles and equipment; enforce FMVSS compliance; investigate and manage recall/remedy of noncompliances and safety-related defects nationwide; communicate and educate on motor vehicle safety. States: license human drivers and register vehicles; enact and enforce traffic laws; conduct safety inspections where the State chooses; regulate motor vehicle insurance and liability. If a State still pursues ADS performance-related regulations, consult NHTSA.
- **Related DOT lanes.** FHWA: safety, evaluation, planning, and maintenance of infrastructure. FMCSA: safe operation of interstate motor carriers and commercial drivers, plus registration and insurance requirements in that domain.
- **Legislative best practice: technology-neutral environment.** Do not confine ADS testing or deployment to traditional motor vehicle manufacturers only. Manufacturing pedigree is not treated as a safety proxy; any entity that meets Federal and State prerequisites should be able to operate.
- **Legislative best practice: licensing and registration procedures.** Define "motor vehicle" under ADS laws to cover vehicles on state roads; license ADS entities and test operators; register ADS-equipped vehicles; establish proof of financial responsibility (surety bond or self-insurance patterns named). Goal: same class of records States already keep for conventional vehicles, improved for ADS operation.
- **Legislative best practice: public safety reporting and communications.** Create paths so entities coordinate with public safety agencies; improve understanding among officials, other road users, and ADS passengers; define procedures for reporting crashes and roadway incidents involving ADSs to law enforcement and first responders.
- **Legislative best practice: scrub traffic-law barriers.** Review vehicle codes and traffic rules that unintentionally block ADS testing or deployment (example named: a permanent one-hand-on-wheel rule that collides with Levels 3-5 operation).
- **State highway safety official framework (seven topic blocks).** Assistance for States that want structure, not a mandate to create new bureaucracy. NHTSA does not expect every State to invent new entities; the list is guidance for States that choose to adapt existing processes.
- **Administrative structure (block 1).** Optional patterns: designate a lead agency for ADS testing deliberation; consider a jurisdictional ADS technology committee spanning governor's office, motor vehicle administration, DOT, law enforcement, SHSO, IT, insurance regulator, aging/disability offices, toll/trucking/bus/transit authorities; keep the committee informed of test requests and responses; examine statutes for unnecessary barriers; consider an internal test-application process and test-vehicle permit process.
- **Application to test on public roads (block 2).** Prefer State-level applications (local only if the State so chooses, with the same considerations). Request entity identity and contacts; identify each ADS test vehicle (VIN, type, or year/make/model); identify each test operator and license data; optionally take a safety and compliance plan, evidence of ability to satisfy injury/death/property judgments (insurance, surety, or self-insurance), and a summary of test-operator training.
- **Permission to test (block 3).** Involve law enforcement before answering applications; suspend permission when insurance or driver requirements fail; allow requests for more information or application modification; notify entities of permission and consider requiring proof of permission to be carried in test vehicles.
- **Test drivers and operations (block 4).** States may request training summaries; test drivers follow traffic rules and crash-reporting duties; licensed human drivers remain necessary for less-than-full automation (SAE Levels 3 and lower) with duty to operate, monitor, or be immediately available on request or disengagement; fully automated operation (SAE Levels 4 and 5 under specified conditions) performs the driving task without a licensed human driver in those conditions.
- **Registration and titling (block 5).** Consider identifying ADS capability on title and registration (all ADSs, or only those that can operate without a human driver); consider notice when a vehicle is significantly upgraded with ADS capability after sale, with forms updated to match.
- **Public safety officials (block 6).** Train officials as deployments arrive; coordinate across States on monitoring how human driver behavior changes around ADS-controlled vehicles.
- **Liability and insurance (block 7).** Begin allocating crash liability among owners, operators, passengers, manufacturers, and other entities; decide who must carry insurance in which roles; begin rules for tort liability. These questions need scenario work and use-case knowledge (personal, rental, ridehail, corporate). Who was "the operator" at a moment may not alone settle liability.

## Key Concepts

- **Two sovereign layers, one roadway.** Federal equipment rules and State operation rules both apply; Section 2 keeps that split visible for ADSs.
- **Design performance is Federal.** States regulating ADS performance risk conflict; consultation with NHTSA is the named escape hatch if they proceed anyway.
- **Guidance is not for codification.** Writing ADS 2.0 Section 1 into state law as a design mandate is the anti-pattern the preface calls out.
- **Consistency over cloning.** States should read each other's drafts and aim for interoperable enough rules, not word-identical codes.
- **Infrastructure is part of ADS readiness.** MUTCD adherence and marking/sign quality matter more as machine perception replaces forgiving human vision.
- **Technology neutrality.** Non-OEM entities that meet prerequisites are in scope for testing and deployment permission structures.
- **Recordkeeping parity.** ADS licensing, registration, and financial responsibility should produce information comparable to conventional fleets.
- **Applications are optional tools.** NHTSA sketches application and permit content for States that want them; it does not order every State to stand up a new agency.
- **Level-dependent driver duty.** Lower automation keeps a licensed human in the loop; Level 4/5 conditional full automation shifts the driving operation to the system in its conditions.
- **Liability is unfinished business.** Section 2 flags allocation and insurance questions as work States should begin, not as settled federal answers.

## Mental Models

- **Equipment versus driver.** If the question is "is the vehicle acceptably designed," start with NHTSA/FMVSS/defect. If the question is "who may operate, on which roads, under which traffic rules, with which insurance," start with the State.
- **Assistance, not preemption theater.** Section 2 helps States write their own rules without turning the Voluntary Guidance into fifty divergent design codes.
- **Lead agency as switchboard.** A designated lead and optional multi-agency committee exist to route test requests, not to re-run Federal design approval.
- **Permission is operational, not type approval.** State test permission tracks identity, insurance, operators, and reporting; it is not a substitute for the entity's safety design process in ch05.
- **Train the humans around the machine.** Public safety training and consumer-facing clarity (ch05 element 11) are the State-facing complements to vehicle design elements.

## Anti-patterns

- **Copy-pasting ADS 2.0 safety elements into state criminal or traffic codes as design mandates.** Preface says not to codify the Voluntary Guidance that way.
- **State ADS "performance standards" drafted without NHTSA consultation.** Roles section asks States that go there to consult the Agency.
- **OEM-only testing statutes.** Technology-neutrality practice rejects manufacturer-only gates without safety basis.
- **Silent one-hand-on-wheel or similar rules left in force against Level 3-5 operation.** Barrier review is an explicit legislature practice.
- **No crash/incident reporting path from ADS entities to first responders.** Public safety communications practice exists to close that gap.
- **Local patchwork of incompatible test-permit regimes with no State coordination.** Framework prefers State-level application/permission, with local only as a deliberate choice carrying the same considerations.
- **Permission without insurance or driver-requirement teeth.** Suspension on those failures is called out as appropriate.
- **Assuming a licensed driver is always required, including for Level 4/5 operation under its conditions.** Block 4 separates those cases.
- **Titles and registrations that cannot show ADS capability or post-sale upgrades.** Block 5 exists because responders and records systems need the flag.
- **Deferring all liability and insurance questions indefinitely.** Block 7 tells States to begin allocation and coverage rules even while facts are still moving.

## Key Takeaways

1. Section 2 assists States; it does not replace Section 1's twelve safety elements or create Federal type approval.
2. NHTSA keeps motor vehicle and equipment safety design, FMVSS, compliance, and defect recall; States keep driver licensing, registration, traffic law, optional inspection, insurance, and liability.
3. States should not codify the Voluntary Guidance as a legal design requirement; conflicting State performance rules can impede deployment.
4. Aim for cross-State consistency sufficient for safe innovation, not necessarily identical statutes; review peer State drafts.
5. Legislature practices: stay technology-neutral; license and register ADS entities and vehicles with financial responsibility proof; build public-safety reporting channels; remove unintentional traffic-law barriers.
6. Highway safety official framework covers administration, test applications, permission, test-driver rules, titling/registration flags, public-safety training, and liability/insurance starters.
7. Test applications, when used, identify the entity, vehicles, and operators, and may include safety plans, judgment-satisfaction evidence, and operator training summaries.
8. Licensed human drivers remain central at SAE Levels 3 and lower; Level 4/5 operation under specified conditions can proceed without a licensed human driver performing the driving task.
9. MUTCD-aligned infrastructure and continued FHWA/AASHTO work support both ADS and remaining human drivers.
10. Liability allocation and compulsory insurance roles are acknowledged open State work items that depend on use case and control facts, not on a single federal formula in this document.

## Connects To

- **ch01** - document map: when a question is State operation versus Federal equipment guidance or FMVSS.
- **ch05** - Section 1 safety design elements, ODD/OEDR/MRC, and VSSA that entities still own regardless of State permit structure.
- **ch07** - FMVSS and Part 571 self-certification duties that remain Federal even when States regulate drivers and insurance.
- **ch02-ch04** - cybersecurity programme expectations that travel with the vehicle across state lines.
- **automotive-signpost** - citation-only industry designations named in ADS material when taxonomy or practice standards appear.
