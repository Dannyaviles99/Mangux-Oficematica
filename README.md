# Mangux releases

Signed Android packages of Mangux and their catalogue. **No source code lives here.**

| File | What it is |
|---|---|
| `versions.json` | The catalogue: for each app its package, version, versionCode, APK name, download address, size, SHA-256, signing certificate, publication date and release notes. |
| `versions.json.sig` | Ed25519 signature of `versions.json`. Mangux Ofimática refuses a catalogue whose signature does not match. |
| `notes/<app>-<version>.md` | Release notes. |
| Releases `<app>-v<version>` | The signed APKs. |

Mangux Ofimática reads `versions.json`, offers only newer, compatible, correctly signed packages, checks each download's SHA-256 and signing certificate, and asks Android to install it.
