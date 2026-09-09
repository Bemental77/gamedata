# gamedata

Static game-library assets for **caseybement.com**.

GitHub Pages serves this repo at `https://caseybement.com/gamedata/` — the *same
origin* as the main site, so pages fetching from here keep cross-origin isolation
(`SharedArrayBuffer`) and need no CORS. File paths mirror their old locations in
`Bemental77/Bemental77.github.io` exactly, so the only change on the site side is
a single `ASSET_BASE` prefix per page.

Why it was split out: the main site's Pages artifact was 9.07 GiB, and every push
— including a one-line HTML edit — re-uploaded the whole library. Deploys took
~960 s, so pushes arrived faster than deploys finished and cancelled each other,
and real fixes never reached production. Moving 211 files here drops that
artifact to 0.23 GiB.

Contents mirror: `gamecube/roms/`, `ps1/ps1Wasm/roms/`, `dreamcast/discs/`,
`n64/N64Wasm/roms/`, `gba/gbaWasm/roms/`.
