# Cablox Runtime Components

This directory is the lightweight component catalog used by Cablox/Kblox Studio on Android.

- `manifest.json` is the source of truth for downloadable runtime components.
- The Android client must verify SHA-256 before installing a component.
- Unchanged local components are reused across app updates.
- Roblox Studio binaries, authentication material, cookies and user data are never stored here.
- Large redistributable binaries should be hosted as release assets or fetched from their upstream project; Git history should contain only small manifests/configuration.

The goal is to keep the APK small and make updates incremental: only a component whose version/hash changed should be downloaded again.
