# Changelog

All notable changes to CyberURLs are documented here.

## v2.0.1 — 2026-09-28

### Added

- Two-level taxonomy: 45 named subcategory groups inside the 12 category panels.
- Subgroup headers hide themselves automatically when the text filter removes every link in the group.
- DFIR Dominican (`dfirdominican.com`) under Training & Certs → Forensics & IR Training.
- Inline version marker: `<meta name="version">` in the head and a version badge in the footer.
- `CHANGELOG.md`.

### Changed

- Restructured 11 categories into 12: Investigations split into **Legal Process** and **LE Databases**; Social Media folded into **OSINT & People**; threat-intel platforms moved into **Malware & Threat Intel**; TraX moved to **Mobile & Device**; NIST NSRL moved to **Malware & Threat Intel**; IntelTechniques moved to **OSINT & People**.
- `applyFilters()` now tracks per-subgroup visibility; `.link-list` max-height raised to 6000px.
- Full link audit of all URLs (automated HTTP probe, redirects followed). Updated to canonical targets: InfraGard → `infragard.fbi.gov`, EchoTrail → `echotrail.io`, ZetX TraX → `trax.lexisnexisrisk.com`, XDA → `xdaforums.com`, Objective-See Mac malware → GitHub, USSS NCFI → `ncfi.usss.gov/fpr/`, X-Ways → public `x-ways.net/forensics/` page.
- Professor Messer courses updated from retired exam versions to Security+ `SY0-701` and Network+ `N10-009`.
- VIN decoder replaced: `vindecoder.net` no longer answers on port 80 or 443 → Vincario (`vincario.com`).
- README rewritten with the subcategory table and a Link status section.

### Known issues

- Field Search (NLECTC) — `justnet.org` serves an expired TLS certificate; browsers will show a warning.
- IP Quality Score and IPLogger resolve to `0.0.0.0` on filtered DNS resolvers; reachable from unfiltered networks.
- Meta / Facebook LE Portal cannot be verified by automated probe.
