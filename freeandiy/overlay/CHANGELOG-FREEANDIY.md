<!-- Modified-by: FreeANDIY (Free Andy Agency), 2026. New file, not part of upstream GridCraft. -->
# FreeANDIY Sheets: changes from upstream GridCraft

This file lists what the FreeANDIY fork changes in GridCraft (Apache-2.0 section 4(b)). The
exact changes are generated from `freeandiy/` (see `NOTICE`); `git diff upstream-main main`
shows every changed file.

## Unreleased

### Branding
- Product name **FreeANDIY Sheets** everywhere users see it: window title, ribbon, About,
  messages, installers, desktop entries, the web page.
- Application id `agency.freeandy.sheets` (was `ai.storyteller.gridcraft`), so FreeANDIY builds
  install next to GridCraft.
- Executables `freeandiy-sheets` and `freeandiy-sheets-cli`; the cargo packages keep their names.
- New app icon set (the angel Andy, Free Andy Agency) and DMG background.
- Light and dark themes in FreeANDIY's paper-and-ink print look (no soft shadows, the stamp-rose
  accent, the yellow highlighter on selected headers); the sheet itself stays white or black.
- UI font IBM Plex Sans (OFL 1.1) on the desktop, ahead of the system font.

### Removed
- The ArtCraft name, wordmark and logos (`docs/brand/`), as their terms require of forks.
- The ArtCraft Discord links (About, the macOS Help menu).
- Upstream's release, Flatpak-pages and platform workflows (upstream's CI still runs
  `cargo xtask ci`).

### Added
- About: attribution to upstream GridCraft and the Free Andy Agency seal; a link to this
  repository.
- Slovak user interface (every interface label).
- `NOTICE` section and `ATTRIBUTION.md` rows for FreeANDIY's assets and fonts; packages now ship
  `NOTICE`, `ATTRIBUTION.md`, the font licences and the brand terms.
