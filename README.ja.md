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

Mac アプリ 2.4.12 と同梱の Chrome 拡張 2.1.13 は、Web サイトの全 12 言語に対応しています。Chrome ウェブストアの更新は審査後に別途配信されるため、ストアに表示されるバージョンを確認してください。

## SWG のバイパスと TLS 検査の例外

SWG をバイパスする場合、接続のネットワーク経路が変わります。TLS 検査の例外では、復号せずにゲートウェイ経由で通信を転送することがあります。公開証明書チェーンが見えるだけでは、経路が変わったとは判断できません。

[SWG バイパスと TLS 検査例外の違い](https://swgbar.com/ja/guides/swg-bypass-vs-tls-exception/)と、[HTTPS 検査を確認するガイド](https://swgbar.com/ja/guides/detect-https-inspection/)をご覧ください。

2026 年 11 月 4 日に確認済みです。正式版 2.4.12（ビルド 42）のインストーラは公開 SHA-256 と一致し、Apple の署名・公証検証に合格しました。インストール済みアプリとネイティブネットワーク拡張も一致し、同梱の Chrome 拡張は 2.1.13 です。有効化、無効化、終了、再起動の実測は以下に記載しています。

[操作手順](https://swgbar.com/ja/guides/how-to-bypass-swg/) · [実測の詳細と制限](https://swgbar.com/ja/guides/certificate-check-case-study/)

## 実測例とお問い合わせ

[実測の詳細と制限](https://swgbar.com/ja/guides/certificate-check-case-study/)

SWG bar 2.4.12 で `www.doubao.com:443` への 6 回の接続をテストしたところ、バイパスを無効にした状態とアプリ終了時には検査用の証明書チェーンが、有効にした状態と復元後には公開証明書チェーンが返されました。この事例では、新しい TLS 接続の検証、再起動時の動作、アプリの自動検証の限界を記録しています。結果は、このネットワークでテストした接続に限られます。

このリポジトリは公式の公開プロジェクト紹介です。公開の質問やドキュメントの提案には [Issues](https://github.com/nonbutAworker/swg-bar/issues) をご利用ください。個別のお問い合わせは [support@swgbar.com](mailto:support@swgbar.com) へ。ライセンスキーや閲覧履歴は公開しないでください。

[SWG bar について](https://swgbar.com/ja/about/) · [プライバシー](https://swgbar.com/ja/privacy/) · [利用規約](https://swgbar.com/ja/terms/)
