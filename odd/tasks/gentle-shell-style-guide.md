# Gentle Shell style guide

Create Gentle Shell's design-system documentation: a style-guide document (`design/system.md`) and a self-contained token artboard (`design/system.html`), built only from tokens found in project sources (theme JSON, CSS custom properties, shell-rework artboards, and brand assets).

## Specs

S1 — Create `design/system.md`, Gentle Shell's style guide. It must cover: colors (token name, value, usage, source `path`), typography (font families, type scale, weights, line-heights), spacing, radius, shadows, and component rules. It must also include a Logo / brand assets section listing each brand image with its path, format, and role. Every token entry names its source `path`. Record only values found in project sources; never invent tokens.

S2 — Create `design/system.html`, a self-contained 1440 px-wide token artboard. It renders the system tokens: color swatches, type scale, spacing scale, radius, shadows, and the core components, plus the logo/brand assets. It must obey the no-external-URL rule: no CDNs, remote fonts, remote images, or scripts. Use system font stacks only.

S3 — Self-check: list the colors and font families used in `design/system.html` and compare them with the tokens in `design/system.md`; fix every deviation before finishing. Confirm `system.html` contains no external URL references.

S4 — After writing or changing the artboard, open the canvas with the `gentle_design` tool and report the returned URL.

## Tasks

T1 — S1: write `design/system.md` with all token groups, source paths, and the Logo / brand assets section. Route: delegated writer.
T2 — S2: write `design/system.html` token artboard. Route: delegated writer.
T3 — S3: self-check `design/system.html` tokens against `design/system.md`; fix deviations; confirm no external URLs. Route: delegated writer, parent readback.
T4 — S4: open canvas, report URL. Route: inline.

## Log

L1 — User request verbatim: "Crea una hoja/guía de estilo de gentle shell, con sus colores, logos, fuentes,..."
L2 — Explorer handoff delivered: theme JSON tokens (`themes/Gentle.json`, `themes/Gentleman-Cute.json`, `themes/Gentleman-Sexy.json`), CSS custom properties (`assets/install-wizard/wizard.css`, `assets/design-canvas/canvas.css`), shell-rework artboard tokens (`design/shell-rework/*.html`), and brand assets (`assets/gentle-logo-only.png`, `docs/assets/brand/*`, `docs/assets/features/*`). No existing `design/system.md`.
L3 — Completed. `design/system.md` (style guide: 5 palettes, typography, spacing, radius, shadows, component rules, logo/brand assets, every token with source path) and `design/system.html` (83 KB self-contained 1440 px token artboard) created. Self-check passed: no external http/https/cdn/@import-url references; exactly 83 unique hex values matching `system.md`; all five font stacks match. Canvas opened: http://127.0.0.1:43749/MkrzE4mnbiDJgeJaRSRnxym_pXc8cAmA/d/shell-rework/. Local main updated to `origin/main` (`f4cc69a33`). Branch reset onto updated main and style commit cherry-picked as `498b04106`. PR/push remain user decisions.
