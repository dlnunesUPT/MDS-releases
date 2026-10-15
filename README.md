# MDS — Mechanics Drawing System: releases

This repository holds only the published releases of MDS. The source is not here.

Each release has:

- `MDS-x.y.z.html` — the page. It opens in any browser and works offline.
- `MDS-x.y.z-setup.exe` — the Windows installer: MDS with its local calculator (OpenSees,
  sectionproperties and a Python 3.12 of its own), installed in `C:\MDS` for every user of
  the computer. It asks for administrator rights. It is not code-signed yet, so Windows may
  warn about an unknown publisher.
- `latest.json` and `latest.json.sig` — what an installed MDS reads to find out whether a newer
  version exists. The manifest is signed (Ed25519), and MDS refuses an update whose signature
  or checksum does not match.
- `.sha256` files for each download.

An installed MDS checks this repository at most once a day and offers the update on its page.

## Licence

© 2026 Daniel Luís Nunes. All rights reserved. MDS may not be copied, modified or
distributed without the written permission of the author; being able to download it from
here grants no licence.

The installer includes third-party software under its own terms; see
`THIRD-PARTY-NOTICES.txt` in the installation. OpenSees and OpenSeesPy are free for
education, research and internal use only; commercial use needs a licence from their owners.
