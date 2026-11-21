# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Public logo files `logos/3g-logo-white.png` and `logos/3g-logo-black.png` (copies of the design system originals), served by GitHub Pages from `main`, so platforms that need a logo at a public URL can link to them (ADR 0001).

### Changed
- The README update procedure now says changes arrive "by pull request", and the pre-commit configuration comment no longer names workstation-specific security rules. Both are part of the rebuilt initial commit.

### Security
- Repository settings: secret scanning and push protection on; Wiki, Issues and Projects off; Actions limited to GitHub-owned actions. Commits use a GitHub noreply address, so no personal or company email appears in public history.
