# v2 — domain-split feeds

Each file is a signed manifest (same `{keyIdentifier, payload, signature}`
envelope as the root `manifest.json`, key `roadrecce-data-2026-01`) but scoped
to one consumer, so a re-publish of one domain never disturbs the other.

| File | Products | Consumer |
|---|---|---|
| `routing.json` | `rescue`, `railway-crossings`, `rescue-routing`, `-skeleton`, `rescue-routing-<region>` — routing packs at **schema v11** — `point_obstacle` table (`data-2026-09-09-routing-v11` release) | the routing engine |
| `basemap.json` | `basemap-vector-<region>`, `basemap-raster-<region>` | the map service (not published yet) |

The repo root `manifest.json` stays the 2-product set the current TestFlight
build can decode.

Regenerated with `make manifest-routing` / `make manifest-basemap` in
`RoadRecce/Tools/DatasetPublisher`.
