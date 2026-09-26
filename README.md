<!--
Copyright (c) 2026 JG Systems Consulting Ltd. - MIT License (see LICENSE).
SPDX-License-Identifier: MIT
-->

<h1 align="center">jgs-automotive-knowledge-packs</h1>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT%20(tooling)-blue" alt="License: MIT (tooling)">
  <img src="https://img.shields.io/badge/version-0.1.0-green" alt="Version 0.1.0">
</p>

<p align="center">
  <strong>Installable catalogue of automotive engineering knowledge-pack skills for
  coding agents, with one orchestrator that routes free-text sector questions to
  the right packs.</strong>
</p>

**Copyright (c) 2026 JG Systems Consulting Ltd. - MIT License (tooling); pack content under each source's own licence (see [NOTICE](NOTICE)).**

---

## What it is

This repo is the Automotive member of the industry knowledge-pack fleet: one repo
per engineering sector, each an installable catalogue of knowledge-pack skills for
coding agents. The packs are reconstructed reference notes on vehicle cybersecurity
best practices (NHTSA), Automated Driving Systems guidance, and the FMVSS
(Federal Motor Vehicle Safety Standards) landscape, plus signposts to the wider
automotive and functional-safety standards world (ISO 26262, ISO/SAE 21434, UNECE
WP.29 and related instruments, cited by designation only). It is engineering
signposting and reference material, not legal or regulatory advice.

## Install

```bash
python install.py --dry-run   # preview
python install.py             # install the packs as agent skills
```

Shell equivalents: `install.sh` (bash) and `install.ps1` (PowerShell). After
install, each pack is invocable as an Agent Skill.

## Use

- **`/auto <question>`**: the orchestrator. Type a free-text automotive question
  and it routes through a curated topic, agency, and deliverable map to the right
  pack(s), reads them, and answers with pack and chapter citations.
- **`/nhtsa-vehicle`**: the content pack. NHTSA Cybersecurity Best Practices,
  Automated Driving Systems 2.0 guidance, and 49 CFR Part 571 (FMVSS) reference
  notes in one skill.
- **`/automotive-signpost`** and **`/functional-safety-signpost`**: signpost
  packs. Citation-only maps into the automotive and functional-safety standards
  landscape; they name where a standard lives and what it covers, and carry no
  standard text.

## Gates

Run all three from the repo root:

```bash
python tooling/validate_pack.py --all   # every pack matches docs/PACK-SPEC.md
python tooling/check_release.py         # release readiness: files, versions, leaks, links, index, headers
python tooling/test_ci_gate.py          # proves CI (.github/workflows/validate.yml) checks the same things
```

CI green is not release-ready: `check_release.py` is the pre-tag gate. Run it
before tagging and confirm the sha on its `RELEASE CHECK: PASS` receipt matches
the commit you tag.

## Licence

Two separable layers:

- **Pack content:** Public Domain (US Government work, 17 U.S.C. 105) for the
  NHTSA-derived material. Attributions and caveats live in [NOTICE](NOTICE) and
  each `packs/<slug>/LICENSE`; the model is set out in
  [docs/LICENSING.md](docs/LICENSING.md).
- **Tooling and scaffolding:** [MIT](LICENSE) (JG Systems Consulting Ltd.).
