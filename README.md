# keepass-web

A single-file, self-contained KDBX password manager for the browser.

- No build step required to use the distributable
- Vanilla HTML5/CSS/JS — no frameworks, no external libraries
- WebCrypto API is the only browser runtime dependency
- No data persists outside in-memory browser context

## Distributables

| File | Purpose |
|------|---------|
| `keepassweb-0x67.html` | KDBX 3.1 and 4.x database support |
| `keepassweb.html` | Router, identifies database format and links to the correct file |

Each released file carries a published SHA-256 checksum. See [REPRODUCING.md](https://github.com/keepass-web/build/blob/main/REPRODUCING.md) for independent verification instructions.

## Development

```sh
npm ci
npm run typecheck
npm run lint
npm test
```

The build step (`npm run build`) requires the `keepass-web/build` tools checked out at `.build/` and is run by CI only.
