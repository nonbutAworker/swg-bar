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

Mac 應用程式 2.4.12 與隨附的 Chrome 擴充功能 2.1.13 均支援官網全部 12 種語言。Chrome 商店更新須另行審查後發布，請以商店顯示的版本為準。

## 如何繞過 SWG：區分路由與 TLS 解密例外

繞過 SWG 意味著連線採用不同的網路路徑。TLS 解密例外則可能讓流量繼續經過閘道，但不在閘道解密。因此，僅看到公開憑證鏈，並不能證明流量繞過了閘道。

閱讀 [SWG 繞過與 TLS 解密例外的差異](https://swgbar.com/zh-TW/guides/swg-bypass-vs-tls-exception/)及 [HTTPS 偵測指南](https://swgbar.com/zh-TW/guides/detect-https-inspection/)，了解應檢查哪些證據。

2026 年 11 月 4 日驗證：正式 2.4.12 安裝套件（組建 42）與公布的 SHA-256 一致，並通過 Apple 簽章與公證檢查。本機應用程式及原生網路延伸功能與套件一致，隨附 Chrome 配套擴充功能仍為 2.1.13。實際啟用、關閉、結束與重新啟動測試見下方紀錄。

[逐步操作教學](https://swgbar.com/zh-TW/guides/how-to-bypass-swg/) · [完整實測紀錄與限制](https://swgbar.com/zh-TW/guides/certificate-check-case-study/)

## 實際測量與回饋

[完整實測紀錄與限制](https://swgbar.com/zh-TW/guides/certificate-check-case-study/)

使用 SWG bar 2.4.12 對 `www.doubao.com:443` 進行了六次新連線測試：關閉繞過或結束應用程式時傳回檢查機構簽發的憑證鏈，啟用繞過或重新啟動恢復後傳回公用憑證鏈。案例記錄了新的 TLS 驗證、重新啟動行為與應用程式自動驗證的限制。結果僅適用於本次網路中測試的連線。

這裡是專案的官方公開介紹儲存庫。公開問題與文件建議可提交至 [Issues](https://github.com/nonbutAworker/swg-bar/issues)。安裝、訂單或其他私人問題請聯絡 [support@swgbar.com](mailto:support@swgbar.com)。請勿在公開問題中放入授權金鑰或瀏覽紀錄。

[關於 SWG bar](https://swgbar.com/zh-TW/about/) · [隱私說明](https://swgbar.com/zh-TW/privacy/) · [服務條款](https://swgbar.com/zh-TW/terms/)
