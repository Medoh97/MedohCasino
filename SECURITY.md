# Security & verification

MedohCasino is a single-player, fully **offline** Android casino game. This page exists so you can
independently verify that a build is safe before installing it.

## What it is
- A native Android app (Kotlin / Jetpack Compose) — card & dice casino games against an AI/dealer.
- 100% single-player and offline. No account, no login, no ads, no analytics, no trackers.
- Nothing you do in the app leaves your device.

## Permissions — and the only reasons they exist
- **INTERNET** — solely to check this GitHub Releases page for a newer version.
- **REQUEST_INSTALL_PACKAGES** — solely to install an update *you* explicitly choose to download in-app.

There are no permissions for contacts, location, camera, microphone, SMS, or your files.

## How to verify a download
Every release shows a **SHA-256** and ships a `SHA256SUMS.txt`.
1. Confirm your downloaded file matches the published hash:
   - Windows: `certutil -hashfile MedohCasino-<version>.apk SHA256`
   - macOS / Linux: `shasum -a 256 MedohCasino-<version>.apk`
2. Scan it on [VirusTotal](https://www.virustotal.com) (~70 antivirus engines): drag the APK in
   (free, no account needed), or open `https://www.virustotal.com/gui/file/<the-sha-256>` if it has
   already been scanned.

## Build provenance
Builds are produced by GitHub Actions and published here. The APK is a standard Android **debug**
build (debug-signed) and is not obfuscated.

## Contact
Questions about a specific build? Open an issue on this repository.
