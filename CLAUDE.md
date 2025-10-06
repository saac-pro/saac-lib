# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

SAAC Icons is an open pictogram library supporting Augmentative and Alternative Communication (AAC), education, and accessibility. The project distributes 10,000+ pictograms in consistent style under the SAAC Custom License v1.0.

**Key characteristics:**
- Icon library distribution project (not a code development project)
- Focuses on versioned releases with integrity verification
- All icons created with human-in-the-loop under Provenance & Authorship Policy
- Licensed under custom tiered licensing (free for individuals/nonprofits/small companies, paid for medium/large enterprises)

## Repository Structure

```
releases/           # Versioned icon releases
  v1.0/
    icons/svg/      # SVG format icons
    icons/png512/   # PNG format icons (512x512)
    manifest.json   # Metadata and icon catalog
    SHA256SUMS.txt  # Integrity checksums
    LICENSE         # License file
docs/               # Gallery and documentation site (planned)
.github/workflows/  # Release automation
```

## Release Management

### Build and Release Process

The project uses GitHub Actions for automated releases on version tags:

**Trigger a release:**
```bash
git tag -a v1.0 -m "Release v1.0"
git push origin v1.0
```

**Workflow steps (automated):**
1. Validates manifest.json syntax with `jq`
2. Generates SHA256 checksums for all SVG, PNG, and manifest files
3. Creates GitHub Release with checksums and release artifacts

**Manual checksum generation:**
```bash
find releases -type f \( -name '*.svg' -o -name '*.png' -o -name 'manifest.json' \) -exec sha256sum {} \; > SHA256SUMS.txt
```

**Validate manifest.json:**
```bash
jq . releases/*/manifest.json
```

### Manifest Structure

Each release includes a `manifest.json` with:
- Unique IDs for each pictogram
- Metadata (categories, keywords, descriptions)
- License reference
- Version information

## Git LFS Configuration

The repository uses Git LFS for binary assets:
- PNG files are tracked via LFS (`*.png filter=lfs`)
- SVG, JSON, and MD files are stored as text

**Before committing PNG files:**
```bash
git lfs track "*.png"
git lfs ls-files  # Verify LFS tracking
```

## Licensing Requirements

**SAAC Custom License v1.0** - always include attribution:
> "Pictogram source: SAAC Library (© SAAC sp. z o.o.), https://saac.pro"

**Tier structure:**
- Free: Individuals, non-profits, public institutions, companies ≤ €2M turnover
- Paid: Medium (€2-10M), Large (€10-50M), Very large (>€50M) companies

Contact `license@saac.pl` for commercial licensing.

## Security

**Report security issues privately to:** as@saac.pl (do not open public issues)

Supported versions:
- v1.0 (LTS) — supported until 2026-12-31
- Latest (Current) — rolling support

## Contact

- License inquiries: license@saac.pl
- Security issues: as@saac.pl
- General questions: as@saac.pl