# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This is a static asset repository for the Jyotish/OpenClaw ecosystem. It hosts binary files (images) that are served via GitHub raw URLs for use by other projects, primarily `openclaw-main/instagram-poster`.

## Structure

Assets follow this convention:

```
<project-name>/
└── <sub-module>/
    └── <asset-file>
```

Currently:
- `openclaw-main/instagram-poster/` — background templates for Instagram transit posts

## How assets are consumed

Assets are referenced by other projects via GitHub raw URLs:

```
https://raw.githubusercontent.com/inggonzalogarcia/jyotish-assets/main/<path-to-asset>
```

The consuming project (`instagram-poster`) references the image via the `TRANSIT_POST_DEFAULT_IMAGE_URL` environment variable in its `.env` file.

## Binary file handling

`.gitattributes` marks all image formats (`jpg`, `jpeg`, `png`, `gif`, `webp`) as binary to prevent line-ending normalization by Git. New image formats added to the repo should be registered there as well.
