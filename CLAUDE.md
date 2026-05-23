# CLAUDE.md

Agent instructions for `digittl/geojson`.

## Before doing any work

**Always read `CODEBASE.md` first.** It is the canonical map of this repo — what files are here and how they are used. Read it before making changes.

## Keeping CODEBASE.md current

If your change adds, removes, or renames a GeoJSON file — **update `CODEBASE.md` in the same PR**.

## Keeping CHANGELOG.md current

`CHANGELOG.md` follows [Keep a Changelog 1.1.0](https://keepachangelog.com/en/1.1.0/) and [SemVer](https://semver.org/). Add a bullet under `## [Unreleased]` for any file added, updated, or removed.

## House rules

- **Conventional Commits**: `feat:`, `fix:`, `chore:`, `docs:`
- This is a data-only repo — no build system, no runtime code
- GeoJSON files are large; avoid unnecessary edits to reduce diff noise
- Files are consumed as static assets — do not rename files without updating all consumers
