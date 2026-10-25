# Express Upgrade Audit

Upgrade-audit package for our Node service, prepared ahead of sprint planning.

## Pinned version

Our Node service is pinned to **Express 4.21.2** (published 2024-12-05).

Release notes for 4.21.2 (https://github.com/expressjs/express/releases/tag/4.21.2) list the following changes:

- Add funding field (v4) - @bjohansebas (PR #6065)
- deps: path-to-regexp@0.1.11 - @blakeembrey (PR #5956)
- deps: bump path-to-regexp@0.1.12 - @jonchurch (PR #6209)
- Release: 4.21.2 - @UlisesGascon (PR #6094)

## Latest version

- npm-advertised latest version: **Express 5.3.0** (npm `latest` dist-tag)
- Release date: 2026-10-09
- GitHub's latest release is also v5.3.0, so npm and GitHub agree on the latest version.

Headline changes in v5.3.0 (https://github.com/expressjs/express/releases/tag/v5.3.0):

- Fixed HTTP header conflict between Content-Length and Transfer-Encoding in `res.send()` (PR #4893 / #7459)
- Upgraded `qs` to ^6.16.0, fixing CVE-2026-2391, CVE-2026-82417 and CVE-2026-82562 (arrayLimit bypasses in comma parsing and a DoS via an attacker-controlled isBuffer) (PRs #7057, #7478, #7305)
- Upgraded `proxy-addr` to ^2.0.8, fixing CVE-2026-90711 (PR #7474)
- Allow conditional revalidation for QUERY requests via `req.fresh` (PR #7366)
- Improved HTML structure in `res.redirect()` responses (DOCTYPE, title, body tags) (PR #5167)
- `app.render` now handles options set to null correctly (PR #6903)
- Upgraded `content-type` to ^2.0.0 (faster parsing, ~1.5x in `res.send()`; charset handling keeps existing parameters and no longer throws on unparseable Content-Type) and `type-is` to ^2.1.0 (PR #7234)
- Default error handler now logs the full error object (Error.cause, etc.) (PR #6464)
- Upgraded `content-disposition` to ^2.0.1: valid HTTP-token file names are no longer quoted in the Content-Disposition header from `res.download()`, `res.attachment()` and `res.sendFile()` (PR #7233)
- Upgraded `body-parser` to ^2.3.0, fixing CVE-2026-12590 (invalid `limit` previously disabled body-size enforcement, allowing DoS; it now throws at parser initialization) (PR #7390)
- Performance: avoid duplicate Content-Type header processing in `res.send()` for string responses without an explicit Content-Type (PR #6991)

## Upstream issue status

The first issue/PR referenced in the 4.21.2 release notes is PR #6065:

- Number: #6065
- Title: "Add funding field (v4)"
- Author: @bjohansebas
- Current state: **Closed** - the pull request was merged into the 4.x line on 2024-10-20 (merged by @UlisesGascon).
- Link: https://github.com/expressjs/express/pull/6065
