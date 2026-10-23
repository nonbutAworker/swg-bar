# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · **日本語** · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

[公式サイト](https://swgbar.com/ja/) · [Mac 版をダウンロード](https://swgbar.com/ja/#pricing) · [ガイド](https://swgbar.com/ja/guides/)

SWG bar は、セキュア Web ゲートウェイ（SWG）による HTTPS 検査を確認するための、macOS ネイティブのメニューバーアプリです。Mac 上でドメインの検査結果や証明書を調べ、Chrome 拡張機能から既存のローカル結果を確認できます。

## 主な機能

- 観測したドメインを検索し、最新のプローブ結果を確認。
- 証明書の発行者、有効期間、フィンガープリント、関連するドメインを表示。
- macOS の証明書信頼評価と、公開ルート証明書に基づく独立した検証を比較。
- Mac アプリが保持するドメインの結果を Chrome のツールバーに表示。

検出データの分析と保存は Mac 内で行います。プローブは別の TLS 接続を作成し、拡張機能は既存のローカル結果を読み取ります。詳細は[仕組み](https://swgbar.com/ja/how-it-works/)と[プライバシー](https://swgbar.com/ja/privacy/)をご覧ください。

## はじめに

**macOS 14 以降、Apple シリコン搭載 Mac** に対応しています。無料試用は**実際に利用した 14 日間**です。現在のプランは公式サイトに掲載しています。

1. [公式サイト](https://swgbar.com/ja/#pricing)からインストーラーをダウンロードし、[インストールガイド](https://swgbar.com/ja/install/)に従ってください。
2. メニューバーから SWG bar を開き、ドメインと証明書の情報を確認します。
3. 必要に応じて [Chrome 拡張機能](https://swgbar.com/ja/chrome-extension/)を設定します。

アプリと拡張機能は英語、簡体字中国語、繁体字中国語、日本語、韓国語に対応しています。Web サイトとこのプロジェクト紹介は 12 言語に対応しています。

## SWG のバイパスと TLS 検査の例外

SWG をバイパスする場合、接続のネットワーク経路が変わります。TLS 検査の例外では、復号せずにゲートウェイ経由で通信を転送することがあります。公開証明書チェーンが見えるだけでは、経路が変わったとは判断できません。

[SWG バイパスと TLS 検査例外の違い](https://swgbar.com/ja/guides/swg-bypass-vs-tls-exception/)と、[HTTPS 検査を確認するガイド](https://swgbar.com/ja/guides/detect-https-inspection/)をご覧ください。

**2026 年 10 月 23 日時点**：公開インストーラーは 2.3.5 です。ワンクリックのドメインバイパスは 2.4.0 に向けて準備中です。確認済みの手順は[リリース情報](https://swgbar.com/ja/releases/)と[公式ガイド](https://swgbar.com/ja/guides/)に掲載します。

## 実測例とお問い合わせ

[証明書検証の事例](https://swgbar.com/ja/guides/certificate-check-case-study/)には、`swgbar.com:443` の測定日時、再実行できる OpenSSL コマンド、macOS の信頼評価結果、SWG bar の検査コードによる別の観測結果を記載しています。結果は測定した接続についての情報であり、ゲートウェイのバイパスを証明するものではありません。

このリポジトリは公式の公開プロジェクト紹介です。公開の質問やドキュメントの提案には [Issues](https://github.com/nonbutAworker/swg-bar/issues) をご利用ください。個別のお問い合わせは [support@swgbar.com](mailto:support@swgbar.com) へ。ライセンスキーや閲覧履歴は公開しないでください。

[SWG bar について](https://swgbar.com/ja/about/) · [プライバシー](https://swgbar.com/ja/privacy/) · [利用規約](https://swgbar.com/ja/terms/)
