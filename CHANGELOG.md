# Changelog

## 0.1.1

### Fixes

- Fixed inbound image parsing for Zalo webhook events:
  - `message.image.received` now reads image URL from `photo_url` (correct field) instead of `photo`.
  - Restored image download pipeline in `handleImageMessage` so photo attachments are no longer skipped.

## 0.1.0

### Features

- Initial community fork of the Zalo Bot API plugin for OpenClaw.
- Independent channel id: `zalo_fixed` (safe to run alongside official `zalo`).
- Token-based auth (env/config/file), DM policies, polling + webhook modes.
- Text + image messaging with 2000-char chunking and media size caps.
- Multi-account support with per-account config.
