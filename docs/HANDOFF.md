# Handoff

**Updated:** 2026-11-20 | **Branch:** feature/wrap-up-2026-11-20 | **Phase:** none (maintenance)

## Current state
- The white and black 3G logo PNGs are live through GitHub Pages from `main` (`2e8b650`). The URLs and SHA-256 values are in README.md.
- Verified 2026-11-20: both URLs return 200 `image/png` without signing in, and the downloads match the README hashes. An unknown path returns 404. A gitleaks scan of the full history is clean.
- Repository settings, confirmed through the API:
  - public, default branch `develop`;
  - rulesets `protect-main-develop` and `require-pr`;
  - Wiki, Issues and Projects off;
  - secret scanning and push protection on;
  - Actions limited to GitHub-owned actions (the Pages build works under it);
  - Pages HTTPS enforced.
- Commits use a GitHub noreply address through a repo-local `user.email` (ADR 0001).
- `develop` (`7a07e1b`) holds ADR 0001 and the CHANGELOG entry on top of `main`. Nothing in it changes the published logos.

## In progress
None.

## Next steps
- Add other sizes or formats only when a platform asks for them, following README "Updating".
- Releasing `develop` to `main` is only needed when a logo changes; docs-only changes can wait.

## Open questions
See TODO.md.

## Context worth knowing
- This repository is public. Anything committed is visible to anyone and stays in history; check the commit email and the content before every push.
- File names are part of public URLs: never rename a logo file.
- Pages serves every tracked file at the site URL, including this one.
