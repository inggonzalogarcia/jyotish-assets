# jyotish-assets

> **Purpose**: Public static asset host (images) served via GitHub raw URLs for the BeAstral/jyotish ecosystem. **Status**: vigente. **Last updated**: 2026-07-06. **Related docs**: [CLAUDE.md](CLAUDE.md) · [claude-global.md](../claude-global.md).

Public static assets for the Jyotish/OpenClaw ecosystem.

## Structure

```
jyotish-assets/
└── openclaw-main/
    └── instagram-poster/
        └── CieloVedico-template.jpg   # Default background image for transit posts
```

## Usage

Reference assets via raw URL:

```
https://raw.githubusercontent.com/inggonzalogarcia/jyotish-assets/main/openclaw-main/instagram-poster/CieloVedico-template.jpg
```

Set in `instagram-poster/.env`:

```env
TRANSIT_POST_DEFAULT_IMAGE_URL=https://raw.githubusercontent.com/inggonzalogarcia/jyotish-assets/main/openclaw-main/instagram-poster/CieloVedico-template.jpg
```
