# SWG bar

[English](README.md) · **Deutsch** · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**HTTPS-Inspektion erkennen. SWG mit einem Klick umgehen.**

[Offizielle Website](https://swgbar.com/de/) · [Download für Mac](https://swgbar.com/de/#pricing) · [Anleitungen](https://swgbar.com/de/guides/) · [CLI](https://swgbar.com/de/cli/) · [MCP](https://swgbar.com/de/mcp/)

SWG bar ist eine native macOS-Menüleisten-App zum Erkennen von **HTTPS-/SSL-Inspektion (Break-and-Inspect)** durch Enterprise-Secure-Web-Gateways (SWGs) – wie Zscaler, Netskope und Cloudflare Gateway – sowie zum Steuern der **domänenbasierten SWG-Umgehung per Klick**. Prüfen Sie Domain-Ergebnisse und Zertifikatsnachweise auf Ihrem Mac, zeigen Sie gespeicherte lokale Ergebnisse mit der begleitenden Erweiterung in Chrome an oder steuern Sie Prüfungen und Domain-Regeln über Terminal und KI-Coding-Agenten.

## Funktionen

- **HTTPS-/SSL-Inspektion & Zertifikatsnachweise:** inspizierte Domains erkennen, Aussteller, Gültigkeit, SHA-256-Fingerabdrücke und zugehörige Hostnamen prüfen sowie die macOS-Schlüsselbundprüfung (einschließlich per MDM installierter Stammzertifikate) mit einer unabhängigen Prüfung öffentlicher Stammzertifikate vergleichen.
- **Domänenbasierte SWG-Umgehung mit einem Klick:** ausgewählte Hostnamen auf autorisierten Netzwerken unter macOS über Menüleiste, CLI oder MCP ohne HTTPS-Entschlüsselung am Gateway routen.
- **Chrome-Erweiterung (`2.1.13`):** das in der Mac-App gespeicherte lokale Ergebnis für die aktuelle Domain direkt in der Browser-Symbolleiste einsehen.
- **Natives `swgbar`-CLI & MCP-Server:** Inspektionsdaten abfragen, TLS-Prüfungen bei Bedarf auslösen und Domain-Umgehungen im Terminal ([CLI-Anleitung](https://swgbar.com/de/cli/)) oder in MCP-kompatiblen KI-Agenten wie Claude Desktop, Cursor, Windsurf und Claude Code ([MCP-Anleitung](https://swgbar.com/de/mcp/)) verwalten.

Analyse und Speicherung der Erkennungsdaten erfolgen lokal auf dem Mac. Prüfungen öffnen separate ausgehende IPv4-TLS-Verbindungen; die Chrome-Erweiterung arbeitet schreibgeschützt über Chrome Native Messaging und liest vorhandene lokale Ergebnisse. Details stehen unter [Funktionsweise](https://swgbar.com/de/how-it-works/), [Datenschutz](https://swgbar.com/de/privacy/) und [Erweiterungsdatenschutz](https://swgbar.com/de/extension-privacy/).

## Erste Schritte

Voraussetzung: **macOS 14 oder neuer und Apple Silicon** (`arm64`). Die kostenlose Testphase umfasst **14 tatsächliche Nutzungstage** ohne Kreditkarte; aktuelle Einzel- und Team-Lizenzen finden Sie auf der [offiziellen Website](https://swgbar.com/de/#pricing).

1. Laden Sie das signierte und notarisierte `.pkg`-Installationspaket (`2.4.12`, Build `42`) von der [offiziellen Website](https://swgbar.com/de/#pricing) herunter und folgen Sie der [Installationsanleitung](https://swgbar.com/de/install/).
2. Öffnen Sie SWG bar über die Menüleiste und prüfen Sie Hostnamen, Stammzertifikate und SWG-Bypass-Regeln.
3. Verbinden Sie optional die [Chrome-Erweiterung](https://swgbar.com/de/chrome-extension/), richten Sie das [`swgbar`-CLI](https://swgbar.com/de/cli/) ein oder binden Sie den [MCP-Server](https://swgbar.com/de/mcp/) in Ihren KI-Client ein.

Die Mac-App `2.4.12` und die enthaltene Chrome-Erweiterung `2.1.13` unterstützen alle 12 Sprachen der Website. Updates im Chrome Web Store werden nach einer separaten Prüfung veröffentlicht; beachten Sie die dort angezeigte Version.

## Anleitungen: HTTPS-Inspektion, SWG-Bypass und Zertifikatsfehler in CLI/KI

Trennen Sie bei der Analyse unter macOS **Netzwerk-Routing** von **TLS-Entschlüsselung**. Ein SWG-Bypass ändert den Netzwerkpfad für einen Hostnamen; eine TLS-Inspektionsausnahme kann den Verkehr weiterhin unentschlüsselt durch das Gateway leiten. Eine öffentliche Zertifikatskette allein beweist daher keinen geänderten Pfad.

- [HTTPS- & SSL-Inspektion auf dem Mac erkennen](https://swgbar.com/de/guides/detect-https-inspection/) — Zertifikatsketten und lokale Stammzertifikate unter macOS prüfen.
- [Enterprise-SWG- & MDM-HTTPS-Inspektion auf dem Mac](https://swgbar.com/de/guides/enterprise-swg-https-inspection-macos/) — warum Zscaler, Netskope und Cloudflare Gateway trotz Aufbrechens der Verbindung ein normales Schloss-Symbol im Browser zeigen.
- [SWG auf dem Mac umgehen](https://swgbar.com/de/guides/how-to-bypass-swg/) — Einrichtung pro Domain, Freigabe der macOS-Netzwerkerweiterung, Neustartverhalten und Netzwerkgrenzen.
- [SWG-Umgehung vs. TLS-Inspektionsausnahme (Break-and-Inspect)](https://swgbar.com/de/guides/swg-bypass-vs-tls-exception/) — Unterschied zwischen Pfadänderung pro Domain und Entschlüsselungsausnahmen am Gateway.
- [SWG-TLS- & SSL-Zertifikatsfehler in CLI- und KI-Tools auf dem Mac beheben](https://swgbar.com/de/guides/swg-tls-certificate-errors-macos/) — `CERTIFICATE_VERIFY_FAILED` und Ausstellerfehler in `git`, `npm`, `Python`, `Claude Code` und `Cursor` lösen.

**Stand, geprüft am 18. November 2026:** Veröffentlicht ist **SWG bar 2.4.12** (Build `42`) mit signierter nativer Netzwerkerweiterung für die domänenbasierte SWG-Umgehung, `swgbar`-CLI und MCP-Server sowie der Chrome-Erweiterung `2.1.13`. SHA-256-Prüfsumme, Apple-Signatur und Notarisierung sind verifiziert. Siehe [Versionsinformationen](https://swgbar.com/de/releases/) und [offizielle Anleitungen](https://swgbar.com/de/guides/).

## Fragen und Feedback

Dies ist die offizielle öffentliche Projektübersicht. Öffentliche Fragen und Dokumentationsvorschläge können Sie als [Issue](https://github.com/nonbutAworker/swg-bar/issues) einreichen. Für Installation, Bestellungen oder private Anliegen: [support@swgbar.com](mailto:support@swgbar.com). Veröffentlichen Sie keine Lizenzschlüssel oder Browserverläufe.

[Über SWG bar](https://swgbar.com/de/about/) · [Datenschutz](https://swgbar.com/de/privacy/) · [Erweiterungsdatenschutz](https://swgbar.com/de/extension-privacy/) · [Nutzungsbedingungen](https://swgbar.com/de/terms/)
