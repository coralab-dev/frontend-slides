---
name: frontend-slides
description: Build, convert, and improve animated HTML slide presentations with the frontend-slides design system. Use when the user asks for slides, a pitch deck, an HTML presentation, PPT/PPTX-to-web conversion, or improvements to an existing slide deck.
---

# Frontend Slides for Codex

This is the Codex entry point for the **frontend-slides** project. The existing upstream resources at the repository root remain the source of truth; do not duplicate or invent them.

## Where to find the resources

1. Locate the repository root (the folder containing the original `SKILL.md`, `viewport-base.css`, and `STYLE_PRESETS.md`).
2. Read that root `SKILL.md` for the full presentation workflow. **All relative paths mentioned in the original instructions resolve from the repository root**, not from this nested Codex skill folder.
3. Load only the files needed for the current task:
   - `STYLE_PRESETS.md` for preset design systems.
   - `viewport-base.css` for the mandatory 1920×1080 stage.
   - `html-template.md` for the presentation controller and structure.
   - `animation-patterns.md` for entrance and transition patterns.
   - `bold-template-pack/selection-index.json` and the selected template's preview/design files for optional bold themes.
   - `scripts/extract-pptx.py` when extracting content from a PowerPoint file.

If these root files are unavailable (for example, if someone copied only this nested `SKILL.md` elsewhere), say that the full repository is required for the original design system rather than silently pretending those resources exist.

## Workflow

1. Identify the requested mode: new presentation, PPT/PPTX conversion, or enhancement of existing HTML slides.
2. For a new deck, discover content, audience, slide count, and whether it is speaker-led or reading-first. Use existing information rather than asking the user to repeat it.
3. Offer three distinct visual preview options, then implement the selected direction using the original templates and referenced assets.
4. Keep each slide on the fixed 1920×1080 stage, uniformly scaled to the viewport; preserve navigation, accessible contrast, reduced-motion support, and inline editing where requested by the upstream workflow.
5. Review the generated HTML for missing assets, incorrect slide visibility, clipping, overlap, and navigation failures. Where browser automation is available, visually verify at desktop and mobile viewports. State clearly which checks actually ran.
6. Return the presentation's file path and brief usage instructions.

## Safety and current limitations

- **Do not execute** `scripts/deploy.sh` or `scripts/export-pdf.sh` from the upstream project by default. Their current versions have unresolved security/functional reports; audit and fix them separately before any use.
- Never deploy or publicly share a deck without the user's explicit authorization, and never include unrelated files or secrets in a deployment.
- Do not claim that PDF export, PowerPoint conversion, or visual checks passed without actually testing them.
- Keep the repository's MIT license and original attribution intact when modifying or redistributing code.

For full project-wide installation, copy the whole repository or package the required referenced resources alongside the skill. This initial integration targets **Codex opened at the root of this fork**.
