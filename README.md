# CyberURLs

**Live:** https://cyberbyteir.github.io/CyberURLs/

Single-file, offline-capable link dashboard for OSINT and cyber investigation resources.

**170 resources across 12 categories and 45 subcategories.** Open [`index.html`](index.html) in any browser — no build step, no server, no dependencies to install.

## Features

- Live text filter across every link (name, category, host) and across category and subcategory headers — matching a header reveals that whole panel or group
- Category pill filters and collapsible panels
- Named subcategory groups inside each panel; empty groups and empty panels hide themselves while filtering
- Multi-column layout that packs panels vertically, so a tall category leaves no gap beside the short ones
- Gold star marks the author's favorites, on the same footprint as the standard dot so names stay
  aligned; a footer legend and a per-star tooltip say what it means
- Per-link host labels
- Responsive down to 320px: full-width search, a single scrollable pill row,
  larger touch targets and safe-area padding for notched phones
- Keyboard-friendly, dark UI

## Categories

| Category | Count | Subcategories |
|---|---|---|
| Network & Infra | 34 | IP Lookup & Geolocation · IP Reputation, Proxy & Tor · Domain, URL & Site Analysis · Email Header Analysis · Attack Surface & Recon · Wireless & Hardware IDs · Peer-to-Peer & Tracking |
| Malware & Threat Intel | 17 | Threat Intelligence Platforms · File & Sample Analysis · Sample & Hash Repositories · Breach & Credential Data |
| Ransomware | 6 | Leak Site Trackers · Identification & Decryption · Group Intelligence |
| Cryptocurrency | 10 | Investigation Platforms · Block Explorers · Attribution & Abuse Reporting · Reference |
| OSINT & People | 11 | People & Identity · Social Media · Vehicles · Tool Collections |
| LE Databases | 13 | Commercial Data Aggregators · Criminal Justice Systems · Federal & Fusion Portals |
| Legal Process | 8 | Provider Legal Process Portals · Templates & Reference |
| Mobile & Device | 14 | Tool Support & Compatibility · Device Identification · Phone Numbers & Carriers · CDR & Tower Analysis · Community & Technique |
| Forensic Tools | 21 | Vendor Portals & Downloads · Open-Source Forensic Tools · Encoding, Regex & Data Utilities · Passwords & Hash Cracking |
| Reference & Misc | 2 | General |
| Training & Certs | 21 | Forensics & IR Training · Law Enforcement Academies · CompTIA & Vendor Certification · Networking Fundamentals |
| Indiana | 13 | Courts & Case Records · Corrections & Warrants · Vehicles & Geography · State Agency Forms & Programs |

## Link status

Last verified **2026-09-28** (automated HTTP probe, redirects followed).

- 164 of 170 URLs confirmed reachable. Several return `401`/`403`/`429` to a scripted request — that is bot protection or an authentication gate, not link rot; they load normally in a browser.
- Redirected to a new home, URLs updated: InfraGard (`infragard.fbi.gov`), EchoTrail (`echotrail.io`), ZetX TraX (`trax.lexisnexisrisk.com`), XDA (`xdaforums.com`), Objective-See Mac malware collection (GitHub).
- Retired course versions replaced with current ones: Professor Messer Security+ `SY0-701` and Network+ `N10-009`.
- `vindecoder.net` no longer answers on port 80 or 443; replaced with Vincario (`vincario.com`).
- **Field Search (NLECTC)** — `justnet.org` serves an expired TLS certificate. The site is up, but browsers will show a certificate warning. Left in place, flagged here.
- **IP Quality Score** and **IPLogger** resolve to `0.0.0.0` on filtered DNS resolvers (both appear on common threat blocklists). They are reachable from unfiltered networks.
- **Meta / Facebook LE Portal** cannot be verified by script (Facebook returns `400` to unauthenticated non-browser requests).

## Notes

- The page is self-contained HTML/CSS/JS. The only external request is a Google Fonts stylesheet; without network access it falls back to system monospace and sans-serif fonts and remains fully functional.
- Several linked resources are restricted portals (law enforcement, vendor, or subscription) and require existing credentials. No credentials are stored in this repository.
- Link rot is expected in this problem space. Verify before relying on any entry.

## Editing

Add a resource by copying an existing `.link-item` row into the relevant `.sub-label` group inside a `.link-list`, then update that panel's `.cat-count`, the footer `resources` total, and the fallback count in the `applyFilters()` function.
