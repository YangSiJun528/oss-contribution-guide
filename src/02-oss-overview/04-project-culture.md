> 아직 작성 중입니다.

# 프로젝트의 방식과 문화

## OSS에 공통된 한 가지 절차는 없다

GitHub에서 Issue를 고르고 Pull Request를 보내는 방식은 흔하지만 모든 OSS가 이 흐름을 따르지는 않습니다. GitLab의 Merge Request, Gerrit의 Change, 메일링 리스트로 보내는 패치처럼 서로 다른 도구와 절차가 사용됩니다. Issue는 GitHub가 아니라 Jira나 자체 버그 추적기에서 관리할 수도 있습니다.

대표적인 차이는 다음 사례에서 볼 수 있습니다.

- [Linux 커널][linux-kernel-submitting-patches]은 `git`으로 패치를 만들지만, 관련 메인테이너와 메일링 리스트에 패치를 본문으로 보내고 이메일에서 리뷰합니다.
- [Android Open Source Project][aosp-submit-code-changes]는 여러 Git 저장소를 `repo` 도구로 관리하며, 변경을 Gerrit에 올려 패치셋 단위로 검토합니다.
- [Apache 프로젝트][apache-how-it-works]는 개별 도구가 달라도 주요 프로젝트 업무와 의사결정을 공개 메일링 리스트에 기록하는 것을 기본으로 합니다.

이 가이드의 실습 과정은 처음 접하기 쉽고 많은 프로젝트가 사용하는 GitHub의 Issue와 Pull Request를 기준으로 설명합니다. 다른 방식을 사용하는 프로젝트에서는 해당 프로젝트의 안내가 이 가이드보다 우선합니다.

## 주요 문서가 알려주는 것

파일 이름과 위치는 프로젝트마다 다르지만 다음 문서에서 기여에 필요한 정보를 찾을 수 있습니다.

| 문서 | 확인할 내용 |
| --- | --- |
| `README`, 프로젝트 웹사이트 | 프로젝트의 목적, 사용법, 현재 상태와 추가 문서의 위치 |
| `LICENSE`, `COPYING`, `NOTICE` | 코드를 사용·수정·배포할 수 있는 조건과 필요한 고지 |
| `CONTRIBUTING`, 스타일 가이드 | 개발 환경, 테스트, 커밋, Issue와 PR 제출 방식 |
| `CODE_OF_CONDUCT` | 기대하는 행동, 금지되는 행동과 신고 방법 |
| `GOVERNANCE`, `MAINTAINERS`, `OWNERS` | 역할, 검토 권한과 의사결정 방식 |
| `SECURITY` | 취약점을 공개하지 않고 안전하게 신고하는 방법 |
| `CHANGELOG`, 릴리스 노트, 로드맵 | 최근 변화와 프로젝트가 향하는 방향 |

## 실제 문화 확인하기

도구가 같아도 문화는 다를 수 있습니다. 어떤 프로젝트는 작은 수정도 먼저 Issue에서 합의하기를 원하고, 어떤 프로젝트는 바로 PR을 받습니다. 응답에 며칠 또는 몇 달이 걸릴 수도 있고, 리뷰의 엄격함과 설명 방식도 다릅니다.

문서가 있다는 사실만으로 실제 운영까지 보장되지는 않습니다. `CONTRIBUTING`이 오래되어 현재 절차와 다를 수도 있고, 행동강령에 신고 방법이 있어도 실제로 집행되지 않을 수도 있습니다. 문서와 함께 최근 Issue·PR·메일링 리스트에서 질문과 의견 충돌을 어떻게 다루는지 확인합니다.

Discord나 Slack에서 나눈 대화가 있더라도 최종 결정이 Issue, 메일링 리스트, RFC 같은 공식 기록에 남는 프로젝트라면 그 기록을 기준으로 삼아야 합니다.

AI 사용에 대한 입장도 프로젝트 문화의 일부입니다. 관련 정책을 확인하는 방법과 사례는 [AI와 OSS 기여](../05-ai-and-oss/00-index.md)에서 별도로 다룹니다.

## 더 보기

- [오픈소스에 기여하는 방법][open-source-guide]: 일반적인 프로젝트 구조와 의사소통 방식
- [Producing Open Source Software][producing-open-source-software]: 프로젝트 운영과 커뮤니케이션을 깊게 다루는 무료 영문 도서

{{#include ../_includes/references.md}}
