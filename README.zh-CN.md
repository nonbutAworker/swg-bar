# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · **简体中文** · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

[官方网站](https://swgbar.com/zh-CN/) · [下载 Mac 版](https://swgbar.com/zh-CN/#pricing) · [使用指南](https://swgbar.com/zh-CN/guides/)

SWG bar 是一款原生 macOS 菜单栏应用，帮助你了解安全 Web 网关（SWG）对 HTTPS 流量的解密检查。在 Mac 上查看域名结果和证书证据，也可以通过配套 Chrome 扩展查看已有的本地检测结果。

## 主要功能

- 搜索已观测的域名，查看最近一次探测结果。
- 检查证书颁发者、有效期、指纹及其关联域名。
- 对比 macOS 证书信任与独立的公共根证书验证，查看检测分类的依据。
- 在 Chrome 工具栏中查看 Mac 应用已保存的域名结果。

检测数据在 Mac 本地分析和存储。探测会建立独立的 TLS 连接；扩展读取已有的本地结果。详细说明见[工作原理](https://swgbar.com/zh-CN/how-it-works/)和[隐私说明](https://swgbar.com/zh-CN/privacy/)。

## 开始使用

需要 **macOS 14 或更高版本，以及 Apple 芯片 Mac**。免费试用按**实际使用的 14 天**计算，当前方案以官网为准。

1. 从[官网](https://swgbar.com/zh-CN/#pricing)下载当前安装包，按照[安装指南](https://swgbar.com/zh-CN/install/)完成设置。
2. 从菜单栏打开 SWG bar，查看域名及相关证书。
3. 如需在浏览器中查看结果，按照 [Chrome 扩展指南](https://swgbar.com/zh-CN/chrome-extension/)连接扩展。

Mac 应用支持英语、简体中文、繁体中文、日语和韩语。Mac 应用 2.3.7 随附的 Chrome 扩展 2.1.13 支持官网全部 12 种语言。Chrome 商店更新需另行审核后发布，请以商店显示的版本为准。

## 如何绕过 SWG：先区分路由与 TLS 解密例外

绕过 SWG 意味着连接采用了不同的网络路径。TLS 解密例外则可能让流量继续经过网关，但不在网关处解密。因此，仅看到公共证书链，并不能证明流量绕过了网关。

阅读 [SWG 绕过与 TLS 解密例外的区别](https://swgbar.com/zh-CN/guides/swg-bypass-vs-tls-exception/)和 [HTTPS 检测指南](https://swgbar.com/zh-CN/guides/detect-https-inspection/)，了解应当查看哪些证据。

**2026 年 10 月 24 日核验**：当前正式安装包为 2.3.7，一键域名绕过计划在 2.4.0 上线。经核验的版本操作说明以[版本信息](https://swgbar.com/zh-CN/releases/)和[官方指南](https://swgbar.com/zh-CN/guides/)为准。

## 真实测量与反馈

[证书检查案例](https://swgbar.com/zh-CN/guides/certificate-check-case-study/)记录了对 `swgbar.com:443` 的测量时间、可重复执行的 OpenSSL 命令、macOS 信任结果，以及使用 SWG bar 检测代码进行的独立观测。这些结果只描述被测连接，不能据此认定已经绕过网关。

这里是项目的官方公开介绍仓库。公开问题和文档建议可以提交到 [Issues](https://github.com/nonbutAworker/swg-bar/issues)。安装、订单或其他私密问题请联系 [support@swgbar.com](mailto:support@swgbar.com)。请勿在公开问题中放入许可证密钥或浏览历史。

[关于 SWG bar](https://swgbar.com/zh-CN/about/) · [隐私说明](https://swgbar.com/zh-CN/privacy/) · [服务条款](https://swgbar.com/zh-CN/terms/)
