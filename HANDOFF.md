# Handoff — 2026-11-26
## Current state
Foundation v0.2.0: open-source engineering lab, applied research and technical community. Three existing tools registered; flagship undefined. Foundation open to contributions and maintained by the founder; no additional maintainers confirmed. GitHub organization not created. Logo 02 and assets preserved. Website and portfolio updated for the new mission. Website commit 578dbe3 and portfolio commit eb448ac reached Vercel READY in production after opening the foundation to contributions.
## Decisions
GitHub sole source; independent repositories; security, data integrity, backend, algorithms and reliable AI; human review and reproducible checks. Editorial strategy retired (16 files removed); history in Git. English is canonical for active documentation, code comments, commits, issues and PRs; Italian manifesto retained. Historical sessions may remain Italian.
## Open-source readiness
Engineering standard, CONTRIBUTING, SECURITY, RFC and GitHub issue/PR templates created. The founder reports creating intelligenzaumana.lab@gmail.com for general contact and private vulnerability reports. The founder confirmed receipt of a test message on 2026-11-26; reply delivery and each project's reporting channel still need verification. No SLA.
## Product audit
- Learning Ledger: README, MIT LICENSE, marketplace and plugin 1.0.0 manifests, CONTRIBUTING and Python 3.11–3.13 CI workflow verified. Seven skills declared; deterministic local ledger. At 0c733aa: 45 tests pass locally on Python 3.12; main CI passed. Latest GitHub release v0.2.2; manifest declares 1.0.0. Installation and compatibility unverified.
- Spring Security Advisor: README, MIT LICENSE, marketplace and plugin 1.0.0 manifests, Python 3.11–3.13 CI workflow verified. README declares 23 rules and 31 contextual checks; standalone scanner. CONTRIBUTING added in 9415bb7. At ea7ed69 and after the documentation update: 124 tests pass locally on Python 3.12; previous main CI passed. Latest GitHub release v0.2.0; manifest declares 1.0.0. Coverage, false positives and installation remain unverified.
- Project Lifecycle Skill: README, SKILL and Claude/Codex integrations read. Prototype v0.2.0; MIT license added in f9c0774. Native installation and real integration tests remain unverified.
## Next steps
1. Verify mailbox reply delivery and ongoing monitoring; check reporting channels in each project.
2. The founder has been asked to create the separate GitHub organization; confirm its URL and access before any setup. Check URL, CI, marketplace and deployment impact before transfers.
3. Verify Project Lifecycle packaging, native installation and integration tests.
4. Consolidate tools: reconcile manifest 1.0.0 with GitHub releases v0.2.2 (Learning Ledger) and v0.2.0 (Spring Security Advisor), verify installation and release policy, and verify each project security reporting channel.
5. Design shared marketplace with independent repositories and versions; verify official format and installation. Discussed commands are illustrative.
6. Align website and portfolio; research flagship problem with evidence and RFC.
## Verification limits
Foundation tree enumerated at 765c1de: 54 files, including 46 Markdown files; checked Markdown relative link paths exist. The 2026-11-26 check covered relative link paths, not anchors; subsequent website deployments reached READY. The project registry now records the foundation repository as public; the foundation now carries an MIT license. Project Lifecycle tests and installs, product installation compatibility and repository transfers remain unverified. Both production deployments reached READY; mobile rendering is not yet verified. Organization and marketplace not created. Method name and slogan provisional. No artificial deadlines.

## Project identity
Official project READMEs use the label “An Intelligenza Umana project” and link to the foundation and canonical project registry. The label is descriptive and not a cryptographic signature. Publicly verifiable release signing or provenance remains to be researched and designed; no key or signing workflow has been created.
