# CyberURLs

**Live:** https://cyberbyteir.github.io/CyberURLs/

Single-file, offline-capable link dashboard for OSINT and cyber investigation resources.

**169 resources across 11 categories.** Open [`index.html`](index.html) in any browser — no build step, no server, no dependencies to install.

## Features

- Live text filter across every link (name, category, host)
- Category pill filters and collapsible panels
- Per-link host labels
- Keyboard-friendly, dark UI

## Categories

| Category | Count |
|---|---|
| Investigations | 34 |
| Social Media OSINT | 3 |
| Cryptocurrency | 10 |
| Network / IP | 32 |
| Malware & Threat Intel | 11 |
| Ransomware | 8 |
| Software & Tools | 23 |
| Cell / Mobile Forensics | 13 |
| Training & Certifications | 18 |
| Miscellaneous | 3 |
| Indiana | 14 |

## Notes

- The page is self-contained HTML/CSS/JS. The only external request is a Google Fonts stylesheet; without network access it falls back to system monospace and sans-serif fonts and remains fully functional.
- Several linked resources are restricted portals (law enforcement, vendor, or subscription) and require existing credentials. No credentials are stored in this repository.
- Link rot is expected in this problem space. Verify before relying on any entry.

## Editing

Add a resource by copying an existing `.link-item` row into the relevant `.link-list`, then update that panel's `.cat-count`, the footer `resources` total, and the fallback count in the `applyFilters()` function.
