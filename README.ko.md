# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · **한국어** · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**HTTPS 복호화·검사를 탐지하세요. 클릭 한 번으로 SWG를 우회하세요.**

[공식 웹사이트](https://swgbar.com/ko/) · [Mac용 다운로드](https://swgbar.com/ko/#pricing) · [가이드](https://swgbar.com/ko/guides/) · [CLI](https://swgbar.com/ko/cli/) · [MCP](https://swgbar.com/ko/mcp/)

SWG bar는 Zscaler, Netskope, Cloudflare Gateway 등 기업용 보안 웹 게이트웨이(SWG)의 **HTTPS/SSL 검사**(`Break-and-Inspect`)를 탐지하고 **원클릭 도메인별 SWG 우회**를 관리할 수 있는 macOS 네이티브 메뉴 막대 앱입니다. Mac에서 도메인 검사 결과와 인증서 근거를 살펴보고, Chrome 확장 프로그램으로 기록된 로컬 결과를 확인하거나, 터미널 및 AI 코딩 에이전트에서 검사와 우회 규칙을 제어할 수 있습니다.

## 주요 기능

- **HTTPS/SSL 검사 및 인증서 근거:** 검사 대상 도메인을 식별하고 인증서 발급자, 유효 기간, SHA-256 지문, 관련 호스트 이름을 확인하며, macOS 키체인 신뢰 평가(MDM으로 배포된 루트 CA 포함)를 공개 루트 인증서 기반의 독립 검증과 비교합니다.
- **원클릭 도메인별 SWG 우회:** 승인된 네트워크에서 선택한 호스트 이름의 연결을 메뉴 막대, CLI 또는 MCP를 통해 게이트웨이 HTTPS 복호화 경로 밖으로 라우팅합니다.
- **Chrome 확장 프로그램 (`2.1.13`):** Mac 앱에 기록된 현재 도메인의 로컬 검사 결과를 브라우저 툴바에서 바로 확인합니다.
- **네이티브 `swgbar` CLI 및 MCP 서버:** 터미널([CLI 가이드](https://swgbar.com/ko/cli/))이나 Claude Desktop, Cursor, Windsurf, Claude Code 등 MCP 호환 AI 에이전트([MCP 가이드](https://swgbar.com/ko/mcp/))에서 검사 지표를 조회하고 온디맨드 TLS 프로브 및 도메인별 우회 규칙을 관리합니다.

탐지 데이터 분석과 저장은 모두 Mac 로컬에서 이루어집니다. 프로브는 별도의 IPv4 TLS 연결을 생성하며, Chrome 확장 프로그램은 읽기 전용으로 Chrome Native Messaging을 통해 기존 로컬 결과를 읽습니다. 자세한 내용은 [작동 원리](https://swgbar.com/ko/how-it-works/), [개인정보 처리방침](https://swgbar.com/ko/privacy/), [확장 프로그램 개인정보 안내](https://swgbar.com/ko/extension-privacy/)를 확인하세요.

## 시작하기

**macOS 14 이상 및 Apple Silicon Mac**(`arm64`)이 필요합니다. 무료 체험은 신용카드 등록 없이 **실제로 사용한 14일**을 기준으로 제공되며, 개인 및 팀 요금제는 [공식 웹사이트](https://swgbar.com/ko/#pricing)에서 확인할 수 있습니다.

1. [공식 웹사이트](https://swgbar.com/ko/#pricing)에서 서명 및 공증된 `.pkg` 설치 파일(`2.4.12`, 빌드 `42`)을 다운로드하고 [설치 가이드](https://swgbar.com/ko/install/)를 따르세요.
2. 메뉴 막대에서 SWG bar를 열고 **개요**, **도메인**, **인증서** 탭에서 호스트 이름, 루트 CA 및 도메인별 SWG 우회 설정을 확인하세요.
3. 필요한 경우 [Chrome 확장 프로그램](https://swgbar.com/ko/chrome-extension/), [`swgbar` CLI](https://swgbar.com/ko/cli/), 또는 AI 클라이언트용 [MCP 서버](https://swgbar.com/ko/mcp/)를 연결하세요.

Mac 앱 `2.4.12`와 함께 제공되는 Chrome 확장 프로그램 `2.1.13`은 웹사이트의 12개 언어를 모두 지원합니다. Chrome 웹 스토어 업데이트는 별도 심사를 거쳐 배포되므로 스토어에 표시된 버전을 확인하세요.

## 가이드: HTTPS 검사, SWG 우회 및 CLI·AI 인증서 오류 해결

macOS에서 HTTPS 검사와 우회 방법을 검토할 때는 **네트워크 경로 변경**과 **TLS 복호화 예외**를 구분해야 합니다. SWG 우회는 호스트 이름의 연결 경로를 바꾸는 것이며, 게이트웨이의 TLS 검사 예외는 트래픽이 복호화 없이 게이트웨이를 그대로 통과하도록 둘 수 있으므로 공개 인증서 체인만으로는 경로 변경을 단정할 수 없습니다.

- [Mac에서 HTTPS 및 SSL 검사를 확인하는 방법](https://swgbar.com/ko/guides/detect-https-inspection/) — macOS에서 인증서 체인과 로컬 루트 CA를 검증하는 방법.
- [Mac의 기업용 SWG 및 MDM HTTPS 검사 원리](https://swgbar.com/ko/guides/enterprise-swg-https-inspection-macos/) — Zscaler, Netskope, Cloudflare Gateway 환경에서 MDM 루트 CA로 인해 브라우저 자물쇠 아이콘이 그대로 표시되는 이유.
- [Mac에서 SWG를 우회하는 방법](https://swgbar.com/ko/guides/how-to-bypass-swg/) — 도메인별 우회 설정 절차, macOS 네트워크 확장 승인, 재시작 동작 및 네트워크 조건.
- [SWG 우회와 TLS 검사 예외(Break-and-Inspect) 비교](https://swgbar.com/ko/guides/swg-bypass-vs-tls-exception/) — 도메인별 라우팅과 게이트웨이 복호화 예외 설정의 구조적 차이.
- [Mac의 CLI 및 AI 도구에서 발생하는 SWG TLS/SSL 인증서 오류 해결](https://swgbar.com/ko/guides/swg-tls-certificate-errors-macos/) — `git`, `npm`, `Python`, `Claude Code`, `Cursor`에서 발생하는 `CERTIFICATE_VERIFY_FAILED` 및 로컬 발급자 오류 해결 방법.

**릴리스 상태 (2026년 11월 18일 확인):** 현재 공개 버전은 **SWG bar 2.4.12**(빌드 `42`)로, 도메인별 SWG 우회를 위한 서명된 네이티브 네트워크 확장, `swgbar` CLI 및 MCP 서버, Chrome 확장 프로그램 `2.1.13`을 포함합니다. 패키지 SHA-256 체크섬, Apple 코드 서명 및 공증 검증을 완료했습니다. [릴리스 정보](https://swgbar.com/ko/releases/)와 [공식 가이드](https://swgbar.com/ko/guides/)를 참고하세요.

## 질문과 피드백

이 저장소는 공식 공개 프로젝트 소개입니다. 공개 질문이나 문서 제안은 [Issues](https://github.com/nonbutAworker/swg-bar/issues)를 이용하세요. 설치, 주문 또는 비공개 문의는 [support@swgbar.com](mailto:support@swgbar.com)으로 보내 주세요. 라이선스 키나 방문 기록은 공개하지 마세요.

[SWG bar 소개](https://swgbar.com/ko/about/) · [개인정보 처리방침](https://swgbar.com/ko/privacy/) · [확장 프로그램 개인정보 안내](https://swgbar.com/ko/extension-privacy/) · [이용약관](https://swgbar.com/ko/terms/)
