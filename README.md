# brand-public-logos

Public hosting for the 3G logo, for platforms that need a logo published at a public URL.

The logos are served by GitHub Pages from the `main` branch.

| Logo | Use on | URL |
|---|---|---|
| White | dark backgrounds | https://3g-productions-llc.github.io/brand-public-logos/logos/3g-logo-white.png |
| Black | light backgrounds | https://3g-productions-llc.github.io/brand-public-logos/logos/3g-logo-black.png |

Both are PNG, 978 × 254 pixels, with a transparent background.

## Integrity

| File | SHA-256 |
|---|---|
| `logos/3g-logo-white.png` | `8c337e1193c2219fb4415ce1355069e815fdd181755e73553fd37d071d78751d` |
| `logos/3g-logo-black.png` | `56e4d5ccafc81cb3523aea3608e84bb87c57faae79a2063a9f77d9b06157b74b` |

The source of truth is 3G's internal design system. These files are byte-for-byte copies of it. To change a logo, change it there first, then copy it here and update this table.

## Updating

1. On a `feature/` branch, replace the file under `logos/` and update the SHA-256 table above.
2. Merge into `develop` by pull request.
3. Merge `develop` into `main` by pull request. Pages republishes `main` within a few minutes.

Keep a file's name when it changes, because platforms link to the URL. A new variant gets a new file name.

## Contributing

Pre-commit hooks scan for secrets and block direct commits to `main` and `develop`:

```bash
py -m pre_commit install
```

The secret scan uses the official gitleaks binary, version 8.30.1 or later (`winget install Gitleaks.Gitleaks`).

This repository is public. Commit nothing except the published logos and the files that describe them.

## Trademark

The 3G name and logo are trademarks of 3G Productions, LLC. They are published here so that partners and platforms can display them when referring to 3G. No licence is granted to modify them or to use them in a way that suggests endorsement.
