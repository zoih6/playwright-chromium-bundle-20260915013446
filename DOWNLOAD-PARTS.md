# Downloading the complete bundle from repository files

The complete archive is stored in numbered parts because GitHub limits individual Git files to 100 MB.

Download all files named `playwright-chromium-bundle.part-*` from this directory, then run:

```bash
cat playwright-chromium-bundle.part-* > playwright-chromium-bundle-linux-x64.tar.gz
sha256sum -c SHA256SUMS
```

The release asset remains available on the [Release page](../../releases/tag/v151.0.7922.34) as a single archive for authenticated users.
