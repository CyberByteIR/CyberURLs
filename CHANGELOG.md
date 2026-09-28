# Changelog

All notable changes to CyberURLs are documented here.

## v2.1.1 — 2026-09-28

### Changed

- Reference & Misc now sits before Training & Certs in the panel and pill order.
- Added 10px separation between columns and between stacked panels, with a 10px inset from the viewport edge. The grid background moved from `--border` to `--bg` so the widened gaps read as space rather than thick dividers, and panels gained a `1px solid var(--border)` outline to keep their edges defined.

### Fixed

- Footer no longer forces horizontal page scroll on narrow screens. It was a non-wrapping flex row, pushed past the viewport by the version badge added in v2.0.1; it now wraps. Verified zero horizontal overflow at 420, 700, 1000 and 1900px.

## v2.1.0 — 2026-09-28

### Added

- Text filter now matches category and subcategory headers, not just link names. Searching a category header (e.g. `legal process`) reveals that whole panel; searching a subcategory header (e.g. `block explorers`) reveals that whole group.
- Panels with no remaining matches hide themselves during a search so the column layout stays packed.

### Changed

- Category order is now Network & Infra, Malware & Threat Intel, Ransomware, Cryptocurrency, OSINT & People, LE Databases, Legal Process, Mobile & Device, Forensic Tools, Training & Certs, Reference & Misc, Indiana. Filter pills follow the same order.
- Layout switched from CSS grid to CSS multi-column with `break-inside: avoid`, so panels stack and pack vertically instead of every panel in a row being padded to the height of the tallest one. Measured at 1900px: 5 columns of 1169–1364px, total page height 1366px.

### Fixed

- `.link-list` max-height returned to 2000px (from 6000px). The tallest list is 1125px, so the oversized value made most of the 0.25s collapse transition produce no visible movement.

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
