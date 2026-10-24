# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · **繁體中文** · [Bahasa Indonesia](README.id.md)

[官方網站](https://swgbar.com/zh-TW/) · [下載 Mac 版](https://swgbar.com/zh-TW/#pricing) · [使用指南](https://swgbar.com/zh-TW/guides/)

SWG bar 是一款原生 macOS 選單列應用程式，協助你了解安全 Web 閘道（SWG）對 HTTPS 流量的解密檢查。在 Mac 上查看網域結果與憑證證據，也能透過配套 Chrome 擴充功能查看既有的本機偵測結果。

## 主要功能

- 搜尋已觀測的網域，查看最近一次探測結果。
- 檢查憑證簽發者、有效期限、指紋及相關網域。
- 比較 macOS 憑證信任與獨立的公開根憑證驗證，了解偵測分類的依據。
- 在 Chrome 工具列查看 Mac 應用程式已儲存的網域結果。

偵測資料在 Mac 本機分析與儲存。探測會建立獨立的 TLS 連線；擴充功能讀取既有的本機結果。詳細說明請見[運作原理](https://swgbar.com/zh-TW/how-it-works/)與[隱私說明](https://swgbar.com/zh-TW/privacy/)。

## 開始使用

需要 **macOS 14 或更新版本，以及 Apple 晶片 Mac**。免費試用依**實際使用的 14 天**計算，目前方案以官網為準。

1. 從[官網](https://swgbar.com/zh-TW/#pricing)下載目前的安裝套件，依照[安裝指南](https://swgbar.com/zh-TW/install/)完成設定。
2. 從選單列開啟 SWG bar，查看網域及相關憑證。
3. 如需在瀏覽器中查看結果，請依照 [Chrome 擴充功能指南](https://swgbar.com/zh-TW/chrome-extension/)完成連接。

Mac 應用程式支援英語、簡體中文、繁體中文、日語及韓語。Mac 應用程式 2.3.7 隨附的 Chrome 擴充功能 2.1.13 支援官網全部 12 種語言。Chrome 商店更新需另行審核後發布，請以商店顯示的版本為準。

## 如何繞過 SWG：區分路由與 TLS 解密例外

繞過 SWG 意味著連線採用不同的網路路徑。TLS 解密例外則可能讓流量繼續經過閘道，但不在閘道解密。因此，僅看到公開憑證鏈，並不能證明流量繞過了閘道。

閱讀 [SWG 繞過與 TLS 解密例外的差異](https://swgbar.com/zh-TW/guides/swg-bypass-vs-tls-exception/)及 [HTTPS 偵測指南](https://swgbar.com/zh-TW/guides/detect-https-inspection/)，了解應檢查哪些證據。

**2026 年 10 月 24 日核驗**：目前正式安裝套件為 2.3.7，一鍵網域繞過預計於 2.4.0 上線。經核驗的版本操作說明請以[版本資訊](https://swgbar.com/zh-TW/releases/)及[官方指南](https://swgbar.com/zh-TW/guides/)為準。

## 實際測量與回饋

[憑證檢查案例](https://swgbar.com/zh-TW/guides/certificate-check-case-study/)記錄了 `swgbar.com:443` 的測量時間、可重複執行的 OpenSSL 指令、macOS 信任結果，以及使用 SWG bar 檢查程式碼進行的獨立觀測。這些結果僅描述受測連線，不能據此認定已繞過閘道。

這裡是專案的官方公開介紹儲存庫。公開問題與文件建議可提交至 [Issues](https://github.com/nonbutAworker/swg-bar/issues)。安裝、訂單或其他私人問題請聯絡 [support@swgbar.com](mailto:support@swgbar.com)。請勿在公開問題中放入授權金鑰或瀏覽紀錄。

[關於 SWG bar](https://swgbar.com/zh-TW/about/) · [隱私說明](https://swgbar.com/zh-TW/privacy/) · [服務條款](https://swgbar.com/zh-TW/terms/)
