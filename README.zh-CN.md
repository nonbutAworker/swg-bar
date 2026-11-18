# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · **简体中文** · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**看清哪些域名被解密。一键绕过 SWG。**

[官方网站](https://swgbar.com/zh-CN/) · [下载 Mac 版](https://swgbar.com/zh-CN/#pricing) · [使用指南](https://swgbar.com/zh-CN/guides/) · [CLI](https://swgbar.com/zh-CN/cli/) · [MCP](https://swgbar.com/zh-CN/mcp/)

SWG bar 是一款原生 macOS 菜单栏应用，用于检测企业安全 Web 网关（SWG，如 Zscaler、Netskope、Cloudflare Gateway）执行的 **HTTPS/SSL 解密检查**（Break-and-Inspect），并支持**一键按域名绕过 SWG**。你可以在 Mac 上核查域名检测结果与证书证据，通过配套 Chrome 扩展在浏览器工具栏查看已记录的本地结果，或直接在终端与 AI 编程代理中查询状态并管理域名规则。

## 主要功能

- **HTTPS/SSL 检查与证书证据**：识别被解密检查的域名，查看证书颁发者、有效期、SHA-256 指纹及关联主机名，并将 macOS 钥匙串信任结果（含 MDM 下发的企业根证书）与独立的公共根证书验证进行对比。
- **一键单域名 SWG 绕过**：在获授权的网络环境中，通过菜单栏、CLI 或 MCP 为选定主机名启用绕过，使连接不再经过网关 HTTPS 解密。
- **Chrome 配套扩展（`2.1.13`）**：在浏览器工具栏中直接查看 Mac 应用已记录的当前域名本地检测结果。
- **原生 `swgbar` CLI 与 MCP 服务**：在终端（[CLI 使用指南](https://swgbar.com/zh-CN/cli/)）或 Claude Desktop、Cursor、Windsurf、Claude Code 等支持 MCP 的 AI 客户端（[MCP 使用指南](https://swgbar.com/zh-CN/mcp/)）中查询检查统计、发起按需 TLS 探测并切换单域名绕过规则。

检测数据均在 Mac 本地分析与存储。探测会建立独立的出站 IPv4 TLS 连接；Chrome 扩展为只读模式，通过 Chrome Native Messaging 读取已有的本地结果。详细说明见[工作原理](https://swgbar.com/zh-CN/how-it-works/)、[隐私说明](https://swgbar.com/zh-CN/privacy/)和[扩展隐私说明](https://swgbar.com/zh-CN/extension-privacy/)。

## 开始使用

需要 **macOS 14 或更高版本，以及 Apple 芯片 Mac**（`arm64`）。免费试用无需绑定信用卡，按**实际使用的 14 天**计算；个人版与团队版方案以[官方网站](https://swgbar.com/zh-CN/#pricing)为准。

1. 从[官方网站](https://swgbar.com/zh-CN/#pricing)下载已签名并完成公证的 `.pkg` 安装包（`2.4.12`，构建 `42`），按照[安装指南](https://swgbar.com/zh-CN/install/)完成设置。
2. 从菜单栏打开 SWG bar，在**概览**、**域名**和**证书**中查看主机名、根证书（Root CA）与单域名绕过控件。
3. 可按需连接 [Chrome 配套扩展](https://swgbar.com/zh-CN/chrome-extension/)、配置 [`swgbar` CLI](https://swgbar.com/zh-CN/cli/)，或在 AI 客户端中接入 [MCP 服务](https://swgbar.com/zh-CN/mcp/)。

Mac 应用 `2.4.12` 及随附的 Chrome 扩展 `2.1.13` 均支持官网全部 12 种语言。Chrome 应用商店更新需经单独审核后发布，请以商店显示的版本为准。

## 指南：HTTPS 检查、SWG 绕过与 CLI/AI 证书错误排查

在 macOS 上排查 HTTPS 解密检查或研究如何绕过 SWG 时，请先区分**网络路由变化**与 **TLS 解密例外**。绕过 SWG 是让目标主机名的连接走不经网关解密的路径；而管理员配置的 TLS 解密例外可能让流量继续穿过网关但不予解密，因此仅看到公共证书链并不能单独证明路由已改变。

- [如何在 Mac 上检测 HTTPS 与 SSL 检查](https://swgbar.com/zh-CN/guides/detect-https-inspection/) — 在 macOS 上核验 TLS 证书链与本地根证书。
- [Mac 上的企业 SWG 与 MDM HTTPS 解密检查解析](https://swgbar.com/zh-CN/guides/enterprise-swg-https-inspection-macos/) — 解析 Zscaler、Netskope、Cloudflare Gateway 配合 MDM 根证书时浏览器依然显示正常锁图标的原因。
- [如何在 Mac 上绕过 SWG](https://swgbar.com/zh-CN/guides/how-to-bypass-swg/) — 单域名绕过设置步骤、macOS 网络扩展授权、重启恢复机制与网络边界说明。
- [SWG 绕过与 TLS 解密例外（Break-and-Inspect）对比](https://swgbar.com/zh-CN/guides/swg-bypass-vs-tls-exception/) — 区分单域名路径切换与网关侧不解密放行规则。
- [修复 Mac 终端 CLI 与 AI 工具中的 SWG TLS/SSL 证书错误](https://swgbar.com/zh-CN/guides/swg-tls-certificate-errors-macos/) — 解决 `git`、`npm`、`Python`、`Claude Code`、`Cursor` 中的 `CERTIFICATE_VERIFY_FAILED` 与本地颁发者证书报错。

**2026 年 11 月 18 日核验**：当前正式发布版本为 **SWG bar 2.4.12**（构建 `42`），内置已签名的原生网络扩展（支持按域名绕过 SWG）、`swgbar` CLI 与 MCP 服务，以及随附 Chrome 配套扩展 `2.1.13`。安装包 SHA-256 校验和、Apple 代码签名与公证均已核验。详见[版本信息](https://swgbar.com/zh-CN/releases/)和[官方指南](https://swgbar.com/zh-CN/guides/)。

## 问题与反馈

这里是项目的官方公开介绍仓库。公开问题和文档建议可以提交到 [Issues](https://github.com/nonbutAworker/swg-bar/issues)。安装、订单或其他私密问题请联系 [support@swgbar.com](mailto:support@swgbar.com)。请勿在公开问题中放入许可证密钥或浏览历史。

[关于 SWG bar](https://swgbar.com/zh-CN/about/) · [隐私说明](https://swgbar.com/zh-CN/privacy/) · [扩展隐私说明](https://swgbar.com/zh-CN/extension-privacy/) · [服务条款](https://swgbar.com/zh-CN/terms/)
