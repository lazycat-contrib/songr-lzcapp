# Songr LazyCat App

LazyCat LPK v2 packaging for [Songr](https://github.com/roethlar/songr), a browser controller for Roon Core.

## Runtime

- Package: `community.lazycat.app.songr`
- Upstream image: `ghcr.io/roethlar/songr`
- Current packaged version: `1.1.1`
- Service port: `3333`
- Persistent data:
  - `/lzcapp/var/config:/app/config`
  - `/lzcapp/var/data:/app/data`

## Build

```bash
lzc-cli project release -o dist/songr.lpk
```

## GitHub Actions

`.github/workflows/lazycat.yml` uses `ca-x/lazycat-github-action/.github/workflows/lazycat.yml@v1`.

Required repository or organization secrets:

- `LZC_API_TOKEN` for LazyCat image delivery and official store publishing
- `APPSTORE_URL` and `APPSTORE_TOKEN` for private store publishing

Optional secrets:

- `LZC_API_HOST`
- `APP_ID`
- `PRIVATE_STORE_GROUP_CODES`
