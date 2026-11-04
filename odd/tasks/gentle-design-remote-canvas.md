# Gentle Design remote canvas

Goal: allow the `gentle-design` canvas to be opened from another machine while preserving the current loopback-only default.

## Specs

S1. When `GENTLE_DESIGN_HOST` is unset, the canvas server binds `127.0.0.1` and behaves exactly as before.

S2. `GENTLE_DESIGN_HOST` may bind the canvas to another address, for example `192.168.1.10` or `0.0.0.0`.

S3. `GENTLE_DESIGN_PUBLIC_HOST` controls the public URL, allowed `Host` headers, and allowed `Origin` values.

S4. When `GENTLE_DESIGN_API_KEY` is set, the canvas requires that key in addition to the per-server token.

S5. The API key may be supplied by:
- an `HttpOnly` cookie named `gd_api_key`, set by `GET /TOKEN/login?key=KEY`;
- an `Authorization: Bearer KEY` header for API clients.

S6. When the canvas is bound outside loopback and no API key is configured, `startDesignCanvasServer` fails before opening the port.

S7. Existing tests continue to pass; new tests cover remote host, public URL, login cookie, Bearer auth, denied access, and static route behavior.

S8. The browser can still use `EventSource` and iframes. The cookie is enough for the canvas page and API requests; static artboard and asset routes remain readable through the token path.

## Tasks

T1. Add `host`, `publicHost`, and `apiKey` options to `DesignCanvasServerOptions`, plus validation.

T2. Bind the HTTP server to the configured host and update the post-bind assertion.

T3. Update `Host`, `Origin`, `ownOrigins`, `origin`, `artboardCsp`, and returned URLs.

T4. Add `GET /TOKEN/login?key=KEY` and API-key authentication for non-static routes.

T5. Wire `GENTLE_DESIGN_HOST`, `GENTLE_DESIGN_PUBLIC_HOST`, and `GENTLE_DESIGN_API_KEY` in `lib/gentle-design.ts`.

T6. Add tests for default behavior, remote host, login, Bearer auth, and denied access.

T7. Update `odd/tasks/gentle-design.md`, `docs/gentle-shell.md`, and `README.md`. Done: `609a51cbb`.

## Delivery

Forecast: about 419 authored changed lines. Strategy: `single-pr` for one coherent canvas-server behavior, with `609a51cbb` as the single PR slice unless follow-ups are added.

## Log

L1. User asked how to access the `gentle-design` canvas from another machine.

L2. User chose option 3: configurable host plus reinforced authentication.

L3. Implemented T1-T6 and committed `609a51cbb`. The full `design-canvas-server.test.ts` suite passed with `node --test --test-timeout=30000 --test-reporter=tap tests/design-canvas-server.test.ts` before documentation was committed.
