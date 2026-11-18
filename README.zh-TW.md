# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · **繁體中文** · [Bahasa Indonesia](README.id.md)

**看清哪些網域被解密。一鍵繞過 SWG。**

[官方網站](https://swgbar.com/zh-TW/) · [下載 Mac 版](https://swgbar.com/zh-TW/#pricing) · [使用指南](https://swgbar.com/zh-TW/guides/) · [CLI](https://swgbar.com/zh-TW/cli/) · [MCP](https://swgbar.com/zh-TW/mcp/)

SWG bar 是一款原生 macOS 選單列應用程式，用於偵測企業安全 Web 閘道（SWG，如 Zscaler、Netskope、Cloudflare Gateway）執行的 **HTTPS/SSL 解密檢查**（Break-and-Inspect），並支援**一鍵依網域繞過 SWG**。你可以在 Mac 上檢視網域偵測結果與憑證證據，透過配套 Chrome 擴充功能在瀏覽器工具列查看已記錄的本機結果，或直接在終端機與 AI 程式開發代理中查詢狀態並管理網域規則。

## 主要功能

- **HTTPS/SSL 檢查與憑證證據**：識別受解密檢查的網域，檢查憑證簽發者、有效期限、SHA-256 指紋與關聯主機名稱，並將 macOS 鑰匙圈信任結果（含透過 MDM 部署的企業根憑證）與獨立的公開根憑證驗證進行比較。
- **一鍵單網域 SWG 繞過**：在獲授權的網路環境中，透過選單列、CLI 或 MCP 為指定主機名稱啟用繞過，使連線不經閘道 HTTPS 解密。
- **Chrome 配套擴充功能（`2.1.13`）**：在瀏覽器工具列直接查看 Mac 應用程式已記錄的目前網域本機偵測結果。
- **原生 `swgbar` CLI 與 MCP 伺服器**：在終端機（[CLI 使用指南](https://swgbar.com/zh-TW/cli/)）或 Claude Desktop、Cursor、Windsurf、Claude Code 等支援 MCP 的 AI 用戶端（[MCP 使用指南](https://swgbar.com/zh-TW/mcp/)）中查詢檢查統計、執行即時 TLS 探測並切換單網域繞過規則。

偵測資料均在 Mac 本機分析與儲存。探測會建立獨立的出站 IPv4 TLS 連線；Chrome 擴充功能為唯讀模式，透過 Chrome Native Messaging 讀取既有的本機結果。詳細說明請見[運作原理](https://swgbar.com/zh-TW/how-it-works/)、[隱私說明](https://swgbar.com/zh-TW/privacy/)與[擴充功能隱私說明](https://swgbar.com/zh-TW/extension-privacy/)。

## 開始使用

需要 **macOS 14 或更新版本，以及 Apple 晶片 Mac**（`arm64`）。免費試用無需信用卡，依**實際使用的 14 天**計算；個人版與團隊版方案請以[官方網站](https://swgbar.com/zh-TW/#pricing)為準。

1. 從[官方網站](https://swgbar.com/zh-TW/#pricing)下載已簽署並通過公證的 `.pkg` 安裝套件（`2.4.12`，組建 `42`），依照[安裝指南](https://swgbar.com/zh-TW/install/)完成設定。
2. 從選單列開啟 SWG bar，在**概覽**、**網域**與**憑證**中檢視主機名稱、根憑證（Root CA）與單網域繞過控制項。
3. 可依需求連線 [Chrome 擴充功能](https://swgbar.com/zh-TW/chrome-extension/)、設定 [`swgbar` CLI](https://swgbar.com/zh-TW/cli/)，或在 AI 用戶端中註冊 [MCP 伺服器](https://swgbar.com/zh-TW/mcp/)。

Mac 應用程式 `2.4.12` 與隨附的 Chrome 擴充功能 `2.1.13` 均支援官網全部 12 種語言。Chrome 線上應用程式商店的更新須經另行審核後發布，請以商店顯示的版本為準。

## 指南：HTTPS 檢查、SWG 繞過與 CLI/AI 憑證錯誤排解

在 macOS 上排解 HTTPS 解密檢查或研究如何繞過 SWG 時，請先區分**網路路由變更**與 **TLS 解密例外**。繞過 SWG 是讓目標主機名稱改走不經閘道解密的路徑；而管理員設定的 TLS 解密例外可能讓流量繼續通過閘道但不進行解密，因此僅看到公開憑證鏈並不能單獨證明路由已改變。

- [如何在 Mac 上偵測 HTTPS 與 SSL 檢查](https://swgbar.com/zh-TW/guides/detect-https-inspection/) — 在 macOS 上驗證 TLS 憑證鏈與本機根憑證。
- [Mac 上的企業 SWG 與 MDM HTTPS 解密檢查解析](https://swgbar.com/zh-TW/guides/enterprise-swg-https-inspection-macos/) — 解析 Zscaler、Netskope、Cloudflare Gateway 搭配 MDM 根憑證時瀏覽器仍顯示正常鎖頭圖示的原因。
- [如何在 Mac 上繞過 SWG](https://swgbar.com/zh-TW/guides/how-to-bypass-swg/) — 單網域繞過設定步驟、macOS 網路延伸功能核准、重新啟動行為與網路條件限制。
- [SWG 繞過與 TLS 解密例外（Break-and-Inspect）對比](https://swgbar.com/zh-TW/guides/swg-bypass-vs-tls-exception/) — 區分單網域路徑切換與閘道端不解密放行規則。
- [修復 Mac 終端機 CLI 與 AI 工具中的 SWG TLS/SSL 憑證錯誤](https://swgbar.com/zh-TW/guides/swg-tls-certificate-errors-macos/) — 排解 `git`、`npm`、`Python`、`Claude Code`、`Cursor` 中的 `CERTIFICATE_VERIFY_FAILED` 與本機簽發者憑證錯誤。

**2026 年 11 月 18 日核驗**：目前正式發布版本為 **SWG bar 2.4.12**（組建 `42`），內建已簽署的原生網路延伸功能（支援依網域繞過 SWG）、`swgbar` CLI 與 MCP 伺服器，以及隨附 Chrome 配套擴充功能 `2.1.13`。安裝套件 SHA-256 校驗碼、Apple 程式碼簽章與公證均已核驗。詳見[版本資訊](https://swgbar.com/zh-TW/releases/)和[官方指南](https://swgbar.com/zh-TW/guides/)。

## 問題與回饋

這裡是專案的官方公開介紹儲存庫。公開問題與文件建議可提交至 [Issues](https://github.com/nonbutAworker/swg-bar/issues)。安裝、訂單或其他私人問題請聯絡 [support@swgbar.com](mailto:support@swgbar.com)。請勿在公開問題中放入授權金鑰或瀏覽紀錄。

[關於 SWG bar](https://swgbar.com/zh-TW/about/) · [隱私說明](https://swgbar.com/zh-TW/privacy/) · [擴充功能隱私說明](https://swgbar.com/zh-TW/extension-privacy/) · [服務條款](https://swgbar.com/zh-TW/terms/)
