# 0001: A separate public repository hosts the logos

- **Status:** Accepted
- **Date:** 2026-11-20

## Context
Some platforms accept a logo only as a link to a publicly hosted image. The 3G logo lives in the internal design system repository, which is private, so its files can't be linked to.

## Decision
A separate public repository, `brand-public-logos`, holds byte-for-byte copies of the white and black 3G logo PNGs and serves them with GitHub Pages from the `main` branch. The internal design system stays the source of truth.

## Alternatives considered
- **Make the design system repository public.** It holds internal design work, tests and notes that shouldn't be public.
- **Raw file links (`raw.githubusercontent.com`).** No setup, but GitHub doesn't intend them as a CDN: they are rate-limited, and the URL includes the branch name.
- **Azure Blob Storage with a public container.** It works, but costs money and adds an Azure resource to manage, while Pages is free for a public repository.

## Consequences
- Each logo has a stable public URL. A file name can't change without breaking the platforms that link to it.
- Anything committed here is public, so the repository holds only the logos and the files that describe them. Secret scanning runs before every commit.
- A logo change is made in the design system first, then copied here. The README records each file's SHA-256 so a copy can be checked.
- Pages builds run on GitHub Actions, which is free for public repositories.
- A custom domain can be added later with a DNS record, but that would change the URLs platforms already use.
