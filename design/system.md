# Gentle Shell design system

This design system is built only from values found in Gentle Shell project sources. It distinguishes the three Pi theme palettes, the two CSS palettes, the shell-rework artboard tokens, and brand asset colors.

Primary shell look: **Gentleman-Cute** rose palette. Gentle Shell installs with `Gentleman-Cute` as the default TUI theme when a user has not already declared one: `scripts/install-tui-mode-setting.mjs:20-24`. The shell-rework artboards also use Gentleman-Cute as the default preview theme: `design/shell-rework/02-proposal.html:58`.

## Colors

### Gentleman-Cute — primary shell palette

Source: `themes/Gentleman-Cute.json`.

| Token | Value | Usage | Source |
| --- | --- | --- | --- |
| `bg` | `#060407` | Page background. | `themes/Gentleman-Cute.json` |
| `bgPanel` | `#100A0F` | Panel background. | `themes/Gentleman-Cute.json` |
| `bgElement` | `#100A0F` | Element or card background. | `themes/Gentleman-Cute.json` |
| `userMessageBg` | `#2A1523` | User message surface. | `themes/Gentleman-Cute.json` |
| `bgSubtle` | `#100A0F` | Subtle surface and custom message background. | `themes/Gentleman-Cute.json` |
| `border` | `#563040` | Primary border and scrollbar thumb. | `themes/Gentleman-Cute.json` |
| `borderSubtle` | `#2A1720` | Subtle border and disabled thinking surface. | `themes/Gentleman-Cute.json` |
| `text` | `#F6EFF3` | Primary text. | `themes/Gentleman-Cute.json` |
| `muted` | `#A78E9B` | Muted text. | `themes/Gentleman-Cute.json` |
| `dim` | `#76616B` | Dim text. | `themes/Gentleman-Cute.json` |
| `accent` | `#F095C8` | Primary accent, links, list bullets. | `themes/Gentleman-Cute.json` |
| `deepPink` | `#C96AA2` | Search match background and markdown quote border. | `themes/Gentleman-Cute.json` |
| `activePink` | `#FFB1DD` | Active accent and maximum thinking color. | `themes/Gentleman-Cute.json` |
| `champagne` | `#E0C27A` | Custom message label, tool title, markdown heading/code, bash mode. | `themes/Gentleman-Cute.json` |
| `pearl` | `#D2CBD0` | Neutral pearl variable. | `themes/Gentleman-Cute.json` |
| `softRose` | `#D7A0B8` | Thinking text. | `themes/Gentleman-Cute.json` |
| `powderBlue` | `#A9C7EE` | Syntax function and medium thinking. | `themes/Gentleman-Cute.json` |
| `mint` | `#B4E7C7` | Success, markdown code, added diff. | `themes/Gentleman-Cute.json` |
| `peach` | `#F2B86D` | Warning and syntax number. | `themes/Gentleman-Cute.json` |
| `sky` | `#C4DAF6` | Syntax operator. | `themes/Gentleman-Cute.json` |
| `warning` | `#F2B86D` | Warning color. | `themes/Gentleman-Cute.json` |
| `error` | `#FF718F` | Error color and removed diff. | `themes/Gentleman-Cute.json` |
| `selection` | `#28121E` | Selected background. | `themes/Gentleman-Cute.json` |
| `toolPendingBg` | `#100A0F` | Pending tool output background. | `themes/Gentleman-Cute.json` |
| `toolSuccessBg` | `#151316` | Success tool output background. | `themes/Gentleman-Cute.json` |
| `toolErrorBg` | `#261019` | Error tool output background. | `themes/Gentleman-Cute.json` |
| `infoBg` | `#100A0F` | Info background. | `themes/Gentleman-Cute.json` |

### Gentle — blue Pi theme

Source: `themes/Gentle.json`.

| Token | Value | Usage | Source |
| --- | --- | --- | --- |
| `bg` | `#06080f` | Page background. | `themes/Gentle.json` |
| `bgPanel` | `#06080f` | Panel background. | `themes/Gentle.json` |
| `bgElement` | `#06080f` | Element or card background. | `themes/Gentle.json` |
| `userMessageBg` | `#161D2E` | User message surface. | `themes/Gentle.json` |
| `bgSubtle` | `#0d0f14` | Subtle surface and custom message background. | `themes/Gentle.json` |
| `surfaceLine` | `#0d0f14` | Surface line. | `themes/Gentle.json` |
| `border` | `#313342` | Primary border. | `themes/Gentle.json` |
| `borderSubtle` | `#232A40` | Subtle border, code block border, quote border, disabled thinking. | `themes/Gentle.json` |
| `text` | `#F3F6F9` | Primary text. | `themes/Gentle.json` |
| `muted` | `#5C6170` | Muted text. | `themes/Gentle.json` |
| `dim` | `#5C6170` | Dim text. | `themes/Gentle.json` |
| `disabled` | `#5C6170` | Disabled text. | `themes/Gentle.json` |
| `accent` | `#E0C15A` | Accent variable. | `themes/Gentle.json` |
| `blue` | `#7FB4CA` | Semantic accent, border accent, links, tool title, list bullet, bash mode. | `themes/Gentle.json` |
| `secondary` | `#A3B5D6` | Secondary color and maximum thinking. | `themes/Gentle.json` |
| `heading` | `#B5B2D0` | Markdown heading. | `themes/Gentle.json` |
| `syntaxComment` | `#8394A3` | Syntax comment. | `themes/Gentle.json` |
| `syntaxKeyword` | `#C99AD6` | Syntax keyword. | `themes/Gentle.json` |
| `syntaxFunction` | `#B99BF2` | Syntax function. | `themes/Gentle.json` |
| `syntaxString` | `#DFBD76` | Syntax string. | `themes/Gentle.json` |
| `syntaxNumber` | `#A4DAA7` | Syntax number. | `themes/Gentle.json` |
| `syntaxType` | `#8FB8DD` | Syntax type. | `themes/Gentle.json` |
| `syntaxPunctuation` | `#96A2B0` | Syntax punctuation. | `themes/Gentle.json` |
| `green` | `#B7CC85` | Success, markdown code, added diff. | `themes/Gentle.json` |
| `warning` | `#DEBA87` | Warning, markdown quote, syntax operator. | `themes/Gentle.json` |
| `red` | `#CB7C94` | Error and removed diff. | `themes/Gentle.json` |
| `brightBlack` | `#8394A3` | Bright black. | `themes/Gentle.json` |
| `brightGreen` | `#D1E8A9` | Bright green. | `themes/Gentle.json` |
| `brightYellow` | `#DEBA87` | Bright yellow. | `themes/Gentle.json` |
| `brightPurple` | `#B99BF2` | Bright purple. | `themes/Gentle.json` |
| `brightMagenta` | `#C99AD6` | Bright magenta. | `themes/Gentle.json` |
| `brightBlue` | `#8FB8DD` | Bright blue. | `themes/Gentle.json` |
| `selection` | `#232A40` | Selected background. | `themes/Gentle.json` |
| `toolSuccessBg` | `#1a2e1a` | Success tool output background. | `themes/Gentle.json` |
| `toolPendingBg` | `#0d0f14` | Pending tool output background. | `themes/Gentle.json` |
| `toolErrorBg` | `#2e1a1a` | Error tool output background. | `themes/Gentle.json` |
| `infoBg` | `#0d0f14` | Info background. | `themes/Gentle.json` |

### Gentleman-Sexy — hot-pink Pi theme

Source: `themes/Gentleman-Sexy.json`.

| Token | Value | Usage | Source |
| --- | --- | --- | --- |
| `bg` | `#060407` | Page background. | `themes/Gentleman-Sexy.json` |
| `bgPanel` | `#100A0F` | Panel background. | `themes/Gentleman-Sexy.json` |
| `bgElement` | `#100A0F` | Element or card background. | `themes/Gentleman-Sexy.json` |
| `userMessageBg` | `#2E0F1F` | User message surface. | `themes/Gentleman-Sexy.json` |
| `bgSubtle` | `#100A0F` | Subtle surface and custom message background. | `themes/Gentleman-Sexy.json` |
| `border` | `#563040` | Primary border and scrollbar thumb. | `themes/Gentleman-Sexy.json` |
| `borderSubtle` | `#2A1720` | Subtle border and disabled thinking. | `themes/Gentleman-Sexy.json` |
| `text` | `#F6EFF3` | Primary text. | `themes/Gentleman-Sexy.json` |
| `muted` | `#A78E9B` | Muted text. | `themes/Gentleman-Sexy.json` |
| `dim` | `#76616B` | Dim text. | `themes/Gentleman-Sexy.json` |
| `accent` | `#F43888` | Primary accent. | `themes/Gentleman-Sexy.json` |
| `deepPink` | `#BF0F50` | Search match background and markdown quote border. | `themes/Gentleman-Sexy.json` |
| `activePink` | `#FF4F9A` | Active accent, links, list bullet, maximum thinking. | `themes/Gentleman-Sexy.json` |
| `champagne` | `#E0C27A` | Custom message label, tool title, markdown heading/code, bash mode. | `themes/Gentleman-Sexy.json` |
| `violet` | `#C49BFF` | Syntax function and high thinking. | `themes/Gentleman-Sexy.json` |
| `pearl` | `#D2CBD0` | Success. | `themes/Gentleman-Sexy.json` |
| `softRose` | `#D7A0B8` | Syntax number. | `themes/Gentleman-Sexy.json` |
| `powderBlue` | `#A9C7EE` | Syntax type and added diff. | `themes/Gentleman-Sexy.json` |
| `warning` | `#F2B86D` | Warning color. | `themes/Gentleman-Sexy.json` |
| `error` | `#FF718F` | Error color and removed diff. | `themes/Gentleman-Sexy.json` |
| `selection` | `#28121E` | Selected background. | `themes/Gentleman-Sexy.json` |
| `toolPendingBg` | `#100A0F` | Pending tool output background. | `themes/Gentleman-Sexy.json` |
| `toolSuccessBg` | `#151316` | Success tool output background. | `themes/Gentleman-Sexy.json` |
| `toolErrorBg` | `#261019` | Error tool output background. | `themes/Gentleman-Sexy.json` |
| `infoBg` | `#100A0F` | Info background. | `themes/Gentleman-Sexy.json` |

### Install wizard palette

Source: `assets/install-wizard/wizard.css:8-24`.

| Token | Value | Usage | Source |
| --- | --- | --- | --- |
| `--bg` | `#1a1218` | Page background. | `assets/install-wizard/wizard.css` |
| `--bg-deep` | `#000000` | Deep background. | `assets/install-wizard/wizard.css` |
| `--surface` | `#20161e` | Surface. | `assets/install-wizard/wizard.css` |
| `--surface-1` | `#241822` | Elevated surface. | `assets/install-wizard/wizard.css` |
| `--surface-2` | `#342230` | Scrollbar surface. | `assets/install-wizard/wizard.css` |
| `--border` | `#342230` | Border. | `assets/install-wizard/wizard.css` |
| `--border-soft` | `#ffffff17` | Soft border. | `assets/install-wizard/wizard.css` |
| `--text` | `#f6eff3` | Text. | `assets/install-wizard/wizard.css` |
| `--text-muted` | `#a78e9b` | Muted text. | `assets/install-wizard/wizard.css` |
| `--text-faint` | `#76616b` | Faint text. | `assets/install-wizard/wizard.css` |
| `--accent` | `#f095c8` | Accent. | `assets/install-wizard/wizard.css` |
| `--accent-strong` | `#ff76c3` | Strong accent. | `assets/install-wizard/wizard.css` |
| `--accent-soft` | `#ffb1dd` | Soft accent. | `assets/install-wizard/wizard.css` |
| `--success` | `#b4e7c7` | Success. | `assets/install-wizard/wizard.css` |
| `--warning` | `#e0c27a` | Warning. | `assets/install-wizard/wizard.css` |
| `--error` | `#ff718f` | Error. | `assets/install-wizard/wizard.css` |
| `--info` | `#a9c7ee` | Info. | `assets/install-wizard/wizard.css` |

### Design canvas palette

Source: `assets/design-canvas/canvas.css:3-15`.

| Token | Value | Usage | Source |
| --- | --- | --- | --- |
| `--gd-bg` | `#111214` | Canvas background. | `assets/design-canvas/canvas.css` |
| `--gd-stage` | `#1a1b1e` | Stage background. | `assets/design-canvas/canvas.css` |
| `--gd-panel` | `#222327` | Panel background. | `assets/design-canvas/canvas.css` |
| `--gd-border` | `#3a3b40` | Border. | `assets/design-canvas/canvas.css` |
| `--gd-text` | `#ececee` | Text. | `assets/design-canvas/canvas.css` |
| `--gd-muted` | `#a9abb2` | Muted text. | `assets/design-canvas/canvas.css` |
| `--gd-accent` | `#8ab4ff` | Accent. | `assets/design-canvas/canvas.css` |
| `--gd-accent-text` | `#0b1220` | Accent text. | `assets/design-canvas/canvas.css` |
| `--gd-danger` | `#ff9b9b` | Danger. | `assets/design-canvas/canvas.css` |
| `--gd-focus` | `#ffd479` | Focus. | `assets/design-canvas/canvas.css` |
| `--gd-pin` | `#8ab4ff` | Pin. | `assets/design-canvas/canvas.css` |
| `--gd-pin-resolved` | `#7d8a7f` | Resolved pin. | `assets/design-canvas/canvas.css` |
| `--gd-success` | `#9be0a8` | Success. | `assets/design-canvas/canvas.css` |

### Shell-rework artboard tokens

Source: `design/shell-rework/02-proposal.html:10-23`; the same token block appears in the other shell-rework artboards.

#### Rose default — Gentleman-Cute

| Token | Value | Usage | Source |
| --- | --- | --- | --- |
| `--bg` | `#060407` | Background. | `design/shell-rework/02-proposal.html` |
| `--rail` | `#100A0F` | Rail. | `design/shell-rework/02-proposal.html` |
| `--user` | `#2A1523` | User message. | `design/shell-rework/02-proposal.html` |
| `--sel` | `#28121E` | Selection. | `design/shell-rework/02-proposal.html` |
| `--border` | `#563040` | Border. | `design/shell-rework/02-proposal.html` |
| `--text` | `#F6EFF3` | Text. | `design/shell-rework/02-proposal.html` |
| `--sec` | `#A78E9B` | Secondary text. | `design/shell-rework/02-proposal.html` |
| `--accent` | `#F095C8` | Accent. | `design/shell-rework/02-proposal.html` |
| `--accent-strong` | `#FFB1DD` | Accent strong. | `design/shell-rework/02-proposal.html` |
| `--success` | `#B4E7C7` | Success. | `design/shell-rework/02-proposal.html` |
| `--warning` | `#F2B86D` | Warning. | `design/shell-rework/02-proposal.html` |
| `--error` | `#FF718F` | Error. | `design/shell-rework/02-proposal.html` |
| `--thinking` | `#D7A0B8` | Thinking. | `design/shell-rework/02-proposal.html` |
| `--label` | `#E0C27A` | Label. | `design/shell-rework/02-proposal.html` |
| `--ok-bg` | `#151316` | OK background. | `design/shell-rework/02-proposal.html` |

#### Blue — Gentle

| Token | Value | Usage | Source |
| --- | --- | --- | --- |
| `--bg` | `#06080f` | Background. | `design/shell-rework/02-proposal.html` |
| `--rail` | `#0d0f14` | Rail. | `design/shell-rework/02-proposal.html` |
| `--user` | `#161D2E` | User message. | `design/shell-rework/02-proposal.html` |
| `--sel` | `#232A40` | Selection. | `design/shell-rework/02-proposal.html` |
| `--border` | `#313342` | Border. | `design/shell-rework/02-proposal.html` |
| `--text` | `#F3F6F9` | Text. | `design/shell-rework/02-proposal.html` |
| `--sec` | `#8394A3` | Secondary text. | `design/shell-rework/02-proposal.html` |
| `--accent` | `#7FB4CA` | Accent. | `design/shell-rework/02-proposal.html` |
| `--accent-strong` | `#7FB4CA` | Accent strong. | `design/shell-rework/02-proposal.html` |
| `--success` | `#B7CC85` | Success. | `design/shell-rework/02-proposal.html` |
| `--warning` | `#DEBA87` | Warning. | `design/shell-rework/02-proposal.html` |
| `--error` | `#CB7C94` | Error. | `design/shell-rework/02-proposal.html` |
| `--thinking` | `#8394A3` | Thinking. | `design/shell-rework/02-proposal.html` |
| `--label` | `#7FB4CA` | Label. | `design/shell-rework/02-proposal.html` |
| `--ok-bg` | `#1a2e1a` | OK background. | `design/shell-rework/02-proposal.html` |

#### Hot-pink — Gentleman-Sexy

| Token | Value | Usage | Source |
| --- | --- | --- | --- |
| `--user` | `#2E0F1F` | User message. | `design/shell-rework/02-proposal.html` |
| `--accent` | `#F43888` | Accent. | `design/shell-rework/02-proposal.html` |
| `--accent-strong` | `#FF4F9A` | Accent strong. | `design/shell-rework/02-proposal.html` |
| `--success` | `#D2CBD0` | Success. | `design/shell-rework/02-proposal.html` |
| `--thinking` | `#A78E9B` | Thinking. | `design/shell-rework/02-proposal.html` |

### Brand asset colors

| Color | Usage | Source |
| --- | --- | --- |
| `#120d16` | Banner background start and terminal rectangle. | `docs/assets/brand/gentle-pi-banner.svg:5,29` |
| `#251124` | Banner background middle. | `docs/assets/brand/gentle-pi-banner.svg:5` |
| `#0b0910` | Banner background end. | `docs/assets/brand/gentle-pi-banner.svg:5` |
| `#f095c8` | Banner rule, glow, accent stroke, terminal divider. | `docs/assets/brand/gentle-pi-banner.svg:6,7,11,26,27,28`; `docs/assets/brand/terminal-divider.svg` |
| `#d7a0b8` | Banner rule soft stop and terminal glyph. | `docs/assets/brand/gentle-pi-banner.svg:6,23,31` |
| `#fff7f1` | Banner wordmark and terminal glyph stroke. | `docs/assets/brand/gentle-pi-banner.svg:12,30` |

## Typography

### Font families

| Role | Stack | Source |
| --- | --- | --- |
| Install wizard sans | `Inter, "SF Pro Text", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif` | `assets/install-wizard/wizard.css:40` |
| Install wizard mono | `"IosevkaTerm NF", "Iosevka Term", "JetBrains Mono", ui-monospace, "SFMono-Regular", Menlo, Consolas, "DejaVu Sans Mono", monospace` | `assets/install-wizard/wizard.css:41` |
| Design canvas sans | `system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif` | `assets/design-canvas/canvas.css:16` |
| Design canvas mono | `ui-monospace, SFMono-Regular, Menlo, Consolas, monospace` | `assets/design-canvas/canvas.css` |
| Shell-rework terminal | `"IosevkaTerm NF", "Iosevka Term", "JetBrains Mono", ui-monospace, "SFMono-Regular", Menlo, Consolas, "DejaVu Sans Mono", monospace` | `design/shell-rework/02-proposal.html:15` |

The shell-rework font stack appears on line 15 of all six shell-rework HTML files.

### Type scale

| Role | Size / line-height | Weight | Source |
| --- | ---: | --- | --- |
| Shell terminal body | `13px / 17px` | normal | `design/shell-rework/02-proposal.html:15` |
| Wizard body base | `16px / 1.6` | normal | `assets/install-wizard/wizard.css:56` |
| Display headline | `clamp(34px, 4.6vw, 58px) / 1.08` | 800 | `assets/install-wizard/wizard.css:364-367` |
| Section title | `18px` | 700 | `assets/install-wizard/wizard.css:399-401` |
| Lead | `clamp(17px, 1.6vw, 18px)` | normal | `assets/install-wizard/wizard.css:388-390` |
| Card title | `16px` | 700 | `assets/install-wizard/wizard.css:441-442` |
| Card body | `15px` | normal | `assets/install-wizard/wizard.css:422` |
| Inline code | `.9em` | normal | `assets/install-wizard/wizard.css:86` |
| Detail code | `13px` | normal | `assets/install-wizard/wizard.css:458` |
| Topbar note | `12px / 1.4` | 500 | `assets/install-wizard/wizard.css:197` |
| Stage label | `12px / 1.2` | 600 | `assets/install-wizard/wizard.css:237` |
| Eyebrow / label | `12px / 1.4` | 600 | `assets/install-wizard/wizard.css:356,468,774,974` |
| Plan step marker | `12px / 1` | 600 | `assets/install-wizard/wizard.css:521` |
| Step icon | `12px / 1` | 700 | `assets/install-wizard/wizard.css:849` |
| Step status | `11px / 1.4` | 600 | `assets/install-wizard/wizard.css:859` |
| Caption / log body | `13px / 1.7` | normal | `assets/install-wizard/wizard.css:983` |
| Command line | `16px / 1.4` | normal | `assets/install-wizard/wizard.css:1055` |
| Progress count | `14px / 1.4` | 600 | `assets/install-wizard/wizard.css:780` |
| Wordmark mark | `14px / 1` | 700 | `assets/install-wizard/wizard.css:179` |
| Wordmark | `18px` | 800 | `assets/install-wizard/wizard.css:165-167` |
| Canvas base | `14px` | normal | `assets/design-canvas/canvas.css:16-17` |
| Canvas title | `15px` | 600 | `assets/design-canvas/canvas.css:57` |
| Canvas artboard title | `16px` | 600 | `assets/design-canvas/canvas.css:220-221` |
| Canvas meta / handoff | `12px` | normal | `assets/design-canvas/canvas.css:236` |
| Canvas pin | `12px` | 700 | `assets/design-canvas/canvas.css:360-361` |

## Spacing

No dedicated spacing-scale custom properties exist in the project sources. The following pixel values occur in layout, padding, gap, margin, sizing, radius, shadow, or width rules in the two CSS sources. They are recorded as observed values, not as an abstract scale.

Source: `assets/install-wizard/wizard.css`, `assets/design-canvas/canvas.css`.

| Value | Found in |
| ---: | --- |
| `1px` | border widths, hairline rules, hidden elements |
| `2px` | focus outlines, shadow offsets |
| `3px` | inset accent rings |
| `4px` | small gaps and padding |
| `5px` | topbar note padding |
| `6px` | pill gaps, button padding, badge padding |
| `8px` | common gap, padding, and shadow spread |
| `9px` | small spacing values |
| `10px` | wordmark gap, progress and layout gaps |
| `11px` | small status text |
| `12px` | label, gap, and padding value |
| `13px` | caption, code, and meta text |
| `14px` | wordmark mark, progress count, small label |
| `15px` | card body and note text |
| `16px` | topbar gap, card spacing, headline margin |
| `17px` | terminal line height |
| `18px` | section spacing and channel padding |
| `20px` | footer and consent padding |
| `22px` | card padding |
| `24px` | main padding, grid spacing, panel padding |
| `26px` | plan step marker height |
| `28px` | blocker and rail spacing |
| `30px` | shadow spread and error alert shadow |
| `32px` | progress spacing and footer bottom padding |
| `34px` | wordmark mark size |
| `36px` | block spacing and glow hover blur |
| `40px` | panel shadow blur |
| `46px` | primary button minimum height |
| `52px` | maximum panel padding |
| `56px` | main bottom padding |
| `58px` | maximum display headline size |
| `60px` | panel shadow spread |
| `80px` | design canvas world gap |
| `96px` | screenshot preview maximum height |
| `100px` | skip-link hidden top position |
| `120px` | hero glow inset |
| `160px` | screenshot preview maximum width |
| `240px` | channel grid minimum column width |
| `300px` | card grid minimum column width |
| `340px` | design canvas panel maximum width |
| `360px` | popover maximum width |
| `380px` | progress body minimum column width |
| `560px` | toast maximum width |
| `600px` | maximum content width values |
| `999px` | pill radius |
| `1040px` | topbar/main/footer content width |

## Radius

Source: `assets/install-wizard/wizard.css:25-28`, `assets/install-wizard/wizard.css`, `assets/design-canvas/canvas.css`.

| Token / value | Usage | Source |
| --- | --- | --- |
| `--radius-sm: 8px` | Small radius: buttons, skip link, popover-style surfaces. | `assets/install-wizard/wizard.css:25` |
| `--radius-md: 12px` | Medium radius: cards, alerts, progress, log. | `assets/install-wizard/wizard.css:26` |
| `--radius-lg: 16px` | Large radius: main wizard panel. | `assets/install-wizard/wizard.css:27` |
| `--radius-pill: 999px` | Pill radius: pills, progress track. | `assets/install-wizard/wizard.css:28` |
| `4px` | Badge, screenshot, and small rounded surfaces. | `assets/design-canvas/canvas.css:416,513` |
| `6px` | Code, buttons, comment items, popover. | `assets/install-wizard/wizard.css:90`; `assets/design-canvas/canvas.css:76` |
| `8px` | Popover and small wizard surfaces. | `assets/install-wizard/wizard.css`; `assets/design-canvas/canvas.css` |
| `10px` | Step rows. | `assets/install-wizard/wizard.css` |
| `13px 13px 13px 2px` | Design canvas pin. | `assets/design-canvas/canvas.css` |
| `50%` | Dots and circular step markers. | `assets/install-wizard/wizard.css` |

## Shadows

Source: `assets/install-wizard/wizard.css:30-32`, `assets/install-wizard/wizard.css`, `assets/design-canvas/canvas.css`.

| Token / value | Usage | Source |
| --- | --- | --- |
| `--glow: 0 10px 30px #f095c84d` | Primary accent glow. | `assets/install-wizard/wizard.css:30` |
| `--glow-hover: 0 14px 36px #f095c86b` | Hover glow. | `assets/install-wizard/wizard.css:31` |
| `--shadow-panel: 0 24px 60px #00000073, 0 0 40px #f095c81a` | Main panel shadow. | `assets/install-wizard/wizard.css:32` |
| `0 6px 18px #f095c826` | Wordmark mark shadow. | `assets/install-wizard/wizard.css:180` |
| `0 0 0 4px #f095c826, var(--glow)` | Current stage ring and glow. | `assets/install-wizard/wizard.css:275` |
| `inset 0 1px 0 #f095c81f` | Accent disclosure inset highlight. | `assets/install-wizard/wizard.css:428` |
| `0 10px 30px #ff718f14` | Error alert shadow. | `assets/install-wizard/wizard.css:726` |
| `0 0 16px #ffb1dd66` | Progress value glow. | `assets/install-wizard/wizard.css:803` |
| `inset 0 1px 0 #ffffff0a` | Log inset highlight. | `assets/install-wizard/wizard.css:936` |
| `0 2px 16px rgba(0, 0, 0, 0.5)` | Canvas artboard and frame shadow. | `assets/design-canvas/canvas.css:266` |
| `0 2px 8px rgba(0, 0, 0, 0.5)` | Shield hint shadow. | `assets/design-canvas/canvas.css:313` |
| `0 4px 16px rgba(0, 0, 0, 0.6)` | Back button shadow. | `assets/design-canvas/canvas.css:338` |
| `0 8px 32px rgba(0, 0, 0, 0.6)` | Popover and toast shadow. | `assets/design-canvas/canvas.css:470` |
| `0 0 0 calc(3px * var(--gd-inv-zoom, 1)) var(--gd-accent), 0 2px 16px rgba(0, 0, 0, 0.5)` | Chosen artboard frame. | `assets/design-canvas/canvas.css:260` |
| `inset 0 0 0 calc(2px * var(--gd-inv-zoom, 1)) var(--gd-accent)` | Shield hover inset accent. | `assets/design-canvas/canvas.css` |
| `inset 0 0 0 calc(3px * var(--gd-inv-zoom, 1)) var(--gd-focus)` | Shield focus inset focus color. | `assets/design-canvas/canvas.css` |

## Component rules

### Buttons

- Primary button uses accent background, page-background text, `8px` radius, `46px` minimum height, and `--glow`.
- Secondary/ghost buttons use transparent background, border, and text colors.
- Disabled buttons reduce opacity and remove cursor affordance.
- `:focus-visible` uses a `2px` accent outline with `2px` offset.
- Source: `assets/install-wizard/wizard.css`.

### Cards

- Cards use `--surface`, border, `12px` radius, and `22px 24px` padding.
- Card titles use `16px` weight `700`.
- Card body text uses `15px` muted text.
- Source: `assets/install-wizard/wizard.css`.

### Alerts

- Alerts use `--surface`, border, `12px` radius.
- The left border encodes state: info, success, warning, or error.
- Error alerts add an error-tinted shadow.
- Source: `assets/install-wizard/wizard.css`.

### Pills and labels

- Pills use `999px` radius, `12px / 1.4` monospace text, and soft borders.
- Accent pills use accent-tinted background and soft accent border.
- Source: `assets/install-wizard/wizard.css`.

### Progress

- Progress track is `10px` tall with pill radius.
- Track uses a faint white overlay.
- Progress value uses an accent-to-info gradient and soft glow.
- Source: `assets/install-wizard/wizard.css`.

### Steps and logs

- Steps use `10px` radius and state colors for done, running, failed, blocked, pending, and skipped.
- Terminal logs use `--bg-deep`, border, `12px` radius, and `13px / 1.7` monospace text.
- Source: `assets/install-wizard/wizard.css`.

### Design canvas components

- Pins use `13px 13px 13px 2px` radius, accent background, and resolved muted state.
- Focus states use `2px` `--gd-focus` outlines.
- Chosen artboards use accent ring plus soft shadow.
- Source: `assets/design-canvas/canvas.css`.

### Shell-rework terminal artboards

- Artboards use a `1440px` preview frame and a `180ch` terminal grid.
- They are terminal-expressible: monospace cells, theme foreground/background colors, bold, italic, underline, and no radius, shadow, or gradient.
- Theme toggles preview Gentle, Gentleman-Cute, and Gentleman-Sexy.
- Source: `design/shell-rework/*.html`.

## Logo / brand assets

| File | Format | Role | Source |
| --- | --- | --- | --- |
| `assets/gentle-logo-only.png` | PNG | Gentle Shell logo; Pi package image. | `assets/gentle-logo-only.png`; `package.json:59` |
| `docs/assets/brand/gentle-shell-banner.gif` | GIF | Gentle Shell banner. | `docs/assets/brand/gentle-shell-banner.gif` |
| `docs/assets/brand/gentle-pi-banner.svg` | SVG | Gentle-PI banner. | `docs/assets/brand/gentle-pi-banner.svg` |
| `docs/assets/brand/terminal-divider.svg` | SVG | Terminal divider. | `docs/assets/brand/terminal-divider.svg` |
| `docs/assets/features/audio-notifications.png` | PNG | Feature thumbnail: audio notifications. | `docs/assets/features/audio-notifications.png` |
| `docs/assets/features/gentle-shell.png` | PNG | Feature thumbnail: Gentle Shell. | `docs/assets/features/gentle-shell.png` |
| `docs/assets/features/agents-view.png` | PNG | Feature thumbnail: agents view. | `docs/assets/features/agents-view.png` |
| `docs/assets/features/command-palette.png` | PNG | Feature thumbnail: command palette. | `docs/assets/features/command-palette.png` |
| `docs/assets/features/changes-view.png` | PNG | Feature thumbnail: changes view. | `docs/assets/features/changes-view.png` |
| `docs/assets/features/profiles-routing.png` | PNG | Feature thumbnail: profiles routing. | `docs/assets/features/profiles-routing.png` |
