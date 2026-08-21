# Syosetu Translate Releases

[中文](README.md) | **English**

This is the public distribution and update repository for Syosetu Translate. Android source code is kept in a private repository. This repository contains only signed and minified release APKs, `release-manifest.json`, `latest.json`, and public release notes.

## Download

- Release application ID: `com.wearshoes.syosetu`
- Minimum Android version: Android 8.0 (API 26)
- Downloads: [GitHub Releases](https://github.com/wearshoes/syosetu-releases/releases)
- Current update metadata: [`latest.json`](latest.json)

The debug application ID is `com.wearshoes.syosetu.debug`. Debug APKs are for local development only and are never published here. Debug and release builds can be installed together.

## Updates

The app reads `latest.json` and displays the same Chinese changelog as the corresponding GitHub Release. `latest.json` remains the Android client compatibility projection. Every Release also includes `release-manifest.json` using the standard `release-ops/release-manifest/v1` contract.

Release APKs must keep the same signing certificate and use monotonically increasing `versionCode` values.

## Integrity

```powershell
Get-FileHash .\syosetu-vX.Y.Z.apk -Algorithm SHA256
```

The result must equal `latest.json.sha256`. Every public Release contains exactly one release APK and no debug artifacts.

This is an unofficial personal reader. Novel content is loaded from the original site and is not archived or republished here. LLM credentials are supplied on the device and are not included in the APK or repository.
