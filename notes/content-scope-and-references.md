# 집필 범위와 참고자료 맵

> 공개 본문이 아니라 집필할 때 참고하는 내부 문서다. 어떤 내용을 직접 쓰고 어떤 내용을 외부 자료로 넘길지 정리한다.

2026-08-14: AI를 별도 장으로 다루지 않고 프로젝트 공동체에 참여하는 태도와 정책 사례에 통합했다.

## 기본 원칙

- 이 가이드는 OSS 전반을 설명하는 교과서가 아니라 모임 참가자가 첫 코드 기여를 시도할 때 쓰는 안내서다.
- 모임의 목표, 판단 기준, 체크리스트처럼 이 프로젝트에만 있는 내용은 직접 쓴다.
- 일반 개념, GitHub 조작법, 법률적인 세부 사항은 짧게 요약하고 신뢰할 수 있는 원문으로 보낸다.
- 외부 가이드보다 해당 프로젝트의 `README`, `CONTRIBUTING`, `SECURITY`, 행동 강령, AI 정책이 우선한다.
- 링크만 나열하지 않고, 무엇을 확인하기 위한 자료인지 한 문장으로 설명한다.
- 정책과 화면은 바뀔 수 있으므로 사례와 정책에는 확인 날짜를 남긴다.

## 모임에서 우선 다룰 내용

수요조사 9명의 응답을 개인 식별 정보 없이 집계했다.

| 주제 | 응답 수 | 처리 |
|---|---:|---|
| 기여 문화와 태도 | 6 | 2.4와 3장에서 직접 설명 |
| 프로젝트 선택 기준 | 5 | 4.1에서 직접 설명 |
| 첫 이슈·작업 선택 | 4 | 4.1에서 직접 설명 |
| AI 기준과 주의점 | 3 | 3.2에서 문제를, 3.3에서 정책 사례를 설명 |
| 대규모 코드베이스 파악 | 2 | 4.2에 짧은 체크리스트 제공 |
| 장기적인 기여 | 2 | 5장에서 선택지로 제시 |
| 프로젝트별 절차 | 2 | 2.4와 4.1에 확인 목록 제공 |
| 코드 수정과 테스트 | 1 | 4.2에 검증 기준 제공 |

원본 CSV와 설문 화면에는 이메일, 이름, 얼굴, 자유응답이 포함되어 있으므로 공개하지 않는다.

## 현재 목차의 축약 방향

아래의 `직접`도 장문을 뜻하지 않는다. 모임에서 판단에 쓸 수 있는 짧은 설명이나 체크리스트면 충분하다.

| 범위 | 처리 | 넘길 자료 |
|---|---|---|
| 1.1 이 가이드의 대상과 목표 | 직접 | 없음. 추천 독자, 필요한 사전 지식, 코드 기여의 범위와 `검토 가능한 PR 제출`은 이 가이드의 기준이다. |
| 1.2 기여를 시작하기 전에 | 직접 | 일반적인 동기와 장점은 [Open Source Guides](https://opensource.guide/ko/how-to-contribute/)로 보낼 수 있다. |
| 1.3 저자와 이 글의 관점 | 직접 | 저자의 [GitHub 프로필](https://github.com/YangSiJun528)과 공개 가능한 기여 사례만 사용한다. |
| 1.4 이 가이드를 읽는 방법 | 합치기 | 1장 첫 페이지나 책 첫 페이지에 넣는다. |
| 2.1 OSS와 FOSS | 요약+링크 | [OSI의 Open Source Definition](https://opensource.org/osd), [FSF의 자유 소프트웨어 정의](https://www.gnu.org/philosophy/free-sw.ko.html) |
| 2.2 라이선스 | 요약+링크 | [Choose a License의 라이선스 없음 안내](https://choosealicense.com/ko/no-permission/), [DCO 1.1](https://developercertificate.org/) |
| 2.3 사람과 조직 | 요약+링크 | 공통 역할만 소개하고 실제 권한은 각 프로젝트의 거버넌스 문서를 확인하게 한다. |
| 2.4 프로젝트 문화 | 직접 | GitHub 외의 방식과 최근 Issue·PR, 공식 채널에서 실제 규칙을 확인하는 방법을 다룬다. |
| 3.1 공동체에 참여한다는 것 | 직접 | 변경 제출 외에도 사용, 문제 제기, 운영과 후원이 참여가 될 수 있음을 설명한다. |
| 3.2 공동체를 고려하지 않은 기여 | 직접 | 검토·유지 비용과 AI가 같은 문제를 쉽게 만든 사례를 함께 설명한다. |
| 3.3 프로젝트마다 다른 AI 사용 규칙 | 사례 중심 | CPython·Linux·Fedify, Rust, OpenJDK·QEMU를 AI 생성 기여의 허용 범위에 따른 유형별 사례로 소개하고 Zig는 더 강경한 사례로 다룬다. |
| 3.4 기여할 때 가져갈 태도 | 직접 | 프로젝트 존중, 검증, 대화와 떠날 수 있다는 점을 정리한다. |
| 4.1 계속할 이유가 있는 프로젝트에서 명확한 첫 작업을 고른다 | 세 글을 합치기 | 프로젝트 선택, 기여 방식 확인, 첫 작업 선택을 한 흐름으로 설명한다. [GitHub에서 기여할 곳 찾기](https://docs.github.com/ko/get-started/exploring-projects-on-github/finding-ways-to-contribute-to-open-source-on-github)를 보충 자료로 둔다. |
| 4.2 문제를 재현하고 필요한 변경만 구현·검증한다 | 세 글을 합치기 | 문제 재현과 이해, 필요한 변경, 테스트, 제출 전 diff 검토를 한 흐름으로 설명한다. |
| 4.3 검토자가 판단할 수 있는 PR을 제출하고 근거로 리뷰에 응답한다 | 두 글을 합치기 | PR에 들어갈 정보와 “검토 가능” 기준만 쓰고 기능 설명은 [GitHub PR 문서](https://docs.github.com/ko/pull-requests/get-started/about-pull-requests)와 [리뷰 문서](https://docs.github.com/ko/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews)로 보낸다. |
| 5.1 PR 결과 | 직접 | 병합 여부와 이 가이드의 목표 달성을 분리해 설명한다. |
| 5.2 경험 정리 | 직접 | 모임에서 공유할 짧은 회고 양식을 둔다. |
| 6.1 후원과 인증 | 직접 | 후원처 선정 기준과 인증 방법을 다루고, 일반적인 OSS 규칙이 아니라 모임 참가 규칙임을 명시한다. |
| 이 가이드 개선 안내 | 섹션 첫 페이지로 합치기 | 실제 `CONTRIBUTING.md`가 생기면 그 파일로 보낸다. |
| 추천 자료 | 링크 중심 | 독자가 사용할 핵심 자료와 한 줄 설명만 둔다. |
| 라이선스 | 직접 | 이 저장소의 콘텐츠·예제 코드·외부 자료의 라이선스를 구분해 명시한다. |

AI 관련 넓은 사례 메모는 공개 목차에서 제외하고 `notes/oss-ai-case-notes.md`에 보관한다. 본문에는 공동체와 기여자의 태도에 직접 필요한 내용만 남긴다.

## 외부로 넘기기 좋은 핵심 자료

### 전체 흐름

- [오픈소스에 기여하는 방법](https://opensource.guide/ko/how-to-contribute/): 역할, 프로젝트 선택, 의사소통, Issue·PR, 제출 후 결과까지 한 번에 다룬다. 2~6장의 일반론을 가장 많이 넘길 수 있다.
- [네이버 오픈소스 가이드](https://naver.github.io/OpenSourceGuide/book/): 한국어로 OSS 개념, 라이선스, 기여 절차를 폭넓게 설명한다. 오래된 GitHub 화면이나 절차는 최신 공식 문서와 함께 확인한다.
- [Producing Open Source Software](https://producingoss.com/): 프로젝트 운영, 의사소통, 거버넌스를 더 깊게 보고 싶은 독자용 무료 영문 도서다.
- 『오픈 소스로 미래를 연마하라』(VM 브라수어): 기여 생태계와 참여 과정을 길게 보고 싶은 독자에게 소개한다. 공개 링크는 넣지 않으며, 2019년 책이므로 AI 정책은 별도 자료를 봐야 한다.

### GitHub 작업

- [GitHub에서 OSS에 기여할 방법 찾기](https://docs.github.com/ko/get-started/exploring-projects-on-github/finding-ways-to-contribute-to-open-source-on-github): 관리 중인 프로젝트와 첫 작업을 찾는 최신 GitHub 기능을 확인할 때 사용한다.
- [Pull Request 소개](https://docs.github.com/ko/pull-requests/get-started/about-pull-requests): PR, Draft PR, fork 기반 흐름의 기능 설명을 넘긴다.
- [Pull Request 리뷰 소개](https://docs.github.com/ko/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews): 승인, 변경 요청, 댓글 등 리뷰 기능을 넘긴다.
- [오픈소스 입문을 위한 아주 구체적인 가이드](https://parksb.github.io/article/13.html): 한국어 실습 흐름을 보여 주는 보충 자료다. 2018년 글이라 브랜치 이름과 일부 Git 명령은 그대로 따라 하지 않는다.

### AI 정책과 사례

AI 정책은 프로젝트마다 크게 다르다는 점을 보여 주는 사례로만 사용한다. 이 목록에서 보편 규칙을 도출하지 않는다.

- [Nobody's job, everybody's problem: F/OSS in the age of AI](https://hongminhee.codeberg.page/foss-kaist-cs350/): 유지보수 문제를 기여자 신뢰와 리뷰 용량 문제로 나누고, AI 정책이 어떤 문제를 해결하려는지 구분하는 강의 자료다.
- [Rust LLM 사용 정책](https://forge.rust-lang.org/policies/llm-usage.html): 허용 범위와 책임을 세분화한 정책 사례다.
- [Zig의 strict no-LLM 정책](https://ziglang.org/code-of-conduct/#strict-no-llm-no-ai-policy): 생성, 편집, 번역, 브레인스토밍 등을 폭넓게 금지하는 사례다.
- [Servo의 AI contribution 안내](https://book.servo.org/contributing/getting-started.html#ai-contributions): 제출물 생성은 금지하지만 코드 탐색과 직접 검증한 버그 발견 등은 구분하는 사례다.
- [QEMU의 code provenance 정책](https://www.qemu.org/docs/master/devel/code-provenance.html): 생성물의 출처와 라이선스 위험을 중심으로 한 사례다.
- [Fedify의 AI 정책](https://github.com/fedify-dev/fedify/blob/main/AI_POLICY.md): AI 사용 공개, 사람의 검증과 `Assisted-by` 태그를 요구하는 사례다.
- [HwpLibSharp 포팅 경험](https://devwrite.ai/ko/posts/hwplibsharp-upstream-management/): AI로 언어 포팅을 보조하되 사람이 방향 설정과 도메인 검증을 맡은 사례다.

### 기여와 유지보수 책임

- [Richard Hipp의 공짜 강아지 비유](https://www.youtube.com/watch?v=lSVgeMoXJTs&t=1733s): PR은 코드만 받는 일이 아니라 검토, 테스트, 문서와 장기 유지보수 책임을 함께 인수하는 일이라는 설명이다.

## 공개 자료에 넣지 않을 것

- Gmail 링크와 원치 않는 연락·스팸의 발신자 정보
- 설문 Form, 원본 CSV·ZIP, 응답자의 이메일과 자유응답
- 이름·얼굴·기수 번호가 보이는 Slack 화면
- 이름·프로필 사진이 보이는 카카오톡 화면
- 개인정보나 결제 식별자를 가리지 않은 후원 인증 화면
- 본문을 직접 확인하지 못한 X 게시물과 원문을 찾지 못한 2차 요약

개인 경험을 쓸 때는 공개 저장소·릴리스처럼 누구나 확인할 수 있는 자료를 우선하고, 타인의 개인정보가 들어간 화면은 비식별화한 파생본만 사용한다.

## 사용 보류

다음 항목은 정확한 1차 출처나 대상이 정해지기 전까지 본문에 넣지 않는다.

- RustPython·Fastify의 AI 친화 정책
- Zig rewrite와 Pyre 실험 프로젝트
- 개인 중심에서 기업 중심으로 바뀌었다는 생태계 변화 통계
- Yorkie나 Apache 멤버에게 제공되는 기회·지원 사례

마지막 확인: 2026-08-14
