# SWG bar

**English** · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**Detect HTTPS Inspection. Bypass SWG in One Click.**

[Official website](https://swgbar.com/en/) · [Download for Mac](https://swgbar.com/en/#pricing) · [Guides](https://swgbar.com/en/guides/)

SWG bar is a native macOS menu bar app for understanding HTTPS inspection by a secure web gateway (SWG). Inspect domain results and certificate evidence on your Mac, and view available local results in Chrome with the companion extension.

## What you can inspect

- **Domains:** find observed hosts and examine their latest probe results.
- **Certificate evidence:** inspect issuers, validity dates, fingerprints, and the domains associated with a certificate.
- **Trust results:** compare macOS certificate trust with an independent public-root check and review the evidence behind an inspection classification.
- **Chrome results:** view the Mac app's existing result for a domain from the browser toolbar.

Detection analysis and storage run locally on your Mac. Probes make separate outbound TLS connections; the Chrome extension reads existing local results. See [how SWG bar works](https://swgbar.com/en/how-it-works/) and the [privacy notice](https://swgbar.com/en/privacy/) for details.

## Get started

Requires **macOS 14 or later and Apple silicon**. The trial provides **14 days of actual use**; current plans are on the website.

1. Download the current installer from the [official website](https://swgbar.com/en/#pricing) and follow the [installation guide](https://swgbar.com/en/install/).
2. Open SWG bar from the menu bar. Use Domains and Certificates to examine a hostname and its supporting evidence.
3. Optionally follow the [Chrome extension setup](https://swgbar.com/en/chrome-extension/) to see available results while browsing.

The Mac app supports English, Simplified Chinese, Traditional Chinese, Japanese, and Korean. Chrome companion 2.1.13, bundled with Mac app 2.3.7, supports all 12 website languages. Chrome Web Store updates become available separately after review; check the version shown in the store.

## How to bypass SWG: routing and HTTPS inspection

If you are researching **how to bypass SWG** on macOS, first distinguish a route change from an inspection exception. To **bypass SWG** is to use a different network route for a connection; a TLS inspection exception can leave traffic flowing through the gateway without decrypting it. A public certificate chain alone cannot tell you which happened.

Read [SWG bypass vs. a TLS inspection exception](https://swgbar.com/en/guides/swg-bypass-vs-tls-exception/) and [how to detect HTTPS inspection](https://swgbar.com/en/guides/detect-https-inspection/) for the evidence to examine.

**Release status, checked October 24, 2026:** the published installer is 2.3.7. The one-click domain bypass workflow is planned for 2.4.0. Follow the [release information](https://swgbar.com/en/releases/) and [official guides](https://swgbar.com/en/guides/) for verified version-specific instructions.

## A documented certificate check

Our [certificate check case study](https://swgbar.com/en/guides/certificate-check-case-study/) records a dated check of `swgbar.com:443`, with OpenSSL commands you can repeat and macOS trust results. It also publishes a separate observation from SWG bar's released probe code. These results describe the measured connections; they do not establish that a gateway was bypassed or that another app used the same TLS connection.

## Questions and feedback

This is SWG bar's official public project overview. Use this repository's [issues](https://github.com/nonbutAworker/swg-bar/issues) for public product questions and documentation suggestions. For installation, orders, or private support, contact [support@swgbar.com](mailto:support@swgbar.com). Keep license keys and browsing history out of public issues.

[About SWG bar](https://swgbar.com/en/about/) · [Privacy](https://swgbar.com/en/privacy/) · [Terms](https://swgbar.com/en/terms/)
