# openclaw-zalo-fixed

Community-maintained patched Zalo channel plugin for OpenClaw.

## Why this exists

This plugin is a community-maintained fork of the official Zalo channel plugin, so users can apply fixes quickly without waiting for upstream merge/release.

## Install (local path)

```bash
openclaw plugins install /path/to/openclaw-zalo-fixed
```

## Install (npm)

```bash
openclaw plugins install openclaw-zalo-fixed
```

## Channel config

Use `channels.zalo_fixed` (not `channels.zalo`):

```json5
{
  channels: {
    zalo_fixed: {
      enabled: true,
      botToken: "12345689:abc-xyz",
      dmPolicy: "pairing",
      webhookUrl: "https://example.com/zalo-webhook",
      webhookSecret: "your-secret-8-plus-chars",
      webhookPath: "/zalo-webhook"
    }
  }
}
```

Restart gateway after config changes.

## Notes

- Designed to run independently from official `@openclaw/zalo`.
- Safe for users who want to keep using OpenClaw updates while pinning Zalo fixes here.
