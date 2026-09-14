# Summon releases

Public Sparkle artifacts for [Summon](https://github.com/zachuntitled/summon). **Source stays private.** This repo only hosts:

- `appcast.xml` (stable URL Sparkle fetches)
- GitHub Release DMGs (`Summon-<version>.dmg`)

## URLs

- Appcast: https://raw.githubusercontent.com/zachuntitled/summon-releases/main/appcast.xml
- Example DMG: `https://github.com/zachuntitled/summon-releases/releases/download/v0.1.2/Summon-0.1.2.dmg`

## How a new tag updates users

1. Tag `v*` on `zachuntitled/summon`.
2. The private repo's **Release DMG** workflow builds the ad-hoc DMG, Sparkle-signs it with `SPARKLE_PRIVATE_KEY`, creates a public release here, and updates `appcast.xml`.
3. Installed builds with Sparkle fetch the appcast. Check for Updates installs the new DMG.

Do not put source, tokens, or the EdDSA private seed in this repository.
