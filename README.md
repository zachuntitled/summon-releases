# Summon releases

Public Sparkle artifacts for [Summon](https://github.com/zachuntitled/summon). **Source stays private.** This repo only hosts:

- `appcast.xml` (stable URL Sparkle fetches)
- `releases/Summon-<version>.dmg` on `main` (deploy-key publish; no PAT)

## URLs

- Appcast: https://raw.githubusercontent.com/zachuntitled/summon-releases/main/appcast.xml
- Example DMG: `https://github.com/zachuntitled/summon-releases/raw/main/releases/Summon-0.1.2.dmg`

## How a new tag updates users

1. Tag `v*` on `zachuntitled/summon`.
2. The private repo's **Release DMG** workflow builds the ad-hoc DMG, Sparkle-signs it with `SPARKLE_PRIVATE_KEY`, commits the DMG + appcast here over the write deploy key (`SUMMON_RELEASES_DEPLOY_KEY`), and still publishes the private GitHub Release on `summon`.
3. Installed builds with Sparkle fetch the appcast. Check for Updates installs the new DMG.

Do not put source, tokens, deploy keys, or the EdDSA private seed in this repository.
