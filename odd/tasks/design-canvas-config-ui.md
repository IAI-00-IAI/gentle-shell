# Gentle Design canvas configuration UI

Goal: let the user configure the `gentle-design` canvas from the Pi UI, while keeping the API key in the current session only and asking for it only when starting a remote canvas.

## Specs

S1. Add a `config` subcommand under `/gentle:design`:
- `/gentle:design config`
- `/gentle:design config show`
- `/gentle:design config reset`
- `/gentle:design config host <host>`
- `/gentle:design config public-host <host>`
- `/gentle:design config key`
- `/gentle:design config key <apiKey>`

S2. `config` stores the canvas configuration in the current Pi session only. It must not write a persistent configuration file.

S3. The effective canvas configuration is resolved from:
1. the current session configuration set by `config`;
2. `GENTLE_DESIGN_HOST`, `GENTLE_DESIGN_PUBLIC_HOST`, and `GENTLE_DESIGN_API_KEY`;
3. the existing defaults.

S4. When `/gentle:design open` starts a canvas bound outside loopback and no API key is already available from session configuration or environment, it asks for the API key once through the Pi UI.

S5. The API key requested during `open` is remembered for the rest of the current session. It must not be asked again for corrections, updates, or refreshed opens of the same running canvas.

S6. If the canvas is already running and the effective configuration changes, the next open uses the new configuration. If the running canvas would otherwise keep an old remote host, public host, or API key, it is closed and restarted when the new configuration requires it.

S7. `config` must validate the bind host and public host using the same rules as the canvas server.

S8. Existing behavior remains unchanged when no canvas configuration is set: the canvas still binds `127.0.0.1` by default.

S9. The full `design-canvas-server.test.ts` and `gentle-design.test.ts` suites must pass.
S10. When `/gentle:design` is typed without arguments, or with `help`, the available design subcommands are printed before any canvas action is taken.

## Tasks

| ID | Specs | Route | Status | Commit / evidence |
|----|-------|-------|--------|-------------------|
| T1 | S1-S9 (session state, resolution, masking) | delegated: context backstop | done | `lib/gentle-design.ts`: `DesignCanvasConfig`, `DesignCanvasConfigSource`, `DesignCanvasConfigSummary`, `DesignCanvasUIInput`, `maskDesignApiKey`, `resolveDesignCanvasConfig`, `requiresDesignCanvasApiKey`, `sameDesignCanvasConfig`, `askDesignCanvasApiKey`; tests 1-8 pass |
| T2 | S3, S4, S5, S6 | delegated: context backstop | done | `createDesignCanvas` tracks `designCanvasConfig`, `serverFor` restarts when `running.root` or `sameDesignCanvasConfig` changes, `open` asks for a missing remote API key once and stores it in session state, `stop` clears the running server; tests 75-80 pass |
| T3 | S1, S4, S5 | delegated: context backstop | done | `extensions/gentle-design.ts` parses `config`, `show`, `reset`, `host`, `public-host`, and `key`; `open` uses `askApiKey` and stores the result; remote open prompt tests pass |
| T4 | S2, S3, S4, S5, S7, S8, S9 | delegated: context backstop | done | added tests for default config, session-only config, invalid host/public-host, masked key, reset, remote open prompting, repeated open reuse, restart on config change, and no persistent config file; `tests/design-canvas-server.test.ts` and `tests/gentle-design.test.ts` pass |
| T5 | S9 | delegated: context backstop | done | docs and ODD document updated; commit `d34bba260`; `design-canvas-server.test.ts` and `gentle-design.test.ts` pass |
| T6 | S10 | inline: help path | done | `lib/gentle-design.ts` exposes `help`; no arguments or `help` print the available design subcommands; `extensions/gentle-design.ts` handles both; tests updated; `design-canvas-server.test.ts`, `gentle-design.test.ts`, and typecheck pass |

## Delivery

Forecast: about 380 authored changed lines. Strategy: `single-pr` for one coherent canvas configuration behavior, unless follow-ups are added.

## Log

L1. User said the introduced canvas configurations should be possible to configure from the UI.

L2. User selected a dedicated `/gentle:design config` command.

L3. User corrected the API key behavior: ask when opening the canvas, do not persist it, but keep it for the current session rather than asking for every correction or canvas update.

L4. Implemented T1-T5 and committed `d34bba260`. The focused suites passed: `node --test --test-timeout=30000 --test-reporter=tap tests/design-canvas-server.test.ts tests/gentle-design.test.ts`.

L5. User reported that the printed remote login URL omitted the per-server token, so `http://<publicHost>:<port>/login?key=...` returned 404. Fixed `lib/gentle-design.ts` to build the login URL as `/<token>/login?key=<apiKey>` and added a regression test in `tests/gentle-design.test.ts`; committed `1e724448c`.
