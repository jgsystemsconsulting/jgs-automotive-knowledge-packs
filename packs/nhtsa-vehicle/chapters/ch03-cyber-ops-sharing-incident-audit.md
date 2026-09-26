# Chapter 3: Cyber Ops, Sharing, Incident, and Audit

Sources: S1 Cybersecurity Best Practices for the Safety of Modern Vehicles, Updated 2022 (NHTSA final; 87 FR 55459; docket NHTSA-2020-0087; pub. 15745-090822-v2a), secs 4.3-7 (Information Sharing, Security Vulnerability Reporting Program, Organizational Incident Response Process, Self-Auditing, Education, Aftermarket/User-Owned Devices, Serviceability), body pp. 12-16 of `sources/text/S1.txt` (printed PDF pp. 8-12). Practices in this slice: [G.25]-[G.45]. Development-process practices [G.2]-[G.24] are ch02; technical practices [T.x] are ch04. ISO/SAE 21434 and related standards appear as name citations only.

## Core Idea

Once leadership and the development process exist (ch02), S1 turns to how the organization operates cybersecurity after products leave the design desk. The operating loop has four named process blocks: share intelligence through Auto-ISAC, run a public-facing vulnerability reporting programme, respond to incidents with a documented plan, and self-audit the paperwork and the practice. Around those blocks sit education, aftermarket and user-owned devices, and serviceability. The common theme is lifecycle duty: a vehicle remains on the road for more than a decade, so post-production operation is part of the cybersecurity programme, not an optional extra.

## Frameworks Introduced

- **Auto-ISAC information sharing (4.3, [G.25]-[G.26]).** NHTSA encouraged formation of the Automotive Information Sharing and Analysis Center under the private-sector sharing policy in EO 13691. Extended industry members (OEMs, suppliers, software developers, communication providers, aftermarket suppliers, fleet managers, and peers) are strongly encouraged to join Auto-ISAC and to share timely vulnerability and intelligence information. Auto-ISAC members should collaborate on containment and countermeasures for reported issues even when their own products are not yet hit.
- **Vulnerability reporting programme (4.4, [G.27]).** Industry members should publish their own vulnerability reporting policies and mechanisms so security researchers and the public can report findings confidentially and with clear triage expectations.
- **Product cybersecurity incident response process (4.5, [G.28]-[G.34]).** Build a response process that includes a documented plan, named internal roles, external communication channels and contacts, and procedures that keep those three current. Add effectiveness metrics, per-incident documentation, vulnerability nature and management rationale, and a risk-commensurate plan for consumer-owned field vehicles, built-but-not-shipped stock, dealer inventory, and future products. Report incidents to CISA/US-CERT per federal notification guidelines. Run and join organized cyber incident response exercises and revise the process from lessons learned. Restated participation in Auto-ISAC sharing sits beside these duties.
- **Self-auditing via process documentation and review (4.6, [G.35]-[G.39]).** Document the vehicle cybersecurity risk management process so it can be audited. Retain those documents for the expected product lifespan. Keep them under version control and revise them as new information arrives. Establish internal review procedures for cybersecurity management and documentation. Consider annual organizational and product cybersecurity audits; a public version of audit reports can show commitment to stakeholders and consumers.
- **Workforce education (sec 5, [G.40]).** Vehicle manufacturers, suppliers, universities, and other stakeholders should support educational efforts that build the automotive cybersecurity workforce.
- **Aftermarket and user-owned devices (sec 6, [G.41]-[G.43]).** Vehicle manufacturers should account for risks from user-owned or aftermarket devices connected to vehicle systems and provide reasonable protections; third-party connections should be authenticated and given limited access. Aftermarket device manufacturers should put strong cybersecurity protections on their own products because those devices attach to cyber-physical systems that can affect safety of life, even when the device's primary purpose is not safety.
- **Serviceability without gutting cybersecurity (sec 7, [G.44]-[G.45]).** Consider serviceability of components and systems by individuals and third parties. Provide strong cybersecurity protections that do not unduly restrict access by alternative third-party repair services the owner authorizes. Cybersecurity is not a justification for locking out serviceability; serviceability is not a justification for weak cybersecurity.

## Key Concepts

- **Extended industry, not OEM-only.** [G.25] lists vehicle manufacturers, equipment suppliers, software developers, communication service providers, aftermarket system suppliers, and fleet managers among the parties encouraged to join and share.
- **Share even when you are not the victim yet.** [G.26] pushes Auto-ISAC members to work containment options for reported vulnerabilities regardless of immediate impact on their own systems.
- **Reporting path is an asset.** [G.27] expects written policies and mechanisms so external researchers know how to report without theatre or dead ends.
- **Incident response is a four-part minimum.** [G.28] requires plan, roles, external contacts, and keep-current procedures for those three.
- **Metrics and records close the loop.** [G.29]-[G.31] add periodic effectiveness metrics, per-event documentation, and written rationale for how each vulnerability is managed.
- **Field population is segmented.** [G.32] plans coverage for consumer-owned vehicles, factory inventory, dealer inventory, and future products, scaled to assessed risk. Applying known remedies even when a flaw is not yet judged safety-critical on its own is called out as good practice.
- **Federal incident notification.** [G.33] points incidents to CISA/US-CERT under the US-CERT Federal Incident Notification Guidelines.
- **Exercises are required practice, not theatre.** [G.34] uses organized exercises to test disclosure operations and response processes and to drive revisions.
- **Documentation enables audit.** [G.35]-[G.37] bind risk-management process detail, lifespan retention, and version control together.
- **Internal review plus optional annual audit.** [G.38]-[G.39] separate routine internal review from the stronger step of annual organizational and product audits, with public summary reports as a transparency option.
- **Education is a multi-party duty.** [G.40] names manufacturers, suppliers, universities, and other stakeholders together.
- **Two sides of the aftermarket interface.** Vehicle makers protect the vehicle side ([G.41]-[G.42]); aftermarket makers harden the device side ([G.43]).
- **Serviceability-cybersecurity balance.** [G.44]-[G.45] refuse both "cyber means no third-party repair" and "repair access means weak controls."

## Mental Models

- **Ops is half the programme.** Design-time [G.3]-[G.15] work fails open if sharing, reporting, response, and audit never run.
- **Auto-ISAC is the sector nervous system.** Membership without timely sharing is an empty seat; sharing without joint containment still leaves peers exposed.
- **Every vulnerability has a written fate.** Intake, nature, disposition, and rationale are one record chain, not hallway memory.
- **Inventory classes differ by custody.** Field, factory, dealer, and future product stock need distinct response plans even for one CVE.
- **Exercise finds the broken phone tree.** Paper plans that never rehearse fail at first contact.
- **Audit reads the versioned file, not the slide.** Self-audit assumes the risk-management process was written, retained, and controlled.
- **Aftermarket is an untrusted peer on a safety-capable bus.** Authenticate and limit; do not assume the dongle is benign because the driver paid for it.
- **Repair access and cyber controls co-design.** Owner-authorized third-party service is in scope; so is keeping protections strong.

## Anti-patterns

- **Sitting outside Auto-ISAC while consuming others' alerts.** [G.25]-[G.26] push join-and-share, plus collaborative containment.
- **No published vulnerability reporting channel.** Researchers then dump findings publicly or go silent; [G.27] wants policy and mechanism.
- **Incident "process" that is only a distribution list.** Missing plan, roles, external contacts, or keep-current procedures breaks [G.28].
- **No metrics, no per-incident file, no management rationale.** [G.29]-[G.31] treat those as part of the process, not paperwork afterthoughts.
- **Patch plan that covers only next model year.** [G.32] explicitly includes consumer-owned field vehicles and dealer/factory stock.
- **Never reporting to CISA/US-CERT when the guidelines apply.** [G.33] is a named external reporting duty.
- **Skipping exercises because the plan "looks complete."** [G.34] uses exercises to find and fix process gaps.
- **Undocumented risk-management process, or documents discarded at end of production.** [G.35]-[G.36] require detail and lifespan retention.
- **Documents without version control or refresh.** [G.37] couples control protocol with regular revision.
- **No internal review of cybersecurity management activity.** [G.38] makes review a standing procedure.
- **Open OBD or app interfaces to aftermarket devices with no authentication or scope limit.** [G.41]-[G.42] reject open trust.
- **Aftermarket device shipped with weak protections because "we only collect telematics."** [G.43] notes non-safety primary purpose still sits on a safety-capable architecture.
- **Using cybersecurity as the reason to block owner-authorized third-party repair, or gutting controls to make repair easy.** [G.45] rejects both extremes.

## Key Takeaways

1. Post-production cybersecurity is a named S1 duty: share, accept reports, respond, audit, educate, handle aftermarket risk, and keep vehicles serviceable.
2. Extended industry members should join Auto-ISAC and share timely vulnerability and intelligence information ([G.25]); members should help contain issues even when not yet impacted ([G.26]).
3. Each organization needs its own vulnerability reporting policies and mechanisms ([G.27]).
4. Incident response requires a documented plan, roles, external contacts, keep-current procedures, metrics, per-event records, management rationale, multi-population fix plans, CISA/US-CERT reporting, and periodic exercises ([G.28]-[G.34]).
5. Self-audit rests on documented, retained, version-controlled risk-management process records, internal review procedures, and consideration of annual organizational and product audits ([G.35]-[G.39]).
6. Manufacturers, suppliers, universities, and peers share responsibility for automotive cybersecurity workforce education ([G.40]).
7. Vehicle makers must reason about aftermarket and user-owned device risk, authenticate third-party connections, and limit access ([G.41]-[G.42]); aftermarket makers must harden their devices ([G.43]).
8. Strong cybersecurity and owner-authorized third-party serviceability are co-constraints, not trade-offs that erase either side ([G.44]-[G.45]).

## Connects To

- **ch02** - leadership, development process, risk, inventory, testing, and monitoring foundations these operating practices assume.
- **ch04** - technical controls (diagnostics, wireless paths, update integrity) that incident response and aftermarket protections rely on.
- **ch01** - orientation on which NHTSA document answers process versus regulatory questions.
- **ch05** - ADS safety design elements that still need vulnerability handling and incident response when automation is present.
- **automotive-signpost** - ISO/SAE 21434 and related designations S1 footnotes name beside these process practices.
