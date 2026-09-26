# Chapter 2: Cyber Process and Leadership

Sources: S1 Cybersecurity Best Practices for the Safety of Modern Vehicles, Updated 2022 (NHTSA final; 87 FR 55459; docket NHTSA-2020-0087; pub. 15745-090822-v2a), secs 1-4.2 (Purpose, Scope, Background, General Cybersecurity Best Practices through 4.2.11), body pp. 5-11 of `sources/text/S1.txt` (printed PDF pp. 1-7). Practices in this slice: opening NIST CSF practice labeled [G.18] in sec 4 intro; [G.2]-[G.17]; second [G.18] in 4.2.9; [G.19]-[G.24]. Technical practices [T.x] begin in ch04. ISO/SAE 21434 and Auto-ISAC guides appear as name citations only.

## Core Idea

S1 is non-binding voluntary guidance. NHTSA updates the 2016 practices so industry can decide whether and how to apply them to its own systems. Vehicles are cyber-physical systems; cybersecurity faults can become safety faults. The agency's focus is strengthening electronic architecture so systems stay safe even when an attack partly succeeds. A layered approach assumes some systems can be compromised, lowers the chance a compromise escalates, and limits the damage when it does.

Scope covers all motor vehicles and motor vehicle equipment, including software. It binds no one by force of law, but it applies to every designer, supplier, manufacturer, modifier, and alterer in the chain. Implementation will differ by size and tier; the security of a system is still measured by its weakest link. Organizations should set clear cybersecurity expectations for suppliers that match these practices and then verify those expectations are met.

Background places the 2022 text on top of the 2016 guidance, Auto-ISAC membership growth, Auto-ISAC best-practice guides, and emerging voluntary standards such as ISO/SAE 21434 (named only). The general block that follows is the management system: leadership, development process, risk, inventory, testing, monitoring, documentation, continuous reassessment, and industry participation. The [T.x] technical controls in ch04 sit on top of that system; they do not replace it.

## Frameworks Introduced

- **Voluntary, non-binding best practices (secs 1-2).** S1 updates NHTSA guidance for motor vehicle cybersecurity. Manufacturers review it and choose how to apply it; it is not a regulation and creates no independent legal duty on its own.
- **Layered cybersecurity with compromise assumed (sec 4 intro).** Design as if some vehicle systems can be reached by an attacker. Reduce success probability and contain unauthorized access rather than betting on a single hard perimeter.
- **NIST Cybersecurity Framework as the industry scaffold (sec 4 intro [G.18]).** Build vehicle protections around Identify, Protect, Detect, Respond, and Recover. Prioritize safety-critical controls, remove risk where feasible, detect and respond in the field, recover quickly, and push lessons across industry through sharing such as Auto-ISAC.
- **Leadership priority on product cybersecurity (4.1, [G.2]).** Executive commitment shows up as dedicated cyber resources, direct communication paths up the ranks, and an independent cyber voice inside the vehicle safety design process. One concrete form is a high-level officer with staff, authority, and budget for product cybersecurity.
- **Systems-engineering development process with cyber in scope (4.2.1, [G.3]).** Run a product development process aimed at systems free of unreasonable safety risk, including risk from cybersecurity threats and vulnerabilities.
- **Lifecycle cybersecurity risk assessment (4.2.2, [G.4]-[G.5]).** Include a risk assessment step sized to the vehicle's full lifecycle. Treat safety of occupants and other road users as the primary consideration when ranking risks.
- **Sensor vulnerability and signal integrity (4.2.3, [G.6]).** Account for sensor attack classes the guidance names: GPS spoofing, road-sign modification, lidar/radar jamming and spoofing, camera blinding, and machine-learning false positives.
- **Remove or mitigate safety-critical risk; layer residual risk (4.2.4-4.2.5, [G.7]-[G.9]).** Design out unreasonable risk to safety-critical systems; drop avoidable risky functions where possible. Put remaining function behind risk-appropriate layers of protection, and state clear cybersecurity expectations to the suppliers that implement those layers.
- **Hardware/software inventory and component detail (4.2.6, [G.10]-[G.11]).** Keep a database of operational hardware and software in each automotive ECU. Track enough software-component detail that a newly disclosed open-source or off-the-shelf flaw maps quickly to affected ECUs and vehicles (the SBOM habit).
- **Cybersecurity testing and vulnerability disposition (4.2.7, [G.12]-[G.15]).** Evaluate COTS and open-source ECU software against known vulnerabilities. Run product cybersecurity testing, including penetration tests. Use qualified testers outside the development team. Produce a vulnerability analysis for each known or newly found issue, with disposition and rationale.
- **Detection, containment, remediation, and minimal risk condition (4.2.8, [G.16]-[G.17]).** Build rapid incident detection and remediation capability beyond design-time protections. When an attack is detected, mitigate safety risk to occupants and surrounding road users and move the vehicle to a minimal risk condition as the risk warrants.
- **Attack intelligence, documentation, and version control (4.2.9, [G.18]-[G.20]).** Collect potential-attack information, analyze it, and share it through Auto-ISAC and other channels. Document cybersecurity actions, design choices, analyses, evidence, and changes. Keep those work products traceable under document version control.
- **Continuous risk reevaluation (4.2.10, [G.21]).** Reassess risks on a systematic, ongoing schedule as the threat landscape moves, and update processes and designs when the reassessment says so.
- **Secure development practice and industry participation (4.2.11, [G.22]-[G.24]).** Follow secure software development practice (S1 points at NIST publications and names ISO/SAE 21434). Join automotive standards and Auto-ISAC practice work. Collaborate on new mitigations when future risks appear.

## Key Concepts

- **Non-binding character.** S1 is guidance. Citing it as a hard legal requirement confuses voluntary practice with the FMVSS self-certification duty covered later in the pack.
- **Whole-chain scope.** Designers, suppliers, manufacturers, modifiers, and alterers all sit inside the guidance. A weak supplier link is a vehicle link.
- **Safety-first risk ranking.** Occupant and other-road-user safety is the primary axis when assessing cybersecurity risk ([G.5]).
- **Full-lifecycle assessment.** The risk step is not a launch gate only; it reflects mitigation across the vehicle life ([G.4]).
- **Sensor integrity is in scope.** Cybersecurity here includes physical and wireless manipulation of perception inputs, not only network code bugs ([G.6]).
- **Eliminate, then layer.** Unreasonable safety-critical risk is removed or mitigated by design; leftover function gets layered protection and supplier expectations ([G.7]-[G.9]).
- **Inventory enables response.** Without ECU hardware/software inventories and component detail, a public vulnerability cannot be mapped to fielded vehicles in time ([G.10]-[G.11]).
- **Independent testing.** Penetration and related tests need qualified people who did not build the system and who are incentivized to find faults ([G.14]).
- **Documented vulnerability management.** Every assessed or discovered vulnerability gets an analysis, a disposition, and a written rationale ([G.15]).
- **Field detection path.** Design protections are necessary but not sufficient; detection and remediation capability must exist after sale ([G.16]-[G.17]).
- **Minimal risk condition.** When a cyber event is detected, the vehicle should be able to move toward a minimal risk condition appropriate to that risk ([G.17]).
- **Share attack data.** Potential-attack information is collected, analyzed, and shared through Auto-ISAC and peers ([G.18] in 4.2.9).
- **Traceable cyber work products.** Actions and evidence live under version control so audits and later changes have a trail ([G.19]-[G.20]).
- **Living process.** Periodic reevaluation updates both process and design as the landscape changes ([G.21]).
- **Name-only external standards.** ISO/SAE 21434, NIST publications, Auto-ISAC guides, CISA, and related bodies are cited as places industry should look; this pack does not carry their text.

## Mental Models

- **Management system first, controls second.** [G.2]-[G.24] build the programme. [T.1]-[T.25] in ch04 are the vehicle-side controls that programme must own.
- **Compromise is an input, not a surprise.** Layering starts from the assumption that some system will be reached.
- **Safety is the sort key.** When cyber risk and other product risks compete, occupant and road-user safety decides priority.
- **Inventory is an incident-response tool.** SBOM-like detail exists so a CVE can be turned into a vehicle list, not so a spreadsheet looks complete.
- **Independent eyes find what builders miss.** Testers outside the development team are part of the process definition, not a luxury.
- **Detection closes the design loop.** Protections reduce likelihood; detection and minimal-risk transition limit harm after a breach starts.
- **Documentation is how the process becomes auditable.** If the choice is not written and versioned, later self-audit and field fixes have nothing to stand on.

## Anti-patterns

- **Treating S1 as a binding FMVSS-style rule.** It is voluntary guidance; overstating its legal force is a category error.
- **Executive sponsorship as a poster only.** [G.2] wants resources, communication paths, and an independent voice in safety design, not a title without staff or budget.
- **Cyber review bolted on after architecture freeze.** [G.3]-[G.4] put cybersecurity inside the systems-engineering development process and lifecycle risk step.
- **Ignoring sensor attacks because "the ECU code is clean."** [G.6] lists spoofing, jamming, blinding, and ML false-positive excitation as in-scope risks.
- **Leaving known safety-critical cyber risk in the field without design mitigation.** [G.7] requires removal or mitigation to acceptable levels; avoidable risky function should be eliminated where possible.
- **Single-layer "secure gateway" stories with no residual-risk layering or supplier requirements.** [G.8]-[G.9] pair layered protection with communicated supplier expectations.
- **No ECU software inventory, then surprise when a library CVE ships in production vehicles.** [G.10]-[G.11] exist to prevent that gap.
- **Penetration tests run by the same team that wrote the code, with no separate vulnerability write-ups.** [G.14]-[G.15] reject that pattern.
- **Design-time controls with no field detection or remediation path.** [G.16]-[G.17] require rapid detection capability and safety-minded response, including minimal risk condition.
- **Hoarding attack observations inside one OEM.** [G.18] in 4.2.9 expects analysis and sharing through Auto-ISAC and other mechanisms.
- **One-time risk assessment at SOP with no periodic reevaluation.** [G.21] requires ongoing reassessment as the landscape moves.

## Key Takeaways

1. S1 is voluntary NHTSA guidance for motor vehicle and equipment cybersecurity; it is not itself a regulation.
2. Scope reaches the full design and supply chain; weakest-link security and verified supplier expectations are explicit.
3. The opening general practice anchors industry work on the NIST CSF functions Identify, Protect, Detect, Respond, and Recover, under a layered, compromise-assumed model.
4. Leadership priority ([G.2]) means dedicated resources, open internal reporting lines, and an independent cybersecurity voice in vehicle safety design.
5. Development follows a systems-engineering process ([G.3]) with a full-lifecycle cybersecurity risk assessment ([G.4]) ranked by occupant and road-user safety ([G.5]).
6. Sensor integrity, safety-critical risk removal, layered residual protection, and supplier cybersecurity requirements are first-class design duties ([G.6]-[G.9]).
7. ECU hardware/software inventories and component-level tracking make vulnerability response possible at vehicle scale ([G.10]-[G.11]).
8. COTS/open-source evaluation, independent penetration testing, and written vulnerability disposition form the assurance loop ([G.12]-[G.15]).
9. Field detection and remediation must be able to protect people and drive a minimal risk condition when an attack is seen ([G.16]-[G.17]).
10. Attack-intelligence sharing, full documentation under version control, continuous risk reevaluation, secure-development practice, and industry collaboration keep the programme current ([G.18]-[G.24] in 4.2.9-4.2.11).

## Connects To

- **ch01** - which NHTSA document answers which question, and how voluntary cyber guidance sits beside FMVSS.
- **ch03** - information sharing, vulnerability reporting, incident response, self-audit, education, aftermarket devices, and serviceability ([G.25]-[G.45]).
- **ch04** - technical vehicle controls ([T.1]-[T.25]) that the process in this chapter must specify, test, and maintain.
- **ch05-ch06** - ADS 2.0 safety design elements and roles; cyber process still applies when the vehicle includes automated driving functions.
- **ch08** - functional-safety orientation and signpost routing when ISO 26262 or related names appear beside these practices.
- **automotive-signpost** - ISO/SAE 21434 and related paywalled or citation-only designations named in S1 footnotes.
