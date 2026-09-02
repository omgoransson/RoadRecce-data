# RoadRecce data

This repository publishes versioned, offline road-data packages used by the RoadRecce iOS application.

- `manifest.json` is an Ed25519-signed description of the current packages.
- Large GeoPackage files are immutable GitHub Release assets.
- RoadRecce activates a package only after verifying its exact size, SHA-256, signed metadata, and expected GeoPackage schema.

## Sources and licence

The files are derived from open data supplied by Trafikverket through Lastkajen. Trafikverket generally publishes its open data under Creative Commons CC0 1.0. The `Plankorsning väg-järnväg` delivery explicitly includes a CC0 1.0 declaration.

Database values are reference information and do not establish current road conditions or the absence of a restriction.

## Publication

Only the repository owner publishes releases. The private Ed25519 signing key is kept outside GitHub.
