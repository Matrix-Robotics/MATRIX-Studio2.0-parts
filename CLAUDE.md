# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repo Is

A parts library for MATRIX Robotics components used in BrickLink **Studio 2.0**. Users copy the files into Studio 2.0's `CustomParts` directory so the parts appear inside the software.

The installer tool (MATRIX Parts Updater) is maintained in a **separate project** and its compiled `.exe` / `.app` releases are dropped into this repo when ready.

## Parts File Conventions

Each MATRIX component requires three files with the same base name:

| Folder | Extension | Role |
|---|---|---|
| `parts/` | `.dat` | 3D geometry (LDraw format) |
| `collider/` | `.col` | Collision mesh |
| `connectivity/` | `.conn` | Snap/connection points |

File naming follows `MX{series}-{id}.ext` (e.g. `MX01-0003.dat`). A new component is complete only when all three files exist.

## Studio 2.0 Install Paths

Files must land under `CustomParts/` inside the Stud.io directory:

- **Windows:** `C:\Users\{user}\AppData\Local\Stud.io\CustomParts\`
- **macOS (global):** `/Applications/Studio 2.0/Stud.io/CustomParts/`
- **macOS (user):** `~/Applications/Studio 2.0/Stud.io/CustomParts/`

## GitHub Releases

The separate updater tool fetches from **GitHub Releases**, not from the main branch. When publishing new parts, create a tagged Release (e.g. `v1.0.4`) so the updater can detect the new version.
