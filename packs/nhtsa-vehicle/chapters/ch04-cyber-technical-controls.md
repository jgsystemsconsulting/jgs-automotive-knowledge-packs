# Chapter 4: Cyber Technical Controls

Sources: S1 Cybersecurity Best Practices for the Safety of Modern Vehicles, Updated 2022 (NHTSA final; 87 FR 55459; docket NHTSA-2020-0087; pub. 15745-090822-v2a), sec 8 (Technical Vehicle Cybersecurity Best Practices), body pp. 17-21 of `sources/text/S1.txt` (printed PDF pp. 12-17). Practices in this slice: [T.1]-[T.25]. Glossary appendix pp. 22-23 excluded per pin. General practices [G.x] are ch02-ch03. NIST FIPS 140 series is named for cryptographic technique selection; ISO/SAE 21434 appears as name citation only.

## Core Idea

Section 8 turns the management programme in secs 4-7 into vehicle-side technical controls. The topics are the paths attackers actually use: leftover developer debug access, weak or shared cryptography, abusive diagnostics, unprotected internal messages, thin event logs, open wireless and IP services, and unauthenticated or rollbackable software updates including OTA. Each [T.x] practice is a design constraint the process chapters must specify, test, and maintain. S1 still does not bind by regulation; it states what NHTSA recommends the architecture enforce.

## Frameworks Introduced

- **Developer and debugging access on production devices (8.1, [T.1]-[T.2]).** Limit or eliminate developer-level access to deployed ECUs when there is no foreseeable operational need. If access must remain, protect debug interfaces so only authorized privileged users can use them. Hiding connectors, traces, or pins is not enough protection by itself.
- **Cryptographic techniques and credentials (8.2, [T.3]-[T.5]).** Keep cryptographic techniques current and non-obsolescent for the application; implementation quality still decides real security. Protect credentials that grant elevated access to vehicle platforms from unauthorized disclosure or modification. A credential taken from one vehicle must not open other vehicles. S1 notes public-key approaches beat symmetric keys reused across many vehicles, and points at NIST FIPS 140 series updates for technique selection.
- **Vehicle diagnostic functionality (8.3, [T.6]-[T.8]).** Confine diagnostic features, as far as possible, to an operating mode that matches their purpose. Design diagnostic operations so misuse outside that purpose has little or no dangerous effect (example pattern: brake-disable diagnostics only at low speed, never all brakes at once, time-bounded). Minimize global symmetric keys and ad-hoc cryptography for diagnostic access.
- **Diagnostic tools (8.4, [T.9]).** Vehicle and tool manufacturers should control tool access to systems that can run diagnostics or reprogramming through authentication and access control.
- **Vehicle internal communications (8.5, [T.10]-[T.11]).** Move critical safety signals, when possible, on paths external interfaces cannot reach (for example dedicated sensor transport instead of a shared CAN spoof surface; segmented buses to limit aftermarket device impact). On shared or possibly insecure channels, use best practice against replay, integrity loss, and spoofing, and tightly restrict physical and logical access. Critical safety messages are those that can directly or indirectly affect safety-critical control operation.
- **Event logs (8.6, [T.12]-[T.13]).** Keep an event log rich enough to show the nature of a cyberattack or successful breach and to support reconstruction. Periodically review logs that can be aggregated across vehicles for attack trends.
- **Wireless paths into vehicles (8.7, [T.14]-[T.21]).** Treat networks and systems outside the vehicle's wireless interfaces as untrusted and mitigate accordingly. Use segmentation and isolation so wireless-connected ECUs do not sit open to low-level safety controls (braking, steering, propulsion, power management), including privilege separation and logical/physical isolation. Put strong boundary controls on gateways, such as strict whitelist filtering of message flows between segments. For IP-facing services: remove unnecessary services from production vehicles, limit remaining services to essential function, and protect those ports so only authorized parties use them. Use appropriate encryption and authentication between external servers and the vehicle. Plan processes that can push routing-rule changes quickly to one vehicle, a subset, or the whole connected fleet.
- **Software updates and modifications (8.8, [T.22]-[T.23]).** Use current techniques so only authorized, authenticated parties can modify firmware (digital signing so ECUs refuse unauthorized images is one named approach). Limit firmware version rollback attacks that reinstall older, weaker software.
- **Over-the-air software updates (8.9, [T.24]-[T.25]).** When OTA is offered, maintain integrity of the updates, the update servers, the transmission path, and the update process. Design security measures against compromised servers, insider threats, man-in-the-middle attacks, and protocol vulnerabilities.

## Key Concepts

- **Production debug is an attack surface.** Leftover JTAG-class or similar access on field ECUs is in scope even if "only manufacturing used it" ([T.1]-[T.2]).
- **Obscurity is not a control.** Physical concealment of debug pins does not satisfy [T.2].
- **Crypto ages; implementations fail first.** [T.3] demands non-obsolescent techniques and reminds that bad implementation voids good algorithm choice.
- **Credential scope is per vehicle.** [T.5] blocks fleet-wide blast radius from one extracted secret; [T.4] protects elevated credentials at rest and in use.
- **Diagnostics are privileged operations.** Mode limits, safety interlocks, and avoidance of global diagnostic keys reduce abuse ([T.6]-[T.8]).
- **Tools are part of the trust boundary.** [T.9] puts authentication and access control on diagnostic and reprogramming tools, not only on the vehicle.
- **Critical signals deserve isolation.** [T.10] prefers transport that external interfaces cannot reach; shared-bus designs need the channel protections in [T.11].
- **Logs are for reconstruction and fleet trend detection.** [T.12] sets content; [T.13] sets cross-vehicle review cadence.
- **External wireless peers are untrusted.** [T.14] is the default posture for anything beyond the vehicle interface.
- **Segment safety from connectivity.** [T.15]-[T.16] isolate wireless ECUs from low-level controls and filter gateway message flows by whitelist.
- **Close unused listeners.** [T.17]-[T.19] remove unnecessary IP services, keep essentials only, and authorize use of what remains.
- **Server links authenticate both ways in spirit.** [T.20] requires appropriate encryption and authentication on operational vehicle-to-server communication.
- **Routing rules must be field-updatable at fleet scale.** [T.21] is the rapid containment lever when a network path goes bad.
- **Signed firmware and anti-rollback.** [T.22]-[T.23] address malware install and downgrade-to-vulnerable paths.
- **OTA integrity is end-to-end.** [T.24]-[T.25] cover package, server, transport, process, and named threat classes (compromised server, insider, MITM, protocol flaws).

## Mental Models

- **Every leftover interface is a door.** Debug, diag, wireless service, and update path are four doors; each needs an explicit lock story.
- **One vehicle's secret must not be every vehicle's secret.** Credential design is fleet-blast-radius design.
- **Diagnostics obey physics of misuse.** If a diag action can brick safety while driving, mode, concurrency, and time limits belong in the design.
- **Bus trust is not free.** Critical control data on a shared, externally reachable bus is a spoof invitation unless isolated or cryptographically protected.
- **Logs without review are storage.** Aggregation and periodic trend review turn logs into detection.
- **Connectivity ECUs are semi-hostile neighbors to safety ECUs.** Segmentation and gateway allowlists encode that distrust.
- **Update systems are remote installers.** Whoever can push firmware owns the ECU; authentication, signing, and anti-rollback are the install policy.
- **OTA multiplies server risk.** A bad server or MITM scales to the fleet; integrity controls must assume that scale.

## Anti-patterns

- **Shipping production ECUs with open developer debug access "for support."** [T.1]-[T.2] require elimination or real privileged protection, not hidden headers.
- **Fleet-wide symmetric diagnostic or update keys.** Conflicts with [T.5] and the diagnostic key guidance in [T.8]; public-key patterns are preferred where S1 compares them.
- **Obsolete or home-grown crypto for elevated access.** [T.3] wants current techniques; ad-hoc diagnostic crypto is minimized under [T.8].
- **Diagnostic routines that can disable safety functions at highway speed or in combination.** [T.6]-[T.7] demand mode limits and misuse-safe design.
- **Any shop tool can reflash without authentication.** [T.9] requires controlled tool access.
- **Safety-critical messages only on an open shared CAN reachable from OBD or wireless bridges.** [T.10]-[T.11] push isolation or strong channel protections.
- **No forensic trail after a breach.** Missing [T.12] logs, or logs never reviewed across the fleet ([T.13]).
- **Treating cellular, Wi-Fi, or Bluetooth peers as trusted networks.** [T.14] says untrusted.
- **Flat architecture: telematics ECU can speak directly to brake or steer controllers.** [T.15]-[T.16] call for segmentation, isolation, and gateway allowlists.
- **Telnet, debug bridges, or other non-essential IP services left enabled in production.** [T.17]-[T.19].
- **Cleartext or unauthenticated back-end links.** [T.20].
- **No way to push emergency routing or firewall changes to field vehicles.** [T.21].
- **Unsigned or roll-backable firmware update paths.** [T.22]-[T.23].
- **OTA pipeline that trusts the server farm and the radio path by default.** [T.24]-[T.25] list integrity duties and explicit threat classes.

## Key Takeaways

1. Technical best practices [T.1]-[T.25] specify vehicle-side controls for debug access, cryptography, diagnostics, internal comms, logs, wireless paths, and software/OTA updates.
2. Remove or tightly authorize developer debug on production ECUs; concealment alone fails ([T.1]-[T.2]).
3. Use current cryptography, protect elevated credentials, and keep one vehicle's credential from unlocking others ([T.3]-[T.5]).
4. Constrain diagnostic features by mode and misuse effect; minimize global diagnostic keys; authenticate diagnostic and reprogramming tools ([T.6]-[T.9]).
5. Isolate or strongly protect critical safety signals; restrict physical and logical access on shared channels ([T.10]-[T.11]).
6. Maintain reconstructive event logs and review aggregatable logs for fleet attack trends ([T.12]-[T.13]).
7. Treat external networks as untrusted; segment wireless ECUs from safety controls; whitelist gateway flows; minimize and lock down IP services; encrypt and authenticate server links; support rapid routing-rule updates ([T.14]-[T.21]).
8. Allow only authenticated parties to modify firmware, block rollback to weaker versions, and keep OTA packages, servers, transport, and process integrity under explicit threat models ([T.22]-[T.25]).

## Connects To

- **ch02** - development process, risk assessment, testing, and monitoring that decide which of these controls are required where.
- **ch03** - incident response, aftermarket device risk, and serviceability constraints that these controls must still allow to function.
- **ch01** - orientation on voluntary guidance versus FMVSS obligations.
- **ch05** - ADS design elements (for example fallback and data recording) that still ride on these vehicle technical controls.
- **automotive-signpost** - ISO/SAE 21434 and related designations named beside technical engineering practice.
