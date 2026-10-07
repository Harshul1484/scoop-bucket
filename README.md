# Scoop bucket for oow

[![Tests](https://github.com/Harshul1484/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/Harshul1484/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/Harshul1484/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/Harshul1484/scoop-bucket/actions/workflows/excavator.yml)

[Scoop](https://scoop.sh) manifests for [oow (out-of-windows)](https://github.com/Harshul1484/out-of-windows),
a terminal-first Windows maintenance toolkit: cleanup, complete app uninstall, disk analyzer,
developer-artifact purge, installer cleanup, diagnostics and a live status dashboard.

## Install

```pwsh
scoop bucket add oow https://github.com/Harshul1484/scoop-bucket
scoop install oow/oow
```

Update with `scoop update oow`, remove with `scoop uninstall oow`. A Scoop install is managed
by Scoop: `oow update` and `oow remove` point you to these commands instead of changing it.

## Verifying

The manifest pins the SHA-256 of each release zip, taken from the release's `SHA256SUMS`;
Scoop refuses a download that does not match. Every release file also has a build-provenance
attestation (`gh attestation verify <file> --repo Harshul1484/out-of-windows`).

Microsoft Defender may flag `oow.exe` as a false positive; see
[DEFENDER.md](https://github.com/Harshul1484/out-of-windows/blob/main/docs/DEFENDER.md).

## Updates

The Excavator workflow checks for new oow releases every few hours and updates the manifest
(version, URLs and hashes from `SHA256SUMS`) automatically.

Report problems with the manifest here; problems with oow itself go to the
[oow issue tracker](https://github.com/Harshul1484/out-of-windows/issues).
