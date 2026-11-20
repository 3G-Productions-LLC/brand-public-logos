# brand-public-logos

Public hosting for the 3G logo (GitHub Pages from `main`), for platforms that need a logo at a public URL.

**This repository is public.** Commit nothing except the published logos and the files that describe them: no internal hostnames, email addresses, paths, credentials or internal project details.

## Target platform
GitHub Pages, served from the `main` branch root. There is no code and no build (`.nojekyll`).

## Commands
- Lint: `py -m pre_commit run --all-files` (gitleaks, branch guard)
- Test: none. After a change reaches `main`, check each URL in README.md answers 200 with `Content-Type: image/png` and matches its SHA-256.

## Structure
- `logos/`: the published logos. File names are part of public URLs; never rename one.
- `docs/decisions/`: ADRs.

## References
- Handoff (where work stands): docs/HANDOFF.md
- Decisions: docs/decisions/
