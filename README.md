<div align="center">
  <img src="assets/wildflover-sigil-512.png" alt="Wildflover" width="128" height="128" />

  # Wildflover Database

  Official skin repository for the [Wildflover](https://wildflover.wf) application - curated, fixed, and ready to install.

  [Website](https://wildflover.wf) | [Discord](https://discord.gg/wildflover)

</div>

---

## About

**Wildflover Database** is the public skin depot consumed by Wildflover. Packages here are maintained for install reliability: broken paths, missing assets, and known load issues are fixed before they ship to users.

This repository is not a general-purpose skin dump. It exists so Wildflover can resolve, download, and apply skins against a stable catalog.

## What you get

- Skin packages prepared for Wildflover install flow
- Fixes applied to packages that fail or misbehave in-game
- Champion / skin / chroma catalog via `skins/index.json`
- Continuous updates aligned with current League patches

## Structure

```text
Wildflover-Database/
├── assets/
│   └── wildflover-sigil-512.png
├── skins/
│   ├── index.json                 # patch + champion / skin / chroma / form names
│   └── {championId}/
│       └── {skinId}/
│           ├── {skinId}.zip       # base skin package
│           └── {variantId}/
│               └── {variantId}.zip  # chroma / variant package
└── README.md
```

| Path | Role |
| --- | --- |
| `skins/index.json` | Catalog metadata (`patch`, champion keys, skin / chroma / form display names) |
| `skins/{championId}/` | Champion folder (Riot champion ID) |
| `skins/{championId}/{skinId}/` | Skin folder (`skinId` = champion ID x 1000 + skin number) |
| `{skinId}.zip` / `{variantId}.zip` | Packages Wildflover installs |

Examples:
- Base skin -> `skins/1/1001/1001.zip`
- Chroma / variant -> `skins/1/1013/1014/1014.zip`

## Usage

1. Install **Wildflover** from [wildflover.wf](https://wildflover.wf).
2. Open the app and browse or search skins from this database.
3. Install - Wildflover fetches the matching package from this repository and applies local fixes when needed.

Manual browsing of this repo is optional. Day-to-day use is through the application.

## Credits

Skin package development, repair, and maintenance by **copief**.

## Community

- **Discord:** [discord.gg/wildflover](https://discord.gg/wildflover)
- **Website:** [wildflover.wf](https://wildflover.wf)

## Disclaimer

Wildflover Database is a community project and is not affiliated with, endorsed by, or sponsored by Riot Games, Inc. League of Legends and related trademarks are property of Riot Games, Inc.
