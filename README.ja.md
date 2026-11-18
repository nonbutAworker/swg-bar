# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · **日本語** · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**HTTPS の復号・検査を検出。ワンクリックで SWG を回避。**

[公式サイト](https://swgbar.com/ja/) · [Mac 版をダウンロード](https://swgbar.com/ja/#pricing) · [ガイド](https://swgbar.com/ja/guides/) · [CLI](https://swgbar.com/ja/cli/) · [MCP](https://swgbar.com/ja/mcp/)

SWG bar は、Zscaler、Netskope、Cloudflare Gateway などの企業向けセキュア Web ゲートウェイ（SWG）による **HTTPS/SSL 検査**（Break-and-Inspect）を検出し、**ワンクリックでドメイン単位の SWG 回避**を管理できる macOS ネイティブのメニューバーアプリです。Mac 上でドメインの検査結果や証明書の根拠を調べ、Chrome 拡張機能から記録済みのローカル結果を確認できるほか、ターミナルや AI コーディングエージェントから検査やルール操作を実行できます。

## 主な機能

- **HTTPS/SSL 検査と証明書の根拠**：検査対象となっているドメインを特定し、証明書の発行者、有効期間、SHA-256 フィンガープリント、関連ホスト名を確認。macOS キーチェーンの信頼評価（MDM で配布されたルート CA を含む）と、公開ルート証明書に基づく独立した検証を比較します。
- **ワンクリックのドメイン単位 SWG 回避**：許可されたネットワーク環境で、選択したホスト名の通信をメニューバー、CLI、または MCP からゲートウェイの HTTPS 復号を経由しない経路へ切り替えます。
- **Chrome 拡張機能（`2.1.13`）**：Mac アプリに記録された現在のドメインのローカル検査結果を、ブラウザのツールバーから直接確認できます。
- **ネイティブ `swgbar` CLI & MCP サーバー**：ターミナル（[CLI ガイド](https://swgbar.com/ja/cli/)）や、Claude Desktop、Cursor、Windsurf、Claude Code などの MCP 対応 AI エージェント（[MCP ガイド](https://swgbar.com/ja/mcp/)）から、検査状況の取得、オンデマンド TLS プローブ、ドメイン単位の回避ルール操作を行えます。

検出データの分析と保存はすべて Mac ローカルで行います。プローブは個別の IPv4 TLS 接続を確立し、Chrome 拡張機能は Chrome Native Messaging 経由で既存のローカル結果を読み取るのみ（読み取り専用）です。詳細は[仕組み](https://swgbar.com/ja/how-it-works/)、[プライバシー](https://swgbar.com/ja/privacy/)、[拡張機能のプライバシー](https://swgbar.com/ja/extension-privacy/)をご覧ください。

## はじめに

**macOS 14 以降、Apple シリコン搭載 Mac**（`arm64`）に対応しています。無料試用はクレジットカード不要で、**実際に利用した 14 日間**のみカウントされます。個人向け・チーム向けの最新プランは[公式サイト](https://swgbar.com/ja/#pricing)に掲載しています。

1. [公式サイト](https://swgbar.com/ja/#pricing)から署名・公証済みの `.pkg` インストーラー（`2.4.12`、ビルド `42`）をダウンロードし、[インストールガイド](https://swgbar.com/ja/install/)に従ってセットアップします。
2. メニューバーから SWG bar を開き、**概要**、**ドメイン**、**証明書**からホスト名、ルート CA、ドメイン別の SWG 回避設定を確認します。
3. 必要に応じて [Chrome 拡張機能](https://swgbar.com/ja/chrome-extension/)、[CLI ツール `swgbar`](https://swgbar.com/ja/cli/)、または AI クライアント向けの [MCP サーバー](https://swgbar.com/ja/mcp/)を設定します。

Mac アプリ `2.4.12` と同梱の Chrome 拡張機能 `2.1.13` は、Web サイトの全 12 言語に対応しています。Chrome ウェブストアの更新は審査後に別途配信されるため、ストアに表示されるバージョンをご確認ください。

## ガイド：HTTPS 検査、SWG 回避、CLI・AI ツールの証明書エラー

macOS 上で HTTPS 検査や回避方法を調べる際は、**ネットワーク経路の切り替え**と **TLS 復号の除外**を区別してください。SWG の回避は対象ホスト名の通信経路を変更しますが、ゲートウェイ側の TLS 検査除外設定では復号しないままゲートウェイ経由で通信が流れることがあります。そのため、公開証明書チェーンが見えるだけでは経路変更の証明にはなりません。

- [Mac で HTTPS・SSL 検査（インスペクション）を検出する方法](https://swgbar.com/ja/guides/detect-https-inspection/) — macOS 上で証明書チェーンとローカルルート CA を確認する手順。
- [Mac における企業向け SWG と MDM の HTTPS 検査（インスペクション）](https://swgbar.com/ja/guides/enterprise-swg-https-inspection-macos/) — Zscaler、Netskope、Cloudflare Gateway 環境で MDM ルート CA によりブラウザの鍵アイコンが維持される仕組み。
- [Mac で SWG を回避する方法](https://swgbar.com/ja/guides/how-to-bypass-swg/) — ドメイン単位の設定手順、macOS ネットワーク拡張の承認、再起動時の動作、ネットワーク条件。
- [SWG 回避と TLS 検査の除外設定（Break-and-Inspect）の違い](https://swgbar.com/ja/guides/swg-bypass-vs-tls-exception/) — ドメイン単位の経路制御とゲートウェイ上の復号除外の違い。
- [Mac の CLI・AI ツールにおける SWG TLS/SSL 証明書エラーを解決する方法](https://swgbar.com/ja/guides/swg-tls-certificate-errors-macos/) — `git`、`npm`、`Python`、`Claude Code`、`Cursor` で発生する `CERTIFICATE_VERIFY_FAILED` などの証明書エラーへの対処法。

**2026 年 11 月 18 日確認**：現在の公開バージョンは **SWG bar 2.4.12**（ビルド `42`）で、署名済みのネイティブネットワーク拡張によるドメイン別 SWG 回避、`swgbar` CLI および MCP サーバー、Chrome 拡張機能 `2.1.13` を含みます。パッケージの SHA-256 チェックサム、Apple 署名、公証を確認済みです。詳細は[リリース情報](https://swgbar.com/ja/releases/)と[公式ガイド](https://swgbar.com/ja/guides/)をご覧ください。

## 質問とフィードバック

このリポジトリは公式の公開プロジェクト紹介です。公開の質問やドキュメントの提案には [Issues](https://github.com/nonbutAworker/swg-bar/issues) をご利用ください。インストール、注文、個別のお問い合わせは [support@swgbar.com](mailto:support@swgbar.com) へご連絡ください。ライセンスキーや閲覧履歴は公開しないでください。

[SWG bar について](https://swgbar.com/ja/about/) · [プライバシー](https://swgbar.com/ja/privacy/) · [拡張機能のプライバシー](https://swgbar.com/ja/extension-privacy/) · [利用規約](https://swgbar.com/ja/terms/)
