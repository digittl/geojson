# CODEBASE.md

Canonical map of `digittl/geojson` for AI agents and new contributors.

## Overview

Static GeoJSON data repository containing Australian geographic boundary files. Files are consumed as static assets by digittl mapping features (postcode/suburb lookups, delivery zones, etc.). No build system, no runtime — files are used directly.

## Files

| File | Description |
|---|---|
| `AUSWIDE.geojson` | Australia-wide boundary (all states combined, ~11 MB) |
| `Aus Postcode & State.geojson` | Australian postcodes with state annotations (~11 MB) |
| `australian-suburbs.geojson` | Australian suburb boundaries (~10 MB) |
| `NSW.geojson` | New South Wales postcode boundaries (~3 MB) |
| `QLD.geojson` | Queensland postcode boundaries (~2.4 MB) |
| `VIC.geojson` | Victoria postcode boundaries (~1.8 MB) |
| `WA.geojson` | Western Australia postcode boundaries (~1.9 MB) |
| `TAS.geojson` | Tasmania postcode boundaries (~845 KB) |
| `SA.geojson` | South Australia postcode boundaries (~685 KB) |
| `NT.geojson` | Northern Territory postcode boundaries (~399 KB) |

## Conventions

- Files are committed directly — no compression or pre-processing.
- File names are stable references used by consuming applications; do not rename without updating consumers.
- Source data is Australian government / ABS boundary data. Update from source when boundaries change.
- Files can be very large (up to ~11 MB each) — avoid loading all files simultaneously in consumer apps.

## Usage

Files are referenced by URL or path in consuming apps. For performance, prefer the state-level files over the australia-wide files where possible.
