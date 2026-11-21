# TODO

## Open
- [ ] Delete the merged branch `feature/adr-0001-public-repo` (the maintainer decides when).
- [ ] Push protection is not proven by a negative test (it would mean pushing a fake token to a public repo).
- [ ] Deferred: Tier 2 (CI) is not recommended now. Outside platforms use the logo URLs, but the repo has no code to lint or test, and GitHub secret scanning with push protection covers secrets (assessed 2026-11-20). Re-raise if code or workflows are added.
- [ ] Deferred: no SCOPE.md. The README and ADR 0001 define the repo, and a retroactive scope isn't worth it for two files. Re-raise if the repo grows beyond logos.

## Done
