# SWG bar

[English](README.md) · **Deutsch** · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

[Offizielle Website](https://swgbar.com/de/) · [Download für Mac](https://swgbar.com/de/#pricing) · [Anleitungen](https://swgbar.com/de/guides/)

SWG bar ist eine native macOS-Menüleisten-App, mit der Sie HTTPS-Inspektion durch ein Secure Web Gateway (SWG) untersuchen können. Prüfen Sie Domain-Ergebnisse und Zertifikate auf Ihrem Mac und sehen Sie vorhandene lokale Ergebnisse mit der begleitenden Erweiterung in Chrome.

## Funktionen

- Beobachtete Domains finden und ihre letzten Prüfergebnisse ansehen.
- Aussteller, Gültigkeit, Fingerabdrücke und zugehörige Domains von Zertifikaten untersuchen.
- Die Zertifikatsprüfung von macOS mit einer unabhängigen Prüfung öffentlicher Stammzertifikate vergleichen.
- Vorhandene Domain-Ergebnisse der Mac-App in der Chrome-Symbolleiste anzeigen.

Analyse und Speicherung der Erkennungsdaten erfolgen auf dem Mac. Prüfungen öffnen separate TLS-Verbindungen; die Erweiterung liest vorhandene lokale Ergebnisse. Mehr dazu unter [Funktionsweise](https://swgbar.com/de/how-it-works/) und [Datenschutz](https://swgbar.com/de/privacy/).

## Erste Schritte

Voraussetzung: **macOS 14 oder neuer und Apple Silicon**. Die Testphase umfasst **14 tatsächliche Nutzungstage**; aktuelle Angebote stehen auf der Website.

1. Laden Sie das Installationspaket von der [offiziellen Website](https://swgbar.com/de/#pricing) herunter und folgen Sie der [Installationsanleitung](https://swgbar.com/de/install/).
2. Öffnen Sie SWG bar über die Menüleiste und prüfen Sie eine Domain und ihre Zertifikate.
3. Richten Sie bei Bedarf die [Chrome-Erweiterung](https://swgbar.com/de/chrome-extension/) ein.

Die Mac-App unterstützt Englisch, vereinfachtes und traditionelles Chinesisch, Japanisch und Koreanisch. Die mit der Mac-App 2.3.7 gebündelte Chrome-Erweiterung 2.1.13 unterstützt alle 12 Sprachen der Website. Updates im Chrome Web Store werden nach einer separaten Prüfung verfügbar; prüfen Sie die dort angezeigte Version.

## SWG umgehen oder eine TLS-Ausnahme nutzen?

Ein SWG-Bypass ändert den Netzwerkpfad einer Verbindung. Bei einer Ausnahme von der TLS-Inspektion kann der Verkehr weiterhin durch das Gateway fließen, ohne dort entschlüsselt zu werden. Eine öffentliche Zertifikatskette allein beweist keinen Bypass.

Lesen Sie den [Vergleich von SWG-Bypass und TLS-Ausnahme](https://swgbar.com/de/guides/swg-bypass-vs-tls-exception/) sowie die [Anleitung zur Erkennung von HTTPS-Inspektion](https://swgbar.com/de/guides/detect-https-inspection/).

**Stand: 24. Oktober 2026.** Veröffentlicht ist Version 2.3.7; der Domain-Bypass mit einem Klick ist für 2.4.0 vorgesehen. Aktuelle Hinweise finden Sie in den [Versionsinformationen](https://swgbar.com/de/releases/) und [Anleitungen](https://swgbar.com/de/guides/).

## Dokumentierte Messung und Hilfe

Die [Fallstudie zur Zertifikatsprüfung](https://swgbar.com/de/guides/certificate-check-case-study/) enthält eine datierte Messung von `swgbar.com:443`, wiederholbare OpenSSL-Befehle, macOS-Prüfergebnisse und eine separate Beobachtung mit dem Prüfcode von SWG bar. Die Ergebnisse gelten für die gemessenen Verbindungen und belegen keinen Gateway-Bypass.

Dies ist die offizielle öffentliche Projektübersicht. Öffentliche Fragen und Dokumentationsvorschläge können Sie als [Issue](https://github.com/nonbutAworker/swg-bar/issues) einreichen. Für private Anliegen: [support@swgbar.com](mailto:support@swgbar.com). Veröffentlichen Sie keine Lizenzschlüssel oder Browserverläufe.

[Über SWG bar](https://swgbar.com/de/about/) · [Datenschutz](https://swgbar.com/de/privacy/) · [Nutzungsbedingungen](https://swgbar.com/de/terms/)
