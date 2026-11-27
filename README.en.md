# QuotaClock

[简体中文](./README.md) · **English**

<img src="./logo.png" width="80" alt="QuotaClock logo">

A Windows desktop dashboard for tracking AI quotas, reset countdowns, and local token usage across providers.

**[Download for Windows](https://github.com/PhiloKlein/-QuotaClock/releases)** · **QQ community `1135481515`**

## Join the community

Search for group **1135481515** in QQ to share feedback, report issues, or suggest the next model to support.

<details>
<summary>Show the QQ group QR code</summary>

<img src="./qq-group.png" width="240" alt="QR code for QuotaClock QQ group 1135481515">

</details>

## Quick start

1. Download and run `QuotaClock.exe` from the **Assets** section of a GitHub release.
2. Open **Settings → Data sources** and choose Codex, Gemini, or Claude.
3. Use **Add data source** for DeepSeek or a compatible JSON quota endpoint. Open Settings from the Windows tray to adjust appearance, startup, and alerts.

## Data sources

- **OpenAI Codex** reads account quotas through the signed-in Codex CLI.
- **Google Gemini** reads Antigravity shared quotas. AI Studio settings can test a project API key and open the official usage page.
- **Anthropic Claude** reads subscription snapshots from the Claude Code status line when Claude Code supplies quota data.
- **DeepSeek** shows the API account balance in CNY or USD.
- **Other services** can use a read-only JSON GET endpoint over HTTPS or loopback HTTP, with optional bearer authentication. A card supports up to two quota windows.

For a custom endpoint, return a `windows` array. Each window can use `remaining_percent` or a `remaining` / `limit` pair, with an optional `resets_at` in Unix seconds or RFC 3339.

```json
{"windows":[{"label":"Daily","remaining_percent":72,"resets_at":"2026-12-01T08:00:00Z"}]}
```

[Xiaohongshu](https://www.xiaohongshu.com/user/profile/5c0767606b58b7084fdc17f1) · [Bilibili](https://space.bilibili.com/2552988) · [Report an issue](https://github.com/PhiloKlein/-QuotaClock/issues) · [Third-party licenses](./THIRD-PARTY-LICENSE.txt)
