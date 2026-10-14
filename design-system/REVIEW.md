# Review notes and GitHub update checklist

Status of this design system for 凡纳弘途 VANAHOM (asset key `vanahom`, main language 中文), prepared for `ksamint/dsys_vanahom`.

## What is in this folder

| Path | What |
| --- | --- |
| `README.md` | Brand book (中文): identity, voice, colour, type, layout, shape, motion, imagery, logo, always/never |
| `SANCTEM.md` | Sub-brand rules |
| `tokens.json` | Source of truth: 20 colours, 2 font families, 12 type styles, spacing, radius, border, motion |
| `tokens.css` | Compiled from `tokens.json` (CSS custom properties). Regenerate; don't edit by hand |
| `components/bundle.css` | `.vh-*` component styles, responsive |
| `components/<Name>/` | `README.md` (usage) + `preview.html` (standalone; open directly in a browser) for 11 components |
| `assets/Logos/` | 6 SVG wordmarks (red, white, grey, ink; square red, grey) |
| `index.html` | Links to every preview |

## Sources

- IPTrust brand reference for `vanahom` (palette #B12137 / #A8ADAD / #8E1A2C, naming rule, links) as supplied in the request.
- Brand guideline v0.4 as relayed in that reference: red under 8% of a view, square corners, no shadows, hairlines, 8pt spacing, 320ms ease-out, Cormorant Garamond / Noto Serif SC + Manrope / Noto Sans SC.
- `slim-VANAHOM凡纳弘途v0.4.pdf` (40 pages): copy, structures, sampled colours (`red-wash`, `cell`, SANCTEM tiers), team and project examples.
- The four logo PNGs supplied.

## Not verified (could not reach these)

`apuch.art` (brand API, MCP) was blocked from the build environment and GitHub access was not enabled, so:

1. **The repo's existing files were not read.** The IPTrust docs say the repo holds `VANAHOM/vanahom_design.md` and `data/*.json` (assets with checksums, theme tokens, provenance). Nothing here was diffed against them. This folder is designed to go in as a new top-level `design-system/` directory so it cannot overwrite them.
2. **IPTrust is not updated.** The brand API's `tokens` array was empty when read. Pushing these tokens back to IPTrust (Skill / MCP) is a separate step; nothing syncs automatically.
3. **Logo SVGs are traced, not designer originals.** Contour trace of the supplied 6000 px PNGs, IoU ≈ 0.98 against the raster. Replace with the official SVGs from IPTrust when available (keep the file names).

## Decisions needed from the brand owner

1. **Typeface conflict.** The guideline says Cormorant Garamond + Manrope; the v0.4 deck uses a geometric sans (Montserrat-style) for English and Noto Sans CJK for Chinese. The system follows the guideline. If the deck is the truth, change `type.families` in `tokens.json`.
2. **Fonts are loaded from Google Fonts** (`@import` in `bundle.css`). Google Fonts is often unreachable from mainland China. For a CN-facing site, self-host the four families and replace the `@import`. No font files are bundled.
3. **Deck contrast issues, deliberately not copied:** white text on the `sanctem-tier-essence` card is 2.86:1 (system uses ink, 5.93:1). The eyebrow style is cangling-grey on white at 2.27:1; the source does this, so it is kept but documented as decorative only. `grey-deep` on `mist` is 4.33:1, below 4.5:1, so keep it on paper.
4. **Rules I derived rather than found in the guideline** (labelled as suggestions where they appear): image rules in README, page side margin `space-24`, the 96px red rule under `SectionTitle`, the responsive breakpoints (960 / 640), and the `Button` component (the deck has no buttons; it follows "red for calls to action"). Confirm or delete.
5. **Real people and a real project appear as examples** in `TeamCard`, `BioBanner` and `CaseStudy` previews (陈鹏飞 David CHEN, 曹幸媛 Tiffany CAO, 延安杨家岭石窑宾馆), taken from the deck. If the repo is public, confirm those people and that project may be named there; otherwise swap in placeholders.

## Still missing

SANCTEM wordmark SVG, AXISEE assets, an icon set (the brand has none documented), project photography and team portraits, real font files. `Cover/` has a preview only (no README).

## Before you push

- [ ] Enable GitHub access for `ksamint/dsys_vanahom` so the existing `VANAHOM/` and `data/` contents can be read, then check nothing here duplicates or contradicts `vanahom_design.md`.
- [ ] Put this folder in the repo as `design-system/`; do not merge it into `VANAHOM/` or `data/`.
- [ ] Settle the open decisions above (fonts first).
- [ ] Swap in the official logo SVGs if you have them; keep the file names.
- [ ] If `data/assets.json` tracks checksums, add the six SVGs there with new SHA-256 values.
- [ ] Decide repo visibility, then keep or replace the named people and project.
- [ ] After pushing, sync tokens and rules back to IPTrust.
- [ ] Re-run `tokens.css` generation if `tokens.json` changes.
