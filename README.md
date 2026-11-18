# SWG bar

**English** · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**Detect HTTPS Inspection. Bypass SWG in One Click.**

[Official website](https://swgbar.com/en/) · [Download for Mac](https://swgbar.com/en/#pricing) · [Guides](https://swgbar.com/en/guides/) · [CLI](https://swgbar.com/en/cli/) · [MCP](https://swgbar.com/en/mcp/)

SWG bar is a native macOS menu bar app for detecting **HTTPS/SSL inspection (break-and-inspect)** by enterprise secure web gateways (SWGs)—such as Zscaler, Netskope, and Cloudflare Gateway—and managing **one-click per-domain SWG bypass**. Inspect domain results and certificate evidence on your Mac, view recorded local results in Chrome with the companion extension, or automate checks and domain rules from Terminal and AI coding agents.

## Capabilities

- **HTTPS/SSL inspection & certificate evidence:** identify inspected domains, examine certificate issuers, validity dates, SHA-256 fingerprints, and associated hostnames, and compare macOS Keychain trust (including MDM-installed root CAs) with an independent public-root check.
- **One-click per-domain SWG bypass:** route selected hostnames on macOS without gateway HTTPS decryption when authorized, from the menu bar, CLI, or MCP.
- **Chrome companion (`2.1.13`):** view the Mac app's recorded local result for the current domain directly from the browser toolbar.
- **Native `swgbar` CLI & MCP server:** query inspection telemetry, trigger on-demand TLS probes, and toggle per-domain bypass from Terminal ([CLI guide](https://swgbar.com/en/cli/)) or MCP-compatible AI coding agents such as Claude Desktop, Cursor, Windsurf, and Claude Code ([MCP guide](https://swgbar.com/en/mcp/)).

Detection analysis and storage run locally on your Mac. Probes open separate outbound IPv4 TLS connections; the Chrome extension is read-only and reads existing local results via Chrome Native Messaging. See [how SWG bar works](https://swgbar.com/en/how-it-works/), the [privacy notice](https://swgbar.com/en/privacy/), and the [extension privacy notice](https://swgbar.com/en/extension-privacy/) for details.

## Get started

Requires **macOS 14 or later and Apple silicon** (`arm64`). The free trial provides **14 days of actual use** with no credit card required; current Personal and Team plans are on the [official website](https://swgbar.com/en/#pricing).

1. Download the signed and notarized `.pkg` installer (`2.4.12`, build `42`) from the [official website](https://swgbar.com/en/#pricing) and follow the [installation guide](https://swgbar.com/en/install/).
2. Open SWG bar from the menu bar. Use **Overview**, **Domains**, and **Certificates** to examine hostnames, root CAs, and per-domain SWG bypass controls.
3. Optionally follow the [Chrome extension setup](https://swgbar.com/en/chrome-extension/), configure the [`swgbar` CLI](https://swgbar.com/en/cli/), or connect the [MCP server](https://swgbar.com/en/mcp/) to your AI client.

Mac app `2.4.12` and its bundled Chrome companion `2.1.13` support all 12 website languages. Chrome Web Store updates become available separately after review; check the version shown in the store.

## Guides: HTTPS inspection, SWG bypass, and CLI/AI certificate errors

If you are researching **how to bypass SWG** or troubleshooting HTTPS interception on macOS, separate **network routing** from **TLS decryption**. To **bypass SWG** is to use a route outside gateway decryption for a hostname; a TLS inspection exception can leave traffic flowing through the gateway without decrypting it, so a public certificate chain alone does not prove a route change.

- [How to detect HTTPS & SSL inspection on a Mac](https://swgbar.com/en/guides/detect-https-inspection/) — verify certificate chains and local root CAs on macOS.
- [Enterprise SWG & MDM HTTPS inspection on a Mac](https://swgbar.com/en/guides/enterprise-swg-https-inspection-macos/) — why Zscaler, Netskope, and Cloudflare Gateway keep browser lock icons intact via MDM root CAs.
- [How to bypass SWG on a Mac](https://swgbar.com/en/guides/how-to-bypass-swg/) — step-by-step per-domain bypass setup, macOS network extension approval, restart behavior, and network boundaries.
- [SWG bypass vs. TLS inspection exception](https://swgbar.com/en/guides/swg-bypass-vs-tls-exception/) — differences between per-domain routing and gateway decryption exceptions.
- [Fix SWG TLS & SSL certificate errors in CLI and AI tools on a Mac](https://swgbar.com/en/guides/swg-tls-certificate-errors-macos/) — resolve `CERTIFICATE_VERIFY_FAILED` and local issuer errors in `git`, `npm`, `Python`, `Claude Code`, and `Cursor`.

**Release status, checked November 18, 2026:** the published release is **SWG bar 2.4.12** (build `42`), including the signed native network extension for per-domain SWG bypass, the `swgbar` CLI and MCP server, and Chrome companion `2.1.13`. Package SHA-256 checksum, Apple code signature, and notarization have been verified. See the [release information](https://swgbar.com/en/releases/) and [official guides](https://swgbar.com/en/guides/).

## Questions and feedback

This is SWG bar's official public project overview. Use this repository's [issues](https://github.com/nonbutAworker/swg-bar/issues) for public product questions and documentation suggestions. For installation, orders, or private support, contact [support@swgbar.com](mailto:support@swgbar.com). Keep license keys and browsing history out of public issues.

[About SWG bar](https://swgbar.com/en/about/) · [Privacy](https://swgbar.com/en/privacy/) · [Extension privacy](https://swgbar.com/en/extension-privacy/) · [Terms](https://swgbar.com/en/terms/)
