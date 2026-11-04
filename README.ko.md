# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · **한국어** · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

[공식 웹사이트](https://swgbar.com/ko/) · [Mac용 다운로드](https://swgbar.com/ko/#pricing) · [가이드](https://swgbar.com/ko/guides/)

SWG bar는 보안 웹 게이트웨이(SWG)의 HTTPS 검사를 살펴볼 수 있는 macOS 기본 메뉴 막대 앱입니다. Mac에서 도메인 검사 결과와 인증서 정보를 확인하고, Chrome 확장 프로그램에서 저장된 로컬 결과를 볼 수 있습니다.

## 주요 기능

- 관측된 도메인을 검색하고 최근 검사 결과를 확인합니다.
- 인증서 발급자, 유효 기간, 지문, 관련 도메인을 살펴봅니다.
- macOS의 인증서 신뢰 평가를 공개 루트 인증서에 기반한 별도의 검증과 비교합니다.
- Mac 앱에 저장된 도메인 결과를 Chrome 툴바에서 확인합니다.

탐지 데이터는 Mac에서 분석하고 저장합니다. 검사는 별도의 TLS 연결을 생성하며, 확장 프로그램은 기존 로컬 결과를 읽습니다. 자세한 내용은 [작동 방식](https://swgbar.com/ko/how-it-works/)과 [개인정보 처리방침](https://swgbar.com/ko/privacy/)을 확인하세요.

## 시작하기

**macOS 14 이상 및 Apple Silicon Mac**이 필요합니다. 무료 체험은 **실제로 사용한 14일**을 기준으로 합니다. 현재 요금제는 웹사이트에 안내되어 있습니다.

1. [공식 웹사이트](https://swgbar.com/ko/#pricing)에서 설치 파일을 다운로드하고 [설치 가이드](https://swgbar.com/ko/install/)를 따르세요.
2. 메뉴 막대에서 SWG bar를 열고 도메인과 인증서 정보를 확인하세요.
3. 필요한 경우 [Chrome 확장 프로그램](https://swgbar.com/ko/chrome-extension/)을 설정하세요.

Mac 앱 2.4.12와 동봉된 Chrome 확장 2.1.13은 웹사이트의 12개 언어를 모두 지원합니다. Chrome 웹 스토어 업데이트는 별도 심사 후 배포되므로 스토어에 표시된 버전을 확인하세요.

## SWG 우회와 TLS 검사 예외

SWG 우회는 연결의 네트워크 경로를 바꾸는 것입니다. TLS 검사 예외는 트래픽이 게이트웨이를 계속 통과하되 복호화되지 않도록 할 수 있습니다. 공개 인증서 체인이 보인다는 사실만으로 경로가 바뀌었다고 판단할 수는 없습니다.

[SWG 우회와 TLS 검사 예외 비교](https://swgbar.com/ko/guides/swg-bypass-vs-tls-exception/) 및 [HTTPS 검사 확인 가이드](https://swgbar.com/ko/guides/detect-https-inspection/)를 참고하세요.

2026년 11월 4일 검증했습니다. 정식 2.4.12 설치 패키지(빌드 42)는 공개 SHA-256과 일치하며 Apple 서명 및 공증 검사를 통과했습니다. 설치된 앱과 기본 네트워크 확장도 일치하고, 동봉된 Chrome 확장은 2.1.13입니다. 실제 활성화, 비활성화, 종료와 재시작 테스트는 아래 기록을 참고하세요.

[단계별 우회 안내](https://swgbar.com/ko/guides/how-to-bypass-swg/) · [전체 실측 기록과 한계](https://swgbar.com/ko/guides/certificate-check-case-study/)

## 실제 측정과 문의

[전체 실측 기록과 한계](https://swgbar.com/ko/guides/certificate-check-case-study/)

SWG bar 2.4.12로 `www.doubao.com:443`에 새 연결 6개를 만들어 테스트했습니다. 우회를 끄거나 앱을 종료한 상태에서는 검사 기관의 인증서 체인이, 우회를 켜거나 복원한 상태에서는 공개 인증서 체인이 반환되었습니다. 사례에는 새로운 TLS 연결 검사, 재시작 동작, 앱 자동 검증의 한계를 기록했습니다. 결과는 이 네트워크에서 테스트한 연결에 한정됩니다.

이 저장소는 공식 공개 프로젝트 소개입니다. 공개 질문이나 문서 제안은 [Issues](https://github.com/nonbutAworker/swg-bar/issues)를 이용하세요. 비공개 문의는 [support@swgbar.com](mailto:support@swgbar.com)으로 보내 주세요. 라이선스 키나 방문 기록은 공개하지 마세요.

[SWG bar 소개](https://swgbar.com/ko/about/) · [개인정보 처리방침](https://swgbar.com/ko/privacy/) · [이용약관](https://swgbar.com/ko/terms/)
